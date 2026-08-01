---
title: '[!DNL Yandex] configuración de anuncios de texto'
description: Hacer referencia a la configuración de  [!DNL Yandex] anuncios de texto.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 0%

---

# [!DNL Yandex] configuración de anuncios de texto

<!-- DON'T HAVE ANY CAMPAIGNS TO TEST WITH -->

## [!UICONTROL Basic Settings]

*Solo anuncios nuevos*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign]:** La campaña.

**[!UICONTROL Ad Group]:** El grupo de anuncios.

## [!UICONTROL Text Ad Settings]

**[!UICONTROL Ad Title]:** El titular del titular (anuncio). La longitud máxima es de 33 caracteres y una sola palabra no puede incluir más de 23 caracteres.

>[!NOTE]
>
>Al cambiar la copia de un anuncio de [!DNL Yandex], se eliminará el anuncio existente y se creará un anuncio nuevo con las mismas propiedades.

**[!UICONTROL Description Line 1]:** El cuerpo del titular (anuncio). La longitud máxima es de 75 caracteres y una sola palabra no puede tener más de 22 caracteres.

>[!NOTE]
>
>Al cambiar la copia de un anuncio de [!DNL Yandex], se eliminará el anuncio existente y se creará un anuncio nuevo con las mismas propiedades.

**[!UICONTROL Status]:** Estado del anuncio: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

>[!NOTE]
>
>La dirección URL también puede incluir las variables de sustitución [`{param1}` y `{param2}`](https://yandex.com/support/direct/statistics/url-tags.html). Cuando se usan, las variables se sustituyen por los valores `{param1}` y `{param2}` definidos para la palabra clave que se usa para mostrar el anuncio.

>[!MORELIKETHIS]
>
>* [Administrar anuncios](/help/search-social-commerce/new-ui/manage/ads/ad-manage.md)
