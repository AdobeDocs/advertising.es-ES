---
title: Copiar nodos secundarios a otro nodo de destino en el mismo nivel
description: Obtenga información sobre cómo copiar todos los nodos secundarios de un nodo de destino principal a otro nodo de destino en el mismo nivel
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
source-git-commit: 5d8b511708008c77e817ccdb00ae02c158dfe63e
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Copiar nodos secundarios a otro nodo de destino en el mismo nivel

*Solo experiencias con direccionamiento en árbol de decisiones*
*Beta cerrada*

Puede copiar todos los nodos secundarios de un nodo de destino principal (incluidos todos los destinos secundarios y los paquetes creativos asignados a ellos) a otro nodo de destino en el mismo nivel. Puede copiar los nodos: a) añadiendo los nodos copiados al marco de trabajo existente o b) reemplazando completamente el marco de trabajo existente. <!-- Give the main use case or an example to explain. -->

Esta característica no afecta al destino especificado para el nodo principal, sólo afecta a los nodos secundarios.

<!-- 1. [ways to get to the decision tree] -->

1. Haga clic en el nodo principal cuyos elementos secundarios desee copiar, haga clic en ![Agregar](/help/creative/assets/add.png "Agregar") y, a continuación, seleccione **[!UICONTROL Copy Children ctrl+c]** o b\) escriba **[!UICONTROL Ctrl+C]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-C]** ([!DNL Apple Macintosh]) en el teclado.

1. Realice una de las acciones siguientes:

   * Para reemplazar todos los nodos secundarios y creativos de un nodo, haga clic en el nodo en el que desea pegar la información copiada, haga clic en **...** y, a continuación, seleccione **[!UICONTROL Replace ctrl+shift+v]** o b\) escriba **[!UICONTROL Ctrl+Shift+V]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-Shift-V]** ([!DNL Apple Macintosh]) en el teclado.

   * (Nodos con varios destinos secundarios, sin nodos &quot;Todos&quot; y sin creativos únicamente) Para agregar todos los nodos secundarios y creativos a un nodo, sin eliminar los existentes, haga clic en el nodo al que desea pegar la información copiada, haga clic en **...** y, a\) seleccione **[!UICONTROL Add ctrl+v]** **&#x200B; o b\) escriba &#x200B;** [!UICONTROL Ctrl+V] **&#x200B; ([!DNL Microsoft Windows]) o &#x200B;** [!UICONTROL Command-V]** ([!DNL Apple Macintosh]) en el teclado.

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
>* [Asignar elementos creativos a un nodo final](experience-assign-creative-bundles.md)
>* [Eliminar un nodo de destino o de hoja creativa](/help/creative/experiences/experience-target-node-delete.md)
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
>* [Configuración de experiencia de destino](experience-settings-targeting.md)
