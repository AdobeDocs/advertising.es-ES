---
title: Formatos de rastreo de clics para [!DNL Google Ads]
description: Obtenga información acerca de los formatos de seguimiento de clics para [!DNL Google Ads] cuentas.
exl-id: 68f6da43-3430-4c0a-9369-937fa52c071a
feature: Search Tracking
source-git-commit: ceb2fc07eb5116b3a2bb01cf72fd779f78bba1f0
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Formatos de rastreo de clics para [!DNL Google Ads]

A continuación se muestran los formatos de plantilla de seguimiento base y sufijo de página de aterrizaje (sufijo de URL final) que Search, Social y Commerce requieren para [!DNL Google Ads].

## Formatos de plantilla de seguimiento

### Red de búsqueda/visualización, incluidos los enlaces de sitios

El siguiente formato se aplica a todos los tipos de anuncios a los que se puede realizar un seguimiento en las redes de búsqueda y visualización, así como a los vínculos de sitios.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Ejemplo:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante dentro de Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si el paso de tokens está deshabilitado, sustituya `cq?` después `<advertiser_ID>` con `c?`.
>
>* El [!DNL ValueTrack] Los parámetros para indicar las direcciones URL finales en las plantillas de seguimiento deben ser `{lpurl}` o `!{unescapedurl}`.
>
>* (Anuncios de texto) Cuando pujas por palabra clave, el parámetro `ev_pl` (para ubicaciones) no tiene valor. Cuando pujas por ubicación, `ev_ln` (para palabras clave) no tiene valor. Cuando pujas por grupo de anuncios o por cualquier otra dimensión, tanto `ev_ln` y `ev_pl` no tiene valores.
>
>* (Anuncios dinámicos de búsqueda) `{keyword}` indica la expresión de destino de búsqueda dinámica, como `_cat:[VALUE]` o `_url:[VALUE]`.
>
>* (Anuncios dinámicos de búsqueda) [!DNL Google Ads] determina la dirección URL final de forma dinámica, por lo que no es necesario introducir una.
>
>* (Vínculos de sitio) Puede ver qué conversiones resultaron de un clic en un vínculo de sitio al generar un [!UICONTROL Transaction Report]. El [!UICONTROL Link Type] el valor de columna para un vínculo de sitio es `sl:<Sitelink text>`, como `sl:See Current Offers`.

### Red de compras

El siguiente formato se aplica a los anuncios de compras y grupos de productos en redes de compras. Puede especificar una plantilla de seguimiento en los niveles de cuenta, campaña, grupo de publicidad o grupo de productos.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Ejemplo:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante dentro de Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si el paso de tokens está deshabilitado, sustituya `cq?` después `<advertiser_ID>` con `c?`.
>
>* El [!DNL ValueTrack] Los parámetros para indicar las direcciones URL finales en las plantillas de seguimiento deben ser `{lpurl}` o `!{unescapedurl}`.
>
>* [!DNL Google Ads] utiliza las direcciones URL del producto en la fuente de Google Merchant Center como direcciones URL finales, por lo que no es necesario que introduzca las direcciones URL finales para los datos o grupos de productos.
>
>* Puede ver qué conversiones resultaron de un clic en un anuncio de compra al generar un [!UICONTROL Transaction Report]. El [!UICONTROL Link Type] valor de columna para un anuncio de producto:`<product ID>`, como `pla:8525822`.

## Formatos de sufijo de página de aterrizaje (sufijo de URL final)

Las cuentas que utilizan el seguimiento de conversión de Adobe Advertising deben incluir el identificador de clic ( ) de la red de publicidad`gclid` para [!DNL Google Ads]) en el sufijo:

* Cuando el anunciante tiene una integración de Adobe Analytics, el sufijo debe incluir uno de los siguientes:

   * [!DNL Google Ads] cuentas que utilizan la última versión [Formato de ID de AMO](/help/integrations/analytics/ids.md#amo-id-formats) (comenzando por `s_kwcid`), que admite la creación de informes de nivel de campaña y de grupo de publicidad para campañas Máximo rendimiento de y campañas de borradores y experimentos:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Si la cuenta tiene una implementación de AMO ID del lado del servidor y la configuración de la cuenta o la campaña &quot;[!UICONTROL Auto Upload]&quot; está habilitado y, a continuación, el parámetro se agrega automáticamente. De lo contrario, debe agregarlo manualmente. Consulte &quot;[ID de Adobe Advertising utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement).&quot;

   * Todos los demás [!DNL Google Ads] cuentas:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Cuando el anunciante no tiene una integración de Adobe Analytics, el sufijo debe incluir lo siguiente:

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Los sufijos de la página de aterrizaje en niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el editor de la red de anuncios.
>
>* (Anuncios dinámicos de búsqueda; anunciantes con Adobe Analytics y sin seguimiento del lado del servidor) Si desea incluir el seguimiento de la fuente inversa de Adobe Advertising a Analytics, añada el código de seguimiento de ID de AMO al final del sufijo de página de aterrizaje de nivel de cuenta.

>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID de AMO](/help/integrations/analytics/ids.md#amo-id-formats)
