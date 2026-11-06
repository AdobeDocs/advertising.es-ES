---
title: Acerca de las simulaciones
description: Obtenga información acerca de simulaciones de portafolios.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
TQID: 'https://experienceleague.adobe.com/9B4gKrZnnUmgj0LzxwM2CIkJsIO9Pe9R8RDR4mAmIwo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 0%
---
# Acerca de las simulaciones

*característica de Beta*

Los informes de simulación muestran el valor marginal estimado de coste a objetivo, el coste, el número de clics y el valor objetivo que puede esperar para una cartera en varios niveles de gasto (coste) y los presupuestos diarios correspondientes u otros objetivos. Opcionalmente, puede [personalizar la vista](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) para ver métricas de tráfico adicionales, configuraciones de simulación y solo un tipo de simulación específico ([!UICONTROL Weekly] o [!UICONTROL Custom]).

<!--
 Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Tipos de simulaciones

* Simulación semanal automatizada

* Simulaciones personalizadas generadas por el usuario

### Simulación semanal automatizada

Search, Social y Commerce ejecutan automáticamente informes de simulación cada semana utilizando la configuración actual del portafolio. Las simulaciones semanales automatizadas solo están disponibles para los períodos en los que el portafolio esté [optimizado o activo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

Puede [descargar simulaciones semanales de hasta 100 portafolios para una fecha de ejecución seleccionada desde la vista [!UICONTROL Portfolios]](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#download-simulations), o [descargar simulaciones individuales desde la vista [!UICONTROL Simulations]](simulation-download.md).

#### Simulaciones semanales descargadas

Puede descargar simulaciones semanales como libros individuales o combinarlas en un libro. El informe de cada simulación incluye el objetivo de cada uno de los niveles de 20 pasos y el coste proyectado, los clics, los ingresos ponderados (valor objetivo) y las métricas de conversión del objetivo, según el objetivo correspondiente. La simulación calcula las 20 primeras filas de datos sin restricciones y las filas de datos restantes con restricciones.

#### Detalles de la simulación semanal en pantalla

Los detalles de la simulación en pantalla muestran perspectivas visuales y tabulares a nivel de portafolio. Para datos por campaña, grupos de anuncios, unidades de oferta o dispositivo, [descargue la simulación](simulation-download.md).

##### Visualización de gráfico

La vista de gráfico muestra el valor objetivo esperado u otra métrica especificada ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) para el objetivo de gasto para cada uno de los 20 niveles de gasto. El gráfico identifica el punto medio de destino y, opcionalmente, puede cambiar el punto medio de destino para ver los datos predichos mediante ese valor. Mantenga el cursor sobre cualquier punto del gráfico para ver los datos de ese punto.

Puede ver datos con restricciones, sin restricciones o ambas cosas. Cuando se ven datos con restricciones, la vista identifica esas restricciones encima del gráfico.

##### Vista de tabla

La vista de tabla muestra el gasto objetivo para cada uno de los 20 niveles de gasto. También incluye el coste estimado, el coste marginal al valor objetivo, los clics, el valor objetivo y las métricas de conversión correspondientes en el objetivo de la cartera para cada nivel de gasto. La tabla identifica el punto medio de destino y, opcionalmente, puede cambiar el punto medio de destino para ver los datos predichos mediante ese valor.

Puede ver datos con restricciones, sin restricciones o ambas cosas. Cuando se ven datos con restricciones, la vista identifica esas restricciones encima del gráfico.

##### Configuración de simulación

La vista muestra los ajustes de simulación de solo lectura debajo del gráfico o la tabla.

##### Configuración de Portfolio

Para ver la configuración de solo lectura del portafolio aplicable, haga clic en **[!UICONTROL Portfolio Settings]** en la esquina superior derecha.

### Simulaciones personalizadas generadas por el usuario

Puede crear un informe de simulación personalizado para un único portafolio [optimizado o activo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) usando la configuración actual del portafolio o usando la configuración personalizada del portafolio, con o sin restricciones de nivel de unidad de oferta aplicadas, para ver los resultados que esa configuración produciría sin cambiarla realmente. Por ejemplo, puede crear una simulación personalizada para ver el efecto de utilizar una estrategia de gasto o un presupuesto de aprendizaje diferentes sin tener en cuenta las restricciones activas en las unidades de oferta del portafolio. Puede ver el rendimiento estimado en los niveles de portafolio, campaña, unidad de oferta y dispositivo.

#### Simulaciones personalizadas descargadas

Puede descargar simulaciones personalizadas como libros individuales o combinarlas en un libro. El informe de cada simulación incluye una hoja de cálculo por cada nivel de entidad especificado (portafolios, campañas, grupos de anuncios y unidades de oferta) cuando los datos están disponibles para ese nivel. Cuando se especifican datos en el nivel de dispositivo, cada hoja de cálculo incluye una columna [!UICONTROL Device]. Cada hoja de cálculo incluye una fila para cada entidad aplicable y, cuando se solicitan datos de nivel de dispositivo, el tipo de dispositivo para cada uno de 20 pasos (por ejemplo, una fila por campaña). Los datos de cada fila incluyen la relación coste/ingresos marginal proyectada, el coste, los clics, los ingresos ponderados (valor objetivo), el tipo de dispositivo y las métricas de conversión del objetivo, en función del objetivo correspondiente. La hoja de cálculo de nivel de portafolio también incluye el objetivo para los niveles de paso y la hoja de cálculo de nivel de entidad incluye la red de publicidad, la cuenta, la campaña y (cuando corresponda) el grupo de publicidad.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### Detalles de simulación personalizados en pantalla

Los detalles de la simulación en pantalla muestran perspectivas visuales y tabulares a nivel de portafolio. Para datos por campaña, grupos de anuncios, unidades de oferta o dispositivo, [descargue la simulación](simulation-download.md).

#### Visualización de gráfico

La vista de gráfico muestra el valor objetivo esperado u otra métrica especificada ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) para el destino de gasto durante el número especificado de niveles de gasto (pasos) para la simulación. El gráfico identifica el punto medio de destino. Mantenga el cursor sobre cualquier punto del gráfico para ver los datos de ese punto.

Cuando la simulación tiene en cuenta las restricciones, la vista identifica las restricciones por encima del gráfico.

##### Vista de tabla

La vista de tabla muestra el gasto objetivo para cada uno de los niveles de gasto (pasos) especificados para la simulación. También muestra el coste estimado, el coste marginal al valor objetivo, los clics, el valor objetivo y las métricas de conversión correspondientes en el objetivo de la cartera para cada nivel de gasto. La tabla identifica el punto medio de destino.

Cuando la simulación tiene en cuenta las restricciones, la vista identifica las restricciones por encima del gráfico.

##### Configuración de simulación

La vista muestra los ajustes de simulación de solo lectura debajo del gráfico o la tabla.

##### Configuración de Portfolio

Para ver la configuración de solo lectura del portafolio aplicable, haga clic en **[!UICONTROL Portfolio Settings]** en la esquina superior derecha.

## La vista [!UICONTROL Simulations]

La vista [!UICONTROL Simulations] enumera simulaciones semanales y simulaciones personalizadas. El administrador y otros tipos de usuarios <!-- Verify which --> pueden ver simulaciones personalizadas creadas por otros usuarios. El resto de usuarios solo pueden ver las simulaciones personalizadas que crean.

La tabla de datos muestra el progreso de cada simulación; el [!UICONTROL Target Midpoint] de cada fila; y columnas para predicciones de costos/impresiones/clics/valores objetivos, valores reales y precisión. Si lo desea, puede agregar columnas personalizadas adicionales (incluidas las métricas de alza, como el valor objetivo real dividido por el coste).

### Acciones disponibles {#simulations-actions}

* [Personalice la vista](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) para incluir métricas adicionales, incluidas las impresiones estimadas; el costo real, los clics, las impresiones y el valor objetivo; el valor costo-objetivo; la precisión de costo, la precisión de clic y la precisión del valor objetivo; y la diferencia (delta) entre el valor objetivo previsto y el real y el valor costo-objetivo. También puede incluir columnas para la mayoría de los ajustes de simulación y el tipo de simulación ([!UICONTROL Custom] o [!UICONTROL Weekly]).

* [Generar una simulación personalizada](simulation-create.md#simulation-create) para un único portafolio, utilizando la configuración actual del portafolio como valores predeterminados.

* [Vuelva a ejecutar hasta 10 simulaciones con la configuración existente](simulation-create.md#rerun-a-simulation-with-the-existing-settings). Search, Social y Commerce omiten las simulaciones con un estado de [!UICONTROL Queued] o [!UICONTROL In Progress].

* [Ver una simulación semanal o personalizada en pantalla](simulation-view.md).

* [Descargue hasta 10 simulaciones semanales y personalizadas](simulation-download.md) como un solo libro de [!DNL Microsoft Excel] o como libros separados en un archivo ZIP.

* Con el botón [!UICONTROL Spend Planner], abra la herramienta Recomendación de gastos heredada, que le ayuda a identificar la distribución óptima del gasto en todos los portafolios.

## Prácticas recomendadas

Monitorice los informes de simulación en las siguientes situaciones:

* Antes de iniciar un portafolio, para calcular el rendimiento que puede esperar con la configuración correspondiente del portafolio; use al menos dos semanas de datos. Si los resultados de la simulación indican un rendimiento menor del que cabría esperar en función de los datos históricos de las campañas incluidas, investigue y resuelva los problemas antes de lanzar el catálogo de productos.

* Después de cualquier cambio importante en un portafolio, como añadir una campaña o cambiar el objetivo. Si realiza cambios en la fecha de inicio del modelado del portafolio, en la ponderación de una métrica de conversión o en el valor de clic de un objetivo, espere hasta después de las 17:00 PST del día siguiente para ejecutar la simulación cuando estén disponibles los modelos de ingresos y costes actualizados.

* Monitorizar periódicamente las tendencias de rendimiento en el nivel de métrica de conversión.

>[!MORELIKETHIS]
>
>* [Ejecutar o volver a ejecutar una simulación](simulation-create.md)
>* [Ver detalles de la simulación](simulation-view.md)
>* [Descargar simulaciones](simulation-download.md)
