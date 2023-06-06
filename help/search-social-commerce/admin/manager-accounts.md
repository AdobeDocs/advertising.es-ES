---
title: Administrar credenciales para cuentas de administrador de red de anuncios
description: Obtenga información sobre cómo proporcionar credenciales para su [!DNL Google Ads] cuentas de responsable.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Administrar credenciales para cuentas de administrador de red de anuncios

*Función beta*

*[!DNL Google Ads]solo cuentas*

Proporcione las credenciales para su [!DNL Google Ads] las cuentas de administrador en las que quiera que Search, Social y Commerce carguen conversiones entre cuentas. Utilice esta función si desea realizar una carga [!DNL Adobe]Métricas de conversión de varias cuentas con seguimiento personalizado a [!DNL Google Ads] cuenta de manager o b) cargar objetivos de portafolio que incluyan conversiones entre cuentas a [!DNL Google Ads] para la optimización híbrida.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Puede agregar credenciales para nuevos registros de cuenta de administrador o volver a autenticar una cuenta de administrador existente.

Una vez agregadas las credenciales de una cuenta de administrador, la configuración de la cuenta muestra el identificador de la cuenta de administrador asociado como de sólo lectura. Además, un &quot; opcional[!UICONTROL Manager Account for Cross-Account Conversions]&quot; en la columna [!UICONTROL Campaigns] > [!UICONTROL Accounts] La vista muestra el ID de cuenta de responsable de cada cuenta secundaria e indica un error cuando la cuenta de responsable no está autenticada. [!UICONTROL Notification Center] incluye notificaciones cuando faltan las credenciales de una cuenta de administrador ([el [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) o cuando caduca un token de autenticación de cuenta de administrador ([el [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Para agregar credenciales para una nueva cuenta de administrador

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Seleccionar **[!UICONTROL Create new manager account]**.

1. Introduzca las credenciales de inicio de sesión de la cuenta del responsable.

   El **[!UICONTROL Manager Account ID]** y **[!UICONTROL Login Email]** son obligatorios. Search, Social y Commerce capturan y almacenan automáticamente el token de la cuenta que se utilizará para la autenticación.

   Si lo desea, puede incluir un **[!UICONTROL MCC Account Name]** para la identificación dentro de Search, Social y Commerce, y la cuenta **[!UICONTROL Password]**. Introduzca la contraseña cuando desee cifrarla y guárdela para que el administrador de cuentas pueda actualizar los tokens según sea necesario.

1. Haga clic **[!UICONTROL Authenticate]**.

1. Haga clic **[!UICONTROL Save]**.

## Para volver a autenticar una cuenta de administrador existente

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Seleccionar **[!UICONTROL Reauthenticate existing manager account]**.

1. Seleccione la cuenta del responsable.

1. Introduzca las credenciales de inicio de sesión de la cuenta del responsable.

   El **[!UICONTROL Manager Account ID]** y **Correo electrónico de inicio** son obligatorios. Search, Social y Commerce capturan y almacenan automáticamente el token de la cuenta que se utilizará para la autenticación.

   Si lo desea, puede incluir un **[!UICONTROL MCC Account Name]** para la identificación dentro de Search, Social y Commerce, y la cuenta **[!UICONTROL Password]**. Introduzca la contraseña cuando desee cifrarla y guárdela para que el administrador de cuentas pueda actualizar los tokens según sea necesario.

1. Haga clic **[!UICONTROL Authenticate]**.

1. Haga clic **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Habilitar la carga de objetivos en las redes de publicidad](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Cargar métricas de conversión en [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Editar la configuración de notificaciones](/help/search-social-commerce/notifications/notification-edit.md)

