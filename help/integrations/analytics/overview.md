---
title: Overview of [!DNL Analytics for Advertising]
description: Overview of [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
TQID: https://experienceleague.adobe.com/OHxJO1mtbzOtt5oGDJF26xSuVLG-HnRDdIGDrUH2pzk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1306
ht-degree: 0%

---

# Overview of [!DNL Analytics for Advertising]

*Advertisers with Advertising Creative, Advertising DSP, and[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integrates Adobe Analytics and Adobe Advertising to extend and enhance the capabilities of each product.

The integration allows advertisers to track click-through and view-through site interactions in their [!DNL Analytics] instances, allowing brands to see how their advertising spend leads to site engagement and critical business objectives.

In addition, Adobe Advertising can access the vast first-party data that [!DNL Analytics] collects using [!DNL Analytics] tags already on the site. This allows more robust journey management, first-party remarketing, and paid media site reporting. Adobe Advertising can further use the [!DNL Analytics] data for spend and bid optimization.

When properly employed, [!DNL Analytics for Advertising] blurs the lines between two traditional roles: advertising journey management (the act of sending users to the site through advertisements) and understanding that site engagement through web analytics.

Primary benefits:

* Send [!DNL Analytics] segments directly to Adobe Advertising for first-party site remarketing.
* Use [!DNL Analytics] custom and standard events as conversion signals for optimizing paid media advertising.
* Take advantage of [!DNL Analytics] Analysis Workspace to better understand site entry points and visit behavior.
* Enable closer collaboration between web analysts and paid media teams.
* Use persistent Adobe Advertising view-through and click-through IDs within [!DNL Analytics] to understand site engagement.
* Enhance traditional paid media reports in Analysis Workspace with custom metrics, custom dimensions, and site activity not achievable when exporting data or pixels to ad servers or other DSPs.
* Take advantage of [!DNL Analytics] code already on your website for tracking and optimization within Adobe Advertising.

>[!TIP]
>
> Vea un [vídeo de presentación de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Uso de Analytics para informes de medios de pago

[!DNL Analytics for Advertising] mejora los informes y el insight en la forma en que la publicidad impulsa el comportamiento del sitio, ya que le permite:

* Use identificadores persistentes de pulsaciones y visualizaciones de Adobe Advertising dentro de [!DNL Analytics] para comprender la participación en el sitio.
* Aproveche Analysis Workspace para comprender mejor los puntos de entrada del sitio y el comportamiento de las visitas. Puede acceder a los datos de dimensiones y eventos de medios de pago, que incluyen nombres de entidades de Adobe Advertising Campaign (hasta ubicaciones y anuncios) y sus métricas asociadas, como clics, impresiones y costes.

Para usar [!DNL Analytics] como herramienta de informes de medios de pago, su organización necesita un inicio de sesión de Adobe CX Enterprise (anteriormente Adobe Experience Cloud) con acceso a Analysis Workspace. Su equipo de Adobe Advertising le ayudará a asignar los datos de Adobe Advertising a grupos de informes individuales en Analysis Workspace. Puede enviar datos de Adobe Advertising a cualquier grupo de informes, pero debe tener en cuenta los grupos de informes que se han asignado a Adobe Advertising y los que no. En función del grupo de informes, esto puede cambiar los datos de los informes.

[Los Adobe Advertising ID dentro de [!DNL Analytics]](ids.md) funcionan como otros [!DNL eVars], con una caducidad personalizada y persistente. De forma predeterminada, la ventana retrospectiva de atribución se establece en 60 días durante la implementación de Adobe Advertising. Para cambiar esta configuración, colabore con su equipo de cuenta de Adobe.

Las dimensiones de Adobe Advertising se anexan con el sufijo &quot;(AMO ID)&quot; (como &quot;Tipo de anuncio (AMO ID)&quot;). Consulte &quot;[Métricas de Adobe Advertising en Analysis Workspace](advertising-metrics-in-analytics.md)&quot; para obtener una lista de las dimensiones disponibles.

>[!NOTE]
>
> Cuando vea datos de Adobe Advertising (o cualquier conjunto de datos) en [!DNL Analytics], tenga en cuenta que las métricas y los informes se basan en las reglas establecidas en [!DNL Analytics]. Los datos podrían ser diferentes a los que se ven en otros sistemas de informes, como los informes de servidores de publicidad, [!DNL DSP] o los informes de motores de búsqueda. Para comprender las diferencias de datos en [!DNL Analytics], necesita saber cuándo caducan los datos de [!DNL eVar], qué define una visita, qué se considera atribución de último contacto frente a atribución de persistencia total y otros factores. Para obtener más información, consulte [Variaciones de datos previstas entre [!DNL Analytics]  y Adobe Advertising](data-variances.md).

## Uso de Analytics para impulsar campañas y portafolios de Adobe Advertising

Sin requerir píxeles adicionales, [!DNL Analytics for Advertising] permite una mejor optimización y una segmentación de audiencia más sencilla al enviar dos señales principales a Adobe Advertising:

* Métricas de conversión que se utilizarán como señales de oferta:
   * métricas estándar, como [!UICONTROL Revenue] y [!UICONTROL Cart Views].
   * métricas de participación del sitio, como las métricas de vista de página y visita.
   * métricas de ingresos personalizadas.
   * métricas de ingresos reservadas.
* Segmentos creados en [!DNL Analytics] y publicados en CX Enterprise.

  Puede usar [!DNL Analytics] segmentos para el redireccionamiento de sitios de origen en [!DNL DSP], [!DNL Creative] y anuncios de búsqueda de pago.

  ([!DNL Search, Social, & Commerce] solamente) Los anunciantes con [!DNL Analytics] pero no Audience Manager también pueden crear audiencias basadas en etiquetas del sitio web de Google (listas de remarketing) y audiencias coincidentes de clientes (listas de clientes) a partir de [!DNL Analytics] segmentos que se comparten con CX Enterprise.

### Métricas de conversión del sitio como señales de oferta

Puede usar sus eventos estándar y eventos personalizados de [!DNL Analytics] para crear objetivos ponderados en Adobe Advertising. Los objetivos informan las decisiones de oferta de sus paquetes de [!DNL DSP] y portafolios de Search, Social y Commerce.

Para las campañas [!DNL Google Ads] y [!DNL Google Microsoft Advertising] en portafolios híbridos de Search, Social y Commerce, puede, opcionalmente, cargar los objetivos, incluidos los eventos [!DNL Analytics] de los objetivos, directamente en las redes de anuncios, donde estarán disponibles como acciones de conversión para los objetivos de conversión personalizados de nivel de cuenta y de campaña.

>[!NOTE]
>
> No puede asignar métricas calculadas de [!DNL Analytics] a Adobe Advertising.

Su equipo de Adobe Advertising le ayudará a identificar y asignar los eventos aplicables al rendimiento de los medios de pago en Adobe Advertising.

Consulte &quot;[Métricas de Analytics en Adobe Advertising](analytics-data-in-advertising.md)&quot; para obtener una lista de las métricas disponibles.

### Segmentos de Analytics para redireccionamiento de sitios

Adobe Advertising puede ingerir [!DNL Analytics] segmentos con fines de remarketing para los anuncios [!DNL Creative], [!DNL DSP] y [!DNL Search, Social, & Commerce] mediante la integración nativa de audiencias de CX Enterprise entre [!DNL Analytics] y CX Enterprise.

Para acceder a los segmentos de [!DNL Analytics], una cuenta de anunciante debe habilitar el [servicio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html). Cuando el servicio de ID está habilitado, todos los segmentos de CX Enterprise están disponibles en Adobe Advertising en cuanto se procesan. Los segmentos de CX Enterprise incluyen los segmentos creados en [!DNL Analytics] y publicados en CX Enterprise, los segmentos creados en Adobe Audience Manager, los segmentos creados en CX Enterprise con [!DNL People core service] y los segmentos creados en Adobe Experience Platform y enviados a Adobe Advertising mediante Audience Manager.

[!DNL Analytics] segmentos están disponibles en un plazo de 24 horas y se actualizan diariamente.

Para obtener más información sobre el servicio de audiencias de CX Enterprise, consulte [Audiencias de CX Enterprise](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Ejemplos de cómo utilizar la integración {#integration-examples}

### Uso de datos de Adobe Advertising en Analysis Workspace

Para obtener información sobre cómo usar los datos de Adobe Advertising para crear informes visuales en Analysis Workspace, vea el vídeo &quot;[Introducción a Workspace y Creación de informes](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;.

#### Uso de conversiones de visualización de TV conectada en informes

*Solo usuarios de Advertising DSP*

Puede medir la efectividad de funnel completo de sus campañas de TV conectadas (CTV) vinculando la exposición de anuncios en dispositivos CTV a conversiones in situ. El nuevo filtro [!UICONTROL Landing Type] &quot;[!UICONTROL View-through (CTV)]&quot; divide las conversiones en filas independientes para los valores [!UICONTROL Click Through], [!UICONTROL View Through] y [!UICONTROL View Through (CTV)].

Para ver las métricas de conversión de visualizaciones de CTV, utilice la vista Ubicación o la vista Canal de marketing en Analysis Workspace.

Uso de la vista Ubicación:

1. Incluya ubicaciones de gasto de CTV en la vista de informes.

1. Incluya las métricas deseadas, como &quot;Impresiones&quot;, &quot;Clics&quot;, etc.

1. Aplique los siguientes filtros:

   Plataforma de publicidad: `Advertising Cloud DSP`

   Página de aterrizaje: `View-Through (CTV)`

Uso de la vista Canal de marketing:

1. Incluya la dimensión `Marketing Channel`.

1. Incluya las métricas deseadas, como &quot;Impresiones&quot;, &quot;Clics&quot;, etc.

1. Aplique los siguientes filtros:

   Plataforma de publicidad: `Advertising Cloud DSP`

   Página de aterrizaje: `View-Through (CTV)`

### Creación de paneles de Adobe Advertising

Para obtener información sobre cómo realizar un seguimiento de los datos de Adobe Advertising en relación con los objetivos de Analysis Workspace, vea el vídeo &quot;[Crear paneles de Adobe Advertising con Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)&quot;.

### Uso del Adobe Advertising ID para el análisis de entrada al sitio

Para ver cómo crear un informe de entrada al sitio de Adobe Advertising para supervisar las influencias del día de la semana, la hora del día, el explorador y la zona geográfica, vea el vídeo &quot;[Crear informes de entrada al sitio de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

## Iniciar una implementación de [!DNL Analytics for Advertising]

Póngase en contacto con el equipo de su cuenta de Adobe, que completará la configuración inicial necesaria para comenzar y le ayudará a planificar su implementación y el uso de los datos en función de las necesidades de su organización.

>[!MORELIKETHIS]
>
>* [Vídeo: Introducción a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Requisitos previos e información clave para implementar [!DNL Analytics for Advertising]](prerequisites.md)
>* [ID de Adobe Advertising usados por Analytics](ids.md)
>* [Código JavaScript para Analytics para Advertising](/help/integrations/analytics/javascript.md)
>* [Variaciones de datos previstas entre [!DNL Analytics]  y Adobe Advertising](data-variances.md)
>* [Métricas de Adobe Advertising en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
