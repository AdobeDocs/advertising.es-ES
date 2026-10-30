---
title: Añadir un nodo de destino al nivel final de una experiencia
description: Obtenga información sobre cómo añadir un nodo de destino al nivel de destino final de una experiencia publicitaria.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
TQID: 'https://experienceleague.adobe.com/1T0Jwc8noxF-uaTA2cN78uOBsgHDjSnoD9Scmmw4L3s'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 0%
---
# Añadir un nodo de destino al nivel final de una experiencia

*Solo experiencias con direccionamiento en árbol de decisiones*

Cuando agrega un nodo de destino al nivel inferior de la experiencia (ya sea el nodo raíz &quot;Todos&quot;, un nodo específico de destino o un nodo &quot;Todo lo demás&quot;), define el destino directamente y no necesita crear un nodo relacionado. Al agregar un nodo de nivel inferior, se crea el nodo de destino y un nodo &quot;Todo lo demás&quot; adicional en el mismo nivel.

>[!NOTE]
>
>Para insertar un nodo de destino entre los niveles existentes de un árbol de decisión, consulte &quot;[Insertar un nodo de destino entre nodos en una experiencia](experience-target-node-add-inner.md)&quot;.

## Uso del editor controlado por IA (Beta) {#ai-editor}

Mientras [crea](experience-create-targeting.md#ai-editor) o [edita](experience-edit-targeting.md#ai-editor) la experiencia, puede describir el nuevo destino y su rama principal al agente de IA. Revise el árbol resultante antes de guardar. Para añadir el objetivo directamente en el lienzo:

1. Mantenga el cursor sobre el nodo principal al final de la rama y haga clic en **[!UICONTROL +]**.

1. En **[!UICONTROL New targeting level]**, seleccione la categoría de destino y haga clic en **[!UICONTROL Add targeting level]**.

1. Especifique los valores objetivo para la categoría:

   * Para destinos de audiencia:

     * Para añadir el primer segmento, busque y seleccione el segmento de audiencia.

     * Para agregar segmentos a un grupo de segmentos existente:

       1. Seleccione el grupo de segmentos.

       1. (Opcional) Cambie la lógica de grupo a **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**, según sea necesario.

          **[!UICONTROL Include Any]** coincide con los usuarios de al menos un segmento seleccionado; **[!UICONTROL Include All]** requiere pertenencia en todos los segmentos seleccionados.

          **[!UICONTROL Exclude All]** no está disponible para el primer grupo de segmentos. Para una audiencia que incluya solamente exclusiones, genere la audiencia con **[!UICONTROL Include Any]** y luego excluya esa audiencia cuando la agregue a una ubicación dentro de su DSP.

       1. Busque y seleccione los segmentos adicionales.

     * Para agregar un nuevo grupo de segmentos:

       1. Añada un grupo.

       1. (Opcional) Cambie la lógica entre el grupo anterior y el nuevo a **[!UICONTROL And]** o **[!UICONTROL Or]**, según sea necesario.

          **[!UICONTROL And]** requiere que los usuarios cumplan las condiciones de ambos grupos; **[!UICONTROL Or]** requiere que cumplan al menos las condiciones de un grupo.

       1. Busque y seleccione los segmentos para el nuevo grupo.

       1. (Opcional) Cambie la lógica de grupo a **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**, según sea necesario.

   * Para objetivos geográficos:

     * Seleccione las ubicaciones dentro de la categoría geográfica que haya elegido, como países, regiones o ciudades.

     * Para los destinos de código postal, seleccione el país e introduzca los códigos postales que desea incluir. Para introducir varios códigos postales de forma masiva, sepárelos con comas o coloque cada código en una línea independiente.

   * Para los destinos de paso de datos, introduzca la clave y el valor que deben coincidir.

     La clave de paso de datos predeterminada está configurada en el campo **[!UICONTROL Data Pass]** de la sección **[!UICONTROL Advanced]** de la [configuración general de la experiencia](experience-settings-targeting.md). Personalice la clave del destinatario si es necesario.

   * Para destinos de píxel de retargeting, seleccione el píxel de retargeting y especifique los valores de los atributos de píxel necesarios para mostrar los elementos creativos.

     Los atributos disponibles están configurados en la [configuración de píxeles de retargeting](/help/creative/pixels/retargeting-pixel-manage.md).

   * Para los destinos de dispositivo, seleccione los valores dentro de la categoría de dispositivo que elija: tipos de dispositivo, sistemas operativos o exploradores.

1. (Si está disponible; opcional) Seleccione **[!UICONTROL Split Nodes]** para crear un nodo de destino independiente para cada valor seleccionado, con sus propias asignaciones de paquete creativo. De lo contrario, los valores seleccionados se agrupan en un nodo de destino.

1. Haga clic en **[!UICONTROL Add Node]**.

1. (Opcional) Para cambiar el nombre de un nodo de destino definido por el usuario, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, escriba **[!UICONTROL Node Name]** y, a continuación, haga clic en **[!UICONTROL Save]**.

   No puede cambiar el nombre de un nodo &quot;Todos&quot; o &quot;Todos los demás&quot;.

1. [Asigne paquetes creativos](experience-assign-creative-bundles.md#ai-editor) a los nuevos nodos finales, incluida la rama de reserva, o use elementos creativos predeterminados al [guardar la experiencia](#save).

## Uso del editor manual {#manual-editor}

[Abra el editor manual](experience-edit-targeting.md#experience-open) antes de seguir estos pasos.

1. En el nodo en el que desea insertar el destino, haga clic en ![Agregar](/help/creative/assets/add.png "Agregar") y, a continuación, seleccione **[!UICONTROL Insert New Target]**.

1. Especifique los valores objetivo para la categoría:

   * Para destinos de audiencia:

     1. Seleccione **[!UICONTROL Audience]** y haga clic en **[!UICONTROL Click to Browse]** para abrir las opciones de **[!UICONTROL Audience Targeting]**.

     1. Configure los segmentos y grupos de audiencia:

        * Para añadir el primer segmento, localícelo en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento.

        * Para agregar segmentos a un grupo de segmentos existente:

          1. Haga clic en el grupo de segmentos en el panel derecho.

          1. (Opcional) Cambie la lógica de grupo a **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**, según sea necesario.

             **[!UICONTROL Include Any]** coincide con los usuarios de al menos un segmento seleccionado; **[!UICONTROL Include All]** requiere pertenencia en todos los segmentos seleccionados.

             **[!UICONTROL Exclude All]** no está disponible para el primer grupo de segmentos. Para una audiencia que incluya solamente exclusiones, genere la audiencia con **[!UICONTROL Include Any]** y luego excluya esa audiencia cuando la agregue a una ubicación dentro de su DSP.

          1. Busque el nuevo segmento en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento. Repita el proceso para cada segmento adicional.

             El grupo de segmentos se actualiza automáticamente con los nuevos segmentos.

        * Para agregar un nuevo grupo de segmentos:

          1. Haga clic en **[!UICONTROL + New Group]** en el panel derecho.

          1. (Opcional) Cambie la lógica entre el grupo anterior y el nuevo a **[!UICONTROL And]** o **[!UICONTROL Or]**, según sea necesario.

             **[!UICONTROL And]** requiere que los usuarios cumplan las condiciones de ambos grupos; **[!UICONTROL Or]** requiere que cumplan al menos las condiciones de un grupo.

          1. Busque los segmentos para el nuevo grupo en el panel izquierdo y seleccione las casillas de verificación situadas junto a los nombres de los segmentos.

          1. (Opcional) Cambie la lógica de grupo a **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**, según sea necesario.

     1. Haga clic en **[!UICONTROL Create]**.

     1. Haga clic en **[!UICONTROL Apply]**.

   * Para los destinos geográficos, seleccione una sola categoría geográfica (como **[!UICONTROL Geo: Country]**) y, a continuación, haga lo siguiente:

     1. Haga clic en **[!UICONTROL Click to Browse]** para abrir las opciones de [!UICONTROL Geo Targeting], especificar uno o varios destinos geográficos y, a continuación, haga clic en **[!UICONTROL Save]**.

        Los destinos de código postal tienen opciones de edición masiva. Para pegar varios códigos postales, haga clic en la ficha **[!UICONTROL Paste postal codes]**, seleccione el país, pegue o escriba códigos postales separados por comas o en líneas independientes y, a continuación, haga clic en **[!UICONTROL Include All]**. Para quitar un destino de código postal incluido, mantenga el cursor sobre el destino y haga clic en ![Quitar](/help/creative/assets/delete.png "Quitar") **[!UICONTROL Remove]**.

     1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

        Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada destino geográfico especificado. Si no divide los destinos, el usuario debe pertenecer a todas las ubicaciones especificadas (una instrucción [!DNL Boolean] `AND`).

     1. Haga clic en **[!UICONTROL Apply]**.

   * Para un destino de paso de datos, seleccione **[!UICONTROL Data Pass]**; si lo desea, personalice la clave de paso de datos, escriba un único valor de paso de datos y haga clic en **[!UICONTROL Apply]**.

     La clave de paso de datos predeterminada está configurada en el campo **[!UICONTROL Data Pass]** de la sección **[!UICONTROL Advanced]** de la [configuración general de la experiencia](experience-settings-targeting.md). Personalice la clave del destinatario si es necesario.

   * Para un destino de píxel de retargeting, seleccione **[!UICONTROL RT Pixel]**, seleccione un único píxel de retargeting para usar y los valores de cualquiera de los atributos del píxel necesarios para mostrar los elementos creativos y, a continuación, haga clic en **[!UICONTROL Apply]**.

     Los atributos disponibles están configurados en la [configuración de píxeles de retargeting](/help/creative/pixels/retargeting-pixel-manage.md).

   * Para los destinos de dispositivo, haga lo siguiente:

     1. Seleccione una sola categoría de destino (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** o **[!UICONTROL Device: Browser]**) y, a continuación, seleccione los destinos.

     1. (Opcional) Para crear varios nodos de destino cuando se especifiquen varios destinos geográficos, seleccione **[!UICONTROL Split targets to create nodes]**.

        Esta función crea un nodo de destino independiente (con paquetes creativos independientes) para cada destino geográfico especificado. Si no divide los destinos, el usuario debe pertenecer a todas las ubicaciones especificadas (una instrucción [!DNL Boolean] `AND`).

     1. Haga clic en **[!UICONTROL Apply]**.

1. (Opcional) Especifique un nombre de rama personalizado para una rama definida por el usuario.

   De forma predeterminada, las ramas definidas por el usuario se etiquetan con los destinos aplicados.

   No se puede crear un nombre de rama personalizado para una rama &quot;Todos&quot; o &quot;Todos los demás&quot;.

   1. Mantenga el cursor sobre el nodo de destino y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Escriba **[!UICONTROL Node Name]** y haga clic en **[!UICONTROL Save]**.

1. (Opcional) [Asigne paquetes creativos](experience-assign-creative-bundles.md#manual-editor) al nuevo nodo de destino y al nodo &quot;Todo lo demás&quot;.

## Guarde la experiencia {#save}

Los siguientes pasos se aplican a ambos editores.

{{$include /help/_includes/experience-save.md}}

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
