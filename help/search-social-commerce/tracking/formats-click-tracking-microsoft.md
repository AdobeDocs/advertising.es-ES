---
title: Formatos de rastreo de clics para  [!DNL Microsoft Advertising]
description: Obtenga información acerca de los formatos de seguimiento de clics para  [!DNL Microsoft Advertising] cuentas.
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Formatos de rastreo de clics para [!DNL Microsoft Advertising]

A continuación se muestran los formatos base de plantilla de seguimiento y sufijo de página de aterrizaje (sufijo de dirección URL final) que Search, Social y Commerce requieren para [!DNL Microsoft Advertising].

## Formatos de plantilla de seguimiento

### Redes de búsqueda y audiencia (excepto vínculos de sitios)

El siguiente formato se aplica a todos los tipos de anuncios a los que se puede realizar un seguimiento en las redes de búsqueda y audiencia.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante en Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si la transferencia de tokens está deshabilitada, sustituya `cq?` después de `<advertiser_ID>` por `c?`.
>
>* `{TargetId}` representa el identificador de a) la palabra clave o b) la palabra clave y la lista de remarketing (audiencia) que activaron el anuncio (por ejemplo, &quot;kwd-123:aud-456&quot; para una palabra clave y una lista de remarketing o &quot;kwd-123&quot; solo para palabra clave).

### Vínculos de sitio

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante en Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si la transferencia de tokens está deshabilitada, sustituya `cq?` después de `<advertiser_ID>` por `c?`.
>
>* `{TargetId}` representa el identificador de a) la palabra clave o b) la palabra clave y la lista de remarketing (audiencia) que activaron el anuncio (por ejemplo, &quot;kwd-123:aud-456&quot; para una palabra clave y una lista de remarketing o &quot;kwd-123&quot; solo para palabra clave).
>
>* `{adextensionid}` no se utiliza.
>
>* (Vínculos de sitio) Puede ver qué conversiones resultaron de un clic en un vínculo de sitio al generar un [!UICONTROL Transaction Report]. El valor de columna [!UICONTROL Link Type] para un vínculo de sitio es `sl:<Sitelink text>`, como `sl:See Current Offers`.

### Red de compras

Los siguientes formatos se aplican a los anuncios de compras en redes de compras. Puede especificar una plantilla de seguimiento en los niveles de cuenta, campaña, grupo de publicidad o grupo de productos.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante en Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si la transferencia de tokens está deshabilitada, sustituya `cq?` después de `<advertiser_ID>` por `c?`.
>
>* `{TargetId}` representa el identificador de a) la palabra clave o b) la palabra clave y la lista de remarketing (audiencia) que activaron el anuncio (por ejemplo, &quot;kwd-123:aud-456&quot; para una palabra clave y una lista de remarketing o &quot;kwd-123&quot; solo para palabra clave).
>
>* (Opcional) En lugar de introducir plantillas de seguimiento en el nivel de cuenta, campaña, grupo de anuncios o grupo de productos, puede añadir la URL de seguimiento a los datos del producto dentro de la cuenta [!DNL Microsoft Merchant Center]. Para ello, incluya la dirección URL de seguimiento, junto con el valor en el campo &quot;`link`&quot; o &quot;`mobile_link`&quot;, según corresponda, en una columna personalizada &quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot; dentro de la fuente del producto. El valor del campo &quot;`bingads_redirect`&quot; reemplaza los valores de los campos &quot;`link`&quot; y &quot;`mobile_link`&quot;. Las direcciones URL generadas con este método no incluyen ningún parámetro de seguimiento especificado en la configuración de la cuenta de Search, Social y Commerce o de la campaña.

## Formatos de sufijo de página de aterrizaje (sufijo de URL final)

>[!NOTE]
>
>Los sufijos de la página de aterrizaje en niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el editor de la red de anuncios.

### Redes de búsqueda y audiencia

Las cuentas que usan el seguimiento de conversión de Adobe Advertising deben incluir el identificador de clic (`msclkid` para [!DNL Microsoft Advertising]) de la red de publicidad en el sufijo:

* Cuando el anunciante tiene una integración de Adobe Analytics, el sufijo debe incluir lo siguiente:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}`

* Cuando el anunciante no tiene una integración de Adobe Analytics, el sufijo debe incluir lo siguiente:

  `&ev_efid={msclkid}:G:s`

### Red de compras

Las cuentas que usan el seguimiento de conversión de Adobe Advertising deben incluir el identificador de clic (`msclkid` para [!DNL Microsoft Advertising]) de la red de publicidad en el sufijo:

* Cuando el anunciante tiene una integración de Adobe Analytics, el sufijo debe incluir lo siguiente:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`

* Cuando el anunciante no tiene una integración de Adobe Analytics, el sufijo debe incluir lo siguiente:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID de AMO](/help/integrations/analytics/ids.md#amo-id-formats)
