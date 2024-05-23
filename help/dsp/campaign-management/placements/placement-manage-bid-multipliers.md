---
title: Administrar multiplicadores de oferta para ubicaciones
description: Aprenda a crear y editar multiplicadores de oferta para sus destinos de colocación.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 5f358bbc63a5767649f42551f05cfae9fdc2b445
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 2%

---

# Administrar multiplicadores de oferta para ubicaciones

Puede crear y administrar multiplicadores de oferta, por los cuales se multiplica una oferta para aumentar o disminuir la oferta, para los objetivos de colocación existentes de [tipos de destinatario aptos](#bid-multiplier-by-target). Puede editar manualmente los valores del multiplicador de oferta o cargar una hoja de cálculo con valores.

De forma predeterminada, el multiplicador de oferta para un objetivo es 1,00, lo que significa que la oferta no se ajusta para ese objetivo. Los valores pueden variar de 0,10 a 10,00. Por ejemplo, un modificador de oferta de 0,5 reduce una oferta de 6 USD a 3 USD (0,5 x 6). Cuando una subasta cumple los requisitos para varios modificadores de oferta, se multiplican todos los modificadores de oferta aplicables. Los modificadores de oferta nunca aumentan la oferta por encima de la oferta máxima.

Puede establecer multiplicadores de oferta (con valores distintos de 1,00) para una [número limitado de objetivos](#bid-multiplier-limits-by-target).

Esta función funciona con los destinos de colocación existentes. Para cambiar los destinos seleccionados para las ubicaciones, consulte[Editar ubicaciones](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Junto al nombre de la ubicación, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Ajuste manualmente los multiplicadores de oferta para los objetivos aptos o cargando un archivo CSV con valores de objetivo:

   * Para ajustar manualmente los valores del multiplicador de oferta, cambie a cada [ficha específica de target](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], y [!UICONTROL Brand Safety]) y edite los valores existentes para los destinos de colocación. La mayoría de las categorías de destino muestran subcategorías a la izquierda. Haga clic en una subcategoría para administrar los multiplicadores de oferta de esa subcategoría, cuando corresponda.

   * Para cargar un archivo CSV con valores de multiplicador de oferta y sobrescribir los valores existentes:

      1. Clic **[!UICONTROL CSV File Edit]** en la parte superior derecha.

      1. Haga clic en **[!UICONTROL Download Template]** e introduzca los objetivos utilizando la misma sintaxis visible en la interfaz de usuario y los valores del multiplicador de oferta correspondientes o b) edite una plantilla descargada anteriormente con la misma información. Guarde el archivo editado en su dispositivo o red.

      1. Clic **[!UICONTROL Next]** para desplazarse a [!UICONTROL Upload File] y a) arrastre y suelte el archivo editado en el cuadro o b) haga clic dentro del cuadro para seleccionar el archivo desde el dispositivo o la red.

      1. Compruebe los datos cargados en la [!UICONTROL Review & Submit] y haga clic en **[!UICONTROL Save]**.

## Tipos de objetivo aptos para multiplicadores de oferta {#bid-multiplier-by-target}

Solo puede configurar modificadores de oferta para destinos incluidos, no excluidos.

* **Destinos geográficos**: geografía (países, estados y ciudades), códigos postales y DMA

* **Destinos de inventario**: fuentes y fuentes para inventario público y [!UICONTROL On Demand] inventario

* **Destinos del sitio:** sitios/aplicaciones segmentados (pero no excluidos), categorías de sitios

* **Destinos de audiencia:** segmentos, partes del día y temas

* **targets ads.txt:** (Cuando se excluye de ads.txt, que le permite comprar inventario de todos los vendedores) solo vendedores de ads.txt, vendedores directos de ads.txt y vendedores de ads.txt más sitios sin ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Número máximo de multiplicadores de oferta por tipo de destino {#bid-multiplier-limits-by-target}

Puede establecer multiplicadores de oferta (con valores distintos de 1,00) para un número limitado de destinatarios. Por ejemplo, puede establecer multiplicadores de oferta para un máximo de 20 destinos de país. A continuación se muestra el número máximo de destinos para cada tipo de destino que puede tener multiplicadores de oferta.

| Categoría | Parámetro | Número máximo |
| -------- | --------- | ----- |
| Geo | País | 20 |
| Geo | Estado | 100 |
| Geo | Ciudad | 100 |
| Geo | Metro | 100 |
| Geo | Códigos postales | 100 |
| Inventario | Fuentes | 100 |
| Inventario | Fuentes | 100 |
| Sites | Categoría del sitio | 100 |
| Sites | Sitios/aplicaciones | 100 |
| Público | Segmentos | 500 |
| Público | Temas | 100 |
| Seguridad de marca | Ads.txt | N/D |

>[!MORELIKETHIS]
>
>* [Acerca de la administración de ubicación](placement-about.md)
>* [Editar ubicaciones](placement-edit.md)
>* [Ver el registro de cambios de una ubicación](placement-change-log.md)
>* [Configuración de ubicación](placement-settings.md)
