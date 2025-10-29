---
title: Configuración de publicidad móvil
description: Consulte las descripciones de las configuraciones de anuncios disponibles para anuncios móviles.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Configuración de publicidad móvil

## [!UICONTROL Insert Ad Tag]

*Solo formatos para nuevos anuncios de vídeo para móviles*

**[!UICONTROL URL]** o **[!UICONTROL Ad Tag]**: una etiqueta de anuncio o etiqueta de anuncio VAST de terceros que contiene recursos creativos y píxeles de seguimiento

**[!UICONTROL Ad Title]** o **[!UICONTROL Title]**: un nombre para el anuncio que se usa en la vista e informes de [!UICONTROL Ads].

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la clave **[!UICONTROL Enter]**. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: anuncios en pantalla móviles

**[!UICONTROL Ad Type]:** (solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en la vista Anuncios y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa del producto Holiday: 300x250 Gamer&quot;).

**\[Ad Source\]**: (Solo lectura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** Dirección URL del recurso creativo de terceros. Cualquier parámetro [timestamp] y [[timestamp]] se reemplaza con valores reales.

**[!UICONTROL Final Display Code]:** Dirección URL del recurso creativo de terceros, con las [macros de seguimiento de Advertising DSP](/help/dsp/campaign-management/macros.md) necesarias insertadas, si corresponde.

### [!UICONTROL Basic]: anuncios de vídeo

**[!UICONTROL Ad Type]:** (solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en la vista Anuncios y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos festivos: Previsualización de teléfono de 30 segundos).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** El ancho de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** Coordenada X de la unidad de anuncio. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** Coordenada Y de la unidad de anuncio. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** El ancho de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Es el mismo que el campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Es el mismo que el campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Dónde incluir los controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se desea conservar las proporciones de anchura y altura del vídeo (*[!UICONTROL Yes]*) o si se desea ampliar el vídeo para rellenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Algunos tipos de anuncios) El número de segundos para retrasar la aparición del botón de cierre.

**[!UICONTROL VAST Tag]:** (anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ingresó como recurso creativo.

**[!UICONTROL Final VAST Tag]:** (anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ingresó como recurso creativo con las [macros de seguimiento de Advertising DSP](/help/dsp/campaign-management/macros.md) necesarias insertadas, si corresponde.

**[!UICONTROL Wmode]:** (algunos tipos de anuncios) El modo de ventana: *[!UICONTROL window]*, *[!UICONTROL transparent]* o *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumerar las ubicaciones asociadas con un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [Macros de DSP](/help/dsp/campaign-management/macros.md)
