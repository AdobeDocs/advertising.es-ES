---
title: '[!DNL LY Ads] configuración de campaña'
description: Hacer referencia a la configuración de  [!DNL LY Ads] campañas.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# [!DNL LY Ads] configuración de campaña

## \[Parte superior de la página]

**[!UICONTROL Campaign Name]:** Un nombre de campaña único en la cuenta.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *En pausa*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

## Ficha [!UICONTROL Basic Settings]

*Solo nuevas campañas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign Type]:** Dónde colocar anuncios: la única opción es *[!UICONTROL Search Network Only]* para mostrar anuncios de texto en la red de búsqueda.

## Ficha [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** El presupuesto, que es la cantidad que desea gastar diariamente, en promedio. El presupuesto diario mínimo es de 100 yenes.

Si asigna esta campaña a un portafolio para el que los límites presupuestarios de la campaña se ajustan automáticamente, según las condiciones de búsqueda, puede gastar más o menos que el presupuesto especificado en un período determinado.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-yahoo-japan.md}}

## Ficha [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-yahoo-japan.md}}

### [!UICONTROL Campaign Tracking]

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
