---
title: Configuración de anuncio de vídeo universal
description: Consulte las descripciones de los ajustes de publicidad disponibles para los anuncios de vídeo universales.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: d4af504a84d8fb356b2aca6d324e20fc0fb8fbbe
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Configuración de anuncio de vídeo universal

>[!NOTE]
>
>Los anuncios de vídeo universales solo se pueden adjuntar a ubicaciones de vídeo universales.

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
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en el [!UICONTROL Ads] ver, y en informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos festivos: vídeo universal de 30 segundos).

**[!UICONTROL Show Controls]:** Dónde se incluyen los controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, o *[!UICONTROL None]* (el valor predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se conservan las proporciones de anchura y altura (*[!UICONTROL Yes]*) o para ampliar el vídeo y rellenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad.

**[!UICONTROL Final VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad con el [DSP Macros de seguimiento de Advertising](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Wmode]:** El modo de ventana: *[!UICONTROL window]*, *[!UICONTROL transparent]*, o *[!UICONTROL opaque]*. Si esta configuración no es aplicable, déjela en blanco.

**[!UICONTROL Video Format]:** El formato del reproductor de anuncios para el inventario potencial: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]*, o *[!UICONTROL VAST]*. La visibilidad siempre se mide para [!UICONTROL VPAID], pero [!UICONTROL VPAID & VAST] incluye el inventario que no permite la medición de la visibilidad. Tenga en cuenta esta distinción si las métricas de visibilidad son importantes para la campaña.

Uso [!UICONTROL VAST], que no permite la medición de la visibilidad, cuando se dirige a un televisor conectado o a un inventario que estrictamente requiere un formato VAST (generalmente de fuentes de suministro como Google Ad Manager, Appnexus, SpotX y Freewheel). Utilice también esta opción para los inventarios que anteriormente eran compatibles con las ubicaciones/anuncios previos a la emisión estándar (VAST) o los anuncios previos a la emisión estándar de teléfono + tableta (VAST).

**[!UICONTROL Clock Number]**: (solo se utiliza en el Reino Unido; disponible solo para usuarios con permiso) Identificador único utilizado para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

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
>* [Preguntas frecuentes sobre Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumeración de las ubicaciones asociadas a un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [DSP macros](/help/dsp/campaign-management/macros.md)

