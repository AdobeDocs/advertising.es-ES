---
title: Copiar nodos secundarios a otro nodo de destino en el mismo nivel
description: Obtenga información sobre cómo copiar todos los nodos secundarios de un nodo de destino principal a otro nodo de destino en el mismo nivel
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
TQID: 'https://experienceleague.adobe.com/KLKVrggOQ8V99Cd-2PcFEdwImKvLYkskSD-DPDvpwu0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
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
source-wordcount: '403'
ht-degree: 0%
---
# Copiar nodos secundarios a otro nodo de destino en el mismo nivel

*Solo experiencias con direccionamiento en árbol de decisiones*

Puede copiar todos los nodos secundarios de un nodo de destino principal (incluidos todos los destinos secundarios y los paquetes creativos asignados a ellos) a otro nodo de destino en el mismo nivel. Puede copiar los nodos: a) añadiendo los nodos copiados al marco de trabajo existente o b) reemplazando completamente el marco de trabajo existente. <!-- Give the main use case or an example to explain. -->

Esta característica no afecta al destino especificado para el nodo principal, sólo afecta a los nodos secundarios.

## Uso del editor controlado por IA (Beta) {#ai-editor}

Mientras [crea](experience-create-targeting.md#ai-editor) o [edita](experience-edit-targeting.md#ai-editor) la experiencia, use los controles de lienzo:

1. En el nodo principal cuyos elementos secundarios desee copiar, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Copy Children]**.

1. En el nodo de destino en el mismo nivel, haga clic en **[!UICONTROL ...]** y, a continuación, elija una de las siguientes opciones:

   * Para agregar los destinos secundarios y creativos copiados sin eliminar los elementos secundarios existentes, haga clic en **[!UICONTROL Add]**.

   * Para reemplazar los elementos secundarios existentes y los elementos creativos con los elementos secundarios copiados, haga clic en **[!UICONTROL Replace]**.

   Una acción se desactiva cuando la estructura de árbol no la admite. Revise las advertencias antes de continuar.

1. Revise la rama de destino y [guarde la experiencia](#save).

## Uso del editor manual {#manual-editor}

[Abra el editor manual](experience-edit-targeting.md#experience-open) antes de seguir estos pasos.

1. Haga clic en el nodo principal cuyos elementos secundarios desee copiar, haga clic en ![Agregar](/help/creative/assets/add.png "Agregar") y, a continuación, seleccione **[!UICONTROL Copy Children ctrl+c]** o b\) escriba **[!UICONTROL Ctrl+C]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-C]** ([!DNL Apple Macintosh]) en el teclado.

1. Realice una de las acciones siguientes:

   * Para reemplazar todos los nodos secundarios y creativos de un nodo, haga clic en el nodo en el que desea pegar la información copiada, haga clic en **[!UICONTROL ...]** y, a continuación, seleccione **[!UICONTROL Replace ctrl+shift+v]** o b\) escriba **[!UICONTROL Ctrl+Shift+V]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-Shift-V]** ([!DNL Apple Macintosh]) en el teclado.

   * (Nodos con varios destinos secundarios, sin nodos &quot;Todos&quot; y sin creativos solamente) Para agregar todos los nodos secundarios y creativos a un nodo, sin eliminar los existentes, haga clic en el nodo en el que desea pegar la información copiada, haga clic en **[!UICONTROL ...]** y, o bien, seleccione **[!UICONTROL Add ctrl+v]** o b\) escriba **[!UICONTROL Ctrl+V]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-V]** ([!DNL Apple Macintosh]) en el teclado.

## Guarde la experiencia {#save}

Los siguientes pasos se aplican a ambos editores.

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
