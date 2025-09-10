---
source-git-commit: 4428fb626de79a98d6a37c36057a0d468ce23166
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---
# ID de Adobe Advertising AMO

### Formatos de ID de AMO {#amo-id-formats}

#### Formato de ID de AMO para [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

donde:

* `AC` indica el canal de visualización.

* `{TM_AD_ID}` es la clave de anuncio alfanumérica generada por Adobe Advertising. Se utiliza como identificador único de un anuncio y sirve como clave para traducir metadatos de entidad de Adobe Advertising a dimensiones legibles de [!DNL Analytics] y Customer Journey Analytics.

* `{TM_PLACEMENT_ID}` es la clave de ubicación alfanumérica generada por Adobe Advertising. Se utiliza como identificador único de una ubicación y sirve como clave para traducir metadatos de entidad de Adobe Advertising a dimensiones legibles de [!DNL Analytics] y Customer Journey Analytics.

Ejemplo de ID de AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### Formatos de ID de AMO para anuncios de Search, Social y Commerce {#amo-id-format-search}

Los parámetros varían según la red de anuncios, pero los siguientes parámetros son comunes a todos los operadores:

* `AL` indica el canal de búsqueda. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` es un identificador de usuario único asignado al anunciante.

* `{sid}` se ha reemplazado por el identificador numérico de la cuenta de red de anuncios del anunciante: *3* para [!DNL Google Ads], *10* para [!DNL Microsoft Advertising], *45* para [!DNL Meta], *86* para [!DNL Yahoo! Display Network], *87* para [!DNL Naver], *88* para [!DNL Baidu], *90* para [!DNL Yandex], *94* para [!DNL Yahoo! Japan Ads], *105* para [!DNL Yahoo Native] (obsoleto) o *106* para [!DNL Pinterest] (obsoleto).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

donde:

* `{creative}` es el identificador numérico único de la red de anuncios para el creativo.
* `{placement}` es el sitio web en el que se hizo clic en el anuncio.
* `{keywordid}` es el identificador numérico único de la red de anuncios para la palabra clave que activó el anuncio.

##### [!DNL Google Ads]

Esto incluye campañas de compra que usan [!DNL Google Merchant Center].

* Cuentas que utilizan el formato de ID de AMO más reciente, que admite la creación de informes de nivel de campaña y de grupo de publicidad para campañas Máximo rendimiento de, así como campañas de borradores y experimentos:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Otras cuentas:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

donde:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` es el ID numérico único [!DNL Google Ads] del creativo.
* `{matchtype}` es el tipo de coincidencia de la palabra clave que activó el anuncio: `e` para exacto, `p` para frase o `b` para amplio.
* `{placement}` es el nombre de dominio del sitio web en el que se hizo clic en el anuncio. Hay un valor disponible para los anuncios de campañas con objetivos de ubicación y para los anuncios de campañas con objetivos de palabras clave que se muestran en sitios de contenido.
* `{network}` indica la red desde la que se produjo el clic: `g` para la búsqueda de [!DNL Google] (solo para anuncios segmentados por palabras clave), `s` para un socio de búsqueda (solo para anuncios segmentados por palabras clave) o `d` para la red de visualización (para anuncios segmentados por palabras clave o por ubicación).
* `{product_partition_id}` es el identificador numérico único de la red de anuncios para el grupo de productos usado con los anuncios de productos.
* `{keyword}` es la palabra clave específica que activó el anuncio (en sitios de búsqueda) o la palabra clave que mejor coincide (en sitios de contenido).
* `{campaignid}` es el identificador numérico único de la red de anuncios para la campaña.
* `{adgroupid}` es el identificador numérico único de la red de anuncios para el grupo de anuncios.

>[!NOTE]
>
>* Para los anuncios dinámicos de búsqueda, {keyword} se completa con el destino automático.
>* Cuando genera el seguimiento de [!DNL Google] anuncios de compras, se inserta un parámetro de id. de producto, `{adwords_producttargetid}`, antes del parámetro de palabra clave. El parámetro de id. de producto no aparece en los parámetros de seguimiento de nivel de cuenta y de campaña [!DNL Google Ads].
>* Para usar el código de seguimiento de ID de AMO más reciente, consulta &quot;[Actualizar el código de seguimiento de ID de AMO para una [!DNL Google Ads] cuenta](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Todos los tipos de campaña:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

donde:

* `{AdId}` es el identificador numérico único de la red de anuncios para el creativo.
* `{OrderItemId}` es el identificador numérico de la red de anuncios para la palabra clave.
* `{CampaignId}` es el identificador numérico único de la red de anuncios para la campaña.
* `{AdGroupId}` es el identificador numérico único de la red de anuncios para el grupo de anuncios.

>[!NOTE]
>
> Para cuentas con campañas sin la opción de seguimiento [!UICONTROL Auto Upload] que aún no se migraron al nuevo formato, actualice manualmente cada sufijo de página de aterrizaje para incluir el formato anterior.
> &#x200B;>Mientras tanto, los formatos heredados, como se indica a continuación, siguen funcionando:
>* Buscar campañas:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Campañas de compra (con [!DNL Microsoft Merchant Center]):
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campañas de Audience Network:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

donde:

* `{creative}` es el identificador numérico único de la red de anuncios para el creativo.
* `{matchtype}` es el tipo de coincidencia de la palabra clave que activó el anuncio: `be` para exacto, `bp` para frase o `bb` para amplio.
* `{network}` indica la red desde la que se produjo el clic: `n` para nativo o `s` para búsqueda.
* `{keyword}` es la palabra clave que activó su anuncio.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

donde:

* `{ad_id}` es el identificador numérico único de la red de anuncios para el creativo.
* `{source_type}` es el tipo de sitio en el que se ha mostrado el anuncio: *b* para la búsqueda, *c* para el contexto (contenido) o *ct* para la categoría.
* `{phrase_id}` es el identificador numérico de la red de anuncios para la palabra clave.
