---
title: Añadir un nodo de destino al nivel final de una experiencia
description: Obtenga información sobre cómo añadir un nodo de destino al nivel de destino final de una experiencia publicitaria.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: 5d8b511708008c77e817ccdb00ae02c158dfe63e
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Añadir un nodo de destino al nivel final de una experiencia

*Solo experiencias con direccionamiento en árbol de decisiones*
*Beta cerrada*

Cuando agrega un nodo de destino al nivel inferior de la experiencia (ya sea el nodo raíz &quot;Todos&quot;, un nodo específico de destino o un nodo &quot;Todo lo demás&quot;), define el destino directamente y no necesita crear un nodo relacionado. Al agregar un nodo de nivel inferior, se crea el nodo de destino y un nodo &quot;Todo lo demás&quot; adicional en el mismo nivel.

>[!NOTE]
>
>Para insertar un nodo de destino entre los niveles existentes de un árbol de decisión, consulte &quot;[Insertar un nodo de destino entre nodos en una experiencia](experience-target-node-add-inner.md)&quot;.

<!-- 1. [ways to get to the decision tree] -->

1. En el nodo en el que desea insertar el destino, haga clic en ![Agregar](/help/creative/assets/add.png "Agregar") y, a continuación, seleccione **[!UICONTROL Insert New Target]**.

1. Especifique los objetivos:

   * Para los destinos de audiencia de Adobe, seleccione **[!UICONTROL Adobe Audience]** y haga lo siguiente:

      1. Haga clic en **[!UICONTROL Click to Browse]** para abrir las opciones de [!UICONTROL Audience Targeting], abrir la ficha **[!UICONTROL Adobe Segments]**, especificar uno o más de los [!DNL Adobe] destinos de audiencia del anunciante y, a continuación, haga clic en **[!UICONTROL Create]**.

      1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varias audiencias, seleccione **[!UICONTROL Split targets to create nodes]**.

         Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada audiencia especificada. Si no divide los destinatarios, el usuario debe pertenecer a todas las audiencias especificadas.

      1. Haga clic en **[!UICONTROL Apply]**.

   * Para los destinos geográficos, seleccione una sola categoría geográfica (como [!UICONTROL Geo: Country]) y, a continuación, haga lo siguiente:

      1. Haga clic en **[!UICONTROL Click to Browse]** para abrir las opciones de [!UICONTROL Geo Targeting], especificar uno o varios destinos geográficos y, a continuación, haga clic en **[!UICONTROL Save]**.

         Los destinos de código postal tienen opciones de edición masiva. Para pegar varios códigos postales, haga clic en la ficha **[!UICONTROL Paste postal codes]**, seleccione el país, pegue o escriba códigos postales separados por comas o en líneas independientes y, a continuación, haga clic en **[!UICONTROL Include All]**. Para quitar un destino de código postal incluido, mantenga el cursor sobre el destino y haga clic en ![Quitar](/help/creative/assets/delete.png "Quitar") **[!UICONTROL Remove]**.

      1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

         Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada destino geográfico especificado. Si no divide los destinos, el usuario debe pertenecer a todas las ubicaciones especificadas.

      1. Haga clic en **[!UICONTROL Apply]**.

   * Para un destino de paso de datos, seleccione **[!UICONTROL Data Pass]**, introduzca un solo valor de paso de datos y haga clic en **[!UICONTROL Apply]**.

   La clave para el par clave-valor ya se ha establecido en el campo **[!UICONTROL Data Pass]** de la sección [!UICONTROL Advanced] de la [configuración de la experiencia](experience-settings-targeting.md).

   * Para un destino de píxel de retargeting, seleccione **[!UICONTROL RT Pixel]**, seleccione un único píxel de retargeting para usar y los valores de cualquiera de los atributos del píxel necesarios para mostrar los elementos creativos y, a continuación, haga clic en **[!UICONTROL Apply]**.

     Los atributos del píxel de redireccionamiento se configuran en [configuración de píxeles de redireccionamiento](/help/creative/pixels/retargeting-pixel-manage.md).

   * Para los destinos de dispositivo, haga lo siguiente:

      1. Seleccione una sola categoría de destino (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** o **[!UICONTROL Device: Browser]**) y, a continuación, seleccione los destinos.

      1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

         Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada destino geográfico especificado. Si no divide los destinos, el usuario debe pertenecer a todas las ubicaciones especificadas.

      1. Haga clic en **[!UICONTROL Apply]**.

1. Realice una de las siguientes acciones:

   * (Opcional) [Asigne elementos creativos](experience-assign-creative-bundles.md) al nuevo nodo de destino y al nodo &quot;Todo lo demás&quot;.

   * (Opcional) Para guardar la experiencia:

      1. Haga clic en **[!UICONTROL Save]** y luego en **[!UICONTROL OK]**.

      1. (Si cada nodo del nivel más bajo no incluye al menos un elemento creativo): Realice una de las siguientes acciones:

         * Para guardar la experiencia sin todos los paquetes creativos necesarios, haga clic en **[!UICONTROL Save as Draft]**.

           No se puede crear una etiqueta de anuncio para una experiencia de borrador.

         * Para asignar el elemento creativo predeterminado a cada destino al que aún no se le haya asignado un paquete creativo, haga clic en **[!UICONTROL Assign Default Creatives]**. Después de revisar el árbol actualizado con los elementos creativos predeterminados asignados, haga clic en **[!UICONTROL Save]** y **[!UICONTROL OK]**.

         * Para continuar editando el árbol de decisión, haga clic en **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Insertar un nodo de destino entre nodos](experience-target-node-add-inner.md)
>* [Agregar un nodo de destino secundario entre nodos](experience-target-node-add-sibling.md)
>* [Copiar nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md)
>* [Asignar elementos creativos a un nodo final](experience-assign-creative-bundles.md)
>* [Eliminar un nodo de destino o de hoja creativa](/help/creative/experiences/experience-target-node-delete.md)
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
>* [Configuración de experiencia de destino](experience-settings-targeting.md)
