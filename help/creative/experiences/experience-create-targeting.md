---
title: Crear una experiencia con la orientación del árbol de decisiones
description: Aprende a crear una experiencia publicitaria orientada mediante un árbol de decisiones.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: 2cf156702b44fe01d217f0f3ca4893a5af64e95f
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# Crear una experiencia con segmentación del árbol de decisiones

Crea una experiencia publicitaria orientada mediante un árbol de decisiones. Cada experiencia utiliza anuncios de una única biblioteca creativa.

>[!NOTE]
>
>* Una vez que haya creado una experiencia específica, no podrá cambiarla posteriormente a una experiencia no específica, que utiliza un flujo de trabajo diferente.
>* Asegúrate de que tus experiencias publicitarias incluyan una orientación que sea compatible con las campañas en las que vas a implementarla. El comportamiento de la orientación jerárquica puede variar en función del DSP. Cuando cargas una etiqueta de experiencia publicitaria en Advertising DSP y la adjuntas a una ubicación, la orientación a nivel de anuncio se aplica sobre la orientación a nivel de ubicación (no en lugar de hacerlo). Por ejemplo, si una ubicación está dirigida a usuarios de Australia y un anuncio está dirigido a usuarios de Japón, el anuncio estará dirigido a la rama &quot;Todos los demás&quot;.

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

         * [Inserte un nodo de destino entre nodos](experience-target-node-add-inner.md).

         * [Agregar un nodo de destino relacionado entre nodos](experience-target-node-add-sibling.md).

         * [Copie nodos secundarios y creativos en otro nodo del mismo nivel](experience-target-node-copy.md).

      * Paquetes de Creative:

         * [Asignar y cancelar la asignación de elementos creativos a un nodo final](experience-assign-creative-bundles.md).

           Si no asigna al menos un paquete a cada nodo final, puede optar por utilizar los recursos creativos predeterminados para cada nodo no asignado cuando guarde la experiencia. Para publicar una experiencia, debe asignar paquetes o utilizar las creatividades predeterminadas para cada nodo final.

         * [Personaliza la optimización y la programación creativas](experience-optimization-scheduling-targeting.md) de los paquetes asignados.

         * [Personaliza las direcciones URL de seguimiento para los creativos de los paquetes asignados](experience-tracking-urls-targeting.md).

1. (Opcional) Alterne entre el árbol de decisiones y la configuración general:

   * Para abrir la configuración general del árbol de decisiones, haga clic en **[!UICONTROL Experience Form]** en la parte superior derecha.

   * Para abrir el árbol de decisión desde la configuración general, haga clic en **[!UICONTROL Decision Tree]** en la esquina superior derecha.

1. Haga clic en **[!UICONTROL Save]** y, a continuación, haga lo siguiente.

   * (Si cada nodo del nivel más bajo incluye al menos un paquete creativo) Haga clic en **[!UICONTROL OK]**.

   * (Si cada nodo del nivel más bajo no incluye al menos un paquete creativo) Realice una de las siguientes acciones:

      * Para guardar la experiencia sin todos los paquetes creativos necesarios, haga clic en **[!UICONTROL Save as Draft]**.

        No puedes crear una etiqueta de anuncio para una experiencia de [borrador](experience-about.md#experience-statuses).

      * Para asignar el elemento creativo predeterminado a cada destino al que aún no se le haya asignado un paquete creativo, haga clic en **[!UICONTROL Assign Default Creatives]**. Después de revisar el árbol actualizado con los elementos creativos predeterminados asignados, haga clic en **[!UICONTROL Save]** y **[!UICONTROL OK]**.

      * Para continuar editando el árbol de decisión, haga clic en **[!UICONTROL Continue Edit]**.

Cuando la experiencia está activa, [!DNL Creative] crea automáticamente una etiqueta de anuncio para cada tamaño creativo o duración de vídeo aplicable. A continuación, puede [exportar una etiqueta de anuncio e implementarla en un DSP](/help/creative/experiences/experience-tag-export.md).

Para las experiencias de anuncios de vídeo, Adobe Advertising DSP transcodifica automáticamente los creativos de vídeo como etiquetas VAST 2.0 para que pueda previsualizarlos. Si lo deseas, puedes [aplicar la transcodificación de un DSP diferente](experience-tag-video-transcoding.md) a cualquier etiqueta de experiencia y vídeo.

>[!MORELIKETHIS]
>
>* [Configuración de la experiencia de destino](experience-settings-targeting.md)
>* [Agregar un nodo de destino al nivel final](experience-target-node-add-final.md)
>* [Insertar un nodo de destino entre nodos](experience-target-node-add-inner.md)
>* [Agregar un nodo de destino secundario entre nodos](experience-target-node-add-sibling.md)
>* [Copiar nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md)
>* [Asignar elementos creativos a un nodo final](experience-assign-creative-bundles.md)
>* [Personalizar las direcciones URL de seguimiento para los creativos en los paquetes asignados](experience-tracking-urls-targeting.md)
>* [Personalizar programación y optimización creativa](experience-optimization-scheduling-targeting.md)
>* [Exportar e implementar una etiqueta de experiencia de anuncio para una experiencia en vivo](/help/creative/experiences/experience-tag-export.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
>* [Ver el registro de cambios de una experiencia](/help/creative/experiences/experience-view-change-log.md)
