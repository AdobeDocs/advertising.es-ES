---
title: Acerca de las simulaciones
description: Obtenga información acerca de simulaciones de portafolios.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
source-git-commit: 73528e2aa905216584d1aa294f5581d2bca88432
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 0%

---

# Acerca de las simulaciones

*característica de Beta*

Los informes de simulación muestran el valor marginal estimado de coste a objetivo, el coste, el número de clics y el valor objetivo que puede esperar para una cartera en varios niveles de gasto (coste) y los presupuestos diarios correspondientes u otros objetivos. Opcionalmente, puede [personalizar la vista](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) para ver métricas de tráfico adicionales, configuraciones de simulación y solo un tipo de simulación específico ([!UICONTROL Weekly] o [!UICONTROL Custom]).

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Tipos de simulaciones

* Simulación semanal automatizada

* Simulaciones personalizadas generadas por el usuario

### Simulación semanal automatizada

Los informes de simulación se ejecutan automáticamente cada semana utilizando la configuración actual del portafolio. Las simulaciones semanales automatizadas solo están disponibles para los períodos en los que el portafolio esté [optimizado o activo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

#### Simulaciones semanales descargadas

Cada simulación semanal descargada consta de un libro de trabajo. Cada libro incluye el objetivo para cada uno de los 20 niveles de paso y el coste proyectado, los clics, los ingresos ponderados (valor objetivo) y las métricas de conversión incluidas en el objetivo, según el objetivo correspondiente. No se aplicaron restricciones a las 20 primeras filas de datos, mientras que se aplicaron restricciones al resto de las filas de datos.

#### Detalles de la simulación semanal en pantalla

Los detalles de la simulación en pantalla muestran perspectivas visuales y tabulares a nivel de portafolio. Para datos por campaña, grupos de anuncios, unidades de oferta o dispositivo, [descargue la simulación](simulation-download.md).

##### Visualización de gráfico

La vista de gráfico muestra el valor objetivo esperado u otra métrica especificada ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) para el objetivo de gasto para cada uno de los 20 niveles de gasto. El punto medio de destino se identifica y, opcionalmente, puede cambiar el punto medio de destino para ver los datos predichos utilizando ese valor. Mantenga el cursor sobre cualquier punto del gráfico para ver los datos de ese punto.

Puede ver los datos con y sin restricciones aplicadas, con restricciones aplicadas y sin restricciones aplicadas. Cuando se ven datos que tienen en cuenta las restricciones, las restricciones aplicadas se identifican encima del gráfico.

##### Vista de tabla

La vista de tabla muestra el gasto objetivo para cada uno de los 20 niveles de gasto. También incluye el coste estimado, el coste marginal al valor objetivo, los clics, el valor objetivo y las métricas de conversión correspondientes en el objetivo de la cartera para cada nivel de gasto. El punto medio de destino se identifica y, opcionalmente, puede cambiar el punto medio de destino para ver los datos predichos utilizando ese valor.

Puede ver los datos con y sin restricciones aplicadas, con restricciones aplicadas y sin restricciones aplicadas. Cuando se ven datos que tienen en cuenta las restricciones, las restricciones aplicadas se identifican encima del gráfico.

##### Configuración de simulación

Los ajustes de simulación se muestran como de solo lectura debajo del gráfico o la tabla.

##### Configuración de Portfolio

Para ver la configuración de solo lectura del portafolio aplicable, haga clic en **[!UICONTROL Portfolio Settings]** en la esquina superior derecha.

### Simulaciones personalizadas generadas por el usuario

Puede crear un informe de simulación personalizado para un único portafolio [optimizado o activo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) usando la configuración actual del portafolio o usando la configuración personalizada del portafolio, con o sin restricciones de nivel de unidad de oferta aplicadas, para ver los resultados que esa configuración produciría sin cambiarla realmente. Por ejemplo, puede crear una simulación personalizada para ver el efecto de utilizar una estrategia de gasto o un presupuesto de aprendizaje diferentes sin tener en cuenta las restricciones activas en las unidades de oferta del portafolio. Puede ver el rendimiento estimado en los niveles de portafolio, campaña, unidad de oferta y dispositivo.

#### Simulaciones personalizadas descargadas

Cada simulación personalizada descargada consta de un libro. Cada libro incluye una hoja de cálculo para cada nivel de simulación de entidad especificado (portafolios, campañas, grupos de anuncios y unidades de oferta) cuando los datos están disponibles para ese nivel. Cuando se especifican datos en el nivel de dispositivo, cada hoja de cálculo incluye una columna [!UICONTROL Device]. Cada hoja de cálculo incluye una fila con datos para cada entidad aplicable y (cuando se especifica para el informe) y tipo de dispositivo para cada uno de 20 pasos (por ejemplo, una fila por campaña). Los datos de cada fila incluyen la relación coste/ingresos marginal proyectada, el coste, los clics, los ingresos ponderados (valor objetivo), el tipo de dispositivo y las métricas de conversión incluidas en el objetivo, en función del objetivo correspondiente. La hoja de cálculo de nivel de portafolio también incluye el objetivo para los niveles de paso y la hoja de cálculo de nivel de entidad incluye la red de publicidad, la cuenta, la campaña y (cuando corresponda) el grupo de publicidad.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### Detalles de simulación personalizados en pantalla

Los detalles de la simulación en pantalla muestran perspectivas visuales y tabulares a nivel de portafolio. Para datos por campaña, grupos de anuncios, unidades de oferta o dispositivo, [descargue la simulación](simulation-download.md).

#### Visualización de gráfico

La vista de gráfico muestra el valor objetivo esperado u otra métrica especificada ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) para el destino de gasto durante el número especificado de niveles de gasto (pasos) para la simulación. Se identifica el punto medio objetivo. Mantenga el cursor sobre cualquier punto del gráfico para ver los datos de ese punto.

Cuando la simulación se ha creado teniendo en cuenta las restricciones, las restricciones aplicadas se identifican encima del gráfico.

##### Vista de tabla

La vista de tabla muestra el gasto objetivo para cada uno de los niveles de gasto (pasos) especificados para la simulación. También muestra el coste estimado, el coste marginal al valor objetivo, los clics, el valor objetivo y las métricas de conversión correspondientes en el objetivo de la cartera para cada nivel de gasto. Se identifica el punto medio objetivo.

Cuando la simulación se ha creado teniendo en cuenta las restricciones, las restricciones aplicadas se identifican encima del gráfico.

##### Configuración de simulación

Los ajustes de simulación se muestran como de solo lectura debajo del gráfico o la tabla.

##### Configuración de Portfolio

Para ver la configuración de solo lectura del portafolio aplicable, haga clic en **[!UICONTROL Portfolio Settings]** en la esquina superior derecha.

## La vista [!UICONTROL Simulations]

La vista [!UICONTROL Simulations] enumera simulaciones semanales y simulaciones personalizadas. El administrador y otros tipos de usuarios <!-- Verify which --> pueden ver simulaciones personalizadas creadas por otros usuarios. El resto de usuarios solo pueden ver las simulaciones personalizadas que crean.

La tabla de datos incluye el progreso de cada simulación, una columna [!UICONTROL Target Midpoint] rellenada para cada fila y columnas para predicciones de costos, impresiones, clics, valores objetivos, y precisión. Si lo desea, puede agregar columnas personalizadas adicionales (incluidas las métricas de alza, como el valor objetivo real dividido por el coste).

### Acciones disponibles {#simulations-actions}

* [Personalice la vista](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) para incluir métricas adicionales, incluidas las impresiones estimadas; el costo real, los clics, las impresiones y el valor objetivo; el valor costo-objetivo; la precisión de costo, la precisión de clic y la precisión del valor objetivo; y la diferencia (delta) entre el valor objetivo previsto y el real y el valor costo-objetivo. También puede incluir columnas para la mayoría de los ajustes de simulación y el tipo de simulación ([!UICONTROL Custom] o [!UICONTROL Weekly]).

* [Generar o volver a ejecutar una simulación personalizada](simulation-create.md) para un solo portafolio. Puede crear una nueva simulación o volver a generar una simulación existente en la lista.

* [Ver una simulación semanal o personalizada en pantalla](simulation-view.md).

* [Descargar simulaciones semanales y personalizadas](simulation-download.md) como [!DNL Microsoft Excel] libros en archivos ZIP.

* Con el botón [!UICONTROL Spend Planner], abra la herramienta Recomendación de gastos heredada, que le ayuda a identificar la distribución óptima del gasto en todos los portafolios.

## Prácticas recomendadas

Monitorice los informes de simulación en las siguientes situaciones:

* Antes de iniciar un portafolio, para calcular el rendimiento que puede esperar con la configuración correspondiente del portafolio; use al menos dos semanas de datos. Si los resultados de la simulación indican un rendimiento menor del que cabría esperar en función de los datos históricos de las campañas incluidas, investigue y resuelva los problemas antes de lanzar el catálogo de productos.

* Después de cualquier cambio importante en un portafolio, como añadir una campaña o cambiar el objetivo. Si realiza cambios en la fecha de inicio del modelado del portafolio, en el peso de una métrica de conversión o en el valor de clic de un objetivo, espere hasta después de 17:00 PST del día siguiente para ejecutar la simulación, cuando estén disponibles los modelos actualizados de costos e ingresos.

* Monitorizar periódicamente las tendencias de rendimiento en el nivel de métrica de conversión.

>[!MORELIKETHIS]
>
>* [Ejecutar o volver a ejecutar una simulación](simulation-create.md)
>* [Ver detalles de la simulación](simulation-view.md)
>* [Descargar simulaciones](simulation-download.md)
