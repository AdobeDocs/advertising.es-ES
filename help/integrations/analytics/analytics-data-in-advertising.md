---
title: '[!DNL Analytics] Datos en Adobe Advertising'
description: '[!DNL Analytics] Datos en Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Analytics] Datos en Adobe Advertising

*Anunciantes con solo integración de Adobe Advertising-Adobe Analytics*

## Segmentos de Analytics

Todos los segmentos creados en [!DNL Analytics] y publicado en el Experience Cloud.

Los nuevos segmentos tardan entre 24 y 48 horas en aparecer en el Adobe Advertising. Las actualizaciones de los segmentos existentes se sincronizan en unas ocho horas.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Métricas de participación del sitio

>[!NOTE]
>
>* [!DNL Analytics] pasa eventos para el EF ID [!DNL eVar] en el Adobe Advertising.  La integración predeterminada no admite el envío de métricas calculadas u otras dimensiones ([!DNL eVars]) en Adobe Advertising. Sin embargo, si la métrica calculada se puede capturar por completo en un evento personalizado, el Adobe Advertising puede introducir el evento personalizado.
>* [!DNL Analytics] pasa datos a Adobe Advertising cada hora.

* [!UICONTROL Timespent_secs_1stvisit]: el número de segundos empleados en el sitio durante la primera visita del visitante.
* [!UICONTROL Timespent_secs_total]: El número total de segundos empleados en el sitio en todas las visitas dentro de la ventana retrospectiva de clics.
* [!UICONTROL Pageviews_1stvisit]: el número de vistas de página en el sitio durante la primera visita del visitante.
* [!UICONTROL Pageviews_total]: El número total de vistas de página en el sitio en todas las visitas dentro de la ventana retrospectiva de clics.
* [[!UICONTROL Bounces] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: el número de veces que [!DNL Analytics] ha recopilado un [!UICONTROL EF ID].

## Métricas de conversión

[!DNL Analytics] pasa métricas de conversión a Adobe Advertising diariamente.

### Métricas de conversión estándar

* [[!UICONTROL Revenue] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Métricas de conversión personalizadas

Estas métricas son específicas del grupo de informes, por lo que las métricas disponibles varían para cada cliente y grupo de informes.

### Métricas de conversión personalizadas creadas desde [!DNL eVars] y [!DNL Props]

Las métricas disponibles varían para cada cliente. Consulte &quot;[Crear métricas de conversión desde Adobe Analytics [!DNL eVars] y [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Métricas de conversión reservadas

Estas métricas son específicas del grupo de informes, por lo que las métricas disponibles varían para cada cliente y grupo de informes.

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Métricas de Adobe Advertising en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
