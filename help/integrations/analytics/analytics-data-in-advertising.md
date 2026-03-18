---
title: Datos de [!DNL Analytics] en Adobe Advertising
description: Datos de [!DNL Analytics] en Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Datos de [!DNL Analytics] en Adobe Advertising

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

## Segmentos de Analytics

Todos los segmentos creados en [!DNL Analytics] y publicados en Experience Cloud.

Los nuevos segmentos tardan entre 24 y 48 horas en aparecer en Adobe Advertising. Las actualizaciones de los segmentos existentes se sincronizan en unas ocho horas.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Métricas de participación del sitio

>[!NOTE]
>
>* [!DNL Analytics] pasa eventos para el EF ID [!DNL eVar] a Adobe Advertising.  La integración predeterminada no admite el envío de métricas calculadas u otras dimensiones ([!DNL eVars]) a Adobe Advertising. Sin embargo, si la métrica calculada se puede capturar por completo en un evento personalizado, Adobe Advertising puede introducir el evento personalizado.
>* [!DNL Analytics] pasa datos a Adobe Advertising cada hora.

* [!UICONTROL Timespent_secs_1stvisit]: número de segundos empleados en el sitio durante la primera visita del visitante.
* [!UICONTROL Timespent_secs_total]: número total de segundos empleados en el sitio en todas las visitas dentro de la ventana retrospectiva de clics.
* [!UICONTROL Pageviews_1stvisit]: número de vistas de página en el sitio durante la primera visita del visitante.
* [!UICONTROL Pageviews_total]: número total de vistas de página en el sitio en todas las visitas dentro de la ventana retrospectiva de clics.
* [[!UICONTROL Bounces] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=es)
* [[!UICONTROL Visits] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=es)
* [!UICONTROL ef_id_instances]: el número de veces que [!DNL Analytics] recopiló un(a) [!UICONTROL EF ID].

## Métricas de conversión

[!DNL Analytics] pasa diariamente las métricas de conversión a Adobe Advertising.

### Métricas de conversión estándar

* [[!UICONTROL Revenue] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=es)
* [[!UICONTROL Orders] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=es)
* [[!UICONTROL Units] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=es)
* [[!UICONTROL Carts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=es)
* [[!UICONTROL Cart Views] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=es)
* [[!UICONTROL Checkouts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=es)
* [[!UICONTROL Cart Additions] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html?lang=es)
* [[!UICONTROL Cart Removals] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=es)

### Métricas de conversión personalizadas

Estas métricas son específicas del grupo de informes, por lo que las métricas disponibles varían para cada cliente y grupo de informes.

### Métricas de conversión personalizadas creadas entre [!DNL eVars] y [!DNL Props]

Las métricas disponibles varían para cada cliente. Consulte &quot;[Crear métricas de conversión a partir de Adobe Analytics [!DNL eVars] y [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;.

### Métricas de conversión reservadas

Estas métricas son específicas del grupo de informes, por lo que las métricas disponibles varían para cada cliente y grupo de informes.

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Métricas de Adobe Advertising en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
