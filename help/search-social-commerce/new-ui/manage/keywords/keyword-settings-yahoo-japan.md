---
title: '[!DNL LY Ads] configuración de palabras clave'
description: Hacer referencia a la configuración de las palabras clave [!DNL LY Ads].
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%
---
# [!DNL LY Ads] configuración de palabras clave

## [!UICONTROL Basic Settings]

*Solo palabras clave nuevas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign]:** La campaña.

**[!UICONTROL Ad Group]:** El grupo de anuncios.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave. La longitud máxima es de 80 caracteres, incluida cualquier [[!DNL LY Ads] sintaxis de tipo de coincidencia](https://ads-help.yahoo-net.jp/s/article/H000044997) para las palabras clave.

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Puede crear palabras clave negativas en la pestaña [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives], así como en el grupo de anuncios y en la configuración de la campaña.
>* [!DNL LY Ads] palabras clave y tipos de coincidencia son mutables, lo que significa que puede editarlos sin eliminar la palabra clave existente.

**[!UICONTROL Status]:** Estado de visualización de la palabra clave: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. El valor predeterminado para las nuevas palabras clave es *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** La cadena que se usará como valor de sustitución si la dirección URL base o la plantilla de seguimiento contiene `{param1}` [parámetro personalizado](https://ads-help.yahoo-net.jp/s/article/H000044803?language=en_US).

**[!UICONTROL Param2]:** La cadena que se usará como valor de sustitución si la dirección URL base o la plantilla de seguimiento contiene `{param2}` [parámetro personalizado](https://ads-help.yahoo-net.jp/s/article/H000044803?language=en_US).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/tracking-template-yahoo-japan.md}}

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](keyword-manage.md)
