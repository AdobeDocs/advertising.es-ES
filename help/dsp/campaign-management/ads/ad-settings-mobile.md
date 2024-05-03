---
title: Configuración de publicidad móvil
description: Consulte las descripciones de las configuraciones de anuncios disponibles para anuncios móviles.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Configuración de publicidad móvil

## [!UICONTROL Insert Ad Tag]

*Nuevos formatos de anuncios de vídeo móviles*

**[!UICONTROL URL]** o **[!UICONTROL Ad Tag]**: una etiqueta de anuncio VAST de terceros o una etiqueta de anuncio que contiene recursos creativos y píxeles de seguimiento

**[!UICONTROL Ad Title]** o **[!UICONTROL Title]**: Un nombre para el anuncio que se utiliza en el [!UICONTROL Ads] Ver e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse el botón **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Anuncios en pantalla móviles

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en la vista Anuncios y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa del producto Holiday: 300x250 Gamer&quot;).

**\[Origen del anuncio\]**: (solo lectura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** La URL del recurso creativo de terceros. Cualquiera [timestamp] y [[timestamp]] parámetros se reemplazarán con valores reales.

**[!UICONTROL Final Display Code]:** La URL del recurso creativo de terceros, con los necesarios [DSP Macros de seguimiento de Advertising](/help/dsp/campaign-management/macros.md) insertado, si procede.

### [!UICONTROL Basic]: anuncios de vídeo

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en la vista Anuncios y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos festivos: Previsualización de teléfono de 30 segundos).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Anchura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** La coordenada X de la unidad publicitaria. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** La coordenada Y de la unidad publicitaria. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** Anchura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Esto es lo mismo que el **[!UICONTROL Width]** field.

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse según el tipo de unidad de publicidad seleccionada.

Esto es lo mismo que el **[!UICONTROL Height]** field.

**[!UICONTROL Show Controls]:** Dónde se incluyen los controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, o *[!UICONTROL None]* (el valor predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se conservan las proporciones de anchura y altura del vídeo (*[!UICONTROL Yes]*) o para ampliar el vídeo y rellenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Algunos tipos de anuncio) El número de segundos para retrasar la aparición del botón de cierre.

**[!UICONTROL VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ha introducido como recurso creativo.

**[!UICONTROL Final VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ha introducido como recurso creativo con el necesario [DSP Macros de seguimiento de Advertising](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Wmode]:** (Algunos tipos de anuncios) El modo de ventana: *[!UICONTROL window]*, *[!UICONTROL transparent]*, o *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de evento existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual. **Sugerencia:** Para editar los píxeles de seguimiento de terceros para varios anuncios en una ubicación a la vez utilizando [!UICONTROL Ad Tools] ver, consulte &quot;[Adjuntar píxeles de seguimiento de terceros a anuncios en una ubicación](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Los siguientes ajustes se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se va a activar. Para este tipo de anuncio, utilice píxeles que se activen en *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La URL de la imagen de píxel, en el formato adecuado para el especificado [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, o *[!UICONTROL IAS]*.

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumeración de las ubicaciones asociadas a un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [DSP macros](/help/dsp/campaign-management/macros.md)
