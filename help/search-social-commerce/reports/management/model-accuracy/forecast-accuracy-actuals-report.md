---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Obtenga información acerca de [!UICONTROL Forecast Accuracy (Actuals) Report], incluidas las columnas de datos.
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# El [!UICONTROL Forecast Accuracy (Actuals) Report]

Este informe muestra los datos reales de impresión, clics, costes e ingresos de la red de publicidad por día de cada portafolio.

## Columnas disponibles

A continuación se indican las columnas que se incluyen automáticamente en cada informe. No se pueden agregar columnas adicionales.

| Columna | ¿Predeterminado? | Descripción |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Predeterminado | El nombre del grupo de portafolios al que pertenece el portafolio. |
| [!UICONTROL Portfolio ID] | Predeterminado | El ID numérico del portafolio. |
| [!UICONTROL EF Portfolio Group ID] | Predeterminado | El ID numérico del grupo de portafolios al que pertenece el portafolio. |
| [!UICONTROL Portfolio] | Predeterminado | El portafolio. |
| [!UICONTROL Portfolio Status] | Predeterminado | El estado del portafolio:<ul><li><i>[!UICONTROL Optimize]:</i> La capacidad de optimización consiste en recopilar datos de clics e ingresos de las campañas relevantes, modelar los datos para optimizar las ofertas y optimizar las ofertas o los presupuestos de campaña (según el tipo de optimización y las estrategias de oferta de la campaña).</li><li><i>[!UICONTROL Active]:</i> La capacidad de optimización recopila datos de clics e ingresos de las campañas relevantes y modela los datos, pero no optimiza las ofertas ni los presupuestos de las campañas.</li><li><i>[!UICONTROL Inactive]:</i> La capacidad de optimización está recopilando datos de clics de las campañas relevantes para fines de creación de informes, pero no está modelando los datos ni optimizando ofertas o presupuestos de campaña. |
| [!UICONTROL Day of Week] | Predeterminado | El día de la semana informó: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, o <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Predeterminado | La fecha del informe. |
| [!UICONTROL Device] | Predeterminado | (Google Ads, Microsoft Advertising, Yahoo! Display Network, Yahoo! Japan Ads y Yahoo Native campaigns) El tipo de dispositivo en el que se mostraron los anuncios: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>, o <i>[!UICONTROL N/A]</i> (sin valor). Las filas de otras redes de anuncios tienen valores de <i>[!UICONTROL N/A]</i>.<br><br>En campañas de búsqueda, si las plantillas de seguimiento o las direcciones URL de destino para las palabras clave, los anuncios o las extensiones de publicidad incluían parámetros para rastrear los datos por dispositivo (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) en el momento en que se hizo clic en el anuncio, los datos de conversión también se incluyen en la fila para cada tipo de dispositivo. De lo contrario, si los datos de conversión no pueden atribuirse a un tipo de dispositivo, se agregan en una fila independiente con el signo &quot;[!UICONTROL Device]&quot; valor de <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Predeterminado | Los ingresos totales. |
| [!UICONTROL Impressions] | Predeterminado | El total de impresiones. |
| [!UICONTROL Clicks] | Predeterminado | El total de clics. |
| [!UICONTROL Cost] | Predeterminado | El coste total. |

>[!MORELIKETHIS]
>
>* [Acerca de los informes de precisión de modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [El [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Generar un informe de precisión de modelo](model-accuracy-report-generate.md)
>* [Configuración del informe de precisión de modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
