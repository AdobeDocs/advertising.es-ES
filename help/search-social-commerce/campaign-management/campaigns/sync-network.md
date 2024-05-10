---
title: Sincronizar manualmente datos de red de anuncios
description: Obtenga información sobre cómo almacenar en déclencheur manualmente la sincronización de la estructura de la campaña y las entidades de campaña para las redes de publicidad admitidas.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Sincronizar manualmente datos de red de anuncios

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anteriormente [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex], y existentes [!DNL Baidu] solo cuentas*

La sincronización es el proceso mediante el cual Search, Social y Commerce recopilan información actualizada de las cuentas de red de anuncios conectadas de cada anunciante en [redes de publicidad admitidas](/help/search-social-commerce/introduction/supported-inventory.md). Estos datos incluyen la estructura de campañas y las entidades de campaña del anunciante, incluidos la mayoría de sus atributos que se administran o registran en Buscar, Social y Commerce. No incluye datos de clics, ni ofertas y modificadores de oferta introducidos fuera de Search, Social y Commerce, que se recopilan por separado.

Search, Social y Commerce se sincronizan (sincronizan) automáticamente con sus cuentas de red de publicidad una vez al día, y también siempre que detecta una nueva campaña en una de las redes de publicidad. Además, envía inmediatamente a la red de anuncios todos los cambios realizados en los datos de campaña desde Search, Social y Commerce.

Puede solicitar manualmente la sincronización de todas las campañas activas y en pausa en cuentas especificadas o en campañas activas y en pausa específicas. Esta tarea recopila entidades nuevas o modificadas en la red publicitaria.

Para campañas con la etiqueta &quot;[!UICONTROL Auto Upload]&quot;, la operación de sincronización también genera y publica los códigos de seguimiento que faltan o que deben cambiarse en las plantillas de seguimiento o en las direcciones URL de destino. Las direcciones URL se generan según los parámetros de la configuración de seguimiento de la configuración de la cuenta o la campaña. Si existen direcciones URL de seguimiento para los elementos relevantes, no se regeneran a menos que se necesiten nuevas (como si el tipo de coincidencia de palabra clave, el texto creativo o los parámetros de seguimiento de la cuenta han cambiado).

>[!NOTE]
>
>En cualquier momento [creación de una hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), si lo desea, puede sincronizar con la red de anuncios antes de crear la hoja de edición por lotes.

1. En el menú principal, haga clic en **[!UICONTROL Search]>[!UICONTROL Campaigns]**. En el submenú, seleccione **[!UICONTROL Accounts]** para sincronizar todas las campañas en cuentas específicas o **[!UICONTROL Campaigns]** para sincronizar campañas específicas.

1. (Opcional) Filtre la lista para incluir cuentas o campañas específicas.

1. Seleccione la casilla de verificación situada junto a cada cuenta o campaña que desee sincronizar. Puede sincronizar hasta 50 campañas a la vez. Si sincroniza más de cinco cuentas a la vez, el trabajo se divide en lotes de hasta cinco cuentas cada uno.

1. Clic **![Más](/help/search-social-commerce/assets/more.png "Más")** en la barra de herramientas, y luego seleccione **[!UICONTROL Sync]**.

Puede seguir el estado del trabajo de sincronización en la [!UICONTROL Workspace] vista. El trabajo puede tardar una hora o más en aparecer.

>[!MORELIKETHIS]
>
>* [Descargar/crear un archivo de hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
