---
title: Administrar multiplicadores de oferta para ubicaciones
description: Obtenga información sobre cómo crear y editar multiplicadores de oferta para objetivos de ubicación especificados.
feature: DSP Placements
source-git-commit: 8d1cb46c8756c7312c6bd23e7a30118a8835ffd6
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Administrar multiplicadores de oferta para ubicaciones


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

Puede cambiar los multiplicadores de oferta para los destinos de colocación existentes mediante esta función.

Para cambiar los destinos seleccionados para las ubicaciones, consulte[Editar una ubicación](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Administrar los multiplicadores de oferta para una o más ubicaciones

Para todas las ubicaciones seleccionadas, puede editar valores manualmente o cargar una hoja de cálculo con valores.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Seleccione la casilla de verificación situada junto a cada ubicación cuyos multiplicadores de oferta desee administrar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Ajuste manualmente los multiplicadores de oferta para los objetivos aptos o cargando un archivo CSV con valores de objetivo:

   * Para ajustar manualmente los valores del multiplicador de oferta, vaya a cada pestaña específica de destinatario ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], y[!UICONTROL Brand Safety]) y edite los valores existentes para los destinos de colocación.

   Se realizarán los mismos cambios en todas las ubicaciones seleccionadas.

   * Para cargar un archivo CSV con valores de multiplicador de oferta que sobrescriban los valores existentes:

     >[!NOTE]
     >
     >Si deja un campo vacío, se eliminan todos los valores de ese tipo de destino.<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there will be only one data row applicable for all. -->

      1. Clic **[!UICONTROL CSV Edit]** en la parte superior derecha.

      1. Haga clic en **[!UICONTROL Download Template]** y editar los valores del multiplicador de oferta o b) editar una plantilla descargada anteriormente. Guarde el archivo editado en su dispositivo o red.

      1. A) arrastre y suelte el archivo editado en el cuadro o b) haga clic dentro del cuadro para seleccionar el archivo desde el dispositivo o la red.

   1. Clic **[!UICONTROL Upload]**.

   De forma predeterminada, el multiplicador de oferta para un objetivo es 1,00, lo que significa que la oferta no se ajusta para ese objetivo. Los valores pueden variar de 0,10 a 10,00. Por ejemplo, un modificador de oferta de 0,5 reduce una oferta de 6 USD a 3 USD (0,5 x 6). Puede establecer multiplicadores de oferta (con valores distintos de 1,00) para una [número limitado de objetivos](#bid-multiplier-limits-by-target).

   Cuando una subasta cumple los requisitos para varios modificadores de oferta, se multiplican todos los modificadores de oferta aplicables.

   Los modificadores de oferta nunca aumentan la oferta por encima de la oferta máxima.

1. Clic **[!UICONTROL Save]**.

-->

## Cargar una hoja de cálculo para administrar los multiplicadores de oferta para una sola ubicación<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

Los cambios en el archivo cargado sobrescriben los valores del multiplicador de oferta existentes.<!-- what if you delete a row? -->

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Junto al nombre de la ubicación, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. Haga clic en **[!UICONTROL Download Template]** y editar los valores del multiplicador de oferta o b) editar una plantilla descargada anteriormente. Guarde el archivo editado en su dispositivo o red.

   De forma predeterminada, el multiplicador de oferta para un objetivo es 1,00, lo que significa que la oferta no se ajusta para ese objetivo. Los valores pueden variar de 0,10 a 10,00. Por ejemplo, un modificador de oferta de 0,5 reduce una oferta de 6 USD a 3 USD (0,5 x 6). Puede establecer multiplicadores de oferta (con valores distintos de 1,00) para una [número limitado de objetivos](#bid-multiplier-limits-by-target).

   Cuando una subasta cumple los requisitos para varios modificadores de oferta, se multiplican todos los modificadores de oferta aplicables.

   Los modificadores de oferta nunca aumentan la oferta por encima de la oferta máxima.

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
>* [Edit a Placement](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
