---
title: El parámetro de seguimiento de ID de AMO (s_kwcid)
description: Obtenga información acerca del parámetro de seguimiento utilizado para compartir datos de Adobe Advertising con Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# El parámetro de seguimiento de ID de AMO (s_kwcid)

*Anunciantes solo con una integración de Adobe Advertising y Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe Advertising comparte datos sobre sus campañas con Adobe Analytics mediante el parámetro de datos anexados de ID de AMO, también denominado `s_kwcid` , que consiste en elementos específicos del canal de publicidad y de la red de publicidad.

El parámetro se añade a las direcciones URL de seguimiento de una de las siguientes maneras:

* (Recomendado) Se implementa la función de inserción del lado del servidor.

   * DSP Clientes de: El servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final ve un anuncio en pantalla con el píxel de Adobe Advertising.

   * Clientes de Search, Social y Commerce:

      * Para [!DNL Google Ads] y [!DNL Microsoft® Advertising] cuentas con el [!UICONTROL Auto Upload] con la configuración habilitada para la cuenta o campaña, el servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final hace clic en un anuncio con el píxel de Adobe Advertising.

      * Para otras redes de publicidad, o [!DNL Google Ads] y [!DNL Microsoft® Advertising] cuentas con el [!UICONTROL Auto Upload] Si la opción está desactivada, añada manualmente el parámetro a los parámetros de adición de nivel de cuenta, que lo adjuntan a las direcciones URL base.

* La función de inserción del lado del servidor no está implementada:

   * DSP clientes de:

      * Para [!DNL Flashtalking] Para agregar etiquetas, inserte manualmente macros adicionales por &quot;[Añadir [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Para [!DNL Google Campaign Manager 360] Para agregar etiquetas, inserte manualmente macros adicionales por &quot;[Añadir [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Clientes de Search, Social y Commerce:

      * Para ([!DNL Google Ads] y [!DNL Microsoft® Advertising]), agregue manualmente el parámetro de ID de AMO a los sufijos de la página de aterrizaje.

      * Para los anuncios del resto de redes de anuncios, agregue manualmente el parámetro de ID de AMO a los parámetros de datos anexados de nivel de cuenta, que lo adjuntan a las direcciones URL base.

Para implementar la función de inserción del lado del servidor o para determinar la mejor opción para su empresa, hable con el equipo de cuenta de Adobe.

DSP Para los formatos de ID de AMO para los servicios de búsqueda, búsqueda, medios sociales y comercio de, consulte &quot;[ID de Adobe Advertising utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [ID de Adobe Advertising utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* (Búsqueda, Social Y Comercio) [Administrar las cuentas de red de publicidad](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* (Búsqueda, Social Y Comercio) [Configuración de campaña de Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* (Búsqueda, Social Y Comercio) [Configuración de campañas de Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* (Búsqueda, Social Y Comercio) [Configuración de campañas de Microsoft® Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* (Búsqueda, Social Y Comercio) [Yahoo! Configuración de campañas de anuncios de Japón](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* (Búsqueda, Social Y Comercio) [Configuración de campaña de Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
