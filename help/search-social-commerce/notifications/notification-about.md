---
title: Acerca de las notificaciones
description: Obtenga información acerca de las notificaciones, incluidos los distintos tipos y categorías.
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 49dc6a4a18966bbf68402d70aec9574ed11e1886
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Acerca de las notificaciones

*Función beta*

Puede configurar los ajustes de notificación para suscribirse o cancelar la suscripción a diferentes tipos de alertas. Puede ver las notificaciones de cualquiera de las siguientes maneras:

* Desde el [!UICONTROL Notifications] panel, que está disponible en el menú principal en ![Notificaciones](/help/search-social-commerce/assets/notifications-panel.png "Notificaciones").

* Desde [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* Desde una [!UICONTROL Notification Center] aplicación web, que se abre [!UICONTROL Notification Center] en una ventana independiente fuera de Buscar, Social y Comercio.

  La aplicación se carga más rápido que la versión normal del explorador y se actualiza automáticamente. Puede instalar la aplicación y administrarla mediante el administrador de aplicaciones del explorador.

* Desde notificaciones push al explorador.

  Cuando se habilitan las notificaciones push, aparecen según las convenciones de notificación del explorador.

Puede ver las notificaciones, marcarlas como leídas o no leídas y eliminarlas.

## Tipos de notificación

* **[!UICONTROL Notices]**: lanzamiento, tiempo de inactividad y otros avisos de administración de cambios.

* **[!UICONTROL Recommendations]**: Oportunidades identificadas para mejorar el rendimiento, implementar prácticas recomendadas, etc.

* **[!UICONTROL Warnings]**: Problemas que requieren atención, pero que no son críticos para la optimización o la administración.

* **[!UICONTROL Issues]**: Problemas críticos que requieren atención inmediata. Se incluyen notificaciones de error de autorización de cuenta.

## Categorías de notificación

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: Notificaciones que [operación de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) se ha completado o ha fallado.

   * **[!UICONTROL Manager Account Missing]**: Notificaciones de que Search, Social y Commerce no tienen las credenciales de un [cuenta de administrador de red de anuncios](/help/search-social-commerce/admin/manager-accounts.md), que son necesarios para la correcta configuración de las funciones esenciales.

   * **[!UICONTROL UI Actions]**: notificaciones de que los trabajos realizados en segundo plano se han completado o han dado error. Los tipos de trabajo incluyen [trabajos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), trabajos de edición masiva dentro de la tabla de datos o mediante la barra de herramientas, trabajos de asignación de entidades u otras acciones dentro de la interfaz de usuario (como sincronizar con redes de publicidad, pegar filas o cambiar el nombre de entidades). Las asignaciones de entidad incluyen la asignación o cancelación de asignación de una [valor de clasificación de etiquetas](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) a cualquier entidad, asignando una campaña a un portafolio y asignando o anulando la asignación de una restricción a un portafolio.<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: se utiliza para una versión beta cerrada

      * **[!UICONTROL File Upload to Cloud Storage]**: se utiliza para una versión beta cerrada

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: Notificaciones de que Search, Social y Commerce no han podido acceder a un [cuenta de red de publicidad](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) debido a credenciales no válidas o a un token de autorización no válido o caducado.

      * **[!UICONTROL Account Missing]**: Notificaciones de que Search, Social y Commerce no tienen las credenciales de un [cuenta de red de publicidad](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md).

      * **[!UICONTROL Manager Account Auth Error]**: Notificaciones que Search, Social y Commerce no han podido sincronizar con un [cuenta de administrador de red de anuncios](/help/search-social-commerce/admin/manager-accounts.md) debido a credenciales no válidas o a un token de autorización no válido o caducado.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: Notificaciones que [un [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) se ha completado o ha fallado.

   * **[!UICONTROL Custom Alerts]**: Notificaciones que [instancias de alerta](/help/search-social-commerce/alerts/alert-about.md) se activaron para una plantilla de alerta.

   * **[!UICONTROL Reports]**: Notificaciones que [informe personalizado o programado](/help/search-social-commerce/reports/report-about.md) se ha completado o ha fallado.

   * **[!UICONTROL Spreadsheet Feeds]**: Notificaciones que [fuente de hoja de cálculo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) se ha completado o ha fallado.

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: 

-->

<!--
* [!UICONTROL Portfolio Management]

  * **[!UICONTROL Simulation Report]**: 

-->

<!--
* [!UICONTROL System]

  * **[!UICONTROL Change Management]**: 

-->

>[!MORELIKETHIS]
>
>* [Ver las notificaciones](notification-view.md)
>* [Marcar una notificación como leída o no leída](notification-mark-read-unread.md)
>* [Eliminación de una notificación](notification-delete.md)
>* [Editar la configuración de notificaciones](notification-edit.md)
>* [Habilitar y deshabilitar notificaciones push desde [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Instale y desinstale el [!UICONTROL Notification Center] aplicación web](notification-app-install-uninstall.md)
