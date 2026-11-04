---
title: Editar y comprobar la calidad de los creativos dinámicos
description: Aprenda a editar la configuración creativa dinámica y el contenido del catálogo de comprobación de calidad en una biblioteca creativa.
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ed1682eff9ce28df30a5314de90f6f67c10f338a
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%
---
# Editar y comprobar la calidad de los creativos dinámicos

Edite la configuración creativa para cambiar su configuración, como el nombre, los catálogos y la asignación de atributos. Utilice el agente de control de calidad para revisar los anuncios resultantes y los valores de catálogo correctos.

## Editar configuración creativa {#edit-creative-settings}

### Desde la nueva IU {#from-the-new-ui}

1. Abra la configuración creativa:

   * Desde una biblioteca creativa:

     1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Abra la biblioteca mediante cualquiera de estos métodos:

        * Haga clic en el nombre de la biblioteca.

        * Junto al nombre de la biblioteca, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Open]**.

     1. En la ficha **[!UICONTROL Creatives]**, haga clic en **[!UICONTROL ...]** junto al nombre del elemento creativo y, a continuación, haga clic en **[!UICONTROL Edit]**.

   * De [!UICONTROL Creative Studio]:

     1. En el menú principal, haga clic en **[!UICONTROL Creative]>[!UICONTROL Creative Studio]**.

     1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

        Se abrirá un editor de pantalla completa con una vista previa del anuncio a la izquierda y un panel de configuración a la derecha.

1. Edite la configuración creativa mediante las fichas **[!UICONTROL Details]** y **[!UICONTROL Attribute Mapping]**:

   Ficha **[!UICONTROL Details]**:

   * **[!UICONTROL Advertiser]**, **[!UICONTROL Ad Library]** y **[!UICONTROL Ad template]** son de solo lectura.
   * **[!UICONTROL Dynamic creative name]:** El nombre para mostrar del creativo.
   * **[!UICONTROL Number of cards]:** Número de ofertas de catálogo incluidas en cada combinación de publicidad (1-50).
   * (Opcional) En **[!UICONTROL Catalogs]**, actualice la selección del catálogo:
     * Use **[!UICONTROL Catalog template]** para filtrar los catálogos disponibles. Si lo desea, puede descargar el archivo de plantilla haciendo clic en **[!UICONTROL Download feed template]**.
     * Busque y seleccione catálogos de la lista, o cargue un nuevo archivo de catálogo arrastrándolo al área de carga o haciendo clic en **[!UICONTROL Browse Files]** (formatos admitidos: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP, MP4; máximo 25 MB; un archivo a la vez). Los catálogos cargados están etiquetados **(cargados)** en la lista de chips.

     Todos los catálogos deben pertenecer a la misma familia de plantillas de catálogo.

   Ficha **[!UICONTROL Attribute Mapping]**:

   * En **[!UICONTROL Targeting]**, seleccione al menos un origen de datos: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** o **[!UICONTROL Audience Segment]**.
   * En **[!UICONTROL Attribute Mapping]**, actualice la asignación de cada nombre de capa de plantilla a la etiqueta de columna de catálogo correspondiente.

1. Haga clic en **[!UICONTROL Update Creative]**.

### Desde la IU heredada {#from-the-legacy-ui}

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Haga clic en **[!UICONTROL Switch to classic UI]**.

1. Haga clic en el nombre de la biblioteca.

1. Mantenga el cursor sobre la fila creativa y haga clic en **[!UICONTROL Edit]**.

1. Editar la [configuración de publicidad dinámica](creative-settings-dynamic.md).

1. Haga clic en **[!UICONTROL Continue]** para previsualizar los elementos creativos que desea generar. Puede realizar cualquiera de las siguientes acciones dentro de la vista previa:

   * Para filtrar los elementos creativos por catálogo, valor de filtro <!-- explain more--> y tamaño de anuncio, utilice los filtros situados encima del área de vista previa.

   * Para buscar un producto por su ID único, vaya al campo de búsqueda debajo del área de vista previa.

   * Para cambiar las columnas mostradas, haga clic en ![Filtro de columna](/help/creative/assets/custom-columns.png "Filtro de columna") debajo del área de vista previa.

   * Para obtener una vista previa de un elemento creativo específico, active la casilla de verificación de la fila.

   * Cambiar el contenido:

     * (Solo anuncios de visualización) Para editar el valor de una celda dentro de la tabla, haga clic dentro de la celda y edite el valor. Haga clic fuera de la celda o presione la tecla **[!DNL Enter]** para guardar los cambios.

     * Para marcar un solo producto como predeterminado <!--Explain what this means. -->, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

     * (Cuando el anuncio incluya más de una oferta) Para marcar varios productos como predeterminados, seleccione las filas (hasta el número de ofertas) y haga clic en **[!UICONTROL Set as Default]** en la barra de herramientas de acciones por lotes.

     * Para eliminar un producto del catálogo, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

     * (Cuando el anuncio incluya más de una oferta) Para eliminar varios productos del catálogo, seleccione las filas (hasta el número de ofertas) y haga clic en **[!UICONTROL Delete Row]** en la barra de herramientas de acciones por lotes.

1. Guarde a los creativos:

   * Para guardar los anuncios y agregarlos a un [paquete creativo](bundle-manage.md) de la biblioteca:

     1. Haga clic en **[!UICONTROL Save and Attach to Bundle]**.

     1. Haga clic **[!UICONTROL Save]** para guardar los anuncios.

     1. Seleccione los paquetes y haga clic en **[!UICONTROL Attach Creative to Bundles]**.

   * Para guardar los anuncios y salir de la configuración, haga clic en **[!UICONTROL Save]** y, a continuación, haga clic de nuevo en **[!UICONTROL Save]**.

## Comprobar la calidad de un elemento creativo dinámico (solo interfaz de usuario nueva) {#qa-dynamic-creative}

Utilice el agente de control de calidad en la nueva interfaz de usuario para analizar las filas del catálogo con la plantilla de un creativo dinámico, previsualizar los anuncios resultantes e identificar posibles problemas de contenido. Puede filtrar y agrupar anuncios utilizando **[!UICONTROL AI Assistant]**, revisar las alertas del catálogo y corregir manualmente los valores del catálogo antes de publicar los cambios.

>[!NOTE]
>
>Puede comprobar la calidad de los elementos creativos dinámicos de [!UICONTROL Creative Libraries] o [!UICONTROL Creative Studio]. Consulte &quot;[Comprobar la calidad de un creativo dinámico de Creative Studio](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#qa-dynamic-creative)&quot; para el otro punto de entrada.

El agente de control de calidad solo está disponible para creativos de pantallas dinámicas basadas en plantillas dinámicas, no en creativos estándar o creativos de vídeos dinámicos.

### Abra el agente de control de calidad {#open-qa-agent}

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Abra la biblioteca mediante cualquiera de estos métodos:

   * Haga clic en el nombre de la biblioteca.
   * Junto al nombre de la biblioteca, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. En la ficha **[!UICONTROL Creatives]**, haga clic en **[!UICONTROL ...]** junto al nombre del elemento creativo dinámico y, a continuación, haga clic en **[!UICONTROL QA Agent]**.

   La pantalla **[!UICONTROL Dynamic Creative QA]** se abre con un lienzo de vista previa y el panel de chat **[!UICONTROL AI Assistant]**.

1. Si el creativo utiliza varios catálogos, seleccione el catálogo que desea revisar de **[!UICONTROL Catalog]** en el encabezado.

   El asistente analiza el catálogo seleccionado. El selector de catálogo se desactiva cuando el creativo utiliza un solo catálogo.

### Analizar y filtrar anuncios con IA {#analyze-ads}

1. En el panel **[!UICONTROL AI Assistant]**, escriba una solicitud en **[!UICONTROL Ask anything]** y presione **[!UICONTROL Enter]**, o bien haga clic en una de las indicaciones sugeridas:

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   El asistente responde en el panel de chat y muestra las filas de catálogo coincidentes como vistas previas de anuncios en el lienzo. Hasta que envíe una solicitud, el lienzo le pedirá que pida al asistente que analice el catálogo.

1. Seguir perfeccionando la revisión con solicitudes de seguimiento. El ayudante puede ayudarle a lo siguiente:

   * Filtre los anuncios por segmento de audiencia, idioma, ubicación geográfica o código postal.
   * Compruebe las longitudes de caracteres utilizando un umbral que especifique.
   * Compruebe si hay errores de fuentes, contenido faltante y contenido sospechoso.
   * Revise el estado de traducción.
   * Comparar variantes de prueba A/B.
   * Agrupar anuncios para su revisión, como por producto o problema.

   Compruebe las respuestas del asistente e inspeccione las vistas previas antes de guardar los cambios.

### Revisar previsualizaciones y alertas {#review-previews}

* Utilice la barra de herramientas de lienzo para:

  * Ajuste el zoom.
  * Cambiar entre **[!UICONTROL Thumbnail view]** y **[!UICONTROL Actual size]**.
  * Haga clic en **[!UICONTROL Replay animations]** para reproducir las vistas previas.
  * Seleccione el número de filas por página, seleccione un número de página o use **[!UICONTROL Previous page]** y **[!UICONTROL Next page]**.

* Cuando el asistente agrupe los resultados, haga clic en el vínculo para ver todos los creativos de un grupo. Use **[!UICONTROL Back to groups]** para volver a los resultados agrupados o **[!UICONTROL Catalog Rows]** para salir de la vista agrupada.

* Cuando una vista previa muestre **[!UICONTROL Issues detected]**, mantenga el cursor sobre el indicador para ver los detalles del problema.

* Cuando haya alertas de catálogo disponibles, haga clic en **[!UICONTROL View Alerts]**. El cuadro de diálogo **[!UICONTROL Alerts]** enumera el catálogo, el número de fila, la columna y el mensaje de error de cada problema. Haga clic en **[!UICONTROL Close]** para regresar al lienzo.

### Valores de catálogo correctos {#correct-catalog-values}

Puede editar manualmente los valores del catálogo desde una vista previa del anuncio sin salir de la pantalla de control de calidad.

1. En la vista previa que desee corregir, haga clic en **[!UICONTROL Edit]**.

1. En el cuadro de diálogo de edición, seleccione las columnas que desea cambiar en **[!UICONTROL Catalog columns to edit]**. Para buscar una columna, use **[!UICONTROL Search columns]**.

1. En **[!UICONTROL Columns content]**, actualice los valores de los campos seleccionados.

1. Haga clic en **[!UICONTROL Update]**.

   La vista previa se actualiza para reflejar los valores actualizados. Los cambios del catálogo no se publican hasta que guarde el elemento creativo dinámico.

>[!IMPORTANT]
>
>Estas ediciones actualizan los datos del catálogo, no solo la vista previa del anuncio. Revise los valores antes de publicarlos.

### Guardar cambios o salir {#save-or-exit}

* Para guardar el elemento creativo dinámico existente y publicar cualquier edición del catálogo:

  1. Haga clic en **[!UICONTROL Save Dynamic Creative]** en el encabezado.

  1. En el cuadro de diálogo de confirmación **[!UICONTROL Update Dynamic Creative]**, haga clic en **[!UICONTROL Update]**.

     Vuelve a la biblioteca creativa.

* Para salir sin publicar las ediciones de catálogo pendientes, haga clic en **[!UICONTROL Cancel]** en el encabezado de la página.

>[!MORELIKETHIS]
>
>* [Configuración creativa dinámica](creative-settings-dynamic.md)
>* [Agregar elementos creativos dinámicos a una biblioteca creativa](creative-add-dynamic.md)
>* [Ver el registro de cambios de un elemento creativo](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
