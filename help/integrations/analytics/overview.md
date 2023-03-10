---
title: Información general de [!DNL Analytics for Advertising]
description: Información general de [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# Información general de [!DNL Analytics for Advertising]

*DSP Anunciantes con Advertising y[!DNL Advertising Search]*

[!DNL Analytics for Advertising] integra Adobe Analytics y publicidad de Adobe para ampliar y mejorar las capacidades de cada producto.

La integración permite a los anunciantes rastrear las interacciones de sitios de clics y visualizaciones en sus [!DNL Analytics] , lo que permite a las marcas ver cómo su gasto en publicidad conduce a la participación del sitio y a objetivos comerciales críticos.

Además, Adobe Advertising puede acceder a la gran cantidad de datos de origen que [!DNL Analytics] recopila mediante [!DNL Analytics] etiquetas que ya se encuentran en el sitio. Esto permite una administración de recorridos más sólida, remarketing de origen y creación de informes de sitios de medios de pago. Adobe Advertising puede utilizar aún más el [!DNL Analytics] datos para la optimización de gastos y ofertas.

Cuando se utilice correctamente, [!DNL Analytics for Advertising] desdibuja las líneas entre dos funciones tradicionales: la administración de recorridos publicitarios (el acto de enviar usuarios al sitio a través de anuncios) y la comprensión de esa participación del sitio a través del análisis web.

Beneficios primarios:

* Enviar [!DNL Analytics] Segmentos de directamente a la publicidad de Adobe para el remarketing de sitios de origen.
* Uso [!DNL Analytics] eventos personalizados y estándar como señales de conversión para optimizar la publicidad en medios de pago.
* Aproveche las ventajas de [!DNL Analytics] Analysis Workspace para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas.
* Permite una colaboración más estrecha entre los analistas web y los equipos de medios de pago.
* Usar ID de pulsaciones y visualizaciones de Adobe persistente en [!DNL Analytics] para comprender la participación en el sitio.
* Mejore los informes de medios de pago tradicionales en Analysis Workspace DSP con métricas, dimensiones personalizadas y actividad del sitio personalizadas que no se pueden conseguir al exportar datos o píxeles a servidores de publicidad u otros servicios de publicidad
* Aproveche las ventajas de [!DNL Analytics] ya hay código en su sitio web para el seguimiento y la optimización dentro de la publicidad de Adobe.

>[!TIP]
>
> Ver una [introducción de vídeo a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Uso de Analytics para informes de medios de pago

[!DNL Analytics for Advertising] mejora los informes y la perspectiva de cómo la publicidad impulsa el comportamiento del sitio, lo que le permite:

* Usar ID de pulsaciones y visualizaciones de Adobe persistente en [!DNL Analytics] para comprender la participación en el sitio.
* Aproveche Analysis Workspace para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas. Puede acceder a los datos de dimensiones y eventos de medios de pago, que incluyen nombres de entidades de campaña de publicidad de Adobe (hasta ubicaciones y anuncios) y sus métricas asociadas, como clics, impresiones y costes.

Para usar [!DNL Analytics] como herramienta de informes de medios de pago, su organización necesita un inicio de sesión de Experience Cloud con acceso a Analysis Workspace. Su equipo de publicidad de Adobe le ayudará a asignar los datos de publicidad de Adobe a grupos de informes individuales en Analysis Workspace. Puede enviar datos de publicidad de Adobe a cualquier grupo de informes, pero debe tener en cuenta los grupos de informes que se han asignado a la publicidad de Adobe y los que no. En función del grupo de informes, esto puede cambiar los datos de los informes.

[ID de publicidad de Adobe dentro de [!DNL Analytics]](ids.md) funciona como otras eVars, con una caducidad personalizada y persistente. De forma predeterminada, la ventana retrospectiva de atribución se establece en 60 días durante la implementación de la publicidad de Adobe. Para cambiar esta configuración, colabore con su equipo de cuenta de Adobe.

Las dimensiones de publicidad de Adobe se anexan con el sufijo &quot;(AMO ID)&quot; (como &quot;Tipo de anuncio (AMO ID)&quot;). Consulte &quot;[Métricas de publicidad de Adobe en Analysis Workspace](advertising-metrics-in-analytics.md)&quot; para obtener una lista de las dimensiones disponibles.

>[!NOTE]
>
> Cuando vea datos de publicidad de Adobe (o cualquier conjunto de datos) en [!DNL Analytics], tenga en cuenta que las métricas y los informes se basan en las reglas establecidas dentro de [!DNL Analytics]. Los datos pueden ser diferentes a los que se ven en otros sistemas de informes, como los informes de servidores de publicidad, [!DNL DSP] informes o informes de motores de búsqueda. Para comprender las diferencias de datos en [!DNL Analytics]Por lo tanto, debe saber cuándo caducan los datos de eVar, qué define una visita, qué se considera atribución de último contacto frente a atribución de persistencia total y otros factores. Para obtener más información, consulte [Variaciones de datos previstas entre [!DNL Analytics] Publicidad de Adobe y](data-variances.md).

## Uso de Analytics para impulsar campañas publicitarias de Adobe y Portfolio

Sin necesidad de píxeles adicionales, [!DNL Analytics for Advertising] permite una mejor optimización y una segmentación de audiencia más sencilla mediante el envío de dos señales principales a la publicidad de Adobe:

* Métricas de conversión que se utilizarán como señales de oferta:
   * métricas estándar, como [!UICONTROL Revenue] y [!UICONTROL Cart Views].
   * métricas de participación del sitio, como las métricas de vista de página y visita.
   * métricas de ingresos personalizadas.
   * métricas de ingresos reservadas.
* Segmentos creados en [!DNL Analytics] y publicado en el Experience Cloud.

   Puede utilizar [!DNL Analytics] segmentos para redireccionamiento de sitios de origen en [!DNL DSP] y anuncios de búsqueda pagada.

   ([!DNL Search] solo) Anunciantes con [!DNL Analytics] pero no Audience Manager también puede crear audiencias basadas en etiquetas de sitios web de Google (listas de remarketing) y audiencias de coincidencia de clientes (listas de clientes) desde [!DNL Analytics] segmentos compartidos con el Experience Cloud.

### Métricas de conversión del sitio como señales de oferta

Puede utilizar los eventos estándar y los eventos personalizados desde [!DNL Analytics] para crear objetivos ponderados en la publicidad de Adobe. Los objetivos informan las decisiones de oferta de su [!DNL DSP] y Buscar portafolios.

>[!NOTE]
>
> No se pueden asignar métricas calculadas desde [!DNL Analytics] en la publicidad de Adobe.

Su equipo de publicidad de Adobe le ayudará a identificar y asignar los eventos aplicables al rendimiento de los medios de pago a la publicidad de Adobe, donde aparecerán en [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Consulte &quot;[Métricas de Analytics en la publicidad de Adobe](analytics-data-in-advertising.md)&quot; para obtener una lista de las métricas disponibles.

### Segmentos de Analytics para redireccionamiento de sitios

Adobe La publicidad puede ingerir [!DNL Analytics] DSP segmentos para fines de remarketing con fines de publicidad y de publicidad de los segmentos de la [!DNL Search] Anuncios que utilizan la integración nativa de Audiencias de Experience Cloud entre [!DNL Analytics] y Experience Cloud.

Para acceder a [!DNL Analytics] segmentos, una cuenta de anunciante debe tener el [Servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) activado. Cuando el servicio de ID está habilitado, se eliminan todos los segmentos del Experience Cloud (incluidos los creados en [!DNL Analytics] y publicados en Experience Cloud, segmentos creados en Adobe Audience Manager, segmentos creados en Experience Cloud mediante [!DNL People core service]y los segmentos creados en Adobe Experience Platform y enviados a la publicidad de Adobe (a través de Audience Manager) quedan disponibles en la publicidad de Adobe en cuanto se procesan.

[!DNL Analytics] los segmentos están disponibles en un plazo de 24 horas y se actualizan diariamente.

Para obtener más información sobre el servicio Audiencias del Experience Cloud, consulte [Audiencias de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Ejemplos de cómo utilizar la integración

### Uso de datos de publicidad de Adobe en Analysis Workspace

Para aprender a utilizar los datos de publicidad de Adobe para crear informes visuales en Analysis Workspace, consulte el vídeo &quot;[Introducción a Workspace y Creación de informes](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Creación de paneles de publicidad de Adobe

Para obtener información sobre cómo rastrear los datos de publicidad de Adobe en sus objetivos en Analysis Workspace, consulte el vídeo &quot;[Creación de paneles de publicidad de Adobe con Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Uso del ID de publicidad de Adobe para el análisis de entrada al sitio

Para ver cómo puede crear un informe de entrada al sitio de publicidad de Adobe para monitorizar las influencias del día de la semana, la hora del día, el explorador y la zona geográfica, consulte el vídeo &quot;[Crear informes de entrada al sitio de publicidad de Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Vídeo: Introducción a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]](prerequisites.md)
>* [ID de publicidad de Adobe utilizados por Analytics](ids.md)
>* [Código JavaScript para Analytics para publicidad](/help/integrations/analytics/javascript.md)
>* [Variaciones de datos previstas entre [!DNL Analytics] Publicidad de Adobe y](data-variances.md)
>* [Métricas de publicidad de Adobe en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en publicidad de Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)

