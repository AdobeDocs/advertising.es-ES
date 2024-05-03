---
title: Configuración nativa de anuncios en pantalla
description: Consulte las descripciones de la configuración de anuncios disponibles para los anuncios en pantalla nativos.
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Configuración nativa de anuncios en pantalla

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El tipo de anuncio se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre fácil de encontrar al adjuntar el anuncio a una ubicación, en el [!UICONTROL Ads] ver, y en informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como &quot;Vista previa del producto festivo: 15 segundos nativo&quot;).

**[!UICONTROL Native Creative]:** Una imagen de 1200 x 627 para maximizar la entrega en el inventario móvil. Clic **[!UICONTROL Browse]** y busque el archivo en el dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** Un título llamativo para atraer a los espectadores.

**[!UICONTROL Description]:** El cuerpo del anuncio. La longitud máxima es de 100 caracteres.

**[!UICONTROL Landing Page]:** Dirección URL en la que aterriza el visor cuando hace clic en el anuncio.

**[!UICONTROL Final Landing Page]:** El [!UICONTROL Landing Page] URL con el necesario [DSP Macros de seguimiento de Advertising](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Sponsored By (Advertiser Name)]:** El anunciante del anuncio.

**[!UICONTROL Call to Action]:** (Opcional) El paso que desea que los espectadores realicen una vez que vean este anuncio.

**[!UICONTROL Advertiser Logo]:** (Opcional) Un logotipo con una relación 1:1 que se incluirá en el anuncio para lograr un mayor reconocimiento de la marca. Clic **[!UICONTROL Browse]** y busque el archivo en el dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de evento existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual. **Sugerencia:** Para editar los píxeles de seguimiento de terceros para varios anuncios en una ubicación a la vez utilizando [!UICONTROL Ad Tools] ver, consulte &quot;[Adjuntar píxeles de seguimiento de terceros a anuncios en una ubicación](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Los siguientes ajustes se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se va a activar. Para este tipo de anuncio, la única opción es *[!UICONTROL Impression]*.

**[!UICONTROL Pixel Type]:** Si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La URL de la imagen de píxel, en el formato adecuado para el especificado [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, o *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumeración de las ubicaciones asociadas a un anuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [DSP macros](/help/dsp/campaign-management/macros.md)
