---
title: Añadir un nodo de destino del mismo nivel entre nodos de una experiencia
description: Obtenga información sobre cómo agregar un nodo secundario a cualquier nodo que tenga un destino o esté en el mismo nivel que un nodo con un destino.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Añadir un nodo de destino del mismo nivel entre nodos de una experiencia

*Solo experiencias con direccionamiento en árbol de decisiones*

Puede agregar un nodo del mismo nivel a cualquier nodo que tenga un destino o que esté en el mismo nivel que un nodo con un destino.

<!-- 1. Open the decision tree:

In a new experience

In an existing experience,
 -->

1. Encima del nodo al que desea agregar el nodo secundario, haga clic en ![Agregar](/help/creative/assets/add.png "Agregar") y, a continuación, seleccione **[!UICONTROL Insert Sibling Target]**.

1. Especifique los objetivos:

   * Para los objetivos de audiencia, haga lo siguiente:

      1. Haga clic en **[!UICONTROL Click to Browse]** para abrir las opciones de [!UICONTROL Audience Targeting] y, a continuación, haga lo siguiente:

         * Para añadir el primer segmento, localícelo en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento.

         * Para agregar un segmento a un grupo de segmentos existente:

            1. Haga clic en el grupo de segmentos en el panel derecho.

            1. (Opcional) Cambie la lógica de grupo a *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, según sea necesario.

               *[!UICONTROL Exclude All]* no está disponible para el primer grupo de segmentos. Para una audiencia que incluya solo exclusiones, genere esta audiencia como *[!UICONTROL Include Any]* y luego excluya esa audiencia cuando la agregue a una ubicación dentro de su DSP.

            1. Busque el nuevo segmento en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento.

               El grupo de segmentos se actualiza automáticamente con el nuevo segmento.

         * Para agregar un nuevo grupo de segmentos:

         1. Haga clic en **[!UICONTROL + New Group]** en el panel derecho.

         1. (Opcional) Cambie la lógica entre el grupo anterior y el nuevo a *[!UICONTROL And]* o *[!UICONTROL Or]*, según sea necesario.

         1. Busque los segmentos para el nuevo grupo en el panel izquierdo y seleccione las casillas de verificación situadas junto a los nombres de los segmentos.

         1. (Opcional) Cambie la lógica de grupo a *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, según sea necesario.

      1. Haga clic en **[!UICONTROL Create]**.

      1. Haga clic en **[!UICONTROL Apply]**.

   * Para los objetivos geográficos, haga lo siguiente:

      1. Haga clic en **[!UICONTROL Click to Browse]** para abrir las opciones de [!UICONTROL Geo Targeting], especificar uno o varios destinos geográficos y, a continuación, haga clic en **[!UICONTROL Save]**.

         Los destinos de código postal tienen opciones de edición masiva. Para pegar varios códigos postales, haga clic en la ficha **[!UICONTROL Paste postal codes]**, seleccione el país, pegue o escriba códigos postales separados por comas o en líneas independientes y, a continuación, haga clic en **[!UICONTROL Include All]**. Para quitar un destino de código postal incluido, mantenga el cursor sobre el destino y haga clic en ![Quitar](/help/creative/assets/delete.png "Quitar") **[!UICONTROL Remove]**.

      1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

         Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada destino geográfico especificado. Si no divide los destinos, el usuario debe pertenecer a todas las ubicaciones especificadas (una instrucción [!DNL Boolean] `AND`).

      1. Haga clic en **[!UICONTROL Apply]**.

   * Para los destinos de paso de datos, si lo desea, puede personalizar la clave de paso de datos, escribir un único valor de paso de datos y hacer clic en **[!UICONTROL Apply]**.

     Ya hay un valor predeterminado para la clave en el par clave-valor establecido en el campo **[!UICONTROL Data Pass]** de la sección [!UICONTROL Advanced] de la [configuración de la experiencia](experience-settings-targeting.md). Si lo desea, puede personalizar la clave.

   * Para destinos de píxel de retargeting, seleccione el píxel de retargeting que desea utilizar y los valores necesarios para cualquiera de los atributos del píxel que deben estar presentes para mostrar los elementos creativos. Luego haga clic en **[!UICONTROL Apply]**.

     Los atributos del píxel de redireccionamiento se configuran en [configuración de píxeles de redireccionamiento](/help/creative/pixels/retargeting-pixel-manage.md).

   * Para los destinos de dispositivo, haga lo siguiente:

      1. Seleccione los objetivos.

      1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

         Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada destino geográfico especificado. Si no divide los destinos, el usuario debe pertenecer a todas las ubicaciones especificadas (una instrucción [!DNL Boolean] `AND`).

      1. Haga clic en **[!UICONTROL Apply]**.

1. (Opcional) Especifique un nombre de rama personalizado para una rama definida por el usuario.

   De forma predeterminada, las ramas definidas por el usuario se etiquetan con los destinos aplicados.

   No se puede crear un nombre de rama personalizado para una rama &quot;Todos&quot; o &quot;Todos los demás&quot;.

   1. Mantenga el cursor sobre el nodo de destino y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Escriba **[!UICONTROL Node Name]** y haga clic en **[!UICONTROL Save]**.

1. Realice una de las siguientes acciones:

   * (Opcional) [Asigne elementos creativos](experience-assign-creative-bundles.md) al nuevo nodo de destino.

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
>* [Insertar un nodo de destino entre nodos](experience-target-node-add-inner.md)
>* [Copiar nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md)
>* [Asignar elementos creativos a un nodo final](experience-assign-creative-bundles.md)
>* [Eliminar un nodo de destino o de hoja creativa](/help/creative/experiences/experience-target-node-delete.md)
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
>* [Configuración de experiencia de destino](experience-settings-targeting.md)
