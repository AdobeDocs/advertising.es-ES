---
title: Información general sobre [!DNL Analytics for Advertising]
description: Información general sobre [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Información general sobre [!DNL Analytics for Advertising]

*Anunciantes con DSP publicitarias y[!DNL Advertising Search]*

[!DNL Analytics for Advertising] integra Adobe Analytics y Adobe Advertising para ampliar y mejorar las capacidades de cada producto.

La integración permite a los anunciantes realizar un seguimiento de las interacciones de clics y visualizaciones del sitio en sus [!DNL Analytics] , lo que permite a las marcas ver cómo su gasto en publicidad conduce a la participación en el sitio y a objetivos empresariales críticos.

Además, la publicidad de Adobe puede acceder a los vastos datos de origen que [!DNL Analytics] recopila utilizando [!DNL Analytics] etiquetas ya en el sitio. Esto permite una administración de recorridos más sólida, remarketing de origen e informes de sitio de medios de pago. La publicidad de Adobe puede usar la variable [!DNL Analytics] datos para la optimización de gastos y ofertas.

Cuando se utilice correctamente, [!DNL Analytics for Advertising] desdibuja las líneas entre dos funciones tradicionales: administración de recorridos publicitarios (el acto de enviar usuarios al sitio a través de anuncios) y comprender esa participación en el sitio a través del análisis web.

Beneficios principales:

* Enviar [!DNL Analytics] segmenta directamente en Adobe de publicidad para el remarketing de sitios de origen.
* Uso [!DNL Analytics] eventos personalizados y estándar como señales de conversión para optimizar la publicidad de medios de pago.
* Aproveche [!DNL Analytics] Analysis Workspace para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas.
* Permita una colaboración más estrecha entre analistas web y equipos de medios de pago.
* Utilice ID de pulsaciones y visualizaciones de publicidad de Adobe persistente en [!DNL Analytics] para comprender la participación del sitio.
* Mejore los informes de medios de pago tradicionales en Analysis Workspace con métricas personalizadas, dimensiones personalizadas y actividad del sitio que no se pueden lograr al exportar datos o píxeles a servidores de publicidad u otros DSP.
* Aproveche [!DNL Analytics] código que ya se encuentra en el sitio web para el seguimiento y la optimización dentro de la publicidad de Adobe.

>[!TIP]
>
> Ver un [introducción de vídeo a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Uso de Analytics para informes de medios pagados

[!DNL Analytics for Advertising] mejora los informes y la perspectiva sobre cómo la publicidad impulsa el comportamiento del sitio al permitirle:

* Utilice ID de pulsaciones y visualizaciones de publicidad de Adobe persistente en [!DNL Analytics] para comprender la participación del sitio.
* Aproveche Analysis Workspace para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas. Puede acceder a los datos dimensionales y de evento de medios de pago, que incluyen los nombres de entidad de la campaña de publicidad de Adobe (hasta las ubicaciones y publicidades) y sus métricas asociadas, como clics, impresiones y costes.

Para usar [!DNL Analytics] como herramienta de informes multimedia de pago, su organización necesita un inicio de sesión de Experience Cloud con acceso a Analysis Workspace. Su equipo de publicidad de Adobe le ayudará a asignar los datos de publicidad de Adobe a grupos de informes individuales en Analysis Workspace. Puede enviar datos de publicidad de Adobe a cualquier grupo de informes, pero debe tener en cuenta los grupos de informes que se han asignado a publicidad de Adobe y los que no lo han hecho. En función del grupo de informes, esto puede cambiar los datos notificados.

[ID de publicidad de Adobe dentro de [!DNL Analytics]](ids.md) funciona como otras eVars, con una caducidad personalizada y persistente. De forma predeterminada, la ventana de retrospectiva de atribución se establece en 60 días durante la implementación de Publicidad de Adobe. Para cambiar esta configuración, trabaje con su [!DNL Adobe] equipo de la cuenta.

Las dimensiones de publicidad de Adobe se agregan con el sufijo &quot;(ID de AMO)&quot; (como &quot;Tipo de anuncio (ID de AMO)&quot;). Consulte &quot;[Métricas de publicidad de Adobe en Analysis Workspace](advertising-metrics-in-analytics.md)&quot; para obtener una lista de las dimensiones disponibles.

>[!NOTE]
>
> Cuando visualiza datos de publicidad de Adobe (o cualquier conjunto de datos) dentro de [!DNL Analytics], tenga en cuenta que las métricas y los informes se basan en reglas que se establecen dentro de [!DNL Analytics]. Los datos podrían ser diferentes a los que se ven en otros sistemas de informes, como los informes de servidores de publicidad, [!DNL DSP] informes o informes de motor de búsqueda. Para comprender las diferencias de datos en [!DNL Analytics], debe saber cuándo caducan los datos del eVar, qué define una visita, qué se considera atribución de último contacto versus atribución total persistente, y otros factores. Para obtener más información, consulte [Variaciones de datos previstas entre [!DNL Analytics] y publicidad de Adobe](data-variances.md).

## Uso de Analytics para impulsar campañas publicitarias de Adobe y Portfolio

Sin necesidad de píxeles adicionales, [!DNL Analytics for Advertising] permite una mejor optimización y una segmentación de audiencia más sencilla mediante el envío de dos señales principales a la publicidad de Adobe:

* Métricas de conversión que se utilizarán como señales de oferta:
   * métricas estándar, como [!UICONTROL Revenue] y [!UICONTROL Cart Views].
   * métricas de participación en el sitio, como vistas de página y métricas de visitas.
   * métricas de ingresos personalizadas.
   * métricas de ingresos reservadas.
* Segmentos creados en [!DNL Analytics] y publicado para el Experience Cloud.

   Puede usar [!DNL Analytics] segmentos para la resegmentación de sitios de origen en [!DNL DSP] y anuncios de búsqueda pagada.

   ([!DNL Search] solo) Anunciantes con [!DNL Analytics] pero no el Audience Manager también puede crear audiencias basadas en etiquetas de sitios web de Google (listas de remarketing) y audiencias de coincidencia de clientes (listas de clientes) desde [!DNL Analytics] segmentos que se comparten con Experience Cloud.

### Métricas de conversión de sitio como señales de oferta

Puede usar los eventos estándar y los personalizados desde [!DNL Analytics] para crear objetivos ponderados en la publicidad de Adobe. Los objetivos informan a las decisiones de oferta [!DNL DSP] paquetes y portafolios de búsqueda.

>[!NOTE]
>
> No puede asignar métricas calculadas desde [!DNL Analytics] en Publicidad de Adobe.

Su equipo de publicidad de Adobe le ayudará a identificar y asignar los eventos que son aplicables al rendimiento de medios de pago en la publicidad de Adobe, donde aparecerán en [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Consulte &quot;[Métricas de Analytics en publicidad de Adobe](analytics-data-in-advertising.md)&quot; para obtener una lista de las métricas disponibles.

### Segmentos de Analytics para redireccionamiento de sitios

La publicidad de Adobe puede ingerir [!DNL Analytics] segmentos con fines de remarketing para los DSP publicitarios y [!DNL Search] anuncios que utilizan la integración de audiencias de Experience Cloud nativa entre [!DNL Analytics] y Experience Cloud.

Para acceder a la [!DNL Analytics] segmentos, una cuenta de anunciante debe tener la variable [Servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) activada. Cuando el servicio de ID está habilitado, todos los segmentos del Experience Cloud (incluidos los segmentos creados en [!DNL Analytics] y publicados para el Experience Cloud, segmentos creados en Adobe Audience Manager, segmentos creados en Experience Cloud usando la variable [!DNL People core service], así como los segmentos creados en Adobe Experience Platform y enviados a Adobe (mediante Audience Manager), estarán disponibles en Adobe Advertising en cuanto se procesen.

[!DNL Analytics] Los segmentos de están disponibles en un plazo de 24 horas y se actualizan diariamente.

Para obtener más información sobre el servicio Audiencias de Experience Cloud, consulte [Audiencias de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Ejemplos de cómo utilizar la integración

### Uso de datos publicitarios de Adobe en Analysis Workspace

Para aprender a utilizar los datos de publicidad de Adobe para crear informes visuales en Analysis Workspace, consulte el vídeo &quot;[Introducción a Workspace e informes](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Creación de paneles publicitarios de Adobe

Para obtener información sobre cómo realizar un seguimiento de los datos publicitarios de Adobe en relación con sus objetivos en Analysis Workspace, consulte el vídeo &quot;[Creación de paneles publicitarios de Adobe con Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Uso del ID de publicidad de Adobe para el análisis de entrada al sitio

Para ver cómo se puede crear un informe de entrada al sitio de publicidad de Adobe para supervisar las influencias de día de la semana, hora del día, navegador y geográficas, consulte el vídeo &quot;[Creación de informes de entrada al sitio de publicidad de Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Vídeo: Introducción a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]](prerequisites.md)
>* [ID de publicidad de Adobe utilizados por Analytics](ids.md)
>* [Código JavaScript para Analytics for Advertising](/help/integrations/analytics/javascript.md)
>* [Variaciones de datos previstas entre [!DNL Analytics] y publicidad de Adobe](data-variances.md)
>* [Métricas de publicidad de Adobe en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en publicidad de Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)

