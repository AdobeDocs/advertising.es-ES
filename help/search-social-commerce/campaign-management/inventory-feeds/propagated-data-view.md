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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Cuando propaga datos de fuente sin publicarlos simultáneamente en la red de publicidad, puede obtener una vista previa de los datos de una de las siguientes maneras. Más adelante, opcionalmente, puede [publicar datos](propagated-data-post.md) desde cualquier ubicación en las redes de anuncios relevantes.

* Si utilizó la opción para &quot;[!UICONTROL Propagate and Preview]&quot;, vea la hoja de edición masiva generada (denominada &quot;`<feed file name>_<template name>`&quot;) desde la vista [!UICONTROL Bulksheets]. No se incluyen datos en las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads]. Esta opción le permite [validar las páginas de aterrizaje](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) asociadas con los anuncios y las palabras clave antes de publicar los datos.

* Si utilizó la opción para &quot;[!UICONTROL Propagate only]&quot;, vea los datos generados dentro de una vista de jerarquía de campañas desde las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads].

  Las vistas de jerarquía de campañas muestran solo los datos generados a partir del archivo de fuente, no los componentes de cuenta existentes. Una vez que los datos de un componente y todos sus subcomponentes se publican en la red de publicidad, ya no aparecen en la vista de jerarquía de campañas.

   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

   1. (Opcional) Para mostrar solo los componentes de campaña creados para una plantilla específica:

      1. Haga clic en el nombre de la plantilla.

      1. En el menú [!UICONTROL Accounts] del panel de navegación izquierdo, expanda el nodo de red de publicidad y el nodo de cuenta de red de publicidad y, a continuación, active la casilla de verificación situada junto al nombre de la plantilla.

   1. Haga clic en la ficha **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** o **[!UICONTROL Ads]**, según los componentes que desee ver.

      >[!NOTE]
      >
      >* A menos que vea los datos de una plantilla específica, las fichas [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads] muestran todos los grupos de anuncios, palabras clave y anuncios creados a partir de todas las plantillas y archivos de fuentes. Los grupos de productos usados para los anuncios de compras de [!DNL Google Ads] se muestran en la ficha [!UICONTROL Keywords].
      >* Para ver únicamente los subcomponentes de una campaña específica, comience por ver la ficha [!UICONTROL Campaigns]. Del mismo modo, para ver solo los subcomponentes de un grupo de anuncios específico, comience por ver la pestaña [!UICONTROL Ad Groups].

   1. (Opcional) Para ver más información, siga uno de estos procedimientos:

      * Para ver la configuración de cualquier campaña, grupo de anuncios, palabra clave o anuncio, haz clic en [icono Ver/editar configuración](/help/search-social-commerce/assets/settings.png "Icono de ver/editar configuración") junto al nombre.

      * Para ver los subcomponentes de una campaña o grupo de publicidad, haga lo siguiente:

         * Para enumerar todos los grupos de publicidad de una campaña, haga clic en el nombre de la campaña.

         * Para enumerar todas las palabras clave o destinos de producto de un grupo de anuncios, haga clic en el nombre del grupo de anuncios.

         * Para enumerar todos los anuncios de un grupo de anuncios, haga clic en el nombre del grupo de anuncios y, a continuación, haga clic en la ficha [!UICONTROL Ads].

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Editar datos generados a partir de fuentes](propagated-data-edit.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de anuncios](propagated-data-post.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de datos generados a partir de fuentes](propagated-data-status.md)
