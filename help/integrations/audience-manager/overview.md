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

## Sincronizar Audience Manager y otros [!DNL Adobe] segmentos para la segmentación de anuncios

DSP [!DNL Search, Social, & Commerce] y los usuarios pueden extraer metadatos, datos de jerarquía y datos de audiencia únicos para todas las audiencias de Audience Manager de un anunciante o agencia y otras [!DNL Adobe]. Esta conexión única solo está disponible para los especialistas en marketing que utilizan el Adobe Advertising. Consulte &quot;[Importar segmentos de Adobe Audience Manager para la segmentación de anuncios](/help/integrations/audience-manager/import-audiences.md)&quot;.

### Usar Audience Manager y otros [!DNL Adobe] segmentos para crear [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes de inclusión con [!DNL Advertising Search, Social, & Commerce] solamente*

En [!DNL Search, Social, & Commerce], puede crear audiencias de coincidencia de clientes de [!DNL Google Ads] a partir de los ID de usuario utilizando los segmentos de Audience Manager existentes que tienen [!UICONTROL Adobe Media Optimizer (HTTP)] y [!UICONTROL Adobe Media Optimizer Batch Destination] como destinos. ([!DNL Media Optimizer] es un nombre anterior de [!DNL Search, Social, & Commerce]). Esto incluye segmentos de Adobe Analytics que se publican en Adobe Experience Cloud y segmentos que se crean con Adobe Experience Cloud [!DNL Audience Library]. Para obtener más información, consulte &quot;[Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

Las [audiencias de coincidencia de clientes de los ID de usuario](https://support.google.com/google-ads/answer/9199250) funcionan como audiencias basadas en etiquetas de sitios web, pero se asigna un ID que no es PII a los miembros de audiencia única para obtener beneficios distintos sobre las audiencias estándar basadas en etiquetas de sitios web y las coincidencias de clientes.

Para crear los identificadores de usuario necesarios, debe usar una etiqueta JavaScript de Adobe Advertising <!-- with a user ID parameter --> en sus sitios web. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

![proceso de creación de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Una vez creadas las audiencias, puede usarlas en [!DNL Google Ads] campañas como [objetivos o exclusiones a nivel de campaña o de grupo de anuncios](#audience-manager-targets).

### Usar el Audience Manager y otros [!DNL Adobe] segmentos para segmentar o excluir anuncios {#audience-manager-targets}

* (Anunciantes incluidos con [!DNL Search, Social, & Commerce]) Puede usar cualquier audiencia de [!DNL Google Ads] que se haya [creado usando [!DNL Adobe] segmentos](#audience-manager-google-audiences) como objetivos o exclusiones a nivel de campaña o de grupo de anuncios en sus campañas de [!DNL Google Ads].

* DSP (Anunciantes con el servicio de publicidad) Puede usar sus [!DNL Adobe] segmentos existentes como destinatarios para sus ubicaciones de anuncios. Si lo desea, puede incluir los segmentos en audiencias reutilizables, que puede utilizar como destinos o exclusiones para varias ubicaciones.

* (Anunciantes con Advertising Creative) Puede usar sus [!DNL Adobe] segmentos existentes como destinatarios de elementos creativos específicos en sus experiencias publicitarias.

>[!NOTE]
>
>Para obtener más información acerca de cómo crear audiencias en las interfaces de Audience Manager y Experience Cloud [!DNL Audience Library], así como casos de uso comunes para distintos tipos de audiencias, consulte &quot;[Opciones de creación de audiencias](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)&quot;.

## DSP Envío de datos de exposición de medios de comunicación al Audience Manager

DSP *Anunciantes con solo el tipo de anuncio*:

DSP Los clientes de con Adobe Audience Manager pueden capturar datos de campañas de publicidad mediante llamadas en píxeles a Audience Manager. DSP A continuación, puede utilizar los datos de campaña para crear rasgos basados en reglas, que puede utilizar para definir nuevos segmentos y habilitar varios casos de uso de, como segmentación más avanzada, administración de frecuencias, análisis de marketing y perspectivas de creación de informes.

DSP Consulte &quot;[Información general sobre el envío de datos de exposición de medios de comunicación de la a Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obtener más información.

## Obtenga información más detallada sobre la actividad del sitio con Audience Analytics

Los clientes de Adobe Advertising con [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) pueden enviar datos con seguimiento de Adobe Advertising y segmentos de Audience Manager a [!DNL Analytics] para obtener información detallada sobre la actividad del sitio.

Para obtener más información, consulte &quot;[[!DNL Adobe Audience Analytics] para clientes de Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md)&quot;.
