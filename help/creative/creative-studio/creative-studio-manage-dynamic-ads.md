---
title: Administre creativos dinámicos en Creative Studio.
description: Aprenda a crear, editar, duplicar y eliminar creativos dinámicos impulsados por catálogos en Adobe Advertising Creative Studio.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 0%

---

# Administrar elementos creativos dinámicos en [!UICONTROL Creative Studio]

*característica de Beta*

La ficha **[!UICONTROL Creatives]** de [!UICONTROL Creative Studio] enumera los elementos creativos dinámicos por biblioteca. Desde aquí puede crear nuevos creativos dinámicos impulsados por catálogo, editar los detalles y la asignación de atributos de creativos existentes, ver registros de cambios, duplicar creativos y eliminar creativos.

## Cree un creativo dinámico {#build-dynamic-creative}

Utilice este flujo de trabajo para crear creativos dinámicos impulsados por el catálogo. Un asistente guiado de cuatro pasos le guiará a través de la selección de una plantilla, la conexión de un catálogo y la asignación de campos de catálogo a elementos de plantilla. Después de la configuración, [!UICONTROL AI Assistant] le ayudará a obtener una vista previa y a comprobar la calidad de cada combinación de anuncios generada a partir de los datos del catálogo.

Los creativos dinámicos se diferencian de los anuncios estándar de una manera clave: el agente de IA no puede modificar el contenido procedente del catálogo. Puede filtrar, analizar y marcar problemas, pero para cambiar el contenido de los anuncios debe actualizar el catálogo de origen.

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

   Si continúa con el control de calidad, el lienzo muestra todas las combinaciones de anuncios generadas a partir del catálogo, mostradas como filas con una vista previa de cada entrada de catálogo representada en la plantilla.

1. Si continúa con el control de calidad:

   1. Realice una de las siguientes acciones:

      * Utilice los controles **[!UICONTROL Zoom in]** y **[!UICONTROL Zoom out]** para ajustar la vista de lienzo.

      * Use los controles de paginación (**X-Y de Z**) para recorrer las filas del catálogo.

      * Para editar una combinación de anuncios:

         1. Mantenga el cursor sobre la fila del catálogo y haga clic en **[!UICONTROL Edit]**.

         1. En el cuadro de diálogo **[!UICONTROL Edit Row]**, actualice los valores de campo.

         1. Haga clic en **[!UICONTROL Save]**.

        El lienzo se actualiza para reflejar los valores actualizados.

      * Utilice el panel de chat **[!UICONTROL AI Assistant]** para analizar y filtrar combinaciones de catálogos. Escriba la solicitud en el campo **[!UICONTROL Ask anything]** o haga clic en una de las indicaciones sugeridas:

         * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
         * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
         * **[!UICONTROL Show me all ads for millennial women in urban markets]**

        El agente de IA puede:

         * Filtre el lienzo para mostrar anuncios que coincidan con un segmento de audiencia, ubicación geográfica, idioma, categoría u otro campo de catálogo específico.
         * Compruebe problemas de calidad, como saturaciones del límite de caracteres, desbordamiento o sangrado de contenido, vínculos de imágenes rotos y visibilidad de la exención de responsabilidad legal.
         * Compare combinaciones de anuncios para el análisis de pruebas A/B.
         * Organice los anuncios en grupos para revisarlos en paralelo.

        El agente de IA no puede modificar el contenido procedente del catálogo. Para cambiar el contenido del anuncio, actualice el catálogo de origen.

   1. Guardar **[!UICONTROL Save Dynamic Creative]** en el encabezado.

   1. En el mensaje de confirmación, haga clic en **[!UICONTROL Create]**.

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

## Vuelva a abrir el asistente de control de calidad para un elemento creativo dinámico {#qa-dynamic-creative}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   Se abre la pantalla de control de calidad. Consulte &quot;[Paso 5: previsualización y control de calidad con IA](#qa)&quot; para ver los controles de lienzo disponibles y las capacidades del asistente de IA.

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
