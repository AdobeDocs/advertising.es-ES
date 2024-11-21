---
title: Información general de  [!DNL Analytics for Advertising]
description: Información general de  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 2575b737926cfd681fd744401d5f4555402fbee2
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# Información general de [!DNL Analytics for Advertising]

*Anunciantes con Advertising DSP y[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integra Adobe Analytics y Adobe Advertising para ampliar y mejorar las capacidades de cada producto.

La integración permite a los anunciantes rastrear las interacciones del sitio de clics y visualizaciones en sus [!DNL Analytics] instancias, lo que permite a las marcas ver cómo su gasto en publicidad conduce a la participación del sitio y a objetivos comerciales críticos.

Además, el Adobe Advertising puede tener acceso a los grandes datos de origen que [!DNL Analytics] recopila mediante las etiquetas [!DNL Analytics] que ya se encuentran en el sitio. Esto permite una administración de recorridos más sólida, remarketing de origen y creación de informes de sitios de medios de pago. Los Adobes Advertising pueden usar aún más los datos de [!DNL Analytics] para la optimización de gastos y ofertas.

Cuando se emplea correctamente, [!DNL Analytics for Advertising] difumina las líneas entre dos funciones tradicionales: la administración de recorridos de publicidad (el acto de enviar usuarios al sitio a través de anuncios) y la comprensión de la participación del sitio a través del análisis web.

Beneficios primarios:

* Envíe [!DNL Analytics] segmentos directamente al Adobe Advertising para remarketing de sitio de origen.
* Utilice [!DNL Analytics] eventos personalizados y estándar como señales de conversión para optimizar la publicidad en medios de pago.
* Aproveche [!DNL Analytics] Analysis Workspace para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas.
* Permite una colaboración más estrecha entre los analistas web y los equipos de medios de pago.
* Use las ID de pulsaciones y vistas de Adobe Advertising persistente dentro de [!DNL Analytics] para comprender la participación en el sitio.
* Mejore los informes de medios de pago tradicionales en Analysis Workspace DSP con métricas, dimensiones personalizadas y actividad del sitio personalizadas que no se pueden conseguir al exportar datos o píxeles a servidores de publicidad u otros servicios de publicidad
* Aproveche el código [!DNL Analytics] que ya se encuentra en el sitio web para realizar el seguimiento y optimizar en el Adobe Advertising.

>[!TIP]
>
> Vea un [vídeo de presentación de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Uso de Analytics para informes de medios de pago

[!DNL Analytics for Advertising] mejora la generación de informes y la perspectiva sobre cómo la publicidad impulsa el comportamiento del sitio, ya que le permite:

* Use las ID de pulsaciones y vistas de Adobe Advertising persistente dentro de [!DNL Analytics] para comprender la participación en el sitio.
* Aproveche Analysis Workspace para comprender mejor los puntos de entrada del sitio y el comportamiento de las visitas. Puede acceder a los datos de dimensiones y eventos de medios de pago, que incluyen nombres de entidades de campaña de Adobe Advertising (hasta ubicaciones y anuncios) y sus métricas asociadas, como clics, impresiones y costes.

Para usar [!DNL Analytics] como herramienta de informes de medios de pago, su organización necesita un inicio de sesión de Experience Cloud con acceso a Analysis Workspace. Su equipo de Adobe Advertising le ayudará a asignar los datos de Adobe Advertising a grupos de informes individuales en Analysis Workspace. Puede enviar datos de Adobe Advertising a cualquier grupo de informes, pero debe tener en cuenta los grupos de informes que se han asignado al Adobe Advertising y los que no. En función del grupo de informes, esto puede cambiar los datos de los informes.

[Los identificadores de Adobe Advertising dentro de [!DNL Analytics]](ids.md) funcionan como otros [!DNL eVars], con una caducidad personalizada y persistente. De forma predeterminada, la ventana retrospectiva de atribución se establece en 60 días durante la implementación del Adobe Advertising. Para cambiar esta configuración, colabore con su equipo de cuenta de Adobe.

Las dimensiones de Adobe Advertising se anexan con el sufijo &quot;(AMO ID)&quot; (como &quot;Tipo de anuncio (AMO ID)&quot;). Consulte &quot;[Métricas de Adobe Advertising en Analysis Workspace](advertising-metrics-in-analytics.md)&quot; para obtener una lista de las dimensiones disponibles.

>[!NOTE]
>
> Cuando vea datos de Adobe Advertising (o cualquier conjunto de datos) en [!DNL Analytics], tenga en cuenta que las métricas y los informes se basan en las reglas establecidas en [!DNL Analytics]. Los datos podrían ser diferentes a los que se ven en otros sistemas de informes, como los informes de servidores de publicidad, [!DNL DSP] o los informes de motores de búsqueda. Para comprender las diferencias de datos en [!DNL Analytics], necesita saber cuándo caducan los datos de [!DNL eVar], qué define una visita, qué se considera atribución de último contacto frente a atribución de persistencia total y otros factores. Para obtener más información, vea [Variaciones de datos previstas entre [!DNL Analytics]  y el Adobe Advertising](data-variances.md).

## Uso de Analytics para impulsar campañas y Portfolio de Adobe Advertising

Sin requerir píxeles adicionales, [!DNL Analytics for Advertising] permite una mejor optimización y una segmentación de audiencia más sencilla al enviar dos señales principales al Adobe Advertising:

* Métricas de conversión que se utilizarán como señales de oferta:
   * métricas estándar, como [!UICONTROL Revenue] y [!UICONTROL Cart Views].
   * métricas de participación del sitio, como las métricas de vista de página y visita.
   * métricas de ingresos personalizadas.
   * métricas de ingresos reservadas.
* Segmentos creados en [!DNL Analytics] y publicados en el Experience Cloud.

  Puede usar [!DNL Analytics] segmentos para el redireccionamiento de sitios de origen en [!DNL DSP] y anuncios de búsqueda de pago.

  ([!DNL Search, Social, & Commerce] solamente) Los anunciantes con [!DNL Analytics] pero no el Audience Manager también pueden crear audiencias basadas en etiquetas del sitio web de Google (listas de remarketing) y audiencias coincidentes de clientes (listas de clientes) a partir de [!DNL Analytics] segmentos que se comparten con el Experience Cloud.

### Métricas de conversión del sitio como señales de oferta

Puede usar sus eventos estándar y eventos personalizados de [!DNL Analytics] para generar objetivos ponderados en los Adobes Advertising. Los objetivos informan las decisiones de oferta de sus paquetes de [!DNL DSP] y portafolios de Search, Social y Commerce.

>[!NOTE]
>
> No se pueden asignar métricas calculadas de [!DNL Analytics] al Adobe Advertising.

Su equipo de Adobe Advertising le ayudará a identificar y asignar los eventos aplicables al rendimiento de medios de pago en Adobe Advertising, donde se enumeran en [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Consulte &quot;[Métricas de Analytics en Adobe Advertising](analytics-data-in-advertising.md)&quot; para obtener una lista de las métricas disponibles.

### Segmentos de Analytics para redireccionamiento de sitios

El Adobe Advertising puede ingerir [!DNL Analytics] segmentos con fines de remarketing para anuncios de Advertising DSP y [!DNL Search, Social, & Commerce] mediante la integración de audiencias de Experience Cloud nativas entre [!DNL Analytics] y el Experience Cloud.

Para acceder a los segmentos de [!DNL Analytics], una cuenta de anunciante debe habilitar el [servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html). Cuando se habilita el servicio de ID, todos los segmentos del Experience Cloud (incluidos los segmentos creados en [!DNL Analytics] y publicados en Experience Cloud, los segmentos creados en Adobe Audience Manager, los segmentos creados en Experience Cloud mediante [!DNL People core service] y los segmentos creados en Adobe Experience Platform y enviados al Adobe Advertising mediante Audience Manager) quedan disponibles en Adobe Advertising en cuanto se procesan.

[!DNL Analytics] segmentos están disponibles en un plazo de 24 horas y se actualizan diariamente.

Para obtener más información acerca del servicio Audiencias de Experience Cloud, consulte [Audiencias de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Ejemplos de cómo utilizar la integración {#integration-examples}

### Uso de datos de Adobe Advertising en Analysis Workspace

Para obtener información sobre cómo usar los datos de Adobe Advertising para crear informes visuales en Analysis Workspace, vea el vídeo &quot;[Introducción a Workspace y Creación de informes](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;.

#### Uso de conversiones de visualizaciones de TV conectadas en informes

*Solo usuarios de Advertising DSP*

Puede medir la eficacia del canal completo de sus campañas de TV conectadas (CTV) vinculando la exposición de la publicidad en dispositivos CTV a conversiones in situ. El nuevo filtro [!UICONTROL Landing Type] &quot;[!UICONTROL View-through (CTV)]&quot; divide las conversiones en filas independientes para los valores [!UICONTROL Click Through], [!UICONTROL View Through] y [!UICONTROL View Through (CTV)].

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

### Uso del ID de Adobe Advertising para el análisis de entrada al sitio

Para ver cómo puede crear un informe de entrada al sitio de Adobe Advertising para supervisar las influencias del día de la semana, la hora del día, el explorador y la zona geográfica, vea el vídeo &quot;[Crear informes de entrada al sitio de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

## Iniciar una implementación de [!DNL Analytics for Advertising]

Póngase en contacto con el equipo de cuenta de Adobe, que completará la configuración inicial necesaria para comenzar y le ayudará a planificar su implementación y el uso de los datos en función de las necesidades de su organización.

>[!MORELIKETHIS]
>
>* [Vídeo: Introducción a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]](prerequisites.md)
>* [ID de Adobe Advertising usados por Analytics](ids.md)
>* [Código JavaScript para Analytics para Advertising](/help/integrations/analytics/javascript.md)
>* [Variaciones de datos previstas entre [!DNL Analytics]  y el Adobe Advertising](data-variances.md)
>* [Métricas de Adobe Advertising en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en el Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
