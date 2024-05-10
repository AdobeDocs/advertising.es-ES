---
title: DSP Optimización de las campañas con la
description: DSP Descubra cómo optimiza los paquetes en sus campañas.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# DSP Optimización de las campañas con Advertising

DSP Esta página describe cómo funciona el motor de optimización de la, que funciona con [!DNL Adobe Sensei], optimiza los paquetes de las campañas. Para obtener sugerencias y trucos sobre cómo optimizar manualmente las campañas, póngase en contacto con el equipo de cuenta de Adobe. <!-- add link to trading playbook if we add it to help -->

Los objetivos de optimización de paquetes operan en dos niveles:

* DSP Para cada paquete: asigna el presupuesto a cada ubicación dentro del paquete en función del rendimiento de la ubicación con respecto al KPI seleccionado.

* DSP Para cada colocación/subasta del paquete: calcula el valor de KPI económico en tiempo real de cada subasta por cada colocación y, a continuación, utiliza este valor para determinar la oferta.

  >[!NOTE]
  >
  >El valor económico se puede ponderar fuertemente en función de lo bien que esté gastando una colocación. Si una ubicación está detrás de su objetivo de gasto, entonces se le permite comprar subastas de menor calidad. Si una ubicación cumple fácilmente su objetivo de gasto, el enfoque cambia a subastas de mayor calidad.

## Optimización de paquetes

DSP Puede optimizar su envío de dos formas fundamentales, con 20 variaciones disponibles para alinearse con su objetivo de rendimiento específico. Puede elegir entre lo siguiente:

* Priorizar la tasa de rendimiento

* Priorice el equilibrio entre la eficiencia de costes y la tasa de rendimiento

Consulte [Objetivos de optimización y cómo utilizarlos](optimization-goals.md) para determinar qué objetivo de optimización puede ayudarle a lograr sus KPI.

### Paquetes que dan prioridad a la tasa de rendimiento

DSP Para los objetivos de optimización que dan prioridad a la tasa de rendimiento, predice el rendimiento de cada subasta y siempre oferta en la puja máxima. Algunos ejemplos de objetivos de optimización aplicables son [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate], etc.

Este modo de optimización funciona bien si:

* Ya conoce el nivel de CPM efectivo/aceptable (por ejemplo, un valor de referencia histórico).

* Está dispuesto a ajustar manualmente la variable [!UICONTROL Max Bid] para cada ubicación si experimenta desafíos con el escalado.

* Está priorizando la escala por sobre la eficiencia.

#### Lógica de ritmo {#pacing-logic-performance}

* Si el gasto va a buen ritmo, las pujas se vuelven más selectivas, por lo que solo se puja en las subastas en las que se prevé que las tasas de rendimiento sean altas.

* Si el gasto va por detrás del ritmo, las pujas se vuelven menos selectivas, por lo que se puede pujar en subastas en las que se predice que tendrán tasas de rendimiento más bajas para alcanzar el objetivo de ritmo.

#### Sombreado de puja/precio de liquidación {#clearing-price-performance}

DSP Después de ejecutar la lógica de ritmo, ejecuta la oferta propuesta a través de un modelo de predicción de precios de compensación. Si la predicción indica que la oferta se puede reducir con una disminución mínima de la tasa de ganancia, la oferta se reducirá según la predicción.

### Paquetes que priorizan el equilibrio entre eficiencia de costes y tasa de rendimiento

DSP Para algunos objetivos de optimización, predice el rendimiento de cada subasta y ajusta los precios de oferta automáticamente, sin superar nunca los de una ubicación [!UICONTROL Max Bid]. Algunos ejemplos de objetivos de optimización aplicables son [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click], etc.

#### Lógica de ritmo {#pacing-logic-balanced}

* DSP Si el gasto está al ritmo, entonces el gasto se vuelve más sensible a los precios, por lo que la oferta de cantidades más bajas canjea la tasa de ganancia con el plan de ritmo.

* Si también se equilibra una métrica de rendimiento (todos los objetivos excepto [!UICONTROL Lowest CPM]), el KPI previsto se mezcla con la cantidad que se ofrece. Por lo tanto, puede pujar más alto en las subastas que, según las predicciones, tendrán un mejor rendimiento en función del coste por subasta.

* DSP Si el gasto está por detrás del ritmo, entonces el gasto se vuelve menos sensible a los precios y ofrece cantidades más altas, hasta el punto de que el precio es más elevado. [!UICONTROL Max Bid], para intercambiar la tasa de ganancia con el plan de ritmo.

#### Sombreado de puja/precio de liquidación {#clearing-price-balanced}

DSP Después de ejecutar la lógica de ritmo, ejecuta la oferta propuesta a través de un modelo de predicción de precios de compensación. Si la predicción indica que la oferta se puede reducir con una disminución mínima de la tasa de ganancia, la oferta se reducirá según la predicción.

## Optimización de ubicación

Los filtros de preoferta de colocación son la forma más estricta de garantizar un rendimiento sólido. DSP utiliza filtros de oferta previa de forma estratégica en diferentes tipos de anuncios para lograr objetivos de rendimiento en todas las ubicaciones dentro de cada paquete. Puede utilizar filtros de oferta previa simultáneamente con la optimización de nivel de paquete o de forma independiente.

>[!NOTE]
>
>Los filtros de pujas previas disponibles varían según el tipo de anuncio. Por ejemplo, para una ubicación de visualización estándar, puede filtrar por tasa de pulsaciones y visibilidad, pero no por tasa de finalización.

Consulte [Filtros previos a la oferta de nivel de ubicación y cómo utilizarlos](optimization-pre-bid-filters.md) para determinar qué filtro de oferta previa puede ayudarle a lograr sus KPI.

>[!MORELIKETHIS]
>
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Filtros previos a la oferta de nivel de ubicación y cómo utilizarlos](optimization-pre-bid-filters.md)
>* [Solución de problemas de rendimiento](/help/dsp/optimization/troubleshooting-performance.md)
