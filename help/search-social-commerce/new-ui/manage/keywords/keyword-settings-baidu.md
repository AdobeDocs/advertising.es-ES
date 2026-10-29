---
title: '[!DNL Baidu] configuración de palabras clave'
description: Hacer referencia a la configuración de las palabras clave [!DNL Baidu].
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
source-wordcount: '245'
ht-degree: 0%
---
# [!DNL Baidu] configuración de palabras clave

## [!UICONTROL Basic Settings]

*Solo palabras clave nuevas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign]:** La campaña.

**[!UICONTROL Ad Group]:** El grupo de anuncios.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave. La longitud máxima por palabra clave es de 30 caracteres de un byte o 15 de doble byte.

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes. Utilice la siguiente sintaxis:

* `keyword` para la coincidencia amplia
* `"keyword"` para coincidencia de frase
* `[keyword]` para coincidencia exacta

>[!NOTE]
>
>* [!DNL Baidu] solo permite un tipo de coincidencia por palabra clave y grupo de anuncios. Por ejemplo, el grupo de anuncios 1 no puede incluir `"keyword"` y `[keyword]`.
>* Puede crear palabras clave negativas en la pestaña [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives], así como en el grupo de anuncios y en la configuración de la campaña.
>* Al cambiar una palabra clave [!DNL Baidu], se eliminará la palabra clave existente y se creará una nueva con un nuevo identificador de palabra clave. Sin embargo, al cambiar el tipo de coincidencia no se elimina la palabra clave existente.

**[!UICONTROL Status]:** Estado de visualización de la palabra clave: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. El valor predeterminado para las nuevas palabras clave es *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL URL Options]

**[!UICONTROL Base URL]:** (Campañas solo con seguimiento a nivel de palabra clave; opcional) La dirección URL de la página de aterrizaje a la que se llevan los usuarios cuando hacen clic en el anuncio. Puede incluir redirección de terceros y código de seguimiento. Si introduce un valor, anula la dirección URL base del anuncio.

Una vez guardado el registro, la dirección URL base incluye cualquier parámetro de datos anexados configurado para la campaña o cuenta.

Si usa el servicio de seguimiento de conversión de Adobe Advertising y la configuración de campaña incluye el uso de [!UICONTROL EF Redirect] y la adición de seguimiento en el nivel de palabra clave, Search, Social y Commerce agregarán automáticamente su propio código de seguimiento de clics.

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](keyword-manage.md)
