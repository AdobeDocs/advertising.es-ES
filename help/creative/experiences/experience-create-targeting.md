---
title: Crear una experiencia con segmentación del árbol de decisiones
description: Aprenda a crear una experiencia publicitaria segmentada mediante el editor de árboles de decisiones manual o controlado por IA.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
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
source-wordcount: '715'
ht-degree: 0%
---
# Crear una experiencia con segmentación del árbol de decisiones

Cree una experiencia de anuncio segmentada mediante un árbol de decisiones. Cada experiencia utiliza anuncios de una sola biblioteca creativa.

El editor controlado por IA (Beta) se abre de forma predeterminada. Puede configurar el árbol a través del agente de IA o editar su lienzo directamente. También puede cambiar al editor manual existente.

>[!NOTE]
>
>* Una vez creada una experiencia de destino, no se puede cambiar posteriormente a una experiencia de destino, que utiliza un flujo de trabajo diferente.
>* Asegúrese de que las experiencias publicitarias incluyan una segmentación compatible con las campañas en las que la va a implementar. El comportamiento de direccionamiento jerárquico puede variar según DSP. Al cargar una etiqueta de experiencia de anuncio en Advertising DSP y adjuntarla a una ubicación, el objetivo de nivel de anuncio se aplica sobre el objetivo de nivel de ubicación (no en lugar de). Por ejemplo, si una ubicación se dirige a usuarios de Australia y un anuncio a usuarios de Japón, el anuncio se dirigirá a la rama &quot;Todos los demás&quot;.

## Crear la experiencia

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Haga clic en **[!UICONTROL Create New Experience]**.

1. Escriba la [configuración general de la experiencia](experience-settings-targeting.md), con **[!UICONTROL Targeting]** habilitado.

1. Haga clic en **[!UICONTROL Create]**.

   El editor del árbol de decisiones impulsado por IA se abre para la nueva experiencia.

1. Configure el árbol mediante cualquiera de los siguientes procedimientos.

## Configure el árbol con el editor controlado por IA (Beta) {#ai-editor}

1. En la conversación, describa la estructura de segmentación que desee, incluidos los criterios para cada rama y cómo gestionar los visualizadores que no coinciden con un objetivo especificado.

1. Revise el árbol en el lienzo. Para solicitar cambios, descríbalos en la conversación. Espere a que el asistente finalice el procesamiento antes de interactuar con el lienzo.

1. (Opcional) Refine el árbol directamente en el lienzo:

   * [Agregar un destino de nivel final](experience-target-node-add-final.md#ai-editor), [insertar un nivel de destino](experience-target-node-add-inner.md#ai-editor) o [agregar un destino secundario](experience-target-node-add-sibling.md#ai-editor).

   * [Copiar nodos secundarios y elementos creativos](experience-target-node-copy.md#ai-editor) o [eliminar un nodo](experience-target-node-delete.md#ai-editor).

1. [Asigne paquetes creativos a los nodos finales](experience-assign-creative-bundles.md#ai-editor) y, opcionalmente, [personalice la optimización y la programación creativas](experience-optimization-scheduling-targeting.md) y [las direcciones URL de seguimiento](experience-tracking-urls-targeting.md#ai-editor).

   Para publicar la experiencia, debe asignar paquetes a cada nodo final o utilizar los elementos creativos predeterminados de la experiencia. Al guardar, puede asignar valores predeterminados a nodos sin asignar.

1. (Opcional) Edite la configuración general de la experiencia:

   1. Para guardar los cambios de árbol que desee conservar, haga clic en **[!UICONTROL Save]**.

   1. Haga clic en **[!UICONTROL Experience Form]** y, a continuación, haga clic en **[!UICONTROL Yes]** para descartar los cambios de árbol no guardados y abrir el formulario.

   1. Edite la [configuración general de la experiencia](experience-settings-targeting.md) y, a continuación, haga clic en **[!UICONTROL Save]**.

      Se abre el editor controlado por IA.

1. [Guarde la experiencia](#save).

## Configure el árbol con el editor manual {#manual-editor}

1. En el editor controlado por IA, haga clic en **[!UICONTROL Manual Decision Tree]** y, a continuación, haga clic en **[!UICONTROL Yes]** para dejar el editor controlado por IA.

   Guarde los cambios del editor de IA que desee conservar antes de cambiar. Al confirmar el conmutador, se descartan los cambios de árbol no guardados.

1. (Opcional) Cambie la configuración de la vista:

   * Para acercar o alejar, mueva el control deslizante.

   * Cambie entre vistas verticales y horizontales haciendo clic en ![Ver como árbol vertical](/help/creative/assets/tree-vertical.png "Ver como árbol vertical") o ![Ver como árbol horizontal](/help/creative/assets/tree-horizontal.png "Ver como árbol horizontal").

   La configuración de la vista se guardará hasta que cierre la sesión.

1. Configure los objetivos del anuncio y los elementos creativos correspondientes:

   * [Agregar un destino de nivel final](experience-target-node-add-final.md#manual-editor), [insertar un destino entre nodos](experience-target-node-add-inner.md#manual-editor) o [agregar un destino secundario](experience-target-node-add-sibling.md#manual-editor).

   * [Copiar nodos secundarios y elementos creativos](experience-target-node-copy.md#manual-editor) o [eliminar un nodo](experience-target-node-delete.md#manual-editor).

   * [Asigne paquetes creativos](experience-assign-creative-bundles.md#manual-editor) y, opcionalmente, [personalice la optimización y la programación creativas](experience-optimization-scheduling-targeting.md) y [las direcciones URL de seguimiento](experience-tracking-urls-targeting.md#manual-editor).

1. (Opcional) Para editar la configuración general de la experiencia, haga clic en **[!UICONTROL Experience Form]** y edite la [configuración general de la experiencia](experience-settings-targeting.md).

1. [Guarde la experiencia](#save).

## Guarde la experiencia {#save}

Los siguientes pasos se aplican a ambos editores.

{{$include /help/_includes/experience-save.md}}

## Etiquetas de anuncios y transcodificación de vídeo para experiencias guardadas

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
>* [Ver el registro de cambios de una experiencia](/help/creative/experiences/experience-view-change-log.md)
