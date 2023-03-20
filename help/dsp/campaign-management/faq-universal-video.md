---
title: Preguntas frecuentes sobre el vídeo universal
description: Obtenga más información sobre los anuncios universales en vídeo.
feature: DSP Placements, DSP Ads
source-git-commit: 58cbb5b85a1dc790aaf762ba55fd2badeef6fe68
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Preguntas frecuentes sobre el vídeo universal

## ¿Cómo se crean colocaciones y publicidades de vídeo universales?

Las ubicaciones de vídeo universales solo pueden contener anuncios de vídeo universales y los anuncios de vídeo universales solo se pueden adjuntar a las ubicaciones de vídeo universales.

Puede crearlos de forma similar a como crea otros tipos de ubicaciones y vídeos:

1. Dentro de la campaña deseada, [crear una ubicación de vídeo universal](/help/dsp/campaign-management/placements/placement-create.md), seleccionando [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Debe especificar al menos un entorno (escritorio, móvil, TV conectada) para el destino.

1. En la misma campaña que la colocación universal de vídeo, [crear una sola publicidad de vídeo universal](/help/dsp/campaign-management/ads/ad-create.md) o [crear varios anuncios de vídeo universal](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Si crea varias publicidades, asegúrese de especificar &quot;[!UICONTROL Universal Video]&quot; como el [!UICONTROL Ad Type]:

   * Para [!DNL Google] o [!DNL Flashtalking] anuncios: En el[!UICONTROL Review ad types]&quot; después de cargar el archivo, haga clic en el **[!UICONTROL Ad Type]** y seleccione **[!UICONTROL Universal Video]**.

   * Para otros tipos de etiquetas de publicidad: En el archivo de hoja de cálculo que cargue, especifique el campo Tipo de anuncio para cada anuncio como **[!UICONTROL Universal Video]**.

1. [Abra la configuración de publicidad](/help/dsp/campaign-management/ads/ad-edit.md) para cada anuncio nuevo y seleccione el formato de vídeo aplicable:

   * **[!UICONTROL VPAID]:** La visibilidad siempre se mide.
   * **[!UICONTROL VPAID & VAST (Default)]:** Incluye un inventario que no permite la medición de la visibilidad.
   * **[!UICONTROL VAST]** - Adecuado para el inventario de TV conectado.

   Consulte &quot;[Configuración de anuncios de vídeo universal](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; para obtener más información.

1. [Adjunte los nuevos anuncios universales de vídeo](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) a la ubicación de vídeo universal.

## ¿Por qué algunos objetivos y paquetes de optimización no están disponibles cuando se selecciona el entorno de TV conectado para una ubicación de vídeo universal?

Los objetivos que son incompatibles con las ubicaciones de TV conectadas estándar, como Costo por clic más bajo, no son compatibles con el entorno de TV conectado en las ubicaciones de vídeo universales. Del mismo modo, los paquetes con objetivos de optimización incompatibles tampoco están disponibles para la selección.

## ¿Cuándo debería **[!UICONTROL VAST]** ¿el formato de vídeo se utiliza para los anuncios de vídeo universales?

Uso **[!UICONTROL VAST]** en cualquiera de los siguientes escenarios:

* La ubicación se dirige al inventario de TV conectado.
* La ubicación se dirige al inventario de vídeo de Google Ad Manager, Appnexus, SpotX o Freewheel. Estos SSP no admiten el formato de vídeo VPAID y VAST.

## ¿Es posible adjuntar varios anuncios de vídeo universales a la misma ubicación de vídeo universal?

Sí.
