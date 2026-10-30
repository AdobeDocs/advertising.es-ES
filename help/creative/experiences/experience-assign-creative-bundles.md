---
title: Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia
description: Aprenda a asignar elementos creativos a cada destinatario en sus experiencias publicitarias.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
TQID: 'https://experienceleague.adobe.com/HqTq2fiJadk-QIBwYkOxC2N9sTMm29LIXRzSubPuv9M'
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
source-wordcount: '453'
ht-degree: 0%
---
# Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia

*Solo experiencias con direccionamiento en árbol de decisiones*

Puede asignar paquetes creativos a un nodo de destino en el nivel inferior de un árbol de decisión de experiencias. En el caso de las experiencias para las que no ha configurado objetivos, el nivel inferior se encuentra en &quot;Todo&quot;.

Para las experiencias de publicidad estándar, solo puede asignar paquetes creativos estándar. Para las experiencias de publicidad dinámica, solo puede asignar paquetes creativos dinámicos.

>[!NOTE]
>
>Si no asigna al menos un paquete creativo a cada nodo final, puede optar por usar los elementos creativos predeterminados para cada nodo no asignado al [guardar la experiencia](experience-create-targeting.md). Para publicar una experiencia, debe asignar paquetes o utilizar los elementos creativos predeterminados para cada nodo final.

## Uso del editor controlado por IA (Beta) {#ai-editor}

Mientras [crea](experience-create-targeting.md#ai-editor) o [edita](experience-edit-targeting.md#ai-editor) la experiencia, use los controles de lienzo:

1. Realice una de las siguientes acciones:

   * Para un nodo final sin paquetes, haga clic en **[!UICONTROL Assign Bundles]**.

   * Para un nodo con paquetes existentes, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** en su nodo de hoja creativa.

1. En la ficha **[!UICONTROL Assign Bundles]**, active la casilla de verificación situada junto a cada paquete que desee asignar y anule la selección de la casilla de verificación situada junto a cada paquete que desee anular la asignación.

   Solo se enumeran los paquetes del tipo relevante para la experiencia (estándar o dinámica).

1. (Opcional) Abra la ficha **[!UICONTROL Creative optimisation]** para [personalizar la rotación y la programación](experience-optimization-scheduling-targeting.md).

1. Haga clic en **[!UICONTROL Save]** en el cuadro de diálogo para actualizar el árbol de trabajo.

1. (Opcional) [Personalice las direcciones URL de seguimiento](experience-tracking-urls-targeting.md#ai-editor).

1. [Guarde la experiencia](#save) del encabezado del árbol para mantener los cambios.

## Uso del editor manual {#manual-editor}

[Abra el editor manual](experience-edit-targeting.md#experience-open) antes de seguir estos pasos.

1. Realice una de las siguientes acciones:

   * (Nodos finales sin elementos creativos) En el nodo, haga clic en **[!UICONTROL Assign Bundles]**.

   * (Nodos con elementos creativos existentes) Mantenga el cursor sobre el cuadro del paquete creativo debajo del nodo de destino y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Seleccione la casilla de verificación situada junto a cada paquete para asignarlo al nodo de destino y anule la selección de la casilla de verificación situada junto a cada paquete para anular la asignación.

   Solo se muestran los paquetes del tipo de paquete relevante para la experiencia (estándar o dinámica).

1. Haga clic en **[!UICONTROL Save]**.

1. (Opcional) [Personalice la optimización y la programación creativas](experience-optimization-scheduling-targeting.md) para los paquetes asignados.

1. (Opcional) [Personalice las direcciones URL de seguimiento para los creativos en los paquetes asignados](experience-tracking-urls-targeting.md).

## Guarde la experiencia {#save}

Los siguientes pasos se aplican a ambos editores. Al guardar el cuadro de diálogo del paquete solo, no se guarda ni publica la experiencia.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Agregar un nodo de destino al nivel final](experience-target-node-add-final.md)
>* [Insertar un nodo de destino entre nodos](experience-target-node-add-inner.md)
>* [Agregar un nodo de destino secundario entre nodos](experience-target-node-add-sibling.md)
>* [Copiar nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md)
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
>* [Configuración de experiencia de destino](experience-settings-targeting.md)
>* [Exportar e implementar una etiqueta de experiencia de anuncio para una experiencia en vivo](experience-tag-export.md)
>* [Ver el registro de cambios de una experiencia](/help/creative/experiences/experience-view-change-log.md)
