---
title: (Nueva IU) Acerca de los objetivos
description: Conozca cuáles son los objetivos para alcanzar sus metas empresariales.
feature: Search Objectives, Search Optimization
hide: true
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# (Nueva IU) Acerca de los objetivos

*característica de Beta*

Los objetivos son objetivos que un anunciante establece para alcanzar sus objetivos comerciales, como maximizar los beneficios o alcanzar un objetivo de ventas específico. Tanto Advertising Search, Social, Commerce y Advertising DSP usan objetivos:

* Cada portafolio de Search, Social y Commerce debe tener un objetivo para que la capacidad de optimización pueda crear modelos de clics e ingresos para el portafolio.

* En DSP, las metas aparecen como metas personalizadas para cuentas de DSP vinculadas a cuentas de Search, Social y Commerce. Cada paquete que utiliza los objetivos de optimización &quot;Máximo rendimiento de la inversión en publicidad (ROAS)&quot; o &quot;Menor coste por adquisición (CPA)&quot; debe incluir un objetivo personalizado que ayude a lograr el objetivo de optimización general.

Un objetivo consiste en las métricas de conversión que se van a rastrear y optimizar, y los pesos relativos de esas métricas. Por ejemplo, supongamos que una revista en línea con dos niveles de suscripción en línea y un nivel de suscripción de impresión y el objetivo &quot;maximizar los beneficios&quot; tiene tres métricas: &quot;suscripciones en línea básicas&quot; valoradas en 20 USD, &quot;suscripciones en línea premium&quot; valoradas en 40 USD y &quot;suscripciones de impresión&quot; valoradas en 30 USD. Si la revista desea dar peso de acuerdo con el valor monetario único de la suscripción, entonces los pesos relativos de las métricas serían 1, 2 y 1,5, respectivamente.

Para cada métrica del objetivo, puede:

* Configure pesos independientes para las conversiones desde dispositivos móviles.

* Etiquete la métrica como métrica [!UICONTROL Goal] o como métrica [!UICONTROL Assist].

* Aplique recomendaciones de peso a las métricas.

>[!NOTE]
>* (Buscar, Social y Commerce) Puede asociar un objetivo con un portafolio al [crear el portafolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) o al [modificar posteriormente la configuración del portafolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md).
>* (Anunciantes con cuentas de DSP vinculadas a cuentas de Search, Social y Commerce) En Advertising DSP, puede seleccionar un objetivo como [objetivo de optimización personalizado](/help/dsp/campaign-management/packages/package-settings.md) para un paquete con un ritmo de nivel de paquete.
>* Puede utilizar el mismo objetivo para varios portafolios de Search, Social y Commerce o para varios paquetes de DSP.
>* Las métricas de cada objetivo en la vista [!UICONTROL Objectives] no incluyen datos de DSP.

## Métricas disponibles

Puede incluir cualquiera de los siguientes elementos en sus objetivos:

* Métricas que Adobe Advertising rastrea usando el [píxel de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* [Métricas rastreadas por el anunciante a partir de archivos de fuentes de conversión](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* (Anunciantes con [!DNL Adobe Analytics for Advertising]) [Métricas de conversión y participación del sitio sincronizadas desde Adobe Analytics](/help/integrations/analytics/overview.md).

  En Search, Social y Commerce, las siguientes [métricas de participación del sitio](/help/integrations/analytics/analytics-data-in-advertising.md) se incluyen automáticamente en los algoritmos de oferta de portafolios: `timespent_secs_1stvisit`, `timespent_secs_total`, `pageviews_1stvisit`, `pageviews_total` y `bounces`.

* [!DNL Google] métricas:<!-- Search only, or might DSP-only clients also have these? -->

   * Conversiones [[!DNL Google Ads] seguidas ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) desde cuentas sincronizadas [!DNL Google Ads].

   * (Anunciantes con [[!DNL Google Analytics] integraciones](/help/search-social-commerce/admin/data-sources/data-source-about.md)): vistas de página, sesiones, tasa de salida hacia otro sitio (calculada como salidas hacia otro sitio/sesiones) y duración de la sesión.

     En Search, Social y Commerce, estas métricas se incorporan automáticamente a los algoritmos de oferta de portafolios.

## Opción para cargar objetivos en las redes de publicidad

Opcionalmente, puede [cargar los objetivos de los portafolios de la cuenta a [!DNL Google Ads] y/o [!DNL Microsoft Advertising] como conversiones](/help/search-social-commerce/tools/objective-upload-to-networks.md) para poder usarlos para la optimización a nivel de campaña o de grupo de anuncios. Cuando activa la opción, Search, Social y Commerce pasan diariamente a la red de publicidad los datos de ingresos ponderados en el nivel de EF ID (ID de clic). Omite cualquier métrica rastreada en la red de anuncios.

>[!MORELIKETHIS]
>
>* [Crear un objetivo](objective-create.md)
>* [Editar un objetivo](objective-edit.md)
>* [Eliminar un objetivo](objective-delete.md)
>* [Aplicar recomendaciones de peso a un objetivo](objective-apply-weight-recommendations.md)
>* [Configuración de objetivos](objective-settings.md)
