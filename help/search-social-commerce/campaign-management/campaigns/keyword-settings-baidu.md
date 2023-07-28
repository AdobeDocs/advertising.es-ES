---
title: '[!DNL Baidu] configuración de palabras clave'
description: Haga referencia a la configuración de [!DNL Baidu] Palabras clave.
exl-id: 70ecb5da-1056-4d87-82ba-ac03e0c81761
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] configuración de palabras clave

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave. La longitud máxima por palabra clave es de 30 caracteres de un solo byte o 15 de doble byte

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes. Utilice la siguiente sintaxis:

* `keyword` para coincidencia amplia
* `"keyword"` para coincidencia de frase
* `[keyword]` para coincidencia exacta

>[!NOTE]
>
>* [!DNL Baidu] solo permite un tipo de coincidencia por palabra clave y grupo de anuncios. Por ejemplo, el grupo de anuncios 1 no puede incluir ambos `"keyword"` y `[keyword]`.
>* Puede crear palabras clave negativas desde el [!UICONTROL Keywords] > [!UICONTROL Negatives] vea y en el grupo de publicidad y en la configuración de la campaña.
>* Cambio de una [!DNL Baidu] elimina la palabra clave existente y crea una nueva con un nuevo ID de palabra clave. Sin embargo, al cambiar el tipo de coincidencia no se elimina la palabra clave existente.

**[!UICONTROL Status]:** El estado de visualización de la palabra clave: *Activo* o *Pausado*. El valor predeterminado para las palabras clave nuevas es *Activo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Opciones de URL

**[!UICONTROL Base URL]:** (Campañas solo con seguimiento a nivel de palabra clave; opcional) La dirección URL de la página de aterrizaje a la que se llevan los usuarios cuando hacen clic en el anuncio. Puede incluir redirección de terceros y código de seguimiento. Si introduce un valor, anula la dirección URL base del anuncio.

Una vez guardado el registro, la dirección URL base incluye cualquier parámetro de datos anexados configurado para la campaña o cuenta.

Si utiliza el servicio de seguimiento de conversión de Adobe Advertising y la configuración de campaña incluye el uso de la variable [!UICONTROL EF Redirect] y agregar seguimiento en el nivel de palabra clave, Search, Social y Commerce añadirán automáticamente su propio código de seguimiento de clics.

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
