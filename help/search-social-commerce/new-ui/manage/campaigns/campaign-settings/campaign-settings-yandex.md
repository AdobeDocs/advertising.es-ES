---
title: '[!DNL Yandex] configuración de campaña'
description: Hacer referencia a la configuración de  [!DNL Yandex] campañas.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# [!DNL Yandex] configuración de campaña

## \[Parte superior de la página]

**[!UICONTROL Campaign Name]:** Un nombre de campaña único en la cuenta.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *En pausa*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

## Ficha [!UICONTROL Basic Settings]

*Solo nuevas campañas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign Type]:** Dónde colocar los anuncios:

* *[!UICONTROL Search Network Only]:* muestra anuncios de texto en la red de búsqueda. Debe especificar palabras clave para cada grupo de publicidad.

* *[!UICONTROL Search and Display Network]:* muestra anuncios de texto en la red de búsqueda y en [!DNL Yandex Advertising Network]. Para los anuncios de búsqueda, debe especificar palabras clave de búsqueda para cada grupo de anuncios. Para los anuncios en pantalla, debe especificar palabras clave para los sitios web en los que desea anunciar para cada grupo de anuncios.

* *[!UICONTROL Display Network Only]:* muestra anuncios de texto en [!DNL Yandex Advertising Network]. Para cada grupo de anuncios, debe especificar palabras clave para los sitios web en los que desea hacer publicidad.

## Ficha [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

## Ficha [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** El presupuesto, que es la cantidad que desea gastar diariamente (en promedio) o durante la duración de la campaña, según el tipo de presupuesto de la cuenta. El presupuesto mínimo es de 6.300, 10 euros o 10 dólares.

**Notas:**

* Las nuevas campañas tienen la estrategia de administración de ofertas &quot;Posición más alta disponible&quot;.

* Según las condiciones de búsqueda, si asigna esta campaña a un portafolio configurado para permitir que los límites presupuestarios de la campaña se ajusten automáticamente, puede gastar más o menos del presupuesto especificado en cualquier día, mes o duración determinados.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## Ficha [!UICONTROL Additional Campaign Information]

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (solo para [!UICONTROL EF Redirect]; solo lectura) Nivel en el que se debe realizar el seguimiento de los clics y los ingresos. Solo *[!UICONTROL Creative]* está disponible para [!DNL Yandex]; los datos se rastrean solamente en el nivel de anuncio (creativo).

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
