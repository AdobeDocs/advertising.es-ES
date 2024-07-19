---
title: '[!DNL Microsoft Advertising] configuración de palabras clave'
description: Hacer referencia a la configuración de  [!DNL Microsoft Advertising] palabras clave.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configuración de palabras clave

Puede crear palabras clave para las campañas que utilizan las redes de búsqueda y visualización.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave, incluidos los [!DNL Microsoft Advertising] coinciden con la sintaxis y los marcadores de posición. La longitud máxima por palabra clave es de 100 caracteres.

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Puede crear palabras clave negativas desde la vista [!UICONTROL Keywords] > [!UICONTROL Negatives] y en la configuración de grupos de anuncios y campañas.
>* Al cambiar una palabra clave [!DNL Microsoft Advertising], se eliminará la palabra clave existente y se creará una nueva con un nuevo identificador de palabra clave. Sin embargo, al cambiar el tipo de coincidencia no se elimina la palabra clave existente.

**[!UICONTROL Status]:** El estado de visualización de la palabra clave: *Activo* o *En pausa*. El valor predeterminado para las palabras clave nuevas es *Activo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Marcadores

**[!UICONTROL Param2]:** Cadena que se usará como valor de sustitución si la dirección URL base de la palabra clave o el título, la descripción o la dirección URL base del anuncio contiene [la cadena de sustitución dinámica `{Param2}`](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longitud máxima es de 70 caracteres, pero tenga en cuenta la longitud máxima de los elementos de publicidad en los que la utiliza (por ejemplo, el Título 1 y el Título 2 combinados pueden tener un máximo de 76 caracteres).

**[!UICONTROL Param3]:** Cadena que se usará como valor de sustitución si la dirección URL base de la palabra clave o el título, la descripción o la dirección URL base del anuncio contiene [la cadena de sustitución dinámica `{Param3}`](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longitud máxima es de 70 caracteres, pero tenga en cuenta la longitud máxima de los elementos de publicidad en los que la utiliza (por ejemplo, el Título 1 y el Título 2 combinados pueden tener un máximo de 76 caracteres).

## Opciones de URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Este campo puede incluir opcionalmente las variables de sustitución dinámica `{Param2}` y `{Param3}`.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
