---
title: (Nueva IU) Administrar credenciales para cuentas de administrador de Google Ads
description: Obtenga información sobre cómo configurar y administrar credenciales para cuentas de administrador de Google Ads en la nueva interfaz de usuario.
feature: Search Admin
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# (Nueva interfaz de usuario) Administrar credenciales para cuentas de administrador de [!DNL Google Ads]

*característica de Beta*

*[!DNL Google Ads]solo cuentas*

Proporcione credenciales para las cuentas de administrador de [!DNL Google Ads] en las que quiera que Search, Social y Commerce carguen conversiones entre cuentas. Utilice esta característica si desea a) cargar métricas de conversión entre cuentas con seguimiento de [!DNL Adobe] en una cuenta de administrador de [!DNL Google Ads] o b) cargar objetivos de portafolio que incluyan conversiones entre cuentas en [!DNL Google Ads] para la optimización híbrida.

Puede agregar credenciales para nuevos registros de cuenta de administrador o volver a autenticar una cuenta de administrador existente.

Una vez agregadas las credenciales de una cuenta de administrador, la configuración de la cuenta muestra el identificador de la cuenta de administrador asociado como de sólo lectura. [!UICONTROL Notification Center] incluye [notificaciones](/help/search-social-commerce/new-ui/notifications-manage.md) cuando faltan las credenciales de una cuenta de administrador (la [!UICONTROL Manager Account Missing Error]) o cuando caduca un token de autenticación de cuenta de administrador (la [!UICONTROL Manager Account Auth Error]).

## Agregar credenciales para una nueva cuenta de administrador {#create-manager-account}

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Haga clic en **[!UICONTROL +]**.

1. Seleccione la red de anuncios y haga clic en **[!UICONTROL Next]**.

1. Especifique la [configuración de la cuenta del administrador](#manager-account-settings).

1. Haga clic en **[!UICONTROL Authenticate]** e inicie sesión con las credenciales de la cuenta de administrador.

   Search, Social y Commerce capturan y almacenan automáticamente el token de autenticación.

1. En Buscar, Social y Commerce, haga clic en **[!UICONTROL Save]**.

## Editar detalles de la cuenta del responsable {#edit-manager-account}

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Seleccione la cuenta de cualquiera de las siguientes maneras:

   * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

   * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y luego haga clic en (/help/search-social-commerce/assets/edit-new.png &quot;Editar&quot;).

1. Edite la [configuración de la cuenta de administrador](#manager-account-settings).

1. Haga clic en **[!UICONTROL Re-Authenticate]** e inicie sesión con las credenciales de la cuenta de administrador.

   Search, Social y Commerce capturan y almacenan automáticamente el token de autenticación.

1. En Buscar, Social y Commerce, haga clic en **[!UICONTROL Save]**.

## Volver a autenticar una cuenta de administrador {#reauthenticate-manager-account}

Vuelva a autenticar una cuenta de administrador cuando el token de OAuth caduque o deje de ser válido.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Reauthenticate]**.

1. Inicie sesión con las credenciales de la cuenta de administrador.

   Search, Social y Commerce capturan y almacenan automáticamente el nuevo token de autenticación.

## Configuración de cuenta del responsable {#manager-account-settings}

**[!UICONTROL Manager Account ID]:** Identificador único de la cuenta de administrador en la red de anuncios.

**[!UICONTROL Mnaager Account Name]:** Nombre que se mostrará para la cuenta de administrador en Search, Social y Commerce.

**[!UICONTROL Login Email]:** La dirección de correo electrónico asociada con el inicio de sesión de la cuenta de administrador. Necesario para la autenticación.

**[!UICONTROL Password]:** (opcional) La contraseña de la cuenta. Introduzca la contraseña cuando desee cifrarla y guárdela para que el administrador de cuentas pueda actualizar los tokens según sea necesario.

>[!MORELIKETHIS]
>
>* [Habilitar la carga de objetivos en las redes de anuncios](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [Administrar notificaciones](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
