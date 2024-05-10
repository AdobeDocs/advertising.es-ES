---
title: Estados de los datos generados a partir de las fuentes
description: Obtenga información sobre los estados de los datos generados a partir de las fuentes de datos de inventario.
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Estados de los datos generados a partir de las fuentes

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Cada componente puede tener uno de los siguientes estados:

* *[!UICONTROL New]:* El componente no existe en la red de publicidad y no se publicó en la red de publicidad. Puede editar su configuración si es necesario haciendo clic en el nombre del componente. Cuando esté listo para publicar los datos, haga clic en **[!UICONTROL Post to SE]** y especifique los datos que desea enviar.

* *[!UICONTROL Posted]:* (Solo campañas y grupos de anuncios) La campaña o el grupo de anuncios se publicó parcialmente en la red de anuncios, pero algunos componentes no se publicaron debido a errores. El estado de validación de cada palabra clave y anuncio muestra qué información debe corregirse. Si es necesario, puede editar la configuración del componente haciendo clic en su nombre.

* *[!UICONTROL Active]:* El componente ya está activo en la red de publicidad y no puede editar su configuración aquí. Los componentes activos pueden incluir subcomponentes que [!UICONTROL New], que se puede publicar si los datos son válidos.

* *[!UICONTROL Paused]:* El componente ya está en pausa en la red de anuncios y no puede editar su configuración aquí. Los componentes en pausa pueden incluir subcomponentes que están [!UICONTROL New], que se puede publicar si los datos son válidos.

* *[!UICONTROL Deleted]:* El componente ya se ha eliminado en la red de publicidad y no puede editar su configuración aquí. Los componentes eliminados pueden incluir subcomponentes que [!UICONTROL New], que se puede publicar si los datos son válidos.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Ver datos generados a partir de fuentes](propagated-data-view.md)
>* [Editar datos generados a partir de fuentes](propagated-data-edit.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de publicidad](propagated-data-post.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
