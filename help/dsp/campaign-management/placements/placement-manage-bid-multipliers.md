---
title: Administrar multiplicadores de oferta para ubicaciones
description: Aprenda a crear y editar multiplicadores de oferta para sus destinos de colocación.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 28f1b799daaa4e511abab1102a639e72b3a32d18
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Administrar multiplicadores de oferta para ubicaciones

Puede crear y administrar multiplicadores de oferta, por los cuales se multiplica una oferta calculada de forma algorítmica para aumentar o disminuir la oferta, para los objetivos de colocación existentes de [tipos de destinatario aptos](#bid-multiplier-by-target). Puede editar manualmente los valores del multiplicador de oferta para una ubicación o cargar una hoja de cálculo con valores para una o varias ubicaciones.

De forma predeterminada, el multiplicador de oferta para un objetivo es 1,00, lo que significa que la oferta no se ajusta para ese objetivo. Los valores pueden variar de 0,10 a 10,00. Por ejemplo, un multiplicador de oferta de 0,5 reduce una oferta de 6 USD a 3 USD (0,5 x 6). Cuando una subasta cumple los requisitos para varios modificadores de oferta, se multiplican todos los multiplicadores de oferta aplicables. Por ejemplo, si California tiene un multiplicador de oferta de 2 y San Francisco tiene un multiplicador de oferta de 3, el multiplicador de oferta final para los anuncios que se ejecutan en San Francisco es 6.

>[!NOTE]
>
>Los multiplicadores de ofertas nunca aumentan la oferta por encima de la oferta máxima.

Puede establecer multiplicadores de oferta (con valores distintos de 1,00) para una [número limitado de objetivos](#bid-multiplier-limits-by-target).

Esta función funciona con los destinos de colocación existentes. Para cambiar los destinos seleccionados para las ubicaciones, consulte[Editar ubicaciones](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Administrar los multiplicadores de oferta para una sola ubicación

Puede editar valores manualmente o cargar una hoja de cálculo para una sola ubicación.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Junto al nombre de la ubicación, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Ajuste de los multiplicadores de oferta para los objetivos aptos:

   * Para ajustar manualmente los valores del multiplicador de oferta, cambie a cada [ficha específica de target](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], y [!UICONTROL Brand Safety]) y edite los valores existentes para los destinos de colocación.

     La mayoría de las categorías de destino muestran subcategorías a la izquierda. Haga clic en una subcategoría para administrar los multiplicadores de oferta de esa subcategoría, según corresponda.

   * Para cargar un archivo CSV con valores de multiplicador de oferta y sobrescribir todos los valores existentes:

      1. Clic **[!UICONTROL CSV File Edit]** en la parte superior derecha.

      1. Haga clic en **[!UICONTROL Download Template]** y editar el archivo o b) editar una plantilla descargada previamente. Guarde el archivo editado en su dispositivo o red.

         Las hojas de cálculo descargadas incluyen una hoja para cada tipo de destino (como País, Fuentes y Categoría del sitio). Solo se incluyen los multiplicadores de oferta existentes con valores &lt; 1,0 o > 1,0.

         * Para agregar un multiplicador de oferta para un destino existente, introduzca el destino utilizando la misma sintaxis visible en la interfaz de usuario y el valor del multiplicador de oferta correspondiente.

         * Para quitar un modificador de oferta, establezca el valor del multiplicador de oferta en 1,0 o elimine toda la información de la fila.

         ![Fila de ejemplo en un archivo de hoja de cálculo del multiplicador de ofertas](/help/dsp/assets/bid-multiplier-spreadsheet.png "Fila de ejemplo en un archivo de hoja de cálculo del multiplicador de ofertas")

      1. Clic **[!UICONTROL Next]** para desplazarse a [!UICONTROL Upload File] y a) arrastre y suelte el archivo editado en el cuadro o b) haga clic dentro del cuadro para seleccionar el archivo desde el dispositivo o la red.

      1. Compruebe los datos cargados en la [!UICONTROL Review & Submit] y haga clic en **[!UICONTROL Save]**.

## Cargar multiplicadores de oferta para una o más ubicaciones

Cargue una hoja de cálculo para aplicar los mismos valores a todas las ubicaciones seleccionadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Seleccione la casilla de verificación situada junto a cada ubicación cuyos multiplicadores de oferta desee administrar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. Cargue un archivo CSV con valores de multiplicador de oferta para sobrescribir todos los valores existentes de todas las ubicaciones seleccionadas.

   1. Haga clic en **[!UICONTROL Download Template]** y editar el archivo o b) editar una plantilla descargada previamente. Guarde el archivo editado en su dispositivo o red.

      Las hojas de cálculo descargadas incluyen una hoja para cada tipo de destino (como País, Fuentes y Categoría del sitio). Solo se incluyen los multiplicadores de oferta existentes con valores &lt; 1,0 o > 1,0.

      * Para agregar un multiplicador de oferta para un destino existente, introduzca el destino utilizando la misma sintaxis visible en la interfaz de usuario y el valor del multiplicador de oferta correspondiente.

      * Para quitar un modificador de oferta, establezca el valor del multiplicador de oferta en 1,0 o elimine toda la información de la fila.

      ![Fila de ejemplo en un archivo de hoja de cálculo del multiplicador de ofertas](/help/dsp/assets/bid-multiplier-spreadsheet.png "Fila de ejemplo en un archivo de hoja de cálculo del multiplicador de ofertas")

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
