---
title: Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics
description: Haga referencia a las métricas y dimensiones de Adobe Advertising que están disponibles en Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 6e22ead8f91d87cce3f104635e95a2dcab03bc3a
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics

*Solo anunciantes con una integración Adobe Advertising-Customer Journey Analytics*

*característica de Beta*

Adobe Advertising pasa diariamente métricas y dimensiones de tráfico a [!DNL Customer Journey Analytics]. [!DNL Web SDK] captura las pulsaciones y visualizaciones de Adobe Advertising en tiempo real y las pasa a Customer Journey Analytics.

## Métricas de tráfico de Adobe Advertising

<!-- Verify column names -->

En la tabla siguiente:

* &quot;Nombre de campo XDM&quot; es el nombre de campo en Adobe Experience Platform.

* &quot;Nombre para mostrar del campo XDM&quot; indica el nombre para mostrar en Customer Journey Analytics.

| Nombre del campo Adobe Advertising | Nombre de campo XDM | Nombre para mostrar del campo XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Fecha | Fecha | Todo | |
| ID de AMO | oblicuo | ADOBE ADVERTISING ID | Todo |
| Impresiones de AMO | adobe_advertising_impressions | Impresiones de Adobe Advertising | Todo |
| Clics de AMO | adobe_advertising_clicks | Clics en Adobe Advertising | Todo |
| Coste de AMO | adobe_advertising_cost | Coste de Adobe Advertising | Todo |
| Código de divisa | moneda | Moneda | Todo |
| Vistas de AMO | adobe_advertising_views | Vistas de Adobe Advertising | Ad Cloud DSP |
| Vistas de AMO 25% completadas | adobe_advertising_views_25_pct | Vistas de Adobe Advertising 25 % completadas | Ad Cloud DSP |
| Vistas de AMO completadas al 50 % | adobe_advertising_views_50_pct | Vistas de Adobe Advertising 50 % completadas | Ad Cloud DSP |
| Vistas de AMO completadas en un 75 % | adobe_advertising_views_75_pct | Vistas de Adobe Advertising completadas en un 75 % | Ad Cloud DSP |
| Vistas de AMO 100% completadas | adobe_advertising_views_100_pct | Vistas de Adobe Advertising 100 % completadas | Ad Cloud DSP |
| Minutos de AMO vistos | adobe_advertising_minutes_views | Minutos de Adobe Advertising vistos | Ad Cloud DSP |
| Impresiones visibles de AMO | adobe_advertising_viewable_impressions | Impresiones visibles de Adobe Advertising | Ad Cloud DSP |
| Impresiones no visibles de AMO | adobe_advertising_not_viewable_impressions | Impresiones no visibles de Adobe Advertising | Ad Cloud DSP |
| Impresiones mensurables de AMO | adobe_advertising_mensurable_impressions | Impresiones mensurables de Adobe Advertising | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Dimensiones de Adobe Advertising

En la tabla siguiente:

* &quot;Nombre de campo XDM&quot; es el nombre de campo en Adobe Experience Platform.

* &quot;Nombre para mostrar del campo XDM&quot; indica el nombre para mostrar en Customer Journey Analytics.

| Nombre del campo Adobe Advertising | Nombre de campo XDM | Nombre para mostrar del campo XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Clave | oblicuo | ADOBE ADVERTISING ID |
| Plataforma de publicidad | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |
| Cuenta | adobe_advertising_account | Cuenta de Adobe Advertising |
| Campaign | adobe_advertising_campaign | Adobe Advertising Campaign |
| Grupo de publicidad | adobe_advertising_ad_group | Grupo de publicidad de Adobe Advertising |
| Palabra clave | adobe_advertising_keyword | Palabra clave Adobe Advertising |
| Anuncio | adobe_advertising_ad | Adobe Advertising Ad |
| Ubicación | adobe_advertising_placement | Ubicación de Adobe Advertising |
| Tipo de coincidencia | adobe_advertising_match_type | Tipo de coincidencia de Adobe Advertising |
| Título del anuncio | adobe_advertising_ad_title | Título de anuncio de Adobe Advertising |
| Descripción del anuncio | adobe_advertising_ad_description | Descripción del anuncio de Adobe Advertising |
| URL de destino del anuncio | adobe_advertising_ad_destination_url | URL de destino de anuncio de Adobe Advertising |
| URL mostrada de anuncio | adobe_advertising_ad_display_url | URL mostrada de anuncio de Adobe Advertising |
| Dispositivo | adobe_advertising_device | Dispositivo Adobe Advertising |
| MatchType de palabra clave | adobe_advertising_keyword_matchtype | Adobe Advertising Keyword MatchType |
| Red | adobe_advertising_network | Red de Adobe Advertising |
| Tipo de anuncio | adobe_advertising_ad_type | Tipo de anuncio de Adobe Advertising |
| Segmentación de productos | adobe_advertising_product_target | Adobe Advertising Product Target |
| Tipo de aterrizaje | adobe_advertising_landing_type | Tipo de aterrizaje de Adobe Advertising |
| Optimización | adobe_advertising_optimization | Optimización de Adobe Advertising |

>[!MORELIKETHIS]
>
>* [Información general](overview.md)
>* [Requisitos previos](prerequisites.md)
>* [ID de Adobe Advertising usados por [!DNL Customer Journey Analytics]](ids.md)
