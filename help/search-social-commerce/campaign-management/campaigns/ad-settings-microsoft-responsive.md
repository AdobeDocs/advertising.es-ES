---
title: '[!DNL Microsoft Advertising] configuración de publicidad adaptable'
description: Hacer referencia a la configuración de  [!DNL Microsoft Advertising] anuncios adaptables.
exl-id: 29404500-d929-4683-be71-150ea8ab805d
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/K4R8gmgxfaMP0JdZiz4RkZkfC6-0T2BsyxpcwK-X3bQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configuración de anuncio adaptable (audiencia)

El formato de anuncio interactivo está disponible para anuncios de audiencia basados en imágenes, en vídeo y en vídeo de TV conectados en [!DNL Microsoft Audience Network]. La red de anuncios organiza de forma dinámica anuncios interactivos mediante las combinaciones más eficaces de elementos publicitarios.

## [!UICONTROL Ad Settings] (para anuncios de vídeo) y [!UICONTROL Audience CTV Video Ad Details]

**[!UICONTROL Videos]:** Dirección URL de un anuncio de vídeo.

**[!UICONTROL Status]:** Estado del anuncio.

## [!UICONTROL Responsive Ad Details] (para anuncios de imágenes)

>[!NOTE]
>
>La red de anuncios crea automáticamente anuncios para campañas de audiencia vinculadas a un almacén del centro de comerciantes mediante la información de productos del almacén y la segmentación de usuarios a nivel de grupo de anuncios. No es necesario crear anuncios manualmente.

**[!UICONTROL Images]:** hasta 15 imágenes JPEG o PNG para el anuncio. Incluya al menos una imagen con una proporción de aspecto de 1,91:1. Ver las proporciones y dimensiones permitidas para [imágenes de anuncios de audiencia](https://help.ads.microsoft.com/#apex/ads/en/56912/0).

Para los anuncios de audiencia, [!DNL Microsoft Advertising] recorta automáticamente esta imagen para todas las relaciones de aspecto posibles.

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]:** El nombre comercial, con un máximo de 25 caracteres. Se puede utilizar en formatos de anuncios de solo llamada.

**[!UICONTROL Short Headlines]:** Al menos tres y hasta 15 titulares cortos con al menos una palabra y un máximo de 30 caracteres cada uno.

**[!UICONTROL Long Headlines]:** Al menos tres y hasta cinco titulares largos con un máximo de 90 caracteres cada uno.

**[!UICONTROL Ad Text]:** Al menos dos y hasta cuatro descripciones con al menos una palabra y un máximo de 90 caracteres cada una.

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Acerca de los anuncios](ad-about.md)
>* [Administrar anuncios](ad-manage.md)
>* [[!DNL Microsoft Advertising] configuración de anuncios dinámicos de búsqueda expandida](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] configuración de anuncios multimedia](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] configuración de anuncios de productos](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] configuración del anuncio de búsqueda adaptable](ad-settings-microsoft-rsa.md)
