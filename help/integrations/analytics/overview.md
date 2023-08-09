---
title: Información general de [!DNL Analytics for Advertising]
description: Información general de [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 2903bf783969b3e2d59c0933629cbb170c0a314c
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 0%

---

# Información general de [!DNL Analytics for Advertising]

*DSP Anunciantes con Advertising y[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integra Adobe Analytics y Adobe Advertising para ampliar y mejorar las capacidades de cada producto.

La integración permite a los anunciantes rastrear las interacciones de sitios de clics y visualizaciones en sus [!DNL Analytics] , lo que permite a las marcas ver cómo su gasto en publicidad conduce a la participación del sitio y a objetivos comerciales críticos.

Además, el Adobe Advertising de puede acceder a la gran cantidad de datos de origen que [!DNL Analytics] recopila mediante [!DNL Analytics] etiquetas que ya se encuentran en el sitio. Esto permite una administración de recorridos más sólida, remarketing de origen y creación de informes de sitios de medios de pago. El Adobe Advertising puede utilizar más la variable [!DNL Analytics] datos para la optimización de gastos y ofertas.

Cuando se utilice correctamente, [!DNL Analytics for Advertising] desdibuja las líneas entre dos funciones tradicionales: la administración de recorridos publicitarios (el acto de enviar usuarios al sitio a través de anuncios) y la comprensión de esa participación del sitio a través del análisis web.

Beneficios primarios:

* Enviar [!DNL Analytics] Segmentos directamente al Adobe Advertising para remarketing de sitios de origen.
* Uso [!DNL Analytics] eventos personalizados y estándar como señales de conversión para optimizar la publicidad en medios de pago.
* Aproveche las ventajas de [!DNL Analytics] Analysis Workspace para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas.
* Permite una colaboración más estrecha entre los analistas web y los equipos de medios de pago.
* Usar ID de pulsaciones y vistas de Adobe Advertising persistentes dentro de [!DNL Analytics] para comprender la participación en el sitio.
* Mejore los informes de medios de pago tradicionales en Analysis Workspace DSP con métricas, dimensiones personalizadas y actividad del sitio personalizadas que no se pueden conseguir al exportar datos o píxeles a servidores de publicidad u otros servicios de publicidad
* Aproveche las ventajas de [!DNL Analytics] ya hay código en su sitio web para el seguimiento y la optimización dentro del Adobe Advertising.

>[!TIP]
>
> Ver una [introducción de vídeo a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Uso de Analytics para informes de medios de pago

[!DNL Analytics for Advertising] mejora los informes y la perspectiva de cómo la publicidad impulsa el comportamiento del sitio, lo que le permite:

* Usar ID de pulsaciones y vistas de Adobe Advertising persistentes dentro de [!DNL Analytics] para comprender la participación en el sitio.
* Aproveche Analysis Workspace para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas. Puede acceder a los datos de dimensiones y eventos de medios de pago, que incluyen nombres de entidades de campaña de Adobe Advertising (hasta ubicaciones y anuncios) y sus métricas asociadas, como clics, impresiones y costes.

Para usar [!DNL Analytics] como herramienta de informes de medios de pago, su organización necesita un inicio de sesión de Experience Cloud con acceso a Analysis Workspace. Su equipo de Adobe Advertising le ayudará a asignar los datos de Adobe Advertising a grupos de informes individuales en Analysis Workspace. Puede enviar datos de Adobe Advertising a cualquier grupo de informes, pero debe tener en cuenta los grupos de informes que se han asignado al Adobe Advertising y los que no. En función del grupo de informes, esto puede cambiar los datos de los informes.

[ID de Adobe Advertising dentro de [!DNL Analytics]](ids.md) funciona como otros [!DNL eVars], con una caducidad personalizada y persistente. De forma predeterminada, la ventana retrospectiva de atribución se establece en 60 días durante la implementación del Adobe Advertising. Para cambiar esta configuración, colabore con su equipo de cuenta de Adobe.

Las dimensiones de Adobe Advertising se anexan con el sufijo &quot;(AMO ID)&quot; (como &quot;Tipo de anuncio (AMO ID)&quot;). Consulte &quot;[Métricas de Adobe Advertising en Analysis Workspace](advertising-metrics-in-analytics.md)&quot; para obtener una lista de las dimensiones disponibles.

>[!NOTE]
>
> Cuando visualiza datos de Adobe Advertising (o cualquier conjunto de datos) en [!DNL Analytics], tenga en cuenta que las métricas y los informes se basan en las reglas establecidas dentro de [!DNL Analytics]. Los datos pueden ser diferentes a los que se ven en otros sistemas de informes, como los informes de servidores de publicidad, [!DNL DSP] informes o informes de motores de búsqueda. Para comprender las diferencias de datos en [!DNL Analytics], debe saber cuándo [!DNL eVar] los datos caducan, qué define una visita, qué se considera atribución de último contacto frente a atribución de persistencia total y otros factores. Para obtener más información, consulte [Variaciones de datos previstas entre [!DNL Analytics] y ADOBE ADVERTISING](data-variances.md).

## Uso de Analytics para impulsar campañas y Portfolio de Adobe Advertising

Sin necesidad de píxeles adicionales, [!DNL Analytics for Advertising] permite una mejor optimización y una segmentación más sencilla de la audiencia al enviar dos señales principales al Adobe Advertising:

* Métricas de conversión que se utilizarán como señales de oferta:
   * métricas estándar, como [!UICONTROL Revenue] y [!UICONTROL Cart Views].
   * métricas de participación del sitio, como las métricas de vista de página y visita.
   * métricas de ingresos personalizadas.
   * métricas de ingresos reservadas.
* Segmentos creados en [!DNL Analytics] y publicado en el Experience Cloud.

  Puede utilizar [!DNL Analytics] segmentos para redireccionamiento de sitios de origen en [!DNL DSP] y anuncios de búsqueda pagada.

  ([!DNL Search, Social, & Commerce] solo) Anunciantes con [!DNL Analytics] pero no Audience Manager también puede crear audiencias basadas en etiquetas de sitios web de Google (listas de remarketing) y audiencias de coincidencia de clientes (listas de clientes) desde [!DNL Analytics] segmentos compartidos con el Experience Cloud.

### Métricas de conversión del sitio como señales de oferta

Puede utilizar los eventos estándar y los eventos personalizados desde [!DNL Analytics] para construir objetivos ponderados en el Adobe Advertising. Los objetivos informan las decisiones de oferta de su [!DNL DSP] y Buscar portafolios.

>[!NOTE]
>
> No se pueden asignar métricas calculadas desde [!DNL Analytics] en el Adobe Advertising.

Su equipo de Adobe Advertising le ayudará a identificar y asignar los eventos aplicables al rendimiento de los medios de pago en Adobe Advertising, donde aparecerán en [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Consulte &quot;[Métricas de Analytics en Adobe Advertising](analytics-data-in-advertising.md)&quot; para obtener una lista de las métricas disponibles.

### Segmentos de Analytics para redireccionamiento de sitios

El Adobe Advertising puede ingerir [!DNL Analytics] DSP segmentos para fines de remarketing con fines de publicidad y de publicidad de los segmentos de la [!DNL Search, Social, & Commerce] Anuncios que utilizan la integración nativa de Audiencias de Experience Cloud entre [!DNL Analytics] y Experience Cloud.

Para acceder a [!DNL Analytics] segmentos, una cuenta de anunciante debe tener el [Servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) activado. Cuando el servicio de ID está habilitado, se eliminan todos los segmentos del Experience Cloud (incluidos los creados en [!DNL Analytics] y publicados en Experience Cloud, segmentos creados en Adobe Audience Manager, segmentos creados en Experience Cloud mediante [!DNL People core service]y los segmentos creados en Adobe Experience Platform y enviados al Adobe Advertising mediante el Audience Manager) están disponibles en el Adobe Advertising en cuanto se procesan.

[!DNL Analytics] los segmentos están disponibles en un plazo de 24 horas y se actualizan diariamente.

Para obtener más información sobre el servicio Audiencias del Experience Cloud, consulte [Audiencias de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Ejemplos de cómo utilizar la integración {#integration-examples}

### Uso de datos de Adobe Advertising en Analysis Workspace

Para obtener información sobre cómo utilizar los datos de Adobe Advertising para crear informes visuales en Analysis Workspace, consulte el vídeo &quot;[Introducción a Workspace y Creación de informes](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Uso de conversiones de visualizaciones de TV conectadas en informes

*DSP Solo usuarios de Advertising*

Puede medir la eficacia del canal completo de sus campañas de TV conectadas (CTV) vinculando la exposición de la publicidad en dispositivos CTV a conversiones in situ. El nuevo [!UICONTROL Landing Type] filter &quot;[!UICONTROL View-through (CTV)]&quot; divide las conversiones en filas independientes para [!UICONTROL Click Through], [!UICONTROL View Through], y [!UICONTROL View Through (CTV)] valores.

Para ver las métricas de conversión de visualizaciones de CTV, utilice la vista Ubicación o la vista Canal de marketing en Analysis Workspace.

Uso de la vista Ubicación:

1. Incluya ubicaciones de gasto de CTV en la vista de informes.

1. Incluya las métricas deseadas, como &quot;Impresiones&quot;, &quot;Clics&quot;, etc.

1. Aplique los siguientes filtros:

   Plataforma de publicidad: `Advertising Cloud DSP`

   Página de aterrizaje: `View-Through (CTV)`

Uso de la vista Canal de marketing:

1. Incluir la dimensión `Marketing Channel`.

1. Incluya las métricas deseadas, como &quot;Impresiones&quot;, &quot;Clics&quot;, etc.

1. Aplique los siguientes filtros:

   Plataforma de publicidad: `Advertising Cloud DSP`

   Página de aterrizaje: `View-Through (CTV)`

### Creación de paneles de Adobe Advertising

Para obtener información sobre cómo realizar un seguimiento de los datos de Adobe Advertising en comparación con los objetivos en Analysis Workspace, consulte el vídeo &quot;[Creación de paneles de Adobe Advertising con Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Uso del ID de Adobe Advertising para el análisis de entrada al sitio

Para ver cómo puede crear un informe de entrada al sitio de Adobe Advertising para monitorizar las influencias del día de la semana, la hora del día, el explorador y la zona geográfica, consulte el vídeo &quot;[Crear informes de entrada al sitio de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Vídeo: Introducción a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]](prerequisites.md)
>* [ID de Adobe Advertising utilizados por Analytics](ids.md)
>* [Código JavaScript para Analytics para publicidad](/help/integrations/analytics/javascript.md)
>* [Variaciones de datos previstas entre [!DNL Analytics] y ADOBE ADVERTISING](data-variances.md)
>* [Métricas de Adobe Advertising en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
