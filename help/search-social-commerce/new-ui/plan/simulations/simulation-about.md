---
title: Acerca de las simulaciones
description: Obtenga información acerca de simulaciones de portafolios.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Acerca de las simulaciones

*característica de Beta*

Los informes de simulación muestran el valor marginal estimado de coste a objetivo, el coste, el número de clics y el valor objetivo que puede esperar para una cartera en varios niveles de gasto (coste) y los presupuestos diarios correspondientes u otros objetivos. Si lo desea, puede personalizar la vista <!-- add link --> para ver métricas de tráfico adicionales, configuraciones de simulación y solo un tipo de simulación específico ([!UICONTROL Weekly] o [!UICONTROL Custom]).

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Tipos de simulaciones

* **Simulaciones semanales automatizadas:** Los informes de simulación se ejecutan automáticamente cada semana utilizando la configuración actual del portafolio. Las simulaciones semanales automatizadas solo están disponibles para los períodos en los que el portafolio esté [optimizado o activo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

  Cada simulación semanal descargada consta de un libro de trabajo. Cada libro incluye el objetivo para cada uno de los 20 niveles de paso y el coste proyectado, los clics, los ingresos ponderados (valor objetivo) y las métricas de conversión incluidas en el objetivo, según el objetivo correspondiente. No se aplicaron restricciones a las 20 primeras filas de datos, mientras que se aplicaron restricciones al resto de las filas de datos.

* **Simulaciones personalizadas generadas por el usuario:** Puede crear un informe de simulación personalizado para un único portafolio [optimizado o activo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) utilizando la configuración actual del portafolio o utilizando la configuración personalizada del portafolio para ver los resultados que esa configuración produciría sin cambiarla realmente. Por ejemplo, puede crear una simulación personalizada para ver el efecto de usar una estrategia de gasto o un presupuesto de aprendizaje diferentes<!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->. Puede ver el rendimiento estimado en los niveles de portafolio, campaña, unidad de oferta y dispositivo. Las simulaciones personalizadas heredan la configuración de gasto de restricciones del portafolio.

  >[!NOTE]
  >
  > El nuevo formulario de simulación personalizado utiliza los mismos ajustes que el formulario heredado, excepto que hereda la información de restricciones de unidad de oferta de los ajustes del portafolio. No tiene la opción de ignorar las restricciones de unidad de oferta, como lo hizo en la página antigua de configuración de simulación personalizada.

  Cada simulación personalizada descargada consta de un libro. Cada libro incluye una hoja de cálculo para cada nivel de simulación de entidad especificado (portafolios, campañas, grupos de anuncios y unidades de oferta) cuando los datos están disponibles para ese nivel. Cuando se especifican datos en el nivel de dispositivo, cada hoja de cálculo incluye una columna [!UICONTROL Device]. Cada hoja de cálculo incluye una fila con datos para cada entidad aplicable y (cuando se especifica para el informe) y tipo de dispositivo para cada uno de 20 pasos (por ejemplo, una fila por campaña). Los datos de cada fila incluyen la relación coste/ingresos marginal proyectada, el coste, los clics, los ingresos ponderados (valor objetivo), el tipo de dispositivo y las métricas de conversión incluidas en el objetivo, en función del objetivo correspondiente. La hoja de cálculo de nivel de portafolio también incluye el objetivo para los niveles de paso y la hoja de cálculo de nivel de entidad incluye la red de publicidad, la cuenta, la campaña y (cuando corresponda) el grupo de publicidad.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

## La vista [!UICONTROL Simulations]

La vista [!UICONTROL Simulations] enumera simulaciones semanales y simulaciones personalizadas. El administrador y otros tipos de usuarios <!-- Verify which --> pueden ver simulaciones personalizadas creadas por otros usuarios. El resto de usuarios solo pueden ver las simulaciones personalizadas que crean.

La tabla de datos incluye el progreso de cada simulación, una columna [!UICONTROL Target Midpoint] rellenada para cada fila y columnas para predicciones de costos, impresiones, clics, valores objetivos, y precisión. Si lo desea, puede agregar columnas personalizadas adicionales (incluidas las métricas de alza, como el valor objetivo real dividido por el coste).

### Acciones disponibles {#simulations-actions}

* [Personalice la vista](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) para incluir métricas adicionales, incluidas las impresiones estimadas; el costo real, los clics, las impresiones y el valor objetivo; el valor costo-objetivo; la precisión de costo, la precisión de clic y la precisión del valor objetivo; y la diferencia (delta) entre el valor objetivo previsto y el real y el valor costo-objetivo. También puede incluir columnas para la mayoría de los ajustes de simulación y el tipo de simulación ([!UICONTROL Custom] o [!UICONTROL Weekly]).

* [Generar o volver a ejecutar una simulación personalizada](simulation-create.md) para un solo portafolio. Puede crear una nueva simulación o volver a generar una simulación existente en la lista.

* [Descargar simulaciones semanales y personalizadas](simulation-download.md) como [!DNL Microsoft Excel] libros en archivos ZIP.

* Con el botón [!UICONTROL Spend Planner], abra la herramienta Recomendación de gastos heredada, que le ayuda a identificar la distribución óptima del gasto en todos los portafolios.

## Prácticas recomendadas

Monitorice los informes de simulación en las siguientes situaciones:

* Antes de iniciar un portafolio, para calcular el rendimiento que puede esperar con la configuración correspondiente del portafolio; use al menos dos semanas de datos. Si los resultados de la simulación indican un rendimiento menor del que cabría esperar en función de los datos históricos de las campañas incluidas, investigue y resuelva los problemas antes de lanzar el catálogo de productos.

* Después de cualquier cambio importante en un portafolio, como añadir una campaña o cambiar el objetivo. Si realiza cambios en la fecha de inicio del modelado del portafolio, en la ponderación de una métrica de conversión o en el valor de clic de un objetivo, espere hasta después de las 17:00 PST del día siguiente para ejecutar la simulación cuando estén disponibles los modelos de ingresos y costes actualizados.

* Monitorizar periódicamente las tendencias de rendimiento en el nivel de métrica de conversión.

>[!MORELIKETHIS]
>
>* [Ejecutar o volver a ejecutar una simulación](simulation-create.md)
>* [Descargar simulaciones](simulation-download.md)
