---
title: (Nueva interfaz de usuario) Administrar [!DNL Naver] cuentas solo para seguimiento
description: Aprenda a configurar y administrar los detalles de la cuenta en la nueva interfaz de usuario de una cuenta de  [!DNL Naver] .
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# (Nueva interfaz de usuario) Administrar [!DNL Naver] cuentas solo para seguimiento

*característica de Beta*

A continuación se proporcionan instrucciones para administrar [[!DNL Naver] cuentas](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) a fin de realizar un seguimiento, generar informes y visualizar el rendimiento de los anuncios que compra directamente en la red de anuncios. Search, Social y Commerce no sincronizan los datos con la red de anuncios, no proporcionan pujas automatizadas ni ofrecen ningún tipo de optimización o simulación.

Para obtener detalles acerca de la funcionalidad disponible, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Crear y agregar detalles de cuenta de red {#create-account}

Para habilitar el seguimiento de una cuenta, debe crear un registro de cuenta correspondiente que contenga las credenciales de acceso a la cuenta y con el estado *habilitado*.

>[!NOTE]
>
>Para crear una cuenta real en la red de anuncios, vaya al sitio web de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Haga clic en **[!UICONTROL Create Account]**.

1. Haga clic en el nombre de la red publicitaria y, a continuación, haga clic en **[!UICONTROL Next]**.

1. Especifique la [configuración de la cuenta](#account-settings-naver):

   1. En la ficha **[!UICONTROL Enter Account Details]**, especifique la configuración general de la cuenta.

   1. (Anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md)) Haga clic en la ficha **[!UICONTROL Set up Adobe Analytics]** y seleccione los [!DNL Analytics] grupos de informes que quiera usar para realizar el seguimiento y generar informes de la actividad de la campaña.

1. Haga clic en **[!UICONTROL Save]**.

## Editar los detalles de la cuenta de red del anuncio {#edit-account}

Para cambiar el nombre de la cuenta, cambiar el estado de la cuenta o cambiar los grupos de informes [!DNL Analytics] que se usan para el seguimiento y la creación de informes, edite los detalles de la cuenta.

>[!NOTE]
>
>Para editar una cuenta real en la red de anuncios, vaya al sitio web de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Seleccione la cuenta de cualquiera de las siguientes maneras:

   * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

   * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

1. Editar la [configuración de la cuenta](#account-settings-api):

   1. (Opcional) En la ficha **[!UICONTROL Account Details]**, edite los detalles de la cuenta.

   1. (Opcional; anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md)) Haga clic en la ficha **[!UICONTROL Set up Adobe Analytics]** y edite los [!DNL Analytics] grupos de informes que quiera usar para rastrear y generar informes sobre la actividad de la campaña.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Haga clic en **[!UICONTROL Save]**.

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## Configuración de cuenta de red de anuncios {#account-settings-api}

### Ficha [!UICONTROL Account Details]

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Nombre que se mostrará para la cuenta en Search, Social y Commerce.

>[!NOTE]
>
>Si tiene una integración de Search, Social y Commerce-Adobe Analytics y cambia el nombre de la cuenta de búsqueda, pida al equipo de cuenta de Adobe que actualice la asignación.

**[!UICONTROL Network Account ID]:** Identificador de cuenta asignado por la red de publicidad.

**[!UICONTROL Currency]:** La abreviatura de la moneda utilizada para la cuenta.

**[!UICONTROL Time Zone]:** Zona horaria del anunciante.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social y Commerce sincronizan los datos de campaña con la cuenta (cuando es compatible) y envían ofertas automatizadas o presupuestos de campaña para campañas en portafolios.

## Ficha [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md); opcional) Uno o más grupos de informes de Analytics a los que Search, Social y Commerce envían datos que se cargan para la red de anuncios, incluidas las clasificaciones de entidades y los datos de clics de la cuenta.

Para que los datos aparezcan en los grupos de informes, ya sea (a) la función de ID de AMO del lado del servidor debe estar configurada para la cuenta o (b) la configuración de nivel de anunciante a &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; debe estar habilitada. Además, la cuenta del anunciante [!DNL Analytics] debe estar configurada para recibir datos de Search, Social y Commerce. Para obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Acerca de las cuentas de red de anuncios](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
