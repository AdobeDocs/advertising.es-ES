---
title: Administración de plantillas de publicidad en Creative Studio
description: Obtenga información sobre cómo crear, importar, organizar y administrar plantillas de publicidad en Adobe Advertising Creative.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8fa8d6c66228d3a0af1de2514dd016d8f50262e8
workflow-type: tm+mt
source-wordcount: '3702'
ht-degree: 1%
---
# Administrar plantillas de publicidad en [!UICONTROL Creative Studio]

Cree, importe y administre plantillas de anuncios de vídeo y visualización para utilizarlas en sesiones de generación de anuncios.

## La vista [!UICONTROL Creative Studio] > [!UICONTROL Templates]

La ficha **[!UICONTROL Templates]** proporciona acciones rápidas para crear o importar nuevas plantillas de publicidad.

La ficha [!UICONTROL Templates] también enumera las plantillas de anuncios existentes en la parte inferior de la página <!-- Only in the Templates tab -->como [tarjetas individuales (predeterminado) o como tablas/listas](/help/creative/introduction/customize-data-views.md). La lista de plantillas de anuncio incluye fichas para [!UICONTROL All], [!UICONTROL System Templates] (que el equipo de cuenta de Adobe carga en su cuenta) y [!UICONTROL User Templates]. De forma predeterminada, se muestran las plantillas de anuncios de todos los anunciantes. Para ver solo las plantillas de publicidad de un anunciante específico, seleccione en la lista de anunciantes de la parte superior de la página.

<!--
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### Acciones disponibles

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Creación:

* [Generación de una plantilla de anuncio mediante IA](#template-generate)

* [Creación manual de una plantilla de anuncio](#template-create)

* [Importar plantillas de publicidad de HTML5](#templates-import)

Acciones en las plantillas existentes:

* [Generar variaciones de anuncios a partir de una plantilla de anuncio en pantalla](#ad-variations-generate)

* [Edición de una plantilla de publicidad](#template-edit)

* [Adición o eliminación de etiquetas para una plantilla de publicidad](#template-labels)

* [Previsualización de una plantilla de anuncio](#template-preview)

* [Descargar una plantilla de publicidad](#template-download)

* [Agregar o quitar una plantilla de anuncio como favorita](#template-favorite)

* [Eliminación de una plantilla de anuncio](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## Generación de una plantilla de anuncio mediante IA {#template-generate}

*característica de Beta*

Use IA en [!UICONTROL Creative Studio] para convertir una imagen de anuncio en pantalla estática existente en una plantilla de anuncio en pantalla editable. Un asistente de tres pasos le ayuda a generar y revisar la plantilla, solicitar cambios con lenguaje natural y abrir el editor de plantillas para realizar cambios manuales y guardar la plantilla.

### Requisitos previos

Necesita un anuncio de imagen estática en una biblioteca de Creative. Este flujo de trabajo selecciona anuncios de las bibliotecas; no carga una imagen nueva directamente en el cuadro de diálogo de generación.

<!--

Publish this when prompt-based generation becomes available:

To generate a template from an existing image, you need a static image ad in a Creative Library. This option selects ads from your libraries; it doesn't upload a new image directly in the generation dialog. You don't need an existing ad image to generate a template from a prompt.

-->

### Paso 1: Generar y revisar la plantilla

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. (Opcional) Seleccione un anunciante de la lista de anunciantes en la parte superior de la página para ver las bibliotecas de ese anunciante.

1. En el cuadro **[!UICONTROL Use AI to Generate a New Display Ad Template]**, haga clic en **[!UICONTROL Generate]**.

1. En el cuadro de diálogo **[!UICONTROL Generate New Ad Template]**, seleccione **[!UICONTROL Generate from Existing Standard Ad Image]** si aún no está seleccionado.

1. Seleccione la biblioteca que contiene el anuncio de imagen de la lista **[!UICONTROL Ad Library]**.

1. Mantenga el cursor sobre la imagen y la tarjeta y haga clic en **[!UICONTROL Use this Standard Ad]**.

   La generación comienza automáticamente, utilizando la anchura y altura del anuncio seleccionado.

<!--

Switch to this when prompt-based generation becomes available:

1. In the **[!UICONTROL Generate New Ad Template]** dialog, choose how to generate the template:

   * **[!UICONTROL Generate from Prompt]:** Describe the ad template you want to create using a text prompt.

   * **[!UICONTROL Generate from Existing Standard Ad Image]:** Convert an existing static image ad into an editable template.

1. Follow the steps for your selected option:

   * From a prompt:

      1. Enter a description of the template you want to create. Include details such as the layout, headline, call to action, and visual style.

      1. Follow the on-screen instructions to generate the template.

   * From an existing standard ad image:

      1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

      1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

         Generation begins automatically, using the selected ad's width and height.

-->

1. [Revise y perfeccione la plantilla generada](#template-review).

### Paso 2: revisar y perfeccionar la plantilla {#template-review}

1. Espere a que finalice la generación y, a continuación, revise la vista previa de la plantilla y el panel **[!UICONTROL Layers]**, cuando esté disponible.

   Compruebe el texto, las imágenes y el diseño antes de utilizar la plantilla. Las capas que se muestran aquí son para revisión; realice cambios manuales en el editor de plantillas.

1. (Opcional) Solicite cambios en la plantilla generada:

   1. En el campo **[!UICONTROL Ask the AI for any changes]**, describa los cambios que desee. Por ejemplo, escriba `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Haga clic en **[!UICONTROL Regenerate]**.

   1. Revise la vista previa actualizada. Repita el proceso según sea necesario.

1. Cuando esté listo para continuar, haga clic en **[!UICONTROL Use this Ad Template]**.

   La plantilla generada se abre en el editor de plantillas de visualización.

### Paso 3: Editar y guardar la plantilla {#template-save}

>[!TIP]
>
> El asistente de IA utiliza una biblioteca de fuentes de código abierto para encontrar una coincidencia aproximada de la fuente del anuncio. Para usar su propia fuente, cárguela a la ficha [!UICONTROL Assets] o desde el editor de plantillas y, a continuación, reemplace la fuente generada en el editor.
>
> Para obtener mejores resultados, reemplace el logotipo generado por IA con su logotipo original y con píxeles perfectos en el editor de plantillas.

1. En el editor de plantillas, revise los elementos generados y realice los cambios restantes con los [controles del editor de plantillas](#template-controls).

1. Haga clic en **[!UICONTROL Save]**.

1. En el cuadro de diálogo **[!UICONTROL Update Template]**, escriba o actualice **[!UICONTROL Template name]**, seleccione **[!UICONTROL Advertiser]** y, opcionalmente, agregue etiquetas.

1. Haga clic en **[!UICONTROL Update]** para guardar la plantilla y volver a la vista **[!UICONTROL Templates]**.

   Para guardar una copia independiente, haga clic en **[!UICONTROL Save As New]**.

Luego puede usar la plantilla para [generar variaciones de anuncios](#ad-variations-generate).

### Si no puede generar una plantilla {#troubleshooting}

| Problema | Qué hacer |
| --- | --- |
| No se muestran bibliotecas ni anuncios de imagen al generar a partir de una imagen | Compruebe el anunciante seleccionado y **[!UICONTROL Ad Library]**. Si la biblioteca no tiene imágenes de anuncio estándar, seleccione otra biblioteca que contenga un anuncio de imagen estática existente. |
| La generación basada en imágenes falla o no se puede convertir la imagen | Revise el mensaje mostrado, haga clic en **[!UICONTROL Back to library]** y seleccione un anuncio de imagen para intentarlo de nuevo. |

<!--

Add when prompt-based generation is available:

| Prompt-based generation fails | Review the displayed message and revise your prompt before trying again. |

-->

## Creación manual de una plantilla de anuncio {#template-create}

Cree una visualización o una plantilla de vídeo en blanco con el editor de plantillas.

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. En el cuadro **[!UICONTROL Create New Ad Template]**, haga clic en **[!UICONTROL Create]** y seleccione **[!UICONTROL Display Ad Template]** o **[!UICONTROL Video Ad Template]**.

1. (Mostrar anuncios) Seleccione el tamaño de la plantilla de anuncio y haga clic en **[!UICONTROL Continue]**.

1. Configure las opciones de la plantilla con los [controles del editor de plantillas](#template-controls).

1. (Opcional) Para descargar una copia de la plantilla tal como se definió, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   El archivo se descarga según el procedimiento normal del explorador.

1. Guarde la plantilla:

   1. Realice una de las acciones siguientes:

      * Haga clic en **[!UICONTROL Save]**.

      * Para guardar la plantilla como borrador, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**.

   1. Escriba **[!UICONTROL Template name]**, seleccione **[!UICONTROL Advertiser]**, opcionalmente seleccione las etiquetas existentes o agregue nuevas etiquetas a la plantilla y, a continuación, haga clic en **[!UICONTROL Save]**.

## Importar plantillas de publicidad de HTML5 {#templates-import}

Cargue una o más plantillas creadas previamente de HTML5 que estén empaquetadas como archivos ZIP. Las plantillas se validan en la importación; la importación falla si el HTML supera los 200 000 caracteres, el CSS los 60 000 caracteres, la plantilla contiene más de 5000 elementos DOM o incluye etiquetas de script no admitidas.

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Seleccione el anunciante en la parte superior de la página.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. En el cuadro **[!UICONTROL Upload HTML5 Templates]**, haga clic en **[!UICONTROL Upload]** y seleccione **[!UICONTROL Display Ad Template]** o **[!UICONTROL Video Ad Template]**.

1. Seleccione uno o varios archivos ZIP del dispositivo o de la red.

1. En el diálogo **[!UICONTROL Import Templates]**:

   1. Seleccione un(a) **[!UICONTROL Advertiser]**.

      Si ya ha seleccionado un anunciante específico en la parte superior de la página, ese anunciante se preselecciona.

   1. (Opcional) Para cada archivo, edite **[!UICONTROL Template Name]**.

      El nombre de archivo se utiliza de forma predeterminada.

   1. (Opcional) Para agregar más archivos, haga clic en **[!UICONTROL Add more]** y seleccione otros archivos ZIP. Especifique **[!UICONTROL Template Name]** para cada archivo adicional.

1. Haga clic en **[!UICONTROL Import Templates]**.

>[!NOTE]
>
>Si la importación falla, simplifique la plantilla o póngase en contacto con el equipo de cuenta de Adobe.

## Edición de una plantilla de publicidad {#template-edit}

*Solo plantillas de anuncios de visualización.*

>[!IMPORTANT]
>
>El agente de IA no puede cambiar el diseño de la plantilla, las posiciones de los elementos, el espaciado ni la tipografía. Realice cambios estructurales en el editor de plantillas antes de generar contenido.

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la tarjeta de plantilla o fila de tabla y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Template]**.

1. Edite el diseño o los elementos de la plantilla utilizando los [controles del editor de plantillas](#template-controls).

1. (Opcional) Para descargar una copia de la plantilla tal como se definió, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   El archivo se descarga según el procedimiento normal del explorador.

1. Guarde la plantilla:

   * Haga clic en **[!UICONTROL Save]**.

   * Para guardar la plantilla como borrador, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**. Escriba **[!UICONTROL Template name]**, seleccione **[!UICONTROL Advertiser]**, opcionalmente seleccione las etiquetas existentes o agregue nuevas etiquetas a la plantilla y, a continuación, haga clic en **[!UICONTROL Save]**.

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## Generar variaciones de anuncios a partir de una plantilla de anuncio en pantalla {#ad-variations-generate}

*Solo plantillas de anuncios de visualización.*

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la tarjeta de plantilla o fila de tabla y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   [!UICONTROL Ad Variations Generator] se abre con la plantilla precargada.

1. Utilice la interfaz de chat de IA para generar y refinar el contenido de los anuncios. Consulte &quot;[Administrar anuncios estándar en Creative Studio](creative-studio-manage-standard-ads.md)&quot; para ver el flujo de trabajo completo.

## Adición o eliminación de etiquetas para una plantilla de publicidad {#template-labels}

*Solo plantillas de anuncios de visualización.*

Las etiquetas ayudan a organizar y filtrar las plantillas de usuario. No puede agregar etiquetas a las plantillas del sistema.

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la tarjeta de plantilla o fila de tabla y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**.

1. En el diálogo **[!UICONTROL Edit Labels]**:

   * Para agregar una etiqueta, seleccione una etiqueta existente o escriba un nombre en el campo de entrada y haga clic en **[!UICONTROL Add Tag]**.

   * Para quitar una etiqueta, haga clic en **[!UICONTROL X]** junto a la etiqueta.

1. Haga clic en **[!UICONTROL Save]**.

## Previsualización de una plantilla de anuncio {#template-preview}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la tarjeta de plantilla.

1. Realice una de las acciones siguientes:

   * (Vista de tarjeta) Haga clic en el icono **[!UICONTROL Preview template]** o en **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

   * (Vista de tabla) Haga clic en **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

1. Para las plantillas de vídeo, haz clic en ![Reproducir](/help/creative/assets/play.png "Reproducir").

## Descargar una plantilla de publicidad {#template-download}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la tarjeta de plantilla o fila de tabla y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   La plantilla se descarga como archivo ZIP según el procedimiento normal del explorador.

## Agregar o quitar una plantilla de anuncio como favorita {#template-favorite}

*Solo vista de tarjeta*

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la tarjeta de plantilla.

1. Realice una de las acciones siguientes:

   * Para agregar una plantilla como favorita, haz clic en ![Favorito](/help/creative/assets/favorite-null.png "Favorito").

   * Para quitar una plantilla como favorita, haz clic en ![Favorito](/help/creative/assets/favorite.png "Favorito").

## Eliminación de una plantilla de anuncio {#template-delete}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la tarjeta de plantilla o fila de tabla y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Controles del editor de plantillas {#template-controls}

Los editores de plantillas de vídeo y visualización proporcionan una barra de herramientas sobre el lienzo para deshacer cambios y ajustar la vista, paneles a la izquierda para agregar recursos y elementos y un panel [!UICONTROL Layers] a la derecha para administrar capas. Las herramientas para editar los elementos seleccionados y controlar la temporización y la reproducción difieren entre las plantillas de visualización y de vídeo.

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### Deshacer cambios y ajustar la vista de lienzo

La barra de herramientas de acciones generales se encuentra encima del lienzo de edición en el editor de plantillas de publicidad y está dividida en dos partes (izquierda y derecha).

#### Mostrar plantillas de publicidad

| Control | Descripción |
| --- | --- |
| **[!UICONTROL Undo]** | Deshace la última acción. |
| ![Rehacer](/help/creative/assets/cs-icon-redo.png "Rehacer") **[!UICONTROL Redo]** | Rehace la última acción deshecha. |
| **[!UICONTROL Links]** | Abre un panel para administrar las direcciones URL de pulsación adjuntas a los elementos de la plantilla. |
| Controles de zoom | Haga clic en **[!UICONTROL Zoom out]** o **[!UICONTROL Zoom in]** para ajustar la ampliación del lienzo (de 10% a 150%, en incrementos de 10%). Haga clic en la etiqueta de nivel de zoom (que muestra **[!UICONTROL Auto]** cuando el lienzo se ajusta automáticamente o un porcentaje cuando se establece manualmente) para abrir un menú con las opciones: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** y **[!UICONTROL Zoom Out]**. |
| Tamaño del anuncio | Muestra las dimensiones de anuncio actuales (por ejemplo, 300 × 250). Haga clic para abrir el selector de tamaño, que ofrece seis tamaños estándar IAB usados comúnmente como tarjetas, además de un menú desplegable con los 19 tamaños de anuncios estándar IAB. El tamaño predeterminado de las nuevas plantillas es 300 × 250 (rectángulo de Medium). |
| ![Abrir el panel Capas](/help/creative/assets/layers-panel-open.png "Abrir el panel Capas") | Abre el panel [!UICONTROL Layers]. Solo aparece cuando se cierra el panel [!UICONTROL Layers]. |

#### Plantillas de anuncios de vídeo

| Control | Descripción |
| --- | --- |
| **[!UICONTROL Undo]** / ![Rehacer](/help/creative/assets/cs-icon-redo.png "Rehacer") **[!UICONTROL Redo]** | Deshace o rehace la última acción. |
| Controles de zoom | Haga clic en **[!UICONTROL Zoom out]** o **[!UICONTROL Zoom in]** para ajustar la ampliación del lienzo. Haga clic en el nivel de zoom para abrir un menú con las opciones: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** y **[!UICONTROL Zoom Out]**. |
| ![Abrir el panel Capas](/help/creative/assets/layers-panel-open.png "Abrir el panel Capas") | Abre el panel [!UICONTROL Layers]. Solo aparece cuando se cierra el panel [!UICONTROL Layers]. |

<!--

Not there as of 10/15:

| Page resize | Opens the page-size controls to change the video template dimensions. |
| **[!UICONTROL Preview]** | Opens a preview of the video template. |

   -->

### Agregar recursos y elementos

El panel izquierdo le permite agregar recursos y elementos de publicidad a la plantilla. Haga clic en un icono para abrir su panel de contenido; vuelva a hacer clic en el mismo icono para cerrarlo.

#### Mostrar plantillas de publicidad

| Icono | Descripción |
| --- | --- |
| **[!UICONTROL Search]** | Busque en todos los tipos de recursos de la biblioteca. |
| **[!UICONTROL Upload]** | Cargar imágenes o archivos de fuente en el editor para utilizarlos en la plantilla actual. Puede cargar hasta 20 archivos a la vez. |
| **[!UICONTROL Templates]** | Examine las plantillas de anuncios de la biblioteca de Creative Studio para utilizarlas como capa base o elemento de referencia. |
| **[!UICONTROL My Assets]** | Examine todos los recursos que ha cargado en la pestaña de Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Images]** | Examine únicamente los recursos de imagen que ha cargado en la ficha Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Text]** | Agregue un elemento de texto al lienzo, incluidas las fuentes personalizadas que haya cargado. |
| **[!UICONTROL Elements]** | Agregue formas y elementos de diseño como botones y rectángulos. |

Puede arrastrar un elemento desde cualquier panel directamente al lienzo o hacer clic en él para colocarlo en una posición predeterminada.

#### Plantillas de anuncios de vídeo

| Icono | Descripción |
| --- | --- |
| **[!UICONTROL Search]** | Busque en todos los tipos de recursos de la biblioteca. |
| **[!UICONTROL Upload]** | Cargue archivos de imagen, vídeo, audio o fuente (TTF, OTF, WOFF, WOFF2) en el editor para utilizarlos en la plantilla actual. Puede cargar hasta 20 archivos a la vez. |
| **[!UICONTROL Templates]** | Examine las plantillas de anuncios de la biblioteca de Creative Studio. |
| **[!UICONTROL My Assets]** | Examine todos los recursos que ha cargado en la pestaña de Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Images]** | Examine únicamente los recursos de imagen que ha cargado en la ficha Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Video]** | Examine únicamente los recursos de vídeo que ha cargado en la ficha Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Audio]** | Examine únicamente los recursos de audio que ha cargado en la ficha Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Text]** | Agregue un elemento de texto al lienzo, incluidas las fuentes personalizadas que haya cargado. |
| **[!UICONTROL Elements]** | Agregar formas y elementos vectoriales. |

Puede arrastrar un elemento desde cualquier panel directamente al lienzo o hacer clic en él para colocarlo en una posición predeterminada.

### Editar elementos seleccionados

Haga clic en un elemento del lienzo de edición para seleccionarlo. Según el tipo de plantilla, aparecerán una o más barras de herramientas con controles para ese elemento.

Los controles varían según el tipo de elemento.

<!-- From inspectorbar.ts -->

#### Mostrar barra de herramientas de edición de plantillas

| Control | Tipos de elementos | Descripción |
| --- | --- | --- |
| **[!UICONTROL Properties]** | Todo | Abre un panel para editar el nombre de la capa, marcarla como dinámica (intercambiable durante la generación de anuncios) y establecer una URL de pulsación (solo vínculos). Debajo, elija un estado **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** o **[!UICONTROL Focus]** para aplicar estilo al elemento para ese estado de interacción y, a continuación, ajuste el estilo (tipografía (solo texto y vínculos), decoraciones (relleno, borde, radio de vértice), dimensiones, posición) en función del tipo de elemento. |
| **[!UICONTROL Effects]** | Todo | Abre un panel en el que elige un estado **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** o **[!UICONTROL Focus]** para aplicar efectos a para ese estado de interacción y, a continuación, ajusta las secciones **[!UICONTROL Transform]**, **[!UICONTROL Transition]**, **[!UICONTROL Box Shadow]**, **[!UICONTROL Filter]**, **[!UICONTROL Blend Mode]** y **[!UICONTROL Cursor]**. Los elementos de texto también incluyen una sección **[!UICONTROL Text Shadow]**. |
| **[!UICONTROL Animations]** | Todo | Abre un panel para establecer la hora de entrada y salida de la capa en la escala de tiempo y para configurar los ajustes preestablecidos **[!UICONTROL Entrance Animation]**, **[!UICONTROL Loop Animation]** y **[!UICONTROL Exit Animation]** con duración y aceleración. Incluye **[!UICONTROL Copy]**, **[!UICONTROL Paste]** y **[!UICONTROL Reset]** acciones. |
| **[!UICONTROL Crop]** | Imágenes | Abre una barra de herramientas para recortar la imagen. Seleccione un ajuste preestablecido de **[!UICONTROL Aspect Ratio]** (o **[!UICONTROL Free]**) y luego haga clic en **[!UICONTROL Apply]** o **[!UICONTROL Cancel]**. |
| **[!UICONTROL Position]** | Todo | Abre un menú con **[!UICONTROL Move]** opciones (**[!UICONTROL Forward]**, **[!UICONTROL Backward]**, **[!UICONTROL To front]**, **[!UICONTROL To back]**), **[!UICONTROL Align to Page]** opciones (**[!UICONTROL Top]**, **[!UICONTROL Left]**, **[!UICONTROL Middle]**, **[!UICONTROL Center]**, **[!UICONTROL Bottom]**, **[!UICONTROL Right]**, **[!UICONTROL Fit Vertically]**, **[!UICONTROL Fit Horizontally]**, **[!UICONTROL Fit to Page]**) y, para los elementos que no son de imagen, **[!UICONTROL Layer Level Alignment]** opciones (las mismas seis opciones de alineación, más **[!UICONTROL Fit to Content]**). |

#### Barra de herramientas de edición de plantillas de vídeo

| Control | Tipos de elementos | Descripción |
| --- | --- | --- |
| **[!UICONTROL Shape]** | Formas | Establece las opciones específicas de las formas. |
| Controles de recorte | Imágenes | Ajuste el tipo de recorte, el desvío y el suavizado. |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | Varios elementos seleccionados o un grupo | Agrupa los elementos seleccionados o desagrupa un grupo seleccionado. |
| **[!UICONTROL Combine]** | Formas compatibles | Combina las formas seleccionadas en una única forma. |
| **[!UICONTROL Audio replace]** | Audio y vídeo | Reemplaza la pista de audio por un archivo de la biblioteca de recursos. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | Texto | Ajusta la familia de fuentes, el grosor, el tamaño, la alineación horizontal y otros ajustes tipográficos avanzados. |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | Imágenes y vídeo | Establece el origen de vídeo o la imagen de relleno del elemento. |
| **[!UICONTROL Trim]** | Vídeo y audio | Abre el modo de recorte para definir los puntos iniciales y finales del clip. |
| ![Volumen](/help/creative/assets/volume.png "Volumen") ([!UICONTROL Volume]) | Vídeo y audio | Ajusta el nivel de audio. |
| ![Velocidad de reproducción](/help/creative/assets/speed.png "Velocidad de reproducción") ([!UICONTROL Playback speed]) | Vídeo y audio | Ajusta la velocidad de reproducción. |
| ![Recortar](/help/creative/assets/crop.png "Recortar") ([!UICONTROL Crop]) | Todo | Recorta el elemento en un área personalizada. |
| Controles de giro y volteo | Todo | Rotar o voltear el elemento seleccionado. |
| ![Trazo](/help/creative/assets/stroke.png "Trazo") ([!UICONTROL Stroke]) | Todo | Establece el color y el ancho del borde. |
| **[!UICONTROL Text Background]** | Texto | Agrega un color de fondo detrás del texto. |
| **[!UICONTROL Animations]** | Todo | Añade o edita animaciones de entrada, salida o bucle. |
| **[!UICONTROL Style]** | Todo | Abre un menú con las opciones **[!UICONTROL Adjustments]**, **[!UICONTROL Filter]**, **[!UICONTROL Effect]** y **[!UICONTROL Blur]**. |
| **[!UICONTROL Shadow]** | Todo | Agrega o edita una sombra paralela. |
| **[!UICONTROL Opacity]** | Todo | Establece el nivel de transparencia del elemento. |
| **[!UICONTROL Position]** | Todo | Ajusta numéricamente el tamaño, la posición y la rotación del elemento. |
| ![Panel de edición](/help/creative/assets/cs-template-video-editing-panel.png "Panel de edición") | Todo | Abre o cierra un [panel de edición](#detailed-element-properties-for-video-templates) para el elemento seleccionado con más capacidades de edición. |

#### Propiedades detalladas de los elementos para las plantillas de vídeo

En el editor de plantillas de vídeo, haga clic en ![Panel de edición](/help/creative/assets/cs-template-video-editing-panel.png "Panel de edición") en la barra de herramientas para abrir un panel de edición para el elemento seleccionado con más capacidades de edición. El panel de edición aparece a la izquierda del lienzo y es independiente del panel [!UICONTROL Layers], que enumera las capas de la plantilla.

##### Elementos individuales

Al seleccionar una sola imagen, vídeo, forma o elemento de texto, el panel de edición muestra las secciones aplicables a continuación.

| Sección Panel | Herramienta | Controles |
| --- | --- | --- |
| [!UICONTROL Layer] | Alineación y colocación de capas | Alinea la capa seleccionada a la izquierda, horizontal al centro, derecha, arriba, vertical al centro o abajo. El menú de disposición cambia su orden de apilamiento de adelante hacia atrás. Estos controles colocan la capa en sí misma, no justifican el texto dentro de la capa. |
| | [!UICONTROL Rotate & Flip] | Introduzca un ángulo de rotación en grados. Use ![Voltear horizontalmente](/help/creative/assets/cs-template-video-flip.png "Voltear horizontalmente") para reflejar la capa horizontalmente o ![Voltear verticalmente](/help/creative/assets/cs-template-video-flip-vertical.png "Voltear verticalmente") para reflejarla verticalmente. |
| | ![Opacidad](/help/creative/assets/cs-template-video-opacity.png "Opacidad") [!UICONTROL Opacity] | Hace la capa seleccionada más o menos transparente. |
| | ![Modo de fusión](/help/creative/assets/cs-template-video-blend-mode.png "Modo de fusión") [!UICONTROL Blend Mode] | Cambia la forma en que los colores de la capa seleccionada se combinan con las capas que hay detrás. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Abre controles adicionales para la posición y las dimensiones de la capa. La disponibilidad depende de los permisos de transformación de la capa seleccionada. |
| [!UICONTROL Shape] | ![Opciones de forma](/help/creative/assets/cs-template-video-shape-options.png "Opciones de forma") [!UICONTROL Shape] y propiedades específicas de formas | Cambia la forma y sus propiedades disponibles, como puntos, lados, diámetro interior, ancho de línea o radio de esquina. Los controles dependen de la forma seleccionada. |
| | [!UICONTROL Vector]: [!UICONTROL Edit Path] | Entra en modo de edición vectorial para editar el trazado de la forma, cuando está disponible. |
| [!UICONTROL Character] | ![Tipo de letra](/help/creative/assets/cs-template-video-typeface.png "Tipo de letra"), ![Estilo de texto](/help/creative/assets/cs-template-video-text-style.png "Estilo de texto"), ![Negrita](/help/creative/assets/cs-template-video-text-bold.png "Negrita") negrita, ![Cursiva](/help/creative/assets/cs-template-video-text-italic.png "Cursiva") cursiva y ![Tamaño de fuente](/help/creative/assets/cs-template-video-font-size.png "Tamaño de fuente") | (Capas de texto) Cambia la familia de fuentes, el estilo de fuente y el tamaño del texto seleccionado. |
| | ![Alinear a la izquierda](/help/creative/assets/cs-template-video-text-align-l.png "Alinear a la izquierda") / ![Alinear al centro](/help/creative/assets/cs-template-video-text-align-c.png "Alinear al centro") / ![Alinear a la derecha](/help/creative/assets/cs-template-video-text-align-r.png "Alinear a la derecha") Alineación del texto | (Capas de texto) Alinea el texto dentro de su marco a la izquierda, al centro o a la derecha, o detecta la alineación automáticamente. |
| | ![Configuración de texto avanzada](/help/creative/assets/cs-template-video-advanced-text.png "Configuración de texto avanzada") Configuración de texto avanzada | (Capas de texto) Abre ajustes tipográficos adicionales. |
| [!UICONTROL Fill] | ![Rellenar](/help/creative/assets/cs-template-video-fill.png "Rellenar") controles de relleno | Cambia el color, la imagen o el relleno de vídeo de la capa seleccionada. Los controles reflejan el tipo de relleno actual y abren su configuración. Para el texto, cambia el color del texto. |
| [!UICONTROL Stroke] | Controles de trazo de ![Stroke](/help/creative/assets/cs-template-video-stroke.png "Stroke") | Activa o desactiva el contorno y cambia su color, anchura, estilo y ubicación. Cuando el trazo está activado, aparecen controles adicionales. |
| [!UICONTROL Text Background] | ![Fondo de texto](/help/creative/assets/cs-template-video-text-bg.png "Fondo de texto") Controles de fondo | (Capas de texto) Añade o cambia el fondo detrás del texto. |
| [!UICONTROL Animations] | ![Animación](/help/creative/assets/cs-template-video-animation.png "Animación") [!UICONTROL Presets] | Abre los ajustes preestablecidos de animación de la capa seleccionada, incluidas las animaciones de entrada, salida y bucle. |
| [!UICONTROL Appearance] | ![Ajustes](/help/creative/assets/cs-template-video-adjustments.png "Ajustes") [!UICONTROL Adjustments] | Cambia las propiedades visuales de la capa seleccionada. |
| | ![Filtro](/help/creative/assets/cs-template-video-filter.png "Filtro") [!UICONTROL Filter] | Aplica un filtro visual a la capa seleccionada. |
| | ![Efectos](/help/creative/assets/cs-template-video-effects.png "Efectos") [!UICONTROL Effect] | Aplica un efecto a la capa seleccionada. |
| | ![Desenfocar](/help/creative/assets/cs-template-video-blur.png "Desenfocar") [!UICONTROL Blur] | Aplica un desenfoque a la capa seleccionada. |
| | ![Sombra](/help/creative/assets/cs-template-video-shadow.png "Sombra") [!UICONTROL Shadow] | Añade o cambia la sombra de la capa seleccionada. |

##### Selecciones múltiples y elementos especializados

Cuando se seleccionan varios elementos, un grupo, un elemento de recorte o un clip de audio, el panel de edición muestra las secciones específicas de la selección a continuación. Varios elementos, grupos y recortes también conservan la sección [!UICONTROL Layer].

| Sección Panel | Herramienta | Controles |
| --- | --- | --- |
| [!UICONTROL Layer] | Alineación y colocación de capas | Alinea varios elementos seleccionados o un grupo. El menú de disposición cambia su orden de apilamiento de adelante hacia atrás. |
| | [!UICONTROL Rotate & Flip] | Gira o voltea los elementos o el grupo seleccionados. |
| | ![Opacidad](/help/creative/assets/cs-template-video-opacity.png "Opacidad") [!UICONTROL Opacity] | Hace que los elementos o el grupo seleccionados sean más o menos transparentes. |
| | ![Modo de fusión](/help/creative/assets/cs-template-video-blend-mode.png "Modo de fusión") [!UICONTROL Blend Mode] | Cambia la forma en que los colores de los elementos o grupos seleccionados se combinan con las capas que hay detrás. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Abre los controles de la posición y las dimensiones del grupo o los elementos seleccionados. Los controles disponibles dependen de los elementos seleccionados. |
| [!UICONTROL Selection] | ![Grupo](/help/creative/assets/cs-template-video-group.png "Grupo") Grupo / ![Desagrupar](/help/creative/assets/cs-template-video-ungroup.png "Desagrupar") Desagrupar | Aparece debajo de [!UICONTROL Layer] para varias capas seleccionadas o un grupo seleccionado. Agrupa las capas seleccionadas para que se puedan administrar juntas o separa un grupo en capas individuales. |
| [!UICONTROL Settings] | ![Recorte de recorte](/help/creative/assets/cs-template-video-cutout-clip.png "Recorte de recorte") / ![Superposición de recorte](/help/creative/assets/cs-template-video-cutout-overlay.png "Superposición de recorte") Controles de recorte | (Capas de recorte) Aparece por debajo de [!UICONTROL Layer]. Permite seleccionar el tipo de recorte y ajustar el desvío y el suavizado de bordes. |
| [!UICONTROL Audio Properties] | Recorte ![Recortar](/help/creative/assets/cs-template-video-trim.png "Recortar"), volumen ![Volumen](/help/creative/assets/cs-template-video-volume.png "Volumen") y ![Velocidad de reproducción](/help/creative/assets/cs-template-video-playback-speed.png "Velocidad de reproducción") | (Capas de audio) Establece los puntos iniciales y finales del clip, el nivel de audio y la velocidad de reproducción. |

#### Editar elementos directamente en el lienzo

##### Mostrar plantillas de publicidad

| Acción | Descripción |
| --- | --- |
| **[!UICONTROL Replace]** | (Solo elementos de imagen) Abre el panel Imágenes para que pueda reemplazar la imagen por una de la biblioteca de recursos. |
| ![Avanzar](/help/creative/assets/cs-icon-move-forward.png "Avanzar") **[!UICONTROL Move forward]** | Mueve el elemento un paso hacia adelante en el orden de apilamiento (hacia adelante). |
| ![Mover hacia atrás](/help/creative/assets/cs-icon-move-backward.png "Mover hacia atrás") **[!UICONTROL Move backward]** | Mueve el elemento un paso hacia atrás en el orden de apilamiento (hacia atrás). |
| ![Duplicado](/help/creative/assets/cs-icon-duplicate.png "Duplicado") **[!UICONTROL Duplicate]** | Crea una copia del elemento. |
| ![Eliminar](/help/creative/assets/cs-icon-delete.png "Eliminar") **[!UICONTROL Delete]** | Quita el elemento del lienzo. |
| Controlador de rotación | Haga clic y arrastre el controlador sobre un elemento seleccionado para girarlo. Mantenga presionado **[!UICONTROL Shift]** mientras arrastra para ajustar la rotación a incrementos de 15 grados. |

También puede hacer clic y arrastrar un elemento seleccionado para cambiarlo de posición, y hacer clic y arrastrar los controladores que lo rodean para cambiarlo de tamaño.

##### Plantillas de anuncios de vídeo

| Acción | Descripción |
| --- | --- |
| **[!UICONTROL Edit text]** | (Solo elementos de texto) Cambia al modo de edición de texto para que pueda escribir y dar formato al texto directamente en el lienzo. En el modo de edición de texto, un menú secundario proporciona **[!UICONTROL Text color]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]** y **[!UICONTROL Text variables]** (marcadores de posición de plantilla). |
| **[!UICONTROL Replace]** | (Solo elementos de imagen) Abre la biblioteca de recursos para que pueda intercambiar la imagen. |
| **[!UICONTROL Bring forward]** | Mueve el elemento un paso hacia adelante en el orden de apilamiento. |
| **[!UICONTROL Send backward]** | Mueve el elemento un paso hacia atrás en el orden de apilamiento. |
| **[!UICONTROL Duplicate]** | Crea una copia del elemento. |
| **[!UICONTROL Delete]** | Quita el elemento del lienzo. |
| **... >[!UICONTROL Flip horizontal]** | Voltea el elemento horizontalmente 180 grados. |
| **... >[!UICONTROL Flip vertical]** | Voltea el elemento verticalmente 180 grados. |
| **... >[!UICONTROL Copy Element]** | Copia el elemento en el portapapeles de lienzo. |
| **... >[!UICONTROL Pastes Element]** | Pega el elemento copiado. |

También puede hacer clic y arrastrar un elemento seleccionado para cambiarlo de posición, y hacer clic y arrastrar los controladores que lo rodean para cambiarlo de tamaño.

### Control de la sincronización y reproducción

Los editores de vídeo y visualización muestran un panel de cronología en la parte inferior del lienzo.

#### Mostrar plantillas de publicidad

La cronología muestra una pista para cada capa del lienzo, abarcando el intervalo de tiempo en el que la capa es visible en función de la temporización de la animación de entrada y salida. Arrastre el punto de control inicial o final de una pista para ajustar su tiempo de entrada o salida, o arrastre una pista para reordenar las capas. Haga clic en la regla o arrastre el cabezal de reproducción para moverlo a un punto en el tiempo.

La barra de herramientas de la escala de tiempo incluye un campo **[!UICONTROL Duration]** (de 0 a 60 segundos), **[!UICONTROL Play]**/**[!UICONTROL Pause]**, una pantalla de tiempo actual / duración total, un conmutador de bucle, **[!UICONTROL Timeline Scale]** controles de zoom, un botón **[!UICONTROL Fit View]** y un conmutador de contraer o expandir.

#### Plantillas de anuncios de vídeo

La cronología muestra todos los clips de vídeo y audio de la plantilla. Utilice la línea de tiempo para revisar la disposición temporal de los clips y recortarlos arrastrando sus controladores inicial y final. No puede agregar un nuevo clip directamente en la escala de tiempo; en su lugar, agréguelo desde el panel izquierdo o el lienzo y, a continuación, aparecerá como un clip en la escala de tiempo.

### Administración de capas

El panel [!UICONTROL Layers] en el lado derecho del lienzo enumera todos los elementos de la plantilla y le permite administrar su orden, visibilidad y propiedades. Para mostrar las plantillas, haga clic en **[!UICONTROL Open Layers]** en la barra de herramientas del lienzo para abrirlo. Para las plantillas de vídeo, el panel está abierto de forma predeterminada.

Haga clic en cualquier capa para seleccionar el elemento correspondiente en el lienzo.

**Fichas (solo plantillas de anuncios de visualización)**

Las plantillas de visualización tienen dos fichas en la parte superior del panel [!UICONTROL Layers]:

* **[!UICONTROL Dynamic]**: enumera solo las capas que se pueden intercambiar durante la generación de anuncios, como imágenes y texto que el agente de IA puede reemplazar. Esta es la vista predeterminada para generar variaciones de anuncios.
* **[!UICONTROL All]**: muestra la jerarquía de capas completa de la plantilla, incluidos los contenedores estructurales. Utilice esta vista para inspeccionar o reorganizar cómo se anidan los elementos.

Las plantillas de vídeo muestran todas las capas en una sola lista sin pestañas.

**Acciones por capa**

Mantenga el cursor sobre una capa para ver las siguientes acciones.

| Acción | Descripción |
| --- | --- |
| ![Cambiar nombre de capa](/help/creative/assets/edit.png "Cambiar nombre de capa") **[!UICONTROL Rename layer]** | Permite introducir un nuevo nombre de capa en el panel. |
| ![Bloquear capa](/help/creative/assets/cs-icon-lock.png "Bloquear capa") **[!UICONTROL Lock layer]** / ![Desbloquear capa](/help/creative/assets/cs-icon-unlock.png "Desbloquear capa") **[!UICONTROL Unlock layer]** | Evita o permite mover, editar o reordenar la capa. |
| ![Ocultar capa](/help/creative/assets/cs-icon-hidden.png "Ocultar capa") **[!UICONTROL Hide layer]** / ![Mostrar capa](/help/creative/assets/cs-icon-visible.png "Mostrar capa") **[!UICONTROL Show layer]** | Oculta o muestra la capa en el lienzo. Las capas ocultas se conservan en la plantilla, pero no aparecen cuando esta se procesa. |
| ![Arrastrar para reordenar](/help/creative/assets/cs-icon-drag.png "Arrastrar para reordenar") Arrastrar para reordenar | (Solo plantillas de anuncio de visualización) Arrastre el icono de reordenar para cambiar la posición de la capa en el orden de apilamiento. La capa debe estar desbloqueada para reordenarla. |

**Pie de página del panel**

| Acción | Descripción |
| --- | --- |
| ![Duplicar capa seleccionada](/help/creative/assets/cs-icon-duplicate.png "Duplicar capa seleccionada") **[!UICONTROL Duplicate selected layer]** | Crea una copia de la capa seleccionada. |
| ![Eliminar la capa seleccionada](/help/creative/assets/cs-icon-delete.png "Eliminar la capa seleccionada") **[!UICONTROL Delete selected layer]** | Elimina la capa seleccionada. |
| **[!UICONTROL Group selected layers]** (solo plantillas de vídeo) | Agrupa dos o más capas seleccionadas en un solo grupo. Sólo aparece cuando se seleccionan dos o más capas. Puede desagrupar capas agrupadas o quitar capas individuales del grupo mediante los controles de la fila del grupo. |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

>[!MORELIKETHIS]
>
>* [Acerca de Creative Studio en Advertising Creative](creative-studio-about.md)
>* [Administrar recursos en Creative Studio](creative-studio-manage-assets.md)
>* [Administrar anuncios estándar en Creative Studio](creative-studio-manage-standard-ads.md)
>* [Administrar elementos creativos dinámicos en Creative Studio](creative-studio-manage-dynamic-ads.md)
