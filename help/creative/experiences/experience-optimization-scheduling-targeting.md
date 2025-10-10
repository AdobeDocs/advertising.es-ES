---
title: Personalizar la optimización y programación creativas de una experiencia
description: Obtenga información sobre cómo
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 7bcafc7c70333bb6f523873ed08f2bc5123823f7
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# Personalice la optimización y programación creativas para una experiencia con segmentación del árbol de decisiones

*Solo nodos de destino con creativos existentes*

De forma predeterminada, la rotación creativa de una experiencia se determina de forma algorítmica para optimizar la tasa de pulsaciones general y la configuración de optimización creativa se aplica a todos los paquetes asignados. Alternativamente, puede optimizar de forma algorítmica para un objetivo personalizado de Advertising DSP especificado; rotar paquetes según una secuencia de paquetes especificada, con un número especificado de impresiones en cada secuencia de paquetes o según los pesos relativos. También puede programar paquetes creativos específicos para que se ejecuten durante períodos de tiempo especificados y secuenciales, y aplicar ajustes de rotación creativa personalizados a cada programación.

>[!NOTE]
>
>Estas funciones no están disponibles para nodos que utilicen los elementos creativos predeterminados en lugar de los elementos creativos asignados.

## Configuración de la optimización creativa sin programación

Cuando se desactiva la programación creativa, la configuración de optimización creativa se aplica a todos los elementos creativos asignados.

1. Mantenga el cursor sobre el nodo de hoja creativa situado debajo del nodo de destino y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Deshabilitar **[!UICONTROL Schedule]**.

1. Seleccione el tipo de rotación creativa para las variantes de anuncio en los paquetes asociados:

   * *[!UICONTROL Weighted]:* Muestra variantes de anuncio en los paquetes creativos asociados según los pesos relativos. Introduzca el peso de cada paquete como porcentaje. Los pesos de todos los paquetes seleccionados deben sumar 100.<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->

   * *[!UICONTROL Algorithmic]:* Muestra las variantes de anuncio más efectivas con mayor frecuencia, según un objetivo especificado.

      * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]*, (experiencias de anuncios de vídeo estándar) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

   * *[!UICONTROL Sequencing]:* Muestra los paquetes creativos asociados en un orden especificado (con el paquete 1 servido primero, el paquete 2 servido segundo, etc.), con un número total especificado de impresiones en cada secuencia de paquetes. Los tamaños de anuncio ofrecidos están determinados por el inventario disponible. Puede configurar el paquete final en la secuencia para que se muestre de forma indefinida (el bucle predeterminado) o b\) de nuevo al primer paquete. Por ejemplo, puede mostrar cualquiera de las variantes de anuncio en el paquete 1 para tres (3) impresiones, luego mostrar cualquier variante de anuncio en el paquete 2 para una (1) impresión, luego mostrar cualquiera de las variantes de anuncio en el paquete 3 para dos (2) impresiones y luego comenzar el bucle de nuevo. Alternativamente, una vez que se muestran las variantes de anuncio en el paquete 3, puede seguir mostrando las variantes de anuncio en el paquete 3 indefinidamente, en lugar de crear un bucle. Al habilitar la secuenciación:

      1. Arrastre y suelte los paquetes asignados en el orden deseado.

     De forma predeterminada, los paquetes asignados se secuencian en el orden en que se agregaron a la experiencia.

      1. Introduzca el número de impresiones de cada secuencia.

      1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Haga clic en **[!UICONTROL Save]**.

## Configurar la optimización creativa con programación creativa

Si lo desea, puede programar paquetes creativos específicos para que se ejecuten durante períodos de tiempo secuenciales y especificados entre las fechas de inicio y finalización de la experiencia, así como aplicar la configuración de rotación creativa personalizada para cada programación. Por ejemplo, puede programar el paquete 1 para que se ejecute durante las dos primeras semanas a fin de optimizar la tasa de clics y el paquete 2 para que se ejecute durante las dos semanas siguientes a fin de optimizar para un objetivo personalizado especificado.

Al utilizar la programación, debe programar paquetes a lo largo de la duración de la experiencia.

1. Mantenga el cursor sobre el nodo de hoja creativa situado debajo del nodo de destino y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Habilitar **[!UICONTROL Schedule]**.

1. Para la primera programación:

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada paquete creativo para añadirlo a la primera programación.

   1. Especifique las fechas de inicio y finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * *[!UICONTROL Weighted]:* Gira manualmente los elementos creativos de cada paquete según los pesos relativos. Introduzca el peso de cada paquete como porcentaje. Los pesos de todos los paquetes seleccionados deben sumar 100.

      * *[!UICONTROL Algorithmic]:* Gira los elementos creativos de cada paquete de forma algorítmica según un objetivo de optimización especificado.

         * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]*, (experiencias de anuncios de vídeo estándar) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

      * *[!UICONTROL Sequencing]:* gira los paquetes creativos asociados en un orden especificado (con el paquete 1 servido primero, el paquete 2 servido segundo, etc.), con un número total especificado de impresiones en cada secuencia de paquetes. Los tamaños de anuncio ofrecidos están determinados por el inventario disponible. Puede configurar el paquete final en la secuencia para que se muestre de forma indefinida (el bucle predeterminado) o b\) de nuevo al primer paquete. Por ejemplo, puede mostrar cualquiera de los creativos del paquete 1 para tres (3) impresiones, luego mostrar cualquier creativo del paquete 2 para una (1) impresión, luego mostrar cualquiera de los creativos del paquete 3 para dos (2) impresiones y luego comenzar el bucle de nuevo. Alternativamente, una vez que se muestran los creativos en el paquete 3, puede seguir mostrando los creativos en el paquete 3 indefinidamente, en lugar de crear un bucle. Al habilitar la secuenciación:

         1. Arrastre y suelte los paquetes asignados en el orden deseado.

            De forma predeterminada, los paquetes asignados se secuencian en el orden en que se agregaron a la experiencia.

         1. Introduzca el número de impresiones de cada secuencia.

         1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Para cada programación adicional:

   1. Haga clic en **[!UICONTROL + Add Schedule]**.

   1. En la columna de la izquierda, seleccione la casilla de verificación situada junto a cada paquete creativo para añadirlo a la primera programación.

   1. Especifique las fechas de inicio y finalización de la programación.

   1. Seleccione el tipo de rotación creativa:

      * *[!UICONTROL Weighted]:* Gira manualmente los elementos creativos de cada paquete según los pesos relativos. Introduzca el peso de cada paquete como porcentaje. Los pesos de todos los paquetes seleccionados deben sumar 100.

      * *[!UICONTROL Algorithmic]:* Gira los elementos creativos de cada paquete de forma algorítmica según un objetivo de optimización especificado.

         * Para **[!UICONTROL Optimization Goal]**, seleccione *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Si selecciona *[!UICONTROL Custom Objective]*, a continuación, seleccione una [meta personalizada de Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

      * *[!UICONTROL Sequencing]:* Gira los paquetes creativos asociados en un orden especificado, con un número total especificado de impresiones en cada secuencia de paquetes. Al habilitar la secuenciación:

         1. Arrastre y suelte los paquetes asignados en el orden deseado.

            De forma predeterminada, los paquetes asignados se secuencian en el orden en que se agregaron a la experiencia.

         1. Introduzca el número de impresiones de cada secuencia.

         1. Para la última secuencia, cambie si a\) mostrar el paquete final en la secuencia indefinidamente (*[!UICONTROL Infinite]* (el valor predeterminado) o b\) al primer paquete después de que se muestre el paquete final (*[!UICONTROL Keep in Loop]*).

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizar las direcciones URL de seguimiento para los creativos](/help/creative/experiences/experience-tracking-urls-targeting.md)
