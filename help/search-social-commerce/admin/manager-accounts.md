---
title: Administrar credenciales para cuentas de administrador de red de anuncios
description: Aprenda a proporcionar credenciales para sus cuentas de  [!DNL Google Ads] manager.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 4cf04fc7ea22e50b5f56cd278ad9a1aac724edf7
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# Administrar credenciales para cuentas de administrador de red de anuncios

*[!DNL Google Ads]solo cuentas*

Proporcione las credenciales de las cuentas de administrador de [!DNL Google Ads] en las que quiera que Search, Social y Commerce carguen las conversiones entre cuentas. Utilice esta característica si desea a) cargar métricas de conversión entre cuentas con seguimiento de [!DNL Adobe] en una cuenta de administrador de [!DNL Google Ads] o b) cargar objetivos de portafolio que incluyan conversiones entre cuentas en [!DNL Google Ads] para la optimización híbrida.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Puede agregar credenciales para nuevos registros de cuenta de administrador o volver a autenticar una cuenta de administrador existente.

Una vez agregadas las credenciales de una cuenta de administrador, la configuración de la cuenta muestra el identificador de la cuenta de administrador asociado como de sólo lectura. Además, una columna &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; opcional en la vista [!UICONTROL Campaigns] > [!UICONTROL Accounts] muestra el identificador de la cuenta de administrador de cada cuenta secundaria e indica un error cuando la cuenta de administrador no está autenticada. [!UICONTROL Notification Center] incluye notificaciones cuando faltan las credenciales de una cuenta de administrador ([el [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) o cuando caduca un token de autenticación de cuenta de administrador ([el [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Para agregar credenciales para una nueva cuenta de administrador

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Seleccione **[!UICONTROL Create new manager account]**.

1. Introduzca las credenciales de inicio de sesión de la cuenta del responsable.

   Se requieren **[!UICONTROL Manager Account ID]** y **[!UICONTROL Login Email]**. Search, Social y Commerce capturan y almacenan automáticamente el token de cuenta que se utilizará para la autenticación.

   Si lo desea, puede incluir un **[!UICONTROL MCC Account Name]** para su identificación en Search, Social y Commerce, y en la cuenta **[!UICONTROL Password]**. Introduzca la contraseña cuando desee cifrarla y guárdela para que el administrador de cuentas pueda actualizar los tokens según sea necesario.

1. Haga clic en **[!UICONTROL Authenticate]**.

1. Haga clic en **[!UICONTROL Save]**.

## Para volver a autenticar una cuenta de administrador existente

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Seleccione **[!UICONTROL Reauthenticate existing manager account]**.

1. Seleccione la cuenta del responsable.

1. Introduzca las credenciales de inicio de sesión de la cuenta del responsable.

   Se requieren **[!UICONTROL Manager Account ID]** y **el correo electrónico de inicio de sesión**. Search, Social y Commerce capturan y almacenan automáticamente el token de cuenta que se utilizará para la autenticación.

   Si lo desea, puede incluir un **[!UICONTROL MCC Account Name]** para su identificación en Search, Social y Commerce, y en la cuenta **[!UICONTROL Password]**. Introduzca la contraseña cuando desee cifrarla y guárdela para que el administrador de cuentas pueda actualizar los tokens según sea necesario.

1. Haga clic en **[!UICONTROL Authenticate]**.

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Habilitar la carga de objetivos en las redes de anuncios](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Cargar métricas de conversión a [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Editar la configuración de notificaciones](/help/search-social-commerce/notifications/notification-edit.md)
