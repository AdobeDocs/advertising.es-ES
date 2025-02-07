---
title: Personalizar la optimización y programación creativas de una experiencia
description: Obtenga información sobre cómo
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Personalice la optimización y programación creativas para una experiencia con segmentación del árbol de decisiones

*Solo nodos de destino con creativos existentes*
*Beta cerrada*

De forma predeterminada, la rotación creativa de una experiencia se determina de forma algorítmica para optimizar la tasa de pulsaciones general y la configuración de optimización creativa se aplica a todos los paquetes asignados. Puede personalizar la rotación creativa para ejecutar manualmente los creativos en cada paquete según los pesos relativos o para optimizar de forma algorítmica para un objetivo personalizado de Advertising DSP especificado. <!-- verify --> También puede programar paquetes creativos específicos para que se ejecuten durante períodos de tiempo secuenciales especificados y aplicar la configuración de rotación creativa personalizada para cada programación.

>[!NOTE]
>
>Estas funciones no están disponibles para nodos que utilicen los elementos creativos de imagen predeterminados en lugar de los elementos creativos asignados.

## Configuración de la optimización creativa sin programación

Cuando se desactiva la programación creativa, la configuración de optimización creativa se aplica a todos los elementos creativos asignados.

1. Mantenga el cursor sobre el nodo de hoja creativa situado debajo del nodo de destino y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Deshabilitar **[!UICONTROL Schedule]**.

1. Seleccione el tipo de rotación creativa:

   * ** *Ponderado* **: Gira manualmente los elementos creativos de cada paquete según los pesos relativos. Introduzca el peso de cada paquete como porcentaje. Los pesos de todos los paquetes deben sumar 100.

   * ** *Algorítmico* **: Gira los elementos creativos de cada paquete de forma algorítmica de acuerdo con un objetivo de optimización especificado.

   * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Haga clic en **[!UICONTROL Save]**.

## Configurar la optimización creativa con programación creativa

Si lo desea, puede programar paquetes creativos específicos para que se ejecuten durante períodos de tiempo secuenciales y especificados entre las fechas de inicio y finalización de la experiencia, así como aplicar la configuración de rotación creativa personalizada para cada programación. Por ejemplo, puede programar el paquete 1 para que se ejecute durante las dos primeras semanas a fin de optimizar la tasa de clics y el paquete 2 para que se ejecute durante las dos semanas siguientes a fin de optimizar para un objetivo personalizado especificado.

Al utilizar la programación, debe programar paquetes a lo largo de la duración de la experiencia.

1. Mantenga el cursor sobre el nodo de hoja creativa situado debajo del nodo de destino y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Habilitar **[!UICONTROL Schedule]**.

1. Para la primera programación:

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada paquete creativo para añadirlo a la primera programación.

   1. Especifique las fechas de inicio y finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * ** *Ponderado* **: Gira manualmente los elementos creativos de cada paquete según los pesos relativos. Introduzca el peso de cada paquete como porcentaje. Los pesos de todos los paquetes seleccionados deben sumar 100.

      * ** *Algorítmico* **: Gira los elementos creativos de cada paquete de forma algorítmica de acuerdo con un objetivo de optimización especificado.

      * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Para cada programación adicional:

   1. Haga clic en **[!UICONTROL + Add Schedule]**.

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada paquete creativo para añadirlo a la primera programación.

   1. Especifique las fechas de inicio y finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * ** *Ponderado* **: Gira manualmente los elementos creativos de cada paquete según los pesos relativos. Introduzca el peso de cada paquete como porcentaje. Los pesos de todos los paquetes seleccionados deben sumar 100.

      * ** *Algorítmico* **: Gira los elementos creativos de cada paquete de forma algorítmica de acuerdo con un objetivo de optimización especificado.

      * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizar las direcciones URL de seguimiento para los creativos](/help/creative/experiences/experience-tracking-urls-targeting.md)
