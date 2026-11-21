---
title: (Nueva IU) Información de Advertising
description: Aprenda a configurar y ver paneles de insight de publicidad para comprobar la precisión, el rendimiento, las simulaciones, los límites presupuestarios y las conversiones de los modelos.
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%
---
# (Nueva IU) Información de Advertising

Las perspectivas de Advertising presentan datos visuales y procesables para ayudarle a evaluar el rendimiento del portafolio, identificar problemas de optimización y comparar los datos de conversión. Cada insight se genera bajo demanda y se muestra como un panel en pantalla.

La vista **[!UICONTROL Reports]>[!UICONTROL Insights]** muestra las perspectivas disponibles en **[!UICONTROL Dashboards]**. El encabezado de la página es **[!UICONTROL Advertising Insights]**.

>[!NOTE]
>
>En esta página se describen los paneles de insight de la nueva interfaz de usuario beta. La disponibilidad depende de su acceso y de las perspectivas disponibles para el anunciante seleccionado. Las [perspectivas heredadas de Advertising](/help/search-social-commerce/legacy-ui/advertising-insights/insight-about.md) incluyen un conjunto diferente de análisis y procedimientos para los archivos generados.

## Tipos de perspectivas {#insight-types}

| Insight | Descripción |
| --- | --- |
| [!UICONTROL Model Accuracy] | Identifica la eficacia con la que Search, Social y Commerce predicen los costes y los ingresos de un portafolio. Puede revisar la precisión del modelo en los niveles de portafolio, red de publicidad y campaña. |
| [!UICONTROL Performance Insights] | Compara el rendimiento del portafolio antes y después de un cambio de estado de optimización, un cambio objetivo o una fecha especificada. El tablero incluye resúmenes de rendimiento, una auditoría de los cambios que afectan a la optimización, comparaciones de campañas, tendencias y análisis de valor objetivo. |
| [!UICONTROL Portfolio Simulation Analysis] | Compara una simulación personalizada existente con el rendimiento real. Puede revisar los datos de cartera y campaña, analizar la precisión de la simulación y explorar el rendimiento estimado en diferentes niveles de gasto de destino. |
| [!UICONTROL Campaign Budget Cap Analysis] | Indica si el gasto de un portafolio estaba limitado por los límites presupuestarios de la campaña. El panel incluye gasto restringido, campañas afectadas, impresiones perdidas estimadas, tendencias diarias y de día de la semana y recomendaciones para la configuración del portafolio. |
| [!UICONTROL Modeled Conversions] | Compara los valores de conversión de Adobe con los valores notificados por la red de publicidad, incluidos los datos modelados. Puede analizar cuentas, portafolios o campañas y comparar los valores medidos por Adobe y por Adobe y modelados con los valores notificados por el editor. |
| [!UICONTROL Delayed Revenue Analysis] | Mide el retraso de conversión (el tiempo transcurrido entre un clic o una visualización de anuncio y una conversión posterior) y muestra su impacto en el valor objetivo, el retorno de la inversión (ROI) y la precisión del modelo. El análisis solo está disponible para portafolios con atribución de ingresos basada en clics o visualizaciones. |

## Generación de un insight {#insight-generate}

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Insights]**.

1. Haga clic en la insight que desee generar.

1. En el panel **[!UICONTROL Configure]**, especifique la [configuración de insight](#insight-settings).

1. Haga clic en **[!UICONTROL Generate Insight]**.

   El panel de configuración se cierra y el panel muestra el análisis.

1. Revise los [resultados de insight](#insight-results).

Para cambiar la configuración, haga clic en **[!UICONTROL Configure]**, cambie los valores y haga clic de nuevo en **[!UICONTROL Generate Insight]**. Para volver a la lista de insight, haga clic en **[!UICONTROL Analysis List]** en la ruta de exploración.

## Configuración de insight {#insight-settings}

### Precisión de modelo {#model-accuracy-settings}

* **[!UICONTROL Portfolios]:** Seleccione un portafolio.

* **[!UICONTROL Choose Revenue Type]:** Seleccione **[!UICONTROL Actual Revenue]** (predeterminado) o **[!UICONTROL Delayed Revenue]**.

* **[!UICONTROL Date Range]:** Seleccione las fechas a analizar. Consulte [Configuración del intervalo de fechas](#date-range-settings).

### Perspectivas de rendimiento {#performance-insights-settings}

* **[!UICONTROL Portfolios]:** Seleccione un portafolio.

* **[!UICONTROL Revenue Type]:** Seleccione **[!UICONTROL Actual Revenue]** (predeterminado) o **[!UICONTROL Delayed Revenue]**.

* **Fecha del evento:** Seleccione el tipo de fecha en torno a la cual comparar el rendimiento:

  * **[!UICONTROL Optimization Status Change (last 90 days)]** (valor predeterminado): seleccione una fecha de cambio de estado de optimización disponible para el portafolio.

  * **[!UICONTROL Objective Change Date (last 90 days)]:** Seleccione una fecha de cambio objetivo disponible para el portafolio.

  * **[!UICONTROL Specific Date]:** Especifique una fecha con el selector de fechas.

  Seleccione la fecha del evento antes de configurar los periodos de comparación. Si no hay fechas de evento disponibles para el portafolio seleccionado, puede usar **[!UICONTROL Specific Date]**.

* **[!UICONTROL Pre Days]:** Especifique el período antes de la fecha del evento:

  * Seleccione **[!UICONTROL 7]** (el valor predeterminado), **[!UICONTROL 14]** o **[!UICONTROL 30]**.

  * Seleccione **[!UICONTROL Pre Start Date]** y especifique **[!UICONTROL Custom Pre Date]**.

  * Seleccione **[!UICONTROL Custom Pre Days]** e introduzca un número positivo de días.

* **[!UICONTROL Post Days]:** Especifique el período después de la fecha del evento:

  * Seleccione **[!UICONTROL 7]** (el valor predeterminado), **[!UICONTROL 14]** o **[!UICONTROL 30]**.

  * Seleccione **[!UICONTROL Post End Date]** y especifique **[!UICONTROL Custom Post Date]**.

  * Seleccione **[!UICONTROL Custom Post Days]** e introduzca un número positivo de días.

  La fecha del evento en sí no se incluye en ningún periodo de comparación.

* **[!UICONTROL Date Exclusion]:** (opcional) Excluir fechas del análisis:

  1. Haga clic en **[!UICONTROL Select Dates]**.

  1. Seleccione las fechas que desea excluir:

     * Haga clic en fechas individuales para seleccionarlas o anularlas.

     * Mantenga presionado **[!UICONTROL Shift]** mientras hace clic para seleccionar un rango.

     * Para quitar todas las exclusiones, haga clic en **[!UICONTROL Clear All]**.

  1. Haga clic en **[!UICONTROL Done]** cuando haya terminado.

### Análisis de simulación de Portfolio {#simulation-settings}

* **[!UICONTROL Portfolios]:** Seleccione un portafolio con una simulación personalizada existente.

* **[!UICONTROL Simulation Date]:** Seleccione la fecha de la simulación que desea analizar. Si hay varias simulaciones disponibles para esa fecha, seleccione también la simulación por nombre.

  Si no hay simulaciones personalizadas disponibles, [genere una simulación personalizada](/help/search-social-commerce/manage/portfolios/portfolio-create-simulation.md) antes de usar este insight.

* **[!UICONTROL Actual Days]:** Seleccione **[!UICONTROL 7]** (el valor predeterminado), **[!UICONTROL 14]** o **[!UICONTROL 30]** días de datos de rendimiento reales. Para especificar otro número, seleccione **[!UICONTROL Enter Actual Days]** e introduzca un valor entre 1 y 90.

* **[!UICONTROL Type]:** Seleccione **[!UICONTROL Transaction Date]** (el valor predeterminado) o **[!UICONTROL Click Date]** para la atribución de conversión.

### Análisis del límite presupuestario de campaña {#budget-cap-settings}

* **[!UICONTROL Portfolio]:** Seleccione un portafolio.

* **[!UICONTROL Date Range]:** Seleccione las fechas a analizar. Consulte [Configuración del intervalo de fechas](#date-range-settings).

### Conversiones modeladas {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]:** Seleccione **[!UICONTROL Account]**, **[!UICONTROL Portfolio]** (predeterminado) o **[!UICONTROL Campaign]**.

* **[!UICONTROL Accounts]**, **[!UICONTROL Portfolios]** o **[!UICONTROL Campaigns]:** Seleccione las entidades aplicables para el nivel de análisis. Puede seleccionar varias entidades.

* **[!UICONTROL Date Range]:** Seleccione las fechas a analizar. Consulte [Configuración del intervalo de fechas](#date-range-settings).

* **[!UICONTROL Adobe Conversion]:** Seleccione la propiedad de conversión de Adobe que desea comparar.

* **[!UICONTROL Publisher Conversion]:** Seleccione la propiedad de conversión del editor que desea comparar.

  Las propiedades de conversión disponibles dependen del nivel de análisis, las entidades seleccionadas y el intervalo de fechas. Ambas propiedades de conversión son necesarias para la comparación.

### Análisis de ingresos retrasados {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]:** Seleccione un portafolio con atribución de ingresos basada en clics o de visualizaciones.

* **[!UICONTROL Date Range]:** Seleccione las fechas a analizar. Consulte [Configuración del intervalo de fechas](#date-range-settings).

### Configuración de intervalo de fechas {#date-range-settings}

Para obtener información con una configuración de **[!UICONTROL Date Range]**, seleccione **[!UICONTROL Last 7 days]** (el valor predeterminado), **[!UICONTROL Last 14 days]** o **[!UICONTROL Last 30 days]**.

Para especificar otro período, seleccione **[!UICONTROL Custom Date]** e introduzca **[!UICONTROL Start Date]** y **[!UICONTROL End Date]**. Puede seleccionar fechas dentro de los últimos 90 días, hasta la fecha actual.

## Ver resultados de insight {#insight-results}

### Precisión de modelo {#model-accuracy-results}

Revise los detalles del portafolio y utilice las siguientes pestañas:

* **[!UICONTROL Portfolio]:** Revisar la precisión del modelo a nivel de portafolio y las comparaciones presupuestarias.

* **[!UICONTROL Ad Network]:** Revisar la precisión del modelo y las comparaciones presupuestarias por red de anuncios.

* **[!UICONTROL Campaigns]:** Revisar la precisión y el destino del modelo en el nivel de campaña en comparación con el rendimiento real.

* **[!UICONTROL Playground Beta]:** Compare la precisión del modelo para varias campañas.

Para los gráficos de precisión de campaña, seleccione **[!UICONTROL Comparison Options]** y **[!UICONTROL Campaign]**. En **[!UICONTROL Playground Beta]**, puede seleccionar varias campañas. Haga clic en **[!UICONTROL Table View]** para cambiar entre un gráfico y sus datos subyacentes.

### Perspectivas de rendimiento {#performance-insights-results}

El panel muestra **[!UICONTROL Pre Period]** y **[!UICONTROL Post Period]**, las métricas de rendimiento agregadas para ambos períodos y los detalles del portafolio.

**[!UICONTROL Audit Trail]** resume los cambios a los factores que afectan a la optimización, como el presupuesto de portafolio, la estrategia de gasto, el gasto mínimo en campaña y el límite de gasto múltiple. Cuando haya cambios con detalles disponibles, haga clic en **[!UICONTROL View Details]** para inspeccionarlos.

Utilice las fichas **[!UICONTROL Comparative Overview]**, **[!UICONTROL Campaigns Comparison]**, **[!UICONTROL Trends & Patterns]**, **[!UICONTROL Deep Analysis]** y **[!UICONTROL Objective Value And Analysis]** para explorar la comparación.

### Análisis de simulación de Portfolio {#simulation-results}

Revise los detalles de la simulación y utilice las siguientes pestañas:

* **[!UICONTROL Portfolio]:** revisar datos de simulación a nivel de portafolio. En esta pestaña:

  * **[!UICONTROL Simulation Data]** muestra las métricas de simulación y el rendimiento de gasto de destino.

  * **[!UICONTROL Simulation Vs Actual]** compara el rendimiento real y el simulado.

  * **[!UICONTROL Try New Target]** le permite especificar un gasto de destino en **[!UICONTROL Explore Target Spend]** para ver los clics, costos e ingresos estimados. Este es un análisis del rendimiento estimado; no cambia el objetivo de gasto de la cartera.

* **[!UICONTROL Campaigns]:** Revisar comparaciones de simulación a nivel de campaña.

* **[!UICONTROL Accuracy Analysis]:** Revisar precisión de simulación.

### Análisis del límite presupuestario de campaña {#budget-cap-results}

Revise los detalles del portafolio y las métricas de resumen:

* **[!UICONTROL Total Capped Spend]:** Porcentaje de gasto en días en que se alcanzaron los presupuestos de campaña.

* **[!UICONTROL Capped Campaigns]:** Número de campañas que alcanzan sus presupuestos al menos una vez.

* **[!UICONTROL Est. Lost Impressions]:** impresiones estimadas omitidas debido a los límites de presupuesto.

* **[!UICONTROL Peak Capping Day]:** El día de la semana con el gasto más limitado.

Los gráficos **[!UICONTROL Spend on Capped Campaigns by Day]** y **[!UICONTROL Capped Spend by Weekday]** muestran tendencias de límite. Revise **[!UICONTROL Capped Campaign Performance]** para obtener detalles de la campaña y **[!UICONTROL Portfolio Settings Recommendations]** para ver los cambios de configuración sugeridos.

### Conversiones modeladas {#modeled-conversions-results}

Revise las siguientes tablas para las entidades seleccionadas y el intervalo de fechas:

* **[!UICONTROL Adobe Measured vs Publisher Conversions]:** compara los valores de conversión medidos directamente por Adobe con los valores notificados por el editor, que incluyen datos medidos y modelados.

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]:** compara los valores de conversión medidos y modelados por Adobe con los valores notificados por el editor.

Ambas tablas incluyen el nombre y el ID de la entidad, el valor de Adobe, el valor registrado por el editor, la diferencia absoluta y la diferencia porcentual.

Si no hay datos disponibles, compruebe que ha seleccionado las propiedades de conversión y que existen datos para las entidades y el intervalo de fechas seleccionados.

### Análisis de ingresos retrasados {#delayed-revenue-results}

**[!UICONTROL Key Insights Summary]** muestra los ingresos ponderados esperados (ahora denominados &quot;[valor objetivo](/help/search-social-commerce/glossary.md#o-p)&quot;), el retorno de la inversión y la información de precisión del modelo.

La sección **[!UICONTROL Conversion Lag Breakdown by Revenue Property]** muestra el porcentaje de conversiones realizadas el día 0 y los días 3, 7, 14 y 28 para cada propiedad de ingresos.

En **[!UICONTROL Performance Over Time]**, seleccione **[!UICONTROL Objective Value]**, **[!UICONTROL ROI]** o **[!UICONTROL Model Accuracy]** para comparar la fecha de clic, la fecha de transacción y el rendimiento esperado. Haga clic en **[!UICONTROL Table View]** para cambiar entre el gráfico y sus datos subyacentes.

En **[!UICONTROL Metrics Definitions]**, haga clic en **[!UICONTROL Show]** para ver las explicaciones de las fechas y métricas utilizadas en el análisis, o en **[!UICONTROL Hide]** para contraerlas.

Si el análisis no es aplicable, seleccione un portafolio con atribución de ingresos basada en clics o de visualizaciones. Si no hay datos disponibles, compruebe que existan datos para el portafolio y el intervalo de fechas seleccionados.
