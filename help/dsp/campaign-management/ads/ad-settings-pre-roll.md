---
title: Configuración de anuncio previo a la emisión
description: Consulte las descripciones de la configuración de anuncios disponibles para los anuncios previos a la emisión.
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Configuración de anuncio previo a la emisión

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]:** La URL de la etiqueta VAST.

**[!UICONTROL Title]:** Un título para el archivo, que se encuentra en [!UICONTROL Ads] Ver e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse el botón **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en el [!UICONTROL Ads] ver, y en informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos festivos: &quot;Predesplazamiento de 30 segundos&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Solo anuncios previos a la emisión estándar y omitibles) La anchura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Solo anuncios previos a la emisión estándar y omitibles) Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** La coordenada X de la unidad publicitaria. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** La coordenada Y de la unidad publicitaria. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** Anchura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Este campo es el mismo que el **[!UICONTROL Width]** field.

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Esto es lo mismo que el **[!UICONTROL Height]** field.

**[!UICONTROL Show Controls]:** Dónde se incluyen los controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, o *[!UICONTROL None]* (el valor predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se conservan las proporciones de anchura y altura (*[!UICONTROL Yes]*) o para ampliar el vídeo y rellenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad.

**[!UICONTROL Final VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad con el [DSP Macros de seguimiento de Advertising](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Wmode]:** (Solo anuncio previo a la emisión interactivo) El modo de ventana: *[!UICONTROL window]*, *[!UICONTROL transparent]*, o *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Solo anuncio previo a la emisión interactivo) El formato del reproductor de anuncios para el inventario potencial: *[!UICONTROL VPAID]* o *[!UICONTROL VPAID & VAST]*. La visibilidad siempre se mide para VPAID, pero VPAID y VAST incluyen inventario que no permite la medición de la visibilidad. Tenga en cuenta esta distinción si las métricas de visibilidad son importantes para la campaña.

**[!UICONTROL Clock Number]**: (solo anuncio previo a la emisión interactivo; solo se usa en el Reino Unido; disponible solo para usuarios con permiso) Un identificador único para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de evento existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual.

Los siguientes ajustes se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se va a activar. Para este tipo de anuncio, utilice píxeles que se activen en *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La URL de la imagen de píxel, en el formato adecuado para el especificado [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, o *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumeración de las ubicaciones asociadas a un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [DSP macros](/help/dsp/campaign-management/macros.md)

