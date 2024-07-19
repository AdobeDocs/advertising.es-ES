---
title: Preguntas frecuentes sobre Universal Video
description: Más información sobre los anuncios de vídeo universales.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Preguntas frecuentes sobre Universal Video

[Los anuncios de vídeo universales](/help/dsp/campaign-management/ads/ad-about.md#ad-types) le permiten segmentar el inventario de vídeos desde entornos de escritorio, móviles y de TV conectada para el inventario VPAID y VAST con una sola ubicación de vídeo.

## ¿Cómo se crean ubicaciones de vídeo y anuncios universales?

Las ubicaciones de vídeo universales solo pueden contener anuncios de vídeo universales, y los anuncios de vídeo universales solo se pueden adjuntar a ubicaciones de vídeo universales.

Cree ubicaciones de vídeo universales y agregue anuncios de forma similar a como crea otros tipos de ubicaciones y vídeos:

1. Dentro de la campaña deseada, [cree una ubicación de vídeo universal](/help/dsp/campaign-management/placements/placement-create.md), seleccionando [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Debe especificar al menos un entorno (escritorio, móvil, TV conectada) para el destino.

1. En la misma campaña que la ubicación de vídeo universal, [crea un solo anuncio de vídeo universal](/help/dsp/campaign-management/ads/ad-create.md) o [crea varios anuncios de vídeo universales](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Si crea varios anuncios, asegúrese de especificar &quot;[!UICONTROL Universal Video]&quot; como [!UICONTROL Ad Type]:

   * Para anuncios de [!DNL Google] o [!DNL Flashtalking]: en el paso &quot;[!UICONTROL Review ad types]&quot; después de cargar el archivo, haga clic en el campo **[!UICONTROL Ad Type]** y seleccione **[!UICONTROL Universal Video]**.

   * Para otros tipos de etiquetas de anuncio: en el archivo de hoja de cálculo que cargue, especifique el campo Tipo de anuncio para cada anuncio como **[!UICONTROL Universal Video]**.

1. [Abra la configuración del anuncio](/help/dsp/campaign-management/ads/ad-edit.md) para cada anuncio nuevo y seleccione el formato de vídeo aplicable:

   * **[!UICONTROL VPAID]:** La visibilidad siempre se mide.
   * **[!UICONTROL VPAID & VAST (Default)]:** Incluye inventario que no permite la medición de la visibilidad.
   * **[!UICONTROL VAST]** - Adecuado para el inventario de TV conectado.

   Consulte &quot;[Configuración de anuncios de vídeo universales](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; para obtener más información.

1. [Adjunte los nuevos anuncios universales de vídeo](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) a la ubicación universal de vídeo.

## ¿Por qué algunos objetivos y paquetes de optimización no están disponibles cuando el entorno de TV conectado está seleccionado para una ubicación de vídeo universal?

Los objetivos que son incompatibles con las ubicaciones de TV conectadas estándar, como Coste por clic más bajo, no son compatibles con el entorno de TV conectado en ubicaciones de vídeo universales. Del mismo modo, los paquetes con objetivos de optimización incompatibles tampoco están disponibles para su selección.

## ¿Cuándo se debe usar el formato de vídeo **[!UICONTROL VAST]** para los anuncios de vídeo universales?

Utilice **[!UICONTROL VAST]** en cualquiera de los siguientes casos:

* La ubicación se dirige al inventario de TV conectado.
* La ubicación se dirige al inventario de vídeos de Google Ad Manager, Appnexus, SpotX o Freewheel. Estos SSP no admiten el formato de vídeo VPAID y VAST.

## ¿Es posible adjuntar varios anuncios de vídeo universales a la misma ubicación de vídeo universal?

Sí.
