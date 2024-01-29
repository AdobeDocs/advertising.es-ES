---
title: Ver los detalles de sitios, anuncios, frecuencia e inventario de una ubicación
description: Obtenga información sobre cómo ver los sitios segmentados, los anuncios, la frecuencia y los datos de inventario de una ubicación.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Ver los detalles de sitios, anuncios, frecuencia e inventario de una ubicación

En cada ubicación puede hacer lo siguiente [abrir un (vista de detalles) [!UICONTROL Inspector])](placement-details-view.md), que enumera todos los sitios segmentados, los anuncios y las ofertas de una ubicación. También incluye datos de frecuencia para la ubicación. Si lo desea, puede exportar los datos desde cualquier pestaña.

![ubicación Inspector](/help/dsp/assets/placement-inspector.png)

## Información en la ubicación [!UICONTROL Inspector] {#placement-inspector}

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

## Abra el [!UICONTROL Placement Inspector]

1. Abra la vista de ubicaciones de la campaña o el paquete principal:

   * Vea todas las ubicaciones dentro de la campaña principal:

      1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

      1. Haga clic en el nombre de la campaña.

      1. Haga clic en **[!UICONTROL Placements]** pestaña.

   * Ver todas las ubicaciones dentro del paquete principal:

      1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

      1. Haga clic en el nombre de la campaña.

      1. Haga clic en **[!UICONTROL Packages]** pestaña.

      1. Haga clic en el nombre del paquete principal.

1. Mantenga el cursor sobre la fila de colocación y haga clic en **[!UICONTROL More]** y, a continuación, haga clic en una opción:

   * Para ver todos los sitios de destino de la ubicación, haga clic en **[!UICONTROL Sites]**.

   * Para ver todos los anuncios de la ubicación, haga clic en **[!UICONTROL Ads]**.

   * Para ver los datos de frecuencia de la ubicación, haga clic en **[!UICONTROL Frequency]**.

   * Para ver todas las ofertas a las que se dirige la ubicación, haga clic en **[!UICONTROL Inventory]**.

1. (Opcional) [Cambio de la vista de columna](campaign-data-views-manage.md#column-view-change) según sea necesario para ver las métricas requeridas.

1. (Opcional) Para exportar los datos en cualquier pestaña, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más") en la esquina superior derecha y, a continuación, haga clic en **[!UICONTROL Export]**.

   Los datos se guardan en la carpeta de descarga predeterminada del explorador como un informe en formato XLSM.

## Solucionar problemas de inventario

| Problema | Causa posible | Acciones que se deben realizar |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | El publicador no ha comenzado a enviar solicitudes de oferta. | Póngase en contacto con el editor para activar la oferta. |
| | La operación se configuró incorrectamente, por ejemplo, introduciendo un ID de oferta externa incorrecto. | Confirme los detalles de la oferta y edite la oferta. |
| [!UICONTROL Auctions but no Bids] | La segmentación de ubicación no coincide con las solicitudes de oferta entrantes para la oferta. <br><br> Por ejemplo, una ubicación podría estar dirigida a una ubicación geográfica que no cumpla los requisitos para la oferta. | Edite los destinos de colocación según sea necesario para evitar discrepancias en los objetivos. |
| | La ubicación no tiene un anuncio activo con el tipo de medios requerido para la oferta. | Cree y adjunte un anuncio con el tipo de medio correcto a la ubicación. |
| | La ubicación no tiene un presupuesto adecuado. | Aumente el presupuesto de colocación para permitir pujas en las solicitudes entrantes. |
| | Las fechas de vuelo de la ubicación no se superponen con las fechas de entrega de la impresión para la oferta. | Edite las fechas de vuelo de la ubicación según sea necesario. |
| [!UICONTROL Low Win Rate] | La puja máxima de la ubicación (mínima o fija) está por debajo del mínimo requerido por la oferta. | Aumente el de la ubicación [!UICONTROL Max Bid] según sea necesario. |
| | La ubicación utiliza filtros de oferta previa que limitan las ofertas. | Reduzca los umbrales de los filtros de oferta previa para permitir más ofertas. |
| | La segmentación de audiencia para la ubicación es demasiado restrictiva. | Compruebe si los objetivos de audiencia especificados tienen suficientes usuarios activos y expanda la audiencia si es posible. |

>[!MORELIKETHIS]
>
>* [Tipos de informes de rendimiento en las vistas de Campaign Management](campaign-reports-about.md)
>* [Administrar Las Vistas De Datos De Campaign](campaign-data-views-manage.md)
