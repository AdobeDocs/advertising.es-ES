---
title: Propagación de datos de fuentes de inventario mediante plantillas
description: Obtenga información acerca de la propagación de datos desde las fuentes de inventario a través de plantillas de publicidad para administrar la estructura de cuentas y enviar anuncios dinámicos.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Propagación de datos de fuentes de inventario mediante plantillas

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Después de crear una plantilla de fuente específica de la red de anuncios y asociar un archivo de fuente o una [!DNL Google] o [!DNL Microsoft] cuenta del centro de comerciantes con él, puede crear anuncios de forma dinámica propagando los datos de fuente a través de la plantilla según el [configuración de datos de fuente](feed-settings-manage.md). Durante la propagación, los nombres de columna de la plantilla se sustituyen por valores de datos en la fuente y las campañas generadas y sus componentes tienen la configuración predeterminada a menos que la plantilla especifique lo contrario. Según las opciones de plantilla, Buscar, Social y Commerce crean una nueva estructura de cuenta (campañas, grupos de anuncios y palabras clave) para los anuncios o asignan los anuncios a la estructura de cuenta existente.

Cuando los nuevos datos de fuente contienen nuevos valores de datos para un elemento o la plantilla ha cambiado, los anuncios existentes se eliminan y se crean nuevos. Si el único cambio es la designación de [!DNL Google Ads] Param 1 y Param 2, entonces solo se actualizan esos valores. Los anuncios duplicados (la misma copia de anuncio y la misma página de aterrizaje) nunca se crean.

Al propagar datos, puede obtener una vista previa de los datos generados en una vista de jerarquía de campañas, generar un archivo de hoja de edición masiva para revisarlos o generar un archivo de hoja de edición masiva para su publicación inmediata en la red de anuncios. Cuando se completa cada acción de propagación, se añade un resumen de propagación a la pestaña Propagations, indicando el número de cada tipo de entidad que se ha creado, pausado o eliminado en función de la propagación. Si no publica los datos inmediatamente, puede previsualizarlos y publicarlos más adelante.

## Propagación de archivos de fuente desde [!UICONTROL Templates] pestaña

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre a la [!UICONTROL Templates] pestaña.

1. Seleccione la casilla de verificación situada junto a las plantillas que desea propagar.

1. En la barra de herramientas, haga clic en **[!UICONTROL Propagate]** y, a continuación, seleccione una de las siguientes opciones:

   * **[!UICONTROL Propagate Only]:** Para mostrar los datos propagados en [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas. Puede seguir publicando los datos de cualquier componente y sus subcomponentes más adelante desde el [!UICONTROL Templates] pestaña.

   * **[!UICONTROL Propagate and Preview]:** Para crear un archivo de hoja de edición masiva (denominado &quot;`<feed file name>_<template name>`&quot;), que está disponible en el [!UICONTROL Bulksheets] ver para revisión (pero no en el [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas). Posteriormente, puede publicar el archivo de hoja de edición masiva desde el [!UICONTROL Bulksheets] vista.

     Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP. No es necesario descomprimir el archivo para publicarlo.

   * **[!UICONTROL Propagate and Post to SE]:** Para crear un archivo de hoja de edición masiva (denominado &quot;`<feed file name>_<template name>`&quot;) que se pone inmediatamente en cola para su publicación en la red publicitaria. El archivo de hoja de edición masiva está disponible en la [!UICONTROL Bulksheets] vista, pero no está disponible en la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas.

     Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP.

   La &quot;Última prop. La columna Estado muestra el estado del trabajo para las plantillas aplicables.

   Cuando se completa cada acción de propagación, se añade un resumen de propagación a [!UICONTROL Propagations] , que indica el número de cada tipo de entidad que se creó, pausó o eliminó en función de la propagación. La estimación no incluye los cambios realizados desde el editor de anuncios propio de la red de publicidad.

## Propagación de archivos de fuente desde [!UICONTROL Feeds] lista

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Feeds]**.

1. Seleccione la casilla de verificación situada junto al archivo de fuente.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Propagate/Post Feed Data]** y, a continuación, seleccione una de las siguientes opciones:

   * **[!UICONTROL Propagate Only]:** Para mostrar los datos propagados en [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas. Puede seguir publicando los datos de cualquier componente y sus subcomponentes más adelante desde el [!UICONTROL Templates] pestaña.

   * **[!UICONTROL Propagate and Preview]:** Para crear un archivo de hoja de edición masiva (denominado &quot;`<feed file name>_<template name>`&quot;), que está disponible en el [!UICONTROL Bulksheets] ver para revisión (pero no en el [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas). Posteriormente, puede publicar el archivo de hoja de edición masiva desde el [!UICONTROL Bulksheets] vista.

     Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP. No es necesario descomprimir el archivo para publicarlo.

   * **[!UICONTROL Propagate and Post to SE]:** Para crear un archivo de hoja de edición masiva (denominado &quot;`<feed file name>_<template name>`&quot;) que se pone inmediatamente en cola para su publicación en la red publicitaria. El archivo de hoja de edición masiva está disponible en la [!UICONTROL Bulksheets] vista, pero no está disponible en la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas.

     Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP.

1. En la ventana emergente, active la casilla de verificación situada junto a cada plantilla a través de la cual desee propagar datos desde el archivo de fuente y, a continuación, haga clic en **[!UICONTROL Propagate Feed]**.

   Se muestran todas las plantillas asociadas con el archivo.

El [!UICONTROL Templates] se abre la pestaña y aparece el mensaje &quot;[!UICONTROL Last Prop. Status]La columna &quot; muestra el estado del trabajo para las plantillas aplicables.

Cuando se completa cada acción de propagación, se añade un resumen de propagación a [!UICONTROL Propagations] , que indica el número de cada tipo de entidad que se creó, pausó o eliminó en función de la propagación. La estimación no incluye los cambios realizados desde el editor de anuncios propio de la red de publicidad.

## Ver un resumen de propagación

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Haga clic en **[!UICONTROL Propagations]** pestaña.

1. Junto al nombre de la plantilla, haga clic en ![Icono de ver/editar configuración](/help/search-social-commerce/assets/settings.png "Icono de ver/editar configuración") .

## Detener un trabajo de propagación

Puede detener un trabajo de propagación de datos de fuentes de inventario mientras el trabajo sigue en cola.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre a la [!UICONTROL Templates] pestaña.

1. En el campo &quot;[!UICONTROL Last Prop. Status]&quot; junto al nombre de la plantilla, haga clic en **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Administrar plantillas de publicidad para fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Ver datos generados a partir de fuentes](propagated-data-view.md)
>* [Editar datos generados a partir de fuentes](propagated-data-edit.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de publicidad](propagated-data-post.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de los datos generados a partir de las fuentes](propagated-data-status.md)
