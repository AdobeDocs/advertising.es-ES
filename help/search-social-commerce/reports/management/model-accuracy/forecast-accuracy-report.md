---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Obtenga información sobre el informe de precisión de la previsión, incluidas las columnas de datos.
exl-id: f0c42323-eb0d-461a-ab09-440fd1bfc960
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# El [!UICONTROL Forecast Accuracy Report]

El informe muestra la precisión de los modelos de costes e ingresos por día para portafolios específicos. De forma predeterminada, incluye los ingresos, costos y clics diarios previstos y reales, así como la precisión de las previsiones, de cada portafolio. Incluye datos de campañas que están asignadas actualmente a los portafolios.

Puede ver los datos de los 18 meses anteriores.

>[!NOTE]
>
>* Este informe proporciona los mismos datos que el nivel de portafolio [!UICONTROL Model Accuracy Report], excepto que se puede ejecutar en varios portafolios y se puede cambiar la regla de atribución. También puede ejecutar y programar el informe utilizando parámetros personalizados, y puede utilizarlo para crear fuentes de hoja de cálculo.
>
>* La práctica recomendada es ver [!UICONTROL Forecast Accuracy Report] durante al menos los últimos siete días, ya que, independientemente de la estrategia de gasto del portafolio, la mayoría de los portafolios ven una tendencia inherente de día de la semana. La capacidad de optimización tiene en cuenta esta tendencia y asigna el gasto en consecuencia.
>
>* Para las previsiones de costes, se considera aceptable una desviación del 10% en los últimos siete días, por lo que el gasto real que está entre el 90% y el 110% del gasto previsto está bien. Para las previsiones de ingresos, se considera aceptable una desviación del 15% en los últimos siete días, por lo que los ingresos reales que están entre el 85% y el 115% del gasto previsto están bien. Deben investigarse los pronósticos con desviaciones más altas.
>
>* Cuando las palabras clave de la cartera están asociadas con restricciones de desplazamiento de ofertas, la cartera gasta más o menos de lo debido en la cantidad total causada por el cambio de ofertas. Como resultado, las columnas de coste previsto se desvían del gasto objetivo por el aumento o la disminución del gasto.

## Columnas disponibles

Las siguientes son las columnas disponibles para cada informe. Las columnas predeterminadas se incluyen automáticamente de forma predeterminada. Puede agregar las columnas personalizadas disponibles desde la sección [!UICONTROL Columns] de la configuración del informe.

| Columna | ¿Predeterminado? | Descripción |
|----|----|----|
| [!UICONTROL Portfolio] | Predeterminado | El portafolio. |
| [!UICONTROL Day of Week] | Predeterminado | Se informó del día de la semana: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> o <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Predeterminado | Se informó del primer día. |
| [!UICONTROL End Date] | Predeterminado | Se informó del último día. |
| [!UICONTROL Predicted Revenue] | Predeterminado | Ingresos previstos para el portafolio. |
| [!UICONTROL Revenue] | Predeterminado | Ingresos reales de la cartera. |
| [!UICONTROL Revenue Accuracy] | Predeterminado | La precisión de la previsión de ingresos, expresada como porcentaje. |
| [!UICONTROL Predicted Cost] | Predeterminado | El coste previsto para el portafolio. |
| [!UICONTROL Cost] | Predeterminado | El coste real del portafolio. |
| [!UICONTROL Cost Accuracy] | Predeterminado | La precisión de la previsión de costes, expresada como porcentaje. |
| [!UICONTROL Predicted Clicks] | Predeterminado | El número de clics predichos para el portafolio. |
| [!UICONTROL Clicks] | Predeterminado | El número real de clics del portafolio. |
| [!UICONTROL Click Accuracy] | Predeterminado | La precisión de la previsión de clics, expresada como porcentaje. |
| [!UICONTROL EF Portfolio Group ID] | Predeterminado | El ID numérico del grupo de portafolios al que pertenece el portafolio. |
| [!UICONTROL Portfolio Group Name] | Predeterminado | El nombre del grupo de portafolios al que pertenece el portafolio. |
| [!UICONTROL Portfolio ID] | Predeterminado | El ID numérico del portafolio. |

>[!MORELIKETHIS]
>
>* [Acerca de los informes de precisión del modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [El [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Generar un informe de precisión de modelo](model-accuracy-report-generate.md)
>* [Configuración del informe de precisión del modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
