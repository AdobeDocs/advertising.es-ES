---
title: Tipos de informes de rendimiento en las vistas de Campaign Management
description: Obtenga información acerca de los datos de informes incluidos en las vistas de administración de campañas.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: eba8e9813f8daea58b30f7890ac2dca2498f326f
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Tipos de informes de rendimiento en las vistas de Campaign Management

Las vistas de administración de campañas incluyen datos de informe completos. Los informes disponibles le ayudan a identificar los paquetes y las ubicaciones que tienen un buen rendimiento y aquellos que necesitan su atención. Los botones de acción rápida también le hacen más productivo.

## Vista de todas las campañas

La vista [!UICONTROL Campaigns] se abre con un conjunto de gráficos de datos de rendimiento y una lista de todas las campañas de su cuenta.

### Vista de gráfico {#chart-view}

Puede [personalizar gráficos de tendencias de series temporales](campaign-data-views-manage.md#data-visualizations-manage) en todas las campañas usando tres métricas. De manera predeterminada, los datos de [!UICONTROL Net Spend], [!UICONTROL Impressions] y [!UICONTROL Net CPM] se incluyen en gráficos independientes (gráficos de enrejado). Si lo desea, puede cambiar las métricas. Para habilitar los datos por hora en los gráficos de tendencias de series temporales, cambie la selección de fechas a un solo día ([!UICONTROL Today], [!UICONTROL Yesterday] o un día específico).

![gráficos de tendencias independientes para tres métricas](/help/dsp/assets/trend-chart-separate.png)

También puede superponer las tres métricas para facilitar la detección de anomalías y áreas en las que se puede mejorar la escala o el rendimiento.

![gráfico de tendencias con superposición](/help/dsp/assets/trend-chart.png)

### Visualización en tabla

![Lista de campañas](/help/dsp/assets/campaigns-list.png)

De forma predeterminada, cada fila de campaña incluye métricas de ritmo y entrega. Las métricas de ritmo incluyen [!UICONTROL Gross Spend (Lifetime)], que incluye una medición del gasto real en el destino frente al gasto esperado en el destino en todos los paquetes de la campaña, de modo que pueda identificar las campañas con bajo rendimiento de un vistazo. Opcionalmente, puede [cambiar la vista de columna](campaign-data-views-manage.md#column-view-change) o incluso [crear una vista de columna personalizada](campaign-data-views-manage.md#column-view-create).

Puede [personalizar aún más las tablas de datos](campaign-data-views-manage.md#data-tables-manage) de formas adicionales y [filtrar los datos visibles](campaign-data-views-manage.md#filter-data-tables).

Para ver una campaña con más detalle, haga clic en su nombre.

#### Indicadores de alerta

Una columna &quot;[!UICONTROL Alerts]&quot; indica cuándo una campaña, o cualquier entidad secundaria debajo de ella, tiene un problema. Un icono [!UICONTROL Pulse Panel] a la derecha de la barra de herramientas también indica si hay alertas disponibles para las entidades que se muestran. Consulte &quot;[Ver alertas](campaign-alerts.md)&quot; para obtener más información.

## Informes de campaña única {#single-campaign-reporting}

Dentro de una campaña, puede filtrar los datos en función de la entidad de campaña: [!UICONTROL Packages], [!UICONTROL Placements] y [!UICONTROL Ads]. Puede [filtrar más los datos visibles](campaign-data-views-manage.md#filter-data-tables) para incluir solamente los paquetes, las ubicaciones o los anuncios que desee ver.

![Fichas de entidad de campaña](/help/dsp/assets/campaign-subtabs.png)

### Vista de gráfico

Para cada campaña, puede [personalizar gráficos de tendencias de series temporales](campaign-data-views-manage.md#data-visualizations-manage) con tres métricas, que están disponibles en cada vista de entidad. Las mismas métricas se mantienen en todos los gráficos de tendencias de la campaña.

Consulte la sección [&quot;Visualización de gráfico&quot; en las métricas entre campañas](#chart-view) para obtener más información.

### Visualización en tabla

En cada ficha de entidad, cada fila incluye métricas de ritmo y envío de forma predeterminada, pero puede [cambiar la vista de columna](campaign-data-views-manage.md#column-view-change) o incluso [crear una vista de columna personalizada](campaign-data-views-manage.md#column-view-create) para aplicarla a todas las subfichas de la campaña. Puede [personalizar aún más las tablas de datos](campaign-data-views-manage.md#data-tables-manage) de maneras adicionales. Cada tabla de datos incluye una fila [!UICONTROL Subtotals], que muestra la suma o el valor promedio de cada métrica en todas las filas visibles.

#### Indicadores de alerta

Una columna &quot;[!UICONTROL Alerts]&quot; indica cuándo un paquete, una ubicación o un anuncio (o cualquier entidad secundaria de un paquete o una ubicación) tiene un problema. Una columna &quot;[!UICONTROL Alerts]&quot; indica cuándo una campaña, o cualquier entidad secundaria debajo de ella, tiene un problema. Un icono [!UICONTROL Pulse Panel] a la derecha de la barra de herramientas también indica si hay alertas disponibles para las entidades que se muestran. Consulte &quot;[Ver alertas](campaign-alerts.md)&quot; para obtener más información.

### Otros tipos de informes de nivel de campaña

Para otros desgloses de datos, vea [las páginas de informes de nivel de campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md). El informe incluye secciones sobre datos de [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] y [!UICONTROL Audience Performance].

### Otros tipos de informes de nivel de ubicación

Para otros desgloses de datos, vea [las páginas de informes de nivel de ubicación](/help/dsp/campaign-management/placements/placement-view-report.md). El informe incluye secciones sobre datos de [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications] y [!UICONTROL Ads].

Además, puede ver los siguientes datos dentro de la configuración de ubicación:

* [A (vista de detalles [!UICONTROL Inspector])](placement-details-view.md), que muestra todos los sitios segmentados, anuncios, datos de frecuencia y ofertas para una ubicación.

* Un [informe de previsión de ubicación](/help/dsp/campaign-management/reports/placement-forecast.md).

* [Informes de diagnóstico de ubicación](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Otros tipos de informes de nivel de anuncios

Para otros desgloses de datos, vea [las páginas de informes de nivel de anuncio](/help/dsp/campaign-management/ads/ad-view-report.md). El informe incluye datos de [!UICONTROL Overview], [!UICONTROL Geography] y [!UICONTROL Viewability].

>[!MORELIKETHIS]
>
>* [Ver los sitios, anuncios y detalles de frecuencia de una ubicación](placement-details-view.md)
>* [Administrar Las Vistas De Datos De Campaign](campaign-data-views-manage.md)
>* [Exportar datos de una vista de Campaign Management](campaign-export-data.md)
>* [Ver un informe detallado de una campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Ver alertas](campaign-alerts.md)
