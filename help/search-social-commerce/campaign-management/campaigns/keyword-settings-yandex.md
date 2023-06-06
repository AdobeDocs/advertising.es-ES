---
title: "[!DNL Yandex] configuración de palabras clave"
description: Haga referencia a la configuración de [!DNL Yandex] Palabras clave.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!DNL Yandex] configuración de palabras clave

Las palabras clave Yandex se utilizan para las redes de búsqueda y visualización (contenido).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las frases de palabras clave, incluidas las [Sintaxis del tipo de coincidencia Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) para palabras clave. Cada palabra clave puede tener un máximo de siete palabras, excluidas las palabras de detención.

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Cambio de una [!DNL Yandex] keyword o match type elimina la palabra clave existente y crea una nueva.
>* Cada grupo de anuncios de Yandex puede incluir un máximo de 200 palabras clave.


**[!UICONTROL Status]:** El estado de visualización de la palabra clave: *Activo* o *Pausado*. El valor predeterminado para las palabras clave nuevas es *Activo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Marcadores

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** El valor del `{param1}` y `{param2}` variables de sustitución, que sustituyen cualquier instancia de {param1} y {param2} en la dirección URL base para anuncios y vínculos de sitios cuando se utiliza la palabra clave para mostrar el anuncio. La longitud máxima es de 255 bytes.

Los caracteres especiales se codifican automáticamente en UTF-8. Por ejemplo, si el anuncio asociado tiene una dirección URL base de &quot;http://www.example.com/{param1}&quot; y el valor de nivel de palabra clave de {param1} es &quot;shoes/flats.html&quot;, el anuncio dirige a http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

