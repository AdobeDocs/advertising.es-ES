---
title: ID de Adobe Advertising usados por  [!DNL Analytics]
description: ID de Adobe Advertising usados por  [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: dbbba0bd75f3b1003325b665d06bce003c5ee054
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 0%

---

# ID de Adobe Advertising usados por [!DNL Analytics]

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

*Aplicable a Advertising DSP y[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising usa dos ID para el seguimiento del rendimiento en el sitio: el *ID de EF* y el *ID de AMO*.

Cuando se produce una impresión de un anuncio, Adobe Advertising crea los valores de ID de AMO e ID de EF y los almacena. Cuando un visitante que ha visto un anuncio entra al sitio sin hacer clic en un anuncio, [!DNL Analytics] llama a estos valores desde Adobe Advertising a través del código de JavaScript [!DNL Analytics for Advertising]. Para el tráfico de visualización, [!DNL Analytics] genera un identificador suplementario (`SDID`), que se usa para unir el ID de EF y el ID de AMO en [!DNL Analytics]. Para el tráfico de clics, estos identificadores se incluyen en la dirección URL de la página de aterrizaje usando los parámetros de cadena de consulta `ef_id` y `s_kwcid` (para el ID de AMO).

Adobe Advertising distingue entre una entrada de pulsaciones o visualizaciones al sitio web según los siguientes criterios:

* Se registra una entrada de visualización cuando un usuario visita el sitio después de ver un anuncio, pero sin hacer clic en él. [!DNL Analytics] registra una visualización si se cumplen dos condiciones:

   * El visitante no tiene pulsaciones para un anuncio de [!DNL DSP] o [!DNL Search, Social, & Commerce] durante la [ventana retrospectiva de clics](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * El visitante ha visto al menos un anuncio de [!DNL DSP] durante la [ventana retrospectiva de impresiones](/help/integrations/analytics/prerequisites.md#lookback-a4adc). La última impresión se pasa como la visualización.

* Se captura una entrada de pulsación cuando un visitante del sitio hace clic en un anuncio antes de entrar en el sitio. [!DNL Analytics] registra una pulsación cuando se da cualquiera de las siguientes condiciones:

   * La dirección URL incluye un EF ID y un AMO ID, tal como Adobe Advertising lo agregó a la dirección URL de la página de aterrizaje.

   * La dirección URL no contiene códigos de seguimiento, pero el código JavaScript de Adobe Advertising detecta un clic en los últimos dos minutos.

![Integración de [!DNL Analytics] basada en la vista de Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: integración [!DNL Analytics] basada en la vista de Adobe Advertising*

![Integración de [!DNL Analytics] basada en URL de clic de Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Adobe Advertising hace clic en la integración [!DNL Analytics] basada en URL*

## ID de Adobe Advertising EF

El EF ID es un token único que Adobe Advertising utiliza para asociar la actividad con un clic en línea o una exposición de publicidad. El EF ID se almacena en la dimensión [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (reservado [!DNL eVar]) (Adobe Advertising EF ID) y rastrea cada clic o exposición de anuncio en el nivel de navegador o dispositivo individual. Los EF ID actúan principalmente como claves para enviar datos de [!DNL Analytics] a Adobe Advertising para la creación de informes y la optimización de ofertas en Adobe Advertising.

### Formato de ID de EF

>[!NOTE]
>
>Los ID de EF distinguen entre mayúsculas y minúsculas. Si una implementación de [!DNL Analytics] obliga al seguimiento de URL a usar minúsculas, Adobe Advertising no reconocerá el EF ID. Esto afecta las ofertas y los informes de Adobe Advertising, pero no afecta a los informes de Adobe Advertising dentro de [!DNL Analytics].

#### [!DNL Google Ads] anuncios de búsqueda

```
{gclid}:G:s
```

donde:

* `gclid` es [!DNL Google Click ID] (GCLID).
* `s` es el tipo de red (&quot;s&quot; para la búsqueda).

#### [!DNL Microsoft Advertising] anuncios de búsqueda

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

* &lt;*timestamp*> es la hora con formato AAAAMMDDHHMMSS (como 20190821192533 para el año 2019, mes 08, día 21, hora 19:25:33).

* &lt;*tipo de canal*> es el tipo de canal responsable del clic o la exposición:

   * `d` por hacer clic en un anuncio en pantalla de DSP (pulsación en pantalla)
   * `i` para una impresión de un anuncio en pantalla de DSP (visualización completa)
   * `s` para un clic en un anuncio de búsqueda (pulsación de búsqueda).

Ejemplo `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### El Dimension EF ID en [!DNL Analytics]

En [!DNL Analytics] informes, puede encontrar datos de EF ID buscando la dimensión [!UICONTROL EF ID] y usando la métrica [!UICONTROL EF ID Instance].

Los EF ID están sujetos al límite de 500 000 identificadores únicos en Analysis Workspace. Una vez que se alcanza el valor de 500.000, todos los nuevos códigos de seguimiento se incluyen en el título de un elemento de línea &quot;[!UICONTROL Low Traffic]&quot;. Debido a la posibilidad de que falte fidelidad en los informes, los EF ID no se clasifican y no debe utilizarlos para segmentos o informes en [!DNL Analytics].

## ID de Adobe Advertising AMO {#amo-id}

El ID de AMO realiza un seguimiento de cada combinación de anuncios únicos en un nivel menos granular y se usa para la clasificación de datos [!DNL Analytics] y la ingesta de métricas de publicidad (como impresiones, clics y costes) de Adobe Advertising. El identificador de AMO se almacena en una dimensión [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o rVar (identificador de AMO) y se usa exclusivamente para generar informes en [!DNL Analytics].

El identificador de AMO también se denomina `s_kwcid`, y en ocasiones se pronuncia como &quot;[!DNL squid]&quot;.

### Formas de implementar el ID de AMO {#amo-id-implement}

El parámetro se añade a las direcciones URL de seguimiento de una de las siguientes maneras:

* (Recomendado) Cuando se implementa la función de inserción del lado del servidor.

   * Clientes de DSP: El servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final ve un anuncio en pantalla con el píxel de Adobe Advertising.

   * Clientes de Search, Social y Commerce:

      * Para las cuentas de [!DNL Google Ads] y [!DNL Microsoft Advertising] con la configuración [!UICONTROL Auto Upload] habilitada para la cuenta o campaña, el servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final hace clic en un anuncio con el píxel de Adobe Advertising.

      * Para otras redes de anuncios o cuentas de [!DNL Google Ads] y [!DNL Microsoft Advertising] con la configuración de [!UICONTROL Auto Upload] deshabilitada, agregue manualmente el parámetro a los [parámetros de datos anexados de nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que lo anexan a las direcciones URL base.

* Cuando la función de inserción del lado del servidor no está implementada:

   * Clientes de DSP: el [código JavaScript](javascript.md) registra automáticamente las pulsaciones y las visualizaciones. Cuando un explorador no admite cookies de terceros, puede seguir realizando el seguimiento de las conversiones basadas en clics para los siguientes tipos de anuncios:

      * Para las etiquetas de anuncio de [!DNL Flashtalking], inserte manualmente macros adicionales por &quot;[Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de anuncio](/help/integrations/analytics/macros-flashtalking.md)&quot;. **Nota:** Este procedimiento no es necesario si su organización tiene una asociación directa con [!DNL Flashtalking] y usa macros de paso de datos para realizar el seguimiento de los parámetros de seguimiento `s_kwcid` y `ef_id` según la documentación de soporte de [!DNL Flashtalking] en [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

      * Para las etiquetas de anuncio de [!DNL Google Campaign Manager 360], inserte manualmente macros adicionales por &quot;[Anexar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de anuncio](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;.

   * Clientes de Search, Social y Commerce:

      * Para los anuncios ([!DNL Google Ads] y [!DNL Microsoft Advertising]), agregue manualmente el parámetro de ID de AMO a los sufijos de la página de aterrizaje. Lo ideal es hacerlo a [nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, a menos que sea necesario un seguimiento diferente para los componentes de cuenta individuales.

      * Para anuncios en todas las demás redes de anuncios, agrega manualmente el parámetro de ID de AMO a tus [parámetros de datos anexados a nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que lo anexan a tus URL base.

Para implementar la función de inserción del lado del servidor o para determinar la mejor opción para su empresa, hable con el equipo de cuenta de Adobe.

### Formatos de ID de AMO {#amo-id-formats}

#### Formato de ID de AMO para [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

donde:

* `AC` indica el canal de visualización.

* `{TM_AD_ID}` es la clave de anuncio alfanumérica generada por Adobe Advertising. Se utiliza como identificador único de un anuncio y sirve como clave para traducir metadatos de entidad de Adobe Advertising a dimensiones [!DNL Analytics] legibles.

* `{TM_PLACEMENT_ID}` es la clave de ubicación alfanumérica generada por Adobe Advertising. Se utiliza como identificador único de una ubicación y sirve como clave para traducir metadatos de entidad de Adobe Advertising a dimensiones [!DNL Analytics] legibles.

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

### DIMENSION de ID de AMO en [!DNL Analytics]

En los informes de Analytics, puede encontrar datos de ID de AMO buscando la dimensión [!UICONTROL AMO ID] y utilizando la métrica [!UICONTROL AMO ID Instances]. La dimensión [!UICONTROL AMO ID] aloja todos los valores de ID de AMO capturados, mientras que la métrica [!UICONTROL AMO ID Instances] indica la frecuencia con la que el sitio capturó un valor de ID de AMO. Por ejemplo, si se hizo clic cuatro veces en el mismo anuncio de búsqueda pero Analytics rastreó siete entradas de sitio, [!UICONTROL AMO ID Instances] sería siete (7) y [!UICONTROL Clicks] sería cuatro (4).

Para cualquier informe o auditoría dentro de [!DNL Analytics], la práctica recomendada es utilizar el ID de AMO junto con su instancia correspondiente. Para obtener más información, consulte &quot;[Validación de datos con clic para [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; en &quot;Variaciones de datos previstas entre [!DNL Analytics] y Adobe Advertising&quot;.

## Acerca de las clasificaciones de Analytics

En [!DNL Analytics], una [clasificación](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) es un fragmento de metadatos para un código de seguimiento determinado, como Cuenta, Campaña o Anuncio. Adobe Advertising clasifica los datos de Adobe Advertising sin procesar mediante clasificaciones para que pueda mostrarlos de diferentes maneras (por ejemplo, por tipo de anuncio o campaña) al generar informes. Las clasificaciones forman la base de los informes de Adobe Advertising en [!DNL Analytics] y se pueden usar con las métricas de AMO, como [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] y [!UICONTROL AMO Clicks], así como con eventos personalizados y estándar en el sitio, como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] y [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Variaciones de datos previstas entre [!DNL Analytics]  y Adobe Advertising](data-variances.md)
