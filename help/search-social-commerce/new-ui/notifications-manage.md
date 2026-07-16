---
title: (Nueva IU) Administrar notificaciones
description: Obtenga información sobre cómo ver, configurar y administrar las notificaciones de Search, Social y Commerce, incluidas las notificaciones push y la aplicación web del Centro de notificaciones.
feature: Search Notifications
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# (Nueva IU) Administrar notificaciones

*característica de Beta*

Puede configurar los ajustes de notificación para suscribirse o cancelar la suscripción a diferentes tipos de alertas. Puede ver las notificaciones de cualquiera de las siguientes maneras:

* En el panel [!UICONTROL Notifications], que está disponible en la esquina superior derecha en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones"). Desde el panel, puede filtrar la lista, editar la configuración de las notificaciones o abrir [!UICONTROL Notification Center].

* De [!UICONTROL Notification Center], que se abre en una ventana independiente fuera de Buscar, Social y Commerce. Para abrir [!UICONTROL Notification Center] desde el panel [!UICONTROL Notifications], haga clic en **[!UICONTROL View All]**.

* Desde una aplicación web [!UICONTROL Notification Center], que abre [!UICONTROL Notification Center] en una ventana independiente fuera de Search, Social y Commerce.

  La aplicación se carga más rápido que la versión normal del explorador y se actualiza automáticamente. Puede instalar la aplicación y administrarla mediante el administrador de aplicaciones del explorador.

* Desde notificaciones push al explorador.

  Cuando se habilitan las notificaciones push, aparecen según las convenciones de notificación del explorador.

Puede ver las notificaciones, marcarlas como leídas o no leídas y eliminarlas.

## Tipos de notificación

* **[!UICONTROL Notices]**: lanzamiento, tiempo de inactividad y otros avisos de administración de cambios.

* **[!UICONTROL Recommendations]**: oportunidades identificadas para mejorar el rendimiento, implementar prácticas recomendadas, etc.

* **[!UICONTROL Warnings]**: problemas que requieren atención pero que no son críticos para la optimización o administración.

* **[!UICONTROL Issues]**: problemas críticos que requieren atención inmediata. Se incluyen notificaciones de error de autorización de cuenta.

## Categorías de notificación

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: notificaciones que indican que una [operación de hoja de edición por lotes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) se completó o produjo un error.<!-- Update link once file for new UI available-->

   * **[!UICONTROL Manager Account Missing]**: notificaciones de que Search, Social y Commerce no tienen las credenciales de una [cuenta de administrador de red de anuncios](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md), necesarias para la correcta configuración de funciones críticas.<!-- Moving to Campaign Management > Setup Errors at some point -->

   * **[!UICONTROL UI Actions]**: notificaciones de que los trabajos realizados en segundo plano se completaron o dieron error. Los tipos de trabajo incluyen [trabajos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available-->, trabajos de edición masiva dentro de la tabla de datos o mediante la barra de herramientas, trabajos de asignación de entidades u otras acciones dentro de la interfaz de usuario (como sincronizar con redes de anuncios, pegar filas o cambiar el nombre de entidades). Las asignaciones de entidad incluyen la asignación o anulación de la asignación de un [valor de clasificación de etiquetas](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md) a cualquier entidad, la asignación de una campaña a un portafolio y la [asignación o anulación de la asignación de una restricción de oferta a una entidad](/help/search-social-commerce/new-ui/goals/constraints-manage.md).

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: notificaciones que indican que se ha cargado un archivo de datos de cuenta o que se ha producido un error en la carga de datos de cuenta mediante [carga manual de datos de cuenta](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

      * **[!UICONTROL File Upload to Cloud Storage]**: notificaciones que indican que se ha cargado un archivo de datos de cuenta o que se ha producido un error al cargar los datos de cuenta a través de [carga de datos de cuenta en un bloque [!DNL Amazon] [!DNL S3]](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: notificaciones en las que Search, Social y Commerce no pudieron obtener acceso a una [cuenta de red de publicidad](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) debido a credenciales no válidas o a un token de autorización caducado o no válido.

      * **[!UICONTROL Account Missing]**: notificaciones de que Search, Social y Commerce no tienen las credenciales para una [cuenta de red de publicidad](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md).

      * **[!UICONTROL Manager Account Auth Error]**: notificaciones que Search, Social y Commerce no pudieron sincronizar con una [cuenta de administrador de red de anuncios](/help/search-social-commerce/admin/manager-accounts.md) debido a credenciales no válidas o a un token de autorización caducado o no válido.<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: Notificaciones de que [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) se completó o produjo un error.

   * **[!UICONTROL Custom Alerts]**: notificaciones de que se activaron [instancias de alerta](/help/search-social-commerce/new-ui/alerts-manage.md) para una plantilla de alerta.

   * **[!UICONTROL Spreadsheet Feeds]**: notificaciones de que una [fuente de hoja de cálculo](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md) se completó o produjo un error.

   * [!UICONTROL Reports]

      * **[!UICONTROL Grid Reports]**: notificaciones de que un informe de vista de datos de una vista específica (como el contenido de la tabla de datos de la vista [!UICONTROL Camapigns]) se completó o produjo un error.

      * **[!UICONTROL Reports]**: notificaciones de que un [informe personalizado o programado](/help/search-social-commerce/new-ui/reports/management/report-manage.md) se completó o produjo un error.

   * [!UICONTROL Portfolio Management]

      * **[!UICONTROL Intraday Optimization]**: notificaciones cuando la optimización intradía está deshabilitada.

      * **[!UICONTROL Simulation Report]**: notificaciones sobre [trabajos de simulación](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md).

      * [!UICONTROL Objective & Conversion Configuration]

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]**: notificaciones a nivel de anunciante sobre la asignación automática correcta y fallida de los objetivos de conversión de la campaña.

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]**: notificaciones a nivel de portafolio sobre la asignación automática exitosa y fallida de los objetivos de conversión de la campaña.

      * [!UICONTROL Portfolios]

         * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]**: notificaciones sobre [trabajos de edición masiva de portafolios a través de hojas de edición masiva](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md).

         * **[!UICONTROL Portfolio Settings]**: notificaciones sobre [cambios en la configuración del portafolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md).

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## Acciones disponibles

* [Ver las notificaciones](#notification-view)

* [Editar la configuración de notificaciones](#notification-edit)

* [Marcar una notificación como leída o no leída](#notification-mark-read-unread)

* [Eliminación de una notificación](#notification-delete)

* [Habilitar y deshabilitar notificaciones push](#notification-push-enable-disable)

* [Instalar y desinstalar la aplicación web [!UICONTROL Notification Center]](#notification-app-install-uninstall)

## Ver las notificaciones {#notification-view}

Una vez que se haya suscrito a [notificaciones](#notification-edit) acerca de errores de autenticación de cuenta, alertas personalizadas activadas y [!UICONTROL Advertising Insights] generadas, podrá ver las notificaciones en el panel [!UICONTROL Notifications] o en [!UICONTROL Notification Center].

### Ver notificaciones en el panel [!UICONTROL Notifications]

1. En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones").

1. (Opcional) Realice una de las siguientes acciones:

   * Para ver los detalles de cualquier notificación, haga clic en el nombre de la notificación.

     En algunas notificaciones, la sección [!UICONTROL Action Recommended] puede incluir un vínculo que abre una vista filtrada de las entidades afectadas o responsables.

   * Para marcar una notificación como *leída* o *no leída*, mantenga el cursor sobre el nombre de la alerta y haga clic en ![Marcar como leída o no leída](/help/search-social-commerce/assets/notifications-read-unread.png "Marcar como leída o no leída").

     Las notificaciones marcadas como *leer* aparecen en un texto de color más claro, pero permanecerán disponibles hasta que las elimine.

     ![Notificaciones leídas y no leídas](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Notificaciones leídas y no leídas")

   * Para cambiar las preferencias de suscripción para el tipo de notificación, haz clic en ![Configuración](/help/search-social-commerce/assets/settings-nc.png "Configuración") junto a la notificación, cambia la configuración y, a continuación, haz clic en **[!UICONTROL Save]**.

   * Para eliminar una notificación, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto a la notificación.

   * Para abrir [!UICONTROL Notification Center], haga clic en **[!UICONTROL View All]**.

### Ver notificaciones en [!UICONTROL Notification Center]

1. En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones").

1. Haga clic en **[!UICONTROL View All]**.

1. (Opcional) Para filtrar las notificaciones por tipo, haga clic en *[!UICONTROL Notices], [!UICONTROL Recommendations], [!UICONTROL Warnings] o[!UICONTROL Issues]*.

1. (Opcional) Realice una de las siguientes acciones:

   * Para ver los detalles de cualquier notificación, haga clic en el nombre de la notificación.

     En algunas notificaciones, la sección [!UICONTROL Action Recommended] puede incluir un vínculo que abre una vista filtrada de las entidades afectadas o responsables.

   * Para marcar una notificación como *leída* o *no leída*, mantenga el cursor sobre el nombre de la alerta y haga clic en ![Marcar como leída o no leída](/help/search-social-commerce/assets/notifications-read-unread.png "Marcar como leída o no leída").

     Las notificaciones marcadas como *leer* aparecen en un texto de color más claro, pero permanecerán disponibles hasta que las elimine.

   * Para cambiar las preferencias de suscripción para el tipo de notificación, haz clic en ![Configuración](/help/search-social-commerce/assets/settings-nc.png "Configuración") junto a la notificación, cambia la configuración y, a continuación, haz clic en **[!UICONTROL Save]**.

   * Para eliminar una notificación, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto a la notificación.

## Editar la configuración de notificaciones {#notification-edit}

Si lo desea, puede suscribirse a las notificaciones por correo electrónico y web sobre errores de autenticación de cuenta, todas las alertas personalizadas activadas y la finalización de [!UICONTROL Advertising Insights] que genere, o cancelar dicha suscripción.

1. Abra la configuración de notificaciones de cualquiera de las siguientes maneras:

   * En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones") para abrir el panel [!UICONTROL Notifications]. En la esquina superior derecha, haga clic en ![Configuración](/help/search-social-commerce/assets/settings-nc.png "Configuración").

   * En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones"), haga clic en **[!UICONTROL View All]** para abrir [!UICONTROL Notification Center] y, a continuación, en el menú de la izquierda, haga clic en ![Configuración](/help/search-social-commerce/assets/settings-nc.png "Configuración").

1. Cambie la configuración de cualquier categoría de notificación enumerada anteriormente:

   * Para suscribirse o cancelar la suscripción a las notificaciones, mueva el control deslizante de la columna [!UICONTROL Subscribe]:

      * Para cancelar la suscripción a todos los tipos de notificación, mueva el control deslizante a la izquierda (desactivado).

      * Para suscribirse a uno o más tipos de notificación, mueva el control deslizante a la derecha (habilitado).

   * (Cuando [!UICONTROL Subscribe] esté habilitado) Para suscribirse a las notificaciones por correo electrónico, active la casilla de verificación de la columna **[!UICONTROL Email]**.

   * (Cuando [!UICONTROL Subscribe] esté deshabilitado) Para suscribirse a las notificaciones web en Search, Social y Commerce y a las notificaciones push si están habilitadas para el explorador, active la casilla de verificación en la columna **[!UICONTROL Web]**.

     Las notificaciones web solo se entregan cuando [habilita las notificaciones push](#notification-push-enable-disable) en el explorador.

1. Haga clic en **[!UICONTROL Save]**.

## Marcar una notificación como leída o no leída {#notification-mark-read-unread}

Al marcar una notificación como *leída* o *no leída*, se cambia el número de notificaciones no leídas que se indican en el vínculo [!UICONTROL Notifications] en la parte superior de cada página (como el icono ![Notificaciones con el contador de notificaciones no leídas](/help/search-social-commerce/assets/notifications-unread.png "Icono de notificaciones con el contador de notificaciones no leídas")).

Las notificaciones marcadas como *leer* aparecen en un texto de color más claro, pero permanecerán disponibles hasta que las elimine.

![Notificaciones leídas y no leídas](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Notificaciones leídas y no leídas")

1. [Abra el panel Notificaciones o el Centro de notificaciones](#notification-view).

1. Mantenga el cursor sobre el nombre de la alerta y haga clic en ![Marcar como leído o no leído](/help/search-social-commerce/assets/notifications-read-unread.png "Marcar como leído o no leído").

## Eliminación de una notificación {#notification-delete}

### Eliminar una notificación dentro del panel [!UICONTROL Notifications]

1. En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones").

1. Haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto a la notificación.

### Eliminar una notificación dentro de [!UICONTROL Notification Center]

1. En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones").

1. Haga clic en **[!UICONTROL View All]**.

1. (Opcional) Para filtrar las notificaciones por tipo, haga clic en *[!UICONTROL Notices]*, *[!UICONTROL Recommendations]*, *[!UICONTROL Warnings]* o *[!UICONTROL Issues]*.

1. Haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto a la notificación.

## Habilitar y deshabilitar notificaciones push {#notification-push-enable-disable}

Puede activar las notificaciones en Buscar, Social y Commerce, donde aparecerán según las convenciones de notificación del explorador. En dispositivos que usan [!DNL Microsoft Windows], las notificaciones se muestran en la parte inferior derecha de la pantalla (bandeja del sistema). En [!DNL Apple Mac] dispositivos, las notificaciones se muestran en el menú derecho.

Las notificaciones push están disponibles en los siguientes exploradores:

* [!DNL Google Chrome] 40 y superior

* [!DNL Microsoft Edge] 17 y posterior

* [!DNL Mozilla Firefox] 44 y superior

Puede desactivar las notificaciones push según el procedimiento estándar del explorador.

### Habilitar notificaciones push

1. En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones").

1. Haga clic en **[!UICONTROL View All]**.

1. En la parte inferior derecha, haga clic en ![Habilitar notificaciones push](/help/search-social-commerce/assets/notifications-push.png "Habilitar notificaciones push").

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Enable]**.

1. Configure el explorador para que permita las notificaciones de [!UICONTROL Notification Center] a las `https://alert-center-ui-na.efrontier.com`.

   La configuración de notificaciones predeterminada varía según el explorador y es posible que a) se le presente automáticamente la opción para permitir notificaciones de [!UICONTROL Notification Center] o b) necesite administrar manualmente la configuración de notificaciones. Por ejemplo, en [!DNL Microsoft Edge], puede permitir notificaciones de [!UICONTROL Notification Center] desde la barra de herramientas del explorador. Consulte las instrucciones en la ayuda del explorador.

   ![Dónde administrar la configuración de notificaciones en Microsoft Edge](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Dónde administrar la configuración de notificaciones en Microsoft Edge")

1. En su [configuración de notificaciones](#notification-edit), habilite [!UICONTROL Web] notificaciones para los tipos de alertas que desee insertar.

### Deshabilitar notificaciones push

Quitar notificaciones de `https://alert-center-ui-na.efrontier.com` dentro del administrador de notificaciones del explorador. Por ejemplo, en [!DNL Google Chrome], puede quitar o bloquear las notificaciones de sitios especificados en `chrome://settings/content/notifications`.

Consulte las instrucciones en la ayuda del explorador.

## Instalar y desinstalar la aplicación web [!UICONTROL Notification Center] {#notification-app-install-uninstall}

Puede recibir y administrar notificaciones fuera del explorador instalando una aplicación web [!UICONTROL Notification Center]. La aplicación tiene el mismo aspecto y la misma funcionalidad que [!UICONTROL Notification Center] en Search, Social y Commerce. La aplicación está disponible para [!DNL Google Chrome] 40 y versiones posteriores o para [!DNL Microsoft Edge] 17 y versiones posteriores.

Una vez instalada la aplicación [!UICONTROL Notification Center], se habilita automáticamente en el administrador de aplicaciones del explorador y se carga como una ventana independiente cuyo diseño se organiza dinámicamente en función del tamaño de la ventana. Puede abrir y cerrar la aplicación desde el administrador de aplicaciones del explorador o anclarla a la barra de tareas o el muelle del sistema operativo. La aplicación se actualiza automáticamente.

![icono del Centro de notificaciones en la barra de tareas de Microsoft Windows](/help/search-social-commerce/assets/windows-taskbar.png "icono del Centro de notificaciones en la barra de tareas de Microsoft Windows")

Puede deshabilitar o desinstalar la aplicación desde el administrador de aplicaciones del explorador. Para obtener información adicional sobre la administración de aplicaciones web, consulte la ayuda del explorador.

### Instalar la aplicación web [!UICONTROL Notification Center] para [!DNL Google Chrome]

1. En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones").

1. Haga clic en **[!UICONTROL View All]**.

1. En la parte inferior derecha, haga clic en ![Instalar aplicación web del Centro de notificaciones](/help/search-social-commerce/assets/notifications-install-app.png "Instalar aplicación web del Centro de notificaciones").

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Add]**.

1. ¿En la aplicación de instalación? mensaje, haga clic en **[!UICONTROL Install]**.

### Instalar la aplicación web [!UICONTROL Notification Center] para [!DNL Microsoft Edge]

* Desde Buscar, Social y Commerce:

   1. En la parte superior derecha de cualquier página, haga clic en ![Notificaciones](/help/search-social-commerce/assets/notifications.png "Notificaciones").

   1. Haga clic en **[!UICONTROL View All]**.

   1. En la parte inferior derecha, haga clic en ![Instalar aplicación web del Centro de notificaciones](/help/search-social-commerce/assets/notifications-install-app.png "Instalar aplicación web del Centro de notificaciones").

   1. En el mensaje de confirmación, haga clic en **[!UICONTROL Add]**.

   1. En el mensaje de la aplicación [!UICONTROL Install Notification Center], haga clic en **[!UICONTROL Install]**.

* Desde el menú principal [!DNL Edge]:

   1. En la barra de herramientas del explorador, haga clic en **...** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**.

   1. En el mensaje de la aplicación [!UICONTROL Install Notification Center], haga clic en **[!UICONTROL Install]**.

### Desinstalar la aplicación web [!UICONTROL Notification Center] para [!DNL Google Chrome]

* En [!DNL Chrome], vaya a `chrome://apps`, haga clic con el botón secundario en **[!UICONTROL notification-center]** y luego haga clic en **[!UICONTROL Remove from Chrome]**.

### Desinstalar la aplicación web [!UICONTROL Notification Center] para [!DNL Microsoft Edge]

1. En la barra de herramientas del explorador [!DNL Edge], haga clic en **...** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**. Alternativamente, vaya a `edge://apps`.

1. Haga clic con el botón derecho en **[!UICONTROL Notification Center]** y seleccione **[!UICONTROL Uninstall]**.
