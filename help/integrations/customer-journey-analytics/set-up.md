---
title: Configuración de la recopilación de datos, la transferencia de datos y la creación de informes
description: Obtenga información sobre cómo configurar la recopilación de datos, la transferencia de datos y la creación de informes.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: e208432cf19b2661fbce58a898a123bb1224c32b
workflow-type: tm+mt
source-wordcount: 1789
ht-degree: 0%

---

# Configuración de la recopilación de datos, la transferencia de datos y la creación de informes

*Anunciantes con Advertising DSP y[!DNL Advertising Search, Social, & Commerce]*

*Solo anunciantes sin [!DNL Analytics for Advertising]*

Se requieren las siguientes tareas para intercambiar datos de forma nativa entre Adobe Advertising y Customer Journey Analytics mediante [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es). La transferencia y la atribución de datos comienzan después del lanzamiento; no se incluyen datos históricos.

Estas tareas no son necesarias para los anunciantes con [!DNL Analytics for Advertising].

1. (Administrador del sitio de su organización para Adobe Experience Platform) [Configure la recopilación de datos en Experience Platform e implemente etiquetas de seguimiento de conversión](#data-collection).

1. (Administrador del sitio de su organización para Customer Journey Analytics) [Cree una conexión con los conjuntos de datos de Experience Platform en Customer Journey Analytics](#dataset-connection).

1. (Analista web de su organización) [Configure vistas de datos en Customer Journey Analytics](#cja-data-views).

1. (Analista web de su organización) [Configure informes y visualizaciones en Customer Journey Analytics Workspace](#cja-reports).

Las secciones siguientes incluyen los procedimientos detallados, que incluyen las tareas y configuraciones necesarias para la integración, pero no explican todas las funciones disponibles en los flujos de trabajo. Consulte los recursos vinculados para obtener información completa.

## Configure la recopilación de datos en Adobe Experience Platform y en el sitio web {#data-collection}

Se requieren las siguientes tareas para configurar la recopilación de datos en Experience Platform e implementar las etiquetas de seguimiento de conversión. El administrador del sitio de su organización para Experience Platform puede realizar estas tareas, pero es posible que el departamento de TI de su organización necesite ayudar a implementar las etiquetas de seguimiento.

### Recopilación y envío de datos de Adobe Advertising a Experience Platform Edge Network como conjunto de datos

Este procedimiento incluye la creación de un esquema. Si lo desea, puede editar un esquema existente en su lugar; en ese caso, no es necesario crear un conjunto de datos o una secuencia de datos.

1. En Experience Platform, [defina un esquema manual](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/ui/resources/schemas) para los datos que desea recopilar mediante el Experience Data Model (XDM).

   * En [!UICONTROL Schema Details], seleccione **[!UICONTROL Experience Event]** como clase base para que el esquema capture eventos de sitio. Asigne un nombre al esquema y haga clic en **[!UICONTROL Finish]**.

   * En el panel izquierdo, agregue el grupo de campos [Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) para agregar campos específicos de Adobe Advertising. Como mínimo, incluya el objeto conversionDetails con las propiedades `trackingCode` y `trackingIdentities`, que incluyen [AMO ID e EF ID](ids.md). Los demás campos son opcionales.

   * (Opcional) Agregue grupos de campos adicionales según sea necesario para conectar campos de datos adicionales a los datos de Adobe Advertising.

   **Nota:** Puede crear varios esquemas, pero solo puede usar un esquema por conjunto de datos y por secuencia de datos, que creará en los pasos siguientes.

1. [Cree un conjunto de datos](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/create) basado en el esquema para almacenar y administrar la colección de datos de evento. Este será su *conjunto de datos de evento*. Si está editando un esquema existente con un conjunto de datos, puede omitir este paso.

   * Elija la opción para **[!UICONTROL Create dataset from schema]** y seleccione el esquema.

     En función de su conjunto de datos de evento, Adobe Advertising crea dos conjuntos de datos adicionales: 1\) un *conjunto de datos de resumen* con los datos de resumen relacionados (como clics e impresiones) y 2\) un *conjunto de datos de búsqueda* (con metadatos de dimensiones/clasificación, como el nombre de la campaña de Adobe Advertising). Los datos de los conjuntos de datos se rellenan a diario en Experience Platform.

   >[!TIP]
   >
   >Cree primero un conjunto de datos de evento ficticio para validar el flujo de datos antes de utilizar un conjunto de datos de producción.

1. [Cree una secuencia de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/configure) para especificar dónde enviar datos desde su sitio web o aplicación y cómo manejar los datos entrantes.

   * Para la configuración [!UICONTROL Mapping schema], seleccione su esquema.

   * Agregue y habilite los servicios `Adobe Advertising` y `Adobe Experience Platform` a la secuencia de datos.

     El servicio [!UICONTROL Adobe Advertising] permite que las exposiciones de anuncios se asocien a la carga útil y [!UICONTROL Adobe Experience Platform] permite que Edge Network almacene el conjunto de datos y lo enrute a Adobe Advertising.

   * Para la configuración [!UICONTROL Event dataset], seleccione su conjunto de datos de evento.

     Cada conjunto de datos puede insertar datos en un único conjunto de datos.

### Envíe los datos del sitio web de su organización a su conjunto de datos de Experience Platform

Utilice la extensión Adobe Experience Platform Web SDK en Adobe Tags para enviar los datos del sitio web de su organización a su flujo de datos de Experience Platform.

>[!NOTE]
>
>Solo se admiten etiquetas de Adobe. La compatibilidad no está disponible para Experience Platform Web SDK independiente (`alloy.js`) o administradores de etiquetas de terceros.

1. Use Experience Platform [tags](https://experienceleague.adobe.com/es/docs/experience-platform/tags/home) (anteriormente conocido como [!DNL Launch]) para generar una etiqueta JavaScript y enviar los datos del sitio web de su organización al conjunto de datos.

   * Cree una propiedad de etiqueta, que es el contenedor de la configuración de etiqueta.

   * Para su propiedad, [instale la extensión &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/es/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) del catálogo de extensiones.

     Esta extensión envía datos de sus propiedades web a Adobe CX Enterprise a través de Experience Platform Edge Network.

     No utilice la extensión de Adobe Advertising.

   * Crear una [compilación personalizada de Web SDK](https://experienceleague.adobe.com/es/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):

      * En la sección [!UICONTROL Custom build components], habilite el componente **Advertising**.

        Este componente incluye todo el código de JavaScript necesario para Adobe Advertising en la etiqueta y es necesario para los clientes de Advertising DSP y Advertising Search, Social y Commerce. El componente también agrega una configuración &quot;Advertising&quot; en las reglas de etiquetas (que son opcionales) para definir cómo se utilizan los datos de publicidad para la medición de atribución.

        Si lo desea, puede activar componentes adicionales según sea necesario.

      * En la sección [!UICONTROL SDK Instances]:

         * En la configuración de [!UICONTROL Datastreams], seleccione el conjunto de datos que se utilizará para cada uno de los entornos web (producción, ensayo y desarrollo).

         * (Solo organizaciones con Adobe Advertising DSP) En la configuración [[!UICONTROL Adobe Advertising]](https://experienceleague.adobe.com/es/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising), habilite **[!UICONTROL Adobe Advertising DSP]** para permitir el seguimiento de visualización y especifique los anunciantes para los que habilitar el seguimiento de visualización. Si lo desea, puede recopilar ID de ID universales añadiendo el ID de socio ID5 de su organización o la ruta al código JavaScript [!DNL LiveRamp RampID] de su organización (ats.js).

           Si los anunciantes no aparecen en la lista, introduzca el ID de anunciante de cada anunciante. Si es necesario, pida los ID a su equipo de cuenta de Adobe.

         * Guarde la compilación.

   * (Opcional) [Cree reglas](https://experienceleague.adobe.com/es/docs/experience-platform/tags/ui/rules) según sea necesario para determinar cuándo Web SDK debe enviar datos a Edge Network.

      * Para las acciones de `[sendEvent](https://experienceleague.adobe.com/es/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)`, use la configuración [[!UICONTROL Advertising] &#x200B;](https://experienceleague.adobe.com/es/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) para definir cómo se usan los datos de publicidad para la medición de atribución. Esta configuración es útil cuando la regla incluye una secuencia de varias acciones y solo está disponible cuando ha seleccionado el componente &quot;[!UICONTROL Advertising]&quot; para el componente de compilación personalizada.

   * Cree [elementos de datos](https://experienceleague.adobe.com/es/docs/experience-platform/tags/ui/data-elements) según sea necesario para asignar variables en su sitio web a la estructura del esquema XDM que creó anteriormente.

1. [Publique la etiqueta](https://experienceleague.adobe.com/es/docs/experience-platform/tags/publish/publishing-flow) en un entorno de prueba en el que pueda iterar en el desarrollo de etiquetas.

1. [Compruebe la actividad de cada uno de sus tres conjuntos de datos](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/user-guide#view-datasets) para validar el envío.

1. [Publique la etiqueta en su entorno de producción activo](https://experienceleague.adobe.com/es/docs/experience-platform/tags/publish/publishing-flow).

   Es posible que el departamento de TI de su organización u otro grupo tenga que programar la implementación de etiquetas o recibir información al respecto.

## Cree una conexión a los conjuntos de datos de Experience Platform en Customer Journey Analytics {#dataset-connection}

Siga estos pasos para extraer datos de Adobe Advertising de sus conjuntos de datos de Experience Platform en Customer Journey Analytics. El administrador del sitio de Customer Journey Analytics de su organización puede realizar estas tareas.

También puede editar una conexión existente con la misma información.

1. En Customer Journey Analytics, [cree o edite una conexión](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-connections/create-connection) que incluya sus conjuntos de datos y esquema de Experience Platform.

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * Confirme que está seleccionada la zona protegida correcta.

   * Calcule el número medio de eventos diarios (menos de 1 millón para la mayoría de las organizaciones).

   * Agregue el conjunto de datos de métricas de evento de Experience Platform (tipo: `Event`), el conjunto de datos de métricas de resumen de evento <!-- Adobe Advertising --> (tipo: `Event`) y el conjunto de datos de dimensiones <!-- Adobe Advertising --> (clasificaciones/metadatos) (tipo: `Lookup`).

     Su equipo creó el conjunto de datos de evento y Adobe Advertising creó los conjuntos de datos de resumen y dimensiones en función de su conjunto de datos de evento.

     Opcionalmente, puede incluir conjuntos de datos adicionales según sea necesario.

   * Configure las opciones del conjunto de datos:

      * Para la configuración de [!UICONTROL Event Dataset]:

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Use primary identity namespace]:** Habilitar configuración

         * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->

         * **[!UICONTROL Import all new data]:** Habilitar la configuración

      * Para la configuración de [!UICONTROL Lookup Dataset], asigne el conjunto de datos de dimensiones al conjunto de datos de eventos:

         * **[!UICONTROL Key]** (el campo que se utilizará como clave para el conjunto de datos de dimensiones): `Tracking Code` (que es el mismo que el campo `trackingCode` en el esquema).

         * **[!UICONTROL Matching key]** (el campo que se usará como clave coincidente para el conjunto de datos de eventos): `Tracking Code (Event datasets)`.<!-- verify this Later, you'll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).  -->

         * **[!UICONTROL Import all new data]:** Habilitar la configuración

      * Para la configuración de [!UICONTROL Metrics Dataset]:

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Timestamp]:** Confirmar el valor

         * **[!UICONTROL Import all new data]:** Habilitar la configuración

1. En un plazo de tres horas, compruebe que los datos están disponibles en Customer Journey Analytics.

   1. En Customer Journey Analytics, vaya a **[!UICONTROL Connections]** y seleccione la conexión.

   2. En la lista de conjuntos de datos mostrados, compruebe que el informe &quot;[!UICONTROL Number of Records]&quot; muestra que se agregaron datos.

## Configuración de vistas de datos en Customer Journey Analytics {#cja-data-views}

En Customer Journey Analytics, cree una o más vistas de datos para definir las métricas y dimensiones para la creación de informes. Un analista web puede realizar estas tareas.

1. En Customer Journey Analytics, [cree una vista de datos](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configure la vista para incluir la siguiente información.

   * Si tiene una cuenta de Adobe Analytics, use [!UICONTROL Time Zone] para su cuenta de [!DNL Analytics] en la sección [!UICONTROL Calendar] de la ficha [!UICONTROL Configure].

   * En la ficha [!UICONTROL Components]:

      * Añada el conjunto de datos de búsqueda (con dimensiones/datos de clasificación), el conjunto de datos de evento (con los datos de nivel de evento) y el conjunto de datos de resumen (con el resto de las métricas, como los clics).

      * Elija métricas del conjunto de datos de evento y del conjunto de datos de búsqueda para incluirlas en la vista de datos.

      * Busque &quot;[!UICONTROL Tracking Code]&quot; (que forma parte del conjunto de datos de evento con la ruta de acceso de esquema `_experience.adcloud.conversionDetails.trackingCode`). <!-- and do what with it? Add it? Or is that what you --> Establezca **[!UICONTROL Persistence]** en *[!UICONTROL Most Recent]*.

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## Configuración de informes y visualizaciones en Customer Journey Analytics Workspace {#cja-reports}

En Customer Journey Analytics Workspace, siga estos pasos para configurar informes y visualizaciones. Un analista web puede realizar estas tareas.

1. [Cree un proyecto](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) en Workspace para generar informes y visualizaciones basados en las dimensiones y métricas configuradas en la vista de datos.

Puede clasificar métricas de resumen y datos de evento con la misma dimensión en una tabla de forma libre.

1. (Si tiene datos de [!DNL Google Ads] o [!DNL Microsoft Advertising]) Cree un informe de conversiones rastreadas por el publicador usando campos para métricas específicas de red de anuncios, que se agrupan como `googleConversions` y `microsoftConversions`.

>[!TIP]
>
>Los eventos de resumen suelen agregar una pequeña cantidad de datos adicionales a los informes, como algunos eventos adicionales, una sesión adicional por día o una persona adicional por informe. Estas adiciones son insignificantes en comparación con los eventos web estándar. Sin embargo, puede filtrar estos datos de evento de resumen adicionales excluyendo los datos para el ID de persona ficticia `00000000-0000-0000-0000-000000000000`.
>![Ejemplo de exclusión de datos mediante un ID de persona](/help/integrations/assets/cja-report-with-person-id.png "Ejemplo de exclusión de datos mediante un ID de persona")

![Cómo pueden aparecer los conjuntos de datos en Customer Journey Analytics](/help/integrations/assets/cja-report-example.png "Cómo pueden aparecer los conjuntos de datos en Customer Journey Analytics")

>[!MORELIKETHIS]
>
>* [Información general](overview.md)
>* [Requisitos previos](prerequisites.md)
>* [ID de Adobe Advertising usados por [!DNL Customer Journey Analytics]](ids.md)
>* [Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics](advertising-data-in-cja.md)
>* [Recopilar datos históricos para los ID de AMO y EF para su uso en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Guía de Customer Journey Analytics](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-landing)
>* [Guía del usuario de Customer Journey Analytics para usuarios de Adobe Analytics](https://experienceleague.adobe.com/es/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
