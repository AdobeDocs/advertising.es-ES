---
title: '[!DNL Baidu] configuración de palabras clave'
description: Hacer referencia a la configuración de  [!DNL Baidu] palabras clave.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# [!DNL Baidu] configuración de palabras clave

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Las palabras clave. La longitud máxima por palabra clave es de 30 caracteres de un solo byte o 15 de doble byte

Puede escribir o pegar hasta 2000 palabras clave. Separe varias palabras clave con comas o introdúzcalas en líneas independientes. Utilice la siguiente sintaxis:

* `keyword` para la coincidencia amplia
* `"keyword"` para coincidencia de frase
* `[keyword]` para coincidencia exacta

>[!NOTE]
>
>* [!DNL Baidu] solo permite un tipo de coincidencia por palabra clave y grupo de anuncios. Por ejemplo, el grupo de anuncios 1 no puede incluir `"keyword"` y `[keyword]`.
>* Puede crear palabras clave negativas desde la vista [!UICONTROL Keywords] > [!UICONTROL Negatives] y en la configuración de grupos de anuncios y campañas.
>* Al cambiar una palabra clave [!DNL Baidu], se eliminará la palabra clave existente y se creará una nueva con un nuevo identificador de palabra clave. Sin embargo, al cambiar el tipo de coincidencia no se elimina la palabra clave existente.

**[!UICONTROL Status]:** El estado de visualización de la palabra clave: *Activo* o *En pausa*. El valor predeterminado para las palabras clave nuevas es *Activo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Opciones de URL

**[!UICONTROL Base URL]:** (Campañas solo con seguimiento a nivel de palabra clave; opcional) La dirección URL de la página de aterrizaje a la que se llevan los usuarios cuando hacen clic en el anuncio. Puede incluir
código de seguimiento y redirección de terceros. Si introduce un valor, anula la dirección URL base del anuncio.

Una vez guardado el registro, la dirección URL base incluye cualquier parámetro de datos anexados configurado para la campaña o cuenta.

Si usa el servicio de seguimiento de conversión de Adobe Advertising y la configuración de campaña incluye el uso de [!UICONTROL EF Redirect] y la adición de seguimiento en el nivel de palabra clave, Search, Social y Commerce agregarán automáticamente su propio código de seguimiento de clics.

>[!MORELIKETHIS]
>
>* [Administrar palabras clave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
