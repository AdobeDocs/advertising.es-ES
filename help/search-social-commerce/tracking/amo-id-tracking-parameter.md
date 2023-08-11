---
title: El parámetro de seguimiento de ID de AMO (s_kwcid)
description: Obtenga información acerca del parámetro de seguimiento utilizado para compartir datos de Adobe Advertising con Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# El parámetro de seguimiento de ID de AMO (s_kwcid)

*Anunciantes solo con una integración de Adobe Advertising y Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe Advertising comparte datos sobre sus campañas con Adobe Analytics mediante el parámetro de datos anexados de ID de AMO, también denominado `s_kwcid` , que consiste en elementos específicos del canal de publicidad y de la red de publicidad.

<!-- add everything below to IDs page -->

El parámetro se añade a las direcciones URL de seguimiento de una de las siguientes maneras:

* (Recomendado) Se implementa la función de inserción del lado del servidor.

  Para [!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas con el [!UICONTROL Auto Upload] Con la configuración habilitada para la cuenta o campaña, el servidor de píxeles anexa automáticamente el parámetro de ID de AMO a los sufijos de la página de aterrizaje cuando un usuario final hace clic en un anuncio <!-- click a search ad or views a display ad --> con el píxel de Adobe Advertising.

  Para otras redes de publicidad, o [!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas con el [!UICONTROL Auto Upload] Si la opción está deshabilitada, agregue manualmente el parámetro de ID de AMO a los parámetros de datos anexados de nivel de cuenta, los cuales lo adjuntarán a las direcciones URL base.

* <!-- (Search, Social, & Commerce only) -->La función de inserción del lado del servidor no está implementada y debe agregar manualmente el parámetro de ID de AMO a su ([!DNL Google Ads] y [!DNL Microsoft Advertising]) sufijos de página de aterrizaje o (otras redes de anuncios) parámetros de datos anexados de nivel de cuenta.

Para implementar la función de inserción del lado del servidor o para determinar la mejor opción para su empresa, hable con el equipo de cuenta de Adobe.

DSP Para los formatos de ID de AMO para los servicios de búsqueda, búsqueda, medios sociales y comercio de, consulte &quot;[ID de Adobe Advertising utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [ID de Adobe Advertising utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [Administrar las cuentas de red de publicidad](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Configuración de campaña de Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Configuración de campañas de Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Configuración de campañas de Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Configuración de campañas de anuncios de Japón](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Configuración de campaña de Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
