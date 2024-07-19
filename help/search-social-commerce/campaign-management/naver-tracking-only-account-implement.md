---
title: Implementar  [!DNL Naver] cuentas de solo seguimiento
description: Aprenda a configurar campañas de seguimiento para sus cuentas de  [!DNL Naver] para que pueda rastrear, informar y visualizar el rendimiento de los anuncios que compra directamente desde la red de anuncios.
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Implementar [!DNL Naver] cuentas solo de seguimiento

*[!DNL Naver]solo cuentas*

Puede crear campañas de seguimiento para sus cuentas de [!DNL Naver] con el fin de realizar un seguimiento de los anuncios que compra directamente en la red de anuncios, generar informes al respecto y visualizar el rendimiento. Search, Social y Commerce no sincronizan los datos con la red de anuncios, no cargan automáticamente el seguimiento ni hacen pujas por la cuenta.

El seguimiento de campañas reproduce las campañas, los grupos de publicidad y las palabras clave existentes. Una vez creada la estructura de cuentas en Buscar, Social y Commerce y agregado el seguimiento a las campañas originales dentro de la red de anuncios, puede cargar métricas de tráfico de red diarias para sus palabras clave o anuncios. Search, Social y Commerce pueden atribuir las conversiones a los anuncios y a las palabras clave.

Puede rastrear las métricas de rendimiento de todas sus campañas y de cualquier campaña, grupo de publicidad o palabra clave/anuncio individual. También puede incluir información sobre ellos en los informes más básicos, avanzados y de asistencia, junto con datos del resto de redes de anuncios. La compatibilidad para exportar las métricas a Adobe Analytics no está disponible, pero Search, Social y Commerce pueden sincronizar [métricas de las que estás realizando un seguimiento en [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) con Search, Social y Commerce.

>[!NOTE]
>
>No puede agregar campañas de seguimiento a un portafolio para la optimización.

1. Cree campañas de seguimiento en Search, Social y Commerce:

   1. Crear [detalles ficticios de cuenta de red](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Si tiene varias cuentas dentro de una sola red de anuncios, consolidelas en una sola cuenta en la vista [!UICONTROL Accounts].

      [!DNL Naver] no proporciona compatibilidad con API para cargar parámetros de seguimiento en la red de anuncios. Sin embargo, puede generar parámetros de seguimiento mediante hojas de edición masiva y añadirlos manualmente dentro de la red de publicidad (por Paso 2). Para generar los parámetros de seguimiento, debe utilizar el método de seguimiento &quot;[!UICONTROL EF Redirect]&quot;. Si lo desea, puede añadir cualquier parámetro de adición que desee.

      Search, Social y Commerce incluyen automáticamente el parámetro `ev_cl={ef_uniqueid}` en cualquier URL de seguimiento que genere en hojas de edición por lotes para la cuenta. Este ID único se utiliza para hacer coincidir los datos de la campaña con los datos de costes y clics que cargue.

   1. Configurar campañas para realizar el seguimiento:

      1. Dentro de la red de anuncios, cree un archivo de hoja de edición masiva que contenga todas las entidades y sus entidades padre requeridas que quiera que Search, Social y Commerce rastreen en la cuenta.

         Puede incluir datos sobre palabras clave, incluidas las campañas principales y los grupos de anuncios.

      1. Edite el archivo de hoja de edición masiva, si es necesario, de modo que siga el formato de hoja de edición masiva de Search, Social y Commerce [necesario para [!DNL Naver] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. En Buscar, Social y Commerce, [cargue el archivo de hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Nota: Search, Social y Commerce no publican los datos en la cuenta de la red de publicidad.

1. Configure el seguimiento de las campañas:

   1. En Search, Social y Commerce, [descargue un nuevo archivo de hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) con la opción &quot;[!UICONTROL Generate Tracking URLs]&quot;.

   Al usar la opción &quot;[!UICONTROL Generate Tracking URLs]&quot;, se rellena el campo [!UICONTROL Destination URL] de cada palabra clave con el código de seguimiento de Search, Social y Commerce con el prefijo [!UICONTROL Base URL].

   A continuación se muestra un ejemplo de la dirección URL de destino con seguimiento:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Copie los valores de [!UICONTROL Destination URL] del archivo de hoja de edición masiva descargado en la configuración de palabras clave correspondiente de la red.

      Es posible que pueda añadir las direcciones URL a las entidades relevantes cargando el archivo en la red dentro del editor de la red de publicidad. En ese caso, es posible que tenga que quitar algunas columnas, según los requisitos de datos de la red. De lo contrario, debe introducir las direcciones URL manualmente en la red.

1. Descargue periódicamente los datos de clics y costes acumulados diariamente desde la red de anuncios para las palabras clave o los anuncios de marca a nivel de grupo de anuncios que está rastreando y, a continuación, [cargue los datos de clics y costes](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) en Search, Social y Commerce en el [formato requerido](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Incluya la jerarquía de cuentas completa y las métricas que desee incluir. Search, Social y Commerce hacen coincidir los datos cargados con los datos de campañas existentes.

1. (Opcional) Si utiliza las etiquetas del servicio de seguimiento de conversiones de Adobe Advertising en sus páginas web para rastrear conversiones que no se rastrean en la red de anuncios, envíe archivos de fuentes que contengan datos de conversión agregados diariamente para agregarlos a sus campañas de seguimiento.

   Para obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

Todos los datos de seguimiento cargados están disponibles en [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] en las vistas [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] y [!UICONTROL Keywords]. También está disponible para informes en la vista [!UICONTROL Insights & Reports].

>[!MORELIKETHIS]
>
>* [Apéndice: datos de hoja de edición masiva requeridos para [!DNL Naver] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Cargar tráfico y métricas de conversión para [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Requisitos de datos de métrica para [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Formatos de rastreo de clics para [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
