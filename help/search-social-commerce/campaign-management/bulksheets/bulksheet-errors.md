---
title: Errores de hoja de edición masiva
description: Razones potenciales de referencia para cada error de hoja de edición masiva.
exl-id: 0a259aca-2e9a-4e24-b4db-f8d0249d25d4
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 0%

---

# Errores de hoja de edición masiva

Search, Social y Commerce generan dos tipos de archivos de error durante las operaciones de hojas de edición por lotes:

* **Errores de SE:** Cuando se publica un archivo pero la red publicitaria no acepta todos los datos, aparece un archivo de error llamado `<uploaded file name>_se_errors.<extension used for the bulksheet>` se ha creado. Cuando se aceptan algunas filas, pero no todas, el archivo de error muestra las filas que no se publicaron y una explicación de cada error para que pueda corregirlo. Los errores se incluyen en la sección &quot;[!UICONTROL SE Error Message]&quot; columna.

>[!NOTE]
>
>Si publica alguna [!DNL Google Ads] anuncios que violan las políticas publicitarias de la red de anuncios, pero que pueden ser elegibles para exenciones, entonces esos anuncios se vuelven a publicar automáticamente con solicitudes de exención. Si la solicitud de exención falla, la información sobre la infracción se incluye en el archivo de error.

* **Errores de EF:** Cuando la operación de hoja de edición masiva no puede cargar o procesar un archivo o filas individuales del archivo, crea un archivo de error llamado `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Si el problema está en filas individuales, se incluyen esas filas, con una explicación de cada error para que pueda corregirlo. Los errores se incluyen en la sección &quot;[!UICONTROL EF Error Message]&quot; columna.

## [!UICONTROL SE Error] messages

Errores en la [!UICONTROL SE Error] Las columnas de provienen directamente de la red de publicidad.

## [!UICONTROL EF Error] messages

Los siguientes errores pueden estar incluidos en la [!UICONTROL EF Error] columna en [!UICONTROL EF Errors] archivos.

### Descargar/Crear errores

| Categoría | Mensaje | Descripción |
|----|----|----|
| General | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Error total de la operación debido a un error no clasificado o no controlado. Si el problema persiste, póngase en contacto con el equipo de cuenta de Adobe para investigar la causa. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Search, Social y Commerce no se pudieron sincronizar con la red de anuncios antes de crear la hoja de edición masiva, por lo que no se creó ninguna hoja de edición masiva. Si el problema persiste, póngase en contacto con el equipo de cuenta de Adobe. |

### Errores de carga

| Categoría | Mensaje | Descripción |
|----|----|----|
| General | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | Error total en la operación. Si el problema persiste, póngase en contacto con el equipo de cuenta de Adobe. |
| Todas las entidades | [!UICONTROL Invalid Fields.] \[campos y errores no válidos\] | Faltan los datos especificados o no son válidos. |
|  | [!UICONTROL Invalid Reference Given] | El ID de la entidad en la red de publicidad o el ID de una entidad principal (como el ID de cuenta) no corresponde a una entidad en Search, Social y Commerce. Esto puede ocurrir cuando editó el ID en la hoja de edición masiva. |
|  | [!UICONTROL <Entity> is deleted or expired] | La entidad ha caducado o se ha eliminado y no puede cambiar sus propiedades. La entidad se puede eliminar cuando alguien edita el estado manualmente. |
|  | [!UICONTROL <Entity> status should be Active or Paused] | (Nuevas entidades) Una nueva entidad solo puede estar &quot;Activa&quot; o &quot;En pausa&quot;. |
|  | [!UICONTROL Duplicate Entries are present] | Se incluyen varias filas para la misma entidad, con atributos diferentes en cada fila. Consolide los cambios en una fila. |
|  | [!UICONTROL Invalid AMO ID given] | El ID de AMO de la fila no existe. Esto puede ocurrir si editó el ID en la hoja de edición masiva. |
|  | [!UICONTROL Invalid row given] | La fila no incluye información suficiente para determinar el tipo de entidad. Edite la fila para incluir todos los campos obligatorios para el tipo de entidad. |
| Cuentas | [!UICONTROL Provide Valid Account Details] | (Hojas de edición masiva para varias cuentas) Los identificadores de cuenta no se incluyen en todas las filas. Introduzca valores para cualquiera de las siguientes combinaciones de columnas para cada fila: a) &quot;[!UICONTROL AMO ID]&quot; o b) &quot;[!UICONTROL Account Name]&quot; y &quot;[!UICONTROL Platform].&quot; |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search, Social y Commerce no tienen acceso a la cuenta de la red de publicidad, por lo que no puede crear ni editar datos de campañas. Asegúrese de que las credenciales de la cuenta de búsqueda sean correctas y de que la cuenta esté habilitada. |
| Campaign | [!UICONTROL Invalid Shopping Country specified] | (Campañas de compra) El valor de la variable &quot;[!UICONTROL Sales Country]El campo &quot; no es válido. Ver una lista de países válidos [para [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) y [para [!DNL Microsoft® Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| Todos los componentes de campaña | [!UICONTROL Campaign creation failed] | No se creó la campaña principal, por lo que no se creó esta entidad. Asegúrese de que todas las entidades padre contienen todos los campos obligatorios. |
| Grupo de publicidad | [!UICONTROL Campaign Row missing] | La campaña principal especificada no existe, por lo que no se creó el grupo de anuncios. Cree la campaña principal en una nueva fila. |
|  | [!UICONTROL New adgroup has both keywords and placement] | Un grupo de anuncios puede contener palabras clave o ubicaciones, pero no ambas. Cree grupos de anuncios independientes para palabras clave y ubicaciones. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]El grupo de anuncios no se creó porque no incluye al menos una palabra clave. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) No se creó el grupo de anuncios porque no incluye al menos un anuncio. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) No se creó el grupo de anuncios porque no incluye al menos un anuncio. |
| Todos los componentes del grupo de anuncios | [!UICONTROL Adgroup creation failed] | No se ha creado el grupo de anuncios principal, por lo que no se ha podido crear esta entidad. Esto puede deberse a un error en los campos del grupo de anuncios o a que la campaña principal ha fallado. Asegúrese de que todas las entidades padre contienen todos los campos obligatorios. |
|  | [!UICONTROL Adgroup Row Missing] | El grupo de anuncios principal especificado no existe, por lo que no se pudo crear la entidad. Cree el grupo de anuncios principal en una nueva fila. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | El &quot;[!UICONTROL Tracking Template]El campo &quot; solo está disponible para cuentas que utilizan direcciones URL finales/avanzadas. Elimine el valor hasta que haya migrado la cuenta para utilizar las direcciones URL finales/avanzadas. |
| Anuncio | [!UICONTROL Cannot modify attributes other than status code and url for <ad type>] | (Tipos de anuncio que no sean texto, texto expandido, producto, instalación de aplicación y búsqueda dinámica) Solo puede editar el estado y la dirección URL de este tipo de anuncio. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Cada grupo de anuncios puede incluir hasta 50 anuncios y esta hoja de edición masiva incluye más de 50. Reduzca el número de anuncios. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | El anuncio está en una entidad principal caducada o eliminada, por lo que no puede editarla. |
| Palabra clave | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campaña principal o el grupo de anuncios se han eliminado o caducado, por lo que no puede cambiar la entidad. |
| Ubicación | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campaña principal o el grupo de anuncios se han eliminado o caducado, por lo que no puede cambiar la entidad. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google Ads) Solo puede pujar por ubicaciones en campañas solo en la red de búsqueda o solo en la red de contenido, pero no en campañas dirigidas tanto a redes de contenido como de búsqueda. |
| Grupo de productos de compras | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Cada nivel de grupo de productos debe incluir un &quot;[!UICONTROL Everything Else]&quot; grupo. No puede eliminar manualmente un &quot;[!UICONTROL Everything Else]&quot; grupo; se elimina automáticamente cuando se eliminan todos los demás grupos de productos en el mismo nivel. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campaña principal o el grupo de anuncios se han eliminado o caducado, por lo que no puede cambiar la entidad. |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] (solo) El mensaje es inexacto; cada campaña puede incluir hasta cuatro (no 10) enlaces de sitios, y esta hoja de edición masiva incluye más de cuatro. Elimine algunos enlaces de sitios. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | La campaña principal ha caducado o se ha eliminado, por lo que no puede editar el vínculo a sitios. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) No se pudo crear el vínculo de sitio porque no se creó el anuncio. |
| Destino de ubicación | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | La campaña principal o el grupo de anuncios se han eliminado o caducado, por lo que no puede editar los objetivos de ubicación. |
| Exclusiones | [!UICONTROL Other than status is modified] | Solo puede editar el estado de una exclusión (&quot;[!UICONTROL Active]&quot; o &quot;[!UICONTROL Deleted]&quot;). |
| Destinos/audiencias de la lista de remarketing de Google | [!UICONTROL Invalid Audience given] | ([!DNL Google Ads] solo campañas de ) El destino de RLSA no corresponde a una RLSA (audiencia) existente. Corrija los valores en la sección &quot;[!UICONTROL Audience]&quot; y &quot;[!UICONTROL RLSA Target]&quot; columnas. |

### Errores de publicación

Los siguientes errores se producen en [!UICONTROL EF Errors] solo archivos. La mayoría de los errores de publicación provienen de la red de anuncios y se incluyen en un archivo de errores de SE.

| Categoría | Mensaje | Descripción |
|----|----|----|
| General | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | Error total en la operación. Si el problema persiste, póngase en contacto con el equipo de cuenta de Adobe. |
| Todas las entidades | [!UICONTROL Entity] se publica en la red de anuncios | La entidad se publicó en la red de publicidad, pero no se sincronizó con Buscar, Social y Comercio al mismo tiempo, por lo que los datos de la entidad no están disponibles inmediatamente en Buscar, Social y Comercio. El proceso de sincronización se activa automáticamente en este momento.<br><br>Cuando se sincronizan grandes cantidades de datos, es posible que estos no estén disponibles en Search, Social y Commerce durante varias horas o más. |
| | [!UICONTROL Skipping <ENTITY> creation since <PARENT ENTITY> creation failed.] | No se pudo crear la entidad principal, por lo que no se creó esta entidad secundaria. |

>[!MORELIKETHIS]
>
>* [Administración de datos de campaña mediante hojas de edición masiva](bulksheet-about.md)
>* [Descargar/crear un archivo de hoja de edición masiva](bulksheet-download.md)
>* [Validación de páginas de aterrizaje en archivos de hoja de edición masiva](bulksheet-validate-landing-pages.md)
>* [Cargar un archivo de hoja de edición masiva o un archivo de error corregido](bulksheet-upload.md)
>* [Publicación de hojas de edición masiva o archivos de error corregidos](bulksheet-post.md)
