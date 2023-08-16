---
title: ID de Adobe Advertising utilizados por [!DNL Analytics]
description: ID de Adobe Advertising utilizados por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 38f94db19b94f4cb7a6965ccf5da6d83a31154af
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 0%

---

# ID de Adobe Advertising utilizados por [!DNL Analytics]

*Anunciantes con solo integración de Adobe Advertising-Adobe Analytics*

*DSP Aplicable a Advertising y[!DNL Advertising Search, Social, & Commerce]*

El Adobe Advertising de utiliza dos ID para el seguimiento del rendimiento en el sitio: el *EF ID* y el *ID de AMO*.

Cuando se produce una impresión de un anuncio, el Adobe Advertising crea los valores de ID de AMO e ID de EF y los almacena. Cuando un visitante que ha visto un anuncio entra en el sitio sin hacer clic en un anuncio, [!DNL Analytics] llama a estos valores desde el Adobe Advertising hasta el [!DNL Analytics for Advertising] Código JavaScript. Para el tráfico de visualización, [!DNL Analytics] genera un ID suplementario (`SDID`), que se utiliza para unir el EF ID y el AMO ID en [!DNL Analytics]. Para el tráfico de clics, estos ID se incluyen en la dirección URL de la página de aterrizaje utilizando `ef_id` y `s_kwcid` (para el ID de AMO) Parámetros de cadena de consulta.

El Adobe Advertising distingue entre una entrada de pulsaciones o visualizaciones al sitio web según los siguientes criterios:

* Se registra una entrada de visualización cuando un usuario visita el sitio después de ver un anuncio, pero sin hacer clic en él. [!DNL Analytics] registra una visualización si se cumplen dos condiciones:

   * El visitante no tiene pulsaciones para una [!DNL DSP] o [!DNL Search, Social, & Commerce] anuncio durante la [haga clic en ventana retrospectiva](#lookback-a4adc).

   * El visitante ha visto al menos uno [!DNL DSP] anuncio durante la [ventana retrospectiva de impresiones](#lookback-a4adc). La última impresión se pasa como la visualización.

* Se captura una entrada de pulsación cuando un visitante del sitio hace clic en un anuncio antes de entrar en el sitio. [!DNL Analytics] registra una pulsación cuando se da cualquiera de las siguientes condiciones:

   * La dirección URL incluye un EF ID y un AMO ID, añadidos por Adobe Advertising a la dirección URL de la página de aterrizaje.

   * La dirección URL no contiene códigos de seguimiento, pero el código JavaScript de Adobe Advertising detecta un clic en los últimos dos minutos.

![Adobe Advertising basado en vistas [!DNL Analytics] integración](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Adobe Advertising basado en vistas [!DNL Analytics] integración*

![Adobe Advertising de clic basado en URL [!DNL Analytics] integración](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Adobe Advertising de clic basado en URL [!DNL Analytics] integración*

## ID de EF de Adobe Advertising

El EF ID es un token único que utiliza el Adobe Advertising para asociar la actividad con un clic en línea o una exposición de publicidad. El ID de EF se almacena en [un [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (reservado [!DNL eVar]) (ID de EF de Adobe Advertising) y rastrea cada clic o exposición de publicidad en el nivel de navegador o dispositivo individual. Los ID de EF actúan principalmente como claves para el envío [!DNL Analytics] datos al Adobe Advertising para informes y optimización de ofertas dentro del Adobe Advertising.

### Formato de ID de EF

>[!NOTE]
>
>Los ID de EF distinguen entre mayúsculas y minúsculas. Si un [!DNL Analytics] La implementación fuerza el seguimiento de URL a minúsculas y, a continuación, el Adobe Advertising no reconocerá el EF ID. Esto afectará a las ofertas de Adobes Advertising y a los informes, pero no a los informes de Adobes Advertising dentro de [!DNL Analytics].

#### [!DNL Google Ads] anuncios de búsqueda

```
{gclid}:G:s
```

donde:

* `gclid` es el [!DNL Google Click ID] (GCLID).
* `s` es el tipo de red (&quot;s&quot; para la búsqueda).

#### Anuncios de búsqueda de Microsoft Advertising

```
{msclkid}:G:s
```

donde:

* `msclkid` es el [!DNL Microsoft Click ID] (MSCLKID).
* `s` es el tipo de red (&quot;s&quot; para la búsqueda).

#### Mostrar anuncios y anuncios de búsqueda en otros motores de búsqueda

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

donde:

* &lt;*ID de visitante de Adobe Advertising*> es un ID único por visitante (como UhKVaAAABCkJ0mDt). También se denomina *ID de internauta*.

* &lt;*timestamp*> es la hora con el formato AAAAMMDDHHMMSS (como 20190821192533 para el año 2019, mes 08, día 21, hora 19:25:33).

* &lt;*tipo de canal*> es el tipo de canal responsable del clic o la exposición:

   * `d` DSP para hacer clic en un anuncio en pantalla de la (pulsación en pantalla)
   * `i` DSP para obtener una impresión de un anuncio en pantalla de la aplicación de la impresión de un anuncio en pantalla (visualización completa)
   * `s` para hacer clic en un anuncio de búsqueda (pulsación de búsqueda).

Ejemplo `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### El Dimension EF ID en [!DNL Analytics]

Entrada [!DNL Analytics] de, puede encontrar datos de EF ID buscando la variable [!UICONTROL EF ID] dimensión y uso del [!UICONTROL EF ID Instance] métrica.

Los EF ID están sujetos al límite de 500 000 identificadores únicos en Analysis Workspace. Una vez que se alcanza el valor de 500 000, todos los nuevos códigos de seguimiento se registran con el título de un elemento de línea &quot;[!UICONTROL Low Traffic].&quot; Debido a la posibilidad de que falte fidelidad en los informes, los EF ID no se clasifican y no debe utilizarlos para segmentos o informes en [!DNL Analytics].

## Adobe Advertising de ID de AMO {#amo-id}

El ID de AMO realiza un seguimiento de cada combinación de publicidad única en un nivel menos granular y se utiliza para [!DNL Analytics] clasificación de datos e ingesta de métricas de publicidad (como impresiones, clics y costes) de Adobes Advertising. El ID de AMO se almacena en un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o la dimensión rVar (ID de AMO) y se utiliza exclusivamente para la creación de informes en [!DNL Analytics].

El ID de AMO también se denomina `s_kwcid`, que a veces se pronuncia como &quot;[!DNL the squid].&quot;

### Formas de implementar el ID de AMO {#amo-id-implement}

El parámetro se añade a las direcciones URL de seguimiento de una de las siguientes maneras:

* (Recomendado) Se implementa la función de inserción del lado del servidor.

   * DSP Clientes de: El servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final ve un anuncio en pantalla con el píxel de Adobe Advertising.

   * Clientes de Search, Social y Commerce:

      * Para [!DNL Google Ads] y [!DNL Microsoft® Advertising] cuentas con el [!UICONTROL Auto Upload] con la configuración habilitada para la cuenta o campaña, el servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final hace clic en un anuncio con el píxel de Adobe Advertising.

      * Para otras redes de publicidad, o [!DNL Google Ads] y [!DNL Microsoft® Advertising] cuentas con el [!UICONTROL Auto Upload] configuración deshabilitada, agregue manualmente el parámetro a la [parámetros de adición de nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que lo anexan a las direcciones URL base.

* La función de inserción del lado del servidor no está implementada:

   * DSP clientes de:

      * Para [!DNL Flashtalking] Para agregar etiquetas, inserte manualmente macros adicionales por &quot;[Añadir [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Para [!DNL Google Campaign Manager 360] Para agregar etiquetas, inserte manualmente macros adicionales por &quot;[Añadir [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Clientes de Search, Social y Commerce:

      * Para ([!DNL Google Ads] y [!DNL Microsoft® Advertising]), agregue manualmente el parámetro de ID de AMO a los sufijos de la página de aterrizaje. De ser posible, haga lo siguiente en [nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} a menos que sea necesario un seguimiento diferente para los componentes de cuenta individuales.

      * Para los anuncios de todas las demás redes de publicidad, añada manualmente el parámetro de ID de AMO a su [parámetros de adición de nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que lo anexan a las direcciones URL base.

Para implementar la función de inserción del lado del servidor o para determinar la mejor opción para su empresa, hable con el equipo de cuenta de Adobe.

### Formatos de ID de AMO {#amo-id-formats}

#### Formato de ID de AMO para [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

donde:

* `AC` indica el canal de visualización.

* `{TM_AD_ID}` es la clave de anuncio alfanumérica generada por el Adobe Advertising. Se utiliza como identificador único de un anuncio y sirve como clave para traducir metadatos de entidades de Adobe Advertising a legibles [!DNL Analytics] dimensiones.

* `{TM_PLACEMENT_ID}` es la clave de ubicación alfanumérica generada por el Adobe Advertising. Se utiliza como identificador único de una ubicación y sirve como clave para traducir metadatos de entidades de Adobe Advertising a legibles [!DNL Analytics] dimensiones.

Ejemplo de ID de AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### Formatos de ID de AMO para anuncios de Search, Social y Commerce

Los parámetros varían según la red de anuncios, pero los siguientes parámetros son comunes a todos los operadores:

* `AL` indica el canal de búsqueda. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` es un ID de usuario único asignado al anunciante.

* `{sid}` se sustituye por el ID numérico de la cuenta de red de publicidad del anunciante: *3* para [!DNL Google Ads], *10* para [!DNL Microsoft Advertising], *45* para [!DNL Meta], *86* para [!DNL Yahoo! Display Network], *87* para [!DNL Naver], *88* para [!DNL Baidu], *90* para [!DNL Yandex], *94* para [!DNL Yahoo! Japan Ads], *105* para [!DNL Yahoo Native] (obsoleto), o *106* para [!DNL Pinterest] (obsoleto).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

donde:

* `{creative}` es el ID numérico único de la red de publicidad para el creativo.
* `{placement}` es el sitio web en el que se hizo clic en el anuncio.
* `{keywordid}` es el ID numérico único de la red de anuncios para la palabra clave que activó el anuncio.

##### [!DNL Google Ads]

Estos incluyen campañas de compra que utilizan [!DNL Google Merchant Center].

* Cuentas que utilizan el formato de ID de AMO más reciente, que admite la creación de informes de nivel de campaña y de grupo de publicidad para campañas Máximo rendimiento de, así como campañas de borradores y experimentos:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Otras cuentas:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

donde:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` es el [!DNL Google Ads] ID numérico único del creativo.
* `{matchtype}` es el tipo de coincidencia de la palabra clave que activó el anuncio: `e` para obtener información exacta, `p` para la frase, o `b` para amplia.
* `{placement}` es el nombre de dominio del sitio web en el que se hizo clic en el anuncio. Hay un valor disponible para los anuncios de campañas con objetivos de ubicación y para los anuncios de campañas con objetivos de palabras clave que se muestran en sitios de contenido.
* `{network}` indica la red desde la que se produjo el clic: `g` para [!DNL Google] búsqueda (solo para anuncios segmentados por palabras clave), `s` para un socio de búsqueda (solo para anuncios segmentados por palabras clave), o `d` para la red de visualización (para anuncios con objetivo de palabras clave o con objetivo de ubicación).
* `{product_partition_id}` es el ID numérico único de la red de publicidad para el grupo de productos utilizado con los anuncios de productos.
* `{keyword}` es la palabra clave específica que activó el anuncio (en sitios de búsqueda) o la palabra clave que mejor coincide (en sitios de contenido).
* `{campaignid}` es el ID numérico único de la red de publicidad para la campaña.
* `{adgroupid}` es el ID numérico único de la red de anuncios para el grupo de anuncios.

>[!NOTE]
>
>* Para los anuncios dinámicos de búsqueda, {keyword} se rellena con el destino automático.
>* Cuando se genera un seguimiento para [!DNL Google] anuncios de compra, un parámetro de ID de producto, `{adwords_producttargetid}`, se inserta antes del parámetro keyword. El parámetro de ID de producto no aparece en la [!DNL Google Ads] parámetros de seguimiento a nivel de cuenta y de campaña.
>* Para utilizar el código de seguimiento de ID de AMO más reciente, consulte[Actualización del código de seguimiento de ID de AMO para un [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Buscar campañas:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Campañas de compra (con [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campañas de Audience Network:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

donde:

* `{AdId}` es el ID numérico único de la red de publicidad para el creativo.
* `{OrderItemId}` es el ID numérico de la red de publicidad para la palabra clave.
* `{CriterionId}` es el ID numérico de la red de publicidad para el grupo de productos utilizado con los anuncios de productos.

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

donde:

* `{creative}` es el ID numérico único de la red de publicidad para el creativo.
* `{matchtype}` es el tipo de coincidencia de la palabra clave que activó el anuncio: `be` para obtener información exacta, `bp` para la frase, o `bb` para amplia.
* `{network}` indica la red desde la que se produjo el clic: `n` para nativo o `s` para la búsqueda.
* `{keyword}` es la palabra clave que activó el anuncio.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

donde:

* `{ad_id}` es el ID numérico único de la red de publicidad para el creativo.
* `{source_type}` es el tipo de sitio en el que se ha mostrado el anuncio: *b* para la búsqueda, *c* para el contexto (contenido), o *ct* para la categoría.
* `{phrase_id}` es el ID numérico de la red de publicidad para la palabra clave.

### DIMENSION de ID de AMO en [!DNL Analytics]

En los informes de Analytics, puede encontrar datos de ID de AMO buscando el [!UICONTROL AMO ID] dimensión y uso del [!UICONTROL AMO ID Instance] métrica. El [!UICONTROL AMO ID] contiene todos los valores de ID de AMO capturados, mientras que la dimensión [!UICONTROL AMO ID Instance] Esta métrica indica la frecuencia con la que el sitio capturó un valor de ID de AMO. Por ejemplo, si se hizo clic en el mismo anuncio de búsqueda cuatro veces, pero Analytics rastreó siete entradas de sitio, [!UICONTROL AMO ID Instance] sería siete (7) y [!UICONTROL Clicks] sería de cuatro (4).

Para cualquier informe o auditoría dentro de [!DNL Analytics]Sin embargo, se recomienda utilizar el ID de AMO junto con su instancia correspondiente. Para obtener más información, consulte &quot;[Validación de datos para [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; en &quot;Variaciones de datos previstas entre [!DNL Analytics] y Adobe Advertising&quot;.

## Acerca de las clasificaciones de Analytics

Entrada [!DNL Analytics], a [clasificación](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) es un fragmento de metadatos para un código de seguimiento determinado, como Cuenta, Campaña o Anuncio. Adobe Advertising clasifica los datos de Adobe Advertising sin procesar mediante clasificaciones para que pueda mostrarlos de diferentes maneras (por ejemplo, por tipo de anuncio o campaña) al generar informes. Las clasificaciones forman la base de los informes de Adobe Advertising en [!DNL Analytics] y se pueden usar con las métricas de AMO, como [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], y [!UICONTROL AMO Clicks], así como con eventos en el sitio personalizados y estándar como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], y [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Variaciones de datos previstas entre [!DNL Analytics] y ADOBE ADVERTISING](data-variances.md)
