---
title: Datos de [!DNL Analytics] en Adobe Advertising
description: Datos de [!DNL Analytics] en Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
TQID: https://experienceleague.adobe.com/Op96b-n8lH2vLwBfUjlJdunp65Y5o2-gYxaEWFwH2m8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 345
ht-degree: 0%

---

# Datos de [!DNL Analytics] en Adobe Advertising

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

## Segmentos de Analytics

Todos los segmentos creados en [!DNL Analytics] y publicados en Adobe CX Enterprise (anteriormente Adobe) (Experience Cloud).

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
* [Métrica [!UICONTROL Bounces]](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [Métrica [!UICONTROL Visits]](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: el número de veces que [!DNL Analytics] recopiló un(a) [!UICONTROL EF ID].

## Métricas de conversión

[!DNL Analytics] pasa diariamente las métricas de conversión a Adobe Advertising.

### Métricas de conversión estándar

* [Métrica [!UICONTROL Revenue]](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [Métrica [!UICONTROL Orders]](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [Métrica [!UICONTROL Units]](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [Métrica [!UICONTROL Carts]](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [Métrica [!UICONTROL Cart Views]](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [Métrica [!UICONTROL Checkouts]](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [Métrica [!UICONTROL Cart Additions]](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [Métrica [!UICONTROL Cart Removals]](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

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
