---
title: Personalizar la optimización y programación creativas de una experiencia
description: Obtenga información sobre cómo
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 7fee6e0f6e8ad6dbf0329d707af7303ac7229dc9
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# Personalización de la optimización y programación creativas para una experiencia sin segmentación del árbol de decisiones

*Solo experiencias con creativos existentes*
*Beta cerrada*

De forma predeterminada, la rotación creativa de una etiqueta de experiencia publicitaria se determina de forma algorítmica para optimizar la tasa de pulsaciones general y la configuración de optimización creativa se aplica a todos los creativos asignados. Puede personalizar la rotación creativa para ejecutar manualmente los creativos según los pesos relativos o para optimizar de forma algorítmica para un objetivo personalizado de Advertising DSP especificado. También puede programar creativos específicos para que se ejecuten durante períodos de tiempo especificados y secuenciales, y aplicar ajustes de rotación creativa personalizados para cada programación.

## Configuración de la optimización creativa sin programación

Cuando se desactiva la programación creativa, la configuración de optimización creativa se aplica a todos los elementos creativos asignados.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Tag Manager]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Tag Manager]**.

1. Mantenga el cursor sobre la fila de la etiqueta de anuncio correspondiente y haga clic en ![Programación de anuncios](/help/creative/assets/edit-gray.png "Editar URL de seguimiento") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— A partir del segundo semestre, el Administrador de etiquetas solo tiene una vista de lista, pero no de tarjeta. >

1. Deshabilitar **[!UICONTROL Schedule]**.

1. Seleccione el tipo de rotación creativa:

   * *[!UICONTROL Weighted]:* Gira los elementos creativos manualmente según los pesos relativos. Introduzca el peso de cada creativo como porcentaje. Los pesos de todos los creativos seleccionados deben sumar 100.

   * *[!UICONTROL Algorithmic]:* Gira los elementos creativos de forma algorítmica según un objetivo de optimización especificado.

      * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]*, (experiencias de anuncios de vídeo estándar) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Haga clic en **[!UICONTROL Save]**.

## Configurar la optimización creativa con programación creativa

Si lo desea, puede programar creativos específicos utilizados para una etiqueta de experiencia de anuncio para que se ejecuten durante períodos de tiempo especificados y secuenciales entre las fechas de inicio y finalización de la experiencia, así como aplicar la configuración de rotación creativa personalizada para cada programación. Por ejemplo, puede programar Creative 1 para que se ejecute durante las dos primeras semanas a fin de optimizar la tasa de pulsaciones y Creative 2 para que se ejecute durante las dos semanas siguientes a fin de optimizar para un objetivo personalizado especificado.

Al programar, debe programar los elementos creativos durante toda la experiencia.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Tag Manager]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Tag Manager]**.

1. Mantenga el cursor sobre la fila de la etiqueta de anuncio correspondiente y haga clic en ![Programación de anuncios](/help/creative/assets/edit-gray.png "Editar URL de seguimiento") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— A partir del segundo semestre, el Administrador de etiquetas solo tiene una vista de lista, pero no de tarjeta. >

1. Habilitar **[!UICONTROL Schedule]**.

1. Para la primera programación:

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada elemento creativo para añadirlo a la primera programación.

   1. Especifique las fechas de inicio y finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * *[!UICONTROL Weighted]:* Gira los elementos creativos manualmente según los pesos relativos. Introduzca el peso de cada creativo como porcentaje. Los pesos de todos los creativos seleccionados deben sumar 100.

      * *[!UICONTROL Algorithmic]:* Gira los elementos creativos de forma algorítmica según un objetivo de optimización especificado.

         * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]*, (experiencias de anuncios de vídeo estándar) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Para cada programación adicional:

   1. Haga clic en **[!UICONTROL + Add Schedule]**.

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada elemento creativo para añadirlo a la primera programación.

   1. Especifique las fechas de inicio y finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * *[!UICONTROL Weighted]:* Gira los elementos creativos manualmente según los pesos relativos. Introduzca el peso de cada creativo como porcentaje. Los pesos de todos los creativos seleccionados deben sumar 100.

      * *[!UICONTROL Algorithmic]:* Gira los elementos creativos de forma algorítmica según un objetivo de optimización especificado.

         * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Crear manualmente una etiqueta de anuncio para un tamaño creativo aplicable](/help/creative/experiences/experience-tag-create-manually.md)
>* [Asignar elementos creativos a una etiqueta de anuncio para experiencias sin segmentación](experience-tag-assign-creatives.md)
>* [Personalizar las direcciones URL de seguimiento para una experiencia sin segmentación en el árbol de decisiones](experience-tracking-urls-no-targeting.md)
