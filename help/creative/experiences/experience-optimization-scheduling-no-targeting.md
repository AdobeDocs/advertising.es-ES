---
title: Personalizar la optimización y programación creativas de una experiencia
description: Obtenga información sobre cómo configurar la optimización y la programación de anuncios para experiencias sin segmentación.
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 24ae6f65552a2c958488be4f1363c08c3f387d37
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 0%

---

# Personalización de la optimización y programación creativas para una experiencia sin segmentación del árbol de decisiones

*Solo experiencias con creativos existentes*

De forma predeterminada, la rotación creativa de una etiqueta de experiencia publicitaria se determina de forma algorítmica para optimizar la tasa de pulsaciones general y la configuración de optimización creativa se aplica a todos los creativos asignados. Puede personalizar la rotación creativa para ejecutar manualmente los creativos según los pesos relativos o para optimizar de forma algorítmica para un objetivo personalizado de Advertising DSP especificado. También puede programar creativos específicos para que se ejecuten durante períodos de tiempo especificados y secuenciales, y aplicar ajustes de rotación creativa personalizados para cada programación.

## Configuración de la optimización creativa sin programación

Cuando se desactiva la programación creativa, la configuración de optimización creativa se aplica a todos los elementos creativos asignados.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Tag Manager]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Tag Manager]**.

1. Mantenga el cursor sobre la fila de la etiqueta de publicidad aplicable y haga clic en ![Editar optimización creativa](/help/creative/assets/edit-gray.png "Editar optimización creativa") **[!UICONTROL Creative Optimization]**.&lt;!— A partir del segundo semestre, el Administrador de etiquetas solo tiene una vista de lista, pero no de tarjeta. >

1. Deshabilitar **[!UICONTROL Schedule]**.

1. Seleccione el tipo de rotación creativa para las variantes de anuncio en los paquetes asociados:

   * *[!UICONTROL Weighted]:* Muestra variantes de anuncio en los paquetes creativos asociados según los pesos relativos. Introduzca el peso de cada paquete como porcentaje. Para aplicar pesos iguales a todos los paquetes asociados, haga clic en (![Aplicar igual peso](/help/creative/assets/apply-equal-weight.png "Aplicar igual peso")). Los pesos de todos los paquetes seleccionados deben sumar 100.<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->

   * *[!UICONTROL Algorithmic]:* Muestra las variantes de anuncio más efectivas con mayor frecuencia, según un objetivo especificado.

      * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]*, (experiencias de anuncios de vídeo estándar) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

   * *[!UICONTROL Sequencing]:* Muestra los paquetes creativos asociados en un orden especificado (con el paquete 1 servido primero, el paquete 2 servido segundo, etc.), con un número total especificado de impresiones en cada secuencia de paquetes. Los tamaños de anuncio ofrecidos están determinados por el inventario disponible. Puede configurar el paquete final en la secuencia para que se muestre de forma indefinida (el bucle predeterminado) o b\) de nuevo al primer paquete. Por ejemplo, puede mostrar cualquiera de las variantes de anuncio en el paquete 1 para tres (3) impresiones, luego mostrar cualquier variante de anuncio en el paquete 2 para una (1) impresión, luego mostrar cualquiera de las variantes de anuncio en el paquete 3 para dos (2) impresiones y luego comenzar el bucle de nuevo. Alternativamente, una vez que se muestran las variantes de anuncio en el paquete 3, puede seguir mostrando las variantes de anuncio en el paquete 3 indefinidamente, en lugar de crear un bucle. Al habilitar la secuenciación:

      1. Arrastre y suelte los paquetes asignados en el orden deseado.

     De forma predeterminada, los paquetes asignados se secuencian en el orden en que se agregaron a la experiencia.

      1. Introduzca el número de impresiones de cada secuencia.

      1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Haga clic en **[!UICONTROL Save]**.

## Configurar la optimización creativa con programación creativa

Si lo desea, puede programar creativos específicos utilizados para una etiqueta de experiencia de anuncio para que se ejecuten durante períodos de tiempo especificados y secuenciales entre las fechas de inicio y finalización de la experiencia, así como aplicar la configuración de rotación creativa personalizada para cada programación. Por ejemplo, puede programar Creative 1 para que se ejecute durante las dos primeras semanas a fin de optimizar la tasa de pulsaciones y Creative 2 para que se ejecute durante las dos semanas siguientes a fin de optimizar para un objetivo personalizado especificado.

Al programar, debe programar los elementos creativos durante toda la experiencia.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Tag Manager]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Tag Manager]**.

1. Mantenga el cursor sobre la fila de la etiqueta de publicidad aplicable y haga clic en ![Editar optimización creativa](/help/creative/assets/edit-gray.png "Editar optimización creativa") **[!UICONTROL Creative Optimization]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— A partir del segundo semestre, el Administrador de etiquetas solo tiene una vista de lista, pero no de tarjeta. >

1. Habilitar **[!UICONTROL Schedule]**.

1. Para la primera programación:

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada elemento creativo para añadirlo a la primera programación.

   1. Especifique la fecha de inicio y la hora de inicio, así como la fecha de finalización y la hora de finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * *[!UICONTROL Weighted]:* Gira los elementos creativos manualmente según los pesos relativos. Introduzca el peso de cada creativo como porcentaje. Para aplicar pesos iguales a todos los paquetes de la programación, haga clic en (![Aplicar igual peso](/help/creative/assets/apply-equal-weight.png "Aplicar igual peso")). Los pesos de todos los creativos seleccionados deben sumar 100.

      * *[!UICONTROL Algorithmic]:* Gira los elementos creativos de forma algorítmica según un objetivo de optimización especificado.

         * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]*, (experiencias de anuncios de vídeo estándar) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

      * *[!UICONTROL Sequencing]:* gira los paquetes creativos asociados en un orden especificado (con el paquete 1 servido primero, el paquete 2 servido segundo, etc.), con un número total especificado de impresiones en cada secuencia de paquetes. Los tamaños de anuncio ofrecidos están determinados por el inventario disponible. Puede configurar el paquete final en la secuencia para que se muestre de forma indefinida (el bucle predeterminado) o b\) de nuevo al primer paquete. Por ejemplo, puede mostrar cualquiera de los creativos del paquete 1 para tres (3) impresiones, luego mostrar cualquier creativo del paquete 2 para una (1) impresión, luego mostrar cualquiera de los creativos del paquete 3 para dos (2) impresiones y luego comenzar el bucle de nuevo. Alternativamente, una vez que se muestran los creativos en el paquete 3, puede seguir mostrando los creativos en el paquete 3 indefinidamente, en lugar de crear un bucle. Al habilitar la secuenciación:

         1. Arrastre y suelte los paquetes asignados en el orden deseado.

            De forma predeterminada, los paquetes asignados se secuencian en el orden en que se agregaron a la experiencia.

         1. Introduzca el número de impresiones de cada secuencia.

         1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Para cada programación adicional:

   1. Haga clic en **[!UICONTROL + Add Schedule]**.

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada elemento creativo para añadirlo a la primera programación.

   1. Especifique las fechas de inicio y finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * *[!UICONTROL Weighted]:* Gira los elementos creativos manualmente según los pesos relativos. Introduzca el peso de cada creativo como porcentaje. Los pesos de todos los creativos seleccionados deben sumar 100.

      * *[!UICONTROL Algorithmic]:* Gira los elementos creativos de forma algorítmica según un objetivo de optimización especificado.

         * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

      * *[!UICONTROL Sequencing]:* Gira los paquetes creativos asociados en un orden especificado, con un número total especificado de impresiones en cada secuencia de paquetes. Al habilitar la secuenciación:

         1. Arrastre y suelte los paquetes asignados en el orden deseado.

            De forma predeterminada, los paquetes asignados se secuencian en el orden en que se agregaron a la experiencia.

         1. Introduzca el número de impresiones de cada secuencia.

         1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Crear manualmente una etiqueta de anuncio para un tamaño creativo aplicable](/help/creative/experiences/experience-tag-create-manually.md)
>* [Asignar elementos creativos a una etiqueta de anuncio para experiencias sin segmentación](experience-tag-assign-creatives.md)
>* [Personalizar las direcciones URL de seguimiento para una experiencia sin segmentación en el árbol de decisiones](experience-tracking-urls-no-targeting.md)
