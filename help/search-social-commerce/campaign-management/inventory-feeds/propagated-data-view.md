---
title: Ver datos generados a partir de fuentes
description: Obtenga información sobre cómo ver los datos generados a partir de las fuentes de datos de inventario.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Ver datos generados a partir de fuentes

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Cuando propaga datos de fuente sin publicarlos simultáneamente en la red de publicidad, puede obtener una vista previa de los datos de una de las siguientes maneras. Más adelante puede, opcionalmente [publicar datos](propagated-data-post.md) desde cualquier ubicación a las redes de publicidad relevantes.

* Si utilizó la opción para &quot;[!UICONTROL Propagate and Preview],&quot; y vea la hoja de edición masiva generada (denominada &quot;`<feed file name>_<template name>`&quot;) del [!UICONTROL Bulksheets] vista. No se incluyen datos en la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas. Esta opción le permite [validación de las páginas de aterrizaje](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) se asocia con los anuncios y las palabras clave antes de publicar los datos.

* Si utilizó la opción para &quot;[!UICONTROL Propagate only],&quot; y vea los datos generados dentro de una vista de jerarquía de campañas desde el [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas.

  Las vistas de jerarquía de campañas muestran solo los datos generados a partir del archivo de fuente, no los componentes de cuenta existentes. Una vez que los datos de un componente y todos sus subcomponentes se publican en la red de publicidad, ya no aparecen en la vista de jerarquía de campañas.

   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre a la [!UICONTROL Templates] pestaña.

   1. (Opcional) Para mostrar solo los componentes de campaña creados para una plantilla específica:

      1. Haga clic en el nombre de la plantilla.

      1. En el [!UICONTROL Accounts] en el panel de navegación izquierdo, expanda el nodo red de publicidad y el nodo cuenta de red de publicidad y, a continuación, active la casilla de verificación situada junto al nombre de la plantilla.

   1. Haga clic en **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, o **[!UICONTROL Ads]** , en función de los componentes que desee ver.

      >[!NOTE]
      >
      >* A menos que vea los datos de una plantilla específica, la variable [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] las pestañas enumeran todos los grupos de anuncios, palabras clave y anuncios creados a partir de todas las plantillas y archivos de fuentes. Grupos de productos utilizados para [!DNL Google Ads] los anuncios de compras aparecen en la [!UICONTROL Keywords] pestaña.
      >* Para ver solo los subcomponentes de una campaña específica, comience por ver la [!UICONTROL Campaigns] pestaña. Del mismo modo, para ver solo los subcomponentes de un grupo de publicidad específico, comience por ver el [!UICONTROL Ad Groups] pestaña.

   1. (Opcional) Para ver más información, siga uno de estos procedimientos:

      * Para ver la configuración de cualquier campaña, grupo de anuncios, palabra clave o anuncio, haga clic en [Icono de ver/editar configuración](/help/search-social-commerce/assets/settings.png "Icono de ver/editar configuración") junto al nombre.

      * Para ver los subcomponentes de una campaña o grupo de publicidad, haga lo siguiente:

         * Para enumerar todos los grupos de publicidad de una campaña, haga clic en el nombre de la campaña.

         * Para enumerar todas las palabras clave o destinos de producto de un grupo de anuncios, haga clic en el nombre del grupo de anuncios.

         * Para enumerar todos los anuncios de un grupo de anuncios, haga clic en el nombre del grupo de anuncios y, a continuación, haga clic en [!UICONTROL Ads] pestaña.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Editar datos generados a partir de fuentes](propagated-data-edit.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de publicidad](propagated-data-post.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de los datos generados a partir de las fuentes](propagated-data-status.md)
