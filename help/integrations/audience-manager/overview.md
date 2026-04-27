---
title: Integraciones de Adobe Advertising con Adobe Audience Manager
description: Obtenga información sobre las distintas formas en que Adobe Advertising puede intercambiar datos con Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
TQID: https://experienceleague.adobe.com/4O4O-DmHhClvSiOSxM9blAEvVslzYzRobEyU6RGeMEQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2: id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 517
ht-degree: 0%

---

# Integraciones de Adobe Advertising con Adobe Audience Manager

Puede integrar Adobe Advertising con Audience Manager de las siguientes maneras.

## Sincronizar Audience Manager y otros [!DNL Adobe] segmentos para la segmentación de anuncios

[!DNL Search, Social, & Commerce] y DSP pueden extraer metadatos, datos de jerarquía y datos de audiencia única para todas las audiencias de Audience Manager de un anunciante o agencia y otras [!DNL Adobe]. Esta conexión única solo está disponible para los especialistas en marketing que utilizan Adobe Advertising. Consulte &quot;[Importar segmentos de Adobe Audience Manager para segmentar anuncios](/help/integrations/audience-manager/import-audiences.md)&quot;.

### Usar Audience Manager y otros [!DNL Adobe] segmentos para crear [!DNL Google Ads] audiencias {#audience-manager-google-audiences}

*Anunciantes de inclusión con [!DNL Advertising Search, Social, & Commerce] solamente*

En [!DNL Search, Social, & Commerce], puede crear audiencias de coincidencia de clientes de [!DNL Google Ads] a partir de los ID de usuario utilizando los segmentos de Audience Manager existentes que tienen [!UICONTROL Adobe Media Optimizer (HTTP)] y [!UICONTROL Adobe Media Optimizer Batch Destination] como destinos. ([!DNL Media Optimizer] es un nombre anterior de [!DNL Search, Social, & Commerce]). Esto incluye segmentos de Adobe Analytics que se publican en Adobe CX Enterprise y segmentos que se crean con Adobe CX Enterprise [!DNL Audience Library]. Para obtener más información, consulte &quot;[Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

Las [audiencias de coincidencia de clientes de los ID de usuario](https://support.google.com/google-ads/answer/9199250) funcionan como audiencias basadas en etiquetas de sitios web, pero se asigna un ID que no es PII a los miembros de audiencia única para obtener beneficios distintos sobre las audiencias estándar basadas en etiquetas de sitios web y las coincidencias de clientes.

Para crear los ID de usuario necesarios, debe usar una etiqueta JavaScript de Adobe Advertising <!-- with a user ID parameter --> en sus sitios web. Póngase en contacto con el equipo de su cuenta de Adobe para obtener más información.

![proceso de creación de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Una vez creadas las audiencias, puede usarlas en [!DNL Google Ads] campañas como [objetivos o exclusiones a nivel de campaña o de grupo de anuncios](#audience-manager-targets).

### Usar Audience Manager y otros [!DNL Adobe] segmentos para segmentar o excluir anuncios {#audience-manager-targets}

* (Anunciantes incluidos con [!DNL Search, Social, & Commerce]) Puede usar cualquier audiencia de [!DNL Google Ads] que se haya [creado usando [!DNL Adobe] segmentos](#audience-manager-google-audiences) como objetivos o exclusiones a nivel de campaña o de grupo de anuncios en sus campañas de [!DNL Google Ads].

* (Anunciantes con DSP) Puede usar sus [!DNL Adobe] segmentos existentes como destinatarios para sus ubicaciones de anuncios. Si lo desea, puede incluir los segmentos en audiencias reutilizables, que puede utilizar como destinos o exclusiones para varias ubicaciones.

* (Anunciantes con Advertising Creative) Puede usar sus [!DNL Adobe] segmentos existentes como destinatarios de elementos creativos específicos en sus experiencias publicitarias.

>[!NOTE]
>
>Para obtener más información acerca de cómo crear audiencias en las interfaces de Audience Manager y Adobe CX Enterprise [!DNL Audience Library], así como casos de uso comunes para distintos tipos de audiencias, consulte &quot;[Opciones de creación de audiencias](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)&quot;.

## Envío de datos de exposición de medios de DSP a Audience Manager

*Anunciantes solo con DSP*

Los clientes de DSP con Adobe Audience Manager pueden capturar datos de campañas de publicidad usando llamadas en píxeles a Audience Manager. A continuación, puede utilizar los datos de campaña para crear rasgos basados en reglas, que puede utilizar para definir nuevos segmentos y habilitar varios casos de uso de DSP, como segmentación más avanzada, administración de frecuencias, análisis de marketing y perspectivas de creación de informes.

Consulte &quot;[Información general sobre el envío de datos de exposición de medios de DSP a Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obtener más información.

## Obtenga información más completa sobre la actividad del sitio con Audience Analytics

Los clientes de Adobe Advertising con [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) pueden enviar datos seguidos por Adobe Advertising y segmentos de Audience Manager a [!DNL Analytics] para obtener información detallada sobre la actividad del sitio.

Para obtener más información, consulte &quot;[[!DNL Adobe Audience Analytics] para clientes de Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md)&quot;.
