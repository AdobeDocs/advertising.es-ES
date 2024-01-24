---
title: Especificar ubicaciones y anuncios para una oferta privada
description: Aprenda a utilizar un acuerdo privado con ubicaciones y anuncios adicionales.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: d6d295119bc974a87840e757877c1507237a6fa2
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Especificar ubicaciones y anuncios para una oferta privada

Para ofertas no garantizadas, puede especificar la oferta como un objetivo de inventario para nuevas ubicaciones desde el [!UICONTROL Placements] vista.

Para ofertas programáticas garantizadas (PG), puede crear ubicaciones con anuncios especificados desde el [!UICONTROL Deals] vista.

También puede [adjuntar anuncios a ubicaciones](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) asociadas con PG y ofertas no garantizadas en cualquier momento.

## Especificar un acuerdo no garantizado como destino de inventario para una ubicación

* [Cree una ubicación desde el [!UICONTROL Placements] vista](/help/dsp/campaign-management/placements/placement-create.md). En el [!UICONTROL Inventory Targeting] , seleccione la oferta privada.

## Adjuntar ubicaciones y anuncios a una oferta de PG

1. En el menú principal, haga clic en **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. En la fila de la oferta, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. En el [!UICONTROL Ad & Campaign Selection] , seleccione los anuncios que se utilizarán para la ubicación:

       1. Seleccione el anunciante, la campaña y el tipo de anuncio. Si lo desea, seleccione un estado de anuncio según el cual filtrar los anuncios.
       
       1. En la lista de anuncios disponibles, seleccione la casilla de verificación situada junto a cada anuncio que se utilizará para la oferta.
       
       1. Haga clic en **[!UICONTROL Apply]**.
   
   1. En la pantalla de configuración de ubicación:

      1. Introduzca el nombre de la ubicación.

      1. (Opcional) Edite el [configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md), incluida la sobrescritura de la oferta predeterminada, que se rellena automáticamente con el valor CPM de la oferta, el cambio del intervalo de fechas o la adición de más anuncios.

      El acuerdo se establece automáticamente como objetivo en la sección Destinos de inventario. Todas las demás opciones de segmentación no son aplicables.

      1. Clic **[!UICONTROL Create placement]**.

La ubicación empezará a ejecutarse después de que el editor active su ID de acuerdo de PG.

>[!NOTE]
>
> No es necesario que envíe la etiqueta de la oferta al editor para su verificación.

>[!MORELIKETHIS]
>
>* [Acerca del inventario privado](private-inventory-about.md)
>* [Enumerar las ubicaciones y los anuncios para una oferta privada](/help/dsp/inventory/private-deal-view-placements.md)
>* [Creación manual de detalles de ID de acuerdo](deal-id-create.md)
>* [Configuración del ID de acuerdo manual](deal-id-settings.md)
>* [Configurar una oferta garantizada programática](programmatic-guaranteed-set-up.md)
