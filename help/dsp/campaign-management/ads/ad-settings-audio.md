---
title: Configuración de anuncios de audio
description: Consulte las descripciones de los ajustes de publicidad disponibles para anuncios de audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Configuración de anuncios de audio

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]**: la URL de etiqueta VAST.

**[!UICONTROL Title]**: Un nombre para el archivo, que se utilizará en la variable [!UICONTROL Ads] Ver e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse el botón **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio. El valor predeterminado es *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en el [!UICONTROL Ads] ver, y en informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa del producto Holiday: 30sec Audio&quot;).

**[!UICONTROL Ad Duration]:** La longitud del archivo de audio. Se establece automáticamente como lo siguiente [!UICONTROL 15] o [!UICONTROL 30], en función de la unidad de publicidad seleccionada.

Este campo puede mostrarse o no, según los permisos de la cuenta.

**[!UICONTROL VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST) Dirección URL de una fuente de anuncios de terceros. Asegúrese de que la etiqueta VAST incluya solo archivos multimedia de audio.

**[!UICONTROL Final VAST Tag]:** (Anuncios que solo utilizan etiquetas VAST) La URL de la fuente de publicidad de terceros con los necesarios [DSP Macros de seguimiento de Advertising](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Select Rate]:** (Solo usuarios con permiso) Una tarifa negociada previamente que se factura a través del Adobe o una de las tarifas que ha negociado y se facturará a través del proveedor. Para agregar una tarifa, póngase en contacto con el equipo de cuenta de Adobe.

### Píxel

Todos los píxeles de seguimiento de evento existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual.

Los siguientes ajustes se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se va a activar. Para este tipo de anuncio, utilice píxeles que se activen en *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La URL de la imagen de píxel, en el formato adecuado para el Tipo de píxel especificado.

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles:*[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, o *[!UICONTROL IAS]*..

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumeración de las ubicaciones asociadas a un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [DSP macros](/help/dsp/campaign-management/macros.md)
