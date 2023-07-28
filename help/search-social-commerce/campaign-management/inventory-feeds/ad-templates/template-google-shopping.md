---
title: '''[!DNL Google Ads] configuración de plantillas de anuncios de compras para fuentes de inventario'
description: Haga referencia a la configuración de [!DNL Google Ads] plantillas de anuncios de compras para fuentes de inventario.
exl-id: c154e1b3-70eb-437d-80f6-abf6ac192697
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# [!DNL Google Ads] configuración de plantillas de anuncios de compras para fuentes de inventario

Utilice plantillas de anuncios de compras para configurar los anuncios de compras.

>[!NOTE]
>
>* Los siguientes caracteres están reservados para designar nombres de columna y nombres de modificador en la plantilla y, por lo tanto, están prohibidos como texto en todos los campos de atributo:  `[ ] < > `

## \[Sobre todas las fichas\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Panel izquierdo\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** (Opcional para plantillas de archivos de fuentes de cliente) La plantilla de seguimiento de nivel de campaña, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, e incrusta la dirección URL final en un parámetro. Este valor anula la configuración de nivel de cuenta, pero las plantillas de seguimiento a niveles más granulares (con palabra clave como valor más granular) anulan este valor.

Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload],&quot; use el [formato de plantilla de seguimiento para campañas de compra de Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md). Si toda la cuenta está dedicada a anuncios de compra, puede definir una plantilla de seguimiento en el nivel de cuenta.

Para redirecciones y seguimiento de terceros, introduzca un valor.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** El ID de cliente de la cuenta de comerciante cuyos productos se utilizan en la campaña.

**[!UICONTROL Sales Country]:** El país en el que se venden los productos de la campaña. Dado que los productos están asociados a países de destino, esta configuración determina qué productos se anuncian en la campaña.

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** Las redes en las que se colocan los anuncios. *[!UICONTROL Search]* ya está seleccionada. Para incluir pujas en anuncios de [!DNL Google Ads] buscar socios, active la casilla situada junto a **[!UICONTROL Search partners]**.

**[!UICONTROL Campaign Priority]:** Prioridad con la que se utiliza la campaña cuando varias campañas anuncian el mismo producto: *[!UICONTROL Low]* (la opción predeterminada para las nuevas campañas), *[!UICONTROL Medium]*, o *[!UICONTROL High]*. Cuando el mismo producto se incluye en más de una campaña, la red de anuncios utiliza primero la prioridad de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Opcional) Una plantilla de seguimiento de nivel de grupo de anuncios, que especifica todas las redirecciones de dominios de aterrizaje y parámetros de seguimiento e incrusta la dirección URL final en un parámetro. Este valor anula la configuración de nivel de cuenta y de campaña, pero las plantillas de seguimiento a niveles más granulares anulan este valor.

Para el seguimiento de conversiones de Adobe Advertising, no es necesario introducir un valor. El valor de nivel de campaña es suficiente.

Para redirecciones y seguimiento de terceros, introduzca un valor.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** El grupo de productos predeterminado con todo incluido, &quot;[!UICONTROL All products].&quot; No puede eliminar este grupo de productos principal, pero se elimina automáticamente cuando faltan todos los niveles inferiores en la fuente.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Unidades sin grupos de productos secundarios; opcional) La plantilla de seguimiento del grupo de productos, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento e incrusta la dirección URL final en una [!DNL ValueTrack] parámetro. Esta plantilla anula las plantillas de los niveles superiores.

Para el seguimiento de conversiones de Adobe Advertising, no es necesario introducir un valor. El valor de nivel de campaña es suficiente.

Para redirecciones y seguimiento de terceros, introduzca un valor.

**[!UICONTROL Initial Bid]:** La puja inicial por cada anuncio.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Automatización de la administración de anuncios mediante fuentes de inventario](../inventory-feeds-about.md)
>* [Administración de modificadores](../modifiers-manage.md)
>* [Administrar archivos de fuente de datos de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propagación de datos de fuentes mediante plantillas](../feed-data-propagate.md)
>* [Publicar datos de campaña de fuentes de inventario en redes de publicidad](../propagated-data-post.md)
