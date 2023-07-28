---
title: Configuración de los datos de fuente
description: Obtenga información sobre cómo configurar las opciones que controlan cómo se procesan los datos de fuentes.
exl-id: fc72d1bc-aac7-4280-80c6-4fc53a96a49f
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---

# Configuración de los datos de fuente

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Puede configurar cómo gestionar grupos de anuncios, palabras clave y anuncios en archivos de datos de fuentes y cómo procesar los datos en archivos FTP específicamente, a través de la configuración de fuentes.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Settings]**.

1. Especifique el [configuración de datos de fuente](#feed-data-settings):

   1. En el [!UICONTROL Obsolete Item Auto-Processing] , seleccione información en los campos.

   1. (Anunciantes que cargan datos a través de FTP o mediante un vínculo directo a una cuenta de un centro comercial) En el [!UICONTROL FTP/GMC Account Auto-Processing] , seleccione información en los campos.

   1. En el [!UICONTROL Miscellaneous Auto-Processing] , seleccione información en los campos.

1. Haga clic **[!UICONTROL Save]**.

## Configuración de datos de fuente {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Aplica todos los [!UICONTROL Obsolete Item Auto-processing] configuración para:

* *[!UICONTROL Ad Groups Only]:* Solo grupos de anuncios obsoletos.

* *[!UICONTROL Keywords Only]:* Solo palabras clave y grupos de productos obsoletos.

* *[!UICONTROL Ad Variations Only]* (valor predeterminado): Solo anuncios obsoletos.

* *[!UICONTROL Keywords and Ad Variations]:* Tanto palabras clave/productos/grupos de productos obsoletos como anuncios obsoletos.

>[!NOTE]
>
>* Para [!DNL Google Ads] anuncios de compra, solo se ve afectado el grupo de productos de nivel inferior.
>* Para [!DNL Yandex] En las cuentas de, las tareas de procesamiento automático de elementos obsoletos siempre se realizan en variaciones de anuncios, independientemente de esta configuración.

**[!UICONTROL When the Scheduled End Date is reached]:** (Solo datos publicados manualmente) Qué hacer con los elementos de línea en un archivo de fuente publicado con una fecha y hora de finalización especificadas una vez que llega la hora de finalización:

* *[!UICONTROL Delete]* (el valor predeterminado): elimina todos los componentes relevantes cuando llegue la hora de finalización especificada. No puede revertir esta operación.

* *[!UICONTROL Pause]:* Pausar todos los componentes relevantes cuando llegue la hora de finalización especificada. Si es necesario, puede reactivar los componentes más adelante.

* *[!UICONTROL None]:* No cambie el estado de los componentes relevantes.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Qué hacer con los elementos existentes cuando no se incluyen en un nuevo archivo de fuente que se cargó manualmente o cuando no se asignan a campañas o grupos de publicidad existentes según la configuración Asignar solo en la plantilla:

* *[!UICONTROL Delete]:* Eliminar los componentes existentes.

* *[!UICONTROL Pause]:* Pausar los componentes existentes. Se reactivan si un nuevo archivo de fuente contiene alguno de los mismos elementos de línea y conservan su historial y sus puntuaciones de calidad. **Nota:** Si faltan todos los grupos de productos secundarios de un grupo de productos principal, se elimina el grupo de productos principal porque no se pueden pausar los grupos de productos.

* *[!UICONTROL None]* (el valor predeterminado): no cambie los componentes existentes.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Qué hacer con los elementos existentes cuando 1) no se incluyen a) en un nuevo archivo de fuente que se cargó en un directorio FTP o b) en una cuenta de un centro comercial la próxima vez que Search, Social y Commerce se sincronicen con él, o 2) cuando no se asignan a campañas o grupos de publicidad existentes según el [!UICONTROL Map Only] configuración de la plantilla.

* *[!UICONTROL Delete]:* Eliminar los componentes existentes.

* *[!UICONTROL Pause]:* Pausar los componentes existentes. Se reactivan si los nuevos datos contienen alguno de los mismos elementos de línea y conservan su historial y puntuación de calidad. **Nota:** Si faltan todos los grupos de productos secundarios de un grupo de productos principal, se elimina el grupo de productos principal porque no se pueden pausar los grupos de productos.

* *[!UICONTROL None]* (el valor predeterminado): no cambie los componentes existentes.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Qué hacer con los elementos de línea que incluyen un nivel de stock cuando:

* (Para fuentes con valores de existencias solo numéricos en la columna especificada) El nivel de existencias está en una cantidad especificada o por debajo de ella. La cantidad predeterminada es cero (0).

* (Para fuentes con valores de texto en la columna especificada) El valor de [!UICONTROL Availability] es &quot;[!UICONTROL out of stock]&quot;; el valor no distingue entre mayúsculas y minúsculas. **Nota:** **En las plantillas de fuentes, indique las columnas de nivel de stock basadas en texto con la casilla de verificación para &quot;[!UICONTROL This column has non-numeric values].&quot;

Seleccione la acción para ambos casos:

* *[!UICONTROL Delete]* (opción predeterminada) Elimine los componentes.

* *[!UICONTROL Pause]:* Pausar los componentes. Cuando se actualizan los datos, los componentes se reactivan si los valores numéricos de stock superan la cantidad especificada o si el [!UICONTROL Availability] es &quot;[!UICONTROL in stock]&quot; o &quot;[!UICONTROL preorder]&quot;. Los componentes conservan su historial y su puntuación de calidad.

El nivel de stock de cada elemento de línea proviene de una columna del archivo de fuente, como se especifica en la sección &quot;[!UICONTROL Stock Level]&quot; para cada plantilla.

>[!TIP]
>
>* En el caso de los productos o servicios para los que espera volver a almacenar o aumentar la disponibilidad, debe poner en pausa los grupos de anuncios, las palabras clave y los anuncios en lugar de eliminarlos y volver a crearlos. La pausa les permite conservar sus puntuaciones de calidad.
>* Si habilita el procesamiento automático obsoleto para grupos de anuncios y los nuevos datos incluyen un nivel de stock para el grupo de anuncios, resulta significativo eliminar o pausar el grupo de anuncios solo cuando el nivel de stock especificado está en el nivel de categoría en lugar de en el nivel de marca/artículo. Por ejemplo, si tiene un grupo de anuncios &quot;convertibles&quot;, el nivel de stock del grupo de anuncios debe ser el total de todos los modelos convertibles individuales representados en el grupo de anuncios.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Anunciantes que cargan archivos de datos a través de un FTP o una cuenta de un centro comercial) Propaga automáticamente los nuevos datos a través de las plantillas aplicables. La opción está seleccionada de forma predeterminada. Si desactiva la opción, aún puede propagar manualmente los datos de cualquier archivo o cuenta de fuente o de cualquier plantilla.

>[!NOTE]
>
>* En el caso de los archivos FTP, el servicio de fuentes comprueba las actualizaciones en el directorio FTP cada dos horas (horas pares en el huso horario PST). Esta opción procesa todos los archivos cargados desde la última comprobación.
>* Para las cuentas del centro comercial, Search, Social y Commerce se sincronizan con la cuenta diariamente a las 06:00, aproximadamente, en el huso horario del anunciante. Esta opción procesa todos los datos actualizados desde la última sincronización.
>* Los datos propagados están disponibles en [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] pestañas hasta que los datos se publican en la red de publicidad o en el [!UICONTROL Bulksheets] vista.

**[!UICONTROL Post to the SE]:** (Anunciantes que cargan archivos de datos a través de un FTP o una cuenta de un centro comercial) Crea automáticamente archivos de hojas de edición masiva en los formatos correctos para las redes de publicidad relevantes después de que los nuevos datos se propaguen a través de las plantillas aplicables. Esta opción también elimina los datos del [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] a menos que algún subcomponente contenga errores.

Esta opción está desactivada de forma predeterminada. Para habilitar esta opción, active la casilla de verificación y, a continuación, especifique si desea publicar archivos de hojas de edición masiva en las redes de anuncios:

* *[!UICONTROL Immediately]* (predeterminado): Publica los archivos de hoja de edición masiva en las redes de publicidad relevantes después de que los datos se propaguen a través de las plantillas. Los archivos de hojas de edición masiva permanecen disponibles en el [!UICONTROL Bulksheets] vista durante 30 días.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** No publica los archivos de hojas de edición masiva en las redes de publicidad relevantes, sino que los enumera en la [!UICONTROL Bulksheets] vista, desde la cual puede publicarlas más adelante. Los archivos de hojas de edición masiva permanecen disponibles en el [!UICONTROL Bulksheets] vista durante 30 días. Cuando el archivo de hoja de edición masiva ocupa más de 10 MB pero menos de 2 GB, el archivo está en formato ZIP; no es necesario descomprimir el archivo para publicarlo. **Sugerencia:** Si no ha validado previamente las páginas de aterrizaje, utilice esta opción para poder validarlas desde el [!UICONTROL Bulksheets] ver antes de publicar los datos en la red de publicidad.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Evita publicar en la red de anuncios frases de palabras clave con un número de palabras superior al especificado. Cuando se selecciona esta opción, las frases de palabras clave con un número de palabras superior al máximo se propagan y se enumeran en la [!UICONTROL Keywords] , pero no se publican cuando intenta publicar los datos.

Esta opción está deshabilitada de forma predeterminada para que se publiquen todas las palabras clave, independientemente de cuántas palabras incluya la frase. Si selecciona esta opción, seleccione el número máximo de palabras que desea publicar (de 3 a 10).

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagación de datos de fuentes mediante plantillas](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de publicidad](propagated-data-post.md)
