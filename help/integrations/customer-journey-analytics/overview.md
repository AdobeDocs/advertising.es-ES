---
title: Información general sobre la integración entre Adobe Advertising y Adobe Customer Journey Analytics
description: Obtenga información sobre las opciones para integrar Adobe Advertising con Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
TQID: https://experienceleague.adobe.com/nxn5AcKCc-xm-k5LXOcKIquNKyoXbt3soR5nhQR0w-E
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 358bcf190b36bd3c01e33a3d5762361a4a015393
workflow-type: tm+mt
source-wordcount: 498
ht-degree: 0%

---

# Información general sobre la integración entre Adobe Advertising y Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Anunciantes con Advertising DSP y[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising está integrado con Adobe Customer Journey Analytics para el uso compartido y la creación de informes de datos bidireccionales. Tiene dos opciones para configurar la integración:

* Los anunciantes con [!DNL Analytics for Advertising] y Customer Journey Analytics tienen la misma funcionalidad que tienen a través de [!DNL Analytics for Advertising], con la adición de visualizaciones en Customer Journey Analytics.

  Seguirá realizando el seguimiento de los eventos de pulsaciones mediante Adobe Experience Platform Web SDK (`alloy.js`) o el servicio de identidad de Adobe Experience Cloud (`visitorAPI.js`). Anunciantes con Advertising DSP seguirá utilizando un fragmento de JavaScript para rastrear eventos de visualización. Los datos disponibles en Customer Journey Analytics incluyen:

   * Datos de rendimiento de campañas de Adobe Advertising en Customer Journey Analytics

   * Actividad del sitio y conversiones rastreadas por [!DNL Google Ads] y [!DNL Microsoft Advertising] en Customer Journey Analytics, actualizadas a diario

   * Datos de atribución de [!DNL Analytics] en Adobe Advertising, donde se pueden usar para la optimización y generación de informes

  En este caso de uso, debe [recopilar de forma opcional datos históricos para los ID de AMO y EF para su uso en Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* Los anunciantes con Customer Journey Analytics pero no [!DNL Analytics for Advertising] pueden intercambiar datos de forma nativa entre Adobe Advertising y Customer Journey Analytics usando [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es). Puede rastrear eventos de sitio usando cookies, IP con hash e ID universales ([!DNL LiveRamp RampIDs] e ID5) y atribuir eventos de sitio a actividad de medios de pago. Los siguientes datos están disponibles en los niveles de campaña, grupo de anuncios, paquete, ubicación y palabra clave:

   * Datos de rendimiento de campañas de Adobe Advertising en Customer Journey Analytics

     **Nota:** Los datos de [!DNL Apple] y [!DNL Tiktok] no están disponibles.

   * Actividad del sitio y conversiones rastreadas por [!DNL Google Ads] y [!DNL Microsoft Advertising] en Customer Journey Analytics

   * Datos de atribución de Customer Journey Analytics en Adobe Advertising, donde se pueden utilizar para la optimización y la creación de informes

  En este caso de uso, utilice Web SDK para realizar un seguimiento de los eventos del sitio (mediante cookies, direcciones IP con hash o identificadores universales) y atribuir los eventos del sitio a la actividad de medios de pago en [!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Meta] y Adobe DSP. También utilizará Adobe Experience Platform para la recopilación de datos.

## Definiciones de los tipos de datos del informe

* **Datos de nivel de evento:** Eventos con marca de tiempo, como Sesiones, Vistas de páginas, Envíos de formularios de posibles clientes y Envíos de aplicaciones.

* **Datos de resumen:** Datos de informes agregados, como la plataforma de publicidad, la campaña, la ubicación, la impresión, los clics y los costos.

* **Datos de clasificación/dimensiones:** dimensiones de informes, como el nombre de la campaña de Adobe Advertising, el nombre del portafolio o el ID de ubicación. Puede buscar (filtrar) los datos de nivel de evento y los datos de resumen por clasificación/dimensión.

## Cómo iniciar una integración nativa entre Adobe Advertising y Customer Journey Analytics {#integration-cja-initiate}

Póngase en contacto con el equipo de su cuenta de Adobe, que completará la configuración inicial necesaria para comenzar y le ayudará a planificar su implementación y el uso de los datos en función de las necesidades de su organización.

>[!MORELIKETHIS]
>
>* [Requisitos previos](prerequisites.md)
>* [ID de Adobe Advertising usados por [!DNL Customer Journey Analytics]](ids.md)
>* [Configurar la recopilación de datos, la transferencia de datos y la creación de informes](set-up.md)
>* [Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics](advertising-data-in-cja.md)
>* (Usuarios de Adobe Analytics) [Recopilar datos históricos de ID de AMO e ID de EF para usarlos en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Solución de problemas](troubleshooting.md)
