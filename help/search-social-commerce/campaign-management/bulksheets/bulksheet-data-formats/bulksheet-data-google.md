---
title: Se requieren datos de hojas de edición masiva para  [!DNL Google Ads] cuentas
description: Haga referencia a los campos de encabezado y los campos de datos requeridos en hojas de edición masiva para  [!DNL Google Ads] cuentas.
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '7859'
ht-degree: 0%

---

# Apéndice: Datos de hoja de edición masiva requeridos para las cuentas de [!DNL Google Ads]

Para crear y actualizar los datos de la campaña [!DNL Google Ads] de forma masiva, puede usar los archivos de hoja de edición masiva de Search, Social y Commerce con un formato específico para las cuentas de [!DNL Google Ads]. Puede: a) [generar archivos de hojas de edición masiva para cuentas existentes](../bulksheet-download.md) en el formato de archivo requerido o b) crearlos manualmente (consulte &quot;[Formatos de archivo de hojas de edición masiva admitidos](bulksheet-file-formats.md)&quot; para obtener información general sobre los formatos de archivo admitidos).

Cada hoja de edición masiva debe incluir los campos de encabezado y los campos de datos correspondientes necesarios para las [operaciones específicas que desea realizar](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (como crear un anuncio). Cuando un campo no es obligatorio, puede omitirlo del encabezado y de las filas de datos. Todas las columnas personalizadas se eliminan al cargar el archivo de hoja de edición masiva.

A continuación se muestra una tabla con todos los campos de datos disponibles y tablas adicionales que indican qué campos son necesarios para agregar, editar o eliminar datos para entidades individuales (como campañas y palabras clave).

## Todos los campos de datos disponibles {#bulksheet-fields-all-google}

En la tabla siguiente se describen todos los campos de datos disponibles.

Para los campos de datos relevantes para las entidades de cuenta, consulte &quot;[Campos necesarios para crear, editar o eliminar cada componente de cuenta](#bulksheet-fields-per-component-google)&quot;.

>[!NOTE]
>
>* Los valores de todas las columnas de texto distinguen entre mayúsculas y minúsculas.
>* Cuando se crea un nuevo registro y no se incluyen valores para todos los campos de datos requeridos, algunos de esos campos se asignan a los valores predeterminados especificados.
>* Para los campos que no se especifican a continuación, se utiliza el valor predeterminado para la red publicitaria.
>* Para obtener una lista de las filas de hojas de edición masiva disponibles en el cuadro de diálogo [!UICONTROL Download Bulksheet], consulte &quot;[Filas de hojas de edición masiva por red de anuncios](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network)&quot;.

| Campo | Descripción |
| ---- | ---- |
| [!UICONTROL Platform] | (Incluida en las hojas de edición masiva generadas con fines informativos) La plataforma de publicidad. Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Acct Name] | El nombre único que identifica una cuenta de red de publicidad. Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | El nombre único que identifica una campaña para una cuenta. |
| [!UICONTROL Campaign Budget] | Un límite diario de gasto para la campaña, con o sin símbolos monetarios y puntuación. Este valor anula pero no puede superar el presupuesto de la cuenta. |
| [!UICONTROL Delivery Method] | <p>La rapidez con la que se muestran los anuncios de la campaña cada día:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (predeterminado para nuevas campañas): para difundir las impresiones de publicidad a lo largo del día.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (obsoleto en octubre de 2019) Para mostrar los anuncios lo más a menudo posible hasta que se alcance el presupuesto. Como resultado, es posible que los anuncios no aparezcan más tarde ese día.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>Los canales en los que se colocarán los anuncios. Especifique una o varias opciones:</p><ul><li><p><i>[!UICONTROL Search]</i> (el valor predeterminado para nuevas campañas): para colocar anuncios en la red de búsqueda [!DNL Google Ads] (incluidos [!DNL Google Ads] sitios web de socios de búsqueda y búsqueda) y, opcionalmente, también en la red de visualización [!DNL Google Ads]. <b>Nota:</b> Las campañas dirigidas tanto a la red de búsqueda como a la red de visualización no se pueden agregar a un portafolio para la optimización de ofertas.</p></li><li><p><i>[!UICONTROL Display]</i>: para colocar anuncios solamente en la red de visualización [!DNL Google Ads].</p></li><li><p><i>[!UICONTROL Shopping]</i>: para colocar anuncios de compra en la red de compras [!DNL Google Ads] (en determinados países) y en la red de búsqueda [!DNL Google Ads] (incluidos [!DNL Google Ads] sitios web de socios de búsqueda y búsqueda). Para crear anuncios de compras, debes tener productos en una cuenta de [!DNL Google Merchant Center] y [permitir que Search, Social y Commerce descarguen datos de la cuenta](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Consulte &quot;[Implementar [!DNL Google Ads] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; para obtener más información sobre el proceso de creación de anuncios de compras.</p></li></ul> |
| [!UICONTROL Networks] | <p>Dónde colocar los anuncios. Especifique una o varias opciones:</p><ul><li><p><i>[!UICONTROL Google Search]</i>: solo anuncios de búsqueda patrocinados en la red de búsqueda de Google.</p></li><li><p><i>[!UICONTROL Search Partners]</i>: anuncios de búsqueda patrocinados por los socios de búsqueda de Google.</p></li><li><p><i>[!UICONTROL Content]</i>: para hacer pujas para mostrar anuncios de red.</p></li><li><p><i>[!UICONTROL All]</i> (el valor predeterminado para nuevas campañas): segmenta la búsqueda de Google, busca socios y contenido.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Solo red de búsqueda; aplicable solo a anuncios dinámicos de búsqueda expandidos) Dominio raíz (como example.com) o subdominio (como shoes.example.com) del sitio web cuyo contenido la red de publicidad utiliza para segmentar los anuncios dinámicos de búsqueda.<br><br><b>Notas:</b></p><ul><li><p>Los anuncios dinámicos de búsqueda ampliados se dirigen al contenido del sitio web, en lugar de a las palabras clave.</p></li><li><p>El dominio debe estar indexado por el índice de búsqueda orgánica de la red de anuncios para poder segmentarse.</p></li><li><p>Si no especifica un dominio, debe crear destinos de búsqueda dinámica, que se dirijan a todas las páginas del sitio web o a un subconjunto de ellas, para cada grupo de anuncios.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Solo red de búsqueda; aplicable solo a anuncios dinámicos de búsqueda expandidos) El idioma del dominio del sitio web especificado. <b>Nota:</b> Si el dominio contiene páginas en varios idiomas y desea segmentar todos ellos, cree una campaña independiente para cada idioma. |
| [!UICONTROL GDN Custom Bid Level] | (Campañas dirigidas únicamente a la red de visualización) Cómo pujar: por <i>[!UICONTROL Ad Group]</i> (predeterminado), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (sitio web) o <i>[!UICONTROL None]</i> (para restablecer el valor existente). Otras dimensiones (<i>Edad</i>, <i>Sexo</i>, <i>Interés y lista</i>, <i>Tema</i> y <i>Vertical</i>) están disponibles en la interfaz [!DNL Google Ads]. Si ha utilizado la interfaz [!DNL Google Ads] para configurar las ofertas de otra dimensión, se muestra ese valor, pero no puede seleccionar ni introducir esas dimensiones aquí.</p><p><b>Nota:</b></p><ul><li><p>Cuando pujes por palabra clave, crea plantillas de seguimiento en el nivel de palabra clave. Del mismo modo, cuando puje por ubicación, cree plantillas de seguimiento en el nivel de ubicación. Para todas las demás dimensiones, cree plantillas de seguimiento en el nivel de anuncio.</p></li><li><p>Cuando puja por una dimensión no admitida (edad, sexo, interés y lista o tema), Search, Social y Commerce no optimizan las ofertas para la dimensión y se aplica toda la atribución al grupo de anuncios.</p></li><li><p>Los anuncios de la red de búsqueda siempre utilizan ofertas de palabras clave.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Solo campañas de compra) La prioridad con la que se usa la campaña cuando varias campañas anuncian el mismo producto: <i>[!UICONTROL Low]</i> (el valor predeterminado para las nuevas campañas), <i>[!UICONTROL Medium]</i> o <i>[!UICONTROL High]</i>.</p><p>Cuando el mismo producto se incluye en más de una campaña, la red de anuncios utiliza primero la prioridad de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta. |
| [!UICONTROL Merchant ID] | (Campañas de compra y campañas de audiencia vinculadas únicamente a una fuente de comerciante) El ID de cliente de la cuenta de comerciante cuyos productos se utilizan para la campaña. |
| [!UICONTROL Sales Country] | (Solo campañas de compra; solo lectura para campañas existentes) El país en el que se venden los productos de la campaña. Dado que los productos están asociados a países de destino, esta configuración determina qué productos se anuncian en la campaña. |
| [!UICONTROL Product Scope Filter] | (Campañas que solo usan la red de compras [!DNL Google Ads]) Los productos de su cuenta de [!DNL Google Merchant Center] para los que se pueden crear anuncios de compras para la campaña. Puede introducir hasta siete combinaciones de dimensiones de producto y atributos en las que filtrar sus productos, utilizando el formato dimensión=atributo. Separe varios filtros con un delimitador &quot;>>&quot;. Para obtener una lista de las dimensiones de producto disponibles, consulte &quot;[Filtros de productos de campañas de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;.</p><p>Ejemplo: &quot;CategoryL1=animales>>CategoryL2=suministros para mascotas>>Brand=Acme Pet Supplied&quot;</p><p>Para eliminar los valores existentes, use el valor <code>[delete]</code> (incluidos los corchetes).</p> |
| [!UICONTROL Languages] | <p>(Solo redes de búsqueda y visualización) Los idiomas de destino de los anuncios en la campaña.</p><p>Si no escribe un valor para este campo ni para el campo [!UICONTROL Geo Targeting] de una nueva campaña, la moneda especificada para la cuenta determina los idiomas predeterminados, excepto que las campañas con monedas que no están asignadas a idiomas específicos (por ejemplo, EUR) están dirigidas a todos los idiomas. Si no escribe un valor para este campo pero escribe un valor en el campo [!UICONTROL Geo Targeting] para una nueva campaña, el valor predeterminado es <i>[!UICONTROL All]</i>. Si deja este campo en blanco para una campaña existente, se conserva el valor existente.</p><p>Para seleccionar todos los idiomas, ingrese <span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span>. Para dirigirse a idiomas específicos, escriba valores separados por punto y coma usando <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] nombres de idioma</a> (como <i>inglés;japonés</i>, que se sustituyen con los códigos numéricos correctos) o códigos numéricos (como <i>1000;1005</i>). Los valores no distinguen entre mayúsculas y minúsculas.</p> |
| [!UICONTROL Location] | Una ubicación geográfica en la que colocar los anuncios o en la que excluir los anuncios de la campaña. Si no introduce ningún valor en este campo ni en el campo Idiomas para una nueva campaña, la moneda especificada para la cuenta determina las ubicaciones predeterminadas, excepto que las campañas con monedas que no están asignadas a ubicaciones específicas (por ejemplo, EUR) están dirigidas a todas las ubicaciones. Si no escribe un valor para este campo pero escribe un valor en el campo [!UICONTROL Languages] para una nueva campaña, el valor predeterminado es <i>[!UICONTROL All]</i>. Si deja este campo en blanco para una campaña existente, el valor existente se conserva.</p><p>Para dirigirse a una ubicación específica, use uno de [[!DNL Google Ads] nombres de ubicación](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (que se sustituyen por el código numérico correcto) o códigos de ubicación:</p><ul><li><p>Países o territorios: escriba los nombres de los países o territorios (como <i>Estados Unidos;Japón</i>) o los códigos numéricos (como <i>2840;2392</i>).</p></li><li><p>Estados/provincias/regiones: escriba los nombres de los estados/provincias/regiones con las abreviaturas de los países/territorios relacionados (como <i>Tokio, JP;Nueva York, US</i>) o los códigos numéricos (como <i>20636;21167</i>).</p></li><li><p>Ciudades fuera de los Estados Unidos: escriba el nombre de la ciudad, el nombre del estado/provincia/región y las abreviaturas de país/territorio (como <i>Adachi, Tokio, JP;Kita, Tokio, JP</i>) o los códigos numéricos (como <i>1028850;1009293</i>)</p></li><li><p>Áreas metropolitanas de EE. UU.: escriba los nombres de las ciudades, los nombres de los estados y las abreviaturas de los países (como <i>Buffalo NY, US;New York NY, US</i>) o los códigos numéricos (como <i>514;501</i>).</p></li></ul><p>Para excluir una ubicación, coloque delante del nombre de la ubicación o del código un signo menos (`-`), como <i>-Japón</i>.</p><p><b>Nota:</b> Los valores no distinguen entre mayúsculas y minúsculas.</p> |
| [!UICONTROL Location Type] | (Cuando se incluye una ubicación) El [tipo de ubicación](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Un tipo de dispositivo para el cual se realizan ajustes de oferta en el nivel de campaña o de grupo de anuncios: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> o <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(Cuando se incluye un destino de [!UICONTROL Location], [!UICONTROL Device] o [!UICONTROL RLSA]) Si se ajustan las ofertas de anuncios en una ubicación específica, en un tipo de dispositivo específico o con un destino de audiencia específico:</p><ul><li><p>Para usar la oferta a nivel de palabra clave (0% de diferencia), escribe 0. Para nuevos objetivos, también puede dejar esto en blanco.</p></li><li><p>Para utilizar una oferta diferente para este objetivo, introduzca el porcentaje en el que desea aumentar o disminuir las ofertas.</p></li><ul><li><p>Para los objetivos de ubicación y RLSA, los porcentajes válidos incluyen de -90 a 900.</p></li><li><p>Para los ajustes de oferta de dispositivo, los porcentajes válidos incluyen:</p></li><ul><li><p>(Campañas)-100 (para no pujar por anuncios en el tipo de dispositivo) o de -90 a 900.</p></li><li><p>(Grupos de anuncios): 100 para smartphones y tabletas (para no pujar por el tipo de dispositivo) y de -90 a 900 para todos los tipos de dispositivos.</p></li></ul></ul><li><p>(Campañas y grupos de anuncios existentes) Para utilizar el ajuste de oferta existente, déjelo en blanco.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Incluido en las hojas de edición masiva generadas con fines informativos) El ajuste de oferta de solo lectura que Adobe recomienda para el objetivo de ubicación de nivel de campaña o un RLSA. Se calcula únicamente cuando la campaña se encuentra en un portafolio con un objetivo que utiliza métricas de conversión ponderadas (no el objetivo [!UICONTROL Maximize Clicks]) y la campaña contiene al menos dos objetivos de ubicación o RLSA con al menos cinco clics o cinco dólares en coste durante los últimos 90 días.</p><p>Si desea editar manualmente un destino de ubicación o RLSA para utilizar el valor recomendado, espere al menos dos semanas después de crear el destino de ubicación o RLSA para permitir una recopilación de datos suficiente y no cambie el valor más de una vez a la semana. |
| [!UICONTROL Device Targets] | <p>(Solo tipos de campañas heredadas) Los dispositivos en los que se puede mostrar el anuncio: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> o <i>[!UICONTROL Tablets]</i>. Para nuevas campañas, el valor predeterminado es <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Solo tipos de campañas heredadas; aplicable cuando los Destinos del dispositivo incluyen &quot;Smartphones&quot; o &quot;Tablets&quot;) Los sistemas operativos en los que se puede mostrar el anuncio: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> o <i>[!UICONTROL Palm]</i>. Para nuevas campañas, el valor predeterminado es <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Solo tipos de campañas heredadas; aplicable cuando [!UICONTROL Device Targets] incluye &quot;[!UICONTROL All]&quot; o &quot;[!UICONTROL Smartphones]&quot;) Operadores de telefonía móvil a los que pueden estar conectados los smartphones: <i>[!UICONTROL All]</i>, o uno o más operadores indicados por &lt;c<i>código de operador</i>>,&lt;<i>código de país</i>> (como T-Mobile,US) mediante la lista de <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">operadores y códigos disponibles para [!DNL Google Ads]</a>. Separe varios operadores con punto y coma (como T-Mobile,US;T-Mobile,GB). Para nuevas campañas, el valor predeterminado es <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>El nombre único que identifica un grupo de anuncios. La longitud máxima es de 255 caracteres; los caracteres en blanco finales no se guardan (por ejemplo, &quot;Grupo de anuncios 1&quot; se guarda como &quot;Grupo de anuncios 1&quot;). Este campo no es aplicable a vínculos de sitio de nivel de campaña o a destinos de dispositivo de nivel de campaña.</p> |
| [!UICONTROL Ad Group Type] | <p>El tipo de grupo de anuncios: <i>[!UICONTROL Demand Gen]</i> (solo para campañas de generación de demanda), <i>[!UICONTROL Display]</i> (para campañas de visualización), <i>[!UICONTROL Search Dynamic]</i> (para anuncios dinámicos de búsqueda expandidos), <i>[!UICONTROL Search Standard]</i> (para anuncios de búsqueda), <i>[!UICONTROL Shopping Product]</i> (para anuncios de productos de compra), <i>[!UICONTROL Shopping Showcase]</i> (no se admite la creación y edición) o <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Solo campañas CPC) El coste por clic máximo (CPC), que es la cantidad más alta que se paga por un clic de anuncio en la red de anuncios, con o sin símbolos monetarios y puntuación. Puede establecer valores para grupos de anuncios y palabras clave, grupos de productos y destinos de búsqueda dinámica. El valor predeterminado de una palabra clave nueva se hereda del nivel de grupo de anuncios. Para los grupos de productos, puede establecer valores para el nivel de grupo de productos más bajo; el valor predeterminado para un nivel nuevo se hereda del nivel principal.</p><p>Para los grupos de productos existentes y los destinos de búsqueda dinámica en portafolios optimizados, las actualizaciones son efectivas solo para un día y se sobrescriben durante el siguiente ciclo de optimización.</p> |
| [!UICONTROL Max Content CPC] | <p>(Solo campañas CPC) El coste por clic (CPC) máximo de contenido, que es la cantidad más alta que se paga por un clic de anuncio desde un sitio de red de visualización, con o sin símbolos monetarios y puntuación. Puede establecer y editar valores en el nivel de grupo de anuncios en campañas que no estén segmentadas por ubicación.</p> |
| [!UICONTROL Audience Target Method] | <p>(Campañas solo en la red de búsqueda y las campañas existentes de solo lectura [!DNL Gmail] en la red de visualización) Si se desea:</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>: para mostrar anuncios solo a usuarios asociados con audiencias de destino que también cumplan cualquier otro objetivo para el grupo de anuncios.</p></li><li><p><i>[!UICONTROL Bid Only]</i>: para mostrar anuncios incluso a personas que no están asociadas con audiencias de destino siempre y cuando satisfagan otros objetivos de nivel de grupo de anuncios.</p><p>Sin embargo, puedes aumentar las probabilidades de que se muestren anuncios a audiencias específicas si estableces pujas más altas para esas audiencias.</p></li></ul> |
| [!UICONTROL Keyword] | Cadena de palabra clave. La longitud máxima es de 80 caracteres y no más de 10 palabras, y solo puede incluir letras, dígitos y los siguientes caracteres especiales: espacio `# $ & _ - " [ ] ' + . / :`</p><p><b>Nota:</b></p><ul><li><p>Para excluir una palabra clave en el nivel de grupo de anuncios o de campaña, establezca [!UICONTROL Match Type] en <i>[!UICONTROL Negative]</i>. Si la fila incluye el nombre del grupo de anuncios, la palabra clave se excluye para el grupo de anuncios. Si la fila no incluye el nombre del grupo de anuncios, la palabra clave se excluye para toda la campaña.</p></li><li><p>Al cambiar una palabra clave [!DNL Google Ads] o un tipo de coincidencia, se eliminará la palabra clave existente y se creará una nueva.</p></li></ul> |
| [!UICONTROL Placement] | (Campañas que solo usan coincidencia de contenido) Una ubicación en la red de visualización en la que se pueden mostrar los anuncios. Especifique una de las siguientes opciones:</p><ul><li><p>Sitio web: introduzca una dirección URL válida. Puede ser un dominio de nivel superior, un subdominio de primer nivel o un dominio con un solo nombre de directorio. La dirección URL no puede incluir el signo de interrogación (?). Ejemplos:<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>Una posición de anuncio en una página específica: Use el formato `<URL> >> <location,sublocation>` (como `finance.google.com >> Company pages,Top right`).</p></li><li><p>Una categoría de tema: utilice la sintaxis `<category::<category> > <subcategory>`, etc. (como `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Nota:</b> Para excluir una ubicación en el nivel de grupo de anuncios o de campaña, establezca [!UICONTROL Match Type] en <i>[!UICONTROL Negative]</i>. Si la fila incluye el nombre del grupo de anuncios, la ubicación se excluye para el grupo de anuncios. Si la fila no incluye el nombre del grupo de anuncios, la ubicación se excluye para toda la campaña.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Necesario cuando la configuración de campaña &quot;[!UICONTROL Use my website contents to target my ads]&quot; no está habilitada; opcional en caso contrario) Los destinos de búsqueda dinámica para el grupo de anuncios.</p><p>Utilice un asterisco (*) para todos los destinos.</p><p>Para dirigirse a un máximo de tres criterios de búsqueda dinámica, use el formato `<category>=<target>`, donde `<category>` puede incluir cualquiera de las categorías siguientes. Unir varios destinos para una categoría individual con &quot;\[espacio en blanco\] y \[espacio en blanco\]&quot; y unir varias categorías con &quot;[espacio en blanco] y [espacio en blanco]&quot;.</p><ul><li><p><i>[!UICONTROL Category]</i>: para mostrar anuncios dinámicos de búsqueda expandidos para páginas indizadas con una categoría de contenido [!DNL Google Ads] específica.</p></li><li><p><i>[!UICONTROL URL]</i>: para mostrar anuncios dinámicos de búsqueda expandidos para páginas indizadas con una dirección URL específica, donde el valor se puede incluir en cualquier lugar dentro de la dirección URL.</p></li><li><p><i>[!UICONTROL Page Title]</i>: para mostrar anuncios dinámicos de búsqueda expandidos para páginas indizadas con texto específico en el título de la página.</p></li><li><p><i>[!UICONTROL Page Content]</i>: para mostrar anuncios dinámicos de búsqueda expandidos para páginas indizadas con contenido específico.</p></li></ul><p>Ejemplo: url=shoes.example.com y page title=calzado</p> |
| [!UICONTROL Parent Product Groupings] | La jerarquía de cualquier grupo de productos principal.<br><br>Ejemplo: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>El grupo de productos (como &quot;brand=acme&quot; o &quot;All Products&quot;).</p><p><b>Nota:</b></p><ul><li><p>Cuando un grupo de productos especificado no existe en la jerarquía de [!UICONTROL Parent Product Groupings], Search, Social y Commerce crean las partes de la jerarquía que sean necesarias.</p></li><li><p>Search, Social y Commerce crean automáticamente un grupo &quot;[!UICONTROL All Products]&quot; cuando crea un grupo de anuncios en una campaña de compras de [!DNL Google Ads] con una oferta predeterminada establecida en la oferta predeterminada del grupo de anuncios. Search, Social y Commerce crean automáticamente un grupo &quot;[!UICONTROL Everything Else]&quot; con la oferta predeterminada del grupo de anuncios en cada nivel de la jerarquía del grupo de productos. Aún puede crear explícitamente estos grupos predeterminados y excluirlos o cambiar sus ofertas.</p></li><li><p>Cada grupo de anuncios puede incluir hasta ocho niveles de grupos de productos, incluidos &quot;[!UICONTROL All Products]&quot; y otros siete niveles.</p></li></ul> |
| [!UICONTROL Partition Type] | El tipo de partición para el grupo de productos: <i>subdivisión</i> (cuando tiene grupos de productos secundarios) o <i>unidad</i> (cuando no tiene grupos de productos secundarios). |
| [!UICONTROL Match Type] | <p>Para destinos de búsqueda dinámica o grupos de productos: La opción de coincidencia de palabras clave para el destino de búsqueda dinámica o el grupo de productos: <i>[!UICONTROL Dynamic Ad Target]</i> (el valor predeterminado para los nuevos destinos de búsqueda dinámica), <i>[!UICONTROL Product Group]</i> (el valor predeterminado para los nuevos grupos de productos) o <i>[!UICONTROL Negative Product Group]</i> (para excluir un grupo de productos).</p><p>Para palabras clave: La opción de coincidencia de palabras clave para la palabra clave: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> o <i>[!UICONTROL Negative]</i> (para excluir una palabra clave o una ubicación en la red de visualización); los grupos de productos que se utilizan con anuncios de compras tienen un tipo de coincidencia de <i>[!UICONTROL Product Group]</i>. Si usa <i>[!UICONTROL Negative]</i>, también debe incluir el tipo de coincidencia que se va a excluir (por ejemplo, &quot;Frase negativa&quot;).</p><p>Para las nuevas palabras clave, el valor predeterminado es <i>[!UICONTROL Broad]</i>. Un valor para el tipo de coincidencia o el ID de palabra clave solo es necesario para editar una palabra clave con varios tipos de coincidencia.</p><p><b>Nota:</b></p><ul><li><p>Los tipos de coincidencia no son aplicables a los anuncios dinámicos de búsqueda expandidos, que no utilizan palabras clave.</p></li><li><p>Al cambiar el tipo de coincidencia para una palabra clave [!DNL Google Ads], se eliminará la palabra clave existente y se creará una nueva.</p></li><li><p>Para Modificador de coincidencia amplia, elija &quot;Amplia&quot; e inserte un + antes de cualquier palabra dentro de la palabra clave para la cual se requieren variantes cercanas (como &quot;+rojo +zapatos&quot; para requerir variantes cercanas de &quot;rojo&quot; y &quot;zapatos&quot;). <b>Nota:</b> Los modificadores de coincidencia amplia ahora tienen el mismo comportamiento de coincidencia que la coincidencia de frase para algunos idiomas y no ha podido crear nuevas palabras clave de modificador de coincidencia amplia desde julio de 2021. Consulte [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/7042511) para obtener más información.</p> |
| [!UICONTROL First Page Bid] | (Incluido en las hojas de edición masiva generadas con fines informativos) La oferta necesaria para colocar un anuncio en la primera página de los resultados de búsqueda. Este valor no se publica en la red de anuncios. |
| [!UICONTROL Quality Score] | (Incluido en hojas de edición masiva generadas con fines informativos) La puntuación de calidad actual que el motor de búsqueda ha asignado a la palabra clave. Este valor no se publica en la red publicitaria). |
| [!UICONTROL Creative Preferred Devices] | (Anuncios de texto, anuncios dinámicos de búsqueda expandidos y vínculos de sitio mejorados; opcional) Los tipos de dispositivo en los que prefiere mostrar el anuncio: <i>[!UICONTROL All]</i> (predeterminado) o <i>[!UICONTROL Mobile]</i>. Cuando se especifica <i>[!UICONTROL Mobile]</i>, la red intenta mostrar el anuncio a usuarios de dispositivos móviles en lugar de a usuarios de equipos de escritorio o tabletas. De lo contrario, la red muestra el anuncio en cualquier tipo de dispositivo.</p><p><b>Nota:</b></p><ul><li><p>Solo los usuarios administradores y [!DNL Adobe] administradores de cuentas pueden editar esta configuración.</p></li><li><p>La red no garantiza que muestre el anuncio en el tipo de dispositivo preferido.</p></li><li><p>Los nuevos vínculos de sitio mejorados solo se pueden crear en campañas con vínculos de sitio mejorados existentes o sin vínculos de sitio.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Solo anuncios de texto expandidos y anuncios de búsqueda adaptables) Los titulares de un anuncio, cada uno separado por una barra vertical (&vert;). La longitud máxima de cada campo de título de anuncio es de 30 caracteres o 15 caracteres de doble byte, incluido cualquier texto dinámico (como los valores de las palabras clave y los personalizadores de anuncios).</p><p>Para los anuncios adaptables de búsqueda, se requieren [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] y [!UICONTROL Ad Title 3], y todos los demás campos de título de anuncio son opcionales. Para eliminar el valor existente de un campo no obligatorio, use el valor <code>[delete]</code> (incluidos los corchetes).</p><p>Para los anuncios adaptables de búsqueda, inserte un personalizador de anuncios con el formato siguiente: <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, como <code>{CUSTOMIZER.Discount:10%}</code></p><p>No puede crear ni editar, pero sí eliminar los anuncios de texto expandidos que [!DNL Google Ads] dejaron de usarse en junio de 2022. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Solo anuncios de búsqueda adaptables; opcional) Una posición en la que fijar el título del anuncio correspondiente: `[null]` (sin valor, lo que hace que el título del anuncio sea apto para todas las posiciones), <i>1</i>, <i>2</i> o <i>3</i>. Por ejemplo, si [!UICONTROL Ad Title Position] tiene un valor de 1, entonces el Título de anuncio solo aparece en la Posición 1. De forma predeterminada, todos los títulos de los anuncios son nulos (no tienen valores).</p><p>Para eliminar el valor existente, use el valor <code>[delete]</code> (incluidos los corchetes).</p><p><b>Nota:</b> Puede fijar varios títulos de anuncios en la misma posición. La red de anuncios utiliza uno de los títulos de anuncios anclados a la posición. Es posible que los títulos anclados a la posición 3 no se muestren con el anuncio.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Solo anuncios dinámicos de búsqueda expandidos, anuncios de texto expandidos y anuncios de búsqueda adaptables) El cuerpo de un anuncio. La longitud máxima de cada campo de descripción es de 90 caracteres o 45 caracteres de doble byte, incluido cualquier texto dinámico (como los valores de las palabras clave y los personalizadores de anuncios).</p><p>Para los anuncios adaptables de búsqueda, inserte un personalizador de anuncios con el formato siguiente: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, como `{CUSTOMIZER.Discount:10%}`</p><p>Para anuncios dinámicos de búsqueda expandidos, use [!UICONTROL Description Line 1] y [!UICONTROL Description Line 2] solamente. <b>Nota:</b> Para este tipo de anuncio, al cambiar la copia de anuncio se eliminará el anuncio existente y se creará uno nuevo.</p><p>No puede crear ni editar, pero sí eliminar los anuncios de texto expandidos que [!DNL Google Ads] dejaron de usarse en junio de 2022.</p><p>Para los anuncios de búsqueda adaptables, se requieren [!UICONTROL Description Line 1] y [!UICONTROL Description Line 2], y [!UICONTROL Description Line 3] y [!UICONTROL Description Line 4] son opcionales. Para eliminar el valor existente, use el valor <code>[delete]</code> (incluidos los corchetes).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Solo anuncios de búsqueda adaptables; opcional) Una posición en la que fijar la descripción correspondiente: `[null]` (sin valor, lo que hace que la descripción sea apta para todas las posiciones), <i>1</i>, <i>2</i> o <i>3</i>. Por ejemplo, si [!UICONTROL Description 1 Position] tiene un valor de 1, entonces [!UICONTROL Description 1] solo aparece en la posición 1. De forma predeterminada, no se anclan descripciones a una posición.</p><p>Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes).</p><p><b>Nota:</b> Puede fijar varias descripciones en la misma posición. La red publicitaria utiliza una de las descripciones ancladas a la posición. Las descripciones ancladas a la posición 2 pueden no mostrarse con el anuncio. |
| [!UICONTROL Display URL] | Dirección URL que se incluye en el anuncio.<br><br>Para los anuncios dinámicos de búsqueda expandidos, [!DNL Google Ads] genera este valor dinámicamente desde el dominio del sitio web y no es necesario que escriba ningún valor.<br><br>Para los anuncios adaptables de búsqueda, no es necesario que escriba un valor. La dirección URL mostrada se extrae automáticamente del dominio en la dirección URL final. Opcionalmente, puede personalizar la dirección URL mediante los campos Ruta 1 y Ruta 2.<br><br>No puede crear ni editar anuncios de texto expandidos, pero sí eliminar, que [!DNL Google Ads] dejó de usarse en junio de 2022.<br><br><b>Nota:</b> (Cuentas con direcciones URL finales) Los nombres de dominio de la dirección URL mostrada y de la dirección URL final deben coincidir.</p> |
| [!UICONTROL Display Path 1] | <p>(Solo anuncios de texto expandidos <span> y anuncios de búsqueda adaptables </span>)</p><p>(Opcional) Texto que se añade a la dirección URL para mostrar que se extrae automáticamente de la dirección URL final. Va precedido en la dirección URL por una barra diagonal (/). Una ruta de acceso no puede contener caracteres de barra diagonal (/) o de línea nueva (\n). La longitud máxima es de 15 caracteres o 7 caracteres de doble byte.</p><p>Para insertar un personalizador de anuncios, use los siguientes formatos, donde `Default text` es un valor opcional que insertar cuando el archivo de fuente no incluye un valor válido:&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, como `{CUSTOMIZER.Discount:10%}`</p><p>Por ejemplo, si [!UICONTROL Display Path 1] es &quot;ofertas&quot;, la dirección URL para mostrar es &lt;<i>URL para mostrar</i>>/ofertas, como www.example.com/deals.</p><p>No puede crear ni editar, pero sí eliminar los anuncios de texto expandidos que [!DNL Google Ads] dejaron de usarse en junio de 2022.</p> |
| [!UICONTROL Display Path 2] | Una segunda ruta de visualización; vea la entrada de [!UICONTROL Display Path 1].<br><br>Ejemplo: si [!UICONTROL Display Path 1] es &quot;acuerdos&quot; y [!UICONTROL Display Path 2] es &quot;local&quot;, la URL para mostrar es &lt;<i>URL para mostrar</i>>/acuerdos/local, como www.example.com/deals/local.</p><p>No puede crear ni editar, pero sí eliminar los anuncios de texto expandidos que [!DNL Google Ads] dejaron de usarse en junio de 2022.</p> |
| [!UICONTROL Promotion Line] | (Solo anuncios de listado de productos) Una línea de promoción opcional que se incluirá con el listado de productos en los resultados de búsqueda. La longitud máxima es de 45 caracteres.</p><p>La línea de promoción puede aparecer en diferentes ubicaciones relacionadas con el anuncio (por ejemplo, debajo del anuncio), en función de dónde aparezca el anuncio en la página. |
| [!UICONTROL Link Name] | <p>El texto del vínculo de sitio. Puede incluir hasta 25 caracteres.</p><p>Para los nuevos vínculos de sitio, debe incluir el nombre de la campaña dentro de la fila de vínculos de sitio. Para los vínculos de sitios de nivel de grupo de anuncios, también debe incluir el nombre del grupo de anuncios.</p><p><b>Nota:</b> El texto existente de 35 caracteres se seguirá mostrando en los anuncios de equipos de escritorio y tabletas, pero no en los dispositivos móviles.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Solo anuncios de instalación de aplicaciones existentes) El sistema operativo en el que se ejecuta la aplicación móvil: <i>Android™</i> o <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Solo anuncios de instalación de aplicaciones existentes) <p>ID de aplicación o nombre del paquete. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Solo anuncios de instalación de aplicaciones existentes) El nombre de la aplicación. |
| [!UICONTROL Start Date] | <p>(Solo vínculos de sitio mejorados) La primera fecha en la que se pueden realizar ofertas para el vínculo de sitio, en el huso horario del anunciante y en uno de los formatos siguientes: <i>m/d/aaaa</i>, <i>m/d/aa</i>, <i>m-d-aaaa</i> o <i>m-d-aa</i>. El valor predeterminado para los nuevos vínculos de sitio mejorados es el día actual.</p><p><b>Nota:</b> Los nuevos vínculos de sitio mejorados solo se pueden crear en campañas con vínculos de sitio mejorados existentes o sin vínculos de sitio.</p> |
| [!UICONTROL End Date] | <p>(Solo vínculos de sitio mejorados) La última fecha en la que se pueden realizar ofertas para el vínculo de sitio, en el huso horario del anunciante y en uno de los siguientes formatos:  <i>d/m/aaaa</i>, <i>d/m/aa</i>, <i>d-m-aaaa</i> o <i>d-m-aa</i>. El valor predeterminado es ninguno (sin fecha de finalización).</p><p><b>Nota:</b> Los nuevos vínculos de sitio mejorados solo se pueden crear en campañas con vínculos de sitio mejorados existentes o sin vínculos de sitio.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Solo anuncios de instalación de aplicaciones existentes)</p><p>(Opcional) Impide que [!DNL Google Ads] muestre el anuncio a los usuarios de Tablet PC. Los valores pueden incluir <i>yes</i> y <i>no</i>. |
| [!UICONTROL Landing Page Suffix] | Cualquier parámetro que se adjunte al final de las direcciones URL finales para rastrear la información. Ejemplo: `param2=value1&param3=value2`<br><br>Consulte &quot;[Formatos de seguimiento de clics para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)&quot;.<br><br>Los sufijos finales de URL en los niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, use el editor [!DNL Google Ads]. |
| [!UICONTROL Tracking Template] | La plantilla de seguimiento, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, e incrusta la dirección URL final en un parámetro [!DNL ValueTrack]. La plantilla de seguimiento en el nivel más granular (con la palabra clave como más granular) anula los valores en todos los niveles superiores.<br><br>Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce anexa automáticamente su propio código de redirección y seguimiento al guardar el registro.<br><br>Para redirecciones y seguimiento de terceros, escriba un valor. Para obtener una lista de [!DNL ValueTrack] parámetros que indiquen las direcciones URL finales en las plantillas de seguimiento, consulte los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección sobre &quot;Parámetros disponibles [!DNL ValueTrack]&quot; en la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/2375447).<br><br>Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Base URL/Final URL] | La dirección URL de la página de aterrizaje a la que se dirigen los usuarios del motor de búsqueda cuando hacen clic en el anuncio, incluidos los parámetros de adición configurados para la campaña o la cuenta. Las direcciones URL base/final en el nivel de palabra clave anulan las del nivel de anuncio y posteriores.<br><br>Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Destination URL] | (Incluido en hojas de edición masiva generadas con fines informativos; no publicado en el motor de búsqueda) Para cuentas con direcciones URL de destino, esta es la dirección URL que vincula un anuncio a una dirección URL o página de aterrizaje base en el sitio web del anunciante (a veces a través de otro sitio que rastrea el clic y luego redirige al usuario a la página de aterrizaje). Incluye cualquier parámetro de adición configurado para la campaña o cuenta de Search, Social y Commerce. Si ha generado direcciones URL de seguimiento, esto se basa en los parámetros de seguimiento de la configuración de la cuenta y la configuración de la campaña. Si ha anexado parámetros específicos del motor de búsqueda, pueden reemplazarse por los parámetros equivalentes para Buscar, Social y Commerce.<br><br>Para cuentas con direcciones URL finales, esta columna muestra el mismo valor que la columna Dirección URL base/Dirección URL final. |
| [!UICONTROL Custom URL Param] | Datos para sustituir la variable dinámica `{custom_code}` cuando la variable se incluye en los parámetros de seguimiento de la configuración de la cuenta de búsqueda o de la campaña. Para insertar el valor personalizado en la dirección URL de seguimiento, debe cargar el archivo de hoja de edición masiva mediante la opción Generar direcciones URL de seguimiento. |
| [!UICONTROL Creative Type] | El formato de anuncio: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Demand Gen Carousel Ad]</i> (anuncios de carrusel de varias imágenes), <i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>, <i>[!UICONTROL Demand Gen Product Ad]</i> y <i>[!UICONTROL Demand Gen Video Ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (tipo de anuncio obsoleto), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (obsoleto), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (anuncios de compra) o <i>[!UICONTROL Responsive search ad]</i>. El valor predeterminado para los anuncios nuevos es <i>[!UICONTROL Text ad]</i>.<br><br>Necesario para crear o editar el estado de un anuncio de producto. |
| [!UICONTROL Param1] | <p>El valor numérico del parámetro de anuncio `{param1}`, que se puede incluir en la copia de anuncio o en la dirección URL de visualización para cualquier anuncio en el archivo de hoja de edición por lotes. La longitud máxima es de 25 caracteres y puede incluir los siguientes caracteres no numéricos:</p><ul><li><p>El valor puede ir precedido o anexado con un símbolo de moneda o código. Por ejemplo, `£2.000,00` y `2000GBP` son válidos.</p></li><li><p>El valor puede incluir una coma (`,`) o un punto (`.`) como separador, con un punto opcional (`.`) o una coma (`,`) para los valores fraccionarios. Por ejemplo, `1,000.00` y `2.000,10` son válidos.</p></li><li><p>Al valor se le puede agregar un prefijo o un signo de porcentaje (`%`), un signo más (`+`) o un signo menos (`- `). Por ejemplo, `20%`, `208+` y `-42.32` son válidos.</p></li><li><p>Se pueden incrustar dos números con una barra diagonal. Por ejemplo, `4/1` y `0.95/0.45` son válidos.</p></li></ul><p>Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes).</p> |
| [!UICONTROL Param2] | El valor numérico del parámetro de anuncio `{param2}`, que se puede incluir en la copia de anuncio o en la dirección URL de visualización para cualquier anuncio en el archivo de hoja de edición por lotes. Consulte la entrada correspondiente a Param1 para obtener más información. |
| [!UICONTROL Audience] | La lista de remarketing para anuncios de búsqueda (RLSA) incluye la audiencia de destino o excluida para la campaña o el grupo de anuncios. Especifique si se trata de un objetivo o de una exclusión en el campo &quot;Tipo de objetivo&quot;. |
| [!UICONTROL Target Type] | (Cuando se especifica una audiencia) Si la audiencia especificada es una <i>Inclusión</i> (destino) o <i>Exclusión</i>. |
| [!UICONTROL Campaign Status] | El estado de visualización de la campaña: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (no editable) o <i>[!UICONTROL Deleted]</i> (solo campañas existentes). El valor predeterminado para las nuevas campañas es <i>[!UICONTROL Active]</i>. Para eliminar una campaña activa o pausada, ingrese el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | El estado de visualización del grupo de anuncios: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo grupos de anuncios existentes). El valor predeterminado para los nuevos grupos de anuncios es [!UICONTROL Active]. Para eliminar un grupo de anuncios activo o en pausa, escriba el valor `Deleted`. |
| [!UICONTROL Keyword Status] | Estado de visualización de la palabra clave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo palabras clave existentes). El valor predeterminado para las nuevas palabras clave es [!UICONTROL Active]. Para eliminar una palabra clave activa o pausada, escriba el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | El estado de visualización del anuncio: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (solo anuncios existentes), <i>[!UICONTROL Disapproved]</i> (no editable) o <i>[!UICONTROL Paused]</i>. El valor predeterminado para los anuncios nuevos es [!UICONTROL Active]. Para eliminar un anuncio activo o en pausa, escriba el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | El estado de la ubicación del sitio web: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo anuncios existentes). El valor predeterminado para los sitios web nuevos es <i>Activo.</i> Para eliminar una ubicación activa o en pausa, escriba el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | Estado de un destino de búsqueda dinámica: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo destinos existentes). El valor predeterminado para los nuevos destinos es <i>Activo.</i> Para eliminar un destino activo o pausado, escriba el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | El estado de visualización del grupo de productos: <i>[!UICONTROL Active]</i> <span>o</span> <i>[!UICONTROL Deleted]</i> (solo grupos de productos existentes). El valor predeterminado para los nuevos grupos de productos es <i>[!UICONTROL Active]</i>. Para eliminar un grupo de productos activo, escriba el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | Estado de visualización del vínculo de sitio: <i>Activo o eliminado</i> (solo vínculos de sitio existentes). El valor predeterminado para los nuevos vínculos de sitio es <i>[!UICONTROL Active]</i>. Para eliminar un vínculo de sitio activo, escriba el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | Estado del destino de ubicación: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo ubicaciones existentes). El valor predeterminado para las nuevas ubicaciones es [!UICONTROL Active]. Para eliminar una ubicación activa, escriba el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | El estado del destino o la exclusión de RLSA de nivel de grupo de anuncios o de campaña: <i>[!UICONTROL Active]</i> o [!UICONTROL Deleted]</i> (solo destinos existentes). El valor predeterminado para los nuevos destinos o exclusiones es <i>[!UICONTROL Active]</i>. Para eliminar un destino o una exclusión activos, escriba el valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>Estado del destino de dispositivo de nivel de campaña o de grupo de anuncios: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i>. Para nuevas campañas y grupos de anuncios, el valor predeterminado es <i>[!UICONTROL Active]</i>.</p> |
| \[Clasificación de etiquetas específica del anunciante\] | (Nombrado para una clasificación de etiquetas específica del anunciante, como &quot;Color&quot; para una clasificación de etiquetas denominada Color) Un valor para la clasificación especificada que está asociada a la entidad. Solo se puede incluir un valor por clasificación por entidad (como &quot;rojo&quot; para la clasificación de etiquetas &quot;Color&quot; para la Campaña A). La longitud máxima es de 100 caracteres y el valor puede incluir caracteres ASCII y no ASCII.<br><br>Las clasificaciones de etiquetas y sus valores de etiqueta se aplican a todos los componentes secundarios; los nuevos componentes que se agregan posteriormente se asocian automáticamente a la etiqueta. Las clasificaciones de etiquetas para los grupos de productos se aplican al nivel de unidad (más granular).<br><br>Ni el nombre de clasificación ni el valor de clasificación distinguen entre mayúsculas y minúsculas. |
| [!UICONTROL Constraints] | Una restricción asignada a la entidad. Sólo se puede asignar una restricción por entidad.<br><b>>Las entidades secundarias heredan las restricciones, por lo que no es necesario introducir valores para entidades secundarias a menos que desee anular los valores heredados. |
| [!UICONTROL Campaign ID] | ID único que identifica una campaña existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia el nombre de la campaña, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para la campaña. |
| [!UICONTROL Ad Group ID] | ID único que identifica un grupo de anuncios existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia el nombre de la campaña, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para el grupo de anuncios. |
| [!UICONTROL Keyword ID] | Identificador exclusivo que identifica una palabra clave existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia la palabra clave, a menos que la fila incluya a) suficientes columnas de propiedad para identificar la palabra clave o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>ID único que identifica un anuncio existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Para los anuncios adaptables de búsqueda, se requiere el ID del anuncio o el ID de AMO para editar o eliminar los datos del anuncio. Para todos los demás tipos de entidades, el ID de anuncio solo es necesario cuando cambia el estado del anuncio, a menos que la fila incluya a) suficientes columnas de propiedad de anuncio para identificar el anuncio o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Sin embargo, si no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], y las columnas de propiedad de anuncio coinciden con varios anuncios, entonces solo cambiará el estado de uno de ellos.</p><p><b>Nota:</b> Si edita a) columnas de propiedades de anuncios excepto Estado para un anuncio existente o b) cualquier dato para un anuncio de búsqueda adaptable y no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], se creará un anuncio nuevo y no se cambiará el anuncio existente.</p> |
| [!UICONTROL Placement ID] | El ID único que identifica una ubicación del sitio web. Solo es necesario cuando cambia o elimina la ubicación, a menos que la fila incluya a) suficientes columnas de propiedad para identificar la ubicación o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Target ID] | ID único que identifica un destino automático existente. Solo es necesario cuando se cambia o elimina el destino automático, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL Product Group ID] | ID único que identifica un grupo de productos existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia o elimina el grupo de productos, a menos que la fila incluya a) suficientes columnas de propiedades para identificar el grupo de productos o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Sitelink ID] | ID único que identifica un vínculo de sitio existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia o elimina el vínculo a sitios, a menos que la fila incluya a) suficientes columnas de propiedad para identificar el vínculo a sitios o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Sin embargo, si no incluye [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] y las columnas de propiedad coinciden con varios vínculos de sitio, el estado de uno solo de los vínculos de sitio cambiará.</p><p><b>Nota:</b> Si edita las columnas de propiedades de vínculos de sitios excepto Estado para un vínculo de sitios existente y no incluye ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID], se creará un nuevo vínculo de sitios y el vínculo de sitios existente no cambiará. |
| [!UICONTROL RLSA Target ID] | Identificador exclusivo que identifica un objetivo o una exclusión de RLSA de nivel de campaña o de grupo de anuncios existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando se cambia o elimina el destino o la exclusión, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL Device Target ID] | <p>El ID único que identifica un destino o exclusión de dispositivo de nivel de campaña o de grupo de publicidad existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia o elimina el destino, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para el destino.</p> |
| [!UICONTROL AMO ID] | (En hojas de edición masiva generadas) Identificador único generado por Adobe para una entidad sincronizada. Para los anuncios adaptables de búsqueda, el ID de AMO es necesario para editar o eliminar anuncios a menos que incluya el ID de anuncio. Para editar los datos de todos los demás tipos de entidades con un ID de AMO, el ID de AMO es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |
| [!UICONTROL EF Error Message] | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar mensajes de error de la red de publicidad con respecto a los datos de la fila; los mensajes de error se incluyen en [!UICONTROL EF Errors] archivos. Este valor no se publica en la red de anuncios. |
| [!UICONTROL SE Error Message] | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar mensajes de error de la red de publicidad con respecto a los datos de la fila; los mensajes de error se incluyen en [!UICONTROL SE Errors] archivos. Este valor no se publica en la red de anuncios. |
| [!UICONTROL Exemption Request] | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar los nombres y el texto de cualquier política publicitaria de [!DNL Google Ads] que infrinja un anuncio. |
| [!UICONTROL Retail Hash] | (Incluido con fines informativos en hojas de edición masiva generadas mediante Advanced Campaign Management) Código hash alfanumérico (como f9639f40cdf56524b541e5dacf55a991) que indica que el elemento se generó mediante la vista Avanzada (ACM). |

[^1]: [!DNL Excel] convierte los números grandes en notación científica (como 2.12E+09 para 2115585666) cuando abre el archivo. Para ver los dígitos en la notación estándar, seleccione cualquier celda de la columna y haga clic dentro de la barra de fórmulas.

## Campos necesarios para crear, editar o eliminar cada componente de la cuenta {#bulksheet-fields-per-component-google}

Las secciones siguientes incluyen los campos correspondientes a entidades de cuenta específicas.

>[!NOTE]
>
>Cuando un campo no es aplicable a una acción, se ignora cualquier valor introducido en el campo.

### Campos de Campaign

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Campaign Budget] | Necesario para crear una campaña. |
| [!UICONTROL Delivery Method] | Necesario para crear una campaña. |
| [!UICONTROL Channel Type] | Necesario para crear una campaña. |
| [!UICONTROL Networks] | Necesario para crear una campaña. |
| [!UICONTROL DSA Domain Name] | Necesario para crear una campaña con anuncios dinámicos de búsqueda en la red de búsqueda. |
| [!UICONTROL DSA Domain Language] | Necesario para crear una campaña con anuncios dinámicos de búsqueda en la red de búsqueda. |
| [!UICONTROL Campaign Priority] | Necesario para crear una campaña de compras. |
| [!UICONTROL Merchant ID] | Necesario para crear una campaña de compras. |
| [!UICONTROL Sales Country] | Necesario para crear una campaña de compras. |
| [!UICONTROL Product Scope Filter] | (Campañas de compra) Opcional |
| [!UICONTROL Languages] | Opcional |
| [!UICONTROL Device Targets] | Opcional |
| [!UICONTROL Device Targets (Google Adwords)] | Opcional |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Opcional |
| [!UICONTROL Audience Target Method] | n/a |
| [!UICONTROL Landing Page Suffix] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Campaign Status] | Solo es necesario para eliminar una campaña. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Solo es necesario cuando cambia el nombre de la campaña, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para la campaña. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos del grupo de anuncios

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Networks] | n/a |
| [!UICONTROL GDN Custom Bid Level] | Opcional |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Ad Group Type] | Necesario para crear un grupo de anuncios. |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Max Content CPC] | Opcional |
| [!UICONTROL Audience Target Method] | Requerido |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Ad Group Status] | Solo es necesario para eliminar un grupo de anuncios. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Ad Group ID] | Solo es necesario cuando cambia el nombre del grupo de anuncios, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el grupo de anuncios. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de palabra clave

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Keyword] | Requerido |
| [!UICONTROL Match Type] | Se requiere un valor para el tipo de coincidencia o el ID de palabra clave para editar o eliminar una palabra clave con varios tipos de coincidencia. |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Param1] | Opcional |
| [!UICONTROL Param2] | Opcional |
| [!UICONTROL Keyword Status] | Necesario solo para eliminar una palabra clave. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Keyword ID] | Solo es necesario cuando edita o elimina la palabra clave, a menos que la fila incluya a) suficientes columnas de propiedad para identificar la palabra clave o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de colocación

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Max Placement CPC (Google Adwords)] | Opcional |
| [!UICONTROL Max Placement CPM (Google Adwords)] | Opcional |
| [!UICONTROL Placement] | Requerido |
| [!UICONTROL Match Type] | Requerido |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Placement Status] | Solo es necesario para eliminar una ubicación. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Placement ID] | Solo es necesario cuando edita o elimina la ubicación, a menos que la fila incluya a) suficientes columnas de propiedad para identificar la ubicación o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Anuncio de búsqueda dinámica ampliado

Este tipo de anuncio ahora se denomina &quot;anuncio de búsqueda dinámica&quot; en [!DNL Google Ads]. Para obtener más información sobre la creación de anuncios dinámicos de búsqueda, consulte &quot;[Implementar [!DNL Google Ads] anuncios dinámicos de búsqueda](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html?lang=es)&quot;.

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Creative (except RSA)]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Creative Preferred Devices] | Opcional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Necesario para crear un anuncio o editar la descripción. <b>Nota:</b> Para este tipo de anuncio, al cambiar la copia de anuncio se eliminará el anuncio existente y se creará uno nuevo. |
| [!UICONTROL Display URL] | Requerido |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Creative Type] | Necesario para crear o editar el estado de un anuncio de producto. |
| [!UICONTROL Ad Status] | Necesario para eliminar un anuncio. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Solo es necesario cuando cambia el estado del anuncio, a menos que la fila incluya a) suficientes columnas de propiedad de anuncio para identificar el anuncio o b) un &quot;[!UICONTROL AMO ID]&quot;. Sin embargo, si no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], y las columnas de propiedad de anuncio coinciden con varios anuncios, entonces solo cambiará el estado de uno de ellos. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de anuncio de compra/listado de productos

Para obtener más información sobre cómo crear anuncios de compras, consulte &quot;[Implementar [!DNL Google Ads] campañas de compras](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html?lang=es)&quot;.

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Creative (except RSA)]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Promotion Line] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Creative Type] | Necesario para crear o editar el estado de un anuncio de producto. |
| [!UICONTROL Ad Status] | Necesario para eliminar un anuncio. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Solo es necesario cuando cambia el estado del anuncio, a menos que la fila incluya a) suficientes columnas de propiedad de anuncio para identificar el anuncio o b) un &quot;[!UICONTROL AMO ID]&quot;. Sin embargo, si no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], y las columnas de propiedad de anuncio coinciden con varios anuncios, entonces solo cambiará el estado de uno de ellos. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de anuncios de búsqueda interactivos

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Responsive Search Ad]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | Para los anuncios adaptables de búsqueda, se requieren [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] y [!UICONTROL Ad Title 3] para crear un anuncio, y todos los demás campos de título de anuncio son opcionales. Para eliminar el valor existente de un campo no obligatorio, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Opcional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Para los anuncios adaptables de búsqueda, se requieren [!UICONTROL Description Line 1] y [!UICONTROL Description Line 2] para crear un anuncio, y [!UICONTROL Description Line 3] y [!UICONTROL Description Line 4] son opcionales. Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Opcional |
| [!UICONTROL Display Path 1] | Opcional |
| [!UICONTROL Display Path 2] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Necesario para crear un anuncio. |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Creative Type] | Opcional |
| [!UICONTROL Ad Status] | Necesario para eliminar un anuncio. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Es necesario para editar o eliminar anuncios a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar anuncios a menos que incluya el ID de anuncio. |

### Campos de anuncios de texto

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Creative (except RSA)]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

>[!NOTE]
>
>Los anuncios de texto expandidos quedaron obsoletos en junio de 2022. Solo puede eliminar anuncios de texto existentes.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Creative Preferred Devices] | Solo lectura |
| [!UICONTROL Ad Title], Título de anuncio 2-3 | Solo lectura |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Solo lectura |
| [!UICONTROL Display URL] | Solo lectura |
| [!UICONTROL Display Path 1] | Solo lectura |
| [!UICONTROL Display Path 2] | Solo lectura |
| [!UICONTROL Tracking Template] | Solo lectura |
| [!UICONTROL Base URL/Final URL] | Solo lectura |
| [!UICONTROL Custom URL Param] | Solo lectura |
| [!UICONTROL Creative Type] | Opcional |
| [!UICONTROL Ad Status] | Requerido |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Solo es necesario cuando cambia el estado del anuncio, a menos que la fila incluya a&rpar; suficientes columnas de propiedad del anuncio para identificar el anuncio o b&rpar; un &quot;[!UICONTROL AMO ID]&quot;. Sin embargo, si no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], y las columnas de propiedad de anuncio coinciden con varios anuncios, entonces solo cambiará el estado de uno de ellos. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de destino de búsqueda dinámica (destino automático)

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Auto Target Expression] | Solo es necesario cuando la configuración de campaña &quot;[!UICONTROL Use my website contents to target my ads]&quot; no está habilitada. |
| [!UICONTROL Match Type] | Opcional |
| [!UICONTROL Target Status] | Necesario para eliminar un destino |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Target ID] | Solo es necesario cuando se cambia o elimina el destino automático, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos del grupo de productos de compra

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Max CPC] | Necesario para crear un grupo de productos. |
| [!UICONTROL Parent Product Groupings] | Requerido |
| [!UICONTROL Product Grouping] | Requerido |
| [!UICONTROL Partition Type] | Necesario para crear un grupo de productos. |
| [!UICONTROL Match Type] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Requerido |
| [!UICONTROL Product Group Status] | Solo es necesario para eliminar un grupo de productos. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Product Group ID] | Solo es necesario cuando cambia o elimina el grupo de productos, a menos que la fila incluya a) suficientes columnas de propiedad para identificar el grupo de productos o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de vínculo de sitio de nivel de campaña y de nivel de grupo de anuncios

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Necesario para vínculos de sitios de nivel de grupo de anuncios. No aplicable a los vínculos de sitio de nivel de campaña. |
| [!UICONTROL Creative Preferred Devices] | Opcional |
| [!UICONTROL Link Name] | Requerido |
| [!UICONTROL Start Date] | Opcional |
| [!UICONTROL End Date] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Requerido |
| [!UICONTROL Sitelink Status] | Solo es necesario para eliminar un vínculo de sitio. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Sitelink ID] | Solo es necesario cuando cambia o elimina el vínculo de sitio, a menos que la fila incluya a) suficientes columnas de propiedad para identificar el vínculo de sitio o b) un &quot;[!UICONTROL AMO ID]&quot;. Sin embargo, si no incluye [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] y las columnas de propiedad coinciden con varios vínculos de sitio, el estado de uno solo de los vínculos de sitio cambiará.<br><br><b>Nota:</b> Si edita las columnas de propiedad de vínculos de sitios excepto [!UICONTROL Status] para un vínculo de sitio existente y no incluye ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID], se creará un nuevo vínculo de sitio y no se cambiará el vínculo de sitio existente. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Destino de ubicación

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Location] | Requerido |
| [!UICONTROL Location Type] | Opcional |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Location Status] | Necesario solo para eliminar un destino de ubicación. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que incluya [!UICONTROL Campaign ID].<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de destino de dispositivos de nivel de campaña y de nivel de grupo de anuncios

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Device] | Necesario para crear o editar un destino de dispositivo. |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Ad Group Name] | Necesario para destinos de dispositivo en el nivel de grupo de anuncios. No aplicable a los destinos de dispositivo en el nivel de campaña. |
| [!UICONTROL Device Target Status] | Solo es necesario para eliminar un destino de dispositivo. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional; aplicable solo para destinos de dispositivo en el nivel de grupo de anuncios. |
| [!UICONTROL Device Target ID] | Solo es necesario cuando se cambia o elimina el destino, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de destinatario del dispositivo.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de objetivo/exclusión de RLSA a nivel de campaña y de grupo de anuncios

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-google)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Ad Group Name] | Necesario para destinos y exclusiones de nivel de grupo de anuncios. No aplicable a destinos y exclusiones de nivel de campaña. |
| [!UICONTROL Audience] | Necesario para crear un nuevo destino o exclusión. |
| [!UICONTROL Target Type] | Necesario para crear un nuevo destino o exclusión. |
| [!UICONTROL RLSA Target Status] | Solo es necesario para eliminar un destino o una exclusión. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional; aplicable solo para destinos y exclusiones de nivel de grupo de anuncios. |
| [!UICONTROL RLSA Target ID] | Solo es necesario cuando se cambia o elimina el destino, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de destino de RLSA.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

>[!MORELIKETHIS]
>
>* [Apéndice: errores de hojas de edición masiva](../bulksheet-errors.md)
>* [Operaciones que puede realizar en hojas de edición masiva](bulksheet-operations.md)
>* [Formatos de archivo de hojas de edición masiva admitidos](bulksheet-file-formats.md)
>* [Descargar o crear un archivo de hoja de edición masiva](../bulksheet-download.md)
>* [Formatos de rastreo de clics para [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Cargar un archivo de hoja de edición masiva o archivo de error corregido](../bulksheet-upload.md)
