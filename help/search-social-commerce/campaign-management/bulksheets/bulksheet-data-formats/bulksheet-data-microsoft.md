---
title: Se requieren datos de hojas de edición masiva para  [!DNL Microsoft Advertising] cuentas
description: Haga referencia a los campos de encabezado y los campos de datos requeridos en hojas de edición masiva para  [!DNL Microsoft Advertising] cuentas.
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '6928'
ht-degree: 0%

---

# Apéndice: Datos de hoja de edición masiva requeridos para las cuentas de [!DNL Microsoft Advertising]

Para crear y actualizar los datos de la campaña [!DNL Microsoft Advertising] de forma masiva, puede usar los archivos de hoja de edición masiva de Search, Social y Commerce con un formato específico para las cuentas de [!DNL Microsoft Advertising]. Puede: a) [generar archivos de hojas de edición masiva para cuentas existentes](../bulksheet-download.md) en el formato de archivo requerido o b) crearlos manualmente (consulte &quot;[Formatos de archivo de hojas de edición masiva admitidos](bulksheet-file-formats.md)&quot; para obtener información general sobre los formatos de archivo admitidos).

Cada hoja de edición masiva debe incluir los campos de encabezado y los campos de datos correspondientes necesarios para las [operaciones específicas que desea realizar](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (como crear un anuncio). Cuando un campo no es obligatorio, puede omitirlo del encabezado y de las filas de datos. Todas las columnas personalizadas se eliminan al cargar el archivo de hoja de edición masiva.

A continuación se muestra una tabla con todos los campos de datos disponibles y tablas adicionales que indican qué campos son necesarios para agregar, editar o eliminar datos para entidades individuales (como campañas y palabras clave).

## Todos los campos de datos disponibles {#bulksheet-fields-all-microsoft}

En la tabla siguiente se describen todos los campos de datos disponibles.

Para los campos de datos relevantes para las entidades de cuenta, consulte &quot;[Campos necesarios para crear, editar o eliminar cada componente de cuenta](#bulksheet-fields-per-component-microsoft)&quot;.

| Campo | Descripción |
|----|----|
| [!UICONTROL Platform] | (Incluida en las hojas de edición masiva generadas con fines informativos) La plataforma de publicidad. Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Acct Name] | El nombre único que identifica una cuenta de red de publicidad. Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | El nombre único que identifica una campaña para una cuenta. La longitud máxima es de 128 caracteres. |
| [!UICONTROL Campaign Budget] | El presupuesto diario o mensual de la campaña, con o sin símbolos monetarios y puntuación. No puede ser inferior a 0,05. |
| [!UICONTROL Channel Type] | El tipo de canal al que se dirige la campaña: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i> o <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Solo campañas con presupuestos diarios) La rapidez con la que se muestran los anuncios de la campaña cada día:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (predeterminado para nuevas campañas): para difundir las impresiones de publicidad a lo largo del día.</li><li><i>[!UICONTROL Accelerated]:</i> Para mostrar tus anuncios con la mayor frecuencia posible hasta que se alcance tu presupuesto. Como resultado, es posible que los anuncios no aparezcan más tarde ese día.</li></ul> |
| [!UICONTROL Campaign Priority] | (Solo campañas de compra) La prioridad con la que se usa la campaña cuando varias campañas anuncian el mismo producto: <i>[!UICONTROL Low]</i> (el valor predeterminado para las nuevas campañas), <i>[!UICONTROL Medium]</i> o <i>[!UICONTROL High]</i>.<br><br>Cuando el mismo producto se incluye en más de una campaña, la red de anuncios utiliza primero la prioridad de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta. |
| [!UICONTROL Merchant ID] | (Campañas de compra y campañas de audiencia vinculadas únicamente a una fuente de comerciante) El ID de cliente de la cuenta de comerciante cuyos productos se utilizan para la campaña. |
| [!UICONTROL Sales Country] | (Solo campañas de compra; solo lectura para campañas existentes) El país en el que se venden los productos de la campaña. Dado que los productos están asociados a países de destino, esta configuración determina qué productos se anuncian en la campaña. |
| [!UICONTROL Product Scope Filter] | (Campañas que solo utilizan la red de compras) Los productos de la cuenta de comerciante para los que se pueden crear anuncios de productos para la campaña. Puede introducir hasta siete combinaciones de dimensiones de producto y atributos en las que filtrar sus productos, utilizando el formato dimensión=atributo. Separe varios filtros con un delimitador &quot;>>&quot;. Para obtener una lista de las dimensiones de producto disponibles, consulte &quot;[Filtros de productos de campañas de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;.<br><br> Ejemplo: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Para eliminar los valores existentes, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL DSA Domain Name] | (Campañas de tipo a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; o b) &quot;<i>[!UICONTROL Search]</i>&quot; cuando no se ha establecido el elemento [!DNL ExperimentId]) El nombre de dominio del sitio web que se va a segmentar para los anuncios dinámicos de búsqueda. La longitud máxima es de 2048 caracteres. Si el nombre de dominio incluye `www`, está recortado y no se utiliza.<br><br>Para las campañas existentes, no puede editar el dominio, pero debe incluirlo para actualizar otras propiedades. |
| [!UICONTROL DSA Domain Language] | (Campañas de tipo a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; o b) &quot;<i>[!UICONTROL Search]</i>&quot; cuando el elemento [!DNL ExperimentId] no está establecido) El idioma de las páginas del sitio web que se dirigirán a los anuncios dinámicos de búsqueda. Los idiomas de dominio admitidos son [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish] y [!UICONTROL Swedish].<br><br>Para las campañas existentes, no puede editar el idioma, pero debe incluirlo para actualizar otras propiedades. |
| [!UICONTROL Ad Group Name] | El nombre único que identifica un grupo de anuncios. La longitud máxima es de 128 caracteres. Los caracteres en blanco al final no se guardan (por ejemplo, &quot;Grupo de anuncios 1&quot; se guarda como &quot;Grupo de anuncios 1&quot;). |
| [!UICONTROL Ad Group Type] | (Campañas en la red de búsqueda; solo lectura para grupos de anuncios existentes) El tipo de grupo de anuncios: <i>[!UICONTROL Audience]</i> (solo para campañas de audiencia), <i>[!UICONTROL Search Dynamic]</i> (solo para anuncios dinámicos de búsqueda) y <i>[!UICONTROL Search Standard]</i> (solo para anuncios de búsqueda interactivos y anuncios de texto expandido existentes). Algunos tipos de campaña pueden incluir varios tipos de grupos de publicidad. |
| [!UICONTROL Keyword] | (Solo campañas en la red de búsqueda) La cadena de palabra clave. La longitud máxima es de 50 caracteres.<br><br><b>Notas:</b><ul><li>Para excluir una palabra clave en el nivel de grupo de anuncios o de campaña, establezca [!UICONTROL Match Type] en `Negative`. Si la fila incluye el nombre del grupo de anuncios, la palabra clave se excluye para el grupo de anuncios. Si la fila no incluye el nombre del grupo de anuncios, la palabra clave se excluye para toda la campaña.</li><li>Al cambiar una palabra clave [!DNL Microsoft Advertising], se eliminará la palabra clave existente y se creará una nueva con un nuevo identificador de palabra clave. Sin embargo, al cambiar el tipo de coincidencia no se elimina la palabra clave existente.</li></ul> |
| Ubicación | Obsoleto |
| [!UICONTROL Audience] | La lista de remarketing para la audiencia de destino de anuncios de búsqueda (RLSA) de la campaña o grupo de anuncios. |
| [!UICONTROL Target Type] | (Solo destinos de RLSA) El tipo de destino: <i>[!UICONTROL Inclusion]</i> o <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Destinos de búsqueda dinámica para el grupo de anuncios. Para todos los destinos, use &quot;[!UICONTROL All Web Pages]&quot;.<br><br>Para seleccionar hasta tres criterios de búsqueda dinámica, use el formato `<category>=<target>`, donde &lt;category> puede incluir cualquiera de las categorías siguientes. Unir varios destinos para una categoría individual con &quot;`[blank space] and [blank space]`&quot; y unir varias categorías con &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Categoría:</i> Para mostrar anuncios dinámicos de búsqueda para páginas indizadas con una categoría de contenido de Google específica.</li><li><i>URL:</i> para mostrar anuncios dinámicos de búsqueda para páginas indizadas con una dirección URL específica, donde el valor se puede incluir en cualquier lugar dentro de la dirección URL.</li><li><i>Título de página:</i> Para mostrar anuncios dinámicos de búsqueda para páginas indizadas con texto específico en el título de página.</li><li><i>Contenido de la página:</i> Para mostrar anuncios dinámicos de búsqueda para páginas indizadas con contenido específico.</li></ul>Ejemplo: url=shoes.example.com y page title=Footwear<br>Ejemplo: Todas las páginas web |
| [!UICONTROL Location] | Ubicación geográfica en la que se colocan los anuncios de la campaña o el grupo de anuncios; los valores no distinguen entre mayúsculas y minúsculas. Si no introduce ningún valor para la campaña o el grupo de publicidad, se segmentan todas las ubicaciones. Para dirigirse a ubicaciones específicas, escriba la ubicación utilizando los formatos de código de ubicación [!DNL Microsoft Advertising]. Para descargar una lista de ubicaciones, inicie sesión en el portal para desarrolladores de [!DNL Microsoft Advertising] con las credenciales de su cuenta publicitaria de [!DNL Microsoft Advertising]. <b>Nota:</b> Para excluir una ubicación, coloque delante del código de ubicación un signo menos (`-`), como `-United States`. |
| [!UICONTROL Location Type] | El tipo de ubicación, como ciudad, país, área de metro, código postal y estado. Para descargar una lista de ubicaciones, inicie sesión en el portal para desarrolladores de [!DNL Microsoft Advertising] con las credenciales de su cuenta publicitaria de [!DNL Microsoft Advertising]. |
| [!UICONTROL Match Type] | (Solo campañas en la red de búsqueda) Las opciones de coincidencia de palabras clave. Esto puede incluir la opción de coincidencia de palabras clave para un destino de búsqueda dinámica o un grupo de productos. Los valores incluyen: <i>[!UICONTROL Broad]</i> (el valor predeterminado para las nuevas palabras clave), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (establecido automáticamente para las palabras clave cuando el grupo de anuncios se dirige a la red de contenido), <i>[!UICONTROL Negative]</i> (para excluir una palabra clave en la red de contenido), <i>[!UICONTROL Dynamic Ad Target]</i> (el valor predeterminado para los nuevos destinos de búsqueda dinámica), <i>[!UICONTROL Product Group]</i> (el valor predeterminado para los nuevos grupos de productos) o <i>[!UICONTROL Negative Product Group]</i> (para excluir un grupo de productos).  Se requiere un valor para el tipo de coincidencia o el ID de palabra clave para editar o eliminar una palabra clave con varios tipos de coincidencia.<br><br>Para Modificador de coincidencia amplia, elija &quot;Amplia&quot; e inserte un `+` antes de cualquier palabra dentro de la palabra clave que sea necesaria (como &quot;`+red +shoes`&quot; para requerir &quot;rojo&quot; y &quot;zapatos&quot;).<br><br>Al cambiar el tipo de coincidencia para una palabra clave [!DNL Microsoft Advertising], no se elimina la palabra clave existente. |
| [!UICONTROL Max CPC] | (Campañas en la red de búsqueda) El coste por clic máximo (CPC), que es la cantidad más alta que se paga por un clic de anuncio en función de la palabra clave, el grupo de productos o el objetivo de búsqueda dinámica, con o sin símbolos monetarios y puntuación.  Para los registros de palabras clave y grupos de productos existentes en portafolios optimizados, las actualizaciones son efectivas solo para un día y se sobrescriben durante el siguiente ciclo de optimización. <b>Nota:</b> No puedes establecer pujas para palabras clave negativas. |
| [!UICONTROL Max Content CPC] | (Solo lectura para campañas CPC creadas antes de que la red de contenido quedara obsoleta solo en 2017 ). El coste por clic (CPC) de contenido máximo, que es la cantidad más alta que se paga por un clic de anuncio desde un sitio de red de visualización, con o sin símbolos monetarios y puntuación. |
| [!UICONTROL Audience Target Method] | (Grupos de anuncios de audiencias) Si se desea:<ul><li><i>[!UICONTROL Target and Bid]:</i> Para mostrar anuncios solamente a usuarios asociados con audiencias de destino que también cumplan cualquier otro objetivo para el grupo de anuncios.</li><li><i>[!UICONTROL Bid Only]:</i>Para mostrar anuncios incluso a personas que no están asociadas con audiencias de destino siempre y cuando satisfagan otros objetivos de nivel de grupo de anuncios.</li></ul> Sin embargo, puedes aumentar las probabilidades de que se muestren anuncios a audiencias específicas si estableces pujas más altas para esas audiencias. |
| [!UICONTROL Parent Product Groupings] | La jerarquía de cualquier grupo de productos principal.<br><br>Ejemplo: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | El grupo de productos (como &quot;brand=acme&quot; o &quot;All Products&quot;).<br><br><b>Notas:</b><ul><li>Cuando un grupo de productos especificado no existe en la jerarquía de agrupaciones de productos principales, Buscar, Social y Commerce crea las partes de la jerarquía que sean necesarias.</li><li>Search, Social y Commerce crean automáticamente un grupo &quot;[!UICONTROL All Products]&quot; cada vez que crea un grupo de anuncios en una campaña de compras con una oferta predeterminada establecida en la oferta predeterminada del grupo de anuncios. Search, Social y Commerce crean automáticamente un grupo &quot;[!UICONTROL Everything Else]&quot; con la oferta predeterminada de grupo de anuncios en cada nivel de la jerarquía de grupos de productos. Aún puede crear explícitamente estos grupos predeterminados y excluirlos o cambiar sus ofertas.</li><li>Cada grupo de anuncios puede incluir hasta ocho niveles de grupos de productos, incluidos &quot;[!UICONTROL All Products]&quot; y otros siete niveles.</li></ul> |
| [!UICONTROL Partition Type] | El tipo de partición para el grupo de productos: <i>[!UICONTROL subdivision]</i> (cuando tiene grupos de productos secundarios) o <i>[!UICONTROL unit]</i> (cuando no tiene grupos de productos secundarios). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Solo anuncios de texto expandidos, anuncios multimedia, anuncios adaptables y anuncios de búsqueda adaptables) Los titulares de un anuncio. La longitud máxima de cada campo de título de anuncio es de 30 caracteres o 15 caracteres de doble byte, incluido cualquier texto dinámico (como los valores de las palabras clave, las variables de sustitución dinámica `{Param2}` y `{Param3}`, y los personalizadores de anuncios).<br><br> Para anuncios de búsqueda adaptables, inserta un personalizador de anuncios con el siguiente formato, donde &quot;Texto predeterminado&quot; es un valor opcional que se inserta cuando el archivo de fuente no incluye un valor válido: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Para los anuncios de texto expandidos, se requieren el Título de anuncio y el Título de anuncio 2, y [!UICONTROL Ad Title 3] es opcional. [!DNL Microsoft Advertising] dejó de utilizar los anuncios de texto expandidos en agosto de 2022 y ahora solo puede informar sobre ellos y eliminarlos.<br><br>Para los anuncios multimedia, los anuncios adaptables y los anuncios de búsqueda adaptables, se requieren [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] y [!UICONTROL Ad Title 3], y todos los demás campos de título de anuncio son opcionales.<br><br>Para eliminar el valor existente de un campo no obligatorio, use el valor `[delete]` (incluidos los corchetes).<br><br>Para todos los tipos de anuncios, excepto para los anuncios de texto expandido, al cambiar la copia de anuncio se eliminará el anuncio existente y se creará un nuevo anuncio con las mismas propiedades. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Solo anuncios de búsqueda interactivos; opcional) Una posición en la que fijar el título del anuncio correspondiente: `[null]` (sin valor, lo que hace que el título del anuncio sea apto para todas las posiciones), 1, 2 o 3. Por ejemplo, si [!UICONTROL Ad Title Position] tiene un valor de 1, entonces [!UICONTROL Ad Title] solo puede aparecer en la Posición 1. De forma predeterminada, todos los títulos de los anuncios son nulos (no tienen valores). Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes).<br><br><b>Nota:</b> Puede fijar varios títulos de anuncios en la misma posición. La red de anuncios utiliza uno de los títulos de anuncios anclados a la posición. Es posible que los títulos anclados a la posición 3 no se muestren con el anuncio. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Solo anuncios de texto, anuncios dinámicos de búsqueda, anuncios multimedia, anuncios adaptables, anuncios de búsqueda adaptables y vínculos de sitio mejorados de nivel de campaña) El cuerpo de un anuncio o un vínculo de sitio.<br><br>Para los vínculos de sitio, si lo desea, puede usar [!UICONTROL Description Line 1] y [!UICONTROL Description Line 2] para incluir texto adicional que la red de anuncios pueda mostrar debajo del texto del vínculo. Cada campo de descripción puede incluir hasta 35 caracteres de un solo byte o 17 de doble byte.<br><br>Para los anuncios, la longitud máxima de cada campo de descripción es de 90 caracteres o 45 caracteres de doble byte, incluido cualquier texto dinámico (como los valores de palabras clave y personalizadores de anuncios).<br><br>Para los anuncios adaptables de búsqueda, inserte un personalizador de anuncios con el formato siguiente, donde Texto predeterminado es un valor opcional que se debe insertar cuando el archivo de fuente no incluye un valor válido: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Para los anuncios de texto y los anuncios dinámicos de búsqueda, se requiere la Línea de descripción 1 y [!UICONTROL Description Line 2] es opcional.<br><br>Para los anuncios multimedia, los anuncios adaptables y los anuncios de búsqueda adaptables, se requieren [!UICONTROL Description Line 1] y [!UICONTROL Description Line 2], y [!UICONTROL Description Line 3] y [!UICONTROL Description Line 4] son opcionales.<br><br>Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes).<br><br><b>Notas:</b><ul><li>(Anuncios de texto estándar) El título y el texto combinados deben tener al menos tres palabras.</li><li>(Anuncios de texto expandidos) Este campo puede incluir opcionalmente las variables de sustitución dinámica {Param2} y {Param3}. Si es así, la longitud máxima del texto del anuncio es de 300 caracteres de un solo byte o 150 de doble byte. [!DNL Microsoft Advertising] dejó de utilizar los anuncios de texto expandidos en agosto de 2022 y ahora solo puede informar sobre ellos y eliminarlos.</li><li>(Anuncios dinámicos de búsqueda) No se permite el texto de sustitución dinámico.</li><li>Para todos los tipos de anuncio, excepto los anuncios de texto expandidos, al cambiar la copia de anuncio se elimina el anuncio existente y se crea uno nuevo.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Solo anuncios de búsqueda interactivos; opcional) Una posición en la que fijar la descripción correspondiente: `[null]` (sin valor, lo que hace que la descripción sea apta para todas las posiciones), 1, 2 o 3. Por ejemplo, si [!UICONTROL Description 1 Position] tiene un valor de 1, la Descripción 1 solo puede aparecer en la Posición 1. De forma predeterminada, no se anclan descripciones a una posición.<br><br>Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes).<br><br><b>Nota:</b> Puede fijar varias descripciones en la misma posición. La red publicitaria utiliza una de las descripciones ancladas a la posición. Las descripciones ancladas a la posición 2 pueden no mostrarse con el anuncio. |
| [!UICONTROL Business Name] | (Solo anuncios multimedia) El nombre comercial, con un máximo de 25 caracteres. |
| [!UICONTROL Promotion Line] | (Solo anuncios de listado de productos) Una línea de promoción única que se incluirá con el listado de productos en los resultados de búsqueda (como &quot;Envío gratuito ahora&quot;). La longitud máxima es de 45 caracteres.<br><br>La línea de promoción puede aparecer en diferentes ubicaciones relacionadas con el anuncio (por ejemplo, debajo del anuncio), dependiendo de dónde aparezca el anuncio en la página. |
| [!UICONTROL Display URL] | Dirección URL que se incluye en el anuncio.<br><br>Para los anuncios dinámicos de búsqueda expandidos, la red de anuncios genera este valor dinámicamente desde el dominio del sitio web y no es necesario que escriba ningún valor.<br><br>Para anuncios de texto expandidos y anuncios de búsqueda adaptables, no es necesario que escriba un valor. La dirección URL mostrada se extrae automáticamente del dominio en la dirección URL final. Opcionalmente, puede personalizar la dirección URL mediante los campos Ruta 1 y Ruta 2.<br><br><b>Notas:</b><ul><li>(Cuentas con direcciones URL finales) Los nombres de dominio de la dirección URL mostrada y de la dirección URL final deben coincidir.</li><li>[!DNL Microsoft Advertising] dejó de utilizar los anuncios de texto expandidos en agosto de 2022 y ahora solo puede informar sobre ellos y eliminarlos.</li></ul> |
| [!UICONTROL Display Path 1] | (Solo anuncios de texto expandidos, anuncios dinámicos de búsqueda y anuncios de búsqueda interactivos) Texto que se agrega a la dirección URL de visualización que se extrae automáticamente de la dirección URL final. Cada ruta va precedida en la dirección URL por una barra diagonal (/). Una ruta de acceso no puede contener caracteres de barra diagonal (/) o de línea nueva (\n). La longitud máxima de cada ruta es de 15 caracteres o 7 caracteres de doble byte.<br><br>Para insertar un personalizador de anuncios, use los siguientes formatos, donde &quot;Texto predeterminado&quot; es un valor opcional que se debe insertar cuando el archivo de fuente no incluye un valor válido: `{CUSTOMIZER.Attribute name:Default text}`, como `{CUSTOMIZER.Discount:10%}`<br><br>Por ejemplo, si [!UICONTROL Display Path 1] es &quot;ofertas&quot;, la dirección URL para mostrar sería &lt;URL para mostrar>/ofertas, como www.example.com/deals.<br><br>[!DNL Microsoft Advertising] dejó de utilizar los anuncios de texto expandidos en agosto de 2022 y ahora solo puede informar sobre ellos y eliminarlos. |
| [!UICONTROL Display Path 1] | (Solo anuncios de texto expandidos, anuncios dinámicos de búsqueda y anuncios de búsqueda adaptables) Una ruta de visualización adicional; vea la entrada de [!UICONTROL Display Path 1].<br><br>Ejemplo: si [!UICONTROL Display Path 1] es &quot;acuerdos&quot; y [!UICONTROL Display Path 2] es &quot;local&quot;, la URL para mostrar sería &lt;<i>URL para mostrar</i>>/acuerdos/local, como www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Solo vínculos de sitio mejorados) La primera fecha en la que se pueden realizar ofertas para el vínculo de sitio, en el huso horario del anunciante y en uno de los siguientes formatos: dd/mm/aaaa, dd/mm/aa, dd/mm/aaaa o dd/mm-aa. El valor predeterminado para los nuevos vínculos de sitio mejorados es el día actual. <b>Nota:</b> Los nuevos vínculos de sitio mejorados solo se pueden crear en campañas con vínculos de sitio mejorados existentes o sin vínculos de sitio. |
| [!UICONTROL End Date] | La última fecha en la que el vínculo al sitio puede aparecer con anuncios, en el huso horario del anunciante y en uno de los siguientes formatos: dd/mm/aaaa, dd/mm/aa, dd/mm/aaaa o dd/mm/aa. Para un nuevo vínculo de sitio, el valor predeterminado es `[blank]` (es decir, sin fecha de finalización). |
| [!UICONTROL Call To Action] | Llamada a acción para incluir en el anuncio. Consulte la referencia de la API [para obtener una lista de valores posibles](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), pero especifique llamadas de varias palabras como palabras múltiples (como &quot;Apostar ahora&quot; en lugar de &quot;Apostar ahora&quot;) en hojas de edición masiva. |
| [!UICONTROL Call To Action Language] | Idioma para las opciones de llamada a la acción. Consulte la [referencia de API para obtener una lista de idiomas posibles](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | La dirección URL de la página de aterrizaje a la que se dirigen los usuarios del motor de búsqueda cuando hacen clic en el anuncio, incluidos los parámetros de adición configurados para la campaña o la cuenta. Las direcciones URL base/final en el nivel de palabra clave anulan las del nivel de anuncio y posteriores.<br><br>Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Destination URL] | (Incluido en hojas de edición masiva generadas con fines informativos; no publicado en el motor de búsqueda) Para cuentas con direcciones URL de destino, esta es la dirección URL que vincula un anuncio a una dirección URL o página de aterrizaje base en el sitio web del anunciante (a veces a través de otro sitio que rastrea el clic y luego redirige al usuario a la página de aterrizaje). Incluye cualquier parámetro de adición configurado para la campaña o cuenta de Search, Social y Commerce. Si ha generado direcciones URL de seguimiento, esto se basa en los parámetros de seguimiento de la configuración de la cuenta y la configuración de la campaña. Si ha anexado parámetros específicos del motor de búsqueda, pueden reemplazarse por los parámetros equivalentes para Buscar, Social y Commerce.<br><br>Para cuentas con direcciones URL finales, esta columna muestra el mismo valor que la columna Dirección URL base/Dirección URL final. |
| [!UICONTROL Custom URL Param] | Datos para sustituir la variable dinámica `{custom_code}` cuando la variable se incluye en los parámetros de seguimiento de la configuración de la cuenta de búsqueda o de la campaña. Para insertar el valor personalizado en la dirección URL de seguimiento, debe cargar el archivo de hoja de edición masiva mediante la opción Generar direcciones URL de seguimiento. |
| [!UICONTROL Creative Type] | Formato del anuncio: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (anuncios de compra), o <i>[!UICONTROL Responsive Search Ad]</i>, o <i>[!UICONTROL Text ad]</i>. El valor predeterminado para los anuncios nuevos es <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | La primera fecha en la que se pueden realizar ofertas para el grupo de anuncios, en el huso horario del anunciante y en uno de los siguientes formatos: dd/mm/aaaa, dd/mm/aa, dd/mm-aaaa o dd/mm-aa. Para un grupo de anuncios nuevo, el valor predeterminado es la fecha actual. |
| [!UICONTROL Ad Group End Date] | La última fecha en la que se pueden realizar ofertas para el grupo de anuncios, en el huso horario del anunciante y en uno de los siguientes formatos: dd/mm/aaaa, dd/mm/aa, dd/mm-aaaa o dd/mm-aa. Para un grupo de anuncios nuevo, el valor predeterminado es [en blanco] (es decir, sin fecha de finalización). |
| [!UICONTROL Tracking Template] | (Opcional) La plantilla de seguimiento, que especifica todas las redirecciones de dominios fuera de aterrizaje y los parámetros de seguimiento e incrusta la dirección URL final en un parámetro. La plantilla de seguimiento en el nivel más granular (con la palabra clave como más granular) anula los valores en todos los niveles superiores.<br><br>Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce anexa automáticamente el código de redireccionamiento y seguimiento al guardar el registro.<br><br>Para redirecciones y seguimiento de terceros, escriba un valor.<br><br>Para obtener una lista de parámetros que indiquen las direcciones URL finales en las plantillas de seguimiento, consulte la documentación de [!DNL Microsoft Advertising].<br><br> Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Landing Page Suffix] | Cualquier parámetro que se adjunte al final de las direcciones URL finales para rastrear la información. Ejemplo: `param2=value1&param3=value2`<br><br>Consulte &quot;[Formatos de seguimiento de clics para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)&quot;.<br><br>Los sufijos finales de URL en los niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, use el editor [!DNL Microsoft Advertising]. |
| Buscar estado de red | Si se colocan anuncios para el grupo de anuncios en varios elementos de la red de búsqueda:<ul><li><i>Todos:</i> Para colocar anuncios en todas las redes de búsqueda de Bing y en los socios de búsqueda sindicados.</li><li><i>OwnedAndOperatedOnly:</i>Para colocar anuncios solamente en Bing y Yahoo! sitios web.</li><li><i>SyndicatedSearchOnly:</i> Para colocar anuncios solamente en Bing y Yahoo! socios de búsqueda sindicados.</li><li><i>Desactivado:</i> Para colocar anuncios solamente en la red de contenido (no en la red de búsqueda).</li></ul> Para los nuevos grupos de anuncios, el valor predeterminado es Activado. |
| [!UICONTROL Content Network Status] | Obsoleto |
| [!UICONTROL Languages] | El idioma de destino de los anuncios del grupo de anuncios: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish] o [!UICONTROL Swedish]. El valor predeterminado para las nuevas campañas es [!UICONTROL English].<br><br>Esta configuración determina los países y regiones en los que se puede mostrar el anuncio. Asegúrese de elegir un idioma compatible con los objetivos de ubicación de la campaña. |
| [!UICONTROL Budget Type] | Si el presupuesto es <i>[!UICONTROL Daily]</i> (predeterminado) o <i>[!UICONTROL Monthly]</i>.<br><br>Nota: si asigna la campaña a un portafolio optimizado, este valor se establece automáticamente en [!UICONTROL Daily]. |
| [!UICONTROL Device] | Un tipo de dispositivo para el cual se realizan ajustes de oferta en el nivel de campaña o de grupo de anuncios: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> o <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | El ajuste de oferta para un tipo de destino especificado. Por ejemplo, si la oferta a nivel de palabra clave es 1 USD y el ajuste de oferta para smartphones es del 50 %, la oferta para smartphones es de 1,50 USD. De forma predeterminada, todos los destinos se ofertan en el nivel de palabra clave. Los porcentajes válidos pueden incluir:<ul><li>Smartphones y tablets: -100 (para no pujar por el tipo de dispositivo) y de -90 a 900</li><li>Escritorio: de 0 a 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | Tipos de dispositivos en los que prefiere mostrar el anuncio o el vínculo a sitios: <i>[!UICONTROL All]</i> (predeterminado) o <i>[!UICONTROL Mobile]</i>. Cuando se especifica Mobile, la red intenta mostrar el anuncio o el vínculo a sitios a usuarios de dispositivos móviles en lugar de a usuarios de equipos de escritorio o tabletas. De lo contrario, la red muestra el anuncio o el vínculo de sitio en cualquier tipo de dispositivo. <b>Nota:</b> La red no garantiza que mostrará el anuncio en el tipo de dispositivo preferido. |
| [!UICONTROL Param2] | Cadena que se utilizará como valor de sustitución si la dirección URL base de la palabra clave o el título, la descripción o la dirección URL base del anuncio contiene la cadena de sustitución dinámica `{Param2}`. La longitud máxima es de 70 caracteres, pero tenga en cuenta la longitud máxima de los elementos de publicidad en los que la utiliza (por ejemplo, el Título 1 y el Título 2 combinados pueden tener un máximo de 76 caracteres). Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Param3] | Cadena que se utilizará como valor de sustitución si la dirección URL base de la palabra clave o el título, la descripción o la dirección URL base del anuncio contiene la cadena de sustitución dinámica `{Param3}`. La longitud máxima es de 70 caracteres, pero tenga en cuenta la longitud máxima de los elementos de publicidad en los que la utiliza (por ejemplo, el Título 1 y el Título 2 combinados pueden tener un máximo de 76 caracteres). Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Link Name] | El texto del vínculo de sitio. Debe ser único dentro de la campaña. Si especifica Descripción1 y Descripción2, el texto del vínculo a sitios puede incluir hasta 25 caracteres de byte simple o 12 de byte doble; de lo contrario, el texto del vínculo a sitios puede incluir hasta 35 caracteres de byte simple o 17 de byte doble.<br><br>[!DNL Microsoft Advertising] puede mostrar dos, cuatro o seis vínculos de sitio mejorados con descripciones, o cuatro o seis vínculos de sitio en una sola fila sin descripciones, con un anuncio.<br><br>Solo puede crear nuevos vínculos de sitio mejorados en campañas con vínculos de sitio mejorados existentes o sin vínculos de sitio. |
| [!UICONTROL Campaign Status] | El estado de visualización de la campaña: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo campañas existentes). El valor predeterminado para las nuevas campañas es [!UICONTROL Active]. Para eliminar una campaña activa o pausada, ingrese el valor `Deleted`. |
| [!UICONTROL Ad Group Status] | El estado de visualización del grupo de anuncios: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo grupos de anuncios existentes). El valor predeterminado para los nuevos grupos de anuncios es [!UICONTROL Active]. Para eliminar un grupo de anuncios activo o en pausa, escriba el valor `Deleted`. |
| [!UICONTROL Keyword Status] | Estado de visualización de la palabra clave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo palabras clave existentes). El valor predeterminado para las nuevas palabras clave es [!UICONTROL Active]. Para eliminar una palabra clave activa o pausada, escriba el valor `Deleted`. <b>Nota:</b> Si crea direcciones URL de seguimiento para una palabra clave con varios tipos de coincidencia, el estado de la palabra clave para cada tipo de coincidencia debe ser el mismo. |
| [!UICONTROL Placement Status] | Obsoleto |
| [!UICONTROL Ad Status] | El estado de visualización del anuncio: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (solo anuncios existentes), <i>[!UICONTROL Disapproved]</i> (no editable) o <i>[!UICONTROL Paused]</i>. El valor predeterminado para los anuncios nuevos es [!UICONTROL Active]. Para eliminar un anuncio activo o en pausa, escriba el valor `Deleted`. |
| [!UICONTROL Target Status] | Estado de un destino de búsqueda dinámica: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo destinos existentes). El valor predeterminado para los nuevos destinos es [!UICONTROL Active]. Para eliminar un destino activo o pausado, escriba el valor `Deleted`. |
| [!UICONTROL Sitelink Status] | El estado de visualización del vínculo de sitio: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo vínculos de sitio existentes). El valor predeterminado para los nuevos vínculos de sitio es [!UICONTROL Active]. Para eliminar un vínculo de sitio activo, escriba el valor `Deleted`. |
| [!UICONTROL Location Status] | Estado del destino de ubicación: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo ubicaciones existentes). El valor predeterminado para las nuevas ubicaciones es [!UICONTROL Active]. Para eliminar una ubicación activa, escriba el valor `Deleted`. |
| [!UICONTROL Product Group Status] | El estado de visualización del grupo de productos: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo grupos de productos existentes). El valor predeterminado para los nuevos grupos de productos es [!UICONTROL Active]. Para eliminar un grupo de productos activo, escriba el valor `Deleted`. |
| [!UICONTROL Device Target Status] | Estado del destino de dispositivo de nivel de campaña o de grupo de anuncios: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i>. Para nuevas campañas y grupos de anuncios, el valor predeterminado es [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | El estado del destino de RLSA de nivel de campaña o de grupo de anuncios o la exclusión (solo Google Ads): <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo destinos existentes). El valor predeterminado para los nuevos destinos o exclusiones es [!UICONTROL Active]. Para eliminar un destino o una exclusión activos, escriba el valor `Deleted`. |
| \[Clasificación de etiquetas específica del anunciante\] | (Nombrado para una clasificación de etiquetas específica del anunciante, como &quot;Color&quot; para una clasificación de etiquetas denominada Color) Un valor para la clasificación especificada que está asociada a la entidad. Solo se puede incluir un valor por clasificación por entidad (como &quot;rojo&quot; para la clasificación de etiquetas &quot;Color&quot; para la Campaña A). La longitud máxima es de 100 caracteres y el valor puede incluir caracteres ASCII y no ASCII.<br><br>Las clasificaciones de etiquetas y sus valores de etiqueta se aplican a todos los componentes secundarios; los nuevos componentes que se agregan posteriormente se asocian automáticamente a la etiqueta. Las clasificaciones de etiquetas para los grupos de productos se aplican al nivel de unidad (más granular).<br><br>Ni el nombre de clasificación ni el valor de clasificación distinguen entre mayúsculas y minúsculas. |
| [!UICONTROL Constraints] | Una restricción asignada a la entidad. Sólo se puede asignar una restricción por entidad.<br><b>>Las entidades secundarias heredan las restricciones, por lo que no es necesario introducir valores para entidades secundarias a menos que desee anular los valores heredados. |
| [!UICONTROL Campaign ID] | ID único que identifica una campaña existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia el nombre de la campaña, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para la campaña. |
| [!UICONTROL Ad Group ID] | ID único que identifica un grupo de anuncios existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia el nombre de la campaña, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para el grupo de anuncios. |
| [!UICONTROL Placement ID] | Obsoleto |
| [!UICONTROL Keyword ID] | Identificador exclusivo que identifica una palabra clave existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia la palabra clave, a menos que la fila incluya a) suficientes columnas de propiedad para identificar la palabra clave o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>ID único que identifica un anuncio existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Para los anuncios adaptables de búsqueda, se requiere el ID del anuncio o el ID de AMO para editar o eliminar los datos del anuncio. Para todos los demás tipos de entidad, el ID de AMO solo es necesario cuando cambia el estado del anuncio, a menos que la fila incluya a) suficientes columnas de propiedad del anuncio para identificar el anuncio o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Sin embargo, si no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], y las columnas de propiedad de anuncio coinciden con varios anuncios, entonces el estado de uno solo de los anuncios cambia.</p><p><b>Nota:</b> Si edita a) columnas de propiedades de anuncios excepto Estado para un anuncio existente o b) cualquier dato para un anuncio de búsqueda adaptable y no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], se creará un anuncio nuevo y no se cambiará el anuncio existente. </p> |
| [!UICONTROL Sitelink ID] | ID único que identifica un vínculo de sitio existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia o elimina el vínculo a sitios, a menos que la fila incluya a) suficientes columnas de propiedad para identificar el vínculo a sitios o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Sin embargo, si no incluye [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] y las columnas de propiedad coinciden con varios vínculos de sitio, el estado de uno solo de los vínculos de sitio cambiará.</p><p><b>Nota:</b> Si edita las columnas de propiedades de vínculos de sitios excepto Estado para un vínculo de sitios existente y no incluye ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID], se creará un nuevo vínculo de sitios y el vínculo de sitios existente no cambiará. |
| [!UICONTROL Product Group ID] | ID único que identifica un grupo de productos existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia o elimina el grupo de productos, a menos que la fila incluya a) suficientes columnas de propiedades para identificar el grupo de productos o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| ID de ubicación | Identificador [!DNL Microsoft Advertising] único del destino de ubicación. Para descargar una lista de ubicaciones, inicie sesión en el portal para desarrolladores de [!DNL Microsoft Advertising] con las credenciales de su cuenta publicitaria de [!DNL Microsoft Advertising]. Solo es necesario cuando se cambia o elimina el destino de ubicación, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL Target ID] | ID único que identifica un destino automático existente. Solo es necesario cuando se cambia o elimina el destino automático, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL RLSA Target ID] | Identificador exclusivo que identifica un destinatario de RLSA de nivel de campaña o de grupo de anuncios existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando se cambia o elimina el destino o la exclusión, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL AMO ID] | (En hojas de edición masiva generadas) Identificador único generado por el Adobe para una entidad sincronizada. Para los anuncios adaptables de búsqueda, el ID de AMO es necesario para editar o eliminar anuncios a menos que incluya el ID de anuncio. Para editar los datos de todos los demás tipos de entidades con un ID de AMO, el ID de AMO es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |
| [!UICONTROL EF Error Message] | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar mensajes de error de la red de publicidad con respecto a los datos de la fila; los mensajes de error se incluyen en [!UICONTROL EF Errors] archivos. Este valor no se publica en la red de anuncios. |
| [!UICONTROL SE Error Message] | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar mensajes de error de la red de publicidad con respecto a los datos de la fila; los mensajes de error se incluyen en [!UICONTROL SE Errors] archivos. Este valor no se publica en la red de anuncios. |
| [!UICONTROL Exemption Request] | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar los nombres y el texto de cualquier política publicitaria de Google que infrinja un anuncio. |
| [!UICONTROL Retail Hash] | (Se incluye con fines informativos en las hojas de edición masiva generadas mediante Advanced Campaign Management) Código hash alfanumérico (como f9639f40cdf56524b541e5dacf55a991) que indica que el elemento se generó mediante la vista Advanced (ACM). |

[^1]: [!DNL Excel] convierte los números grandes en notación científica (como 2.12E+09 para 2115585666) cuando abre el archivo. Para ver los dígitos en la notación estándar, seleccione cualquier celda de la columna y haga clic dentro de la barra de fórmulas.

## Campos necesarios para crear, editar o eliminar cada componente de la cuenta {#bulksheet-fields-per-component-microsoft}

Las secciones siguientes incluyen los campos correspondientes a entidades de cuenta específicas.

>[!NOTE]
>
>Cuando un campo no es aplicable a una acción, se ignora cualquier valor introducido en el campo.

### Campos de Campaign

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido | El nombre único que identifica una campaña para una cuenta. |
| [!UICONTROL Campaign Budget] | Necesario para crear una campaña. | Un límite diario de gasto para la campaña, con o sin símbolos monetarios y puntuación. Este valor anula pero no puede superar el presupuesto de la cuenta. |
| [!UICONTROL Channel Type] | Necesario para crear una campaña. |
| [!UICONTROL Delivery Method] | Opcional |
| [!UICONTROL Campaign Priority] | Necesario para crear una campaña de compras. |
| [!UICONTROL Merchant ID] | Necesario para crear una campaña de compras. |
| [!UICONTROL Sales Country] | Necesario para crear una campaña de compras. |
| [!UICONTROL Product Scope Filter] | (Campañas de compra) Opcional |
| [!UICONTROL DSA Domain Name] | Necesario para crear una campaña de tipo a) &quot;[!UICONTROL DynamicSearchAds]&quot; o b) &quot;[!UICONTROL Search]&quot; cuando el elemento [!DNL ExperimentId] no está establecido) |
| [!UICONTROL DSA Domain Language] | Necesario para crear una campaña de tipo a) &quot;[!UICONTROL DynamicSearchAds]&quot; o b) &quot;[!UICONTROL Search]&quot; cuando el elemento [!DNL ExperimentId] no está establecido) |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Landing Page Suffix] | <p>Opcional |
| [!UICONTROL Budget Type] | Necesario para crear una campaña. |
| [!UICONTROL Device] | Opcional |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Campaign Status] | Solo es necesario para eliminar una campaña. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Solo es necesario cuando cambia el nombre de la campaña, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot; para la campaña. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos del grupo de anuncios

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Ad Group Type] | Necesario para crear un grupo de anuncios. |
| [!UICONTROL Audience Target Method] | Solo es necesario para crear grupos de anuncios de audiencia. |
| [!UICONTROL Ad Group Start Date] | Opcional |
| [!UICONTROL Ad Group End Date] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Search Network Status] | (Solo campañas en la red de búsqueda) Opcional |
| [!UICONTROL Languages] | Opcional |
| [!UICONTROL Device] | Opcional |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Ad Group Status] | Solo es necesario para eliminar un grupo de anuncios. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Ad Group ID] | Solo es necesario cuando cambia el nombre del grupo de anuncios, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el grupo de anuncios. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de palabra clave

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Keyword] | Requerido |
| [!UICONTROL Match Type] | Se requiere un valor para el tipo de coincidencia o el ID de palabra clave para editar o eliminar una palabra clave con varios tipos de coincidencia. |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Param1] | Opcional |
| [!UICONTROL Param2] | Opcional |
| [!UICONTROL Keyword Status] | Necesario solo para eliminar una palabra clave. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Keyword ID] | Solo es necesario cuando edita o elimina la palabra clave, a menos que la fila incluya a) suficientes columnas de propiedad para identificar la palabra clave o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de anuncios de búsqueda dinámica

>[!NOTE]
>
>La compatibilidad con la creación de no está disponible.

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Creative (except RSA)]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Necesario para editar la descripción. <b>Nota:</b> Para este tipo de anuncio, al cambiar la copia de anuncio se eliminará el anuncio existente y se creará uno nuevo. |
| [!UICONTROL Display Path 1] | Requerido para editar el campo. |
| [!UICONTROL Display Path 2] | Requerido para editar el campo. |
| [!UICONTROL Creative Type] | Necesario para crear o editar el estado de un anuncio de producto. |
| [!UICONTROL Creative Preferred Devices] | Opcional |
| [!UICONTROL Ad Status] | Necesario para eliminar un anuncio. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Solo es necesario cuando cambia el estado del anuncio, a menos que la fila incluya a) suficientes columnas de propiedad de anuncio para identificar el anuncio o b) un &quot;[!UICONTROL AMO ID]&quot;. Sin embargo, si no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], y las columnas de propiedad de anuncio coinciden con varios anuncios, entonces solo cambiará el estado de uno de ellos. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de publicidad de productos (compras)

Para obtener más información sobre cómo crear anuncios de compras, consulte &quot;[Implementar [!DNL Microsoft Advertising] campañas de compras](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html?lang=es)&quot;.

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Creative (except RSA)]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Promotion Line] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Creative Type] | Necesario para crear o editar el estado de un anuncio de producto. |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Ad Status] | Necesario para eliminar un anuncio. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Solo es necesario cuando cambia el estado del anuncio, a menos que la fila incluya a) suficientes columnas de propiedad de anuncio para identificar el anuncio o b) un &quot;[!UICONTROL AMO ID]&quot;. Sin embargo, si no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], y las columnas de propiedad de anuncio coinciden con varios anuncios, entonces solo cambiará el estado de uno de ellos. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de anuncios interactivos (multimedia)

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Creative (except RSA)]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Para los anuncios adaptables, se requieren [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] y [!UICONTROL Ad Title 3] para crear anuncios, y todos los demás campos de título de anuncio son opcionales. Para eliminar el valor existente de un campo no obligatorio, use el valor `[delete]` (incluidos los corchetes). <b>Nota:</b> Para este tipo de anuncio, al cambiar la copia de anuncio se eliminará el anuncio existente y se creará uno nuevo. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Se requieren [!UICONTROL Description Line 1] y [!UICONTROL Description Line 2] para crear anuncios, y [!UICONTROL Description Line 3] y [!UICONTROL Description Line 4] son opcionales. <b>Nota:</b> Para este tipo de anuncio, al cambiar la copia de anuncio se eliminará el anuncio existente y se creará uno nuevo. |
| [!UICONTROL Business Name] | Necesario para crear o eliminar un anuncio. |
| [!UICONTROL Call To Action] | Necesario para crear un anuncio. |
| [!UICONTROL Call To Action Language] | Necesario para crear un anuncio. |
| [!UICONTROL Base URL/Final URL] | Necesario para crear un anuncio. |
| [!UICONTROL Creative Type] | Opcional. |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Ad Status] | Necesario para eliminar un anuncio. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Solo es necesario cuando cambia el estado del anuncio, a menos que la fila incluya a) suficientes columnas de propiedad de anuncio para identificar el anuncio o b) un &quot;[!UICONTROL AMO ID]&quot;. Sin embargo, si no incluye ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], y las columnas de propiedad de anuncio coinciden con varios anuncios, entonces solo cambiará el estado de uno de ellos. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de anuncios de búsqueda interactivos

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Responsive Search Ad]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Para los anuncios adaptables de búsqueda, se requieren [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] y [!UICONTROL Ad Title 3] para crear un anuncio, y todos los demás campos de título de anuncio son opcionales. Para eliminar el valor existente de un campo no obligatorio, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Opcional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Para los anuncios adaptables de búsqueda, se requieren [!UICONTROL Description Line 1] y [!UICONTROL Description Line 2] para crear un anuncio, y [!UICONTROL Description Line 3] y [!UICONTROL Description Line 4] son opcionales. Para eliminar el valor existente, use el valor `[delete]` (incluidos los corchetes). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Opcional |
| [!UICONTROL Display Path 1] | Opcional |
| [!UICONTROL Display Path 2] | Opcional |
| [!UICONTROL Base URL/Final URL] | Necesario para crear un anuncio. |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Creative Type] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Ad Status] | Necesario para eliminar un anuncio. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Es necesario para editar o eliminar anuncios a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar anuncios a menos que incluya el ID de anuncio. |

### Campos de anuncios de texto

Para este tipo de anuncio, utilice la fila &quot;[!UICONTROL Creative (except RSA)]&quot; en el cuadro de diálogo [!UICONTROL Download Bulksheet].

>[!NOTE]
>
>Los anuncios de texto expandidos estaban en desuso. Solo puede eliminar anuncios de texto existentes.

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Solo lectura |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] de solo lectura |
| [!UICONTROL Display URL] | Solo lectura |
| [!UICONTROL Display Path 1] | Solo lectura |
| [!UICONTROL Display Path 2] | Solo lectura |
| [!UICONTROL Base URL/Final URL] | Solo lectura |
| [!UICONTROL Custom URL Param] | Solo lectura |
| [!UICONTROL Creative Type] | Opcional |
| [!UICONTROL Tracking Template] | Solo lectura |
| [!UICONTROL Creative Preferred Devices] | Solo lectura |
| [!UICONTROL Ad Status] | Requerido |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Solo es necesario cuando se cambia el estado del anuncio, a menos que la fila incluya &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que incluya el ID de anuncio.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de destino de búsqueda dinámica (destino automático)

>[!NOTE]
>
>La compatibilidad con la creación de no está disponible.

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Auto Target Expression] | Requerido. |
| [!UICONTROL Match Type] | Opcional |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Target Status] | Necesario para eliminar un destino |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Target ID] | Solo es necesario cuando se cambia o elimina el destino automático, a menos que la fila incluya un &quot;[!UICONTROL AMO ID]&quot; para el destino. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos del grupo de productos de compra

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Requerido |
| [!UICONTROL Match Type] | Necesario para crear un grupo de productos. |
| [!UICONTROL Max CPC] | Necesario para crear un grupo de productos. |
| [!UICONTROL Parent Product Groupings] | Requerido |
| [!UICONTROL Product Grouping] | Requerido |
| [!UICONTROL Partition Type] | Necesario para crear un grupo de productos. |
| [!UICONTROL Base URL/Final URL] | Requerido |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Product Group Status] | Solo es necesario para eliminar un grupo de productos. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Product Group ID] | Solo es necesario cuando cambia o elimina el grupo de productos, a menos que la fila incluya a) suficientes columnas de propiedad para identificar el grupo de productos o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de vínculo de sitio de nivel de campaña

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| Línea de descripción 1 | Opcional |
| [!UICONTROL Description Line 2] | Opcional |
| [!UICONTROL Start Date] | Opcional |
| [!UICONTROL End Date] | Opcional |
| [!UICONTROL Base URL/Final URL] | Requerido |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Creative Preferred Devices] | Opcional |
| [!UICONTROL Link Name] | Requerido |
| [!UICONTROL Sitelink Status] | Solo es necesario para eliminar un vínculo de sitio. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Sitelink ID] | Solo es necesario cuando cambia o elimina el vínculo de sitio, a menos que la fila incluya a) suficientes columnas de propiedad para identificar el vínculo de sitio o b) un &quot;[!UICONTROL AMO ID]&quot;. Sin embargo, si no incluye [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] y las columnas de propiedad coinciden con varios vínculos de sitio, el estado de uno solo de los vínculos de sitio cambiará.<br><br><b>Nota:</b> Si edita las columnas de propiedades de vínculos de sitios excepto Estado para un vínculo de sitios existente y no incluye ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID], se creará un nuevo vínculo de sitios y el vínculo de sitios existente no cambiará. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de destino de ubicación

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Location] | Requerido |
| [!UICONTROL Location Type] | Necesario para crear un destino |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Location Status] | Necesario solo para eliminar un destino de ubicación. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de campaña.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de destino de dispositivos de nivel de campaña y de nivel de grupo de anuncios

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Device] | Necesario para eliminar un destino de dispositivo. |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Ad Group Name] | Necesario para destinos de dispositivo en el nivel de grupo de anuncios. No aplicable a los destinos de dispositivo en el nivel de campaña. |
| [!UICONTROL Device Target Status] | Solo es necesario para eliminar un destino de dispositivo. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional; aplicable solo para destinos de dispositivo en el nivel de grupo de anuncios. |
| [!UICONTROL AMO ID] | Es necesario para editar o eliminar los datos a menos que se incluya el ID de destinatario del dispositivo.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |

### Campos de destino de RLSA de nivel de campaña y de nivel de grupo de anuncios

Para obtener una descripción de cada campo de datos, consulte &quot;[Todos los campos de datos disponibles](#bulksheet-fields-all-microsoft)&quot;.

| Campo | ¿Requerido? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatorio a menos que cada fila incluya &quot;[!UICONTROL AMO ID]&quot; para la entidad. |
| [!UICONTROL Campaign Name] | Requerido |
| [!UICONTROL Ad Group Name] | Necesario para destinos de nivel de grupo de anuncios. No aplicable a destinos de nivel de campaña. |
| [!UICONTROL Audience] | Necesario para crear un nuevo destino. |
| [!UICONTROL Target Type] | Opcional |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL RLSA Target Status] | Necesario para eliminar un destino. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional; aplicable solo para destinos de nivel de grupo de anuncios. |
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
