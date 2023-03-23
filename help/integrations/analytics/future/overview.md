---
title: Integraciones de publicidad de Adobe con Adobe Analytics
description: Obtenga información sobre cómo la publicidad de Adobe puede intercambiar datos con Adobe Analytics y cómo puede utilizar los datos en Buscar, Social y Comercio.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 06996ee9eb635fe204c0c3938e6937e8871c8a90
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Integraciones de publicidad de Adobe con Adobe Analytics

Puede integrar la publicidad de Adobe con Analytics de las siguientes maneras.

## Intercambiar datos entre [!DNL Analytics] y publicidad de Adobe

### Pull [!DNL Analytics] Datos en publicidad de Adobe

con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] y DSP extraer:

* **[!DNL Analytics]segmentos:**  Metadatos, datos de jerarquía y datos de audiencia únicos para todos los segmentos de un anunciante o de una agencia creados en [!DNL Analytics] y publicado para el Experience Cloud.

* **[!DNL Analytics]métricas de participación del sitio**

* **[!DNL Analytics]métricas estándar, personalizadas y reservadas**

### Enviar datos publicitarios de Adobe a [!DNL Analytics]

* **Métricas de tráfico de la publicidad de Adobe**

* **Dimension de publicidad de Adobe**

>[!NOTE]
>
>Para [!DNL Search, Social, & Commerce], esta función es compatible con la mayoría de las redes de anuncios y tipos de campañas. Consulte &quot;Inventario compatible&quot; en la sección [!DNL Search, Social, & Commerce] Guía para obtener más información.<!-- add link when that's published in ExL -->

### Uso [!DNL Analytics] Segmentos para crear [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes de inclusión con [!DNL Advertising Search, Social, & Commerce] only*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], puede crear [!DNL Google Ads] Los clientes de Google hacen coincidir las audiencias de los ID de usuario que usan su [!DNL Analytics] segmentos. Esto incluye los segmentos de Adobe Analytics que se publican en Adobe Experience Cloud y los segmentos que se crean mediante Adobe Experience Cloud [!DNL Audience Library]. Para obtener más información, consulte la ayuda del producto en [!DNL Search, Social, & Commerce].

[Audiencias de coincidencia del cliente con ID de usuario](https://support.google.com/google-ads/answer/9199250) funcionan como las audiencias basadas en etiquetas de sitios web, pero se asigna un ID que no es de PII a miembros de audiencia únicos para obtener ventajas distintas con respecto a las audiencias estándar de coincidencia de clientes y las basadas en etiquetas de sitios web.

Para crear los ID de usuario necesarios, debe utilizar una etiqueta JavaScript de publicidad de Adobe <!-- with a user ID parameter -->en sus sitios web. Póngase en contacto con su equipo de cuentas de Adobe para obtener más información.

![proceso de creación de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Una vez que haya creado las audiencias, puede utilizarlas en [!DNL Google Ads] campañas como [objetivos o exclusiones a nivel de campaña o de grupo de anuncios](#audience-manager-targets).

### Uso [!DNL Analytics] Segmentos para anuncios de destino o exclusión {#analytics-targets}

* (Anunciantes de inclusión con [!DNL Search, Social, & Commerce]) Puede usar cualquier [!DNL Google Ads] audiencias que eran [creado mediante [!DNL Analytics] segmentos](#audience-manager-google-audiences) como objetivos o exclusiones a nivel de campaña o de grupo de anuncios en su [!DNL Google Ads] campañas.

* (Anunciantes con DSP) Puede utilizar su [!DNL Analytics] segmentos como objetivos para las ubicaciones de publicidades. Si lo desea, puede incluir los segmentos en audiencias reutilizables, que puede utilizar como destinos o exclusiones para varias ubicaciones.

* (Anunciantes con Advertising Creative) Puede utilizar su [!DNL Analytics] segmentos como objetivos para creativos específicos en sus experiencias publicitarias.
