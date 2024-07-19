---
title: Administrar archivos de fuente de datos de inventario
description: Obtenga información sobre cómo configurar las opciones que controlan cómo se procesan los datos de fuentes.
exl-id: 7d19ecc0-c939-4996-b22b-970ce8644b09
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Administrar archivos de fuente de datos de inventario

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Si envía sus propios datos de fuente, debe cargar archivos que contengan los datos del producto para crear dinámicamente la estructura de la campaña, los anuncios y las palabras clave, en función de los datos del producto. A continuación, puede asociarlos con plantillas de publicidad específicas de la red de publicidad y procesar los datos a través de las plantillas para, finalmente, publicar los datos en las redes de publicidad relevantes. Puede asociar varias plantillas a un archivo de fuente, pero cada plantilla solo puede asociarse a un archivo de fuente.

>[!NOTE]
>
>No cargue archivos si utiliza datos directamente de una cuenta de un centro de comerciantes.

Puede cargar y procesar archivos de fuentes de datos de cualquiera de las siguientes maneras:

* **Automáticamente usando FTP:** Puede cargar archivos directamente en un directorio FTP; el servicio de fuentes comprueba los nuevos archivos cada dos horas. Después de cargar un archivo por primera vez, puede asociarlo a una plantilla específica de la red de publicidad. Posteriormente, todos los archivos que cargue con el mismo nombre se asociarán automáticamente a la misma plantilla. Según la configuración de [datos de fuente](feed-settings-manage.md), Search, Social y Commerce pueden propagar automáticamente los datos de fuente a través de todas las plantillas aplicables y, opcionalmente, publicar los datos de campaña y publicidad resultantes en las redes de publicidad relevantes.

  Para configurar un directorio FTP para depositar y procesar automáticamente archivos de datos, póngase en contacto con el equipo de cuenta de Adobe.

* **Procesamiento manual:** Puede [cargar archivos de fuentes](#feed-file-upload) manualmente desde la vista [!UICONTROL Advanced] (ACM). Después de asociar un archivo de fuente con una o más [plantillas](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) específicas de la red de anuncios, puede generar datos de campaña y de publicidad [propagando los datos de fuente a través de las plantillas](feed-data-propagate.md) según la [configuración de los datos de fuente](feed-settings-manage.md). Si lo desea, puede obtener una vista previa de los datos generados en las vistas de jerarquía de campañas, generar un archivo de hoja de edición masiva para su revisión o generar un archivo de hoja de edición masiva para su publicación inmediata en la red de anuncios. Si no publicas los datos inmediatamente, puedes [previsualizarlos](propagated-data-view.md) y [publicarlos](propagated-data-post.md) más tarde. Puede [reemplazar posteriormente el archivo de fuente existente por un nuevo archivo](#feed-file-replace) sin perder ninguna asociación de plantilla existente.

## Requisitos del archivo de fuente

No se requieren campos de datos específicos en un archivo individual, pero se requieren los siguientes campos para cada archivo:

* La primera línea del archivo debe contener nombres de columna (también denominados *encabezados*), que corresponden a los parámetros dinámicos de las plantillas asociadas. Las líneas restantes deben incluir datos que correspondan a los nombres de columna. Cada línea de datos (fila) debe pertenecer únicamente a un componente de cuenta, como una campaña o un anuncio. Los valores de todas las líneas deben estar separados por tabulaciones o comas. Consulte el [archivo de ejemplo CSV](#example-csv-feed-file) y el [archivo de ejemplo TSV](#example-tsv-feed-file) a continuación.

* El archivo puede tener cualquier tamaño, pero debe tener una de las siguientes extensiones: `.tsv` (para valores separados por tabulaciones), `.txt` (para texto ASCII compatible con [!DNL Unicode]), `.csv` (para valores separados por comas) o `.zip` (para un solo archivo en formato ZIP comprimido, que se descomprime en un archivo TSV).

* El nombre de archivo distingue entre mayúsculas y minúsculas y no puede incluir los siguientes caracteres: `# % & * | \ : " < > . ? /`

* Si deposita archivos en un directorio FTP, debe utilizar el mismo nombre de archivo para cada versión del archivo.

* ([!DNL Google Ads] plantillas solamente) Si la plantilla usa el parámetro de anuncio Param2 o Param2 en los anuncios de texto, los campos de datos correspondientes del archivo de fuente deben incluir datos numéricos, sin símbolos monetarios.

* Para actualizar los componentes de cuenta existentes, incluya el nombre de la campaña existente (y sus componentes, si corresponde). Si no se especifica la estructura existente, se crean nuevos componentes.

### Ejemplo de archivo de fuente separado por comas {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### Ejemplo de archivo de fuente separado por tabuladores {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## Prácticas recomendadas

* Para datos que incluyen caracteres internacionales, utilice archivos en formato TSV o TXT.

* Para lograr un proceso repetible con una revisión manual o edición limitadas, configure los archivos de fuente y sus datos de estructura de cuentas de la siguiente manera:

   * Incluya columnas y filas que contengan datos suficientes para crear una estructura contable o asignarlas a la estructura contable existente. Lo ideal es utilizar una estructura de cuentas existente que esté estrechamente vinculada a la taxonomía de productos y a la que se asignen fácilmente los datos de fuentes.

   * Incluya descripciones que sean lo suficientemente cortas como para usarlas en una copia de anuncio.

   * Utilice patrones de datos coherentes y convenciones de nomenclatura en todas las filas de productos.

   * Elimine todos los espacios anteriores y finales.

   * Elimine los caracteres ilegibles.

## Ver o descargar un archivo de fuente

Puede abrir o descargar cualquier archivo de fuente que se haya cargado manualmente o mediante FTP.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

1. Busque el archivo de fuente:

1. En la lista de plantillas, busque una plantilla que utilice el archivo de fuente.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Feeds]** para abrir una lista de todos los archivos de fuente.

1. Haga clic en el nombre del archivo de fuente.

1. Abra o guarde el archivo según el procedimiento normal del explorador.

Para obtener más información, consulte la ayuda en línea del explorador.

## Cargar manualmente un archivo de fuente {#feed-file-upload}

>[!NOTE]
> Si asocia una plantilla con un archivo cargado manualmente pero luego carga por FTP otro archivo con el mismo nombre, extensión y formato gramatical, se utilizará al propagar los datos por la plantilla. Por ejemplo, myfile.csv reemplaza a myfile.csv, pero Myfile.CSV no.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Feeds]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Upload]**.

1. Especifique el archivo que desea cargar; para ello, especifique la ruta de acceso completa y el nombre del archivo, o bien haga clic en **[!UICONTROL Browse]** para ubicarlo en su dispositivo o red.

1. Haga clic en **[!UICONTROL Upload].

Se validan todos los campos del archivo. No puede enviar elementos con longitudes de campo no válidas más adelante hasta que corrija los valores. Todos los nombres de columna del archivo estarán disponibles en las plantillas como parámetros dinámicos.

## Reemplazar un archivo de fuente {#feed-file-replace}

Cuando reemplaza un archivo de fuente (incluso si el nuevo archivo tiene un nombre o una extensión diferente), todas las asociaciones de plantilla existentes permanecen. El nuevo archivo se utiliza al propagar datos a través de todas las plantillas que originalmente estaban asociadas al archivo anterior.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

1. Realice una de las acciones siguientes:

   * En la columna [!UICONTROL Feed] de cualquier plantilla aplicable, haga clic en ![Más opciones](/help/search-social-commerce/assets/options.png "Más opciones") y seleccione **[!UICONTROL Re-upload]**.

   * En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Feeds]**. En la lista de archivos de fuentes, active la casilla situada junto al nombre del archivo existente. Sobre la tabla de datos, haga clic en **[!UICONTROL Upload]**.

   >[!NOTE]
   >
   >El origen del archivo de fuente (&quot;[!UICONTROL FTP]&quot; o &quot;&amp;mdash&quot; para archivos cargados manualmente) se incluye en la columna [!UICONTROL Source].

1. Especifique el archivo que desea cargar; para ello, especifique la ruta de acceso completa y el nombre del archivo, o bien haga clic en **[!UICONTROL Browse]** para ubicarlo en su dispositivo o red.

Incluso si el nuevo archivo tiene un nombre o una extensión diferente, el archivo existente se sobrescribe con el nuevo archivo.

1. Haga clic en **[!UICONTROL Re-Upload]**.

Se validan todos los campos del archivo. No puede enviar elementos con longitudes de campo no válidas más adelante hasta que corrija los valores. Todos los nombres de columna del archivo estarán disponibles en las plantillas como parámetros dinámicos.

## Eliminar archivos de fuente

Puede eliminar cualquier archivo de fuente que se haya cargado manualmente o mediante FTP. Cuando se elimina un archivo de fuente, ya no está asociado a ninguna plantilla.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Feeds]**.

1. Active la casilla de verificación situada junto a cada archivo que desee eliminar.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagar datos de fuentes a través de plantillas](feed-data-propagate.md)
>* [Ver datos generados a partir de fuentes](propagated-data-view.md)
>* [Editar datos generados a partir de fuentes](propagated-data-edit.md)
>* [Publicar datos de campaña generados a partir de fuentes en redes de anuncios](propagated-data-post.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de datos generados a partir de fuentes](propagated-data-status.md)
