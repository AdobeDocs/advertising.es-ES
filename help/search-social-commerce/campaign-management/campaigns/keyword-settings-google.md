---
title: '[!DNL Google Ads] configuración de palabras clave'
description: Haga referencia a la configuración de [!DNL Google Ads] Palabras clave.
exl-id: 8834e852-214b-4b2c-9a95-4b1c802e800d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# [!DNL Google Ads] configuración de palabras clave

Puede crear palabras clave para las campañas que utilizan las redes de búsqueda y visualización.

Consulte la ayuda de Google Ads para [límites de palabras clave por cuenta](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave, incluidas las [!DNL Google Ads] sintaxis de coincidencia para palabras clave y marcadores de posición. [!DNL Google Ads] Las cuentas de requieren palabras clave con los atributos siguientes:

* La longitud máxima por palabra clave es de 80 caracteres y no más de 10 palabras.
* La palabra clave solo puede incluir letras, dígitos y los siguientes caracteres especiales: espacio `# $ & _ - " [] ' + . / :`

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

>[!NOTE]
>
>* Puede crear palabras clave negativas desde el [!UICONTROL Keywords] > [!UICONTROL Negatives] vea y en el grupo de publicidad y en la configuración de la campaña.
>* Cambio de una [!DNL Google Ads] keyword o match type elimina la palabra clave existente y crea una nueva.

**[!UICONTROL Status]:** El estado de visualización de la palabra clave: *Activo* o *Pausado*. El valor predeterminado para las palabras clave nuevas es *Activo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Marcadores

**[!UICONTROL Param1]:** Cadena que se utilizará como valor de sustitución si la dirección URL base o la plantilla de seguimiento contienen [el `{param1}`](https://support.google.com/google-ads/answer/6305348) cadena de sustitución dinámica.

**[!UICONTROL Param2]:** Cadena que se utilizará como valor de sustitución si la dirección URL base o la plantilla de seguimiento contienen [el `{param2}`](https://support.google.com/google-ads/answer/6305348) cadena de sustitución dinámica.

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
