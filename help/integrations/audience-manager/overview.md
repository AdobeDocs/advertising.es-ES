---
title: Integraciones de Adobe Advertising con Adobe Audience Manager
description: Obtenga información sobre las distintas formas en que Adobe Advertising puede intercambiar datos con Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Integraciones de Adobe Advertising con Adobe Audience Manager

Puede integrar Adobe Advertising con Audience Manager de las siguientes maneras.

## Sincronizar Audience Manager y otros [!DNL Adobe] Segmentos para segmentación de anuncios

[!DNL Search, Social, & Commerce] DSP y puede extraer metadatos, datos de jerarquía y datos de audiencia únicos para todos los Audience Manager de un anunciante o agencia y otros [!DNL Adobe] audiencias. Esta conexión única solo está disponible para los especialistas en marketing que utilizan el Adobe Advertising. Consulte &quot;[Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios](/help/integrations/audience-manager/import-audiences.md).&quot;

### Usar Audience Manager y otros [!DNL Adobe] Segmentos para crear [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes de inclusión con [!DNL Advertising Search, Social, & Commerce] solamente*

En [!DNL Search, Social, & Commerce], puede crear [!DNL Google Ads] audiencias de coincidencia de clientes de los ID de usuario que usan sus segmentos de Audience Manager existentes que tienen [!UICONTROL Adobe Media Optimizer (HTTP)] y [!UICONTROL Adobe Media Optimizer Batch Destination] como destinos. ([!DNL Media Optimizer] es un nombre anterior de [!DNL Search, Social, & Commerce].) Esto incluye segmentos de Adobe Analytics que se publican en Adobe Experience Cloud y segmentos que se crean con Adobe Experience Cloud [!DNL Audience Library]. Para obtener más información, consulte &quot;[Crear [!DNL Google Ads] audiencias de coincidencia de cliente de [!DNL Adobe] audiencias](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Audiencias de coincidencia de clientes a partir de ID de usuario](https://support.google.com/google-ads/answer/9199250) funcionan como las audiencias basadas en etiquetas de sitios web, pero se asigna un ID sin PII a los miembros de audiencia única para obtener beneficios distintos sobre las audiencias estándar basadas en etiquetas de sitio web y en coincidencias de clientes.

Para crear los ID de usuario necesarios, debe utilizar una etiqueta JavaScript de Adobe Advertising <!-- with a user ID parameter -->en sus sitios web. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

![proceso de creación de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Una vez creadas las audiencias, puede utilizarlas en [!DNL Google Ads] campañas como [objetivos o exclusiones a nivel de campaña o de grupo de anuncios](#audience-manager-targets).

### Uso de Audience Manager y otros [!DNL Adobe] Segmentos para segmentar o excluir anuncios {#audience-manager-targets}

* (Anunciantes de inclusión con [!DNL Search, Social, & Commerce]) Puede usar cualquiera [!DNL Google Ads] audiencias que fueron [creado mediante [!DNL Adobe] segmentos](#audience-manager-google-audiences) como objetivos o exclusiones de nivel de campaña o de nivel de grupo de publicidad en su [!DNL Google Ads] campañas.

* DSP (Anunciantes con el servicio de publicidad Puede utilizar el [!DNL Adobe] segmentos como destinatarios para sus ubicaciones de anuncios. Si lo desea, puede incluir los segmentos en audiencias reutilizables, que puede utilizar como destinos o exclusiones para varias ubicaciones.

* (Anunciantes con Advertising Creative) Puede utilizar su [!DNL Adobe] Segmentos como destinatarios de elementos creativos específicos en sus experiencias publicitarias.

>[!NOTE]
>
>Para obtener más información sobre cómo crear audiencias en el Audience Manager y en el Experience Cloud [!DNL Audience Library] interfaces y casos de uso comunes para diferentes tipos de audiencia, consulte &quot;[Opciones de creación de audiencias](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## DSP Envío de datos de exposición de medios de comunicación al Audience Manager

*DSP Anunciantes solo con la opción*

DSP Los clientes de con Adobe Audience Manager pueden capturar datos de campañas de publicidad mediante llamadas en píxeles a Audience Manager. DSP A continuación, puede utilizar los datos de campaña para crear rasgos basados en reglas, que puede utilizar para definir nuevos segmentos y habilitar varios casos de uso de, como segmentación más avanzada, administración de frecuencias, análisis de marketing y perspectivas de creación de informes.

Consulte &quot;[DSP Información general sobre el envío de datos de exposición de medios de comunicación de a Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obtener más información.

## Obtenga información más detallada sobre la actividad del sitio con Audience Analytics

Adobe Advertising de clientes con [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) puede enviar datos rastreados por Adobe Advertising y segmentos de Audience Manager a [!DNL Analytics] para obtener información detallada sobre la actividad del sitio.

Para obtener más información, consulte &quot;[[!DNL Adobe Audience Analytics] para clientes de Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md).&quot;
