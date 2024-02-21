---
title: Tipos de informes de rendimiento en las vistas de Campaign Management
description: Obtenga información acerca de los datos de informes incluidos en las vistas de administración de campañas.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: c7860d98edbf44b71d97c3800edf47a409606b74
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Tipos de informes de rendimiento en las vistas de Campaign Management

Las vistas de administración de campañas incluyen datos de informe completos. Los informes disponibles le ayudan a identificar los paquetes y las ubicaciones que tienen un buen rendimiento y aquellos que necesitan su atención. Los botones de acción rápida también le hacen más productivo.

## Vista de todas las campañas

El [!UICONTROL Campaigns] esta vista permite acceder a un conjunto de gráficos de datos de rendimiento y a una lista de todas las campañas de su cuenta.

### Vista de gráfico {#chart-view}

Puede [personalizar gráficos de tendencias de series temporales](campaign-data-views-manage.md#data-visualizations-manage) en todas las campañas con tres métricas. De forma predeterminada, los datos de [!UICONTROL Net Spend], [!UICONTROL Impressions], y [!UICONTROL Net CPM] se incluyen en gráficos separados (gráficos de enrejado). Si lo desea, puede cambiar las métricas. Para habilitar los datos por hora en los gráficos de tendencias de series temporales, cambie la selección de fecha a un solo día ([!UICONTROL Today], [!UICONTROL Yesterday], o un día específico).

![separar gráficos de tendencias para tres métricas](/help/dsp/assets/trend-chart-separate.png)

También puede superponer las tres métricas para facilitar la detección de anomalías y áreas en las que se puede mejorar la escala o el rendimiento.

![gráfico de tendencias con superposición](/help/dsp/assets/trend-chart.png)

### Visualización en tabla

![Lista de campañas](/help/dsp/assets/campaigns-list.png)

De forma predeterminada, cada fila de campaña incluye métricas de ritmo y entrega. Las métricas de ritmo incluyen [!UICONTROL Gross Spend (Lifetime)], que incluye una medición del gasto real en el objetivo frente al gasto esperado en el objetivo en todos los paquetes de la campaña, para que pueda identificar de un vistazo las campañas con bajo rendimiento. Si lo desea, puede [cambiar la vista de columna](campaign-data-views-manage.md#column-view-change) o incluso [crear una vista de columna personalizada](campaign-data-views-manage.md#column-view-create).

Puede hacer lo siguiente [personalizar las tablas de datos](campaign-data-views-manage.md#data-tables-manage) de formas adicionales y [filtrar los datos visibles](campaign-data-views-manage.md#filter-data-tables).

Para ver una campaña con más detalle, haga clic en su nombre.

#### Indicadores de alerta

*Función beta*

Un &quot;[!UICONTROL Alerts]&quot; indica cuándo una campaña, o cualquier entidad secundaria debajo de ella, tiene un problema. A [!UICONTROL Pulse Panel] a la derecha de la barra de herramientas también indica si hay alertas disponibles para las entidades que se muestran. Consulte &quot;[Ver alertas](campaign-alerts.md)&quot; para obtener más información.

## Informes de campaña única {#single-campaign-reporting}

Dentro de una campaña, puede filtrar los datos en función de la entidad de la campaña: [!UICONTROL Packages], [!UICONTROL Placements], y [!UICONTROL Ads]. Puede hacer lo siguiente [filtrar los datos visibles](campaign-data-views-manage.md#filter-data-tables) para incluir solo los paquetes, las ubicaciones o los anuncios que desee ver.

![Fichas de entidad de campaña](/help/dsp/assets/campaign-subtabs.png)

### Vista de gráfico

En cada campaña puede hacer lo siguiente [personalizar gráficos de tendencias de series temporales](campaign-data-views-manage.md#data-visualizations-manage) con tres métricas, que están disponibles en cada vista de entidad. Las mismas métricas se mantienen en todos los gráficos de tendencias de la campaña.

Consulte la [Sección &quot;Visualización de gráfico&quot; sobre las métricas de varias campañas](#chart-view) para obtener más información.

### Visualización en tabla

En cada pestaña de entidad, cada fila incluye métricas de ritmo y envío de forma predeterminada, pero se puede [cambiar la vista de columna](campaign-data-views-manage.md#column-view-change) o incluso [crear una vista de columna personalizada](campaign-data-views-manage.md#column-view-create) para aplicar en todas las subpestañas de la campaña. Puede hacer lo siguiente [personalizar las tablas de datos](campaign-data-views-manage.md#data-tables-manage) de formas adicionales. Cada tabla de datos incluye una [!UICONTROL Subtotals] fila, que muestra la suma o el valor promedio de cada métrica en todas las filas visibles.

#### Indicadores de alerta

*Función beta*

Un &quot;[!UICONTROL Alerts]&quot; indica cuándo un paquete, una ubicación o un anuncio (o cualquier entidad secundaria de un paquete o una ubicación) tiene un problema. Un &quot;[!UICONTROL Alerts]&quot; indica cuándo una campaña, o cualquier entidad secundaria debajo de ella, tiene un problema. A [!UICONTROL Pulse Panel] a la derecha de la barra de herramientas también indica si hay alertas disponibles para las entidades que se muestran. Consulte &quot;[Ver alertas](campaign-alerts.md)&quot; para obtener más información.

### Otros tipos de informes de nivel de campaña

Para otros desgloses de datos, consulte [las páginas de informes de nivel de campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md). El informe incluye secciones sobre [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], y [!UICONTROL Audience Performance] datos.

### Otros tipos de informes de nivel de ubicación

Para otros desgloses de datos, consulte [las páginas de informes de nivel de ubicación](/help/dsp/campaign-management/placements/placement-view-report.md). El informe incluye secciones sobre [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications], y [!UICONTROL Ads] datos.

Además, puede ver los siguientes datos dentro de la configuración de ubicación:

* [A (vista de detalles) [!UICONTROL Inspector])](placement-details-view.md), que muestra todos los sitios segmentados, los anuncios, los datos de frecuencia y las ofertas de una ubicación.

* A [informe de previsión de ubicación](/help/dsp/campaign-management/reports/placement-forecast.md)

* [Informes de diagnóstico de ubicación](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Otros tipos de informes de nivel de anuncios

Para otros desgloses de datos, consulte [las páginas de informes de nivel de anuncio](/help/dsp/campaign-management/ads/ad-view-report.md). El informe incluye [!UICONTROL Overview], [!UICONTROL Geography], y [!UICONTROL Viewability] datos.

>[!MORELIKETHIS]
>
>* [Ver los sitios, anuncios y detalles de frecuencia de una ubicación](placement-details-view.md)
>* [Administrar Las Vistas De Datos De Campaign](campaign-data-views-manage.md)
>* [Exportar datos desde una vista de Campaign Management](campaign-export-data.md)
>* [Ver un informe detallado de una campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Ver alertas](campaign-alerts.md)
