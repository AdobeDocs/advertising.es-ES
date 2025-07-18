---
title: Crear una experiencia con segmentación del árbol de decisiones
description: Obtenga información sobre cómo crear una experiencia de publicidad segmentada mediante un árbol de decisiones.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: e79becc860143b749ec96134e7b224649686c672
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# Crear una experiencia con segmentación del árbol de decisiones

*Beta cerrada*

Cree una experiencia de anuncio segmentada mediante un árbol de decisiones. Cada experiencia utiliza anuncios de una sola biblioteca creativa.

>[!NOTE]
>
>* Una vez creada una experiencia de destino, no se puede cambiar posteriormente a una experiencia de destino, que utiliza un flujo de trabajo diferente.
>* Asegúrese de que las experiencias publicitarias incluyan una segmentación compatible con las campañas en las que la va a implementar. El comportamiento de direccionamiento jerárquico puede variar según DSP. Al cargar una etiqueta de experiencia de anuncio en Advertising DSP y adjuntarla a una ubicación, el objetivo de nivel de anuncio se aplica sobre el objetivo de nivel de ubicación (no en lugar de). Por ejemplo, si una ubicación se dirige a usuarios de Australia y un anuncio a usuarios de Japón, el anuncio se dirigirá a la rama &quot;Todos los demás&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Haga clic en **[!UICONTROL Create New Experience]**.

1. Escriba la [configuración general de la experiencia](experience-settings-targeting.md).

1. Haga clic en **[!UICONTROL Create]**.

1. En el árbol de decisión, haga lo siguiente:

   1. (Opcional) Cambie la configuración de vista del árbol de decisión.

      La configuración se guardará hasta que cierre la sesión.

      * Para acercar o alejar, mueva el control deslizante.

      * Cambie entre ver una lista vertical y una lista horizontal haciendo clic en ![Ver como árbol vertical](/help/creative/assets/tree-vertical.png "Ver como árbol vertical") o ![Ver como árbol horizontal](/help/creative/assets/tree-horizontal.png "Ver como árbol horizontal"), respectivamente.

   1. (Opcional) Configure los targets de anuncios y los elementos creativos correspondientes de cualquiera de las siguientes maneras:

      * Destinos:

         * [Agregar un nodo de destino al nivel final](experience-target-node-add-final.md).

         * [Insertar un nodo de destino entre nodos](experience-target-node-add-inner.md).

         * [Agregar un nodo de destino secundario entre nodos](experience-target-node-add-sibling.md).

         * [Copie nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md).

      * Paquetes de Creative:

         * [Asignar y cancelar la asignación de elementos creativos a un nodo final](experience-assign-creative-bundles.md).

           Si no asigna al menos un paquete a cada nodo final, puede optar por utilizar los elementos creativos predeterminados para cada nodo no asignado al guardar la experiencia. Para publicar una experiencia, debe asignar paquetes o utilizar los elementos creativos predeterminados para cada nodo final.

         * [Personalice las direcciones URL de seguimiento para los creativos en los paquetes asignados](experience-tracking-urls-targeting.md).

         * [Personalizar la optimización y programación creativas](experience-optimization-scheduling-targeting.md) para los paquetes asignados.

1. (Opcional) Cambie entre el árbol de decisión y la configuración general:

   * Para abrir la configuración general desde el árbol de decisión, haga clic en **[!UICONTROL Experience Form]** en la esquina superior derecha.

   * Para abrir el árbol de decisión desde la configuración general, haga clic en **[!UICONTROL Decision Tree]** en la esquina superior derecha.

1. Haga clic en **[!UICONTROL Save]** y, a continuación, haga lo siguiente.

   * (Si cada nodo del nivel más bajo incluye al menos un paquete creativo) Haga clic en **[!UICONTROL OK]**.

   * (Si cada nodo del nivel más bajo no incluye al menos un paquete creativo) Realice una de las siguientes acciones:

      * Para guardar la experiencia sin todos los paquetes creativos necesarios, haga clic en **[!UICONTROL Save as Draft]**.

        No puedes crear una etiqueta de anuncio para una experiencia de [borrador](experience-about.md#experience-statuses).

      * Para asignar el elemento creativo predeterminado a cada destino al que aún no se le haya asignado un paquete creativo, haga clic en **[!UICONTROL Assign Default Creatives]**. Después de revisar el árbol actualizado con los elementos creativos predeterminados asignados, haga clic en **[!UICONTROL Save]** y **[!UICONTROL OK]**.

      * Para continuar editando el árbol de decisión, haga clic en **[!UICONTROL Continue Edit]**.

Cuando la experiencia está activa, [!DNL Creative] crea automáticamente una etiqueta de anuncio para cada tamaño creativo o duración de vídeo aplicable. A continuación, puede [exportar una etiqueta de anuncio e implementarla en un DSP](/help/creative/experiences/experience-tag-export.md).

Para las experiencias de anuncios de vídeo, Adobe Advertising DSP transcodifica automáticamente los creativos de vídeo como etiquetas VAST 2.0 para que pueda previsualizarlos. Opcionalmente, puede [aplicar la transcodificación para un DSP diferente](experience-tag-video-transcoding.md) a cualquier etiqueta de experiencia de anuncio de vídeo.

>[!MORELIKETHIS]
>
>* [Configuración de experiencia de destino](experience-settings-targeting.md)
>* [Agregar un nodo de destino al nivel final](experience-target-node-add-final.md)
>* [Insertar un nodo de destino entre nodos](experience-target-node-add-inner.md)
>* [Agregar un nodo de destino secundario entre nodos](experience-target-node-add-sibling.md)
>* [Copiar nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md)
>* [Asignar elementos creativos a un nodo final](experience-assign-creative-bundles.md)
>* [Personalizar las direcciones URL de seguimiento para los creativos en los paquetes asignados](experience-tracking-urls-targeting.md)
>* [Personalizar programación y optimización creativa](experience-optimization-scheduling-targeting.md)
>* [Exportar e implementar una etiqueta de experiencia de anuncio para una experiencia en vivo](/help/creative/experiences/experience-tag-export.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
