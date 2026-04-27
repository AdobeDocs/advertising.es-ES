---
title: Crear  [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias
description: Aprenda a crear  [!DNL Google Ads] audiencias de coincidencia de cliente a partir de las audiencias existentes de Adobe Analytics y Audience Manager.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/Ep3X-eo2kcGlW3NsV3CJEKBkEapa-oAv0HLexc1xnhM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 586
ht-degree: 0%

---

# Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de las audiencias de Adobe Analytics y Audience Manager

*[!DNL Google Ads]cuentas elegibles para la coincidencia de clientes solamente*

*Anunciantes con una integración Adobe Advertising-Adobe Audience Manager o Adobe Advertising-Adobe Analytics solamente*

Los anunciantes de inclusión pueden crear audiencias de coincidencia de clientes de [!DNL Google Ads] con los ID de usuario a partir de: [!DNL Analytics] segmentos que se comparten con Adobe CX Enterprise y b) segmentos de Audience Manager que tienen Search, Social y Commerce como destino, incluidos [!DNL Analytics] segmentos publicados en Adobe CX Enterprise y segmentos creados con la biblioteca de audiencias de Adobe CX Enterprise. Search, Social y Commerce devuelven automáticamente una URL de seguimiento [!DNL Google] a cada segmento [!DNL Analytics] o Audience Manager para que [!DNL Google] pueda rastrear la audiencia.

Cada audiencia [!DNL Adobe] se puede usar para una sola audiencia [!DNL Google].

Cada nueva audiencia [!DNL Google] tiene el mismo nombre que la audiencia [!DNL Adobe] original. [!DNL Google] determina el tamaño de la audiencia que debe ser objetivo.

>[!TIP]
>
>Para la segmentación en tiempo real, utilice audiencias creadas por Audience Manager. Los segmentos creados en [!DNL Analytics] y sincronizados con Adobe CX Enterprise pueden tener poblaciones más pequeñas porque solo se sincronizan diariamente; es posible que un internauta que cumpla los requisitos para un segmento no se incluya en el segmento hasta el día siguiente. Los segmentos de [!DNL Analytics] tienen la fuente de datos &quot;grupo de informes - .&quot;

>[!NOTE]
>
>Search, Social y Commerce no almacenan los datos de clientes de sus segmentos de [!DNL Adobe] utilizados para crear o editar una audiencia de [!DNL Google].

1. Complete los requisitos previos según sea necesario:

   1. (Para crear audiencias de lista de remarketing con ID de usuario) Un usuario administrador de [!DNL Adobe] o administrador de cuentas debe seleccionar la configuración de nivel de anunciante para habilitar las audiencias de coincidencia de clientes.

   1. Implemente el [Servicio de identidad de Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html) versión 2.0 o superior.

   1. Implemente la siguiente etiqueta lo más alto posible en las páginas web del anunciante desde las que se debe realizar el seguimiento de la audiencia

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      donde `Advertising_Cloud_UserID` es el identificador numérico de usuario único asignado al anunciante.

      Ejemplo: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Si aún no se ha completado) Un usuario autorizado debe configurar la cuenta del anunciante para [sincronizar con la cuenta de organización del anunciante en Adobe CX Enterprise](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network and the account name, and then click **[!UICONTROL Continue]**.

1. Specify the audience information:

   1. In the **[!UICONTROL Data Source]** menu, select **[!UICONTROL Adobe Audience]**.

   1. Select the [!UICONTROL Adobe Audience] on which to base the [!DNL Google] audience.

      >[!NOTE]
      >
      >[!DNL Adobe] audiences that are already used for another [!DNL Google] audience aren&#39;t available.

      You can optionally search for audiences that contain a specific text string with a minimum of three characters. For any matching audience, click **[!UICONTROL Include]** to select it.

      If you select multiple [!DNL Adobe] audiences, then a separate [!DNL Google] audience is created for each.

   1. Select the **[!UICONTROL Audience Type]** to create: **[!UICONTROL Customer List_User ID]**.

      The advertiser&#39;s [!DNL Google Ads] account must be [eligible for custom match](https://support.google.com/adspolicy/answer/6299717) and opted in for [user ID remarketing](https://support.google.com/google-ads/answer/9199250).

   1. Select the check box to indicate that you agree with the terms of the [!DNL Adobe] and ad network privacy policies.

   1. Specify the number of **[!UICONTROL Membership Days]**, which is the number of days a user&#39;s cookie stays in the audience.

      Use the length of time for which you expect your ad to be relevant to the user. Remarketing lists have a maximum duration of 540 days. Customer lists don&#39;t have a maximum duration; to indicate that the cookie never expires, enter 10000.

   1. Click **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] may take up to 24 hours to process the file.
>
>* See [[!DNL Google Ads] documentation on how customer match works and limitations](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [About audiences](audience-about.md)
>* [Create a [!DNL Google Ads] customer match audience from an Adobe Campaign email list](google-audience-from-campaign-email-list.md)
>* [Manage customer match audiences using customer data lists](audience-from-customer-data-list.md)
>* [Manage dynamic remarketing audiences](audience-dynamic-remarketing-manage.md)
