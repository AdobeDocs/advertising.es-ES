---
title: ID de Adobe Advertising utilizados por Customer Journey Analytics
description: ID de Adobe Advertising utilizados por Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: af60dcb4-4d1a-4097-ac30-688bd8b9f644
source-git-commit: 6e2a1c5d335806bb4e5fcbcdfb619ad387c7f7cb
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# ID de Adobe Advertising utilizados por Customer Journey Analytics

*Solo anunciantes con una integración Adobe Advertising-Adobe Customer Journey Analytics*

*Aplicable a Advertising DSP y[!DNL Advertising Search, Social, & Commerce]*

*característica de Beta*

Adobe Advertising usa dos ID para el seguimiento del rendimiento en el sitio: el *ID de EF* y el *ID de AMO*.

<!-- Rewrite for CJA:

When an ad impression occurs, Adobe Advertising creates the AMO ID and EF ID values and stores them. For click-through traffic, these IDs are included in the landing page URL using the `ef_id` and `s_kwcid` (for the AMO ID) query string parameters.

Adobe Advertising distinguishes between a click-through or view-through entry to the website using the following criteria:

* A view-through entry is captured when a user visits the site after viewing an ad but not clicking it. [!DNL Analytics] or Web SDK records a view-through if two conditions are met:

    * The visitor has no click-throughs for a [!DNL DSP] or [!DNL Search, Social, & Commerce] ad during the [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

    * The visitor has seen at least one [!DNL DSP] ad during the [impression lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc). The last impression is passed as the view-through.

* A click-through entry is captured when a site visitor clicks an ad before entering the site. [!DNL Analytics] or Web SDK captures a click-through when either of the following conditions occurs:

    * The URL includes an EF ID and AMO ID as added to the landing page URL by Adobe Advertising.

    * The URL contains no tracking codes, but the Adobe Advertising JavaScript code detects a click within the last two minutes.

![Adobe Advertising view-based [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1: Adobe Advertising view-based [!DNL Analytics] integration*

![Adobe Advertising click URL-based [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2: Adobe Advertising click URL-based [!DNL Analytics] integration*

-->

<!-- ## Adobe Advertising EF IDs -->

{{$include /help/_includes/ef-id.md}}

## ID de Adobe Advertising AMO {#amo-id}

{{$include /help/_includes/amo-id.md}}

<!-- rewrite for CJA:

### AMO ID Dimension in [!DNL Customer Journey Analytics]

In Analytics reports, you can find AMO ID data by searching for the [!UICONTROL AMO ID] dimension and using the [!UICONTROL AMO ID Instances] metric. The [!UICONTROL AMO ID] dimension houses all AMO ID values captured, whereas the [!UICONTROL AMO ID Instances] metric indicates how often an AMO ID value was captured by the site. For example, if the same search ad was clicked four times but Analytics tracked seven site entries, then [!UICONTROL AMO ID Instances] would be seven (7) and [!UICONTROL Clicks] would be four (4).

For any reporting or auditing within [!DNL Analytics], the best practice is to use the AMO ID along with its corresponding instance. For more information, see "[Click-Through Data Validation for [!DNL Analytics for Advertising]](data-variances.md#data-validation)" in "Expected Data Variances Between [!DNL Analytics] and Adobe Advertising."

-->

>[!MORELIKETHIS]
>
>* [Información general](overview.md)
>* [Requisitos previos](prerequisites.md)
>* [Configurar la recopilación de datos, la transferencia de datos y la creación de informes](set-up.md)
>* [Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics](advertising-data-in-cja.md)
