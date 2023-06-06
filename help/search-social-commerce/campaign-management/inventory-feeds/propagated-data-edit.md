---
title: Editar datos generados a partir de fuentes
description: Obtenga información sobre cómo editar los datos generados a partir de las fuentes de datos de inventario.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Editar datos generados a partir de fuentes

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Cuando propaga datos de fuentes sin publicarlos simultáneamente en la red de publicidad, puede editar los datos de cualquiera de las siguientes maneras. Más adelante puede, opcionalmente [publicar datos](propagated-data-post.md) desde cualquier ubicación a las redes de publicidad relevantes:

* Si utilizó la opción para &quot;[!UICONTROL Propagate and Preview],&quot; podrá editar el archivo de hoja de edición masiva generado (denominado &quot;`<feed file name>_<template name>`&quot;) descargándolo desde el [!UICONTROL Bulksheets] vea, edite el archivo y vuelva a cargarlo. No se incluyen datos en la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas.

* Si utilizó la opción para &quot;[!UICONTROL Propagate only],&quot; podrá editar los datos generados para los componentes con [[!UICONTROL New] status](propagated-data-status.md) dentro de una vista de jerarquía de campañas desde el [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas.

   Las vistas de jerarquía de campañas muestran solo los datos generados a partir del archivo de fuente, no los componentes de cuenta existentes. Una vez que los datos de un componente y todos sus subcomponentes se publican en la red de publicidad, ya no aparecen en la jerarquía de campañas.

   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre a la [!UICONTROL Templates] pestaña.

   1. (Opcional) Para mostrar solo los componentes de campaña creados para una plantilla específica:

      1. Haga clic en el nombre de la plantilla.

      1. En el [!UICONTROL Accounts] en el panel de navegación izquierdo, expanda el nodo red de publicidad y el nodo cuenta de red de publicidad y, a continuación, active la casilla de verificación situada junto al nombre de la plantilla.
   1. Haga clic en **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, o **[!UICONTROL Ads]** , en función de los componentes que desee ver.

      >[!NOTE]
      >
      >* A menos que vea los datos de una plantilla específica, la variable [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] las pestañas enumeran todos los grupos de anuncios, palabras clave y anuncios creados a partir de todas las plantillas y archivos de fuentes. Grupos de productos utilizados para [!DNL Google Ads] los anuncios de compras aparecen en la [!UICONTROL Keywords] pestaña.
      >* Para ver solo los subcomponentes de una campaña específica, comience por ver la [!UICONTROL Campaigns] pestaña. Del mismo modo, para ver solo los subcomponentes de un grupo de publicidad específico, comience por ver el [!UICONTROL Ad Groups] pestaña.


   1. (Opcional; para editar grupos de anuncios, palabras clave o solo anuncios) Filtre la lista para incluir solo los subcomponentes de una campaña o grupo de anuncios específico:

      * Para enumerar todos los grupos de publicidad de una campaña, haga clic en el nombre de la campaña.

      * Para enumerar todas las palabras clave de un grupo de anuncios, haga clic en el nombre del grupo de anuncios.

      * Para enumerar todos los como en un grupo de anuncios, haga clic en el nombre del grupo de anuncios y, a continuación, haga clic en [!UICONTROL Ads] pestaña.
   1. Clic [Icono de ver/editar configuración](/help/search-social-commerce/assets/settings.png "Icono de ver/editar configuración") junto a la campaña, el grupo de anuncios, la palabra clave o el nombre del anuncio.

   1. Edite la configuración y haga clic en **[!UICONTROL Save]**.



>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Ver datos generados a partir de fuentes](propagated-data-view.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de publicidad](propagated-data-post.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de los datos generados a partir de las fuentes](propagated-data-status.md)

