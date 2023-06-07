---
title: El parámetro de seguimiento s_kwcid
description: Obtenga información acerca del parámetro de seguimiento utilizado para compartir datos de publicidad de Adobe con Adobe Analytics.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# El parámetro de seguimiento s_kwcid

*Anunciantes con una integración de Adobe Advertising-Adobe Analytics solamente*

<!-- Where should this go? It probably belongs in the Analytics integration chapter, but I'll need to fit it in/create context around it/explain more about implementation and how this works.  SPECIFICALLY, I'll need to update the second section that explains when/where to add the code for DSP clients. -->

Adobe Advertising comparte datos sobre sus campañas con Adobe Analytics mediante el `s_kwcid` parámetro append, que consiste en elementos específicos del canal de publicidad y de la red de publicidad. El parámetro se añade a las direcciones URL de seguimiento de una de las siguientes maneras:

* (Recomendado)<!--; the only option for Advertising DSP-->) Se ha implementado la función s_kwcid del lado del servidor.

   Para [!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas con el [!UICONTROL Auto Upload] configuración habilitada para la cuenta o campaña, el servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final hace clic en un anuncio <!-- click a search ad or views a display ad --> con el píxel de publicidad de Adobe.

   Para otras redes de publicidad, o [!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas con el [!UICONTROL Auto Upload] Si la opción está desactivada, añada manualmente el parámetro a los parámetros de adición de nivel de cuenta, que lo adjuntan a las direcciones URL base.

* <!-- (Search, Social, & Commerce only) -->La función s_kwcid del lado del servidor no está implementada y debe añadir manualmente el parámetro s_kwcid a su ([!DNL Google Ads] y [!DNL Microsoft Advertising]) sufijos de página de aterrizaje o (otras redes de anuncios) parámetros de datos anexados de nivel de cuenta.

Para implementar la función s_kwcid del lado del servidor o para determinar la mejor opción para su empresa, hable con el equipo de cuenta de Adobe.

## `s_kwcid` DSP formato de los anuncios de Advertising

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

donde:

* `AC` indica el canal de visualización.

* `{TM_AD_ID}` es la clave de anuncio alfanumérica.

* `{TM_PLACEMENT_ID}` es la clave de ubicación alfanumérica.

## `s_kwcid` formatos para anuncios de Search, Social y Commerce

Los parámetros varían según la red de anuncios, pero los siguientes parámetros son comunes a todos los operadores:

* `AL` indica el canal de búsqueda. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` es un ID de usuario único asignado al anunciante.

* `{sid}` se sustituye por el ID numérico de la cuenta de red de publicidad del anunciante: *3* para [!DNL Google Ads], *10* para [!DNL Microsoft Advertising], *45* para [!DNL Meta], *86* para [!DNL Yahoo! Display Network], *87* para [!DNL Naver], *88* para [!DNL Baidu], *90* para [!DNL Yandex], *94* para [!DNL Yahoo! Japan Ads], *105* para [!DNL Yahoo Native] (obsoleto), o *106* para [!DNL Pinterest] (obsoleto).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Estos incluyen campañas de compra que utilizan [!DNL Google Merchant Center].

* Cuentas que utilizan el formato s_kwcid más reciente, que admite informes de nivel de campaña y de grupo de publicidad para campañas Máximo rendimiento de, así como campañas de borradores y experimentos:

   `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Otras cuentas:

   `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* Para los anuncios dinámicos de búsqueda, {keyword} se rellena con el destino automático.
>* Cuando se genera un seguimiento para [!DNL Google] anuncios de compra, un parámetro de ID de producto, `{adwords_producttargetid}`, se inserta antes del parámetro keyword. El parámetro de ID de producto no aparece en la [!DNL Google Ads] parámetros de seguimiento a nivel de cuenta y de campaña.
>* Para utilizar el código de seguimiento s_kwcid más reciente, consulte &quot;[Actualizar el código de seguimiento s_kwcid para un [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md).&quot;


<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* Buscar campañas:

   `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Campañas de compra (con [!DNL Microsoft Merchant Center]):

   `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campañas de Audience Network:

   `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
>* [Administrar las cuentas de red de publicidad](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Configuración de campaña de Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Configuración de campañas de Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Configuración de campañas de Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Configuración de campañas de anuncios de Japón](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Configuración de campaña de Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
