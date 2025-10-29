---
title: Configuración de anuncio de visualización
description: Consulte las descripciones de las configuraciones de anuncios disponibles para los anuncios en pantalla.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Configuración de anuncio de visualización

Los siguientes ajustes son para anuncios en pantalla estándar.

## [!UICONTROL Ad Options]

### Básico

**[!UICONTROL Ad Type]:** (solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar el anuncio. El valor predeterminado es *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Use un nombre que sea fácil de encontrar al adjuntar el anuncio a una ubicación, en la vista [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa del producto Holiday: 300x250 Gamer&quot;).

**\[Ad Source\]**: (Solo lectura) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (solo anuncios de terceros) Indica que el anuncio es un anuncio de banner expansible. La configuración de expansión relacionada determina qué inventario comprar, por lo que debe asegurarse de que refleje el comportamiento del anuncio.

**[!UICONTROL Expansion Method]:** (Solo anuncios de banner expandibles de terceros) Si el banner se expande en *[!UICONTROL Click]* o *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (solo anuncios de banners expandibles de terceros) Dirección en la que se expande el anuncio: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* o *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (solo anuncios de banner expandibles de terceros) El proveedor certificado para el que el anuncio está disponible: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* o *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (solo anuncios de terceros) Dirección URL del recurso creativo de terceros. Cualquier parámetro [timestamp] y [[timestamp]] se reemplaza con valores reales.

**[!UICONTROL Final Display Code]:** (solo anuncios de terceros) Dirección URL del recurso creativo de terceros, con las [macros de seguimiento de Advertising DSP](/help/dsp/campaign-management/macros.md) necesarias insertadas, si corresponde.

**[!UICONTROL Ad Size]:** La anchura y altura del anuncio. Debe ser un [tamaño estándar de anuncio en pantalla admitido](ad-specs.md). Puede introducir manualmente el tamaño del anuncio antes de cargar el anuncio o escribir un [!UICONTROL Display Code]. Si no introduce el tamaño del anuncio, las dimensiones del anuncio cargado o de la etiqueta de anuncio se introducen automáticamente como de solo lectura.

>[!IMPORTANT]
>
> El tamaño del anuncio declarado en los campos de anchura y altura coincide con las solicitudes de oferta entrantes. Puede experimentar problemas de envío si las dimensiones del anuncio no coinciden con el tamaño del anuncio declarado.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Enumerar las ubicaciones asociadas con un anuncio](ad-list-placements.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [Macros de DSP](/help/dsp/campaign-management/macros.md)
