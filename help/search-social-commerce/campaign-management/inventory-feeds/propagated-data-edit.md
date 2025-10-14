---
title: Editar datos generados a partir de fuentes
description: Obtenga información sobre cómo editar los datos generados a partir de las fuentes de datos de inventario.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Editar datos generados a partir de fuentes

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Cuando propaga datos de fuentes sin publicarlos simultáneamente en la red de publicidad, puede editar los datos de cualquiera de las siguientes maneras. Más tarde, opcionalmente, puede [publicar datos](propagated-data-post.md) desde cualquier ubicación en las redes de anuncios relevantes:

* Si utilizó la opción para &quot;[!UICONTROL Propagate and Preview]&quot;, podrá editar el archivo de hoja de edición masiva generado (denominado &quot;`<feed file name>_<template name>`&quot;) descargándolo de la vista [!UICONTROL Bulksheets], editando el archivo y cargándolo de nuevo. No se incluyen datos en las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads].

* Si utilizó la opción para &quot;[!UICONTROL Propagate only]&quot;, puede editar los datos generados para los componentes con el estado [[!UICONTROL New] &#x200B;](propagated-data-status.md) dentro de una vista de jerarquía de campaña desde las pestañas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads].

  Las vistas de jerarquía de campañas muestran solo los datos generados a partir del archivo de fuente, no los componentes de cuenta existentes. Una vez que los datos de un componente y todos sus subcomponentes se publican en la red de publicidad, ya no aparecen en la jerarquía de campañas.

   1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

   1. (Opcional) Para mostrar solo los componentes de campaña creados para una plantilla específica:

      1. Haga clic en el nombre de la plantilla.

      1. En el menú [!UICONTROL Accounts] del panel de navegación izquierdo, expanda el nodo de red de publicidad y el nodo de cuenta de red de publicidad y, a continuación, active la casilla de verificación situada junto al nombre de la plantilla.

   1. Haga clic en la ficha **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** o **[!UICONTROL Ads]**, según los componentes que desee ver.

      >[!NOTE]
      >
      >* A menos que vea los datos de una plantilla específica, las fichas [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads] muestran todos los grupos de anuncios, palabras clave y anuncios creados a partir de todas las plantillas y archivos de fuentes. Los grupos de productos usados para los anuncios de compras de [!DNL Google Ads] se muestran en la ficha [!UICONTROL Keywords].
      >* Para ver únicamente los subcomponentes de una campaña específica, comience por ver la ficha [!UICONTROL Campaigns]. Del mismo modo, para ver solo los subcomponentes de un grupo de anuncios específico, comience por ver la pestaña [!UICONTROL Ad Groups].

   1. (Opcional; para editar grupos de anuncios, palabras clave o solo anuncios) Filtre la lista para incluir solo los subcomponentes de una campaña o grupo de anuncios específico:

      * Para enumerar todos los grupos de publicidad de una campaña, haga clic en el nombre de la campaña.

      * Para enumerar todas las palabras clave de un grupo de anuncios, haga clic en el nombre del grupo de anuncios.

      * Para enumerar todos los elementos como en un grupo de anuncios, haga clic en el nombre del grupo de anuncios y, a continuación, haga clic en la ficha [!UICONTROL Ads].

   1. Haga clic en el [icono Ver/editar configuración](/help/search-social-commerce/assets/settings.png "Icono de ver/editar configuración") junto a la campaña, el grupo de anuncios, la palabra clave o el nombre del anuncio.

   1. Edite la configuración y haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Ver datos generados a partir de fuentes](propagated-data-view.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de anuncios](propagated-data-post.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de datos generados a partir de fuentes](propagated-data-status.md)
