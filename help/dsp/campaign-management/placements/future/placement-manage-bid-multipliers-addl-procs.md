---
title: Administrar multiplicadores de oferta para ubicaciones
description: Conozca xxx
feature: DSP Placements
source-git-commit: b6758541b59f1fd924a2fe83c769f5ba385409aa
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# XXX

## Administrar los multiplicadores de oferta para una sola ubicación

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

         Las plantillas descargadas incluyen una hoja para cada tipo de destino (como País, Fuentes y Categoría del sitio). Solo se incluyen los multiplicadores de oferta existentes con valores distintos de 1,0.

         * Para agregar un multiplicador de oferta para un destino existente, introduzca el destino utilizando la misma sintaxis visible en la interfaz de usuario y el valor del multiplicador de oferta correspondiente.

         * Para quitar un modificador de oferta, establezca el valor del multiplicador de oferta en 1,0 o elimine toda la información de la fila.

         ![Fila de ejemplo en un archivo de hoja de cálculo del multiplicador de ofertas](/help/dsp/assets/bid-multiplier-spreadsheet.png "Fila de ejemplo en un archivo de hoja de cálculo del multiplicador de ofertas")

      1. Clic **[!UICONTROL Next]** para desplazarse a [!UICONTROL Upload File] y a) arrastre y suelte el archivo editado en el cuadro o b) haga clic dentro del cuadro para seleccionar el archivo desde el dispositivo o la red.

      1. Compruebe los datos cargados en la [!UICONTROL Review & Submit] y haga clic en **[!UICONTROL Save]**.

## Administrar los multiplicadores de oferta para una o más ubicaciones

<!-- verify all and edit accordingly -->

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Seleccione la casilla de verificación situada junto a cada ubicación cuyos multiplicadores de oferta desee administrar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

<!-- Check the following this functionality when available in UAT -->

1. Ajuste de los multiplicadores de oferta para los objetivos aptos:

   * Para ajustar manualmente los valores del multiplicador de oferta, vaya a cada pestaña específica de destinatario ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], y[!UICONTROL Brand Safety]) y edite los valores existentes para los destinos de colocación.

   Los mismos cambios se aplican a todas las ubicaciones seleccionadas.

* Para cargar un archivo CSV con valores de multiplicador de oferta y sobrescribir todos los valores existentes:

   1. Clic **[!UICONTROL CSV File Edit]** en la parte superior derecha.

   1. Haga clic en **[!UICONTROL Download Template]** y editar el archivo o b) editar una plantilla descargada previamente. Guarde el archivo editado en su dispositivo o red.

      Las plantillas descargadas incluyen una hoja para cada tipo de destino (como País, Fuentes y Categoría del sitio). Solo se incluyen los multiplicadores de oferta existentes con valores distintos de 1,0.

      * Para agregar un multiplicador de oferta para un destino existente, introduzca el destino utilizando la misma sintaxis visible en la interfaz de usuario y el valor del multiplicador de oferta correspondiente.

      * Para quitar un modificador de oferta, establezca el valor del multiplicador de oferta en 1,0 o elimine toda la información de la fila.

      ![Fila de ejemplo en un archivo de hoja de cálculo del multiplicador de ofertas](/help/dsp/assets/bid-multiplier-spreadsheet.png "Fila de ejemplo en un archivo de hoja de cálculo del multiplicador de ofertas")

   1. Clic **[!UICONTROL CSV Edit]** en la parte superior derecha.

   1. Haga clic en **[!UICONTROL Download Template]** y editar los valores del multiplicador de oferta o b) editar una plantilla descargada anteriormente. Guarde el archivo editado en su dispositivo o red.

   1. A) arrastre y suelte el archivo editado en el cuadro o b) haga clic dentro del cuadro para seleccionar el archivo desde el dispositivo o la red.

   1. Clic **[!UICONTROL Upload]**.

1. Clic **[!UICONTROL Save]**.

## Tipos de objetivo aptos para multiplicadores de oferta {#bid-multiplier-by-target}

no engañado aquí

## Número máximo de multiplicadores de oferta por tipo de destino {#bid-multiplier-limits-by-target}

no engañado aquí

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
