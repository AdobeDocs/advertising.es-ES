---
title: Integraciones de Adobe Advertising con Adobe Analytics
description: Obtenga información sobre cómo el Adobe Advertising de puede intercambiar datos con Adobe Analytics y cómo puede utilizar los datos en Search, Social y Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Integraciones de Adobe Advertising con Adobe Analytics

Puede integrar Adobe Advertising con Analytics de las siguientes maneras.

## Intercambiar datos entre [!DNL Analytics] y el Adobe Advertising

### Extraer [!DNL Analytics] datos al Adobe Advertising

DSP Con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] y la extracción de la:

* **[!DNL Analytics]segmentos:** Metadatos, datos de jerarquía y datos de audiencia única para todos los segmentos de un anunciante o agencia creados en [!DNL Analytics] y publicados en el Experience Cloud.

* **[!DNL Analytics]métricas de participación del sitio**

* **[!DNL Analytics]métricas estándar, personalizadas y reservadas**

### Enviar datos de Adobe Advertising a [!DNL Analytics]

* **Métricas de tráfico del Adobe Advertising**

* **Dimension del Adobe Advertising**

>[!NOTE]
>
>Para [!DNL Search, Social, & Commerce], esta característica es compatible con la mayoría de las redes de anuncios y tipos de campañas. Consulte &quot;Inventario admitido&quot; en la guía [!DNL Search, Social, & Commerce] para obtener más información.<!-- add link when that's published in ExL -->

### Usar [!DNL Analytics] segmentos para crear [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes de inclusión con [!DNL Advertising Search, Social, & Commerce] solamente*

<!-- Verify all -->

En [!DNL Search, Social, & Commerce], puede crear [!DNL Google Ads] audiencias de coincidencia de clientes de Google a partir de los ID de usuario utilizando sus [!DNL Analytics] segmentos existentes. Esto incluye segmentos de Adobe Analytics que se publican en Adobe Experience Cloud y segmentos que se crean con Adobe Experience Cloud [!DNL Audience Library]. Para obtener más información, consulte &quot;[Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

Las [audiencias de coincidencia de clientes de los ID de usuario](https://support.google.com/google-ads/answer/9199250) funcionan como audiencias basadas en etiquetas de sitios web, pero se asigna un ID que no es PII a los miembros de audiencia única para obtener beneficios distintos sobre las audiencias estándar basadas en etiquetas de sitios web y las coincidencias de clientes.

Para crear los identificadores de usuario necesarios, debe usar una etiqueta JavaScript de Adobe Advertising <!-- with a user ID parameter --> en sus sitios web. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

![proceso de creación de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Una vez creadas las audiencias, puede usarlas en [!DNL Google Ads] campañas como [objetivos o exclusiones a nivel de campaña o de grupo de anuncios](#audience-manager-targets).

### Usar [!DNL Analytics] segmentos para segmentar o excluir anuncios {#analytics-targets}

* (Anunciantes incluidos con [!DNL Search, Social, & Commerce]) Puede usar cualquier audiencia de [!DNL Google Ads] que se haya [creado usando [!DNL Analytics] segmentos](#audience-manager-google-audiences) como objetivos o exclusiones a nivel de campaña o de grupo de anuncios en sus campañas de [!DNL Google Ads].

* DSP (Anunciantes con el servicio de publicidad) Puede usar sus [!DNL Analytics] segmentos existentes como destinatarios para sus ubicaciones de anuncios. Si lo desea, puede incluir los segmentos en audiencias reutilizables, que puede utilizar como destinos o exclusiones para varias ubicaciones.

* (Anunciantes con Advertising Creative) Puede usar sus [!DNL Analytics] segmentos existentes como destinatarios de elementos creativos específicos en sus experiencias publicitarias.
