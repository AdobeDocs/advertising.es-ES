---
title: Configuración de anuncio de vídeo universal
description: Consulte las descripciones de los ajustes de publicidad disponibles para los anuncios de vídeo universales.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Configuración de anuncio de vídeo universal

>[!NOTE]
>
>Los anuncios de vídeo universales solo se pueden adjuntar a ubicaciones de vídeo universales.

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]:** URL de la etiqueta VAST.

**[!UICONTROL Title]:** Un título para el archivo, que se encuentra en la vista e informes de [!UICONTROL Ads].

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la clave **[!UICONTROL Enter]**. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Use un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en la vista [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos festivos: vídeo universal de 30 segundos).

**[!UICONTROL Show Controls]:** Dónde incluir los controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se desea mantener las proporciones de anchura y altura del vídeo (*[!UICONTROL Yes]*) o si se desea expandir el vídeo para rellenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que especificó como origen de anuncio.

**[!UICONTROL Final VAST Tag]:** (anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ingresó como fuente de publicidad con las [macros de seguimiento de Advertising DSP](/help/dsp/campaign-management/macros.md) necesarias insertadas, si corresponde.

**[!UICONTROL Wmode]:** Modo de ventana: *[!UICONTROL window]*, *[!UICONTROL transparent]* o *[!UICONTROL opaque]*. Si esta configuración no es aplicable, déjela en blanco.

**[!UICONTROL Video Format]:** El formato del reproductor del anuncio para el inventario potencial: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* o *[!UICONTROL VAST]*. La visibilidad siempre se mide para [!UICONTROL VPAID], pero [!UICONTROL VPAID & VAST] incluye el inventario que no permite la medición de la visibilidad. Tenga en cuenta esta distinción si las métricas de visibilidad son importantes para la campaña.

Utilice [!UICONTROL VAST], que no permite la medición de la visibilidad, cuando se dirija a un televisor conectado o a un inventario que solo requiera un formato VAST (normalmente de fuentes de suministro como Google Ad Manager, Appnexus, SpotX y Freewheel). Utilice también esta opción para los inventarios que anteriormente eran compatibles con las ubicaciones/anuncios previos a la emisión estándar (VAST) o los anuncios previos a la emisión estándar de teléfono + tableta (VAST).

**[!UICONTROL Clock Number]**: (solo se usa en el Reino Unido; disponible solo para usuarios con permiso) Identificador único utilizado para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Preguntas más frecuentes sobre el vídeo universal](/help/dsp/campaign-management/faq-universal-video.md)
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumerar las ubicaciones asociadas con un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [Macros de DSP](/help/dsp/campaign-management/macros.md)
