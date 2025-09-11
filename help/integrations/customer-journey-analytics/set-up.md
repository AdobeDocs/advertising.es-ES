---
title: Configuración de la recopilación de datos, la transferencia de datos y la creación de informes
description: Obtenga información sobre cómo configurar la recopilación de datos, la transferencia de datos y la creación de informes.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 222f04c9e3c6e8af2ad7dbabcba234008dd14606
workflow-type: tm+mt
source-wordcount: '1801'
ht-degree: 0%

---

# Configuración de la recopilación de datos, la transferencia de datos y la creación de informes

*característica de Beta*

Se requieren las siguientes tareas para ver los datos de Advertising Cloud en Customer Journey Analytics.

1. (Analista web de su organización; opcional) [Recopilar datos históricos para los ID de AMO e ID de EF](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Este paso solo es aplicable a los anunciantes con [!DNL Analytics for Advertising].

1. (Administrador del sitio de su organización para Adobe Experience Platform) [Configure la recopilación de datos en Experience Platform e implemente etiquetas de seguimiento de conversión](#data-collection).

1. (Administrador del sitio de su organización para Customer Journey Analytics) [Cree una conexión con los conjuntos de datos de Experience Platform en Customer Journey Analytics](#dataset-connection).

1. (Analista web de su organización) [Configure vistas de datos en Customer Journey Analytics](#cja-data-views).

1. (Analista web de su organización) [Configure informes y visualizaciones en Customer Journey Analytics Workspace](#cja-reports).

Las secciones siguientes incluyen los procedimientos detallados, que incluyen las tareas y configuraciones necesarias para la integración, pero no explican todas las funciones disponibles en los flujos de trabajo. Consulte los recursos vinculados para obtener información completa.

## Configure la recopilación de datos en Adobe Experience Platform y en el sitio web {#data-collection}

Se requieren las siguientes tareas para configurar la recopilación de datos en Experience Platform e implementar las etiquetas de seguimiento de conversión. El administrador del sitio de su organización para Experience Platform puede realizar estas tareas, pero es posible que el departamento de TI de su organización necesite ayudar a implementar las etiquetas de seguimiento.

### Recopilación y envío de datos de Adobe Advertising a Experience Platform Edge Network como conjunto de datos

1. En Experience Platform, [defina un esquema manual](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) para los datos que desea recopilar mediante el Experience Data Model (XDM).

   * En [!UICONTROL Schema Details], seleccione **[!UICONTROL Experience Event]** como clase base para que el esquema capture eventos de sitio. Asigne un nombre al esquema y haga clic en **[!UICONTROL Finish]**.

   * En el panel izquierdo, agregue el grupo de campos `Adobe Advertising Cloud ExperienceEvent Full Extension` para agregar campos específicos de Adobe Advertising.<!-- Add link once published --> Como mínimo, incluya el objeto conversionDetails con las propiedades `trackingCode` y `trackingIdentities`, que incluyen [AMO ID e EF ID](ids.md). Los demás campos son opcionales.

   * (Opcional) Agregue grupos de campos adicionales según sea necesario para conectar campos de datos adicionales a los datos de Adobe Advertising.

   **Nota:** Puede crear varios esquemas, pero solo puede usar un esquema por conjunto de datos y por secuencia de datos, que creará en los pasos siguientes.

1. [Cree un conjunto de datos](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) basado en el esquema para almacenar y administrar la colección de datos de evento.

   * Elija la opción para **[!UICONTROL Create dataset from schema]** y seleccione el esquema.

     Adobe Advertising crea conjuntos de datos adicionales para los datos de métricas de resumen relacionados (como valores de conversión) y datos de búsqueda (dimensiones/metadatos de clasificación, como el nombre de la campaña de Adobe Advertising) basados en el conjunto de datos de evento. Los datos de los conjuntos de datos se rellenan a diario en Experience Platform.

1. [Crear un conjunto de datos](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) para el esquema.

   * Para la configuración [!UICONTROL Mapping schema], seleccione su esquema.

   * Agregue y habilite los servicios `Adobe Advertising` y `Adobe Experience Platform` a la secuencia de datos.

     Estos servicios permiten a Edge Network almacenar el conjunto de datos y enrutarlo a Adobe Advertising.

   * Para la configuración [!UICONTROL Event dataset], seleccione su conjunto de datos.

     Cada conjunto de datos puede insertar datos en un único conjunto de datos.

### Envíe los datos del sitio web de su organización a su conjunto de datos de Experience Platform

1. Use Experience Platform [tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (anteriormente conocido como [!DNL Launch]) para generar una etiqueta JavaScript y enviar los datos del sitio web de su organización al conjunto de datos.

   * Cree una propiedad de etiqueta, que es el contenedor de la configuración de etiqueta.

   * Para su propiedad, [instale la extensión &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) del catálogo de extensiones.

     Esta extensión envía datos de las propiedades web a Experience Cloud a través de Experience Platform Edge Network.

     No utilice la extensión de Adobe Advertising.

   * Crear una [compilación personalizada de Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):

      * En la sección [!UICONTROL Custom build components], habilite el componente **Advertising**.

        Este componente incluye todo el código JavaScript necesario para Adobe Advertising en la etiqueta. También agrega una configuración &quot;Advertising&quot; en las reglas de etiquetas (que son opcionales) para definir cómo se utilizan los datos de publicidad para la medición de atribución.

        Si lo desea, puede activar componentes adicionales según sea necesario.

      * En la sección [!UICONTROL SDK Instances]:

         * En la configuración de [!UICONTROL Datastreams], seleccione el conjunto de datos que se utilizará para cada uno de los entornos web (producción, ensayo y desarrollo).

         * (Solo organizaciones con Adobe Advertising DSP) En la configuración de [!UICONTROL Adobe Advertising]:

            * Habilite la configuración **[!UICONTROL Adobe Advertising DSP]** para habilitar el seguimiento de visualizaciones.

            * Especifique los anunciantes para los que desea habilitar el seguimiento de visualizaciones.

            * (Opcional) Introduzca el ID de socio ID5 de su organización para recopilar los ID.

            * (Opcional) Introduzca la ruta del código JavaScript [!DNL LiveRamp RampID] de su organización (ats.js) para recopilar los ID.

         * Guarde la compilación.

   * (Opcional) [Cree reglas](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) según sea necesario para determinar cuándo Web SDK debe enviar datos a Edge Network.

      * Para las acciones de `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#send-event)`, use la configuración de [!UICONTROL Advertising] para definir cómo se usan los datos de publicidad para la medición de atribución. Esta configuración es útil cuando la regla incluye una secuencia de varias acciones y solo está disponible cuando ha seleccionado el componente &quot;[!UICONTROL Advertising]&quot; para el componente de compilación personalizada. Las opciones incluyen:

        *Automático:* Permite que se usen datos de publicidad para medir la atribución de publicidad en la acción actual `sendEvent` en función de los datos de la caché. En este caso, el evento de exposición de anuncio se activa cuando tiene la oportunidad y es posible que no esté disponible para el evento actual. Por ejemplo, si activa un evento de cierre de compra y no hay datos de exposición de publicidad disponibles en la caché, el evento de cierre de compra no se atribuye a la exposición de publicidad.

        *Espera:* Retrasa la ejecución de la llamada hasta que los datos de publicidad se recuperan correctamente del servidor y se resuelven, lo que garantiza una medición de atribución precisa. Por ejemplo: es posible que desee esperar a que se resuelva el evento de exposición de publicidad antes de activar un evento de cierre de compra. **Nota:** La resolución de los identificadores puede tardar unos segundos según el explorador y el tipo de identificador. Utilice esta opción si la acción actual `sendEvent` puede admitir unos segundos de retraso.

        *Deshabilitado:* (El valor predeterminado) Excluye los datos de publicidad de la solicitud que está activando, por lo que no están disponibles para la atribución o el seguimiento relacionado.

        *Proporcionar un elemento de datos:* Use un elemento de datos para incluir o excluir datos publicitarios durante la carga de la página. Los valores resueltos para el elemento de datos pueden incluir `automatic`, `wait` y `disabled`. Consulte el paso siguiente.

     Si no usa una regla para configurar una acción de `sendEvent`, los datos de publicidad se enviarán como un evento de enriquecimiento de anuncios independiente.

   * Cree [elementos de datos](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) según sea necesario para asignar variables en su sitio web a la estructura del esquema XDM que creó anteriormente.

1. [Publique la etiqueta](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) en un entorno de prueba en el que pueda iterar en el desarrollo de etiquetas.

1. Valide el envío de los conjuntos de datos y, a continuación, [publique la etiqueta en su entorno de producción activo](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Es posible que el departamento de TI de su organización u otro grupo tenga que programar la implementación de etiquetas o recibir información al respecto.

## Cree una conexión a los conjuntos de datos de Experience Platform en Customer Journey Analytics {#dataset-connection}

Siga estos pasos para extraer datos de Adobe Advertising de sus conjuntos de datos de Experience Platform en Customer Journey Analytics. El administrador del sitio de Customer Journey Analytics de su organización puede realizar estas tareas.

1. En Customer Journey Analytics, [cree una conexión](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) que incluya sus conjuntos de datos y esquema de Experience Platform.

   **Nota:** En la actualidad, debe enviar datos de todas las cuentas de DSP y Search, Social y Commerce a una sola instancia de Experience Platform y zona protegida.

   * Añada su conjunto de datos de evento de Experience Platform (métricas), su conjunto de datos de resumen (métricas) y su conjunto de datos de dimensiones (clasificaciones/metadatos).

     Su equipo creó el conjunto de datos de evento y Adobe Advertising creó los conjuntos de datos de resumen y dimensiones en función de su conjunto de datos de evento.

     Opcionalmente, puede incluir conjuntos de datos adicionales según sea necesario.

   * Asigne el conjunto de datos de dimensiones al conjunto de datos de eventos:

      1. Abra la configuración del conjunto de datos de dimensión.

         El encabezado de la página de configuración es &quot;[!UICONTROL Lookup Dataset]&quot;, lo que indica que puede unir el conjunto de datos de dimensiones con uno de los conjuntos de datos específicos de métricas.

      1. En la sección [!UICONTROL Adobe Advertising Dimensions], asigne el conjunto de datos de dimensiones al conjunto de datos de eventos:

         1. Para el campo [!UICONTROL Key], seleccione el campo que se utilizará como clave para el conjunto de datos de dimensiones: `Adobe Advertising ID` (que es el mismo que el campo `trackingCode` en el esquema).

         1. Para el campo [!UICONTROL Matching key], seleccione el campo que se utilizará como clave de coincidencia para el conjunto de datos de eventos. Los nombres de campo disponibles incluyen el nombre del conjunto de datos entre paréntesis. Por ejemplo, si está asignando el conjunto de datos de dimensiones al conjunto de datos de eventos, seleccione `Tracking Code (Event datasets)`.

         Más adelante, también asignará el conjunto de datos de eventos al conjunto de datos de resumen al configurar las vistas #cja-data-views datos.

1. Después de un par de horas, compruebe que los datos están disponibles en Customer Journey Analytics.

   1. En Customer Journey Analytics, vaya a **[!UICONTROL Connections]** y seleccione la conexión.

   1. En la lista de conjuntos de datos mostrados, compruebe que el informe &quot;[!UICONTROL Number of Records]&quot; muestra que se agregaron datos.

## Configuración de vistas de datos en Customer Journey Analytics {#cja-data-views}

En Customer Journey Analytics, cree una o más vistas de datos para definir las métricas y dimensiones para la creación de informes. Un analista web puede realizar estas tareas.

1. En Customer Journey Analytics, [cree una vista de datos](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configure la vista para incluir la siguiente información.

   * Si tiene una cuenta de Adobe Analytics, use [!UICONTROL Time Zone] para su cuenta de [!DNL Analytics] en la sección [!UICONTROL Calendar] de la ficha [!UICONTROL Configure].

   * En la ficha [!UICONTROL Components]:

      * Añada sus dimensiones, eventos y conjuntos de datos de resumen.

      * Elija métricas del conjunto de datos de eventos (métricas) y de las dimensiones (clasificaciones/metadatos) que desea incluir en la vista de datos.

        Ya ha unido estos dos conjuntos de datos en la conexión que creó en el [último procedimiento](#dataset-connection).

      * Una el conjunto de datos de eventos al conjunto de datos de resumen, que aún no está unido a nada:

         * Para cada dimensión con datos de resumen que desee que estén disponibles en Customer Journey Analytics, [cree un campo derivado](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

           Por ejemplo, para ver los datos de resumen de las campañas, cree un campo derivado para la dimensión `Adobe Advertising Campaign`.

           Vinculará los dos conjuntos de datos con la clave coincidente `trackingCode` (que es el campo de esquema para el Adobe Advertising ID).

            * En la sección [!UICONTROL Lookup] del generador de reglas derivado:

               * Para el campo **[!UICONTROL Value]**, seleccione &quot;[!UICONTROL Tracking Code]&quot; del conjunto de datos de resumen de métricas.

               * Para el campo **[!UICONTROL Lookup dataset]**, seleccione el conjunto de datos de dimensiones (como &quot;Clasificación de Adobe Advertising&quot;).

               * Para el campo **[!UICONTROL Matching Key]**, seleccione &quot;[!UICONTROL Tracking Code]&quot; del conjunto de datos de clasificación.

               * Para el campo **[!UICONTROL Values to return]**, seleccione la dimensión (como &quot;[!UICONTROL Adobe Advertising Campaign]&quot;) del conjunto de datos de clasificación.

           El nombre del campo derivado se anexa con &quot;(DF)&quot;, como `Adobe Advertising Campaign(DF)`.

         * Para cada campo derivado:

            * En la sección [!UICONTROL Included components], agregue el campo derivado.

              Ahora se muestran dos nombres para la misma dimensión (por ejemplo, &quot;Adobe Advertising Campaign(DF)&quot; (el campo derivado) y &quot;Adobe Advertising Campaign&quot; (el campo en el conjunto de datos de resumen)).

            * Seleccione la dimensión en el conjunto de datos de resumen (como &quot;Adobe Advertising Campaign&quot;) y edite la configuración del conjunto de datos.

              La configuración se abre a la derecha.

               * En la sección Grupo de datos de resumen, seleccione la opción **[!UICONTROL Create grouping]**.

               * Para el campo **[!UICONTROL Dimension]**, seleccione el campo derivado (que se anexa con &quot;(DF)&quot;, como &quot;Adobe Advertising Campaign(DF)&quot;).

               * Seleccione la opción **[!UICONTROL Hide in reporting]**, que oculta el nombre del campo derivado en Workspace.

## Configuración de informes y visualizaciones en Customer Journey Analytics Workspace {#cja-reports}

En Customer Journey Analytics Workspace, siga estos pasos para configurar informes y visualizaciones. Un analista web puede realizar estas tareas.

1. [Cree un proyecto](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) en Workspace para generar informes y visualizaciones basados en las dimensiones y métricas configuradas en la vista de datos.

1. (Si tiene datos de [!DNL Google Ads] o [!DNL Microsoft Advertising]) Cree un informe de conversiones rastreadas por el publicador usando campos para métricas específicas de red de anuncios, que se agrupan como `googleConversions` y `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Información general](overview.md)
>* [Requisitos previos](prerequisites.md)
>* [ID de Adobe Advertising usados por [!DNL Customer Journey Analytics]](ids.md)
>* [Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics](advertising-data-in-cja.md)
>* [Recopilar datos históricos para los ID de AMO y EF para su uso en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Guía de Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* [Guía del usuario de Customer Journey Analytics para usuarios de Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
