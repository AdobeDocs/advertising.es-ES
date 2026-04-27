---
title: Integración con soluciones y servicios de Adobe CX Enterprise
description: Obtenga información acerca de las integraciones de Search, Social y Commerce con las soluciones y servicios de Adobe CX Enterprise.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
TQID: https://experienceleague.adobe.com/vIjCxWutfGn8H9-TqxLvztNazb9RWq7ECeoOQXLfyEw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: f2860a4b-f905-4545-bead-1bbc92564592
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 619
ht-degree: 0%

---

# Integración con soluciones y servicios de Adobe CX Enterprise

Advertising Search, Social y Commerce están integrados con los siguientes [!DNL Adobe] productos.

* [Etiquetas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html): puede usar la [extensión de Adobe Advertising Cloud](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) para Adobe Experience Platform para [crear etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md), así como etiquetas de seguimiento de terceros, para sus páginas de aterrizaje de anuncios. Si su organización no tiene una cuenta de Experience Platform, puede instalar la extensión directamente en la [interfaz de usuario para la recopilación de datos de Adobe Experience Platform](https://experience.adobe.com/#/data-collection/), que está disponible de forma gratuita para los clientes de Adobe CX Enterprise.

  Para instalar la extensión necesaria, póngase en contacto con el administrador de su organización para obtener acceso a las funciones de recopilación de datos en la interfaz de usuario y pídale que le conceda el permiso `manage_properties`.

  **Nota:** También puedes [crear etiquetas de seguimiento de conversión directamente en Search, Social y Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — (función Opt-in) Adobe Advertising y [!DNL Analytics] se integran de las siguientes maneras:

   * Adobe Advertising y [!DNL Analytics] comparten datos sin problemas. [!DNL Analytics] puede enviar datos de participación y conversión de forma diaria a Search, Social y Commerce, donde los datos están disponibles para la optimización de anuncios y para la creación de informes. Además, Adobe Advertising puede enviar datos sobre el tráfico de anuncios, incluidas las impresiones, los clics y los costes, desde las redes de anuncios diariamente a [!DNL Analytics], donde los datos están disponibles en todas las herramientas de creación de informes.

     Consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot; para obtener más información sobre la compatibilidad con [!DNL Analytics] para cada red de anuncios y tipo de anuncio. Consulte también &quot;[Información general de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; para obtener más información sobre el intercambio de datos.

     Para intercambiar datos, Adobe Advertising y [!DNL Analytics] deben estar configurados inicialmente. Póngase en contacto con el equipo de su cuenta de Adobe para obtener más información sobre la configuración inicial.

     >[!NOTE]
     >
     >De manera predeterminada, las métricas [!DNL Analytics] no son visibles en las pantallas de Search, Social y Commerce. Debe [hacer que las métricas estén explícitamente disponibles en las vistas de administración de campañas, portafolios e informes](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) después de que el equipo de implementación de [!DNL Adobe] haya configurado los eventos estándar o personalizados seleccionados para pasarlos a Adobe Advertising. Si lo desea, puede cambiar los nombres de las métricas que se muestran (sin cambiarlos en [!DNL Analytics]). Puede hacer que las métricas sean visibles en la interfaz de usuario y cambiarles el nombre desde [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Los anunciantes con [!DNL Analytics] pero no Audience Manager pueden [crear [!DNL Google Ads] audiencias de coincidencia de clientes](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) a partir de [!DNL Analytics] segmentos compartidos con Adobe CX Enterprise. Para ser elegible, un anunciante debe implementar el [servicio de identidad de Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html) e implementar una etiqueta en sus sitios web. A continuación, puede usar las audiencias en [!DNL Google Ads] campañas como [objetivos](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [exclusiones](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) a nivel de campaña o de grupo de anuncios.

* Segmentos de Adobe Audience Manager: (función de inclusión) puede [crear [!DNL Google Ads] audiencias de coincidencia de clientes](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) a partir de segmentos de Audience Manager que tengan como destino Search, Social y Commerce. Esto puede incluir [!DNL Analytics] segmentos publicados en Adobe CX Enterprise y segmentos creados con la Biblioteca de audiencias de Adobe CX Enterprise. A continuación, puede usar las audiencias en [!DNL Google Ads] campañas como [objetivos](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) o [exclusiones](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) a nivel de campaña o de grupo de anuncios.

  Consulte &quot;[Integraciones de Adobe Advertising con Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot; para obtener más información.

* Adobe Target: puede implementar el uso compartido de señales de pulsación entre Search, Social y Commerce y [!DNL Target], configurar una actividad de prueba A/B en [!DNL Target] para sus anuncios y, a continuación, usar [!DNL Analytics] Analysis Workspace para ver los datos de prueba.

* Adobe Campaign: puedes [crear y actualizar una audiencia de  [!DNL Google Ads] customer match usando una lista de correo electrónico en [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notificaciones de Adobe CX Enterprise: (cuando haya iniciado sesión a través de Adobe CX Enterprise) Desde el vínculo de notificaciones ([Notificaciones de alerta](/help/search-social-commerce/assets/notifications-panel.png "Notificaciones de alerta")) en la parte superior de cada página, puede ver todas las actualizaciones del sistema, publicaciones, menciones y recursos compartidos de Adobe CX Enterprise. Póngase en contacto con el equipo de su cuenta de Adobe para obtener información sobre el acceso a Adobe CX Enterprise.
