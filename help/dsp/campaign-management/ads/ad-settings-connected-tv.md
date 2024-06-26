---
title: Configuración de anuncios de TV conectados
description: Consulte las descripciones de la configuración de anuncios disponibles para anuncios de TV conectados.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Configuración de anuncios de TV conectados

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]**: la URL de etiqueta VAST.

**[!UICONTROL Title]**: un nombre para el archivo, que se utiliza en la vista Anuncios e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse el botón **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en el [!UICONTROL Ads] ver, y en informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos festivos: &quot;CTV de 30 segundos&quot;).

**[!UICONTROL Width | Ad Unit Width]:** Anchura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height | Ad Unit Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** La coordenada X de la unidad publicitaria. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** La coordenada Y de la unidad publicitaria. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** Anchura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Esto es lo mismo que el **[!UICONTROL Width]** field.

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Esto es lo mismo que el **[!UICONTROL Height]** field.

**[!UICONTROL Show Controls]:** Dónde se incluyen los controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, o *[!UICONTROL None]* (el valor predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se conservan las proporciones de anchura y altura del vídeo (*[!UICONTROL Yes]*) o para ampliar el vídeo y rellenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad.

**[!UICONTROL Final VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad con el [DSP Macros de seguimiento de Advertising](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Clock Number]**: (solo se utiliza en el Reino Unido; disponible solo para usuarios con permiso) Identificador único utilizado para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de evento existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual. **Sugerencia:** Para editar los píxeles de seguimiento de terceros para varios anuncios en una ubicación a la vez utilizando [!UICONTROL Ad Tools] ver, consulte &quot;[Adjuntar píxeles de seguimiento de terceros a anuncios en una ubicación](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Los siguientes ajustes se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se va a activar. Para este tipo de anuncio, utilice píxeles que se activen en *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La URL de la imagen de píxel, en el formato adecuado para el Tipo de píxel especificado.

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, o *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumeración de las ubicaciones asociadas a un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [DSP macros](/help/dsp/campaign-management/macros.md)
