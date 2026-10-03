---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: Más información acerca de [!UICONTROL Google AI Max Search Term Combination Report].
feature: Search Reports, Search Specialty Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
  - id: 7de556b7-2c2a-599d-853b-8c282aafa6e3
    internal-label: Search Specialty Reports
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*Aplicable a [!DNL Google Ads] cuentas con campañas habilitadas para el máximo de IA*

El [!UICONTROL Google AI Max Search Term Combination Report] muestra cómo se asignan las consultas de búsqueda específicas a titulares generados por IA y páginas de aterrizaje dinámicas, así como a acciones de conversión para anuncios en campañas habilitadas para [!DNL Google Ads AI Max] dentro de cuentas especificadas. El informe incluye dos hojas:

* Hoja [!UICONTROL AI Max Search Term]: el rendimiento de combinaciones de anuncios y páginas de aterrizaje específicas basadas en búsquedas dentro de la red de búsqueda. La hoja incluye datos de impresiones, clics y costos, así como cualquier métrica de conversión [!DNL Google Ads] rastreada opcional especificada en la configuración del informe. De forma predeterminada, los datos incluyen una fila para cada término de búsqueda, titular y combinación de página de aterrizaje que recibió al menos una impresión en el intervalo de datos especificado. Las filas están en orden ascendente por campaña de forma predeterminada y, a continuación, por otra columna de su elección.

  Utilice esta hoja para analizar la intención y el rendimiento de los elementos de anuncio resultantes por consulta, de modo que pueda generar listas de palabras clave negativas sólidas.

* <!-- [!UICONTROL Search Term x Conversion Action] sheet? -->Hoja [!UICONTROL AI Max Search Term #1]: datos de conversión rastreados por [!DNL Google Ads] mediante la acción de conversión para cada término de búsqueda y tipo de coincidencia. Cada fila incluye la acción de conversión, el número de conversiones y el valor de conversión, así como cualquier otra métrica de conversión [!DNL Google Ads] rastreada opcional especificada en la configuración del informe. De forma predeterminada, los datos incluyen una fila para cada combinación de término de búsqueda y acción de conversión en el intervalo de datos especificado. Las filas están en el mismo orden que las filas de la primera hoja.

  <!-- Should it be this?  The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions. -->

  Utilice esta hoja para comprender cómo generó conversiones cada término de búsqueda, desglosado por acción de conversión.

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## Columnas predeterminadas

Para obtener descripciones de todas las columnas predeterminadas y personalizadas, consulte &quot;[Columnas de informe para informes de especialidades](specialty-report-columns.md)&quot;.

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Conversion Action] (se incluye automáticamente en la hoja [!UICONTROL AI Max Search Term #1], aunque no lo incluya explícitamente)
* [!UICONTROL Conversions] (se incluye automáticamente en la hoja [!UICONTROL AI Max Search Term #1], aunque no lo incluya explícitamente)
* [!UICONTROL Conversions Value] (se incluye automáticamente en la hoja [!UICONTROL AI Max Search Term #1], aunque no lo incluya explícitamente)

>[!MORELIKETHIS]
>
>* [Acerca de los informes de especialidad](specialty-report-about.md)
>* [Administrar informes programados](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Configuración de informes especiales](specialty-report-settings.md)
>* [Columnas de informes para informes especiales](specialty-report-columns.md)
