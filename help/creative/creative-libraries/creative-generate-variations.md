---
title: Generar variaciones de creativos flexibles de HTML5
description: Aprenda a generar y guardar variaciones asistidas por IA de creativos flexibles de HTML5 desde una biblioteca creativa.
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 1cc477f531051d94ea88eaae0a4fb83918e95ea5
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%
---
# Generar variaciones de creativos flexibles de HTML5

Use [!UICONTROL Ad Variations Generator] para crear nuevas variaciones de un elemento creativo flexible de HTML5 existente. El asistente de IA genera y refina titulares, CTA, imágenes, colores y mucho más, y puede crear nuevas variantes de tamaño en una sola sesión. Guarde las variaciones resultantes como nuevos anuncios estándar en la biblioteca creativa.

>[!NOTE]
>
>También puede generar variaciones de anuncios a partir de [!UICONTROL Creative Studio]. Ambos puntos de entrada abren el mismo [!UICONTROL Ad Variations Generator]. Consulte &quot;[Generar variaciones de anuncios para un anuncio estándar en Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations)&quot; para el otro punto de entrada.

## Disponibilidad {#availability}

La acción **[!UICONTROL Generate Variations]** está disponible para los elementos creativos flexibles de HTML5, incluidos los basados en plantillas del sistema, en la nueva interfaz de usuario de [!UICONTROL Creative Libraries]. No está disponible para otros tipos creativos, incluidos los dinámicos.

La acción se desactiva cuando el creativo no tiene la referencia de plantilla de anuncio principal interna requerida por el generador. Esta referencia no es una configuración que se pueda editar; cargar o reemplazar un archivo en la ficha **[!UICONTROL Template]** del creativo no la establece explícitamente.

## Abra el Generador de variaciones de anuncios {#open-generator}

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Abra la biblioteca mediante cualquiera de estos métodos:

   * Haga clic en el nombre de la biblioteca.
   * Junto al nombre de la biblioteca, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. En la ficha **[!UICONTROL Creatives]**, haga clic en **[!UICONTROL ...]** junto al nombre flexible del elemento creativo de HTML5 y, a continuación, haga clic en **[!UICONTROL Generate Variations]**.

   [!UICONTROL Ad Variations Generator] se abre con el contenido del elemento creativo seleccionado. El lienzo muestra la sección **[!UICONTROL Template Sizes]** con los formatos de anuncio disponibles en la plantilla y una sección **[!UICONTROL Ad Concepts]** en la que aparecerá el contenido generado.

## Generar y refinar variaciones {#generate-variations}

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
      >El asistente de IA puede generar y modificar texto (titulares, subtitulares, CTA, texto independiente), intercambiar imágenes de fondo, aplicar colores de marca, cambiar versiones de logotipos y crear nuevas plantillas de tamaño. No puede cambiar la estructura de la plantilla: posiciones de los elementos, diseño, espaciado, relleno, familia de fuentes, tamaño de fuente o bordes. Realice cambios estructurales en el editor de plantillas antes de iniciar la sesión. Consulte [Editar una plantilla](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template).

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

## Guarde las variaciones {#save-variations}

1. Cuando esté satisfecho con los conceptos generados, haga clic en **[!UICONTROL Save Standard Ads]** en el encabezado.

   El botón está desactivado hasta que exista al menos un concepto.

1. En el cuadro de diálogo **[!UICONTROL Save Standard Ads]**, revise la siguiente configuración y haga clic en **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** El anunciante asociado con la biblioteca creativa de origen. No puede cambiar este valor.

   **[!UICONTROL Creative Library]:** Biblioteca creativa de origen en la que se guardan los nuevos anuncios. No puede cambiar este valor.

   **[!UICONTROL Attach to Bundles]:** (opcional) cuando está habilitada, los elementos creativos guardados se adjuntan a uno o varios paquetes. Para cada variación de anuncio, seleccione un paquete o introduzca un nuevo nombre de paquete.

   **\[Configuración para cada anuncio\]:** Para cada variación de anuncio, puede ver y, opcionalmente, cambiar **[!UICONTROL Name]**, **[!UICONTROL Language]** y la URL de pulsaciones para cada etiqueta de clic.

   Vuelve a la biblioteca creativa.

>[!MORELIKETHIS]
>
>* [Editar elementos creativos estándar](creative-edit-standard.md)
>* [Administrar anuncios estándar en Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [Administrar perfiles de marca en Advertising Creative](/help/creative/brands/brand-manage.md)
>* [Metadatos de C2PA en [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-content-credentials.md)
