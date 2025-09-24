---
title: Usando [!UICONTROL Spend Planner]
description: Aprenda a utilizar [!UICONTROL Spend Planner] para identificar la distribución óptima del gasto en todos los portafolios.
feature: Search Optimization, Search Portfolios, Search Simulations
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
source-git-commit: ff4deeb1cfbcd863e5b0ef2ac9b2f7124906c3dd
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Usando [!UICONTROL Spend Planner]

<!-- When this becomes a menu item, move file and TOC entry accordingly -->

[!UICONTROL Spend Planner] (denominada &quot;Herramienta de recomendación de gastos&quot; en la interfaz de usuario heredada) identifica la distribución óptima del gasto en portafolios optimizados y activos con el mismo objetivo y moneda para que pueda obtener el máximo de ingresos o establecer como objetivo los objetivos del conjunto de portafolios.

Al consultar un informe de recomendación de gasto para portafolios con presupuestos diarios, puede cambiar los presupuestos de cualquiera de los portafolios por los presupuestos recomendados.

## Datos en el informe [!UICONTROL Spend Planner]

Para portafolios con el objetivo [!UICONTROL Maximize Clicks], el informe incluye recomendaciones de gasto y proyecciones de clics. Para todos los demás objetivos, el informe incluye recomendaciones de gasto y proyecciones de ingresos.

Los informes de recomendación de gasto incluyen los siguientes datos:

* Un gráfico de líneas de dispersión muestra los ingresos o clics máximos predichos que se pueden lograr con un coste total determinado para el conjunto de portafolios cuando los objetivos de gasto individuales se establecen de forma óptima. Se incluye el coste previsto para cada punto de ingresos o de clic.

* Dos gráficos circulares que muestran el gasto y los ingresos esperados o la distribución de clics por portafolio para 1\) los objetivos de gasto actuales y 2\) los objetivos de gasto propuestos.

* Un gráfico de barras para cada uno de los portafolios, que muestra el gasto diario recomendado (coste) y la distribución de ingresos prevista o la distribución de clics cuando se mantiene el objetivo de gasto diario total actual en todos los portafolios seleccionados, o para un objetivo de gasto total propuesto. Si lo desea, puede aplicar los objetivos de gasto recomendados a los portafolios seleccionados, lo que afecta a las ofertas en el siguiente ciclo de ejecución de ofertas.

## (Nueva IU) Generar un informe [!UICONTROL Spend Planner]

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

1. (Opcional) Para ver el gasto diario recomendado y los ingresos previstos para cada uno de los portafolios mediante un nuevo objetivo de gasto total, introduzca un objetivo de gasto diario total propuesto en todos los portafolios en el campo [!UICONTROL Total Spend Target]. Luego presione la tecla **Enter**.

   La herramienta de recomendación de gasto utiliza datos de simulaciones semanales, por lo que el gasto total recomendado es el que más se ajusta al objetivo de gasto propuesto con la combinación de gasto ideal.

## (IU heredada) Generar un informe [!UICONTROL Spend Recommendation] desde la vista [!UICONTROL Optimization] > [!UICONTROL Spend Recommendation]

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

## Aplicar recomendaciones de gasto

*Portafolios con presupuestos diarios solamente*

>[!NOTE]
>
>* Si los cambios aplicados aumentan o disminuyen el objetivo de gasto de cualquier portafolio en más del 20 %, recibirá una notificación y deberá aprobar el cambio.
>* Cuando el objetivo de gasto de un portafolio cambia en más del 20 %, Search, Social y Commerce tardan entre 3 y 4 días en ajustar sus modelos y lograr el nuevo objetivo.

1. Ver el informe de recomendación de gasto de uno o más portafolios con presupuestos diarios.

1. Seleccione la casilla de verificación situada junto a cada portafolio para el que desee aplicar el objetivo de gasto recomendado. Para seleccionar todos los portafolios, active la casilla de verificación situada junto a [!UICONTROL Select All Recommendations].

1. Haga clic en **[!UICONTROL Apply Selected Recommendations]**.

1. (Si alguno de los presupuestos cambiará en más del 20%) En el mensaje de confirmación, haga clic en **[!UICONTROL Yes]** para aprobar los cambios.

## Abrir o guardar datos en un archivo

Puede exportar los datos del informe desde cualquier sección del informe [!UICONTROL Spend Recommendation]. Puede abrir o guardar los datos como un archivo de libro de [!DNL Microsoft Excel].

1. Generar un informe de recomendación de gastos para los portafolios seleccionados.

1. Encima del informe, haz clic en ![Descargar](/help/search-social-commerce/assets/download-spend-recommendation.png "Descargar").

   Abra o guarde el archivo según el procedimiento normal del explorador.  Para obtener más información, consulte la ayuda en línea del explorador.
