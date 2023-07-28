---
title: Implementación [!DNL Naver] cuentas solo de seguimiento
description: Obtenga información sobre cómo configurar campañas de seguimiento para su [!DNL Naver] cuentas de para que pueda rastrear, informar y visualizar el rendimiento de los anuncios que compra directamente desde la red de anuncios.
exl-id: 8013d4e8-0b4f-41a7-9c1b-10c55349930f
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Implementación [!DNL Naver] cuentas solo de seguimiento

*[!DNL Naver]solo cuentas*

Puede crear campañas de seguimiento para su [!DNL Naver] cuentas de para que pueda rastrear, informar y visualizar el rendimiento de los anuncios que compra directamente desde la red de anuncios. Search, Social y Commerce no sincronizan los datos con la red de publicidad, ni cargan automáticamente el seguimiento, ni hacen pujas por la cuenta.

El seguimiento de campañas reproduce las campañas, los grupos de publicidad y las palabras clave existentes. Una vez creada la estructura de cuentas en Buscar, Social y Comercio y agregado el seguimiento a las campañas originales dentro de la red de anuncios, puede cargar métricas de tráfico de red diarias para sus palabras clave o anuncios. Search, Social y Commerce pueden atribuir las conversiones a los anuncios y a las palabras clave.

Puede rastrear las métricas de rendimiento de todas sus campañas y de cualquier campaña, grupo de publicidad o palabra clave/anuncio individual. También puede incluir información sobre ellos en los informes más básicos, avanzados y de asistencia, junto con datos del resto de redes de anuncios. La compatibilidad para exportar las métricas a Adobe Analytics no está disponible, pero Search, Social y Commerce pueden sincronizarse [métricas en las que está realizando un seguimiento [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) en Search, Social y Commerce.

>[!NOTE]
>
>No puede agregar campañas de seguimiento a un portafolio para la optimización.

1. Cree campañas de seguimiento en Search, Social y Commerce:

   1. Crear [detalles de cuenta de red ficticia](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Si tiene varias cuentas dentro de una sola red de publicidad, consolide las cuentas en una sola cuenta en la [!UICONTROL Accounts] vista.

      [!DNL Naver] no proporciona compatibilidad con la API para cargar parámetros de seguimiento en la red de publicidad. Sin embargo, puede generar parámetros de seguimiento mediante hojas de edición masiva y añadirlos manualmente dentro de la red de publicidad (por Paso 2). Para generar los parámetros de seguimiento, debe utilizar el &quot;[!UICONTROL EF Redirect]&quot; método de seguimiento. Si lo desea, puede añadir cualquier parámetro de adición que desee.

      Search, Social y Commerce incluyen automáticamente el parámetro `ev_cl={ef_uniqueid}` en cualquier URL de seguimiento que genere en hojas de edición por lotes para la cuenta. Este ID único se utiliza para hacer coincidir los datos de la campaña con los datos de costes y clics que cargue.

   1. Configurar campañas para realizar el seguimiento:

      1. En la red de anuncios, cree un archivo de hoja de edición masiva que contenga todas las entidades y sus entidades principales requeridas que quiera que Search, Social y Commerce rastreen en la cuenta.

         Puede incluir datos sobre palabras clave, incluidas las campañas principales y los grupos de anuncios.

      1. Edite el archivo de hoja de edición por lotes, si es necesario, de modo que siga las instrucciones de Search, Social y Commerce [formato de hoja de edición masiva necesario para [!DNL Naver] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. En Búsqueda, Social Y Comercio, [cargar el archivo de hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Nota: Search, Social y Commerce no publica los datos en la cuenta de la red de publicidad.

1. Configure el seguimiento de las campañas:

   1. En Búsqueda, Social Y Comercio, [descargar un nuevo archivo de hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) uso de la opción para &quot;[!UICONTROL Generate Tracking URLs].&quot;

   Uso de &quot;[!UICONTROL Generate Tracking URLs]&quot; rellena la opción [!UICONTROL Destination URL] para cada palabra clave con el código de seguimiento Buscar, Social y Comercial con el prefijo [!UICONTROL Base URL] valor.

   A continuación se muestra un ejemplo de la dirección URL de destino con seguimiento:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Copie el [!UICONTROL Destination URL] valores en el archivo de hoja de edición masiva descargado a la configuración de palabras clave correspondiente en la red.

      Es posible que pueda añadir las direcciones URL a las entidades relevantes cargando el archivo en la red dentro del editor de la red de publicidad. En ese caso, es posible que tenga que quitar algunas columnas, según los requisitos de datos de la red. De lo contrario, debe introducir las direcciones URL manualmente en la red.

1. Descargue periódicamente datos sobre clics y costes acumulados diariamente desde la red de anuncios para las palabras clave o los anuncios de marca a nivel de grupo de anuncios que esté rastreando y, a continuación, [cargar los datos de clics y costes](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) a Búsqueda, Social y Comercio en la [formato requerido](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Incluya la jerarquía de cuentas completa y las métricas que desee incluir. Search, Social y Commerce hacen coincidir los datos cargados con los datos de las campañas existentes.

1. (Opcional) Si utiliza las etiquetas del servicio de seguimiento de conversiones de Adobe Advertising en sus páginas web para rastrear conversiones que no se rastrean en la red de anuncios, envíe archivos de fuentes que contengan datos de conversión agregados diariamente para agregarlos a sus campañas de seguimiento.

   Para obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

Todos los datos de seguimiento cargados están disponibles en [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] dentro de [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups], y [!UICONTROL Keywords] vistas. También está disponible para informes en [!UICONTROL Insights & Reports] vista.

>[!MORELIKETHIS]
>
>* [Apéndice: Datos de hojas de edición masiva requeridos para [!DNL Naver] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Cargar métricas de tráfico y conversión para [!DNL Naver] cuentas solo de seguimiento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Requisitos de datos de métricas para [!DNL Naver] cuentas solo de seguimiento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Formatos de rastreo de clics para [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
