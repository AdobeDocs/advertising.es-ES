---
title: (Nueva IU) Sincronizar manualmente los datos de red de anuncios
description: Aprenda a almacenar en déclencheur manualmente la sincronización de la estructura de la campaña y las entidades de campaña para las redes de publicidad admitidas desde la nueva interfaz de usuario.
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# (Nueva IU) Sincronizar manualmente los datos de red de publicidad a través de la conexión API

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anteriormente [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] y solo [!DNL Baidu] cuentas existentes*

La sincronización es el proceso mediante el cual Search, Social y Commerce recopilan información actualizada de las cuentas de red de anuncios conectadas de cada anunciante en [redes de anuncios admitidas](/help/search-social-commerce/introduction/supported-inventory.md). Estos datos incluyen la estructura de campañas y las entidades de campaña del anunciante, incluidos la mayoría de sus atributos que se administran o registran en Buscar, Social y Commerce. No incluye datos de clics, ni ofertas y modificadores de oferta introducidos fuera de Search, Social y Commerce, que se recopilan por separado.

Search, Social y Commerce se sincronizan (sincronizan) automáticamente con sus cuentas de red de publicidad una vez al día, y también siempre que detecta una nueva campaña en una de las redes de publicidad. Además, envía inmediatamente a la red de anuncios todos los cambios realizados en los datos de campaña desde Search, Social y Commerce.

Puede solicitar manualmente la sincronización de todas las campañas activas y pausadas en las cuentas especificadas<!--Not available as of 2/23:  or in specific active and paused campaigns -->. Esta tarea recopila entidades nuevas o modificadas en la red publicitaria.

Para las campañas con la opción &quot;[!UICONTROL Auto Update]&quot;, la operación de sincronización también genera y publica los códigos de seguimiento que faltan o que deben cambiarse en las plantillas de seguimiento o en las direcciones URL de destino. Las direcciones URL se generan según los parámetros de la configuración de seguimiento de la configuración de la cuenta o la campaña. Si existen direcciones URL de seguimiento para los elementos relevantes, no se regeneran a menos que se necesiten nuevas (como si el tipo de coincidencia de palabra clave, el texto creativo o los parámetros de seguimiento de la cuenta han cambiado).

>[!NOTE]
>
>Cada vez que [cree una hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), opcionalmente puede sincronizar con la red de anuncios antes de crear la hoja de edición masiva.

## Sincronizar campañas en una cuenta de red de publicidad

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Seleccione la casilla de verificación situada junto al nombre de la cuenta.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**.

   * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

Puede seguir el estado del trabajo de sincronización en la vista [!UICONTROL Workspace]. El trabajo puede tardar
una hora o más para que aparezca.

>[!MORELIKETHIS]
>
>* [Descargar o crear un archivo de hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
