---
title: Integraciones de Adobe Advertising con Adobe Analytics
description: Obtenga información sobre cómo Adobe Advertising puede intercambiar datos con Adobe Analytics y cómo puede utilizar los datos en Search, Social y Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Integraciones de Adobe Advertising con Adobe Analytics

Puede integrar Adobe Advertising con Analytics de las siguientes maneras.

## Intercambio de datos entre [!DNL Analytics] y ADOBE ADVERTISING

### Extraer [!DNL Analytics] Datos en Adobe Advertising

Con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] DSP y arrastre de forma hacia dentro:

* **[!DNL Analytics]segmentos:**  Metadatos, datos de jerarquía y datos de audiencia únicos para todos los segmentos de un anunciante o agencia creados en [!DNL Analytics] y publicado en el Experience Cloud.

* **[!DNL Analytics]métricas de participación del sitio**

* **[!DNL Analytics]métricas estándar, personalizadas y reservadas**

### Envío de datos de Adobe Advertising a [!DNL Analytics]

* **Métricas de tráfico de Adobe Advertising**

* **Dimension del Adobe Advertising**

>[!NOTE]
>
>Para [!DNL Search, Social, & Commerce]Sin embargo, esta función es compatible con la mayoría de las redes de anuncios y tipos de campañas. Consulte &quot;Inventario admitido&quot; en la [!DNL Search, Social, & Commerce] Guía para obtener más información.<!-- add link when that's published in ExL -->

### Uso [!DNL Analytics] Segmentos para crear [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes de inclusión con [!DNL Advertising Search, Social, & Commerce] solamente*

<!-- Verify all -->

En [!DNL Search, Social, & Commerce], puede crear [!DNL Google Ads] Las audiencias de coincidencia de clientes de Google de los ID de usuario de utilizan sus [!DNL Analytics] segmentos. Esto incluye segmentos de Adobe Analytics que se publican en Adobe Experience Cloud y segmentos que se crean con Adobe Experience Cloud [!DNL Audience Library]. Para obtener más información, consulte &quot;[Crear [!DNL Google Ads] audiencias de coincidencia de cliente de [!DNL Adobe] audiencias](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Audiencias de coincidencia de clientes a partir de ID de usuario](https://support.google.com/google-ads/answer/9199250) funcionan como las audiencias basadas en etiquetas de sitios web, pero se asigna un ID sin PII a los miembros de audiencia única para obtener beneficios distintos sobre las audiencias estándar basadas en etiquetas de sitio web y en coincidencias de clientes.

Para crear los ID de usuario necesarios, debe utilizar una etiqueta JavaScript de Adobe Advertising <!-- with a user ID parameter -->en sus sitios web. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

![proceso de creación de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Una vez creadas las audiencias, puede utilizarlas en [!DNL Google Ads] campañas como [objetivos o exclusiones a nivel de campaña o de grupo de anuncios](#audience-manager-targets).

### Uso [!DNL Analytics] Segmentos para segmentar o excluir anuncios {#analytics-targets}

* (Anunciantes de inclusión con [!DNL Search, Social, & Commerce]) Puede usar cualquiera [!DNL Google Ads] audiencias que fueron [creado mediante [!DNL Analytics] segmentos](#audience-manager-google-audiences) como objetivos o exclusiones de nivel de campaña o de nivel de grupo de publicidad en su [!DNL Google Ads] campañas.

* DSP (Anunciantes con el servicio de publicidad Puede utilizar el [!DNL Analytics] segmentos como destinatarios para sus ubicaciones de anuncios. Si lo desea, puede incluir los segmentos en audiencias reutilizables, que puede utilizar como destinos o exclusiones para varias ubicaciones.

* (Anunciantes con Advertising Creative) Puede utilizar su [!DNL Analytics] Segmentos como destinatarios de elementos creativos específicos en sus experiencias publicitarias.
