---
title: Ver los detalles de sitios, anuncios, frecuencia e inventario de una ubicación
description: Obtenga información sobre cómo ver los sitios segmentados, los anuncios, la frecuencia y los datos de inventario de una ubicación.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 0f022babeab6c044949760cedc103323eb0cc950
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Ver los detalles de sitios, anuncios, frecuencia e inventario de una ubicación

Para cada ubicación, puede [abrir un (vista de detalles [!UICONTROL Inspector])](placement-details-view.md), que enumera todos los sitios de destino, anuncios y ofertas de una ubicación. También incluye datos de frecuencia para la ubicación. Si lo desea, puede exportar los datos desde cualquier pestaña.

![Inspector de ubicación](/help/dsp/assets/placement-inspector.png)

## Información en la ubicación [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Todos los sitios en los que la ubicación ha tenido impresiones.

  La ficha [!UICONTROL Sites] incluye características de búsqueda y filtro, las mismas opciones de vista de columna estándar y personalizada que están disponibles en la página principal, y un botón [!UICONTROL Exclude] en cada fila para que pueda excluir rápidamente un sitio de la ubicación.

* **[!UICONTROL Ads]:** Todos los anuncios de la ubicación.

  La ficha [!UICONTROL Ads] incluye características de búsqueda y filtro, las mismas opciones de vista de columna estándar y personalizada que están disponibles en la página principal y botones de acción rápida en cada fila, como [!UICONTROL View Ad Approvals].

* **[!UICONTROL Frequency]:** Datos para cada nivel de frecuencia de anuncio para la ubicación, incluidos:
   * el nivel de frecuencia de anuncio (como &quot;1&quot; para todas las instancias en las que los usuarios vieron un anuncio una vez)
   * número único estimado de dispositivos, exploradores o personas (según el [!UICONTROL Cross Device Level] especificado para la campaña) que recibieron impresiones en el nivel de frecuencia especificado
   * el número estimado de impresiones en el nivel de frecuencia especificado
   * la frecuencia media estimada para el nivel de frecuencia especificado. Este valor es igual a (Impresiones estimadas)/(Valores exclusivos estimados).

* **[!UICONTROL Inventory]:** Información sobre todas las ofertas direccionadas por la ubicación.

  La ficha [!UICONTROL Inventory] permite la solución rápida de problemas mostrando estadísticas de rendimiento, como [!UICONTROL Auctions], [!UICONTROL Bids] y [!UICONTROL Win Rate]. La pestaña incluye características de búsqueda y filtro, las mismas opciones de vista de columna estándar y personalizadas que están disponibles en la página principal y botones de acción rápida en cada fila, incluidos [!UICONTROL Edit], [!UICONTROL View Report] y [[!UICONTROL Auction Insights] para obtener más información sobre la solución de problemas](/help/dsp/inventory/private-deal-auction-insights.md).

## Abrir [!UICONTROL Placement Inspector] {#inspector-open}

1. Abra la vista de ubicaciones de la campaña o el paquete principal:

   * Vea todas las ubicaciones dentro de la campaña principal:

      1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

      1. Haga clic en el nombre de la campaña.

      1. Haga clic en la ficha **[!UICONTROL Placements]**.

   * Ver todas las ubicaciones dentro del paquete principal:

      1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

      1. Haga clic en el nombre de la campaña.

      1. Haga clic en la ficha **[!UICONTROL Packages]**.

      1. Haga clic en el nombre del paquete principal.

1. Mantenga el cursor sobre la fila de ubicación y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Inspector]**.

1. (Opcional) [Cambie la vista de columna](campaign-data-views-manage.md#column-view-change) según sea necesario para ver las métricas requeridas.

1. (Opcional) Para exportar los datos de cualquier ficha, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más") en la esquina superior derecha y, a continuación, haga clic en **[!UICONTROL Export]**.

   Los datos se guardan en la carpeta de descarga predeterminada del explorador como un informe en formato XLSM.

## Quitar un anuncio de una ubicación de [!UICONTROL Placement Inspector] {#remove-ads-placement-inspector}

1. [Abrir [!UICONTROL Placement Inspector]](#inspector-open).

1. Haga clic en la ficha **[!UICONTROL Ads]**.

1. Junto al nombre del anuncio, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Detach]**.

## Solucionar problemas de inventario

| Problema | Causa posible | Acciones que se deben realizar |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | El publicador no ha comenzado a enviar solicitudes de oferta. | Póngase en contacto con el editor para activar la oferta. |
| | La operación se configuró incorrectamente, por ejemplo, introduciendo un ID de oferta externa incorrecto. | Confirme los detalles de la oferta y edite la oferta. |
| [!UICONTROL Auctions but no Bids] | La segmentación de ubicación no coincide con las solicitudes de oferta entrantes para la oferta. <br><br> Por ejemplo, una ubicación podría estar segmentando una ubicación geográfica que no cumpla los requisitos para la oferta. | Edite los destinos de colocación según sea necesario para evitar discrepancias en los objetivos. |
| | La ubicación no tiene un anuncio activo con el tipo de medios requerido para la oferta. | Cree y adjunte un anuncio con el tipo de medio correcto a la ubicación. |
| | La ubicación no tiene un presupuesto adecuado. | Aumente el presupuesto de colocación para permitir pujas en las solicitudes entrantes. |
| | Las fechas de vuelo de la ubicación no se superponen con las fechas de entrega de la impresión para la oferta. | Edite las fechas de vuelo de la ubicación según sea necesario. |
| [!UICONTROL Low Win Rate] | La puja máxima de la ubicación (mínima o fija) está por debajo del mínimo requerido por la oferta. | Aumente la ubicación [!UICONTROL Max Bid] según sea necesario. |
| | La ubicación utiliza filtros de oferta previa que limitan las ofertas. | Reduzca los umbrales de los filtros de oferta previa para permitir más ofertas. |
| | La segmentación de audiencia para la ubicación es demasiado restrictiva. | Compruebe si los objetivos de audiencia especificados tienen suficientes usuarios activos y expanda la audiencia si es posible. |

>[!MORELIKETHIS]
>
>* [Tipos de informes de rendimiento en las vistas de administración de campañas](campaign-reports-about.md)
>* [Administrar Las Vistas De Datos De Campaign](campaign-data-views-manage.md)
