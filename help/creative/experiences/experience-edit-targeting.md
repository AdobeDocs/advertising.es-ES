---
title: Editar una experiencia con segmentación en árbol de decisiones
description: Aprenda a editar una experiencia de publicidad segmentada mediante el editor de árboles de decisiones manual o controlado por IA.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%
---
# Editar una experiencia con segmentación en árbol de decisiones

El editor controlado por IA (Beta) se abre de forma predeterminada para las experiencias con segmentación. Puede trabajar con el agente de IA, editar el lienzo directamente o abrir el editor manual existente.

## Abra la experiencia {#experience-open}

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir experiencias específicas.

1. Realice una de las siguientes acciones:

   * Para abrir el editor controlado por IA:

     * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Edit]**.

     * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Edit]**.

   * Para abrir el editor manual:

     * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * Dentro del editor controlado por IA,

## Edite con el editor controlado por IA (Beta) {#ai-editor}

1. [Abrir la experiencia](#experience-open).

1. Describa los cambios de objetivo que desee en la conversación. Identifique la rama afectada por sus destinos o, cuando se muestre en el lienzo, por su ID de nodo.

1. Revise el árbol actualizado y describa cualquier cambio adicional. Espere a que el asistente finalice el procesamiento antes de interactuar con el lienzo.

1. (Opcional) Realice cambios directamente en el lienzo:

   * [Agregar un destino de nivel final](experience-target-node-add-final.md#ai-editor), [insertar un nivel de destino](experience-target-node-add-inner.md#ai-editor) o [agregar un destino secundario](experience-target-node-add-sibling.md#ai-editor).

   * Edite los criterios de un objetivo haciendo clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]** junto al objetivo, cambiando los valores y, a continuación, haciendo clic en **[!UICONTROL Edit Node]**.

   * [Copiar nodos secundarios y elementos creativos](experience-target-node-copy.md#ai-editor) o [eliminar un nodo](experience-target-node-delete.md#ai-editor).

   * [Asignar o anular la asignación de paquetes creativos](experience-assign-creative-bundles.md#ai-editor).

   * [Personalizar la programación y la optimización creativas](experience-optimization-scheduling-targeting.md) o [URL de seguimiento](experience-tracking-urls-targeting.md#ai-editor).

1. [Guarde la experiencia](#save).

## Edición mediante el editor manual {#manual-editor}

1. [Abrir la experiencia](#experience-open).

1. (Experiencias con estado `[processing](experience-about.md#experience-statuses)`) Si se le solicita un borrador existente sin publicar, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Continue editing draft]** para revisar y seguir editando el borrador.

   * Haga clic en **[!UICONTROL Discard and start again]** para descartar el borrador y comenzar desde la versión activa.

   * Haga clic en **[!UICONTROL Cancel this edit]** para detener la edición.

1. (Opcional) Ajuste el control deslizante del zoom o haga clic en ![Ver como árbol vertical](/help/creative/assets/tree-vertical.png "Ver como árbol vertical") o ![Ver como árbol horizontal](/help/creative/assets/tree-horizontal.png "Ver como árbol horizontal") para cambiar la orientación.

   La configuración de la vista se guardará hasta que cierre la sesión.

1. Cambie los objetivos y los elementos creativos según sea necesario:

   * [Agregar un destino de nivel final](experience-target-node-add-final.md#manual-editor), [insertar un destino entre nodos](experience-target-node-add-inner.md#manual-editor) o [agregar un destino secundario](experience-target-node-add-sibling.md#manual-editor).

   * [Copiar nodos secundarios y elementos creativos](experience-target-node-copy.md#manual-editor) o [eliminar un nodo](experience-target-node-delete.md#manual-editor).

   * [Asignar o anular la asignación de paquetes creativos](experience-assign-creative-bundles.md#manual-editor).

   * [Personalizar la programación y la optimización creativas](experience-optimization-scheduling-targeting.md) o [URL de seguimiento](experience-tracking-urls-targeting.md#manual-editor).

1. [Guarde la experiencia](#save).

## Cambie de editor o edite la configuración de la experiencia {#switch-editors}

>[!IMPORTANT]
>
>Antes de salir del editor controlado por IA, guarde los cambios de árbol que desee conservar. Cambiar al editor manual o al formulario de experiencia no transfiere los cambios no guardados.

* **Editor controlado por IA a editor manual:** Haga clic en **[!UICONTROL Manual Decision Tree]**. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Yes]** para descartar los cambios no guardados y abrir el editor manual, o en **[!UICONTROL No]** para permanecer.

* **Editor controlado por IA para la configuración general:** Haga clic en **[!UICONTROL Experience Form]** y, a continuación, haga clic en **[!UICONTROL Yes]** para descartar los cambios de árbol no guardados y abrir el formulario. Edite la [configuración general de la experiencia](experience-settings-targeting.md) y, a continuación, haga clic en **[!UICONTROL Save]**.

* **Editor manual para la configuración general:** Guarde los cambios de árbol que desee conservar y, a continuación, haga clic en **[!UICONTROL Experience Form]**. Edite la [configuración general de la experiencia](experience-settings-targeting.md) y, a continuación, haga clic en **[!UICONTROL Save]**.

* **Configuración general del editor controlado por IA:** Haga clic en **[!UICONTROL Decision Tree]**. Guardar cambios en la configuración general de una experiencia segmentada también abre el editor controlado por IA.

* **Editor manual en editor controlado por IA:** guarde los cambios del árbol, vuelva a la vista [!UICONTROL Experiences] y seleccione **[!UICONTROL Edit]** para la experiencia.

Para salir del editor controlado por IA sin abrir otro editor, haga clic en **[!UICONTROL Cancel]**. Haga clic en **[!UICONTROL Yes]** para descartar los cambios de árbol no guardados o en **[!UICONTROL No]** para continuar editando.

## Guarde la experiencia {#save}

Los siguientes pasos se aplican a ambos editores.

{{$include /help/_includes/experience-save.md}}

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
>* [Ver el registro de cambios de una experiencia](/help/creative/experiences/experience-view-change-log.md)
