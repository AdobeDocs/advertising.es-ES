---
title: Configurar el rastreo de clics basado en cookies
description: Obtenga información sobre cómo configurar y validar etiquetas de seguimiento de clics.
exl-id: 340aec08-a1a5-4aa5-b666-9c819c1709d0
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Configurar el rastreo de clics basado en cookies

Para que Search, Social y Commerce rastreen los clics, se deben configurar y validar los siguientes elementos.

1. (Equipo de cuenta de Adobe) Configure el anunciante como un cliente en píxeles.

1. [Especifique las opciones de seguimiento correctas para cada una de las cuentas y campañas de red de anuncios del anunciante](#set-up-click-tracking-options).

1. Si es necesario, [genere direcciones URL de seguimiento y cárguelas](#generate-upload-tracking-urls) para algunos elementos de campaign.

1. [Valide el formato de algunas de las direcciones URL de rastreo de clics y pruébelas para validar que se abre la página de aterrizaje correcta](#validate-tracking-urls).

## Configurar las opciones de seguimiento para las cuentas y campañas de red de anuncios {#set-up-click-tracking-options}

*Administrador de cuentas de agencia, [!DNL Adobe] administrador de cuentas y roles de usuario administrador solamente*

1. Para cada cuenta de red de publicidad, haga lo siguiente:

   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Mantenga el cursor sobre el nombre de la cuenta y haga clic en ![Icono de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icono de menú"), y luego seleccione **[!UICONTROL Edit]**.

   1. Haga clic **[!UICONTROL Set Account Tracking]**.

   1. Para el [!UICONTROL Tracking Type] , seleccione **[!UICONTROL EF Redirect]**.

   1. (Para permitir que Search, Social y Commerce intercambien datos con Adobe Analytics o rastreen las conversiones que se producen en ). [!DNL Apple Safari]) Seleccione la [!UICONTROL Redirect Type] opción **[!UICONTROL Token]**.

   1. (Opcional) Active la **[!UICONTROL Auto Upload]** para cargar automáticamente nuevas direcciones URL de seguimiento en la red de publicidad la próxima vez que Search, Social y Commerce se sincronicen con ella. Este valor se hereda como predeterminado para todas las campañas de la cuenta, pero se puede sobrescribir en el nivel de campaña.

1. Para cada campaña, haga lo siguiente:

   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Mantenga el cursor sobre el nombre de la campaña y haga clic en ![Icono de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icono de menú"), y luego seleccione **[!UICONTROL Edit]**.

   1. Haga clic **[!UICONTROL Set Campaign Tracking]**. A continuación, seleccione la opción para **[!UICONTROL Override Account Tracking]**.

   1. Para el [!UICONTROL Tracking Type] , seleccione **[!UICONTROL EF Redirect]**.

   1. (Para permitir que Search, Social y Commerce intercambien datos con Adobe Analytics o rastreen las conversiones que se producen en ). [!DNL Apple Safari]) Seleccione la [!UICONTROL Redirect Type] opción **[!UICONTROL Token]**.

   1. (Opcional) Active la **[!UICONTROL Auto Upload]** para cargar automáticamente nuevas direcciones URL de seguimiento en la red de publicidad la próxima vez que Search, Social y Commerce se sincronicen con ella. Este valor se hereda como predeterminado para todas las campañas de la cuenta, pero se puede sobrescribir en el nivel de campaña.

## Generar y cargar direcciones URL de seguimiento {#generate-upload-tracking-urls}

Consulte &quot;[Cuándo y cómo generar URL de seguimiento de clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

### Prueba del formato de las direcciones URL de seguimiento de clics {#validate-tracking-urls}

Compruebe que se abre la página de aterrizaje correcta para la URL de seguimiento de clics.

1. Imita un clic en un anuncio enviando tráfico al entorno de ensayo del anunciante:

   1. En un editor de texto, pegue una URL de seguimiento de clics, cambie la URL de la página de aterrizaje para que apunte a la misma página dentro del entorno de ensayo del anunciante y, a continuación, pegue la nueva URL en la barra de direcciones del explorador y presione **[!DNL Enter]** clave.

   1. Busque la cookie en las cookies almacenadas del explorador.

   1. Complete una transacción en el sitio de ensayo y compruebe que la página de éxito activa el píxel correcto. Los parámetros reales rastreados por el píxel varían según el anunciante y la dirección URL de seguimiento. En el ejemplo siguiente, el anunciante desea rastrear la cantidad de aplicaciones nuevas y la cantidad de ingresos nuevos:

      Para un nuevo usuario final (con una cookie nueva), se debe activar el siguiente píxel:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Si la cookie no es nueva, se debe activar el siguiente píxel:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Repita el proceso para varias direcciones URL de rastreo de clics en el dominio.

1. Repita el paso 1 para cada dominio, utilizando una página de aterrizaje diferente en consecuencia.

1. Si es necesario, confirme que Buscar, Social y Comercio puede ver los píxeles de los ID de transacción (`ev_transid`) generado durante la prueba.

>[!MORELIKETHIS]
>
>* [Cuándo y cómo generar URL de seguimiento de clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
