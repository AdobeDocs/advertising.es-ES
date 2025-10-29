---
title: Configuración de anuncios de TV conectados
description: Consulte las descripciones de la configuración de anuncios disponibles para anuncios de TV conectados.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Configuración de anuncios de TV conectados

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]**: URL de etiqueta VAST.

**[!UICONTROL Title]**: un nombre para el archivo, que se usa en la vista Anuncios e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la clave **[!UICONTROL Enter]**. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Use un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en la vista [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos festivos: &quot;CTV de 30 segundos&quot;).

**[!UICONTROL Width | Ad Unit Width]:** El ancho de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height | Ad Unit Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** Coordenada X de la unidad de anuncio. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** Coordenada Y de la unidad de anuncio. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** El ancho de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Es el mismo que el campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Es el mismo que el campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Dónde incluir los controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se desea conservar las proporciones de anchura y altura del vídeo (*[!UICONTROL Yes]*) o si se desea ampliar el vídeo para rellenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que especificó como origen de anuncio.

**[!UICONTROL Final VAST Tag]:** (anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ingresó como fuente de publicidad con las [macros de seguimiento de Advertising DSP](/help/dsp/campaign-management/macros.md) necesarias insertadas, si corresponde.

**[!UICONTROL Clock Number]**: (solo se usa en el Reino Unido; disponible solo para usuarios con permiso) Identificador único utilizado para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumerar las ubicaciones asociadas con un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [Macros de DSP](/help/dsp/campaign-management/macros.md)
