---
title: '[!DNL Yandex] configuración de palabras clave'
description: Hacer referencia a la configuración de las palabras clave [!DNL Yandex].
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
source-wordcount: '227'
ht-degree: 0%
---
# [!DNL Yandex] configuración de palabras clave

Las palabras clave [!DNL Yandex] se utilizan en las redes de búsqueda y visualización (contenido).

## [!UICONTROL Basic Settings]

*Solo palabras clave nuevas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign]:** La campaña.

**[!UICONTROL Ad Group]:** El grupo de anuncios.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las frases de palabras clave, incluida cualquier [[!DNL Yandex] sintaxis de tipo de coincidencia](https://yandex.com/support/direct/keywords/symbols-and-operators.html) para palabras clave. Cada palabra clave puede tener un máximo de siete palabras, excluidas las palabras de detención.

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Al cambiar una palabra clave [!DNL Yandex] o un tipo de coincidencia, se eliminará la palabra clave existente y se creará una nueva.
>* Cada grupo de anuncios [!DNL Yandex] puede incluir un máximo de 200 palabras clave.

**[!UICONTROL Status]:** Estado de visualización de la palabra clave: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. El valor predeterminado para las nuevas palabras clave es *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>Los caracteres especiales se codifican automáticamente en UTF-8. Por ejemplo, si el anuncio asociado tiene una dirección URL base de `http://www.example.com/{param1}` y el valor de nivel de palabra clave de `{param1}` es `shoes/flats.html`, el anuncio lleva a `http://www.example.com/shoes%2Fflats.html`.

**[!UICONTROL Param1]:** Cadena que se usará como valor de sustitución si la dirección URL base contiene la cadena de sustitución dinámica `{param1}` para anuncios y vínculos de sitios cuando la palabra clave se usa para mostrar el anuncio. La longitud máxima es de 255 bytes.

**[!UICONTROL Param2]:** Cadena que se usará como valor de sustitución si la dirección URL base contiene la cadena de sustitución dinámica `{param2}` para anuncios y vínculos de sitios cuando la palabra clave se usa para mostrar el anuncio. La longitud máxima es de 255 bytes.

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](keyword-manage.md)
