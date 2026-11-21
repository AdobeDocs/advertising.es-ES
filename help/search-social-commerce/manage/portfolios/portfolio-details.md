---
title: (Nueva IU) Ver detalles de rendimiento del portafolio
description: Obtenga información sobre cómo ver el rendimiento del portafolio, los detalles de la unidad de oferta de palabras clave, las previsiones y el historial de ofertas, y exportar el historial de unidades de ofertas en Adobe Advertising Search, Social y Commerce.
feature: Search Portfolios, Search Optimization
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
TQID: 'https://experienceleague.adobe.com/5hNxKu6YjJTWI4KGEc6aaYnpgXK6k3OsN0-YfetzENw'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 157c45d4939eff028543a0181397a59e6346309e
workflow-type: tm+mt
source-wordcount: '1555'
ht-degree: 0%
---
# (Nueva IU) Ver detalles de rendimiento del portafolio

*característica de Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

La vista de detalles del portafolio incluye la siguiente información sobre un portafolio:

* Los valores reales y predichos de hasta tres métricas de rendimiento. Los informes incluyen los valores de métricas totales del portafolio y el desglose de métricas por fecha.<!-- Not for active portfolios only?  -->

* Datos de precisión del modelo para portafolios activos, que muestran cuánto se desviaron los modelos de las predicciones. El informe muestra la precisión de coste total diaria o móvil en siete días, la precisión de clics y la precisión de valor objetivo.

  Puede ver los datos como un gráfico de tendencias (predeterminado) o como una tabla.

* El gasto objetivo frente al gasto real de las carteras activas. Opcionalmente, también puede incluir los presupuestos de campaña totales para el portafolio.

* La precisión de las predicciones de costo, clic o [valor objetivo](/help/search-social-commerce/glossary.md#o-p) para portafolios activos por red de anuncios.<!-- Verify -->

* La configuración del portafolio.

  Si lo desea, puede abrir la configuración del portafolio para editarla.

* Listas de las redes de anuncios, cuentas, campañas, grupos de anuncios y palabras clave del portafolio, con datos de rendimiento.

  Para palabras clave individuales, puede ver los detalles de la unidad de oferta, incluidas las previsiones, la información histórica y la información jerárquica. La vista [!UICONTROL Bid Unit Details] incluye las siguientes previsiones, información histórica e información jerárquica para la unidad de oferta seleccionada:

  * Pestaña [!UICONTROL Forecast]: los clics, el coste, el coste por clic, la posición y los ingresos proyectados actualmente para la unidad de oferta a precios de oferta diferentes. Se muestran los datos de todos los dispositivos y de cada tipo de dispositivo ([!UICONTROL Mobile], [!UICONTROL Computer] y [!UICONTROL Tablet]).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. -->

    **Nota:** No hay datos de previsión disponibles para un tipo de dispositivo cuando no hay suficientes datos específicos del dispositivo disponibles para generar modelos y establecer ajustes para ese tipo de dispositivo. **Nota:** Para ver la precisión de costos o de ingresos de cada unidad de oferta dentro de un portafolio que recibió un clic durante un intervalo de fechas específico, vea la vista de los detalles de precisión de costos o de ingresos del portafolio, respectivamente.

  * Pestaña [!UICONTROL History]: todas las ofertas de los últimos 36 días, incluidos los datos siguientes de cada una de las ofertas: fecha y hora, impresiones, clics, coste total, CPC promedio, posición promedio e ingresos ponderados mostrados por fecha de clic. Se muestran los datos de todos los dispositivos y de cada tipo de dispositivo (móvil, equipo y tableta).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. **Note:** Whenever the optimization method changes from v6 to v7 and vice-versa, the history data is reset the same day. -->

  * Pestaña [!UICONTROL Details]: la palabra clave, el tipo de coincidencia (cuando corresponda) y el grupo de anuncios principal, la campaña, la cuenta de red de anuncios y el portafolios al que pertenece la unidad de oferta.

## Abrir los detalles de rendimiento de un portafolio

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Mantenga el cursor sobre el nombre del portafolio y haga clic en ![Información general de Portfolio](/help/search-social-commerce/assets/portfolio-overview.png "Información general de Portfolio").

1. (Opcional) Para cambiar el intervalo de fechas de los detalles del portafolio, haga clic en el intervalo de fechas en la esquina superior derecha, especifique el intervalo de fechas y, a continuación, haga clic en **[!UICONTROL Apply]**.

1. (Opcional) En el menú **[!UICONTROL Data Aggregation]**, cambie la unidad de tiempo de los datos incluidos en cada fila: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly].*

   Las opciones disponibles dependen del intervalo de fechas seleccionado. Si la agregación actual no está disponible para un nuevo intervalo de fechas, se selecciona automáticamente otra agregación disponible.

1. (Opcional) En el menú **[!UICONTROL Conversion Based On]** del encabezado de la página, seleccione **[!UICONTROL Click Date]** o **[!UICONTROL Transaction Date]**.

   Esta configuración se aplica a los datos de conversión de los informes de portafolio y las listas de componentes.

Para ver los detalles de otro portafolio, utilice el selector de portafolios situado junto al nombre del portafolio.

## Personalizar la ficha [!UICONTROL Portfolio Overview]

* (Opcional) Para personalizar los informes de [!UICONTROL Portfolio Performance], siga uno de estos procedimientos:

  * Para cambiar las métricas de rendimiento utilizadas tanto para las métricas totales como para las métricas detalladas, haga clic en **[!UICONTROL Metrics]** y seleccione hasta tres métricas.

    Las métricas predeterminadas son *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* y *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

  * Para ver las métricas detalladas:

    * Mueva el modificador junto a **[!UICONTROL Display predictions]** para mostrar u ocultar los valores de métrica predichos.

    * Cambiar entre la vista de gráfico (![Vista de gráfico](/help/search-social-commerce/assets/chart-view.png "Vista de gráfico")) y la vista de tabla (![Visualización en tabla](/help/search-social-commerce/assets/table-view.png "Visualización en tabla")).

    * (En la vista de gráfico) Para ver los datos de cualquier punto del gráfico, mantenga el cursor sobre ese punto.

    * (En la vista de gráfico) Para hacer zoom, seleccione un área del gráfico.

    * (Cuando se muestran los marcadores de cambio de configuración del portafolio) Para ver el historial de cambios del portafolio para una fecha marcada, haga clic en el marcador del gráfico. Para obtener más información acerca del historial, consulte &quot;[Ver el historial de cambios de un portafolio](portfolio-view-change-history.md#portfolio-change-history)&quot;.

* (Opcional) Para personalizar el gráfico de tendencias [!UICONTROL Model accuracy], realice una de las acciones siguientes:

  * Cambiar entre la vista de gráfico (![Vista de gráfico](/help/search-social-commerce/assets/chart-view.png "Vista de gráfico")) y la vista de tabla (![Visualización en tabla](/help/search-social-commerce/assets/table-view.png "Visualización en tabla")).

  * Cambiar entre ver datos sobre *[!UICONTROL Daily Accuracy]* y *[!UICONTROL 7 Day Rolling Accuracy]*.

    [!UICONTROL 7 Day Rolling Accuracy] es la precisión promedio de la previsión para los siete días anteriores, expresada como porcentaje. Por ejemplo, el valor para el 8 de mayo de 2025 es la precisión promedio para el período del 1 al 7 de mayo de 2025.

    [!UICONTROL 7 Day Rolling Accuracy] solo está disponible cuando [!UICONTROL Data Aggregation] está establecido en [!UICONTROL Daily].

  * (En la vista de gráfico) Para ver los datos de cualquier punto del gráfico, mantenga el cursor sobre ese punto.

* (Opcional) Para personalizar el gráfico de tendencias [!UICONTROL Target vs actual spend], realice una de las acciones siguientes:

  * Mueva el conmutador junto a **[!UICONTROL Display budget]** para mostrar u ocultar el presupuesto total de campaña para cada fecha.

  * Para ver los datos de cualquier punto del gráfico, mantenga el cursor sobre ese punto.

* (Opcional) Para personalizar el gráfico de tendencias [!UICONTROL Network Accuracy], realice una de las acciones siguientes:

  * Cambie la métrica de la que se ha informado a *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* o *[!UICONTROL Objective Value]*.

  * Cuando los datos estén disponibles para más de una red, seleccione la red en el menú situado junto al menú de métrica.

  * Para ver los datos de cualquier punto del gráfico, mantenga el cursor sobre ese punto.

  * Para hacer zoom, seleccione un área en el gráfico.

## Personalizar las listas de componentes del portafolio

Las fichas [!UICONTROL Networks], [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] y [!UICONTROL Keywords] incluyen los siguientes controles:

* Para buscar por nombre, escriba texto en el campo de búsqueda situado encima de la tabla y envíe la búsqueda.

* Para [filtrar los datos](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md), haga clic en ![Filtro](/help/search-social-commerce/assets/filter-new.png "Filtro"). Puede editar o eliminar los filtros aplicados utilizando los controles de filtro encima de la tabla.

* Para ver los componentes de una red, cuenta, campaña o grupo de publicidad en la siguiente pestaña, haga clic en su nombre. El elemento principal seleccionado se muestra en la ruta de exploración encima de la tabla y los filtros aplicables se arrastran a medida que aumenta el detalle. Las selecciones principales pueden seguir restringiendo la lista al cambiar de pestaña.

  Para quitar una selección detallada (como un nombre de cuenta o de red), haga clic en **[!UICONTROL X]** junto al nombre del componente en la ruta de exploración que se encuentra sobre la tabla. Las selecciones principales de nivel superior pueden permanecer activas. Para volver a todos los componentes del portafolio, elimine las selecciones principales restantes y cualquier otro filtro.

* Para actualizar los datos, haga clic en ![Actualizar](/help/search-social-commerce/assets/refresh-new.png "Actualizar").

* ([!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] y [!UICONTROL Keywords] solamente) Para cambiar las columnas mostradas o el orden, haga clic en ![Columnas personalizadas](/help/search-social-commerce/assets/custom-columns-new.png "Columnas personalizadas") y [edite el conjunto de columnas y las opciones de ordenación](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md).


## Enumeración de las redes de anuncios del portafolio

* Haga clic en la ficha **[!UICONTROL Networks]**.

## Enumerar las cuentas del portafolio

* Para ver todas las cuentas del portafolio, haga clic en la ficha **[!UICONTROL Accounts]**.

* Para ver las cuentas de una red específica del portafolio, haga clic en la ficha **[!UICONTROL Networks]** y, a continuación, haga clic en el nombre de la red.

## Enumeración de las campañas del portafolio

Los detalles de cada campaña incluyen la estrategia de oferta; el coste real y predicho, los clics y el valor objetivo; y el coste, los clics y la precisión del valor objetivo.

* Para ver todas las campañas del portafolio, haga clic en la ficha **[!UICONTROL Campaigns]**.

* Para ver las campañas de una cuenta específica del portafolio, haga clic en la ficha **[!UICONTROL Accounts]** y, a continuación, haga clic en el nombre de la cuenta.

## Enumeración de los grupos de anuncios del portafolios

Los detalles de cada grupo de anuncios incluyen la red, la oferta predeterminada, el coste, los clics, el CPC, las impresiones, el valor objetivo y las métricas de conversión utilizadas en el objetivo del portafolio.

* Para ver todos los grupos de anuncios del portafolios, haga clic en la ficha **[!UICONTROL Ad Groups]**.

* Para ver todos los grupos de anuncios de una campaña dentro del portafolio, haga clic en la pestaña **[!UICONTROL Campaigns]** y luego haga clic en el nombre de la campaña.

## Mostrar y ver detalles sobre palabras clave en el portafolio {#bid-unit-details}

Los detalles de cada palabra clave incluyen el ID de unidad de oferta; el tipo de coincidencia; el coste real y predicho, los clics y el valor objetivo; y la diferencia de coste, clics y valor objetivo. Puede ver los detalles de la unidad de oferta acerca de una palabra clave individual.

1. Enumerar las palabras clave:

   * Para ver todas las palabras clave del portafolio, haga clic en la ficha **[!UICONTROL Keywords]**.

   * Para ver todas las palabras clave de un grupo de anuncios dentro del portafolios, haga clic en la ficha **[!UICONTROL Ad Groups]** y, a continuación, haga clic en el nombre del grupo de anuncios.

1. (Opcional) Para ver los detalles de una unidad de oferta específica, haga clic en el valor de la columna **[!UICONTROL Bid Unit ID]**. Haga clic en cualquier ficha de [!UICONTROL Bid Unit Details] para obtener más información.

### Ver y descargar el historial de una unidad de oferta individual {#bid-unit-history}

1. [Abrir los detalles de la unidad de oferta](#bid-unit-details).

1. Haga clic en la ficha **[!UICONTROL History]**.

1. (Opcional) En el menú de dispositivos situado encima de la tabla, seleccione un tipo de dispositivo para el que ver el historial. De forma predeterminada, se muestran los datos de todos los dispositivos.

1. (Opcional) Cuando haya datos de historial disponibles, haga clic en **[!UICONTROL Export as csv]** para descargar el historial mostrado.

El archivo se descarga según el procedimiento normal del explorador.

Para ver el historial de ofertas de todo el portafolio y cambiar su intervalo de fechas, consulte &quot;[Ver el historial de cambios de ofertas de un portafolio](portfolio-view-change-history.md#portfolio-bid-change-history)&quot;.

## Ver y editar la configuración del portafolio

* Para ver u ocultar la configuración del portafolio, haga clic en **[!UICONTROL Portfolio Settings]**.

  * Para editar la configuración visible del portafolio, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar") junto a la sección de configuración y [editar la configuración del portafolio](portfolio-edit.md).

Para obtener más información sobre la configuración del portafolio, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.

## Descargar informes y listas de rendimiento de portafolios de los componentes del portafolio

* Para descargar informes de rendimiento y listas de componentes:

  1. En la barra de herramientas, haga clic en **[!UICONTROL Download report]**.

  1. Seleccione la casilla de verificación situada junto a cada tipo de componente de portafolio e informe de rendimiento que desee incluir.

     Los componentes de portafolio disponibles son *[!UICONTROL Campaigns table]*, *[!UICONTROL Ad groups table]* y *[!UICONTROL Keywords table]*. Las tablas [!UICONTROL Networks] y [!UICONTROL Accounts] no se incluyen en esta descarga.

     Para los informes de rendimiento con ambas opciones, seleccione **[!UICONTROL As chart]**, **[!UICONTROL As table]** o ambos. El informe [!UICONTROL Network accuracy chart] solo está disponible como gráfico.

  1. Haga clic en **[!UICONTROL Download report]**.

* Para descargar un informe [!UICONTROL Model accuracy] con tipos de datos específicos:

  1. En la barra de herramientas de [!UICONTROL Model accuracy], haga clic en **[!UICONTROL Download report]**.

  1. Seleccione **[!UICONTROL Cost Accuracy]**, **[!UICONTROL Objective Value Accuracy]** o ambos.

  1. Para cada tipo de datos seleccionado, seleccione **[!UICONTROL By Bid Unit]**, **[!UICONTROL By Click Volume]** o ambos.

  1. Haga clic en **[!UICONTROL Download report]**.

>[!MORELIKETHIS]
>
>* [(Nueva interfaz de usuario) Acerca de los portafolios](portfolio-about.md)
>* [(nueva interfaz de usuario) Editar un portafolio](portfolio-edit.md)
>* [(nueva interfaz de usuario) Descargar datos en la vista [!UICONTROL Portfolios]](portfolio-view-report.md)
