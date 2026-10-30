---
title: Personalizar las direcciones URL de seguimiento de una experiencia
description: Aprenda a personalizar las direcciones URL de seguimiento para cada elemento creativo de una experiencia con segmentación del árbol de decisiones.
feature: Creative Experiences
exl-id: ba3b15b4-116e-4caa-8ce1-4d2e488a6362
TQID: 'https://experienceleague.adobe.com/LjeF7eYU8V93W28VbV-D6NNWWwdKqywOP2BwzDwQAgo'
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
source-wordcount: '448'
ht-degree: 0%
---
# Personalice las URL de seguimiento para creativos en una experiencia con segmentación del árbol de decisiones

*Solo nodos de destino con creativos existentes*

Para las experiencias con segmentación del árbol de decisión, puede crear hasta cinco direcciones URL de seguimiento de impresiones personalizadas y cinco direcciones URL de seguimiento de clics personalizadas para cada creativo individual utilizado para la experiencia. Cuando la anulación de la página de aterrizaje esté disponible, también puede especificar una dirección URL de página de aterrizaje personalizada. Puede personalizar las direcciones URL de seguimiento desde cualquier editor del árbol de decisiones.

Las direcciones URL personalizadas solo se usan para los anuncios creados a partir de la experiencia y no se guardan en la configuración creativa base de [!UICONTROL Creative Libraries].

La anulación de la página de aterrizaje está disponible para experiencias estándar y para nodos que utilizan creativos predeterminados. Para los paquetes dinámicos asignados, las páginas de aterrizaje están determinadas por la fuente y no se muestra la pestaña de página de aterrizaje.

## Uso del editor controlado por IA (Beta) {#ai-editor}

Mientras [crea](experience-create-targeting.md#ai-editor) o [edita](experience-edit-targeting.md#ai-editor) la experiencia, use los controles de lienzo:

1. En el nodo de hoja creativa que se encuentra debajo del nodo de destino, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Seleccione la ficha **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** o (cuando esté disponible) **[!UICONTROL Landing URL]**.

   Los creativos se agrupan por paquete. Los tamaños creativos predeterminados para la experiencia determinan los tamaños creativos disponibles.

1. Expanda el elemento creativo que desee editar y realice una de las acciones siguientes:

   * Para añadir o editar una URL personalizada, introduzca la URL en el campo de entrada.

   * Para agregar otra URL de seguimiento personalizada, haga clic en **[!UICONTROL Add URL]** e introduzca la URL en el campo de entrada.

   * Para quitar una dirección URL personalizada, haga clic en **[!UICONTROL Delete URL]**.

   Haga clic fuera de un campo editado y corrija los errores de validación antes de guardar.

1. Haga clic en **[!UICONTROL Save]** en el cuadro de diálogo para actualizar el árbol de trabajo.

1. [Guarde la experiencia](#save) del encabezado del árbol.

## Uso del editor manual {#manual-editor}

[Abra el editor manual](experience-edit-targeting.md#experience-open) antes de seguir estos pasos.

1. En el nodo de hoja creativa que se encuentra debajo del nodo de destino, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Seleccione la ficha **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** o (cuando esté disponible) **[!UICONTROL Landing URLs]**.

   Las pestañas enumeran los creativos en los paquetes asignados. Los tamaños creativos predeterminados para la experiencia determinan los tamaños creativos disponibles.<!-- There's no distinct "Creative Sizes" setting. -->

1. Expanda el elemento creativo que desee editar y realice una de las acciones siguientes:

   * Para añadir o editar una URL personalizada, introduzca la URL en el campo de entrada.

   * Para agregar otra URL de seguimiento personalizada, haga clic en **[!UICONTROL +]** e introduzca la URL en el campo de entrada.

   * Para quitar una dirección URL personalizada, mantén el cursor sobre la fila creativa y haz clic en ![Eliminar](/help/creative/assets/delete.png "Eliminar").

1. Haga clic en **[!UICONTROL Save]** en el cuadro de diálogo para actualizar el árbol de trabajo.

1. [Guarde la experiencia](#save) del encabezado del árbol.

## Guarde la experiencia {#save}

Los siguientes pasos se aplican a ambos editores. Al guardar el cuadro de diálogo de URL de seguimiento por sí solo, la experiencia no se guarda ni publica.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizar las direcciones URL de seguimiento para una experiencia sin segmentación en el árbol de decisiones](experience-tracking-urls-no-targeting.md)
