---
title: (Nueva IU) Ver Ver detalles de rendimiento del portafolio
description: Obtenga información sobre cómo ver los detalles de rendimiento del portafolio, incluidas las métricas reales y predichas a nivel de portafolio y para cada campaña asignada.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
source-git-commit: fee9c6e4649c348cad7561f81a9d45d92eb672ec
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# (Nueva IU) Ver detalles de rendimiento del portafolio

*característica de Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

La vista de detalles del portafolio incluye la siguiente información sobre un portafolio:

* Los valores reales y predichos de hasta tres métricas de rendimiento. Los informes incluyen los valores de métricas totales del portafolio y el desglose de métricas por fecha.<!-- Not for active portfolios only?  -->

* Datos de precisión del modelo para portafolios activos, que muestran cuánto se desviaron los modelos de las predicciones. El informe muestra la precisión de coste total diaria o móvil en siete días, la precisión de clics y la precisión de valor objetivo.

  Puede ver los datos por fecha de clic (la predeterminada) o por fecha de transacción.   También puede ver los datos como un gráfico de tendencias (predeterminado) o como una tabla.

* El gasto objetivo frente al gasto real de las carteras activas. Opcionalmente, también puede incluir los presupuestos de campaña totales para el portafolio.

* La precisión de las predicciones de costo, clic o [valor objetivo](/help/search-social-commerce/glossary.md#o-p) para portafolios activos por red de anuncios.<!-- Verify -->

* La configuración del portafolio.

  Si lo desea, puede abrir la configuración del portafolio para editarla.

## Abrir los detalles de rendimiento de un portafolio

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Haga clic en el nombre del portafolio.

1. (Opcional) En el menú **[!UICONTROL Granularity]**, cambie la granularidad de los datos entre *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly].*

1. (Opcional) Para cambiar el intervalo de fechas de los detalles del portafolio, haga clic en el intervalo de fechas en la esquina superior derecha, especifique el intervalo de fechas y, a continuación, haga clic en **[!UICONTROL Apply]**.

## Personalizar la ficha [!UICONTROL Portfolio Overview]

* (Opcional) Para personalizar los informes de [!UICONTROL Portfolio Performance], siga uno de estos procedimientos:

   * Para cambiar las métricas de rendimiento utilizadas tanto para las métricas totales como para las métricas detalladas, haga clic en **[!UICONTROL Metrics]** y seleccione hasta tres métricas.

     Las métricas predeterminadas son *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* y *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * Para ver las métricas detalladas:

      * Mueva el modificador junto a **[!UICONTROL Display predictions]** para mostrar u ocultar los valores de métrica predichos.

      * Cambiar entre la vista de gráfico (![Vista de gráfico](/help/search-social-commerce/assets/chart-view.png "Vista de gráfico")) y la vista de tabla (![Visualización en tabla](/help/search-social-commerce/assets/table-view.png "Visualización en tabla")).

      * (En la vista de gráfico) Para ver los datos de cualquier punto del gráfico, mantenga el cursor sobre ese punto.

* (Opcional) Para personalizar el gráfico de tendencias [!UICONTROL Model accuracy], realice una de las acciones siguientes:

   * Cambiar entre la vista de gráfico (![Vista de gráfico](/help/search-social-commerce/assets/chart-view.png "Vista de gráfico")) y la vista de tabla (![Visualización en tabla](/help/search-social-commerce/assets/table-view.png "Visualización en tabla")).

   * Cambiar entre ver datos de *[!UICONTROL Click Date]* y *[!UICONTROL Transaction Date]*.

   * Cambiar entre ver datos sobre *[!UICONTROL Daily Accuracy]* y *[!UICONTROL 7 Day Rolling Accuracy]*.

     [!UICONTROL 7 Day Rolling Accuracy] es la precisión promedio de la previsión para los siete días anteriores, expresada como porcentaje. Por ejemplo, el valor para el 8 de mayo de 2025 es la precisión promedio para el período del 1 al 7 de mayo de 2025.

   * (En la vista de gráfico) Para ver los datos de cualquier punto del gráfico, mantenga el cursor sobre ese punto.

* (Opcional) Para personalizar el gráfico de tendencias [!UICONTROL Target vs actual spend], realice una de las acciones siguientes:

   * Mueva el conmutador junto a **[!UICONTROL Display budget]** para mostrar u ocultar el presupuesto total de campaña para cada fecha.

   * Para ver los datos de cualquier punto del gráfico, mantenga el cursor sobre ese punto.

* (Opcional) Para personalizar el gráfico de tendencias [!UICONTROL Network Accuracy], realice una de las acciones siguientes:

   * Cambie la métrica de la que se ha informado a *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* o *[!UICONTROL Objective Value]*.

   * Para ver los datos de cualquier punto del gráfico, mantenga el cursor sobre ese punto.

1. Haga clic en **[!UICONTROL Download report]**.

## Enumeración de las campañas del portafolio

* Haga clic en la ficha **[!UICONTROL Campaigns]**.

## Enumeración de los grupos de anuncios del portafolios

* Para ver todos los grupos de anuncios de una campaña dentro del portafolio, haga clic en la pestaña **[!UICONTROL Campaigns]** y luego haga clic en el nombre de la campaña.

## Enumerar las palabras clave del portafolio

* Para ver todas las palabras clave del portafolio, haga clic en la ficha **[!UICONTROL Keywords]**.

* Para ver todas las palabras clave de un grupo de anuncios dentro del portafolios, haga clic en la ficha **[!UICONTROL Ad Groups]** y, a continuación, haga clic en el nombre del grupo de anuncios.

## Ver y editar la configuración del portafolio

* Para ver u ocultar la configuración del portafolio, haga clic en **[!UICONTROL Portfolio Settings]**.

   * Para editar la configuración visible del portafolio, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar") junto a la sección de configuración y [editar la configuración del portafolio](portfolio-edit.md).

Para obtener más información sobre la configuración del portafolio, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.

## Descargar informes de rendimiento de la cartera y listas de los componentes de la cartera

1. En la barra de herramientas, haga clic en **[!UICONTROL Download report]**.

1. Seleccione la casilla de verificación situada junto a cada tipo de componente de portafolio e informe de rendimiento que desee incluir.

   Para algunos informes de rendimiento, puede elegir si desea descargar los datos como un carro de compras o como una tabla.

>[!MORELIKETHIS]
>
>* [(Nueva interfaz de usuario) Acerca de los portafolios](portfolio-about.md)
>* [(nueva interfaz de usuario) Editar un portafolio](portfolio-edit.md)
>* [(nueva interfaz de usuario) Descargar datos en la vista [!UICONTROL Portfolios]](portfolio-view-report.md)
