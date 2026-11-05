---
title: Administrar audiencias
description: Obtenga información acerca de la biblioteca de audiencias y cómo administrar las audiencias admitidas para Google Ads y Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%
---
# Administrar audiencias

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo cuentas*

Una audiencia es un grupo de usuarios que puedes usar como [objetivo](audience-targets-manage.md) o [exclusión](audience-exclusions.md) para campañas compatibles y grupos de anuncios en la misma red publicitaria. La red de anuncios determina el tamaño de la audiencia a la que se debe dirigir.

## Acerca de la vista [!UICONTROL Library] {#audience-view-about}

La vista [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Library] enumera las audiencias del anunciante seleccionado. Para ver las audiencias [!DNL Google Ads] y [!DNL Microsoft Advertising], seleccione **[!UICONTROL All Other Network]** en el menú **[!UICONTROL Network]**.

La biblioteca incluye [!DNL Google Ads] audiencias basadas en datos de clientes, en el mercado y similares, y [!DNL Microsoft Advertising] audiencias de remarketing, remarketing dinámico, personalizadas, de coincidencia de clientes, en el mercado y similares.

Para ver los datos se requiere el permiso [!UICONTROL View Audiences]. Para seleccionar filas y eliminar audiencias compatibles se requiere el permiso [!UICONTROL Edit Audience Library].

### Acciones disponibles

<!--
Restricted to internal beta users:

* [Create a customer match audience from a customer data list](#audience-customer-list-create)

* [Create a Google Ads audience from Adobe audiences](#audience-adobe-create)

* [Create a Microsoft Advertising dynamic remarketing audience](#audience-dynamic-create)

* [Update a customer match audience using a customer data list](#audience-customer-list-edit)

* [Edit a dynamic remarketing audience](#audience-dynamic-edit)
-->

* [Eliminación de una audiencia de remarketing dinámico](#audience-delete)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

## Fuentes de datos de audiencia {#audience-data-sources}

Puede utilizar audiencias basadas en las siguientes fuentes de datos:

* **Segmentos de audiencia de Adobe:** Los anunciantes con cuentas de Adobe Audience Manager o Adobe Analytics seleccionadas pueden usar [!DNL Google Ads] audiencias de coincidencia de clientes basadas en sus [!DNL Adobe] segmentos existentes.

  * Para los anunciantes con cuentas de [!DNL Analytics] que no tienen Audience Manager, las audiencias usan identificadores de usuario de [!DNL Analytics] segmentos compartidos con Adobe CX Enterprise.

  * Para los anunciantes con cuentas de Audience Manager, las audiencias utilizan ID de usuario de segmentos de Audience Manager que tienen Search, Social y Commerce como destino. Pueden incluir [!DNL Analytics] segmentos publicados en Adobe CX Enterprise y segmentos creados con la biblioteca de audiencias de Adobe CX Enterprise.

  La cuenta de [!DNL Google Ads] debe ser [elegible para la coincidencia de cliente](https://support.google.com/adspolicy/answer/6299717) y se ha suscrito para [segmentos de ID de usuario](https://support.google.com/google-ads/answer/9199250). La cuenta del anunciante en Buscar, Social y Commerce también debe configurarse para permitir la creación de audiencias de coincidencia de clientes. Póngase en contacto con el equipo de su cuenta de Adobe para habilitar la función.

  [!DNL Adobe] archivos de sincronización de cookies y datos de segmentos para audiencias basadas en datos de clientes se sincronizan diariamente con [!DNL Google Ads].

* **Listas de correos electrónicos de Adobe Campaign:** El equipo de tu cuenta de Adobe puede ayudarte a configurar un flujo de trabajo para crear y actualizar una audiencia de coincidencia de clientes de [!DNL Google Ads] desde una lista de correo electrónico de [!DNL Campaign]. El flujo de trabajo está configurado en [!DNL Campaign], no en la biblioteca de audiencias. Consulte &quot;[Crear una audiencia afín de clientes a partir de una lista de correo electrónico de Adobe Campaign](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)&quot;.

* **Listas de datos de clientes:** Los anunciantes con cuentas elegibles de [!DNL Google Ads] o [!DNL Microsoft Advertising] pueden usar audiencias de coincidencia de clientes basadas en archivos CSV que contienen identificadores principales de sus sistemas de administración de la relación con los clientes (CRM).

* **Listas de remarketing dinámico:** Los anunciantes con cuentas de [!DNL Microsoft Advertising] pueden usar audiencias basadas en usuarios que interactuaron recientemente con sus productos, como visores de productos o compradores anteriores. Estas audiencias requieren la etiqueta de seguimiento de conversión y audiencia JavaScript de la red de anuncios en las páginas web relevantes.

  Las audiencias de remarketing dinámico se pueden utilizar con campañas de compra en las redes de búsqueda y audiencia para redireccionar a los usuarios con anuncios de productos y con campañas de búsqueda para redireccionar a los usuarios con anuncios de texto y anuncios dinámicos de búsqueda.

  >[!NOTE]
  >
  >Los modificadores de oferta para los destinos de audiencia de remarketing dinámico no están optimizados en los portafolios con la configuración [!UICONTROL Auto-optimize Bid Adjustment Values].

>[!NOTE]
>
>Search, Social y Commerce no almacenan los datos de clientes que se cargan o los datos de clientes de [!DNL Adobe] segmentos utilizados para crear o editar una audiencia.

<!--
Restricted to internal beta users: audience creation and library editing.

## Create a customer match audience from a customer data list {#audience-customer-list-create}

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts that are eligible for customer match only*

For [!DNL Microsoft Advertising], the file can include email addresses. For [!DNL Google Ads], the file can include email addresses, mailing addresses, telephone numbers, user IDs, or mobile device IDs.

Creating and editing library audiences requires the [!UICONTROL Edit Audience Library] permission in addition to internal beta access.

1. Prepare a CSV file with the customer data in the required format.

   First and last names, email addresses, and telephone numbers must be hashed using SHA-256. Follow the network's formatting requirements for the selected identifier type. See the [Google Ads formatting guidelines](https://support.google.com/google-ads/answer/7476159) or the [Microsoft Advertising instructions for preparing customer match lists](https://help.ads.microsoft.com/#apex/ads/en/56921).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. In **[!UICONTROL Data Source]**, select the customer-list option.

1. Enter the **[!UICONTROL Audience Name]** and select the **[!UICONTROL Data Upload Type]**:

   * ([!DNL Microsoft Advertising]) **[!UICONTROL Emails]**.

   * ([!DNL Google Ads]) **[!UICONTROL Emails, Phones, and/or Mailing Addresses]**, **[!UICONTROL User IDs]**, or **[!UICONTROL Mobile Device IDs]**.

     User ID lists are available only to eligible [!DNL Google Ads] advertisers in the U.S. who are opted in for user ID segments.

1. (Mobile device ID lists only) Select the **[!UICONTROL OS Type]** and enter the **[!UICONTROL App ID]**.

   For an Android app, use its package name in [!DNL Google Play], such as `com.example.game` from `https://play.google.com/store/apps/details?id=com.example.game`. For an iOS app, use its application ID from the [!DNL App Store], such as `id284882215`. Your development team can provide the ID.

1. In **[!UICONTROL Select File]**, select the CSV file from your device or network.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. ([!DNL Google Ads]; optional) If you do business in the European Economic Area (EEA) or United Kingdom (UK) and have collected all required user consents, select the consent check box to send the consent status as **[!UICONTROL GRANTED]** for advertising and ad personalization.

   If you leave the check box unselected, the consent status is sent as **[!UICONTROL UNSPECIFIED]**. [!DNL Google Ads] ignores data for EEA and UK users with an unspecified consent status, which can cause data discrepancies and performance issues.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Membership days specify how long a user's cookie stays in the audience. Use the length of time for which you expect the ad to remain relevant. Customer lists don't expire unless you enter a value.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change a setting, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

The ad network may take up to 24 hours to process the file. See the [Google Ads documentation on customer match and its limitations](https://support.google.com/displayvideo/answer/9539301).

## Create Google Ads customer match audiences from Adobe audiences {#audience-adobe-create}

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

Each [!DNL Adobe] audience can be used for only one [!DNL Google Ads] audience. Each new audience has the same name as the original [!DNL Adobe] audience.

1. Complete the prerequisites:

   1. Ask an [!DNL Adobe] administrator or account manager to enable customer match audiences for the advertiser.

   1. Implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es){target="_blank"} version 2.0 or higher.

   1. Deploy the following tag as high as possible on the advertiser's webpages from which the audience should be tracked:

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      Replace `Advertising_Cloud_UserID` with the advertiser's unique numeric user ID.

   1. Have an authorized user [configure synchronization with the advertiser's organization account in Adobe CX Enterprise](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Google Ads] and the account.

1. In **[!UICONTROL Data Source]**, select the Adobe audience option.

1. In **[!UICONTROL Adobe Audience]**, select one or more available segments. You can search the list.

   Segments already used for another [!DNL Google Ads] audience aren't available. If you select multiple segments, a separate audience is created for each segment.

1. Select the available customer list user ID option in **[!UICONTROL Audience Type]**.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Remarketing lists have a maximum duration of 540 days. Customer lists don't have a maximum duration; enter 10000 to indicate that the cookie never expires.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Search, Social, & Commerce automatically pushes a [!DNL Google] tracking URL back to each source segment so that [!DNL Google] can track the audience. [!DNL Google] may take up to 24 hours to process the audience.

>[!TIP]
>
>For real-time segmentation, use Audience Manager-created audiences. [!DNL Analytics] segments synced to Adobe CX Enterprise may have smaller populations because they're synced daily. Users who qualify for a segment may not be included until the next day.

## Create a Microsoft Advertising dynamic remarketing audience {#audience-dynamic-create}

You can create multiple dynamic remarketing audiences using the same tracking tag.

1. Implement the [Microsoft Advertising universal event tracking (UET) tag with the required product ID and page type parameters](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85) on the relevant webpages. Identify the tag's name.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Microsoft Advertising] and the account.

1. In **[!UICONTROL Data Source]**, select the dynamic remarketing list option.

1. Enter the **[!UICONTROL Audience Name]**.

1. In **[!UICONTROL Tag Name]**, select the UET tag on the webpages whose users comprise the audience.

1. In **[!UICONTROL Whom to add to your audience]**, select **[!UICONTROL General Visitors]**, **[!UICONTROL Product Searchers]**, **[!UICONTROL Product Viewers]**, **[!UICONTROL Past Buyers]**, or **[!UICONTROL Shopping Cart Abandoners]**.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available. For dynamic remarketing audiences, membership can range from 1-180 days.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Dynamic remarketing audiences are eligible for targeting once they include at least 300 users.

## Update a customer match audience using a customer data list {#audience-customer-list-edit}

You can update customer match audiences created from data files, but not [!DNL Google Ads] audiences created from [!DNL Adobe] audiences. You can add or delete members, or replace all existing members. You can't edit multiple library audiences at once.

1. Prepare a CSV file in the required format, using the same data type as the original list. For mobile device IDs, use the same app and operating system.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. In **[!UICONTROL Select Action]**, select:

   * **[!UICONTROL Add]:** Add members from the uploaded file who aren't already in the audience.

   * **[!UICONTROL Delete]:** Remove members in the uploaded file from the audience.

   * **[!UICONTROL Replace]:** Replace all existing audience members with the uploaded data.

1. In **[!UICONTROL Select File]**, select the CSV file, accept the privacy policies, and configure the applicable consent setting.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.

The ad network may take a while to process audience updates.

## Edit a dynamic remarketing audience {#audience-dynamic-edit}

You can change a [!DNL Microsoft Advertising] dynamic remarketing audience's name, UET tag, and visitor type. You can't change its membership duration or edit multiple library audiences at once.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one dynamic remarketing audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. Edit the **[!UICONTROL Audience Name]**, **[!UICONTROL Tag Name]**, or **[!UICONTROL Whom to add to your audience]**.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.
-->

## Eliminación de una audiencia de remarketing dinámico {#audience-delete}

Puede eliminar [!DNL Microsoft Advertising] audiencias de remarketing dinámico de una en una. No puede eliminar otros tipos de audiencia [!DNL Google Ads] o [!DNL Microsoft Advertising] de la biblioteca.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Audiences]** y luego haga clic en la ficha **[!UICONTROL Library]**.

1. Seleccione **[!UICONTROL All Other Network]** del menú **[!UICONTROL Network]**.

1. Seleccione la casilla de verificación situada junto a una audiencia de remarketing dinámico.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Administrar destinatarios de audiencia para campañas y grupos de anuncios](audience-targets-manage.md)
>* [Administrar exclusiones de audiencia para campañas y grupos de anuncios](audience-exclusions.md)
