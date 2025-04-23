---
title: Administrar Las Vistas De Datos De Campaign
description: Descubra cómo puede personalizar las vistas de datos para campañas, paquetes, ubicaciones y anuncios.
feature: DSP Campaign Data Views
exl-id: a22da10b-104d-4860-a23f-f2a6e59b637c
source-git-commit: 40cfd72c0f295ab1b6b7743828dded4032d435d4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Administrar Las Vistas De Datos De Campaign

Puede personalizar los datos que aparecen en las vistas de administración de campañas ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] y [!UICONTROL Ads]).

## Administrar visualizaciones de datos {#data-visualizations-manage}

Puede cambiar las métricas y el modo de gráfico para todas las visualizaciones de datos entre campañas o para una sola campaña. Los cambios en una sola campaña se aplican a todas las visualizaciones de datos de la campaña, incluidas las vistas [!UICONTROL Packages], [!UICONTROL Placements] y [!UICONTROL Ads].

### Cambio de las métricas de una visualización de datos

1. En la parte superior derecha de la visualización de datos, haga clic en ![Configuración](/help/dsp/assets/settings-chart.png).

1. Seleccione las métricas.

   No puede seleccionar la misma métrica dos veces.

1. Haga clic en **[!UICONTROL Apply]**.

### Cambio del modo de visualización para una visualización de datos

* En la parte superior derecha de la visualización de datos, haga clic en el modificador [!UICONTROL Overlay] (![Modificador de superposición](/help/dsp/assets/overlay.png)) para cambiar entre el modo de superposición (todos los gráficos superpuestos juntos) y el modo de gráfico de enrejado (tres gráficos independientes).

## Administrar tablas de datos {#data-tables-manage}

En todas las vistas de administración de campañas ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] y [!UICONTROL Ads]), puede personalizar los datos que aparecen en la tabla de datos.

### Administrar vistas de columna {#column-views-manage}

Cada nivel de administración de campañas ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] y [!UICONTROL Ads]) incluye vistas [!UICONTROL Pacing] y [!UICONTROL Performance] integradas que incluyen métricas relevantes para esa entidad. De manera predeterminada, se muestra la vista [!UICONTROL Pacing] para que pueda identificar las campañas con bajo rendimiento y los componentes de campaña de un vistazo. Si lo desea, puede crear y editar conjuntos de columnas personalizados.

![selector de vista de columna](/help/dsp/assets/column-view-selector.png)

DSP guarda la vista más reciente como vista predeterminada para que, cada vez que vuelva a la página, siempre vea las métricas que le interesen.

#### Cambio de la vista de columna {#column-view-change}

* En el selector de vista, haga clic en ![flecha abajo](/help/dsp/assets/chevron-down.png) y, a continuación, haga clic en el nombre de la vista de columna que desee.

#### Crear una vista de columna personalizada {#column-view-create}

1. En el selector de vista, haga clic en ![flecha abajo](/help/dsp/assets/chevron-down.png) y, a continuación, haga clic en **[!UICONTROL Create View]**.

1. Especifique las métricas que desea incluir en la vista:

   1. En la lista de métricas disponibles, active la casilla de verificación situada junto a cada métrica que desee incluir.

      Todas las métricas son alfabéticas por categoría: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (métricas estándar que DSP rastrea), [!UICONTROL Viewability] y [!UICONTROL Conversions]. Las métricas anexadas con &quot;([!UICONTROL Lifetime])&quot; devuelven valores desde el inicio de la campaña, independientemente del intervalo de fechas seleccionado en la página.

   1. Edite el orden de las columnas, según sea necesario, haciendo clic en los nombres de las columnas en el panel derecho y arrastrándolas a las posiciones requeridas.

   Algunas columnas tienen posiciones fijas y no se pueden mover ni quitar.

1. Aplique o guarde la configuración:

   * Para aplicar la configuración temporalmente sin guardarla en la vista, haga clic en **[!UICONTROL Apply].**

   * Para guardar la configuración en una nueva vista de columna personalizada, haga clic en **[!UICONTROL Save As]**. En la ventana [!UICONTROL Save View], escriba el nombre de la nueva vista y haga clic en **[!UICONTROL Save]**.

#### Editar una vista de columna {#column-view-edit}

>[!NOTE]
>
>No puede guardar los cambios en una vista de columna estándar (predefinida), pero puede aplicarlos temporalmente o guardarlos en una nueva vista personalizada.

1. En el selector de vista, haga clic en ![flecha abajo](/help/dsp/assets/chevron-down.png) y, a continuación, haga clic en el nombre de la vista de columna existente.

1. En el selector de vista, haga clic en ![flecha abajo](/help/dsp/assets/chevron-down.png) y, a continuación, haga clic en **[!UICONTROL Edit View]**.

1. Edite las métricas que desea incluir en la vista:

   1. En la lista de métricas disponibles, active la casilla de verificación situada junto a cada métrica que desee incluir y desactive la casilla de verificación situada junto a cada métrica que desee excluir.

      Todas las métricas son alfabéticas por categoría: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (métricas estándar que DSP rastrea), [!UICONTROL Viewability] y [!UICONTROL Conversions]. Las métricas anexadas con &quot;([!UICONTROL Lifetime])&quot; devuelven valores desde el inicio de la campaña, independientemente del intervalo de fechas seleccionado en la página.

   1. Edite el orden de las columnas, según sea necesario, haciendo clic en los nombres de las columnas en el panel derecho y arrastrándolas a las posiciones requeridas.

   Algunas columnas tienen posiciones fijas y no se pueden mover ni quitar.

1. Aplique o guarde la configuración:

   * (Solo vistas personalizadas) Para guardar la configuración, haga clic en **[!UICONTROL Save]**.

   * Para aplicar la configuración temporalmente sin guardarla en la vista, haga clic en **[!UICONTROL Apply].**

   * Para guardar la configuración en una nueva vista de columna personalizada, haga clic en **[!UICONTROL Save As]**. En la ventana [!UICONTROL Save View], escriba el nombre de la nueva vista y haga clic en **[!UICONTROL Save]**.

### Filtrado de datos de Campaign {#filter-data-tables}

Los filtros cambian los datos que se muestran en la pestaña actual. Los filtros disponibles varían según el tipo de entidad, pero pueden incluir el nombre de la entidad, el estado y columnas de propiedad adicionales.

1. En la barra de herramientas principal, haga clic en ![Botón Filtro](/help/dsp/assets/filter.png).
1. Para cada filtro que desee aplicar, haga clic en el nombre del filtro en la columna izquierda y, a continuación, especifique los valores del filtro.
1. Haga clic en **[!UICONTROL Apply]**.

#### Filtros disponibles

Los siguientes filtros están disponibles para las vistas [!UICONTROL Campaigns], [!UICONTROL Packages] y [!UICONTROL Placements]:

* [!UICONTROL Campaigns] filtros de vista:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] filtros de vista:
   * [!UICONTROL Custom flights] (existan o no)
   * [!UICONTROL Custom goal] (si corresponde)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] filtros de vista:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (si corresponde)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than] o [!UICONTROL equal to] un valor especificado)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] o [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] filtros de vista:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### Cambio del intervalo de fechas

Cambie el intervalo de fechas utilizado en todas las vistas estándar y personalizadas mediante el selector de intervalo de fechas situado encima de cualquier tabla de datos.

![Selector de intervalo de fecha](/help/dsp/assets/date-range-selector.png "Selector de intervalo de fecha")

* Para un rango preestablecido: seleccione en la lista de incrementos de tiempo comunes. El valor predeterminado es [!UICONTROL Last 30 days]*.

* Para un rango específico, realice una de las acciones siguientes:

   * Haga clic en ![Calendario](/help/dsp/assets/calendar.png "Calendario") y, a continuación, haga clic en la fecha de inicio y en la fecha de finalización dentro del calendario.

   * Haga clic dentro del intervalo de fechas y, a continuación, escriba una fecha de inicio y una fecha de finalización o selecciónelas en el calendario.

     Puede introducir valores numéricos (de D-M-AA a DD-MM-AAAA) o nombres de mes o abreviaturas (como Ene o Enero).

### Ordenar una columna de datos

Puede ordenar cualquier columna de datos en orden ascendente (A a Z o 1 a 10) o descendente (Z a A o 10 a 1).

* Haga clic en el encabezado de la columna para cambiar entre orden ascendente y descendente.


### Especificar el número de filas de datos

En la parte inferior derecha de cualquier página, junto a **[!UICONTROL Items per page]** , seleccione *[!UICONTROL 25]*, *[!UICONTROL 50]* o *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Tipos de informes de rendimiento en las vistas de administración de campañas](campaign-reports-about.md)
>* [Ver los sitios, anuncios y detalles de frecuencia de una ubicación](placement-details-view.md)
>* [Ver el informe de previsión de ubicación](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Ver los informes de diagnóstico de ubicación](placement-diagnostics.md)
>* [Exportar datos de una vista de administración de Campaign](campaign-export-data.md)
>* [Vídeo: estructura de cuenta de DSP e interfaz de usuario](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
