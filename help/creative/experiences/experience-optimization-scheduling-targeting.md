---
title: Personalizar la optimización y programación creativas de una experiencia
description: Obtenga información sobre cómo configurar la optimización y la programación de anuncios para experiencias segmentadas.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
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
source-wordcount: '1244'
ht-degree: 0%
---
# Personalice la optimización y programación creativas para una experiencia con segmentación del árbol de decisiones

*Solo nodos de destino con creativos existentes*

De forma predeterminada, una experiencia optimiza la rotación creativa para la tasa de pulsaciones generales en todos los paquetes asignados. Puede personalizar la configuración de rotación o programar paquetes específicos para que se ejecuten durante períodos de tiempo secuenciales, con ajustes de rotación independientes para cada programación.

>[!NOTE]
>
>Estas funciones no están disponibles para nodos que utilicen los elementos creativos predeterminados en lugar de los elementos creativos asignados.

Puede configurar estos ajustes directamente en el lienzo del editor controlado por IA (Beta) o en el editor manual. En cualquier editor, al guardar el cuadro de diálogo del paquete, se actualiza el árbol de trabajo; también debe [guardar la experiencia](#save) del encabezado del árbol.

## Configuración de rotación {#rotation-settings}

* **[!UICONTROL Weighted]:** Muestra variantes de anuncio en los paquetes creativos asociados según los pesos relativos.

* **[!UICONTROL Algorithmic]:** Muestra las variantes de anuncio más efectivas con mayor frecuencia, según un objetivo de optimización especificado, como la tasa de pulsaciones o un objetivo personalizado de Advertising DSP.

* **[!UICONTROL Sequence](editor controlado por IA) o [!UICONTROL Sequencing] (editor manual):** Muestra los paquetes creativos asociados en un orden especificado, con un número especificado de impresiones para cada paquete en la secuencia. De forma predeterminada, los paquetes se secuencian en el orden en que se agregaron a la experiencia. Los tamaños de anuncio ofrecidos están determinados por el inventario disponible. El paquete final puede servir indefinidamente (el predeterminado), o la secuencia puede volver al primer paquete.

  Por ejemplo, una secuencia podría servir variantes de anuncio del paquete 1 para tres impresiones, el paquete 2 para una impresión y el paquete 3 para dos impresiones, y luego repetir. Sin un bucle, el paquete 3 sigue funcionando indefinidamente.

## Configuración de la optimización creativa sin programación

Cuando se desactiva la programación creativa, la configuración de optimización creativa se aplica a todos los elementos creativos asignados.

### Uso del editor controlado por IA (Beta) {#without-scheduling-ai}

1. Mientras [crea](experience-create-targeting.md#ai-editor) o [edita](experience-edit-targeting.md#ai-editor) la experiencia, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** en el nodo de hoja creativa.

   Para un nodo final sin paquetes, haga clic en **[!UICONTROL Assign Bundles]** y [asigne primero los paquetes](experience-assign-creative-bundles.md#ai-editor).

1. Abra la ficha **[!UICONTROL Creative optimisation]**.

1. Deshabilitar **[!UICONTROL Schedule]**.

1. Seleccione el tipo de rotación creativa y configure sus opciones:

   * **[!UICONTROL Weighted]:** Escriba el peso relativo para cada fila del paquete. Las pesas deben sumar 100. Para distribuir los pesos equitativamente, haga clic en **[!UICONTROL Apply equal weight]**.

   * **[!UICONTROL Algorithmic]:** Seleccione una opción **[!UICONTROL Optimization goals]**. Si elige un objetivo personalizado, seleccione la [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente en **[!UICONTROL Custom objective]**.

   * **[!UICONTROL Sequence]:** Arrastre los paquetes al orden deseado e introduzca el número de impresiones para cada secuencia. Habilite **[!UICONTROL Keep in loop]** para repetir la secuencia o déjela deshabilitada para establecer las impresiones del último paquete en **[!UICONTROL Infinite]**.

1. Haga clic en **[!UICONTROL Save]** en el cuadro de diálogo.

1. [Guarde la experiencia](#save).

### Uso del editor manual {#without-scheduling-manual}

[Abra el editor manual](experience-edit-targeting.md#experience-open) antes de seguir estos pasos.

1. Mientras [crea](experience-create-targeting.md) o [edita](experience-edit-targeting.md) la experiencia, abra la configuración de optimización creativa:

   1. Mantenga el cursor sobre el nodo de hoja creativa situado debajo del nodo de destino y haga lo siguiente:

      * Para los paquetes existentes, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Para nuevos paquetes, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** y [asigne los paquetes](experience-assign-creative-bundles.md).

   1. Haga clic en la ficha **[!UICONTROL Creative Optimization]**.

1. Deshabilitar **[!UICONTROL Schedule]**.

1. Seleccione el tipo de rotación creativa para las variantes de anuncio en los paquetes asociados:

   * *[!UICONTROL Weighted]:* Escriba el peso de cada paquete como porcentaje. Para aplicar pesos iguales a todos los paquetes asociados, haga clic en (![Aplicar igual peso](/help/creative/assets/apply-equal-weight.png "Aplicar igual peso")). Los pesos de todos los paquetes seleccionados deben sumar 100.

   * *[!UICONTROL Algorithmic]:* Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]*, (experiencias de anuncios de vídeo estándar) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*. Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

   * *[!UICONTROL Sequencing]:*

     1. Arrastre y suelte los paquetes asignados en el orden deseado.

     1. Introduzca el número de impresiones de cada secuencia.

     1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Haga clic en **[!UICONTROL Save]**.

## Configurar la optimización creativa con programación creativa

Si lo desea, puede programar paquetes creativos específicos para que se ejecuten durante períodos de tiempo secuenciales y especificados entre las fechas de inicio y finalización de la experiencia, así como aplicar la configuración de rotación creativa personalizada para cada programación. Por ejemplo, puede programar el paquete 1 para que se ejecute durante las dos primeras semanas a fin de optimizar la tasa de clics y el paquete 2 para que se ejecute durante las dos semanas siguientes a fin de optimizar para un objetivo personalizado especificado.

Al utilizar la programación, debe programar paquetes a lo largo de la duración de la experiencia.

### Uso del editor controlado por IA (Beta) {#with-scheduling-ai}

1. Mientras [crea](experience-create-targeting.md#ai-editor) o [edita](experience-edit-targeting.md#ai-editor) la experiencia, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** en el nodo de hoja creativa.

   Para un nodo final sin paquetes, haga clic en **[!UICONTROL Assign Bundles]** y [asigne primero los paquetes](experience-assign-creative-bundles.md#ai-editor).

1. Abra la ficha **[!UICONTROL Creative optimisation]** y habilite **[!UICONTROL Schedule]**.

1. Seleccione **[!UICONTROL Timezone]** para la programación.

1. Para la primera programación:

   1. Seleccione la casilla de verificación situada junto a cada paquete que desea incluir en la columna izquierda.

   1. Especifique las fechas y horas de inicio y finalización.

   1. Seleccione el tipo de rotación creativa y configure sus opciones:

      * **[!UICONTROL Weighted]:** Escriba el peso relativo para cada fila del paquete en la programación. Las pesas deben sumar 100. Para distribuir los pesos equitativamente, haga clic en **[!UICONTROL Apply equal weight]**.

      * **[!UICONTROL Algorithmic]:** Seleccione una opción **[!UICONTROL Optimization goals]**. Si elige un objetivo personalizado, seleccione la [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente en **[!UICONTROL Custom objective]**.

      * **[!UICONTROL Sequence]:** Arrastre los paquetes al orden deseado e introduzca el número de impresiones para cada secuencia. Habilite **[!UICONTROL Keep in loop]** para repetir la secuencia o déjela deshabilitada para establecer las impresiones del último paquete en **[!UICONTROL Infinite]**.

1. Para cada horario adicional, haga clic en **[!UICONTROL + Add Schedule]**, seleccione su tarjeta de horario y configure sus paquetes, fechas y horas, así como la configuración de rotación.

   Las casillas de verificación del paquete se aplican a la programación seleccionada, no a todas las programaciones. Asegúrese de que las programaciones abarquen toda la duración de la experiencia con paquetes asignados.

1. Haga clic en **[!UICONTROL Save]** en el cuadro de diálogo.

1. [Guarde la experiencia](#save).

### Uso del editor manual {#with-scheduling-manual}

[Abra el editor manual](experience-edit-targeting.md#experience-open) antes de seguir estos pasos.

1. Mientras [crea](experience-create-targeting.md) o [edita](experience-edit-targeting.md) la experiencia, abra la configuración de optimización creativa:

   1. Mantenga el cursor sobre el nodo de hoja creativa situado debajo del nodo de destino y haga lo siguiente:

      * Para los paquetes existentes, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Para nuevos paquetes, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** y [asigne los paquetes](experience-assign-creative-bundles.md).

   1. Haga clic en la ficha **[!UICONTROL Creative Optimization]**.

1. Habilitar **[!UICONTROL Schedule]**.

1. Para la primera programación:

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada paquete creativo para añadirlo a la primera programación.

   1. Especifique la fecha de inicio y la hora de inicio, así como la fecha de finalización y la hora de finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * *[!UICONTROL Weighted]:* Escriba el peso de cada paquete como porcentaje. Para aplicar pesos iguales a todos los paquetes de la programación, haga clic en (![Aplicar igual peso](/help/creative/assets/apply-equal-weight.png "Aplicar igual peso")). Los pesos de todos los paquetes seleccionados deben sumar 100.

      * *[!UICONTROL Algorithmic]:* Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]*, (experiencias de anuncios de vídeo estándar) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*. Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

      * *[!UICONTROL Sequencing]:*

        1. Arrastre y suelte los paquetes asignados en el orden deseado.

        1. Introduzca el número de impresiones de cada secuencia.

        1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Para cada programación adicional:

   1. Haga clic en **[!UICONTROL + Add Schedule]**.

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada paquete creativo para añadirlo a la primera programación.

   1. Especifique las fechas de inicio y finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * *[!UICONTROL Weighted]:* Escriba el peso de cada paquete como porcentaje. Los pesos de todos los paquetes seleccionados deben sumar 100.

      * *[!UICONTROL Algorithmic]:* Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*. Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

      * *[!UICONTROL Sequencing]:*

        1. Arrastre y suelte los paquetes asignados en el orden deseado.

        1. Introduzca el número de impresiones de cada secuencia.

        1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Haga clic en **[!UICONTROL Save]**.

## Guarde la experiencia {#save}

Los siguientes pasos se aplican a ambos editores.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizar las direcciones URL de seguimiento para los creativos](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [Ver el registro de cambios de una experiencia](/help/creative/experiences/experience-view-change-log.md)
