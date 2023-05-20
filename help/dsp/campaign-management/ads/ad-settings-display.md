---
title: Configuración de anuncio de visualización
description: Consulte las descripciones de las configuraciones de anuncios disponibles para los anuncios en pantalla.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# Configuración de anuncio de visualización

Los siguientes ajustes son para anuncios en pantalla estándar.

## [!UICONTROL Ad Options]

### Básico

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio. El valor predeterminado es *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en el [!UICONTROL Ads] ver, y en informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa del producto Holiday: 300x250 Gamer&quot;).

**\[Origen del anuncio\]**: (solo lectura) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Solo anuncios de terceros) Indica que el anuncio es un anuncio de banner ampliable. La configuración de expansión relacionada determina qué inventario comprar, por lo que debe asegurarse de que refleje el comportamiento del anuncio.

**[!UICONTROL Expansion Method]:** (Solo anuncios de banners ampliables de terceros) Si el banner se amplía *[!UICONTROL Click]* o *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Solo anuncios de banner expandibles de terceros) La dirección en la que se expande el anuncio: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*, o *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Solo anuncios de banners ampliables de terceros) El proveedor certificado para el que está disponible el anuncio: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*, o *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Solo anuncios de terceros) La URL del recurso creativo de terceros. Cualquiera [timestamp] y [[timestamp]] parámetros se reemplazarán con valores reales.

**[!UICONTROL Final Display Code]:** (Solo anuncios de terceros) La URL del recurso creativo de terceros, con los necesarios [DSP Macros de seguimiento de Advertising](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Ad Size]:** La anchura y altura del anuncio. Debe ser un [tamaño de anuncio de visualización estándar admitido](ad-specs.md). Puede introducir manualmente el tamaño del anuncio antes de cargar el anuncio o introducir un [!UICONTROL Display Code]. Si no introduce el tamaño del anuncio, las dimensiones del anuncio cargado o de la etiqueta de anuncio se introducen automáticamente como de solo lectura. Tenga en cuenta que el anuncio en pantalla no se guardará si las dimensiones no se encuentran dentro de la visualización estándar como tamaños (por ejemplo, 301 x 250 en lugar de 300 x 250).

>[!IMPORTANT]
>
> El tamaño del anuncio declarado en los campos de anchura y altura coincidirá con las solicitudes de oferta entrantes. Puede experimentar problemas de envío si las dimensiones del anuncio no coinciden con el tamaño del anuncio declarado.

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
>* [Enumeración de las ubicaciones asociadas a un anuncio](ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [DSP macros](/help/dsp/campaign-management/macros.md)

