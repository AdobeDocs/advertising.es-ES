---
title: Usando [!UICONTROL Spend Planner]
description: Aprenda a generar, descargar y aplicar recomendaciones de presupuesto de portafolio para ayudarle a lograr la distribución óptima del gasto en sus portafolios.
feature: Search Optimization, Search Portfolios
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
TQID: https://experienceleague.adobe.com/8BAQij06MRhxYoCoFNjhHsgC4o38lQnj9vpmTzYyqGg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4126848d8192a1d4a23406dfeb5b643788670689
workflow-type: tm+mt
source-wordcount: 801
ht-degree: 0%

---

# Usando [!UICONTROL Spend Planner]

[!UICONTROL Spend Planner] (denominado &quot;[!UICONTROL Spend Recommendation Tool]&quot; en la interfaz de usuario heredada) identifica la distribución óptima de gasto en portafolios optimizados y activos con el mismo objetivo y moneda para que pueda maximizar los ingresos o los objetivos objetivo para el conjunto de portafolios.

Al consultar un informe de recomendación de gasto para portafolios con presupuestos diarios, puede cambiar los presupuestos de cualquiera de los portafolios por los presupuestos recomendados.

## Datos en el informe [!UICONTROL Spend Planner]

Para portafolios con el objetivo [!UICONTROL Maximize Clicks], el informe incluye recomendaciones de gasto y proyecciones de clics. Para todos los demás objetivos, el informe incluye recomendaciones de gasto y proyecciones de ingresos.

Los informes de recomendación de gasto incluyen los siguientes datos:

* Un gráfico de líneas de dispersión muestra los ingresos o clics máximos predichos que se pueden lograr con un coste total determinado para el conjunto de portafolios cuando los objetivos de gasto individuales se establecen de forma óptima. Se incluye el coste previsto para cada punto de ingresos o de clic.

* Dos gráficos circulares que muestran el gasto y los ingresos esperados o la distribución de clics por portafolio para 1\) los objetivos de gasto actuales y 2\) los objetivos de gasto propuestos.

* Un gráfico de barras para cada uno de los portafolios, que muestra el gasto diario recomendado (coste) y la distribución de ingresos prevista o la distribución de clics cuando se mantiene el objetivo de gasto diario total actual en todos los portafolios seleccionados, o para un objetivo de gasto total propuesto. Si lo desea, puede aplicar los objetivos de gasto recomendados a los portafolios seleccionados, lo que afecta a las ofertas en el siguiente ciclo de ejecución de ofertas.

## Acciones disponibles

* Generar un informe de [!UICONTROL Spend Planner] desde [la nueva interfaz de usuario](#spend-recommendations-generate) o [la interfaz de usuario heredada](#spend-recommendations-generate-legacy)

* [Aplicar recomendaciones de gasto](#spend-recommendations-apply) a los portafolios correspondientes.

* [Abrir o guardar datos de informes de recomendaciones de gastos en un archivo](#spend-recommendations-download)

## (Nueva IU) Generar un informe [!UICONTROL Spend Planner] {#spend-recommendations-generate}

1. Realice una de las acciones siguientes:

   * En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Spend Planner]**.

   * En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Simulations]**. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Planificador de gastos](/help/search-social-commerce/assets/spend-planner-icon.png "Planificador de gastos").

   La herramienta [!UICONTROL Spend Recommendation] se abre en la interfaz de usuario heredada.

1. Ver datos utilizando los presupuestos actuales combinados para los portafolios seleccionados:

   1. Seleccione el objetivo del portafolio.

   1. Seleccione la moneda.

   1. (Opcional) Seleccione una estrategia de gasto de portafolio para filtrar aún más la lista de portafolios.

   1. Seleccione la casilla de verificación situada junto a cada portafolio que desee incluir. Para seleccionar todos los portafolios, active la casilla de verificación situada junto a [!UICONTROL Portfolios].

      Solo se enumeran los portafolios optimizados y activos con los parámetros seleccionados.

   1. Haga clic en **[!UICONTROL Update]**.

   1. (Opcional) Para ver el coste y los ingresos de cualquier punto del gráfico, mantenga el cursor sobre el punto.

1. (Opcional) Para ver el objetivo de gasto diario recomendado y los ingresos esperados para cada uno de los portafolios utilizando un objetivo de gasto total diferente, introduzca un objetivo de gasto diario total propuesto en todos los portafolios en el campo [!UICONTROL Total Spend Target]. Luego presione la tecla **Enter**.

   La herramienta de recomendación de gasto utiliza datos de simulaciones semanales, por lo que el gasto total recomendado es el que más se ajusta al objetivo de gasto propuesto con la combinación de gasto ideal.

<!--

New UI; validate post-Update steps once I get it to generate a report:

## Generate a spend recommendation report {#spend-recommendations-generate}

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Spend Planner]**.

1. View data using the current, combined budgets for the selected portfolios:

   1. Click **[!UICONTROL Select Objective]**.

   1. Select the portfolio objective.

   1. Select the currency.

   1. (Optional) Select a portfolio spend strategy to further filter the portfolios list.

   1. Select the check box next to each portfolio to include.

      Only optimized and active portfolios with the selected parameters are listed.

   1. Click **[!UICONTROL Update]**.

   1. (Optional) To see the cost and revenue for any point on the chart, hold the cursor over the point.

1. (Optional) To download the proposed allocation and expected revenue per portfolio, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download") next to [!UICONTROL Portfolio Allocation] in the right column.

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

1. (Optional) To view the recommended daily spend and expected revenue for each of the portfolios using a different total spend target, enter a proposed total daily spend target across all portfolios in the [!UICONTROL Total Spend Target] field. Then press the **Enter** key.

   The spend recommendation tool uses data from weekly simulations, so the total recommended spend is the closest match to your proposed spend target with the ideal spend mix.

-->

## (IU heredada) Generar un informe [!UICONTROL Spend Recommendation] desde la vista [!UICONTROL Optimization] > [!UICONTROL Spend Recommendation] {#spend-recommendations-generate-legacy}

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Optimization] >[!UICONTROL Spend Recommendation]**.

1. Ver datos utilizando los presupuestos actuales combinados para los portafolios seleccionados:

   1. Seleccione el objetivo del portafolio.

   1. Seleccione la moneda.

   1. (Opcional) Seleccione una estrategia de gasto de portafolio para filtrar aún más la lista de portafolios.

   1. Seleccione la casilla de verificación situada junto a cada portafolio que desee incluir. Para seleccionar todos los portafolios, active la casilla de verificación situada junto a [!UICONTROL Portfolios].

      Solo se enumeran los portafolios optimizados y activos con los parámetros seleccionados.

   1. Haga clic en **[!UICONTROL Update]**.

   1. (Opcional) Para ver el coste y los ingresos de cualquier punto del gráfico, mantenga el cursor sobre el punto.

1. (Opcional) Para ver el gasto diario recomendado y los ingresos previstos para cada uno de los portafolios mediante un nuevo objetivo de gasto total, introduzca un objetivo de gasto diario total propuesto en todos los portafolios en el campo [!UICONTROL Total Spend Target]. Luego presione la tecla **Enter**.

   La herramienta de recomendación de gasto utiliza datos de simulaciones semanales, por lo que el gasto total recomendado es el que más se ajusta al objetivo de gasto propuesto con la combinación de gasto ideal.

<!--
## (New UI) Apply spend recommendations {#spend-recommendations-apply}

*Portfolios with daily budgets only*

>[!NOTE]
>
>* If the applied changes will increase or decrease the spend target of any portfolio by more than 20%, you must approve the change.
>* When the spend target for a portfolio changes by more than 20%, Search, Social, & Commerce takes up to 3-4 days to adjust its models and achieve the new target.

1. [Generate a spend recommendation report](#spend-recommendations-generate) for one or more portfolios with daily budgets.

1. Select the check box next to each portfolio for which you want to apply the recommended spend target. To select all portfolios, select the check box next to **[!UICONTROL Select All Recommendations]**.

1. Click **[!UICONTROL Apply Selected Recommendations]**.

1. (If any of the budgets will change by more than 20%) In the confirmation message, click **[!UICONTROL Confirm]** to approve the changes.

-->

## &#x200B;<!--(Legacy UI) -->Aplicar recomendaciones de gasto {#spend-recommendations-apply-legacy}

*Portafolios con presupuestos diarios solamente*

>[!NOTE]
>
>* Si los cambios aplicados aumentan o disminuyen el objetivo de gasto de cualquier portafolio en más del 20 %, debe aprobar el cambio.
>* Cuando el objetivo de gasto de un portafolio cambia en más del 20 %, Search, Social y Commerce tardan entre 3 y 4 días en ajustar sus modelos y lograr el nuevo objetivo.

1. [Generar un informe de recomendación de gastos](#spend-recommendations-generate-legacy) para uno o más portafolios con presupuestos diarios.

1. Seleccione la casilla de verificación situada junto a cada portafolio para el que desee aplicar el objetivo de gasto recomendado. Para seleccionar todos los portafolios, active la casilla de verificación situada junto a **[!UICONTROL Select All Recommendations]**.

1. Haga clic en **[!UICONTROL Apply Selected Recommendations]**.

1. (Si alguno de los presupuestos cambiará en más del 20%) En el mensaje de confirmación, haga clic en **[!UICONTROL Yes]** para aprobar los cambios.

<!--

## (New UI) Open or save data as a [!DNL Microsoft Excel] workbook file {#spend-recommendations-download}

You can open or save data from either a) the line chart showing cost points and the expected revenue for each cost and b) the donut charts of the current and proposed media mix. [This seems to be identical to the Portfolio Allocation report -- how should these be different?]

1. [Generate a spend recommendation report](#spend-recommendations-generate) for selected portfolios.

1. Above the report, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download").

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

-->

## &#x200B;<!--(Legacy UI) -->Abrir o guardar datos como un [!DNL Microsoft Excel] archivo de libro {#spend-recommendations-download-legacy}

1. Generar un informe de recomendación de gastos para los portafolios seleccionados.

1. En la parte superior derecha del informe, haga clic en ![Descargar](/help/search-social-commerce/assets/download-spend-recommendation.png "Descargar").

   Abra o guarde el archivo según el procedimiento normal del explorador. Para obtener más información, consulte la ayuda en línea del explorador.
