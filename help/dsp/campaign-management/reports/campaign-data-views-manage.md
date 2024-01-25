---
title: Administrar las vistas de datos de Campaign
description: Descubra cómo puede personalizar las vistas de datos para campañas, paquetes, ubicaciones y anuncios.
feature: DSP Campaign Data Views
source-git-commit: 14da2c26a6a6c3820f691cd752c22c982278314d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# Administrar las vistas de datos de Campaign

## Administrar visualizaciones de datos

Puede cambiar las métricas y el modo de gráfico para todas las visualizaciones de datos entre campañas o para una sola campaña. Los cambios en una sola campaña se aplican a todas las visualizaciones de datos de la campaña, incluida la [!UICONTROL Packages], [!UICONTROL Placements], y [!UICONTROL Ads] pestañas.

### Cambio de las métricas de una visualización de datos

1. En la parte superior derecha de la visualización de datos, haga clic en ![Configuración](/help/dsp/assets/settings-chart.png).
1. Seleccione las métricas.
No puede seleccionar la misma métrica dos veces.
1. Clic **[!UICONTROL Apply]**.

### Cambio del modo de visualización para una visualización de datos

* En la parte superior derecha de la visualización de datos, haga clic en [!UICONTROL Overlay] interruptor (![Conmutador de superposición](/help/dsp/assets/overlay.png)) para cambiar entre el modo de superposición (todos los gráficos superpuestos juntos) y el modo de gráfico de enrejado (tres gráficos independientes).

## Administrar tablas de datos

En todas las vistas de administración de campañas ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], y [!UICONTROL Ads]), puede personalizar los datos que aparecen en la tabla de datos.

### Cambio de la vista de columna

* En el selector de Vista, haga clic en ![flecha hacia abajo](/help/dsp/assets/chevron-down.png)y, a continuación, haga clic en el nombre de la vista de columna deseada.

### Crear una vista de columna personalizada

1. En el selector de Vista, haga clic en ![flecha hacia abajo](/help/dsp/assets/chevron-down.png)y haga clic en **[!UICONTROL Create View]**.

1. Especifique las métricas que desea incluir en la vista:

   1. En la lista de métricas disponibles, active la casilla de verificación situada junto a cada métrica que desee incluir.

   1. Edite el orden de las columnas, según sea necesario, haciendo clic en los nombres de las columnas en el panel derecho y arrastrándolas a las posiciones requeridas.

   Algunas columnas tienen posiciones fijas y no se pueden mover ni quitar.

1. Aplique o guarde la configuración:

   * Para aplicar la configuración temporalmente sin guardarla en la vista, haga clic en **[!UICONTROL Apply].**

   * Para guardar la configuración en una nueva vista de columna personalizada, haga clic en **[!UICONTROL Save As]**. En el [!UICONTROL Save View] , escriba el nombre de la nueva vista y haga clic en **[!UICONTROL Save]**.

### Editar una vista de columna personalizada

>[!NOTE]
>
>No se puede editar una vista de columna estándar (predefinida).

1. En el selector de Vista, haga clic en ![flecha hacia abajo](/help/dsp/assets/chevron-down.png)y, a continuación, haga clic en el nombre de la vista de columna existente.

1. En el selector de Vista, haga clic en ![flecha hacia abajo](/help/dsp/assets/chevron-down.png)y haga clic en **[!UICONTROL Edit View]**.

1. Edite las métricas que desea incluir en la vista:

   1. En la lista de métricas disponibles, active la casilla de verificación situada junto a cada métrica que desee incluir y desactive la casilla de verificación situada junto a cada métrica que desee excluir.

   1. Edite el orden de las columnas, según sea necesario, haciendo clic en los nombres de las columnas en el panel derecho y arrastrándolas a las posiciones requeridas.

   Algunas columnas tienen posiciones fijas y no se pueden mover ni quitar.

1. Aplique o guarde la configuración:

   * Para aplicar la configuración temporalmente sin guardarla en la vista, haga clic en **[!UICONTROL Apply].**

   * Para guardar la configuración en una nueva vista de columna personalizada, haga clic en **[!UICONTROL Save As]**. En el [!UICONTROL Save View] , escriba el nombre de la nueva vista y haga clic en **[!UICONTROL Save]**.

### Filtrado de datos de Campaign

1. En la barra de herramientas principal, haga clic en ![Botón Filtro](/help/dsp/assets/filter.png).
1. Para cada filtro que desee aplicar, haga clic en el nombre del filtro en la columna izquierda y, a continuación, especifique los valores del filtro.
1. Clic **[!UICONTROL Apply]**.

#### Filtros disponibles

Los siguientes filtros están disponibles para su [!UICONTROL Campaigns], [!UICONTROL Packages], y [!UICONTROL Placements] vistas:

* [!UICONTROL Campaigns] ver filtros:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] ver filtros:
   * [!UICONTROL Custom flights] (existan o no)
   * [!UICONTROL Custom goal] (si procede)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] ver filtros:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (si procede)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than], o [!UICONTROL equal to] un valor especificado)
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
* [!UICONTROL Ads] ver filtros:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### Ordenar una columna de datos

Puede ordenar cualquier columna de datos en orden ascendente (A a Z o 1 a 10) o descendente (Z a A o 10 a 1).

* Haga clic en el encabezado de la columna para cambiar entre orden ascendente y descendente.

<!-- add more links-->

>[!MORELIKETHIS]
>
>* [Acerca de los informes en la plataforma](campaign-reports-about.md)
>* [Administrar visualizaciones de datos](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [Cambio de la vista de columna](column-view-change.md)
>* [Crear una vista de columna personalizada](column-view-create.md)
>* [Editar una vista de columna personalizada](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [Filtrado de datos de Campaign](campaign-data-filter.md)
>* [Ordenar una columna de datos](campaign-data-sort.md)
>* [Ver los sitios, anuncios y detalles de frecuencia de una ubicación](placement-details-view.md)
>* [Ver el informe Previsión de ubicación](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Ver los informes de diagnóstico de ubicación](placement-diagnostics.md)
>* [Exportar datos desde una vista de Campaign Management](campaign-export-data.md)
>* [DSP Vídeo: Estructura de cuenta y interfaz de usuario de](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
