---
title: Integración con soluciones y servicios de Adobe Experience Cloud
description: Obtenga información acerca de las integraciones de Search, Social y Commerce con las soluciones y los servicios de Adobe Experience Cloud.
source-git-commit: a9e23de134274d8f5004a908853c4132300b84e8
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Integración con soluciones y servicios de Adobe Experience Cloud

Advertising Search, Social y Commerce están integrados con lo siguiente [!DNL Adobe] productos.

* [Etiquetas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — Puede usar el [Extensión de Adobe Advertising Cloud](https://exchange.adobe.com/apps/ec/100155) para que Adobe Experience Platform cree etiquetas de seguimiento de conversión de Adobe Advertising, así como etiquetas de seguimiento de terceros, para sus páginas de aterrizaje de publicidad. (También puede hacer lo siguiente [cree etiquetas de seguimiento de conversión directamente en Search, Social y Commerce.](/help/search-social-commerce/tools/conversion-tag-generate.md).) Póngase en contacto con el equipo de cuenta de Adobe o con el equipo de implementación para obtener información que incluir en las etiquetas.

* Adobe Analytics — (función de inclusión) Adobe Advertising y [!DNL Analytics] están integrados de las siguientes maneras:

   * Adobe Publicidad y [!DNL Analytics] compartir datos sin problemas. [!DNL Analytics] puede enviar datos de participación y conversión de forma diaria a Search, Social y Commerce, donde los datos están disponibles para la optimización de anuncios y para la creación de informes. Además, los Adobes Advertising pueden enviar datos sobre el tráfico de anuncios, incluidas las impresiones, los clics y los costes, desde las redes de anuncios diariamente a [!DNL Analytics], donde los datos están disponibles en todas las herramientas de sistema de informes.

     Consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot; para obtener más información acerca de [!DNL Analytics] compatibilidad con cada red de publicidad y tipo de anuncio. Consulte también &quot;[Información general de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; para obtener más información sobre el intercambio de datos.

     Para intercambiar datos, tanto el Adobe Advertising como [!DNL Analytics] debe configurarse inicialmente. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información sobre la configuración inicial.

     >[!NOTE]
     >
     >De forma predeterminada, la variable [!DNL Analytics] Las métricas de no son visibles en las pantallas de Búsqueda, Social y Comercio. Debe especificar explícitamente [hacer que las métricas estén disponibles en las vistas, portafolios e informes de administración de campañas](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) después de [!DNL Adobe] El equipo de implementación ha configurado los eventos estándar o personalizados seleccionados para que pasen a la publicidad de Adobe. Si lo desea, puede cambiar los nombres de las métricas que se muestran (sin cambiarlos en [!DNL Analytics]). Puede hacer que las métricas sean visibles en la interfaz de usuario de y cambiarles el nombre desde [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

   * Anunciantes con [!DNL Analytics] pero no el Audience Manager puede [crear [!DNL Google Ads] audiencias de coincidencia de clientes](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) de [!DNL Analytics] segmentos que se comparten con Adobe Experience Cloud. Para ser elegible, un anunciante debe implementar la variable [Servicio de identidad de Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html) e implementar una etiqueta de en sus sitios web. A continuación, puede usar las audiencias de en [!DNL Google Ads] campañas como nivel de campaña o nivel de grupo de publicidad [objetivos](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [exclusiones](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Segmentos de Adobe Audience Manager: (función Opt-in) puede [crear [!DNL Google Ads] audiencias de coincidencia de clientes](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) a partir de segmentos de Audience Manager que tengan Search, Social y Commerce como destino. Esto puede incluir [!DNL Analytics] los segmentos que se publican en Adobe Experience Cloud y los segmentos que se crean con la biblioteca de audiencias de Adobe Experience Cloud. A continuación, puede usar las audiencias de en [!DNL Google Ads] campañas como nivel de campaña o nivel de grupo de publicidad [objetivos](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [exclusiones](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Consulte &quot;[Integraciones de Adobe Advertising con Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot; para obtener más información.

* Adobe Target: puede implementar el uso compartido de señales de pulsación entre Search, Social y Commerce, y [!DNL Target], configure una actividad de prueba A/B en [!DNL Target] para sus anuncios y, a continuación, utilice [!DNL Analytics] Analysis Workspace para ver los datos de prueba.

* Adobe Campaign: puede [crear y actualizar un [!DNL Google Ads] audiencia afín de clientes que usa una lista de correo electrónico en [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notificaciones de Adobe Experience Cloud: (cuando inicia sesión a través de Adobe Experience Cloud) Desde el vínculo de notificaciones ([Notificaciones de alerta](/help/search-social-commerce/assets/notifications-panel.png "Notificaciones de alerta")), en la parte superior de cada página puede ver todas las actualizaciones del sistema, las publicaciones, las menciones y los recursos compartidos de Adobe Experience Cloud. Póngase en contacto con el equipo de cuenta de Adobe para obtener información sobre el acceso a Adobe Experience Cloud.

