---
title: Añadir un nodo de destino entre nodos en una experiencia
description: Obtenga información sobre cómo añadir un nodo de destino entre cuerpos de destinatario en una experiencia publicitaria.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
source-git-commit: 780c84aa8dadb52b55d5ca2bee6974b56972793b
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Añadir un nodo de destino entre nodos en una experiencia

*Solo experiencias con direccionamiento en árbol de decisiones*
*Beta cerrada*

Al insertar un nodo de destino entre los niveles existentes, el nuevo nodo de destino conserva todos los destinos y elementos creativos secundarios existentes y el nuevo nodo se denomina inicialmente &quot;Todo&quot;. Opcionalmente, puede mantener el nuevo nodo sin agregar destinos más específicos.

Para definir un objetivo específico, agregue un nodo de destino secundario adicional en el mismo nivel, especifique el nuevo objetivo y, a continuación, asigne los elementos creativos únicamente a ese objetivo. Al agregar un nodo de destino del mismo nivel, se crea el nuevo nodo de destino y se mueven todos los destinos secundarios y creativos que anteriormente se habían asignado a &quot;Todos&quot; a un nuevo nodo &quot;Todo lo demás&quot; en el mismo nivel. De este modo, la adición del nuevo destino no afecta a las ramas secundarias existentes porque solo el nuevo nodo secundario incluye la nueva información de objetivo.

>[!NOTE]
>
>Para agregar un nodo de destino al nivel inferior de un árbol de decisión, consulte &quot;[Agregar un nodo de destino al nivel final en una experiencia](experience-target-node-add-final.md)&quot;.

<!-- 1. [ways to get to the decision tree] -->

1. En el nodo en el que desea insertar el destino, haga clic en ![Agregar](/help/creative/assets/add.png "Agregar") y, a continuación, seleccione **[!UICONTROL Insert New Target]**.

1. Realice una de las siguientes acciones:

   * Si los nodos del mismo nivel aún no existen, haga lo siguiente:

      1. Seleccione el tipo de destino y haga clic en **[!UICONTROL Apply]**:

         * Para los destinos de audiencia, seleccione **[!UICONTROL Audience]**.

         * Para los destinos geográficos, seleccione una sola categoría geográfica (como [!UICONTROL Geo: Country]).

         * Para los destinos de paso de datos, seleccione **[!UICONTROL Data Pass]**.

         * Para redireccionar destinos de píxeles, seleccione **[!UICONTROL RT Pixel].

         * Para los destinos de dispositivo, seleccione una sola categoría de destino (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** o **[!UICONTROL Device: Browser]**).

   * Si ya existen nodos del mismo nivel, haga lo siguiente:

      * Para los objetivos de audiencia, haga lo siguiente:

         1. Haga clic en **[!UICONTROL Click to Browse]** para abrir las opciones de [!UICONTROL Audience Targeting] y especificar una o más audiencias del anunciante para segmentar.

         1. En la columna derecha, seleccione si desea *[!UICONTROL Include any]* (el valor predeterminado) o *[!UICONTROL Include all]* de los destinos especificados para el nodo.

        Esta opción determina si el usuario debe pertenecer al menos a una de las audiencias especificadas (una instrucción [!DNL Boolean] `OR`) o a todas las audiencias especificadas (una instrucción [!DNL Boolean] `AND`) para poder optar a una impresión.

         1. Haga clic en **[!UICONTROL Create]**.

         1. Haga clic en **[!UICONTROL Apply]**.

      * Para los objetivos geográficos, haga lo siguiente:

         1. Haga clic en **[!UICONTROL Click to Browse]** para abrir las opciones de [!UICONTROL Geo Targeting], especificar uno o varios destinos geográficos y, a continuación, haga clic en **[!UICONTROL Save]**.

            Los destinos de código postal tienen opciones de edición masiva. Para pegar varios códigos postales, haga clic en la ficha **[!UICONTROL Paste postal codes]**, seleccione el país, pegue o escriba códigos postales separados por comas o en líneas independientes y, a continuación, haga clic en **[!UICONTROL Include All]**. Para quitar un destino de código postal incluido, mantenga el cursor sobre el destino y haga clic en ![Quitar](/help/creative/assets/delete.png "Quitar") **[!UICONTROL Remove]**.

         1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

            Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada destino geográfico especificado. Si no divide los destinos, el usuario debe pertenecer a todas las ubicaciones especificadas (una instrucción [!DNL Boolean] `AND`).

         1. Haga clic en **[!UICONTROL Apply]**.

      * Para un destino de paso de datos, si lo desea, puede personalizar la clave de paso de datos, escribir un único valor de paso de datos y, a continuación, hacer clic en **[!UICONTROL Apply]**.

        Ya hay un valor predeterminado para la clave en el par clave-valor establecido en el campo **[!UICONTROL Data Pass]** de la sección [!UICONTROL Advanced] de la [configuración de la experiencia](experience-settings-targeting.md). Si lo desea, puede personalizar la clave.

      * Para un destino de píxel de retargeting, seleccione un único píxel de retargeting para utilizarlo y los valores de cualquiera de los atributos del píxel necesarios para mostrar los elementos creativos y, a continuación, haga clic en **[!UICONTROL Apply]**.

        Los atributos del píxel de redireccionamiento se configuran en [configuración de píxeles de redireccionamiento](/help/creative/pixels/retargeting-pixel-manage.md).

      * Para los destinos de dispositivo, haga lo siguiente:

         1. Seleccione los objetivos.

         1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

            Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada destino geográfico especificado. Si no divide los destinos, el usuario debe pertenecer a todas las ubicaciones especificadas (una instrucción [!DNL Boolean] `AND`).

         1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

         1. Haga clic en **[!UICONTROL Apply]**.

1. (Opcional) Especifique un nombre de rama personalizado para una rama definida por el usuario.

   De forma predeterminada, las ramas definidas por el usuario se etiquetan con los destinos aplicados.

   No se puede crear un nombre de rama personalizado para una rama &quot;Todos&quot; o &quot;Todos los demás&quot;.

   1. Mantenga el cursor sobre el nodo de destino y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Escriba **[!UICONTROL Node Name]** y haga clic en **[!UICONTROL Save]**.

1. Realice una de las siguientes acciones:

   * (Opcional) [Asigne elementos creativos](experience-assign-creative-bundles.md) al nuevo nodo de destino y al nodo &quot;Todo lo demás&quot;.

   * (Opcional) [Agregue un nodo de destino secundario](experience-target-node-add-sibling.md) del tipo de destino especificado.

   * (Opcional) Para guardar la experiencia:

      1. Haga clic en **[!UICONTROL Save]** y luego en **[!UICONTROL OK]**.

      1. (Si cada nodo del nivel más bajo no incluye al menos un elemento creativo): Realice una de las siguientes acciones:

         * Para guardar la experiencia sin todos los paquetes creativos necesarios, haga clic en **[!UICONTROL Save as Draft]**.

           No se puede crear una etiqueta de anuncio para una experiencia de borrador.

         * Para asignar el elemento creativo predeterminado a cada destino al que aún no se le haya asignado un paquete creativo, haga clic en **[!UICONTROL Assign Default Creatives]**. Después de revisar el árbol actualizado con los elementos creativos predeterminados asignados, haga clic en **[!UICONTROL Save]** y **[!UICONTROL OK]**.

         * Para continuar editando el árbol de decisión, haga clic en **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Agregar un nodo de destino al nivel final](experience-target-node-add-final.md)
>* [Agregar un nodo de destino secundario entre nodos](experience-target-node-add-sibling.md)
>* [Copiar nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md)
>* [Asignar elementos creativos a un nodo final](experience-assign-creative-bundles.md)
>* [Eliminar un nodo de destino o de hoja creativa](/help/creative/experiences/experience-target-node-delete.md)
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
>* [Configuración de experiencia de destino](experience-settings-targeting.md)
