---
title: '[!DNL Microsoft Advertising] configuración de palabras clave'
description: Haga referencia a la configuración de [!DNL Microsoft Advertising] Palabras clave.
exl-id: 248f45c7-8b8c-46fe-a65a-66c50c630044
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configuración de palabras clave

Puede crear palabras clave para las campañas que utilizan las redes de búsqueda y visualización.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave, incluidas las [!DNL Microsoft Advertising] coincide con la sintaxis y los marcadores de posición. La longitud máxima por palabra clave es de 100 caracteres.

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Puede crear palabras clave negativas desde el [!UICONTROL Keywords] > [!UICONTROL Negatives] vea y en el grupo de publicidad y en la configuración de la campaña.
>* Cambio de una [!DNL Microsoft Advertising] elimina la palabra clave existente y crea una nueva con un nuevo ID de palabra clave. Sin embargo, al cambiar el tipo de coincidencia no se elimina la palabra clave existente.

**[!UICONTROL Status]:** El estado de visualización de la palabra clave: *Activo* o *Pausado*. El valor predeterminado para las palabras clave nuevas es *Activo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Marcadores

**[!UICONTROL Param2]:** Cadena que se utiliza como valor de sustitución si la dirección URL base de la palabra clave o el título, la descripción o la dirección URL base del anuncio contienen [el `{Param2}` cadena de sustitución dinámica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longitud máxima es de 70 caracteres, pero tenga en cuenta la longitud máxima del elemento publicitario en el que lo utiliza (por ejemplo, el Título 1 y el Título 2 combinados pueden tener un máximo de 76 caracteres).

**[!UICONTROL Param3]:** Cadena que se utiliza como valor de sustitución si la dirección URL base de la palabra clave o el título, la descripción o la dirección URL base del anuncio contienen [el `{Param3}` cadena de sustitución dinámica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longitud máxima es de 70 caracteres, pero tenga en cuenta la longitud máxima del elemento publicitario en el que lo utiliza (por ejemplo, el Título 1 y el Título 2 combinados pueden tener un máximo de 76 caracteres).

## Opciones de URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Este campo puede incluir de forma opcional la variable `{Param2}` y `{Param3}` variables de sustitución dinámica.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
