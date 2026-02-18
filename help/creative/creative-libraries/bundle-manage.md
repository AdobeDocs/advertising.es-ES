---
title: Administrar paquetes creativos
description: Aprenda a administrar y utilizar grupos de creativos.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: 0bcbd20437457ddafbd23969fbc48093e050ca2f
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 0%

---

# Administrar paquetes creativos

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

Los paquetes son grupos de creativos que se pueden añadir a una experiencia como una unidad. Después de crear un contenedor de paquetes, puede adjuntar elementos creativos al paquete. Los paquetes de visualización estándar solo pueden contener anuncios de visualización estándar, los paquetes de vídeo estándar solo pueden contener anuncios de vídeo estándar, los paquetes de visualización dinámica solo pueden contener anuncios de visualización dinámicos y los paquetes de vídeo dinámico solo pueden contener anuncios de vídeo dinámicos. Puede anular las páginas de aterrizaje, las etiquetas de seguimiento de impresiones y las etiquetas de seguimiento de clics de todos los creativos de un paquete asignado a una experiencia desde el árbol de decisión de experiencias, sin afectar a los creativos de base.

[!DNL Creative] rota entre los elementos creativos del paquete según se ha especificado para cada experiencia a la que se ha asignado el paquete. Opcionalmente, puede permitir que [!DNL Creative] optimice los elementos publicitarios para cualquier experiencia en función del rendimiento mediante la rotación algorítmica de anuncios, que funciona con [!DNL Adobe AI].

Para habilitar la optimización de los elementos de publicidad en los paquetes de una experiencia publicitaria, cada paquete puede incluir solo uno de cada combinación \[tamaño creativo o duración + idioma\]. Por ejemplo, si un paquete incluye un creativo de 250 x 250 con un idioma predeterminado de &quot;francés&quot;, no puede añadir un segundo creativo de 250 x 250 con un idioma predeterminado de &quot;francés&quot;. Si tiene varios creativos del mismo tamaño en el mismo idioma, añádalos por separado a la experiencia.

Los elementos creativos adjuntos a los paquetes siguen estando disponibles como elementos creativos individuales. Puede añadir un solo elemento creativo a varios paquetes. Si edita cualquier configuración de un elemento creativo que esté adjunto a un paquete, los cambios se propagarán al paquete. Sin embargo, para la experiencia siempre se utiliza cualquier página de aterrizaje personalizada, etiquetas de seguimiento de impresiones y etiquetas de seguimiento de clics configuradas para el creativo dentro de una experiencia.

<!-- multiselect only to duplicate and delete -->

## Crear un paquete para una biblioteca creativa

Puede adjuntar un elemento creativo a varios paquetes.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**.

1. Escriba un **[!UICONTROL Bundle Name]** único y **[!UICONTROL Bundle Type]:** *Pantalla estándar* (para creativos de pantalla estándar), *Visualización dinámica* (para creativos de pantalla dinámica), *Vídeo estándar* (para creativos de vídeo estándar) o *Dynamic Video* (para creativos de vídeo dinámico).

1. Haga clic en **[!UICONTROL Create]**.

## Enumerar los elementos creativos en un paquete

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Haga clic en la tarjeta o fila del paquete para ver todos los creativos del paquete.

## Paquetes duplicados

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Seleccione los paquetes que desea duplicar:

   * Para duplicar un solo paquete:

      * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre del paquete y, a continuación, haga clic en **[!UICONTROL Duplicate]**.

      * En la vista de tabla, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Duplicate]**.

   * Para duplicar uno o más paquetes, active la casilla de verificación de cada paquete que desee duplicar. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Duplicate].**

     Para seleccionar todas las filas, active la casilla de verificación global en la parte superior izquierda.

   Los nuevos paquetes reciben el nombre `<original name> (copy) # 1` (o el siguiente número de la secuencia). Por ejemplo, si crea dos duplicados de &quot;Paquete de prueba&quot;, los duplicados se denominarán &quot;Paquete de prueba (copia) # 1&quot; y &quot;Paquete de prueba (copia) # 2&quot;.

## Editar un nombre de paquete

Los cambios en un nombre de paquete se propagan por todas las experiencias asociadas.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Seleccione el paquete:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la biblioteca y, a continuación, haga clic en **[!UICONTROL Edit]**.

   * En la vista de tabla, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Edit]**.

1. Editar **[!UICONTROL Bundle Name]**.

   [!UICONTROL Bundle Name] debe ser único.

1. Haga clic en **[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## Adjuntar elementos creativos a un paquete

Puede adjuntar elementos creativos de visualización estándar existentes a un paquete de visualización estándar, elementos creativos de vídeo estándar a paquetes de vídeo estándar, elementos creativos de visualización dinámica a un paquete dinámico y elementos creativos de vídeo dinámico a un paquete de vídeo. Al adjuntar un elemento creativo a un paquete, este estará disponible en todas las experiencias a las que esté asignado el paquete. Cada paquete solo puede incluir una de cada combinación \[creative size or duration + language\].

>[!NOTE]
>
>También puede [adjuntar elementos creativos a paquetes desde las vistas Anuncios estándar y Anuncios dinámicos](creative-attach-detach-bundles.md).

### Adjuntar elementos creativos a un paquete desde la lista Paquetes

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Seleccione el paquete:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre del paquete y, a continuación, haga clic en **[!UICONTROL Attach Creatives]**.

   * En la vista de tabla, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Attach Creatives]**.

   Cada creativo apto para el tipo de paquete se muestra en el cuadro derecho. Los elementos creativos que ya están adjuntos al paquete se muestran, pero no se pueden seleccionar.

1. (Opcional) Cambie entre la vista de tabla predeterminada y una vista de tarjeta de los paquetes disponibles haciendo clic en ![Vista de tarjeta](/help/creative/assets/card-view-button.png "Vista de tarjeta") para abrir la vista de tarjeta o ![Vista de tabla/lista](/help/creative/assets/table-view-button.png "Vista de tabla") para volver a la vista de tabla.

1. En el cuadro derecho, active la casilla de verificación situada junto a cada elemento creativo que desee adjuntar al paquete y, a continuación, haga clic en **[!UICONTROL Attach Creative to Bundle]**.

### Adjunte elementos creativos a un paquete de la lista de elementos creativos del paquete

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Haga clic en la tarjeta o fila del paquete para ver todos los creativos del paquete.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Attach Creatives]**.

1. En el panel derecho, active la casilla de verificación de cada elemento creativo que desee adjuntar.

1. Haga clic en **[!UICONTROL Attach Creatives to Bundle]**.

## Desasociar creativos de un paquete {#bundle-detach-creatives}

Al separar un elemento creativo de un paquete, se elimina la asociación entre ambos, de modo que el elemento creativo ya no se utilice para experiencias dirigidas al paquete.

Al separar un creativo del paquete, no se elimina el creativo de la pestaña Creativos de la biblioteca creativa.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Haga clic en la tarjeta o fila del paquete para ver todos los creativos del paquete.

1. Seleccione los elementos creativos que desea desasociar del paquete:

   * Para separar un solo elemento creativo:

      * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre del creativo y, a continuación, haga clic en **[!UICONTROL Detach]**.

      * En la vista de tabla, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Detach]**.

   * Para separar uno o más creativos, marque la casilla de verificación de cada creativo que desee separar. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Detach]**.

     Para seleccionar todas las filas, active la casilla de verificación global en la parte superior izquierda.

## Previsualización de un solo elemento creativo en un paquete

Puede obtener una vista previa de un elemento creativo tal y como lo verán los visualizadores, incluidos los hipervínculos.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Haga clic en la tarjeta o fila del paquete para ver todos los creativos del paquete.

1. Seleccione el creativo:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre del creativo y, a continuación, haga clic en **[!UICONTROL Preview]**.

   * En la vista de tabla, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Preview]**.

1. (Opcional) Para cambiar el tamaño de la imagen en la pantalla, seleccione una opción en la lista **[!UICONTROL Zoom]**, del 10% al 100% del tamaño de la imagen.

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. (Opcional) Para abrir la página de aterrizaje del creativo, haga clic en el creativo.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Opcional) Para descargar el elemento creativo, haga clic en ![Descargar](/help/creative/assets/download.png "Descargar").

   El archivo se descarga según el procedimiento normal del explorador.

## Previsualizar todos los creativos de un paquete

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Seleccione el paquete:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre del paquete y, a continuación, haga clic en **[!UICONTROL Preview]**.

   * En la vista de tabla, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Preview]**.

1. (Opcional) Para filtrar los elementos creativos por idioma, seleccione una opción en la lista **[!UICONTROL Language]** y, a continuación, haga clic en **[!UICONTROL Preview]** en la parte superior derecha de la vista previa.

1. (Opcional) Para filtrar los elementos creativos por tamaño, seleccione una opción en la lista **[!UICONTROL Size]** y, a continuación, haga clic en **[!UICONTROL Preview]** en la parte superior derecha de la vista previa.

1. (Opcional) Para cambiar el tamaño de las imágenes dentro de la pantalla, seleccione una opción en la lista **[!UICONTROL Zoom]**, del 10% al 100% del tamaño de la imagen.

1. (Opcional) Para abrir la página de aterrizaje de un elemento creativo, haga clic en el elemento creativo.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Opcional) Compartir una URL de demostración para que otras personas sin iniciar sesión en [!DNL Creative] puedan obtener una vista previa de los elementos creativos:

   1. Haga clic en ![Compartir](/help/creative/assets/share.png "Compartir") en la parte superior derecha de la vista previa.

   1. En el cuadro de diálogo [!UICONTROL Share Demo URL], haga clic en **[!UICONTROL Copy]** para copiar la dirección URL en el portapapeles de modo que pueda compartirla con otra persona.

<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## Eliminar paquetes

Puede eliminar paquetes que no estén asignados a una experiencia [live](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses). Si se asigna un paquete a una experiencia en directo, [elimine el paquete del árbol de decisión](/help/creative/experiences/experience-target-node-delete.md) de la experiencia antes de continuar.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Haga clic en el nombre de la biblioteca.

1. Haga clic en la ficha **[!UICONTROL Bundles]**.

1. Seleccione los paquetes que desea eliminar:

   * Para eliminar un solo paquete:

      * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre del paquete y, a continuación, haga clic en **[!UICONTROL Delete]**.

      * En la vista de tabla, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Delete]**.

   * Para eliminar uno o varios paquetes, active la casilla de verificación de cada paquete que desee eliminar. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete].**

     Para seleccionar todas las filas, active la casilla de verificación global en la parte superior izquierda.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Previsualizar un elemento creativo](/help/creative/creative-libraries/creative-preview.md)
>* [Agregar elementos creativos estándar a una biblioteca creativa](/help/creative/creative-libraries/creative-add-standard.md)
>* [Administrar bibliotecas creativas](/help/creative/creative-libraries/creative-library-manage.md)
>* [Acerca de sus bibliotecas creativas](/help/creative/creative-libraries/creative-libraries-about.md)
