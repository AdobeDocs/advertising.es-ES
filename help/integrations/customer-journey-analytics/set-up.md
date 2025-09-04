---
title: Configuración de la recopilación de datos, la transferencia de datos y la creación de informes
description: Obtenga información sobre cómo configurar la recopilación de datos, la transferencia de datos y la creación de informes.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 2d6cba8d5a3d966b272c5048404ac8fdf0185b74
workflow-type: tm+mt
source-wordcount: '1236'
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

1. Recopile y envíe datos de Adobe Advertising a Experience Platform Edge Network como un conjunto de datos:

   1. En Experience Platform, [defina un esquema manual](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/ui/resources/schemas) para los datos que desea recopilar mediante el Experience Data Model (XDM).

      * En [!UICONTROL Schema Details], seleccione **[!UICONTROL Experience Event]** como clase base para que el esquema capture eventos de sitio. Asigne un nombre al esquema y haga clic en **[!UICONTROL Finish]**.

      * En el panel izquierdo, agregue el grupo de campos `Adobe Advertising Cloud ExperienceEvent Full Extension` para agregar campos específicos de Adobe Advertising.<!-- Add link once published --> Como mínimo, incluya el objeto conversionDetails con las propiedades `trackingCode` y `trackingIdentities`, que incluyen [AMO ID e EF ID](ids.html). Los demás campos son opcionales.

      * (Opcional) Agregue grupos de campos adicionales según sea necesario para conectar campos de datos adicionales a los datos de Adobe Advertising.

      **Nota:** Puede crear varios esquemas, pero solo puede usar un esquema por conjunto de datos y por secuencia de datos, que creará en los pasos siguientes.

   1. [Cree un conjunto de datos](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/create) basado en el esquema para almacenar y administrar la colección de datos de evento.

      * Elija la opción para **[!UICONTROL Create dataset from schema]** y seleccione el esquema.

        Adobe Advertising crea conjuntos de datos adicionales para los datos de métricas de resumen relacionados (como valores de conversión) y datos de búsqueda (dimensiones/metadatos de clasificación, como el nombre de la campaña de Adobe Advertising) basados en el conjunto de datos de evento. Los datos de los conjuntos de datos se rellenan a diario en Experience Platform.

   1. [Crear un conjunto de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure) para el esquema.

      * Para la configuración [!UICONTROL Mapping schema], seleccione su esquema.

      * Agregue y habilite los servicios `Adobe Advertising` y `Adobe Experience Platform` a la secuencia de datos.

        Estos servicios permiten a Edge Network almacenar el conjunto de datos y enrutarlo a Adobe Advertising.

      * Para la configuración [!UICONTROL Event dataset], seleccione su conjunto de datos.

        Cada conjunto de datos puede insertar datos en un único conjunto de datos.

1. Envíe los datos del sitio web de su organización a su conjunto de datos de Experience Platform:

   1. Use Experience Platform [tags](https://experienceleague.adobe.com/es/docs/experience-platform/tags/home) (anteriormente conocido como [!DNL Launch]) para generar una etiqueta JavaScript y enviar los datos del sitio web de su organización al conjunto de datos.

      * Cree una propiedad de etiqueta, que es el contenedor de la configuración de etiqueta.

      * Para su propiedad, [instale la extensión &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/es/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) del catálogo de extensiones.

        Esta extensión envía datos de las propiedades web a Experience Cloud a través de Experience Platform Edge Network.

        No utilice la extensión de Adobe Advertising.

      * Cree una compilación personalizada de Web SDK:

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

      * (Opcional) [Cree reglas](https://experienceleague.adobe.com/es/docs/experience-platform/tags/ui/rules) según sea necesario para determinar cuándo Web SDK debe enviar datos a Edge Network.

         * Para la configuración [!UICONTROL Advertising], defina cómo se utilizan los datos de publicidad para la medición de atribución. Esta configuración es útil cuando la regla incluye una secuencia de varias acciones y solo está disponible cuando ha seleccionado el componente &quot;[!UICONTROL Advertising]&quot; para el componente de compilación personalizada. Las opciones incluyen:

           *Automático:* Permite que se usen datos de publicidad para medir la atribución de publicidad en la acción actual `sendEvent` en función de los datos de la caché. En este caso, el evento de exposición de anuncio se activa cuando tiene la oportunidad y es posible que no esté disponible para el evento actual. Por ejemplo, si activa un evento de cierre de compra y no hay datos de exposición de publicidad disponibles en la caché, el evento de cierre de compra no se atribuye a la exposición de publicidad.

           *Espera:* Retrasa la ejecución de la llamada hasta que los datos de publicidad se recuperan correctamente del servidor y se resuelven, lo que garantiza una medición de atribución precisa. Por ejemplo: es posible que desee esperar a que se resuelva el evento de exposición de publicidad antes de activar un evento de cierre de compra. **Nota:** La resolución de los identificadores puede tardar unos segundos según el explorador y el tipo de identificador. Utilice esta opción si la acción actual `sendEvent` puede admitir unos segundos de retraso.

           *Deshabilitado:* (El valor predeterminado) Excluye los datos de publicidad de la solicitud que está activando, por lo que no están disponibles para la atribución o el seguimiento relacionado.

           *Proporcionar un elemento de datos:* Use un elemento de datos para incluir o excluir datos publicitarios durante la carga de la página. Los valores resueltos para el elemento de datos pueden incluir `automatic`, `wait` y `disabled`. Consulte el paso siguiente.

        Si no usa una regla para configurar una acción de `sendEvent`, los datos de publicidad se enviarán como un evento de enriquecimiento de anuncios independiente.

      * Cree [elementos de datos](https://experienceleague.adobe.com/es/docs/experience-platform/tags/ui/data-elements) según sea necesario para asignar variables en su sitio web a la estructura del esquema XDM que creó anteriormente.

   1. [Publique la etiqueta](https://experienceleague.adobe.com/es/docs/experience-platform/tags/publish/publishing-flow) en un entorno de prueba en el que pueda iterar en el desarrollo de etiquetas.

   1. Valide el envío de los conjuntos de datos y, a continuación, [publique la etiqueta en su entorno de producción activo](https://experienceleague.adobe.com/es/docs/experience-platform/tags/publish/publishing-flow).

      Es posible que el departamento de TI de su organización u otro grupo tenga que programar la implementación de etiquetas o recibir información al respecto.

## Cree una conexión a los conjuntos de datos de Experience Platform en Customer Journey Analytics {#dataset-connection}

Siga estos pasos para extraer datos de Adobe Advertising de sus conjuntos de datos de Experience Platform en Customer Journey Analytics. El administrador del sitio de Customer Journey Analytics de su organización puede realizar estas tareas.

*Próximamente*

## Configuración de vistas de datos en Customer Journey Analytics {#cja-data-views}

En Customer Journey Analytics, cree una o más vistas de datos para definir las métricas y dimensiones para la creación de informes. Un analista web puede realizar estas tareas.

*Próximamente*

## Configuración de informes y visualizaciones en Customer Journey Analytics Workspace {#cja-reports}

En Customer Journey Analytics Workspace, siga estos pasos para configurar informes y visualizaciones. Un analista web puede realizar estas tareas.

1. [Cree un proyecto](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) en Workspace para generar informes y visualizaciones basados en las dimensiones y métricas configuradas en la vista de datos.

1. (Si tiene datos de [!DNL Google Ads] o [!DNL Microsoft Advertising]) Cree un informe de conversiones rastreadas por el publicador usando campos para métricas específicas de red de anuncios, que se agrupan como `googleConversions` y `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Información general](overview.md)
>* [Requisitos previos](prerequisites.md)
>* [ID de Adobe Advertising usados por [!DNL Customer Journey Analytics]](ids.md)
>* [Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics](advertising-data-in-cja.md)
>* [Recopilar datos históricos para los ID de AMO y EF para su uso en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Guía de Customer Journey Analytics](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-landing)
>* [Guía del usuario de Customer Journey Analytics para usuarios de Adobe Analytics](https://experienceleague.adobe.com/es/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
