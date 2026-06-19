---
title: (Nueva IU) Descargar o crear un archivo de hoja de edición por lotes
description: Aprenda a crear archivos de hojas de edición masiva descargando datos de cuenta para las redes de anuncios en la nueva IU de Search, Social y Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 1637
ht-degree: 0%

---

# (Nueva IU) Descargar o crear un archivo de hoja de edición por lotes

Puede crear hojas de edición masiva utilizando la configuración personalizada de una o varias cuentas en una o varias [redes de publicidad admitidas](about.md#bulksheet-functionality-by-network). Las hojas de edición masiva incluyen datos dentro de Search, Social y Commerce.

Para las campañas sincronizadas, puede, opcionalmente, sincronizarse con la red de publicidad antes de descargar los datos para asegurarse de que se incluyen los cambios de datos recientes en el lado de la red de publicidad. Para todas las redes de publicidad, puede generar opcionalmente nuevas URL de rastreo de clics para incluirlas en el archivo.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. En la barra de herramientas, haga clic en **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Download Bulksheet]**.

1. Especifique la [configuración de hojas de edición masiva](#bulksheet-settings):

   1. En la ficha **[!UICONTROL Selections]**, seleccione las cuentas, campañas o grupos de anuncios que desee incluir y configure las opciones de hoja de edición masiva.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Rows and Columns]**, especifique los componentes de la cuenta y los estados de los componentes para los que desea incluir filas en la hoja de edición masiva y, a continuación, especifique las columnas que desea incluir para cada componente seleccionado.

      Para obtener una lista de las filas de hojas de edición masiva disponibles, consulte &quot;[Filas de hojas de edición masiva de la red de anuncios](#bulksheet-rows-by-ad-network)&quot;.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Filters]** y, a continuación, especifique los criterios para las campañas, grupos de anuncios, anuncios/creativos, palabras clave, ubicaciones y otras entidades específicos que se incluirán en la hoja de edición masiva.

1. Haga clic en **[!UICONTROL Download]**.

Cuando comienza la tarea, la ventana muestra una notificación, pero permanece abierta para que pueda seguir creando hojas de edición masiva adicionales si es necesario. Cuando se crea el archivo, recibe una notificación por correo electrónico con un vínculo al archivo; según la cantidad de datos que se compile, la notificación puede tardar varios minutos o más. Si la generación de archivos falla, aparece un archivo de error en la vista Hojas de edición masiva y recibe una notificación por correo electrónico con un vínculo al archivo de error.

## Configuración de hoja de edición masiva {#bulksheet-settings}

### Pestaña Selecciones {#bulksheet-selections-settings}

**\[Selección de cuenta, campaña y grupo de publicidad\]**

Expanda la red y la jerarquía de cuentas y, a continuación, active la casilla de verificación situada junto a cada cuenta, campaña o grupo de anuncios cuyos datos desee incluir en la hoja de edición masiva:

* Para incluir todas las campañas y grupos de anuncios de una cuenta, active la casilla de verificación situada junto al nombre de la cuenta.

* Para incluir campañas específicas, expanda la cuenta y, a continuación, active la casilla de verificación situada junto a cada campaña que desee incluir. Para incluir grupos de publicidad específicos, expanda aún más una campaña y seleccione la casilla de verificación situada junto a cada grupo de publicidad.

>[!NOTE]
>
>* Una sola hoja de edición masiva se puede aplicar a varias cuentas dentro de varias redes de publicidad. Las columnas específicas de la red de anuncios se etiquetan en hojas de edición masiva con el nombre de la red de anuncios (como Operadores de telefonía móvil (Google Ads)).
>* Para ver el tipo de componente que es un elemento, mantenga el cursor sobre él.
>* De forma predeterminada, solo se muestran las cuentas activas y habilitadas y sus componentes activos.

**[!UICONTROL Generate Tracking URLs]:** (opcional) incluye plantillas de seguimiento y sufijos de página de aterrizaje (para redes de anuncios aplicables) en cuentas con plantillas de seguimiento o direcciones URL de destino con códigos de seguimiento incrustados en cuentas con direcciones URL de destino, para palabras clave, anuncios, ubicaciones, vínculos de sitios y [!DNL Google Ads] grupos de productos en la hoja de edición masiva. Esta opción está seleccionada de forma predeterminada.

Cuando se selecciona esta opción, las direcciones URL se generan según los parámetros de la sección [!UICONTROL Campaign Tracking] de la configuración de la cuenta o de la campaña. De forma predeterminada, si las direcciones URL de seguimiento ya existen, no se regeneran a menos que se necesiten nuevas direcciones URL (como si el tipo de coincidencia de palabra clave, el texto del anuncio o los parámetros de seguimiento de la cuenta han cambiado).

>[!NOTE]
>
>* Si el anunciante utiliza el seguimiento de conversión de Adobe Advertising y la cuenta correspondiente no está configurada para generar y cargar automáticamente las direcciones URL de seguimiento, debe generar nuevas direcciones URL de seguimiento cuando las direcciones URL base hayan cambiado.
>* Si no selecciona esta opción, puede generar direcciones URL de seguimiento más adelante cuando cargue o publique el archivo.

**[!UICONTROL Perform pre-sync]:** (opcional) indica a Search, Social y Commerce que sincronicen sus archivos con las campañas especificadas para asegurarse de que todos los datos sean iguales. De forma predeterminada, esta opción no está seleccionada.

>[!NOTE]
>
>Search, Social y Commerce se sincronizan automáticamente con la red de anuncios una vez al día, siempre que detecta una nueva campaña en la red de anuncios y cada vez que cambia los datos de campaña desde Search, Social y Commerce. Seleccione esta opción si cree que los cambios recientes en los datos de campaña o cuenta se han realizado directamente en la red de anuncios o mediante el editor de escritorio de la red de anuncios. La creación de hojas de edición masiva tarda más cuando selecciona esta opción.

**[!UICONTROL Bulksheet Name]:** Nombre de la nueva hoja de edición masiva y tipo de archivo. De forma predeterminada, el archivo se crea en formato de valores separados por tabulaciones y se le asigna un nombre de una de las siguientes opciones:

* (Para todas las cuentas de una red publicitaria) `<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (Para una sola cuenta) `<account name>_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (Para varias cuentas) `MultipleAccounts_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`

Puede cambiar el nombre del archivo. El nombre no puede incluir los siguientes caracteres: `# % & * | \ : " < > . ? /`

Si lo desea, puede cambiar el tipo de archivo. Las opciones incluyen *[!UICONTROL .tsv]* (para valores separados por tabulaciones), *[!UICONTROL .txt (unicode)]* (para texto ASCII compatible con Unicode), *[!UICONTROL .csv]* (para valores separados por comas) o *[!UICONTROL .zip]* (para formato ZIP comprimido, que se descomprime en un archivo TSV).

>[!TIP]
>
>Para las hojas de edición masiva que incluyen caracteres internacionales, utilice el formato TSV o TXT.

### Pestaña Filas y columnas {#bulksheet-rows-columns-settings}

**[!UICONTROL Bulksheet Rows]:** Las entidades, y sus estados correspondientes, que se incluirán como filas de datos en la hoja de edición masiva, con una fila por entrada. Por ejemplo, si incluye campañas activas, la hoja de edición por lotes incluye una fila por campaña activa. Solo se incluyen las entidades seleccionadas con los estados seleccionados. Los valores predeterminados se preseleccionan en función de la red de anuncios especificada. De forma predeterminada, solo se incluyen las instancias activas de las entidades seleccionadas.

Para agregar o quitar entidades, active o desactive las casillas de verificación situadas junto a las entidades. Para agregar o quitar estados de una entidad, haga clic en el menú de estado situado junto a la entidad y, a continuación, active o desactive las casillas de verificación de los estados aplicables.

Para obtener una lista de las filas disponibles por red de anuncios, consulte &quot;[Filas de hoja de edición masiva por red de anuncios](#bulksheet-rows-by-ad-network)&quot;.

**[!UICONTROL Cascading Status Hierarchy]:** filtra las entidades secundarias a aquellas con los estados de entidad principal especificados, mediante una operación AND. Por ejemplo, si selecciona &quot;Campaña activa&quot;, &quot;Grupo de publicidad activo&quot; y &quot;Palabra clave activa&quot;, la hoja de edición por lotes solo incluye palabras clave activas en grupos de anuncios activos en campañas activas.

Si no selecciona esta opción, el estado principal no se tiene en cuenta y el filtro utiliza una operación O. Por ejemplo, si selecciona &quot;Campaña activa&quot;, &quot;Grupo de publicidad activo&quot; y &quot;Palabra clave activa&quot;, la hoja de edición masiva incluye todas las campañas activas, todos los grupos de publicidad activos independientemente del estado de la campaña principal y todas las palabras clave activas independientemente del estado de la campaña principal y del grupo de publicidad.

**[!UICONTROL Bulksheet Columns]:** Las columnas que se incluirán en el archivo de hoja de edición masiva descargado:

* *[!UICONTROL AMO ID]:* (obligatorio si &quot;[!UICONTROL SE ID]&quot; no está seleccionado) Incluye un identificador único generado por [!DNL Adobe] para cada entidad o fila. Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no la publican en la red de anuncios. Posteriormente, puede editar los datos de la entidad utilizando [!UICONTROL AMO ID] como identificador, en lugar del ID de entidad y los ID de entidad principal.

* *[!UICONTROL SE ID]:* (obligatorio si &quot;[!UICONTROL AMO ID]&quot; no está seleccionado) Incluye el identificador único de la red publicitaria para cada columna incluida y sus entidades principales. Posteriormente, si edita los datos de cualquier entidad que use [!UICONTROL SE ID] como identificador, también debe incluir filas para las entidades principales (incluidos sus valores [!UICONTROL SE ID]).

* *[!UICONTROL Platform]:* Incluye una columna [!UICONTROL Platform] al principio de cada fila para indicar la plataforma de publicidad (como &quot;Baidu&quot;).

* *[!UICONTROL Acct Name]:* (obligatorio si &quot;[!UICONTROL AMO ID]&quot; no está seleccionado) Incluye el nombre de cuenta de red de anuncios para cada entidad/fila.

* \[Columnas específicas de la entidad\]: para incluir todas, ninguna o solo las columnas seleccionadas relevantes para cada entidad seleccionada en [!UICONTROL Bulksheet Rows], haga clic en ![Punta de flecha derecha](/help/search-social-commerce/assets/compressed-item.png "Punta de flecha derecha") junto al nombre de la entidad para expandirla y, a continuación, active o desactive las casillas de verificación de las columnas individuales. De forma predeterminada, se incluyen todas las columnas relevantes para cada fila de entidad seleccionada.

>[!TIP]
>
>Asegúrese de incluir columnas adecuadas para identificar el elemento en cada fila del archivo de hoja de edición masiva. Por ejemplo, si incluye filas de palabras clave por el selector [!UICONTROL Bulksheet Rows] pero excluye todas las columnas relacionadas con palabras clave, la hoja de edición masiva resultante incluirá una fila por cada instancia de palabra clave sin forma de identificar qué instancia de palabra clave pertenece a una fila específica. En este caso, no puede utilizar la hoja de edición masiva para actualizar los datos a menos que agregue manualmente la columna de ID y los valores adecuados.

### Pestaña Filtros {#bulksheet-filters-settings}

Criterios para campañas, grupos de anuncios, anuncios/creativos, palabras clave o ubicaciones específicos que se incluirán en la hoja de edición por lotes:

1. Seleccione un parámetro (nombre o ID de entidad, o cualquier elemento de un elemento creativo, palabra clave o ubicación), seleccione un operador y, a continuación, introduzca el valor aplicable.

   Por ejemplo, para devolver solamente los anuncios con &quot;zapatos&quot; en el titular de una cuenta de [!DNL Google Ads], seleccione *[!UICONTROL Headline]*, seleccione *[!UICONTROL contains]* y después escriba `shoes` en el campo de entrada.

1. (Para aplicar filtros adicionales) Para cada filtro adicional, haga clic en **[!UICONTROL +Add Filter]**, seleccione **[!UICONTROL AND]** o **[!UICONTROL OR]**, seleccione un elemento o palabra clave de anuncio y un operador y, a continuación, introduzca el valor aplicable.

## Filas de hojas de edición masiva por red de anuncios {#bulksheet-rows-by-ad-network}

| Fila de hoja masiva | [!DNL Baidu] | [!DNL Google Ads] | [!DNL LY Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo DSP] | [!DNL Yahoo Native] | [!DNL Yandex] | Notas |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí | — |
| [!UICONTROL Adgroup] | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí | Sí | — |
| [!UICONTROL Creative] *o* [!UICONTROL Creative (except RSA)] | Sí | Sí | Sí | Sí | — | — | Sí | Sí | Sí | ([!DNL Google Ads]) Úselo para todos los tipos de anuncios excepto para los anuncios de búsqueda adaptables, que están disponibles en la fila [!UICONTROL Responsive Search Ad]. |
| [!UICONTROL Responsive Search Ad] | — | Sí | — | Sí | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Sí | Sí | Sí | Sí | Sí | Sí | — | Sí | Sí | Se utiliza solo para palabras clave no negativas. Para ver las palabras clave negativas creadas en el nivel de campaña o de grupo de anuncios, utilice la fila [!UICONTROL Campaign Negative Keyword] o [!UICONTROL Adgroup Negative Keyword] cuando esté disponible. |
| [!UICONTROL Promoted Pin] | — | — | — | — | — | Sí | — | — | — | — |
| [!UICONTROL Placement] | — | Sí | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Sí | — | Sí | — | — | — | — | — | Se utiliza para los destinos de búsqueda dinámica de un grupo de anuncios. |
| [!UICONTROL Shopping Product Group] | — | Sí | — | Sí | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Sí | — | Sí | — | — | — | Sí | — | — |
| [!UICONTROL Campaign Negative Keyword] | Sí | Sí | Sí | Sí | — | — | — | Sí | — | Se utiliza solo para palabras clave negativas creadas en el nivel de campaña o de grupo de anuncios. Para ver palabras clave que no sean negativas, utilice la fila [!UICONTROL Keyword] cuando esté disponible. |
| [!UICONTROL Campaign Negative Website] | — | Sí | — | Sí | — | — | — | Sí | — | — |
| [!UICONTROL Adgroup Site Link] | — | Sí | — | — | — | — | — | Sí | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Sí | — |
| [!UICONTROL Adgroup Negative Keyword] | Sí | Sí | Sí | Sí | — | — | — | Sí | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Sí | — | Sí | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Sí | Sí | Sí | Sí | — | — | — | Sí | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | — | Sí | — | — | — | Sí | — | — |
| [!UICONTROL Campaign Device Target] | — | Sí | — | Sí | — | — | — | Sí | — | — |
| [!UICONTROL Adgroup Device Target] | — | Sí | — | Sí | — | — | — | Sí | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Sí | — | Sí | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Sí | — | Sí | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Sí | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Sí | — | — | — | — | — | — | — | — |

Para obtener más información sobre las columnas necesarias y opcionales para cada red de publicidad, consulte los artículos sobre el formato de datos de hojas de edición masiva específicas de la red de publicidad:

* [Datos de hoja de edición masiva opcionales y requeridos para  [!DNL Baidu] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)
* [Datos de hoja de edición masiva opcionales y requeridos para  [!DNL Google Ads] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
* [Datos de hoja de edición masiva opcionales y requeridos para  [!DNL LY Ads] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)
* [Datos de hoja de edición masiva opcionales y requeridos para  [!DNL Microsoft Advertising] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
* [Datos de hoja de edición masiva opcionales y requeridos para  [!DNL Naver] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
* [Datos de hoja de edición masiva opcionales y requeridos para  [!DNL Yahoo DSP] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)
* [Datos de hoja de edición masiva opcionales y requeridos para  [!DNL Yandex] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)

>[!MORELIKETHIS]
>
>* [(Nueva IU) Acerca de la administración de datos de campaña mediante hojas de edición por lotes](about.md)
>* [(Nueva IU) Cargar una hoja de edición masiva o archivo de error corregido](upload.md)
>* [(Nueva IU) Publicar hojas de edición masiva o archivos de error corregidos](post.md)
>* [(Nueva IU) Validar páginas de aterrizaje en archivos de hojas de edición masiva](validate-landing-pages.md)
