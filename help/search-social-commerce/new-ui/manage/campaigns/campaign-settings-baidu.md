---
title: '[!DNL Baidu] configuración de campaña'
description: Hacer referencia a la configuración de  [!DNL Baidu] campañas.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 0%

---

# [!DNL Baidu] configuración de campaña

## \[Parte superior de la página]

**[!UICONTROL Campaign Name]:** Un nombre de campaña único en la cuenta.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *En pausa*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

## Ficha [!UICONTROL Basic Settings]

*Solo nuevas campañas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign Type]:** Dónde colocar los anuncios y qué tipos de anuncios puede contener la campaña. La única opción es *Buscar solo en la red*.

## Ficha [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:**(Aplicable a las campañas destinadas a audiencias en la Unión Europea (UE)) Si la campaña contiene o no publicidad política según los requisitos para los anuncios publicados en la Unión Europea según la normativa de la UE 2024/90: *[!UICONTROL Yes]* o *[!UICONTROL No]*.

## Ficha [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]:** Estrategia de oferta para la campaña:

* *[!UICONTROL Maximize Conversions]:* La red de anuncios (no Search, Social y Commerce) optimiza las ofertas para maximizar las conversiones. Opcionalmente, escriba **[!UICONTROL Target CPA]** (costo por adquisición). **Nota:** Utilice esta opción para campañas en portafolios con optimización de nivel de campaña. En portafolios con optimización de nivel de campaña, Search, Social y Commerce optimizan la CPA de Target.

* *[!UICONTROL Maximize Conversion Value]:* La red de anuncios (no Buscar, Social ni Commerce) optimiza las ofertas para maximizar el valor de conversión. Opcionalmente, escriba un **[!UICONTROL Target Return on Ad Spend]** (ROAS) como porcentaje. **Nota:** Utilice esta opción para campañas en portafolios con optimización de nivel de campaña. En portafolios con optimización en el nivel de campaña, Search, Social y Commerce optimizan el ROAS de Target.

## Ficha [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** El idioma del anuncio, que debe coincidir con el idioma de los sitios en los que puede aparecer el anuncio. La red de anuncios determina el idioma de un usuario a partir de diversas señales, incluidas la consulta del usuario, el país del editor y la configuración de idioma del usuario.

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## Ficha [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### Ficha [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (solo para [!UICONTROL EF Redirect]) El nivel en el que se debe realizar el seguimiento de los clics y los ingresos agregando una redirección (cuando sea relevante) y anexando parámetros a las direcciones URL relevantes:

* *[!UICONTROL Keyword]:* Para realizar el seguimiento de los datos solamente en el nivel de palabra clave.

* *[!UICONTROL Creative]:* Para rastrear datos solamente en el nivel de anuncio (creativo).

* *[!UICONTROL Creative and Keyword]:* Para rastrear datos en los niveles de anuncio (creativo) y palabra clave.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** Agrega un parámetro de URL a los anuncios de la cuenta o campaña para el seguimiento de conversiones.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [Administrar campañas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
