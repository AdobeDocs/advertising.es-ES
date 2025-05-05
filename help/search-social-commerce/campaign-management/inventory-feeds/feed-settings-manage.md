---
title: Configuración de los datos de fuente
description: Obtenga información sobre cómo configurar las opciones que controlan cómo se procesan los datos de fuentes.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Configuración de los datos de fuente

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Puede configurar cómo gestionar grupos de anuncios, palabras clave y anuncios en archivos de datos de fuentes y cómo procesar los datos en archivos FTP específicamente, a través de la configuración de fuentes.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Settings]**.

1. Especifique la [configuración de datos de fuente](#feed-data-settings):

   1. En la sección [!UICONTROL Obsolete Item Auto-Processing], seleccione información en los campos.

   1. (Anunciantes que cargan datos a través de FTP o mediante un vínculo directo a una cuenta de un centro comercial) En la sección [!UICONTROL FTP/GMC Account Auto-Processing], seleccione información en los campos.

   1. En la sección [!UICONTROL Miscellaneous Auto-Processing], seleccione información en los campos.

1. Haga clic en **[!UICONTROL Save]**.

## Configuración de datos de fuente {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Aplica toda la configuración de [!UICONTROL Obsolete Item Auto-processing] a:

* *[!UICONTROL Ad Groups Only]:* Solo grupos de anuncios obsoletos.

* *[!UICONTROL Keywords Only]:* Solo palabras clave y grupos de productos obsoletos.

* *[!UICONTROL Ad Variations Only]* (predeterminado): solo anuncios obsoletos.

* *[!UICONTROL Keywords and Ad Variations]:* Tanto palabras clave obsoletas/destinos de producto/grupos de productos como anuncios obsoletos.

>[!NOTE]
>
>* Para [!DNL Google Ads] anuncios de compras, solo se ve afectado el grupo de productos de nivel inferior.
>* Para cuentas de [!DNL Yandex], las tareas de procesamiento automático de elementos obsoletos siempre se realizan en variaciones de anuncios, independientemente de esta configuración.

**[!UICONTROL When the Scheduled End Date is reached]:** (solo datos publicados manualmente) Qué hacer con los elementos de línea de un archivo de fuente publicado con una fecha y hora de finalización especificadas una vez que llega la hora de finalización:

* *[!UICONTROL Delete]* (valor predeterminado): elimina todos los componentes relevantes cuando llegue la hora de finalización especificada. No puede revertir esta operación.

* *[!UICONTROL Pause]:* Pausar todos los componentes relevantes cuando llegue la hora de finalización especificada. Si es necesario, puede reactivar los componentes más adelante.

* *[!UICONTROL None]:* No cambie el estado de los componentes relevantes.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Qué hacer con los elementos existentes cuando no se incluyen en un nuevo archivo de fuente que se cargó manualmente o cuando no se asignan a campañas o grupos de anuncios existentes según la configuración Asignar solo en la plantilla:

* *[!UICONTROL Delete]:* Eliminar los componentes existentes.

* *[!UICONTROL Pause]:* Pausar los componentes existentes. Se reactivan si un nuevo archivo de fuente contiene alguno de los mismos elementos de línea y conservan su historial y sus puntuaciones de calidad. **Nota:** Si faltan todos los grupos de productos secundarios de un grupo de productos principal, se eliminará el grupo de productos principal porque no se pueden pausar los grupos de productos.

* *[!UICONTROL None]* (valor predeterminado): no cambie los componentes existentes.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Qué hacer con los elementos existentes cuando 1) no se incluyen a) en un nuevo archivo de fuente que se cargó en un directorio FTP o b) en una cuenta de un centro comercial la próxima vez que Search, Social y Commerce se sincronicen con él, o 2) cuando no se asignan a campañas o grupos de anuncios existentes según la configuración de [!UICONTROL Map Only] en la plantilla.

* *[!UICONTROL Delete]:* Eliminar los componentes existentes.

* *[!UICONTROL Pause]:* Pausar los componentes existentes. Se reactivan si los nuevos datos contienen alguno de los mismos elementos de línea y conservan su historial y puntuación de calidad. **Nota:** Si faltan todos los grupos de productos secundarios de un grupo de productos principal, se eliminará el grupo de productos principal porque no se pueden pausar los grupos de productos.

* *[!UICONTROL None]* (valor predeterminado): no cambie los componentes existentes.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Qué hacer con los elementos de línea que incluyen un nivel de stock cuando:

* (Para fuentes con valores de existencias solo numéricos en la columna especificada) El nivel de existencias está en una cantidad especificada o por debajo de ella. La cantidad predeterminada es cero (0).

* (Para fuentes con valores de texto en la columna especificada) El valor de [!UICONTROL Availability] es &quot;[!UICONTROL out of stock]&quot;; el valor no distingue entre mayúsculas y minúsculas. **Nota:** **En plantillas de fuentes, indique columnas de nivel de existencias basadas en texto usando la casilla de verificación para &quot;[!UICONTROL This column has non-numeric values]&quot;.&quot;

Seleccione la acción para ambos casos:

* *[!UICONTROL Delete]* (valor predeterminado) Eliminar los componentes.

* *[!UICONTROL Pause]:* Pausar los componentes. Cuando se actualizan los datos, los componentes se reactivan si los valores de existencias numéricos superan la cantidad especificada o si [!UICONTROL Availability] es &quot;[!UICONTROL in stock]&quot; o &quot;[!UICONTROL preorder]&quot;. Los componentes conservan su historial y su puntuación de calidad.

El nivel de stock de cada elemento de línea proviene de una columna del archivo de fuente, tal como se especifica en el campo &quot;[!UICONTROL Stock Level]&quot; para cada plantilla.

>[!TIP]
>
>* En el caso de los productos o servicios para los que espera volver a almacenar o aumentar la disponibilidad, debe poner en pausa los grupos de anuncios, las palabras clave y los anuncios en lugar de eliminarlos y volver a crearlos. La pausa les permite conservar sus puntuaciones de calidad.
>* Si habilita el procesamiento automático obsoleto para grupos de anuncios y los nuevos datos incluyen un nivel de stock para el grupo de anuncios, resulta significativo eliminar o pausar el grupo de anuncios solo cuando el nivel de stock especificado está en el nivel de categoría en lugar de en el nivel de marca/artículo. Por ejemplo, si tiene un grupo de anuncios &quot;convertibles&quot;, el nivel de stock del grupo de anuncios debe ser el total de todos los modelos convertibles individuales representados en el grupo de anuncios.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Anunciantes que cargan archivos de datos a través de FTP o una cuenta de un centro comercial) Propaga automáticamente los nuevos datos a través de las plantillas aplicables. La opción está seleccionada de forma predeterminada. Si desactiva la opción, aún puede propagar manualmente los datos de cualquier archivo o cuenta de fuente o de cualquier plantilla.

>[!NOTE]
>
>* En el caso de los archivos FTP, el servicio de fuentes comprueba las actualizaciones en el directorio FTP cada dos horas (horas pares en el huso horario PST). Esta opción procesa todos los archivos cargados desde la última comprobación.
>* Para las cuentas del centro comercial, Search, Social y Commerce se sincronizan con la cuenta diariamente a las 06:00, aproximadamente, en el huso horario del anunciante. Esta opción procesa todos los datos actualizados desde la última sincronización.
>* Los datos propagados están disponibles desde las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads] hasta que los datos se publiquen en la red de anuncios o en la vista [!UICONTROL Bulksheets].

**[!UICONTROL Post to the SE]:** (Anunciantes que cargan archivos de datos a través de FTP o una cuenta de un centro comercial) Crea automáticamente archivos de hojas de edición masiva en los formatos correctos para las redes de anuncios relevantes después de que los nuevos datos se propaguen a través de las plantillas aplicables. Esta opción también quita los datos de las fichas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads], a menos que algún subcomponente tenga errores.

Esta opción está desactivada de forma predeterminada. Para habilitar esta opción, active la casilla de verificación y, a continuación, especifique si desea publicar archivos de hojas de edición masiva en las redes de anuncios:

* *[!UICONTROL Immediately]* (predeterminado): publica los archivos de hoja de edición masiva en las redes de publicidad relevantes después de que los datos se propaguen a través de las plantillas. Los archivos de hojas de edición masiva permanecen disponibles en la vista [!UICONTROL Bulksheets] durante 30 días.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:**&#x200B; No publica los archivos de hojas de edición masiva en las redes de anuncios relevantes, pero los enumera en la vista [!UICONTROL Bulksheets], desde la cual puede publicarlos más adelante. Los archivos de hojas de edición masiva permanecen disponibles en la vista [!UICONTROL Bulksheets] durante 30 días. Cuando el archivo de hoja de edición masiva ocupa más de 10 MB pero menos de 2 GB, el archivo está en formato ZIP; no es necesario descomprimir el archivo para publicarlo. &#x200B;** Sugerencia:** Si no ha validado previamente sus páginas de aterrizaje, utilice esta opción para poder validarlas desde la vista [!UICONTROL Bulksheets] antes de publicar los datos en la red publicitaria.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Impide que se publiquen en la red de anuncios frases de palabras clave con un número de palabras superior al especificado. Si se selecciona esta opción, las frases de palabras clave con un número de palabras superior al máximo se propagan y se enumeran en la ficha [!UICONTROL Keywords], pero no se publican al intentar publicar los datos.

Esta opción está deshabilitada de forma predeterminada para que se publiquen todas las palabras clave, independientemente de cuántas palabras incluya la frase. Si selecciona esta opción, seleccione el número máximo de palabras que desea publicar (de 3 a 10).

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagar datos de fuentes a través de plantillas](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de anuncios](propagated-data-post.md)
