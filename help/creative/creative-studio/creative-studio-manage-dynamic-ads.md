---
title: Administre creativos dinámicos en Creative Studio.
description: Aprenda a crear, comprobar la calidad, editar, duplicar y eliminar creativos dinámicos impulsados por catálogos en Adobe Advertising Creative Studio.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 88fead9ffc4eaa572be090877790422e67831036
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 0%
---
# Administrar elementos creativos dinámicos en [!UICONTROL Creative Studio]

La ficha **[!UICONTROL Creatives]** de [!UICONTROL Creative Studio] enumera los elementos creativos dinámicos por biblioteca. Desde aquí puede crear nuevos creativos dinámicos impulsados por catálogo, creativos de comprobación de calidad con IA, editar los detalles y la asignación de atributos de creativos existentes, ver registros de cambios, duplicar creativos y eliminar creativos.

## Cree un creativo dinámico {#build-dynamic-creative}

Utilice este flujo de trabajo para crear creativos dinámicos impulsados por el catálogo. Un asistente guiado de cuatro pasos le guiará a través de la selección de una plantilla, la conexión de un catálogo y la asignación de campos de catálogo a elementos de plantilla. Después de la configuración, [!UICONTROL AI Assistant] le ayudará a obtener una vista previa y a comprobar la calidad de cada combinación de anuncios generada a partir de los datos del catálogo.

Los creativos dinámicos se diferencian de los anuncios estándar de una manera clave: el agente de IA no puede modificar el contenido procedente del catálogo. Puede filtrar, analizar y marcar problemas, pero para cambiar el contenido de los anuncios debe actualizar los valores del catálogo manualmente, ya sea desde la pantalla de control de calidad o en el catálogo de origen.

### Requisitos previos

* Debe existir al menos una plantilla de anuncio en pantalla creada por el usuario (no una plantilla del sistema) en la biblioteca de plantillas.
* Hay un catálogo de productos o de contenido (fuente) disponible en su cuenta.

### Paso 1: Abrir el asistente [!UICONTROL Build Dynamic Creative] {#open-wizard}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, haga clic en **[!UICONTROL Build]** en la tarjeta de acciones rápidas **[!UICONTROL Build dynamic creatives from catalog data]**.

   Se abre el cuadro de diálogo de cuatro pasos **[!UICONTROL Build Dynamic Creative]**.

### Paso 2: Seleccionar una plantilla {#select-template}

>[!NOTE]
>
>La galería de plantillas muestra solo las plantillas de anuncios que ha creado. Las plantillas de sistema y las plantillas de anuncios de vídeo no están disponibles como punto de partida para los creativos dinámicos.

1. En la galería de plantillas, haga clic en una plantilla para seleccionarla.

   El botón **[!UICONTROL Next]** se deshabilita hasta que se selecciona una plantilla.

1. Haga clic en **[!UICONTROL Use this template]**.

### Paso 3: Selección de un catálogo {#select-catalog}

1. Configure las opciones creativas:

   * **[!UICONTROL Ad Library]:** Seleccione la biblioteca creativa en la que desea guardar el elemento creativo.
   * **[!UICONTROL Dynamic creative name]:** Escriba un nombre para el creativo dinámico.
   * **[!UICONTROL Number of cards]:** Escriba el número de ofertas de catálogo que se incluirán en cada combinación de anuncios (1-50).
   * **[!UICONTROL Assign dynamic creative to a bundle]:** (opcional) cuando está habilitada, los elementos creativos guardados se adjuntan a un paquete. Seleccione un paquete de la biblioteca.

1. Seleccione uno o varios catálogos:

   1. (Opcional) Use **[!UICONTROL Catalog template]** para filtrar la lista de catálogos a una familia de plantillas específica. Si lo desea, descargue el archivo de plantilla para revisarlo, haga clic en **[!UICONTROL Download feed template]**.

   1. Busque y seleccione catálogos en la lista. Todos los catálogos seleccionados deben pertenecer a la misma familia de plantillas de catálogo; aparece una advertencia si intenta mezclar familias.

   1. (Opcional) Para cargar un nuevo archivo de catálogo, arrastre y suelte el archivo en el área de carga o haga clic en **[!UICONTROL Browse Files]**. Formatos compatibles: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP y MP4. Tamaño máximo de archivo: 25 MB. Puede cargar un archivo a la vez. Los catálogos cargados aparecen en la lista de chips con la etiqueta **(cargada)**.

1. Haga clic en **[!UICONTROL Continue]**.

### Paso 4: Asignar campos de catálogo a elementos de plantilla {#attribute-mapping}

Asigne cada campo de catálogo al elemento correspondiente de la plantilla. Por ejemplo, asigne el campo de nombre de producto del catálogo al elemento de titular de la plantilla y el campo de imagen de producto al elemento de imagen de fondo.

1. En **[!UICONTROL Targeting]**, seleccione al menos un origen de datos para personalizar el elemento creativo: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** o **[!UICONTROL Audience Segment]**.

1. Para cada elemento de plantilla, seleccione el campo de catálogo coincidente de la lista desplegable.

1. Haga clic en **[!UICONTROL Continue]**.

### Paso 5: Previsualización y control de calidad con IA {#qa}

1. Elija si desea *[!UICONTROL Save Dynamic Creative & Skip QA]* o *[!UICONTROL Continue to QA]*.

   Si continúa con el control de calidad, la pantalla **[!UICONTROL Dynamic Creative QA]** se abrirá con un lienzo de vista previa y el panel de chat **[!UICONTROL AI Assistant]**.

1. Si continúa con el control de calidad, siga los procedimientos de &quot;[Comprobar la calidad de un elemento creativo dinámico](#qa-dynamic-creative)&quot; para [analizar y filtrar anuncios](#analyze-ads), [revisar vistas previas y alertas](#review-previews) y, opcionalmente, [corregir valores de catálogo](#correct-catalog-values). Cuando haya terminado, [guarde el elemento creativo dinámico](#save-or-exit).

## Editar un elemento creativo dinámico {#edit-dynamic-creative}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

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

## Comprobar la calidad de un creativo dinámico {#qa-dynamic-creative}

Utilice el agente de control de calidad para analizar las filas del catálogo con la plantilla de un creativo dinámico, previsualizar los anuncios resultantes e identificar posibles problemas de contenido. Puede filtrar y agrupar anuncios utilizando **[!UICONTROL AI Assistant]**, revisar las alertas del catálogo y corregir manualmente los valores del catálogo antes de publicar los cambios.

El agente abre la pantalla **[!UICONTROL Dynamic Creative QA]** desde [!UICONTROL Creative Libraries] o [!UICONTROL Creative Studio]. Aunque las etiquetas de menú difieren, ambos puntos de entrada proporcionan la misma funcionalidad de control de calidad. El análisis depende del creativo, el catálogo y la solicitud seleccionados.

>[!NOTE]
>
>El agente de control de calidad está disponible para creativos de pantallas dinámicas, no para creativos estándar o de vídeo dinámico. En [!UICONTROL Creative Libraries], la acción solo está disponible para los creativos dinámicos basados en plantillas dinámicas.

### Abra el agente de control de calidad {#open-qa-agent}

1. Abra un creativo dinámico guardado para control de calidad de cualquiera de las siguientes maneras:

   * **De [!UICONTROL Creative Libraries]:**

     1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Haga clic en el nombre de la biblioteca para abrirla.

     1. En la ficha **[!UICONTROL Creatives]**, haga clic en **[!UICONTROL ...]** junto al nombre del elemento creativo dinámico y, a continuación, haga clic en **[!UICONTROL QA Agent]**.

   * **De [!UICONTROL Creative Studio]:**

     1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**.

     1. En la ficha **[!UICONTROL Creatives]**, busque el elemento creativo dinámico en su biblioteca creativa debajo de la sección [!UICONTROL Generate or Build Creatives].

     1. Mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

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

* Para guardar el elemento creativo dinámico y publicar cualquier edición del catálogo:

  1. Haga clic en **[!UICONTROL Save Dynamic Creative]** en el encabezado.

  1. Confirme el guardado:

     * Para un nuevo elemento creativo, en el cuadro de diálogo de confirmación **[!UICONTROL Create Dynamic Creative]**, haga clic en **[!UICONTROL Create]**.
     * Para un elemento creativo existente, en el cuadro de diálogo de confirmación **[!UICONTROL Update Dynamic Creative]**, haga clic en **[!UICONTROL Update]**.

     Vuelve a la biblioteca creativa o a [!UICONTROL Creative Studio], según dónde haya abierto la pantalla de control de calidad.

* Para salir sin publicar las ediciones de catálogo pendientes, haga clic en **[!UICONTROL Cancel]** en el encabezado de la página.

## Ver el registro de cambios de un creativo dinámico {#view-change-log}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

## Duplicación de un elemento creativo dinámico {#duplicate-dynamic-creative}

Duplique un elemento creativo dinámico para añadir un nuevo elemento creativo con la misma configuración a la biblioteca. Más adelante puede cambiar el nombre del nuevo elemento creativo y editar la configuración según sea necesario.

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   El nombre del nuevo creativo es `<original name> (copy)`.

## Eliminar un elemento creativo dinámico {#delete-dynamic-creative}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de Creative Studio en Advertising Creative](creative-studio-about.md)
>* [Administrar anuncios estándar en Creative Studio](creative-studio-manage-standard-ads.md)
>* [Administrar plantillas en Creative Studio](creative-studio-manage-templates.md)
