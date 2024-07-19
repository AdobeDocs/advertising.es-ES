---
title: '[!DNL Yandex] configuración de palabras clave'
description: Hacer referencia a la configuración de  [!DNL Yandex] palabras clave.
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# [!DNL Yandex] configuración de palabras clave

Las palabras clave Yandex se utilizan para las redes de búsqueda y visualización (contenido).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las frases de palabras clave, incluida cualquier [sintaxis de tipo de coincidencia Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) para palabras clave. Cada palabra clave puede tener un máximo de siete palabras, excluidas las palabras de detención.

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Al cambiar una palabra clave [!DNL Yandex] o un tipo de coincidencia, se eliminará la palabra clave existente y se creará una nueva.
>* Cada grupo de anuncios de Yandex puede incluir un máximo de 200 palabras clave.

**[!UICONTROL Status]:** El estado de visualización de la palabra clave: *Activo* o *En pausa*. El valor predeterminado para las palabras clave nuevas es *Activo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Marcadores

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** El valor de las variables de sustitución `{param1}` y `{param2}`, que se sustituyen por cualquier instancia de {param1} y {param2} en la dirección URL base para anuncios y vínculos de sitios cuando se utiliza la palabra clave para mostrar el anuncio. La longitud máxima es de 255 bytes.

Los caracteres especiales se codifican automáticamente en UTF-8. Por ejemplo, si el anuncio asociado tiene una dirección URL base de &quot;http://www.example.com/{param1}&quot; y el valor de nivel de palabra clave de {param1} es &quot;shoes/flats.html&quot;, el anuncio lleva a http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
