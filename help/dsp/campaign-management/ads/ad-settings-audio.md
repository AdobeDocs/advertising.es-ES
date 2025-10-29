---
title: Configuración de anuncios de audio
description: Consulte las descripciones de los ajustes de publicidad disponibles para anuncios de audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Configuración de anuncios de audio

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]**: URL de etiqueta VAST.

**[!UICONTROL Title]**: un nombre para el archivo, que se usa en la vista e informes de [!UICONTROL Ads].

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la clave **[!UICONTROL Enter]**. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio. El valor predeterminado es *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Use un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en la vista [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa del producto Holiday: 30sec Audio&quot;).

**[!UICONTROL Ad Duration]:** Longitud del archivo de audio. Se establece automáticamente como [!UICONTROL 15] o [!UICONTROL 30], según la unidad de anuncio seleccionada.

Este campo puede mostrarse o no, según los permisos de la cuenta.

**[!UICONTROL VAST Tag]:** (anuncios que solo usan etiquetas VAST) Dirección URL de un origen de anuncio de terceros. Asegúrese de que la etiqueta VAST incluya solo archivos multimedia de audio.

**[!UICONTROL Final VAST Tag]:** (anuncios que solo usan etiquetas VAST) La URL de la fuente de anuncios de terceros con las [macros de seguimiento de Advertising DSP](/help/dsp/campaign-management/macros.md) necesarias insertadas, si corresponde.

**[!UICONTROL Select Rate]:** (Usuarios solo con permiso) Tarifa negociada previamente que se factura a través de Adobe o una de las tarifas que ha negociado y se factura a través del proveedor. Para agregar una tasa, póngase en contacto con el equipo de cuenta de Adobe.

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
