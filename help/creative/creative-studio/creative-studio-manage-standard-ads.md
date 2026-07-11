---
title: Administración de anuncios estándar en Creative Studio
description: Obtenga información sobre cómo crear, editar, duplicar, descargar y eliminar anuncios en pantalla estándar en la biblioteca de creativos de Creative Studio.
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 0%

---

# Administrar anuncios estándar en [!UICONTROL Creative Studio]

*característica de Beta*

La ficha **[!UICONTROL Creatives]** en [!UICONTROL Creative Studio] es su biblioteca de anuncios en pantalla estándar generados a partir de plantillas. Desde aquí puede crear anuncios utilizando [!UICONTROL Ad Variations Generator], editar anuncios guardados, generar nuevas variaciones a partir de un anuncio existente, ver el registro de cambios, duplicar, descargar y eliminar.

## Creación de anuncios estándar {#create-standard-ads}

Use [!UICONTROL Ad Variations Generator] para generar contenido de anuncios de visualización a partir de una plantilla. El asistente de IA genera y refina titulares, CTA, imágenes, colores y mucho más, y puede crear nuevas variantes de tamaño en una sola sesión.

>[!NOTE]
>
>Actualmente, la generación de anuncios estándar solo admite plantillas de anuncios en pantalla. Las plantillas de anuncios de vídeo no están disponibles como punto de partida, ni en la ficha **[!UICONTROL Creatives]** ni en la ficha **[!UICONTROL Templates]**.

### Requisitos previos

Debe existir al menos una plantilla de anuncio en pantalla en la biblioteca de plantillas.

### Generación de anuncios estándar

1. Abra [!UICONTROL Ad Variations Generator] de cualquiera de las siguientes maneras:

   * **De la ficha [!UICONTROL Creatives]:**

      1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

      1. En la ficha **[!UICONTROL Creatives]**, haga clic en **[!UICONTROL Generate]** en la tarjeta de acciones rápidas **[!UICONTROL Generate standard ads from templates]**.

      1. En el cuadro de diálogo de selección de plantillas, haga clic en una plantilla para seleccionarla y luego haga clic en **[!UICONTROL Use this template]**.

   * (Solo anuncios de visualización) **De la ficha [!UICONTROL Templates]:**

      1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

      1. Haga clic en la ficha **[!UICONTROL Templates]**.

      1. Mantenga el cursor sobre una tarjeta de plantilla y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**.

   Se abre [!UICONTROL Ad Variations Generator]. El lienzo muestra la sección **[!UICONTROL Template Sizes]** con los formatos de anuncio disponibles en la plantilla y una sección **[!UICONTROL Ad Concepts]** en la que aparecerá el contenido generado.

1. (Opcional) Para aplicar un perfil de marca a los anuncios, seleccione un(a) **[!UICONTROL Brand Profile]** en la barra de herramientas de lienzo.

   El asistente de IA utiliza el logotipo, la paleta de colores, las directrices de voz, los estándares de imagen y las directrices de canal de su marca al generar contenido.

1. Generar variaciones de anuncios utilizando [!UICONTROL AI Assistant]:

   1. En el campo **[!UICONTROL Ask AI to generate ad variations…]**, escriba una solicitud y presione **[!UICONTROL Enter]**, o bien haga clic en una de las indicaciones destacadas:

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      La IA genera resultados en el lienzo y los organiza en *conceptos*, cada uno de los cuales representa una variación de contenido distinta. El contador de conceptos de la sección **[!UICONTROL Ad Concepts]** realiza el seguimiento de cuántos conceptos existen (por ejemplo, **(2/10)**). Se permiten hasta 10 conceptos por sesión.

   1. Siga perfeccionando enviando mensajes de seguimiento. Ejemplos:

      * &quot;Haga que toda la copia sea más lúdica y menos corporativa&quot;.
      * &quot;Cambie el logotipo a la versión en blanco.&quot;
      * &quot;Configure CTA en &#39;Comprar ahora&#39; en todos los conceptos&quot;.
      * &quot;Cambie el tamaño de este anuncio a los 6 tamaños de pantalla estándar IAB&quot;.
      * &quot;Dame 3 conceptos de titulares diferentes con una imagen de fondo coincidente para cada uno&quot;.

      >[!NOTE]
      >
      >El asistente de IA puede generar y modificar texto (titulares, subtitulares, CTA, texto independiente), intercambiar imágenes de fondo, aplicar colores de marca, cambiar versiones de logotipos y crear nuevas plantillas de tamaño. No puede cambiar la estructura de la plantilla: posiciones de los elementos, diseño, espaciado, relleno, familia de fuentes, tamaño de fuente o bordes. Realice cambios estructurales en el editor de plantillas antes de iniciar la sesión. Consulte [Editar una plantilla](creative-studio-manage-templates.md#edit-template).

   1. (Opcional) Para incluir una referencia visual en una solicitud, haga clic en el botón **[!UICONTROL +]** en el área de entrada de chat. En el diálogo **[!UICONTROL Select from Asset Library]**:

      * Para usar un recurso en su biblioteca de recursos, haga clic en él y, a continuación, haga clic en **[!UICONTROL Add to chat]**. Envíe el mensaje para incluir el recurso como contexto.

      * Para cargar uno o más recursos, haga clic en **[!UICONTROL Upload Assets]** y seleccione los archivos del dispositivo o de la red.

1. (Opcional) Utilice la barra de herramientas de lienzo para revisar los anuncios generados:

   * **[!UICONTROL Brand]:** Seleccione o cambie el perfil de marca aplicado a la sesión.
   * **[!UICONTROL Zoom in]** / **[!UICONTROL Zoom out]:** Ajustar el nivel de zoom del lienzo.
   * **[!UICONTROL Fit to screen]:** Restablezca la vista para mostrar todos los tamaños.
   * **[!UICONTROL Replay animations]:** Reproducir animaciones de plantilla.

   Cuando la API crea un nuevo tamaño, **[!UICONTROL Adjust]**, **[!UICONTROL Keep]** y los controles de eliminación aparecen en la nueva tarjeta de tamaño. Haga clic en **[!UICONTROL Keep]** para aceptar el tamaño tal cual, haga clic en **[!UICONTROL Adjust]** para abrir la plantilla en el editor de visualización, donde podrá realizar cambios estructurales y, a continuación, haga clic en **[!UICONTROL Update Ad Format]** para guardar, o haga clic en el icono Eliminar para eliminar el nuevo tamaño.

1. (Opcional) Administrar conceptos y variaciones:

   * Para administrar un concepto, mantenga el cursor sobre la etiqueta del concepto (por ejemplo, **[!UICONTROL Concept 3]**) y haga clic en **[!UICONTROL ...]**; a continuación, seleccione una opción:

      * **[!UICONTROL Add to chat]:** Hace referencia al concepto en la siguiente solicitud.
      * **[!UICONTROL Delete]:** quita el concepto.

   * Para administrar una variación individual, mantenga el cursor sobre la tarjeta de variación y haga clic en **[!UICONTROL ...]**. Luego, seleccione una opción:

      * **[!UICONTROL Add to Chat]:** Hace referencia a la variación en el siguiente mensaje. También puede hacer clic directamente en el cuerpo de la tarjeta de variación para alternar la mención.
      * **[!UICONTROL Edit Data]:** Abre un cuadro de diálogo en el que puede actualizar la variación **[!UICONTROL Name]** y la URL de pulsación para cada etiqueta de clic definida en la plantilla. Haga clic **[!UICONTROL Save]** para aplicar.
      * **[!UICONTROL Delete]:** quita la variación.

1. Cuando esté satisfecho con los conceptos generados, haga clic en **[!UICONTROL Save Standard Ads]** en el encabezado.

   El botón está desactivado hasta que exista al menos un concepto.

1. En el cuadro de diálogo **[!UICONTROL Save Standard Ads]**, especifique la siguiente configuración y haga clic en **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** (obligatorio) el anunciante en el que guardar los elementos creativos.

   **[!UICONTROL Creative Library]:** (obligatorio) La biblioteca creativa en la que guardar los elementos creativos. El selector de bibliotecas se activa después de seleccionar un anunciante.

   **[!UICONTROL Attach to Bundles]:** (opcional) cuando está habilitada, los elementos creativos guardados se adjuntan a uno o varios paquetes. Para cada variación de anuncio, seleccione un paquete o introduzca un nuevo nombre de paquete.

   **\[Configuración para cada anuncio\]:** Para cada variación de anuncio, puede ver y, opcionalmente, cambiar **[!UICONTROL Name],** **[!UICONTROL Language],** y **[!UICONTROL click URL].**

## Edición de un anuncio estándar {#edit-standard-ad}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   Se abre un editor de pantalla completa con una vista previa de anuncio en directo a la izquierda y un panel de configuración a la derecha.

1. Edite la configuración del anuncio utilizando las fichas **[!UICONTROL Details]** y **[!UICONTROL Attributes]**:

   Ficha **[!UICONTROL Details]**:

   * **[!UICONTROL Creative Name]:** (obligatorio) El nombre para mostrar del creativo.
   * **[!UICONTROL Language]:** (obligatorio) El idioma del contenido del anuncio.
   * **[!UICONTROL Creative Size]:** (solo lectura) Las dimensiones del anuncio.
   * **Haga clic en etiquetas:** Si la plantilla define etiquetas de clic, cada etiqueta de clic aparecerá como un campo obligatorio etiquetado con el nombre de la etiqueta. Introduzca la URL de destino de pulsación para cada etiqueta.
   * **[!UICONTROL Label]:** etiquetas (opcionales) para organizar a los creativos. Seleccione las etiquetas existentes o escriba una etiqueta nueva y haga clic en **[!UICONTROL Add tag].**

   Ficha **[!UICONTROL Attributes]**:

   La vista previa en directo se actualiza en tiempo real a medida que edita. La ficha **[!UICONTROL Attributes]** no está disponible mientras se carga la vista previa.

   * **Atributos de texto:** Escriba el valor de texto para cada capa de texto editable definida en la plantilla.
   * **Atributos de imagen:** Muestra una miniatura de la imagen actual. Haga clic en **[!UICONTROL Replace Image]** para cargar un reemplazo (PNG, JPEG, GIF, WebP o SVG).

1. Haga clic en **[!UICONTROL Update Creative]**.

## Generar variaciones de anuncios para un anuncio estándar {#generate-ad-variations}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   Se abre [!UICONTROL Ad Variations Generator] con el anuncio seleccionado precargado.

1. Utilice la interfaz de chat de IA para generar y refinar variaciones adicionales. Consulte &quot;[Crear anuncios estándar](#create-standard-ads)&quot; para ver el flujo de trabajo completo.

## Duplicación de un anuncio estándar {#duplicate-standard-ad}

Duplique un anuncio estándar para añadir un nuevo elemento creativo con la misma configuración a la biblioteca. Más adelante puede cambiar el nombre del nuevo elemento creativo y editar la configuración según sea necesario.

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   El nombre del nuevo creativo es `<original name> (copy)`.

## Visualización del registro de cambios de un anuncio estándar {#view-change-log}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

   Se abre un cuadro de diálogo que muestra una tabla de cambios en el anuncio.

## Descargar un anuncio estándar {#download-standard-ad}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   El creativo descarga según el procedimiento normal del explorador.

## Eliminación de un anuncio estándar {#delete-standard-ad}

>[!NOTE]
>
>Esta acción no se puede deshacer.

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de Creative Studio en Advertising Creative](creative-studio-about.md)
>* [Administrar elementos creativos dinámicos en Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Administrar plantillas en Creative Studio](creative-studio-manage-templates.md)
>* [Administrar perfiles de marca en Advertising Creative](/help/creative/brands/brand-manage.md)
