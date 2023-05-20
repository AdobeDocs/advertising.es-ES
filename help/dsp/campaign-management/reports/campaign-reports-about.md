---
title: Acerca de los informes en la plataforma
description: Obtenga información acerca de los datos de informes incluidos en las vistas de administración de campañas.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Acerca de los informes en la plataforma

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Las vistas de administración de campañas incluyen datos de informe completos. Los informes disponibles le ayudan a identificar los paquetes y las ubicaciones que tienen un buen rendimiento y aquellos que necesitan su atención. Los botones de acción rápida también le hacen más productivo.

## Vista de todas las campañas

El [!UICONTROL Campaigns] esta vista permite acceder a un conjunto de gráficos de datos de rendimiento y a una lista de todas las campañas de su cuenta.

### Vista de gráfico {#chart-view}

Puede [personalizar gráficos de tendencias de series temporales](campaign-data-visualization-manage.md) en todas las campañas con tres métricas. De forma predeterminada, los datos de [!UICONTROL Net Spend], [!UICONTROL Impressions], y [!UICONTROL Net CPM] se incluyen en gráficos separados (gráficos de enrejado). Si lo desea, puede cambiar las métricas. Para habilitar los datos por hora en los gráficos de tendencias de series temporales, cambie la selección de fecha a un solo día ([!UICONTROL Today], [!UICONTROL Yesterday], o un día específico).

![separar gráficos de tendencias para tres métricas](/help/dsp/assets/trend-chart-separate.png)

También puede superponer las tres métricas para facilitar la detección de anomalías y áreas en las que se puede mejorar la escala o el rendimiento.

![gráfico de tendencias con superposición](/help/dsp/assets/trend-chart.png)

### Visualización en tabla

![Lista de campañas](/help/dsp/assets/campaigns-list.png)

De forma predeterminada, cada fila de campaña incluye métricas de ritmo y entrega. Las métricas de ritmo incluyen [!UICONTROL Gross Spend (Lifetime)], que incluye una medición del gasto real en el objetivo frente al gasto esperado en el objetivo en todos los paquetes de la campaña, para que pueda identificar de un vistazo las campañas con bajo rendimiento. Si lo desea, puede [cambiar la vista de columna](column-view-change.md) o incluso [crear una vista de columna personalizada](column-view-create.md).

Puede hacer lo siguiente [personalizar las tablas de datos](campaign-data-views-about.md) de formas adicionales y [filtrar los datos visibles](campaign-data-filter.md).

Para ver una campaña con más detalle, haga clic en su nombre.

## Informes de campaña única {#single-campaign-reporting}

Dentro de una campaña, puede filtrar los datos en función de la entidad de la campaña: [!UICONTROL Packages], [!UICONTROL Placements], y [!UICONTROL Ads]. Puede hacer lo siguiente [filtrar los datos visibles](campaign-data-filter.md) para incluir solo los paquetes, las ubicaciones o los anuncios que desee ver.

![Fichas de entidad de campaña](/help/dsp/assets/campaign-subtabs.png)

### Vista de gráfico

En cada campaña puede hacer lo siguiente [personalizar gráficos de tendencias de series temporales](campaign-data-visualization-manage.md) con tres métricas, que están disponibles en cada vista de entidad. Las mismas métricas se mantienen en todos los gráficos de tendencias de la campaña.

Consulte la [Sección &quot;Visualización de gráfico&quot; sobre las métricas de varias campañas](#chart-view) para obtener más información.

### Visualización en tabla

En cada pestaña de entidad, cada fila incluye métricas de ritmo y envío de forma predeterminada, pero se puede [cambiar la vista de columna](column-view-change.md) o incluso [crear una vista de columna personalizada](column-view-create.md) para aplicar en todas las subpestañas de la campaña. Puede hacer lo siguiente [personalizar las tablas de datos](campaign-data-views-about.md) de formas adicionales. Cada tabla de datos incluye una [!UICONTROL Subtotals] fila, que muestra la suma o el valor promedio de cada métrica en todas las filas visibles.

### Ubicación [!UICONTROL Inspector] {#placement-inspector}

En cada ubicación puede hacer lo siguiente [abrir un (vista de detalles) [!UICONTROL Inspector])](placement-details-view.md), que incluye los siguientes datos exhaustivos:

* **[!UICONTROL Sites]:** Todos los sitios en los que la ubicación ha tenido impresiones.

   El [!UICONTROL Sites] La pestaña incluye funciones de búsqueda y filtro, las mismas opciones de vista de columna estándar y personalizadas que están disponibles en la página principal y una [!UICONTROL Exclude] en cada fila para poder excluir rápidamente un sitio de la ubicación.

* **[!UICONTROL Ads]:** Todos los anuncios de la ubicación.

   El [!UICONTROL Ads] La pestaña incluye funciones de búsqueda y filtro, las mismas opciones de vista de columna estándar y personalizadas que están disponibles en la página principal y botones de acción rápida en cada fila, como [!UICONTROL Pause] (para pausar rápidamente un anuncio).

* **[!UICONTROL Frequency]:** Datos de cada nivel de frecuencia de anuncio para la ubicación, incluidos:
   * el nivel de frecuencia de anuncio (como &quot;1&quot; para todas las instancias en las que los usuarios vieron un anuncio una vez)
   * el número único estimado de dispositivos, exploradores o personas (según el especificado). [!UICONTROL Cross Device Level] para la campaña) que recibieron impresiones en el nivel de frecuencia especificado
   * el número estimado de impresiones en el nivel de frecuencia especificado
   * la frecuencia media estimada para el nivel de frecuencia especificado. Este valor es igual a (Impresiones estimadas)/(Valores exclusivos estimados).

* **[!UICONTROL Inventory]:** Información sobre todas las ofertas segmentadas por la ubicación.

   El [!UICONTROL Inventory] La pestaña de permite una solución de problemas rápida mostrando estadísticas de rendimiento, como [!UICONTROL Auctions], [!UICONTROL Bids], y [!UICONTROL Win Rate]. La pestaña incluye funciones de búsqueda y filtro, las mismas opciones de vista de columna estándar y personalizadas disponibles en la página principal y botones de acción rápida en cada fila, como [!UICONTROL Edit], [!UICONTROL View Report], y [[!UICONTROL Auction Insights] para una mayor resolución de problemas](/help/dsp/inventory/private-deal-auction-insights.md).

#### Solucionar problemas de inventario

| Problema | Causa posible | Acciones que se deben realizar |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | El publicador no ha comenzado a enviar solicitudes de oferta. | Póngase en contacto con el editor para activar la oferta. |
|  | La operación se configuró incorrectamente, por ejemplo, introduciendo un ID de oferta externa incorrecto. | Confirme los detalles de la oferta y edite la oferta. |
| [!UICONTROL Auctions but no Bids] | La segmentación de ubicación no coincide con las solicitudes de oferta entrantes para la oferta. <br><br> Por ejemplo, una ubicación podría estar dirigida a una ubicación geográfica que no cumpla los requisitos para la oferta. | Edite los destinos de colocación según sea necesario para evitar discrepancias en los objetivos. |
|  | La ubicación no tiene un anuncio activo con el tipo de medios requerido para la oferta. | Cree y adjunte un anuncio con el tipo de medio correcto a la ubicación. |
|  | La ubicación no tiene un presupuesto adecuado. | Aumente el presupuesto de colocación para permitir pujas en las solicitudes entrantes. |
|  | Las fechas de vuelo de la ubicación no se superponen con las fechas de entrega de la impresión para la oferta. | Edite las fechas de vuelo de la ubicación según sea necesario. |
| [!UICONTROL Low Win Rate] | La puja máxima de la ubicación (mínima o fija) está por debajo del mínimo requerido por la oferta. | Aumente el de la ubicación [!UICONTROL Max Bid] según sea necesario. |
|  | La ubicación utiliza filtros de oferta previa que limitan las ofertas. | Reduzca los umbrales de los filtros de oferta previa para permitir más ofertas. |
|  | La segmentación de audiencia para la ubicación es demasiado restrictiva. | Compruebe si los objetivos de audiencia especificados tienen suficientes usuarios activos y expanda la audiencia si es posible. |

![ubicación Inspector](/help/dsp/assets/placement-inspector.png)

Puede exportar los datos en el [!UICONTROL Sites], [!UICONTROL Ads], o [!UICONTROL Frequency] a la carpeta de descarga predeterminada del explorador como un informe en formato XLSM.

### Otros tipos de informes de nivel de campaña

Para otros desgloses de datos, consulte [las páginas de informes de nivel de campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md). El <!--legacy --> el informe incluye secciones sobre [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], y [!UICONTROL Audience Performance] datos.

>[!MORELIKETHIS]
>
>* [Ver los sitios, anuncios y detalles de frecuencia de una ubicación](placement-details-view.md)
>* [Acerca de las vistas de datos de Campaign](campaign-data-views-about.md)
>* [Crear una vista de columna personalizada](column-view-create.md)
>* [Cambio de la vista de columna](column-view-change.md)
>* [Administrar visualizaciones de datos](campaign-data-visualization-manage.md)
>* [Exportar datos desde una vista de Campaign Management](campaign-export-data.md)
>* [Ver un informe detallado de una campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

