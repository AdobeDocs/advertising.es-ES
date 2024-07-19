---
title: Parámetros de seguimiento opcionales para URL de seguimiento de clics
description: Obtenga información acerca de los parámetros opcionales de seguimiento de Search, Social y Commerce y los parámetros de seguimiento específicos de la red de anuncios que puede agregar a las direcciones URL de seguimiento de clics.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: f633f2af545f034b08b378653b4b967710402a03
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Parámetros de seguimiento opcionales para URL de seguimiento de clics

Solo cuentas de *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan] y [!DNL Yandex]*

En lugar de utilizar únicamente los parámetros de seguimiento estándar para una dirección URL final o una dirección URL de destino, puede agregar más parámetros para rastrear datos específicos de una cuenta de red de publicidad. Puede agregar cualquier combinación de los siguientes parámetros en la configuración de la cuenta o de la campaña:

* Puede anexar cualquier cadena de texto estático como parámetro en las direcciones URL base de la cuenta o campaña.

* Puede anexar parámetros específicos de Adobe Advertising y de red de publicidad en las direcciones URL base de la cuenta o campaña para rastrear más datos:

   * Los parámetros de Adobe Advertising son semiestáticos. El Adobe Advertising inserta un valor de datos cuando carga la dirección URL base en la red publicitaria. Por ejemplo, cuando anexa `campaign={ef_campaign}` a la dirección URL base, Adobe Advertising reemplaza `{ef_campaign}` con el nombre real de la campaña (como &quot;Campaña de vuelta al colegio&quot;) cuando carga la dirección URL.

     **Nota:** Una vez insertados los valores, permanecen estáticos. Si mueve una palabra clave o un anuncio a un grupo de anuncios diferente o mueve el grupo de anuncios a una campaña diferente, el parámetro {ef_adgroup} o {ef_campaign} no se actualiza automáticamente, por lo que debe generar manualmente una nueva dirección URL de destino o una dirección URL base (final).

   * Los parámetros específicos de red de anuncios son dinámicos y el motor de búsqueda inserta un valor de datos cuando el usuario hace clic en un anuncio. Por ejemplo, cuando anexa `{param1}` a la dirección URL base, la red de anuncios la reemplaza por el valor {param1} real cuando un usuario final hace clic en el anuncio.

>[!NOTE]
>
>* Separe los parámetros con comas o el símbolo et (`&`).
>* Los siguientes parámetros no distinguen entre mayúsculas y minúsculas.
>* Los caracteres especiales de los parámetros anexados se sustituyen de la siguiente manera en la URL de destino o la URL base (final) generada:
>  * `=` se ha sustituido por `%3D`
>  * `?` se ha sustituido por `%26`
>  * se ha sustituido un espacio vacío por `%2B`
>  Por ejemplo, cuando se anexa el parámetro `campaign={ef_campaign}` a la dirección URL base http://www.example.com para una palabra clave, la dirección URL base para esa palabra clave se genera como `http://www.example.com/campaign%3D{ef_campaign}`.

## Parámetros de seguimiento estáticos de Search, Social y Commerce

Puede utilizar los siguientes parámetros para cuentas en cualquier red de publicidad y puede combinarlos con parámetros para una red de publicidad específica según sea necesario. Algunos de estos parámetros duplican los parámetros que se agregan automáticamente para redes de anuncios específicas cuando el método de seguimiento de la cuenta es &quot;[!UICONTROL EF Direct]&quot;.

Todos los parámetros siguientes deben especificarse como un par clave-valor; puede incluir varios parámetros para un par de valores. Por ejemplo, para insertar el nombre de la campaña, use `<your_parameter_name>={ef_campaign}`, como `campaign={ef_campaign}`. Para insertar el tipo de coincidencia utilizando los nombres de tipo de coincidencia especificados, use `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, como `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. Los tipos de coincidencia no aplicables no aparecen en la dirección URL resultante.

| Parámetro | Descripción |
| ---- | ---- |
| <code>{custom_code}</code> | Para insertar datos de la columna &quot;Parámetro de URL personalizado&quot; en un archivo de hoja de edición masiva cargado en la dirección URL de seguimiento. {custom_code} solo se puede usar al final del valor de uno o más pares clave-valor en la dirección URL de seguimiento. Ejemplos: <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Nota:</b> Para insertar el valor personalizado del archivo de hoja de edición masiva en la dirección URL de seguimiento, cargue el archivo de hoja de edición masiva mediante la opción &quot;Generar direcciones URL de seguimiento&quot;. Para obtener más información acerca del uso de archivos de hojas de edición masiva, consulte &quot;[Acerca de la administración de datos de campaña mediante hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)&quot;. |
| <code>{ef_uniqueid}</code> | Para insertar el ID único creado por el Adobe Advertising. Se agrega automáticamente cuando el método de seguimiento es &quot;Redireccionamiento de EF&quot;. |
| <code>{ef_userid}</code> | Para insertar el ID de usuario único que el Adobe Advertising asigna al anunciante. |
| <code>{ef_sid}</code> | Para insertar el identificador numérico que Search, Social y Commerce asigna a la red de anuncios: <i>[!UICONTROL 3]</i> para [!DNL Google Ads], <i>[!UICONTROL 10]</i> para [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> para [!DNL Meta], <i>[!UICONTROL 86]</i> para [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> para [!DNL Naver], <i>[!UICONTROL 88]</i> para [!DNL Baidu], <i>[!UICONTROL 90]</i> para [!DNL Yandex], <i>[!UICONTROL 94]</i> para [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> para [!DNL Yahoo Native] (obsoleto) o <i>[!UICONTROL 106]</i> para [!DNL Pinterest] (obsoleto). |
| <code>{ef_searchengine}</code> | Para insertar el nombre de red del anuncio. |
| <code>{ef_campaign}</code> | Para insertar el nombre de la campaña. |
| <code>{ef_campaignid}</code> | Para insertar el ID de campaña. <b>Nota:</b> El identificador de una nueva campaña no se creará hasta que la campaña se publique en la red publicitaria. Si la cuenta usa las opciones &quot;[!UICONTROL EF Redirect]&quot; y &quot;Autocarga&quot;, Adobe Advertising inserta automáticamente el ID de campaña en las direcciones URL de destino relevantes o en las direcciones URL finales al día siguiente. Si la cuenta no utiliza las opciones &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y desea insertar el ID de campaña en las direcciones URL de destino o en las direcciones URL finales relevantes, debe crear la campaña, descargar un archivo de hoja de edición por lotes para la nueva campaña, utilizando la opción para &quot;Generar direcciones URL de seguimiento&quot; y, a continuación, publicar el archivo en la red de publicidad. |
| <code>{ef_adgroup}</code> | Para insertar el nombre del grupo de publicidad. |
| <code>{ef_adgroupid}</code> | Para insertar el ID del grupo de publicidad. <b>Nota:</b> El identificador de un nuevo grupo de anuncios no se creará hasta que se publique el grupo de anuncios en la red de anuncios. Si la cuenta usa las opciones &quot;[!UICONTROL EF Redirect]&quot; y &quot;Autocarga&quot;, Adobe Advertising inserta automáticamente el ID del grupo de publicidad en las direcciones URL de destino relevantes o en las direcciones URL finales al día siguiente. Si la cuenta no utiliza las opciones [!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y desea insertar el ID del grupo de anuncios en las direcciones URL de destino o en las direcciones URL finales relevantes, debe crear el grupo de anuncios, descargar un archivo de hoja de edición por lotes para el nuevo grupo de anuncios y utilizar la opción para &quot;Generar direcciones URL de seguimiento&quot; y, a continuación, publicar el archivo en la red de anuncios. |
| <code>{ef_keyword}</code> | Para insertar la palabra clave. |
| <code>{ef_keywordid}</code> | Para insertar el ID de palabra clave. <b>Nota:</b> El identificador de una nueva palabra clave no se crea hasta que se publique la palabra clave en la red publicitaria. Si la cuenta usa las opciones &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot;, Adobe Advertising inserta automáticamente el identificador de palabra clave en las direcciones URL de destino relevantes o en las direcciones URL finales al día siguiente. Si la cuenta no usa las opciones &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y desea insertar el identificador de palabra clave en las direcciones URL de destino o en las direcciones URL finales relevantes, debe crear la palabra clave, descargar un archivo de hoja de edición por lotes para la nueva palabra clave mediante la opción &quot;Generar direcciones URL de seguimiento&quot; y, a continuación, publicar el archivo en la red de anuncios. |
| <code>{ef_matchtype}</code> | Para insertar el tipo de coincidencia de palabra clave como &quot;Amplia&quot;, &quot;Exacta&quot; o &quot;Frase&quot;. Se incluyó automáticamente para [!DNL Google Ads] y [!DNL Microsoft Advertising] con el método de seguimiento &quot;[!UICONTROL EF Redirect]&quot;. |
| <code>{ef_adid}</code> | Para insertar el ID de anuncio. <b>Nota:</b> El identificador de un anuncio nuevo no se creará hasta que se publique el anuncio en la red publicitaria. Si la cuenta usa las opciones &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot;, Adobe Advertising inserta automáticamente el ID de anuncio en las direcciones URL de destino relevantes o en las direcciones URL finales al día siguiente. Si la cuenta no utiliza las opciones &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y desea insertar el ID de anuncio en las direcciones URL de destino o URL finales relevantes, debe crear el anuncio, descargar un archivo de hoja de edición por lotes para el nuevo anuncio y utilizar la opción para &quot;Generar direcciones URL de seguimiento&quot; y, a continuación, publicar el archivo en la red de anuncios. |

## [!DNL Google Ads] parámetros de seguimiento dinámico

Consulte [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft Advertising] parámetros de seguimiento dinámico

Consulte [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo! Parámetros de seguimiento dinámico de anuncios de Japón

Consulte [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] parámetros de seguimiento dinámico

Consulte [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
