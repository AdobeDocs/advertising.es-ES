---
title: Integración con soluciones y servicios de Adobe Experience Cloud
description: Obtenga información acerca de las integraciones de Search, Social y Commerce con las soluciones y servicios de Adobe Experience Cloud.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Integración con soluciones y servicios de Adobe Experience Cloud

Advertising Search, Social y Commerce están integrados con los siguientes [!DNL Adobe] productos.

* [Etiquetas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html): puede usar la [extensión de Adobe Advertising Cloud](https://exchange.adobe.com/apps/ec/100155) para Adobe Experience Platform para crear etiquetas de seguimiento de conversión de Adobe Advertising, así como etiquetas de seguimiento de terceros, para sus páginas de aterrizaje de anuncios. (También puede [crear etiquetas de seguimiento de conversión directamente en Search, Social y Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md)). Póngase en contacto con el equipo de cuenta de Adobe o con el equipo de implementación para obtener información que incluir en las etiquetas.

* El Adobe Advertising Adobe Analytics — (característica de inclusión) y [!DNL Analytics] se integran de las siguientes maneras:

   * El Adobe Advertising y [!DNL Analytics] comparten datos sin problemas. [!DNL Analytics] puede enviar datos de participación y conversión de forma diaria a Search, Social y Commerce, donde los datos están disponibles para la optimización de anuncios y para la creación de informes. Además, el Adobe Advertising puede enviar datos sobre el tráfico de anuncios, incluidas las impresiones, los clics y los costos, desde las redes de anuncios diariamente a [!DNL Analytics], donde los datos están disponibles en todas las herramientas de generación de informes.

     Consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot; para obtener más información sobre la compatibilidad con [!DNL Analytics] para cada red de anuncios y tipo de anuncio. Consulte también &quot;[Información general sobre [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; para obtener más información acerca del intercambio de datos.

     Para intercambiar datos, tanto el Adobe Advertising como [!DNL Analytics] deben configurarse inicialmente. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información sobre la configuración inicial.

     >[!NOTE]
     >
     >De manera predeterminada, las métricas [!DNL Analytics] no son visibles en las pantallas de Search, Social y Commerce. Debe [hacer que las métricas estén explícitamente disponibles en las vistas de administración de campañas, portafolios e informes](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) después de que el equipo de implementación de [!DNL Adobe] haya configurado los eventos estándar o personalizados seleccionados para que pasen al Adobe Advertising. Si lo desea, puede cambiar los nombres de las métricas que se muestran (sin cambiarlos en [!DNL Analytics]). Puede hacer que las métricas sean visibles en la interfaz de usuario y cambiarles el nombre desde [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Los anunciantes con [!DNL Analytics] pero no el Audience Manager pueden [crear [!DNL Google Ads] audiencias de coincidencia de clientes](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) a partir de [!DNL Analytics] segmentos que se comparten con Adobe Experience Cloud. Para ser elegible, un anunciante debe implementar el [servicio de identidad de Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html) e implementar una etiqueta en sus sitios web. A continuación, puede usar las audiencias en [!DNL Google Ads] campañas como [objetivos](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [exclusiones](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) a nivel de campaña o de grupo de anuncios.

* Segmentos de Adobe Audience Manager: (función de inclusión) puede [crear [!DNL Google Ads] audiencias de coincidencia de clientes](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) a partir de segmentos de Audience Manager que tengan como destino Search, Social y Commerce. Esto puede incluir [!DNL Analytics] segmentos publicados en Adobe Experience Cloud y segmentos creados con la Biblioteca de audiencias de Adobe Experience Cloud. A continuación, puede usar las audiencias en [!DNL Google Ads] campañas como [objetivos](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [exclusiones](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) a nivel de campaña o de grupo de anuncios.

  Consulte &quot;[Integraciones de Adobe Advertising con Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot; para obtener más información.

* Adobe Target: puede implementar el uso compartido de señales de pulsación entre Search, Social y Commerce y [!DNL Target], configurar una actividad de prueba A/B en [!DNL Target] para sus anuncios y, a continuación, usar [!DNL Analytics] Analysis Workspace para ver los datos de prueba.

* Adobe Campaign: puedes [crear y actualizar una audiencia de  [!DNL Google Ads] customer match usando una lista de correo electrónico en [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notificaciones de Adobe Experience Cloud: (cuando haya iniciado sesión a través de Adobe Experience Cloud) Desde el vínculo de notificaciones ([Notificaciones de alerta](/help/search-social-commerce/assets/notifications-panel.png "Notificaciones de alerta")) en la parte superior de cada página, puede ver todas las actualizaciones del sistema, publicaciones, menciones y recursos compartidos de Adobe Experience Cloud. Póngase en contacto con el equipo de cuenta de Adobe para obtener información sobre el acceso a Adobe Experience Cloud.
