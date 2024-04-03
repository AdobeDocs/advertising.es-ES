---
title: Parámetros de seguimiento opcionales para URL de seguimiento de clics
description: Obtenga información acerca de los parámetros opcionales de seguimiento de búsqueda, medios sociales y comerciales y los parámetros de seguimiento específicos de la red de publicidad que puede agregar a sus direcciones URL de seguimiento de clics.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: 3460011a707608c172920801196837f7a278e2c0
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Parámetros de seguimiento opcionales para URL de seguimiento de clics

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo Native], [!DNL Yahoo! Japan], y [!DNL Yandex] solo cuentas*

En lugar de utilizar únicamente los parámetros de seguimiento estándar para una dirección URL final o una dirección URL de destino, puede agregar más parámetros para rastrear datos específicos de una cuenta de red de publicidad. Puede agregar cualquier combinación de los siguientes parámetros en la configuración de la cuenta o de la campaña:

* Puede anexar cualquier cadena de texto estático como parámetro en las direcciones URL base de la cuenta o campaña.

* Puede anexar parámetros específicos de Adobe Advertising y de red de publicidad en las direcciones URL base de la cuenta o campaña para rastrear más datos:

   * Los parámetros de Adobe Advertising son semiestáticos. El Adobe Advertising inserta un valor de datos cuando carga la dirección URL base en la red publicitaria. Por ejemplo, al anexar `campaign={ef_campaign}` a la dirección URL base, el Adobe Advertising reemplaza a `{ef_campaign}` con el nombre real de la campaña (como &quot;Campaña de vuelta al colegio&quot;) cuando carga la dirección URL.

     **Nota:** Una vez insertados los valores, permanecen estáticos. Si mueve una palabra clave o un anuncio a un grupo de anuncios diferente o mueve el grupo de anuncios a una campaña diferente, la variable  {ef_adgroup} o {ef_campaign} El parámetro no se actualiza automáticamente, por lo que debe generar manualmente una nueva URL de destino o una URL base (final).

   * Los parámetros específicos de red de anuncios son dinámicos y el motor de búsqueda inserta un valor de datos cuando el usuario hace clic en un anuncio. Por ejemplo, al anexar `{param1}` a la dirección URL base, la red de publicidad la sustituye por la dirección URL real {param1} valor cuando un usuario final hace clic en el anuncio.

>[!NOTE]
>
>* Separe varios parámetros con comas o símbolos ampersand (`&`).
>* Los siguientes parámetros no distinguen entre mayúsculas y minúsculas.
>* Los caracteres especiales de los parámetros anexados se sustituyen de la siguiente manera en la URL de destino o la URL base (final) generada:
>  * `=` se sustituye por `%3D`
>  * `?` se sustituye por `%26`
>  * se sustituye un espacio vacío por `%2B`
>  Por ejemplo, al anexar el parámetro `campaign={ef_campaign}` a la dirección URL base http://www.example.com para una palabra clave, la dirección URL base para esa palabra clave se genera como `http://www.example.com/campaign%3D{ef_campaign}`.

## Parámetros de seguimiento estáticos de Search, Social y Commerce

Puede utilizar los siguientes parámetros para cuentas en cualquier red de publicidad y puede combinarlos con parámetros para una red de publicidad específica según sea necesario. Algunos de estos parámetros duplican los parámetros que se añaden automáticamente para redes de anuncios específicas cuando el método de seguimiento de la cuenta es &quot;[!UICONTROL EF Direct].&quot;

Todos los parámetros siguientes deben especificarse como un par clave-valor; puede incluir varios parámetros para un par de valores. Por ejemplo, para insertar el nombre de la campaña, utilice `<your_parameter_name>={ef_campaign}`, como `campaign={ef_campaign}`. Para insertar el tipo de coincidencia utilizando los nombres de tipo de coincidencia especificados, utilice `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, como `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. Los tipos de coincidencia no aplicables no aparecen en la dirección URL resultante.

| Parámetro | Descripción |
| ---- | ---- |
| <code>{custom_code}</code> | Para insertar datos de la columna &quot;Parámetro de URL personalizado&quot; en un archivo de hoja de edición masiva cargado en la dirección URL de seguimiento. {custom_code} solo se puede usar al final del valor de uno o más pares clave-valor en la URL de seguimiento. Ejemplos:  <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Nota:</b> Para insertar el valor personalizado del archivo de hoja de edición masiva en la URL de seguimiento, cargue el archivo de hoja de edición masiva con la opción &quot;Generar URL de seguimiento&quot;. Para obtener más información sobre el uso de archivos de hojas de edición masiva, consulte &quot;[Administración de datos de campaña mediante hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| <code>{ef_uniqueid}</code> | Para insertar el ID único creado por el Adobe Advertising. Se agrega automáticamente cuando el método de seguimiento es &quot;Redireccionamiento de EF&quot;. |
| <code>{ef_userid}</code> | Para insertar el ID de usuario único que el Adobe Advertising asigna al anunciante. |
| <code>{ef_sid}</code> | Para insertar el ID numérico que Search, Social y Commerce asignan a la red de anuncios: <i>[!UICONTROL 3]</i> para [!DNL Google Ads], <i>[!UICONTROL 10]</i> para [!DNL Microsoft®® Advertising], <i>[!UICONTROL 45]</i> para [!DNL Meta], <i>[!UICONTROL 86]</i> para [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> para [!DNL Naver], <i>[!UICONTROL 88]</i> para [!DNL Baidu], <i>[!UICONTROL 90]</i> para [!DNL Yandex], <i>[!UICONTROL 94]</i> para [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> para [!DNL Yahoo Native] (obsoleto), o <i>[!UICONTROL 106]</i> para [!DNL Pinterest] (obsoleto). |
| <code>{ef_searchengine}</code> | Para insertar el nombre de red del anuncio. |
| <code>{ef_campaign}</code> | Para insertar el nombre de la campaña. |
| <code>{ef_campaignid}</code> | Para insertar el ID de campaña. <b>Nota:</b> El ID de una nueva campaña no se crea hasta que la campaña se publica en la red de anuncios. Si la cuenta utiliza el &quot;[!UICONTROL EF Redirect]&quot; y &quot;AutoUpload&quot; y, a continuación, Adobe Advertising inserta automáticamente el ID de campaña en las direcciones URL de destino o finales relevantes al día siguiente. Si la cuenta no utiliza el &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y si desea insertar el ID de campaña en las URL de destino relevantes o en las URL finales, debe crear la campaña, descargar un archivo de hoja de edición masiva para la nueva campaña, utilizando la opción para &quot;Generar URL de seguimiento&quot;, y luego publicar el archivo en la red de publicidad. |
| <code>{ef_adgroup}</code> | Para insertar el nombre del grupo de publicidad. |
| <code>{ef_adgroupid}</code> | Para insertar el ID del grupo de publicidad. <b>Nota:</b> El ID de un nuevo grupo de anuncios no se crea hasta que se publica el grupo de anuncios en la red de anuncios. Si la cuenta utiliza el &quot;[!UICONTROL EF Redirect]&quot; y &quot;AutoUpload&quot; y, a continuación, Adobe Advertising inserta automáticamente el ID de grupo de publicidad en las direcciones URL de destino o finales relevantes al día siguiente. Si la cuenta no utiliza el[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y desea insertar el ID del grupo de anuncios en las URL de destino relevantes o en las URL finales, debe crear el grupo de anuncios, descargar un archivo de hoja de edición masiva para el nuevo grupo de anuncios y usar la opción para &quot;Generar URL de seguimiento&quot; y luego publicar el archivo en la red de anuncios. |
| <code>{ef_keyword}</code> | Para insertar la palabra clave. |
| <code>{ef_keywordid}</code> | Para insertar el ID de palabra clave. <b>Nota:</b> El ID de una palabra clave nueva no se crea hasta que se publica la palabra clave en la red de anuncios. Si la cuenta utiliza el &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y, a continuación, Adobe Advertising inserta automáticamente el ID de palabra clave en las URL de destino relevantes o en las URL finales al día siguiente. Si la cuenta no utiliza el &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y desea insertar el ID de palabra clave en las URL de destino relevantes o en las URL finales, debe crear la palabra clave, descargar un archivo de hoja de edición masiva para la nueva palabra clave, utilizando la opción para &quot;Generar URL de seguimiento&quot;, y luego publicar el archivo en la red de publicidad. |
| <code>{ef_matchtype}</code> | Para insertar el tipo de coincidencia de palabra clave como &quot;Amplia&quot;, &quot;Exacta&quot; o &quot;Frase&quot;. Incluido automáticamente para [!DNL Google Ads] y [!DNL Microsoft® Advertising] con el signo &quot;[!UICONTROL EF Redirect]&quot; método de seguimiento. |
| <code>{ef_adid}</code> | Para insertar el ID de anuncio. <b>Nota:</b> El ID de un anuncio nuevo no se crea hasta que se publica el anuncio en la red de anuncios. Si la cuenta utiliza el &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y, a continuación, Adobe Advertising inserta automáticamente el ID de anuncio en las direcciones URL de destino o finales relevantes al día siguiente. Si la cuenta no utiliza el &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Auto Upload]&quot; y desea insertar el ID de anuncio en las URL de destino relevantes o en las URL finales, debe crear el anuncio, descargar un archivo de hoja de edición masiva para el nuevo anuncio, utilizando la opción para &quot;Generar URL de seguimiento&quot;, y luego publicar el archivo en la red de anuncios. |

## [!DNL Google Ads] parámetros de seguimiento dinámico

Consulte [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft® Advertising] parámetros de seguimiento dinámico

Consulte [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## [!DNL Yahoo Native] parámetros de seguimiento dinámico

Consulte [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## [!DNL Yahoo! Japan Ads] parámetros de seguimiento dinámico

Consulte [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] parámetros de seguimiento dinámico

Consulte [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
