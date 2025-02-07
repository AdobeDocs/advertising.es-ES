---
title: Editar una experiencia con segmentación en árbol de decisiones
description: Obtenga información sobre cómo editar la configuración de una experiencia publicitaria de destino mediante un árbol de decisiones.
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Editar una experiencia con segmentación en árbol de decisiones

*Beta cerrada*

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir experiencias específicas.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Edit]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Edit]**.

1. Editar la [configuración general de la experiencia](experience-settings-targeting.md).

1. (Opcional) Para editar el árbol de decisión, haga clic en **[!UICONTROL Decision Tree]** en la esquina superior derecha y, a continuación, siga uno de estos procedimientos:

   * ([Procesando](experience-about.md#experience-statuses) experiencias) Realice una de las siguientes acciones:

      * Para descartar los cambios existentes y no publicados en la experiencia en directo, haga clic en **[!UICONTROL Discard and start again]**.

      * Para mantener los cambios existentes sin publicar, haga clic en **[!UICONTROL Continue editing draft]**.

      * Para editar los detalles de la experiencia, haga clic en **[!UICONTROL Edit Experience Details]**.

   * (Opcional) Cambie la configuración de vista del árbol de decisión.

     La configuración se guardará hasta que cierre la sesión.

   * Para acercar o alejar, mueva el control deslizante.

   * Cambie entre ver una lista vertical y una lista horizontal haciendo clic en ![Ver como árbol vertical](/help/creative/assets/tree-vertical.png "Ver como árbol vertical") o ![Ver como árbol horizontal](/help/creative/assets/tree-horizontal.png "Ver como árbol horizontal"), respectivamente.

   * (Opcional) Cambie los targets de anuncios y los elementos creativos correspondientes de cualquiera de las siguientes maneras:

      * Destinos:

        *[Agregue un nodo de destino al nivel final](experience-target-node-add-final.md) de una experiencia.

         * [Insertar un nodo de destino entre nodos](experience-target-node-add-inner.md).

         * [Agregar un nodo de destino secundario entre nodos](experience-target-node-add-sibling.md).

         * [Copie nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md).

      * Paquetes creativos:

         * [Asignar y cancelar la asignación de elementos creativos a un nodo final](experience-assign-creative-bundles.md).

           Si no asigna al menos un paquete a cada nodo final, puede optar por utilizar los elementos creativos predeterminados para cada nodo no asignado al guardar la experiencia. Para que se publique, la experiencia debe tener asignados paquetes o utilizar los elementos creativos predeterminados para todos los anuncios creados a partir de ella.

         * [Personalice las direcciones URL de seguimiento para los creativos en los paquetes asignados](experience-tracking-urls-targeting.md).

         * [Personalizar la optimización y programación creativas](experience-optimization-scheduling-targeting.md) para los paquetes asignados.

1. Haga clic en **[!UICONTROL Save]** y, a continuación, haga lo siguiente.

   * (Si cada nodo del nivel más bajo incluye al menos un paquete creativo) Haga clic en **[!UICONTROL OK]**.

   * (Si cada nodo del nivel más bajo no incluye al menos un paquete creativo) Realice una de las siguientes acciones:

      * Para guardar la experiencia sin todos los paquetes creativos necesarios, haga clic en **[!UICONTROL Save as Draft]**.

        No puedes crear una etiqueta de anuncio para una experiencia de [borrador](experience-about.md#experience-statuses).

      * Para asignar el elemento creativo predeterminado a cada destino al que aún no se le haya asignado un paquete creativo, haga clic en **[!UICONTROL Assign Default Creatives]**. Después de revisar el árbol actualizado con los elementos creativos predeterminados asignados, haga clic en **[!UICONTROL Save]** y **[!UICONTROL OK]**.

      * Para continuar editando el árbol de decisión, haga clic en **[!UICONTROL Continue Edit]**.

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
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
