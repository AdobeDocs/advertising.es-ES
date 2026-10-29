---
title: '[!DNL Google Ads] configuración de palabras clave'
description: Hacer referencia a la configuración de las palabras clave [!DNL Google Ads].
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%
---
# [!DNL Google Ads] configuración de palabras clave

Puede crear palabras clave para las campañas que utilizan las redes de búsqueda y visualización.

Consulte la ayuda de [!DNL Google Ads] para [límites de palabras clave por cuenta](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Basic Settings]

*Solo palabras clave nuevas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign]:** La campaña.

**[!UICONTROL Ad Group]:** El grupo de anuncios.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave, incluida cualquier [!DNL Google Ads], coinciden con la sintaxis de palabras clave y marcadores de posición. Las cuentas de [!DNL Google Ads] requieren palabras clave con los atributos siguientes:

* La longitud máxima por palabra clave es de 80 caracteres y no más de 10 palabras.

* La palabra clave sólo puede incluir letras, dígitos y los siguientes caracteres especiales: espacio `# $ & _ - " [] ' + . / :`

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Puede crear palabras clave negativas en la pestaña [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives], así como en el grupo de anuncios y en la configuración de la campaña.
>* Al cambiar una palabra clave [!DNL Google Ads] o un tipo de coincidencia, se eliminará la palabra clave existente y se creará una nueva.

**[!UICONTROL Status]:** Estado de visualización de la palabra clave: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. El valor predeterminado para las nuevas palabras clave es *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** La cadena que se va a usar como valor de sustitución si la dirección URL base o la plantilla de seguimiento contiene [la cadena de sustitución dinámica `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** La cadena que se va a usar como valor de sustitución si la dirección URL base o la plantilla de seguimiento contiene [la cadena de sustitución dinámica `{param2}`](https://support.google.com/google-ads/answer/6305348).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](keyword-manage.md)
