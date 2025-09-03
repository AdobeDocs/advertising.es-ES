---
title: Información general sobre la integración entre Adobe Advertising y Adobe Customer Journey Analytics
description: Obtenga información sobre las opciones para integrar Adobe Advertising con Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: fabe7312fc4d1ab899bedcf9eae1c8040a4a6532
workflow-type: tm+mt
source-wordcount: '425'
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

* (Próxima función beta) Los anunciantes con Customer Journey Analytics, pero no [!DNL Analytics for Advertising], pueden intercambiar datos de forma nativa entre Adobe Advertising y Customer Journey Analytics mediante [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es). Puede rastrear eventos de sitio usando cookies, IP con hash e ID universales ([!DNL LiveRamp RampIDs] e ID5) y atribuir eventos de sitio a actividad de medios de pago. Los siguientes datos están disponibles en los niveles de campaña, grupo de anuncios, paquete, ubicación y palabra clave:

   * Datos de rendimiento de campañas de Adobe Advertising en Customer Journey Analytics

     **Nota:** Los datos de [!DNL Apple] y [!DNL Tiktok] no están disponibles.

   * Actividad del sitio y conversiones rastreadas por [!DNL Google Ads] y [!DNL Microsoft Advertising] en Customer Journey Analytics

   * Datos de atribución de Customer Journey Analytics en Adobe Advertising, donde se pueden utilizar para la optimización y la creación de informes

  En este caso de uso, utilice Web SDK para realizar un seguimiento de los eventos del sitio (mediante cookies, direcciones IP con hash o identificadores universales) y atribuir los eventos del sitio a la actividad de medios de pago en [!DNL Google Ads], [!DNL Microsoft Advertising] y [!DNL Meta], así como en Adobe DSP. También utilizará Adobe Experience Platform para la recopilación de datos.

## Cómo iniciar una integración nativa entre Adobe Advertising y Customer Journey Analytics

Póngase en contacto con el equipo de su cuenta de Adobe, que completará la configuración inicial necesaria para comenzar y le ayudará a planificar su implementación y el uso de los datos en función de las necesidades de su organización.

>[!MORELIKETHIS]
>
>* [Requisitos previos](prerequisites.md)
>* [ID de Adobe Advertising usados por [!DNL Customer Journey Analytics]](ids.md)
>* [Configurar la recopilación de datos, la transferencia de datos y la creación de informes](set-up.md)
>* [Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics](advertising-data-in-cja.md)
>* (Usuarios de Adobe Analytics) [Recopilar datos históricos para los ID de AMO e ID de EF para su uso en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
