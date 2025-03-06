---
title: Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia
description: Aprenda a asignar elementos creativos a cada destinatario en sus experiencias publicitarias.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
source-git-commit: 115b769c2880936c422747b44f43b4be7281916d
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Asignar y cancelar la asignación de paquetes creativos a un nodo final en una experiencia

*Solo experiencias con direccionamiento en árbol de decisiones*
*Beta cerrada*

Puede asignar paquetes creativos a un nodo de destino en el nivel inferior de un árbol de decisión de experiencias. En el caso de las experiencias para las que no ha configurado objetivos, el nivel inferior se encuentra en &quot;Todo&quot;.

Para las experiencias de publicidad estándar, solo puede asignar paquetes creativos estándar. Para las experiencias de publicidad dinámica, solo puede asignar paquetes creativos dinámicos.

>[!NOTE]
>
>Si no asigna al menos un paquete creativo a cada nodo final, puede optar por usar los elementos creativos predeterminados para cada nodo no asignado al [guardar la experiencia](experience-create-targeting.md). Para publicar una experiencia, debe asignar paquetes o utilizar los elementos creativos predeterminados para cada nodo final.

<!-- 1. [ways to get to the decision tree] -->

1. Realice una de las siguientes acciones:

   * (Nodos finales sin elementos creativos) En el nodo, haga clic en ![Agregar](/help/creative/assets/add.png "Agregar") y, a continuación, seleccione **[!UICONTROL Assign Bundles]**.

   * (Nodos con elementos creativos existentes) Mantenga el cursor sobre el cuadro del paquete creativo debajo del nodo de destino <!-- wording???? --> y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Seleccione la casilla de verificación situada junto a cada paquete para asignarlo al nodo de destino y anule la selección de la casilla de verificación situada junto a cada paquete para anular la asignación.

   Solo se muestran los paquetes del tipo de paquete relevante para la experiencia (estándar o dinámica).

1. Haga clic en **[!UICONTROL Attach to Bundles]**.

1. (Opcional) [Personalice las direcciones URL de seguimiento para los creativos en los paquetes asignados](experience-tracking-urls-targeting.md).

1. (Opcional) [Personalice la optimización y la programación creativas](experience-optimization-scheduling-targeting.md) para los paquetes asignados.

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Agregar un nodo de destino al nivel final](experience-target-node-add-final.md)
>* [Insertar un nodo de destino entre nodos](experience-target-node-add-inner.md)
>* [Agregar un nodo de destino secundario entre nodos](experience-target-node-add-sibling.md)
>* [Copiar nodos secundarios y creativos a otro nodo en el mismo nivel](experience-target-node-copy.md)
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
>* [Configuración de experiencia de destino](experience-settings-targeting.md)
>* [Exportar e implementar una etiqueta de experiencia de anuncio para una experiencia en vivo](experience-tag-export.md)
