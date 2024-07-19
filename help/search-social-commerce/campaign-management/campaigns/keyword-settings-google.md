---
title: '[!DNL Google Ads] configuración de palabras clave'
description: Hacer referencia a la configuración de  [!DNL Google Ads] palabras clave.
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# [!DNL Google Ads] configuración de palabras clave

Puede crear palabras clave para las campañas que utilizan las redes de búsqueda y visualización.

Consulte la ayuda de Google Ads para [límites de palabras clave por cuenta](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave, incluida cualquier [!DNL Google Ads], coinciden con la sintaxis de palabras clave y marcadores de posición. Las cuentas de [!DNL Google Ads] requieren palabras clave con los atributos siguientes:

* La longitud máxima por palabra clave es de 80 caracteres y no más de 10 palabras.
* La palabra clave sólo puede incluir letras, dígitos y los siguientes caracteres especiales: espacio `# $ & _ - " [] ' + . / :`

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Puede crear palabras clave negativas desde la vista [!UICONTROL Keywords] > [!UICONTROL Negatives] y en la configuración de grupos de anuncios y campañas.
>* Al cambiar una palabra clave [!DNL Google Ads] o un tipo de coincidencia, se eliminará la palabra clave existente y se creará una nueva.

**[!UICONTROL Status]:** El estado de visualización de la palabra clave: *Activo* o *En pausa*. El valor predeterminado para las palabras clave nuevas es *Activo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Marcadores

**[!UICONTROL Param1]:** La cadena que se va a usar como valor de sustitución si la dirección URL base o la plantilla de seguimiento contiene [la cadena de sustitución dinámica `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** La cadena que se va a usar como valor de sustitución si la dirección URL base o la plantilla de seguimiento contiene [la cadena de sustitución dinámica `{param2}`](https://support.google.com/google-ads/answer/6305348).

## Opciones de URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
