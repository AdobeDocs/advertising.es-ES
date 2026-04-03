---
title: Habilitar y deshabilitar notificaciones push de [!UICONTROL Notification Center]
description: Obtenga información sobre cómo habilitar y deshabilitar las notificaciones push desde [!UICONTROL Notification Center].
exl-id: f0e91e76-eb1e-4ff0-9a52-e9bc587552a2
feature: Search Notifications
TQID: https://experienceleague.adobe.com/k-ujCPcKXYOMfYscQOoSQBHrEmW3Pz08nndz-xdTJaA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

---

# Habilitar y deshabilitar notificaciones push de [!UICONTROL Notification Center]

*Característica de Beta*

Puede activar las notificaciones en Buscar, Social y Commerce, donde aparecerán según las convenciones de notificación del explorador. En dispositivos que usan [!DNL Microsoft Windows], las notificaciones se muestran en la parte inferior derecha de la pantalla (bandeja del sistema). En [!DNL Apple Mac] dispositivos, las notificaciones se muestran en el menú derecho.

Las notificaciones push están disponibles en los siguientes exploradores:

* [!DNL Google Chrome] 40 y superior

* [!DNL Microsoft Edge] 17 y posterior

* [!DNL Mozilla Firefox] 44 y superior

Puede desactivar las notificaciones push según el procedimiento estándar del explorador.

## Habilitar notificaciones push

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Insights & Reports]** > **[!UICONTROL Notification Center Beta]**.

2. En la parte inferior derecha, haga clic en ![Habilitar notificaciones push](/help/search-social-commerce/assets/notifications-push.png "Habilitar notificaciones push").

3. En el mensaje de confirmación, haga clic en **[!UICONTROL Enable]**.

4. Configure el explorador para que permita las notificaciones de [!UICONTROL Notification Center] a las `https://alert-center-ui-na.efrontier.com`.

   La configuración de notificaciones predeterminada varía según el explorador y es posible que a) se le presente automáticamente la opción para permitir notificaciones de [!UICONTROL Notification Center] o b) necesite administrar manualmente la configuración de notificaciones. Por ejemplo, en [!DNL Microsoft Edge], puede permitir notificaciones de [!UICONTROL Notification Center] desde la barra de herramientas del explorador. Consulte las instrucciones en la ayuda del explorador.

   ![Dónde administrar la configuración de notificaciones en Microsoft Edge](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Dónde administrar la configuración de notificaciones en Microsoft Edge")

5. En su [configuración de notificaciones](notification-edit.md), habilite [!UICONTROL Web] notificaciones para los tipos de alertas que desee insertar.

## Deshabilitar notificaciones push

Quitar notificaciones de `https://alert-center-ui-na.efrontier.com` dentro del administrador de notificaciones del explorador. Por ejemplo, en [!DNL Google Chrome], puede quitar o bloquear las notificaciones de sitios especificados en `chrome://settings/content/notifications`.

Consulte las instrucciones en la ayuda del explorador.

>[!MORELIKETHIS]
>
>* [Acerca de las notificaciones](/help/search-social-commerce/notifications/notification-about.md)
>* [Ver tus notificaciones](notification-view.md)
>* [Marcar una notificación como leída o no leída](notification-mark-read-unread.md)
>* [Eliminar una notificación](notification-delete.md)
>* [Editar la configuración de notificaciones](notification-edit.md)
>* [Instalar y desinstalar la aplicación web [!UICONTROL Notification Center]](notification-app-install-uninstall.md)
