---
title: Propagación de datos de fuentes de inventario mediante plantillas
description: Obtenga información acerca de la propagación de datos desde las fuentes de inventario a través de plantillas de publicidad para administrar la estructura de cuentas y enviar anuncios dinámicos.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Propagación de datos de fuentes de inventario mediante plantillas

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Después de crear una plantilla de fuente específica de la red de anuncios y asociarle un archivo de fuente o una cuenta de [!DNL Google] o [!DNL Microsoft] del centro de comerciantes, puede crear anuncios de forma dinámica propagando los datos de fuente a través de la plantilla según la [configuración de datos de fuente](feed-settings-manage.md). Durante la propagación, los nombres de columna de la plantilla se sustituyen por valores de datos en la fuente y las campañas generadas y sus componentes tienen la configuración predeterminada a menos que la plantilla especifique lo contrario. Según las opciones de plantilla, Buscar, Social y Commerce crean una nueva estructura de cuenta (campañas, grupos de anuncios y palabras clave) para los anuncios o asignan los anuncios a la estructura de cuenta existente.

Cuando los nuevos datos de fuente contienen nuevos valores de datos para un elemento o la plantilla ha cambiado, los anuncios existentes se eliminan y se crean nuevos. Si el único cambio es la designación de [!DNL Google Ads] Param 1 y Param 2, solo se actualizarán esos valores. Los anuncios duplicados (la misma copia de anuncio y la misma página de aterrizaje) nunca se crean.

Al propagar datos, puede obtener una vista previa de los datos generados en una vista de jerarquía de campañas, generar un archivo de hoja de edición masiva para revisarlos o generar un archivo de hoja de edición masiva para su publicación inmediata en la red de anuncios. Cuando se completa cada acción de propagación, se añade un resumen de propagación a la pestaña Propagations, indicando el número de cada tipo de entidad que se ha creado, pausado o eliminado en función de la propagación. Si no publica los datos inmediatamente, puede previsualizarlos y publicarlos más adelante.

## Propagar archivos de fuentes desde la ficha [!UICONTROL Templates]

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

1. Seleccione la casilla de verificación situada junto a las plantillas que desea propagar.

1. En la barra de herramientas, haga clic en **[!UICONTROL Propagate]** y, a continuación, seleccione una de las siguientes opciones:

   * **[!UICONTROL Propagate Only]:** Para mostrar los datos propagados en las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads]. Puede seguir publicando los datos de cualquier componente y sus subcomponentes más adelante desde la pestaña [!UICONTROL Templates].

   * **[!UICONTROL Propagate and Preview]:** Para crear un archivo de hoja de edición masiva (denominado &quot;`<feed file name>_<template name>`&quot;), que está disponible en la vista [!UICONTROL Bulksheets] para revisión (pero no en las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads]). Posteriormente, puede publicar el archivo de hoja de edición masiva desde la vista [!UICONTROL Bulksheets].

     Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP. No es necesario descomprimir el archivo para publicarlo.

   * **[!UICONTROL Propagate and Post to SE]:** Para crear un archivo de hoja de edición masiva (denominado &quot;`<feed file name>_<template name>`&quot;) que se ponga inmediatamente en cola para su publicación en la red publicitaria. El archivo de hoja de edición masiva está disponible en la vista [!UICONTROL Bulksheets], pero no está disponible en las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads].

     Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP.

   La &quot;Última prop. La columna Estado muestra el estado del trabajo para las plantillas aplicables.

   Cuando se completa cada acción de propagación, se agrega un resumen de propagación a la pestaña [!UICONTROL Propagations], que indica el número de cada tipo de entidad que se creó, pausó o eliminó en función de la propagación. La estimación no incluye los cambios realizados desde el editor de anuncios propio de la red de publicidad.

## Propagar archivos de fuentes de la lista [!UICONTROL Feeds]

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Feeds]**.

1. Seleccione la casilla de verificación situada junto al archivo de fuente.

1. Encima de la tabla de datos, haga clic en **[!UICONTROL Propagate/Post Feed Data]** y, a continuación, seleccione una de las siguientes opciones:

   * **[!UICONTROL Propagate Only]:** Para mostrar los datos propagados en las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads]. Puede seguir publicando los datos de cualquier componente y sus subcomponentes más adelante desde la pestaña [!UICONTROL Templates].

   * **[!UICONTROL Propagate and Preview]:** Para crear un archivo de hoja de edición masiva (denominado &quot;`<feed file name>_<template name>`&quot;), que está disponible en la vista [!UICONTROL Bulksheets] para revisión (pero no en las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads]). Posteriormente, puede publicar el archivo de hoja de edición masiva desde la vista [!UICONTROL Bulksheets].

     Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP. No es necesario descomprimir el archivo para publicarlo.

   * **[!UICONTROL Propagate and Post to SE]:** Para crear un archivo de hoja de edición masiva (denominado &quot;`<feed file name>_<template name>`&quot;) que se ponga inmediatamente en cola para su publicación en la red publicitaria. El archivo de hoja de edición masiva está disponible en la vista [!UICONTROL Bulksheets], pero no está disponible en las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads].

     Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP.

1. En la ventana emergente, active la casilla de verificación situada junto a cada plantilla a través de la cual desee propagar datos desde el archivo de fuente y, a continuación, haga clic en **[!UICONTROL Propagate Feed]**.

   Se muestran todas las plantillas asociadas con el archivo.

Se abre la pestaña [!UICONTROL Templates] y la columna &quot;[!UICONTROL Last Prop. Status]&quot; muestra el estado del trabajo para las plantillas aplicables.

Cuando se completa cada acción de propagación, se agrega un resumen de propagación a la pestaña [!UICONTROL Propagations], que indica el número de cada tipo de entidad que se creó, pausó o eliminó en función de la propagación. La estimación no incluye los cambios realizados desde el editor de anuncios propio de la red de publicidad.

## Ver un resumen de propagación

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Haga clic en la ficha **[!UICONTROL Propagations]**.

1. Junto al nombre de la plantilla, haga clic en ![icono Ver/editar configuración](/help/search-social-commerce/assets/settings.png "icono Ver/editar configuración") .

## Detener un trabajo de propagación

Puede detener un trabajo de propagación de datos de fuentes de inventario mientras el trabajo sigue en cola.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

1. En la columna &quot;[!UICONTROL Last Prop. Status]&quot; junto al nombre de la plantilla, haga clic en **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Administrar plantillas de anuncios para fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Ver datos generados a partir de fuentes](propagated-data-view.md)
>* [Editar datos generados a partir de fuentes](propagated-data-edit.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de anuncios](propagated-data-post.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de datos generados a partir de fuentes](propagated-data-status.md)
