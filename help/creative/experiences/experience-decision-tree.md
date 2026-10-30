---
title: El diseño del árbol de decisión
description: Obtenga información acerca de los editores de árbol de decisiones manuales y controlados por IA para experiencias con segmentación.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
TQID: 'https://experienceleague.adobe.com/JFrcVBHxv90Fchk-VfkmxAITQJswboszNMFOfaAQlL4'
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
source-wordcount: '807'
ht-degree: 0%
---
# Diseño del árbol de decisión para experiencias de [!DNL Creative]

Al habilitar la opción &quot;[!UICONTROL Targeting]&quot; para una experiencia, configura la experiencia mediante un árbol de decisión.

Inicialmente, cada árbol de decisión comienza con el nivel raíz, &quot;Todos&quot;. Puede agregar uno o más nodos de destino y, a continuación, asignar paquetes creativos a los nodos finales en cada rama del árbol de decisión.

## Editor impulsado por IA (Beta) {#ai-editor}

El editor controlado por IA se abre de forma predeterminada al crear o editar una experiencia con segmentación. Combina una conversación con el agente de IA y un lienzo interactivo del árbol de decisiones.

* Describa la estructura de segmentación o los cambios que desee en la conversación y revise el árbol resultante antes de guardar.

* Edite el lienzo directamente para añadir niveles y nodos de destino, asignar paquetes y configurar la optimización creativa y las direcciones URL de seguimiento. No es necesario cambiar al editor manual para utilizar estos controles.

* Vea el nombre de la experiencia, el estado y el anunciante en el encabezado y utilice los ID de nodo, cuando estén disponibles, para identificar nodos de destino cuando describa los cambios.

* Use **[!UICONTROL Zoom in]**, **[!UICONTROL Zoom out]** y **[!UICONTROL Change orientation]** para ajustar la vista. **[!UICONTROL Reset tree]** borra el árbol después de la confirmación; no sólo restablece el zoom.

Mientras el asistente procesa un cambio, el lienzo y su botón **[!UICONTROL Save]** se desactivan temporalmente. Espere a que finalice el procesamiento antes de realizar otro cambio en el lienzo.

## Editor manual {#manual-editor}

Para abrir el editor manual existente desde el editor controlado por IA, haga clic en **[!UICONTROL Manual Decision Tree]**. También puede seleccionar **[!UICONTROL Create Decision Tree Manually (Legacy)]** de las acciones de la experiencia en la vista [!UICONTROL Experiences]. Consulte [Cambiar de editor o editar la configuración de la experiencia](experience-edit-targeting.md#switch-editors).

En el editor manual, el árbol se muestra verticalmente de forma predeterminada. Puede cambiar a una vista horizontal y ajustar el zoom con un control deslizante. La configuración de la vista se guardará hasta que cierre la sesión.

Los siguientes ejemplos muestran el editor manual:

![Ejemplo de árbol de decisión vertical sin destinos](/help/creative/assets/experience-decision-tree-no-targets.png "Ejemplo de árbol de decisión vertical sin destinos")

![Ejemplo de árbol de decisión horizontal sin destinos](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Ejemplo de árbol de decisión horizontal sin destinos")

>[!IMPORTANT]
>
>Guarde los cambios que desee conservar antes de salir del editor controlado por IA. Al hacer clic en **[!UICONTROL Manual Decision Tree]**, **[!UICONTROL Experience Form]** o **[!UICONTROL Cancel]**, se abre un cuadro de diálogo de confirmación. Al hacer clic en **[!UICONTROL Yes]**, se descartarán los cambios de árbol no guardados; al hacer clic en **[!UICONTROL No]**, permanecerá en el editor.

## Términos

**Árbol:** La estructura general de toma de decisiones como un árbol con ramas.

**Nodo de destino:** Un destino dentro de una rama.

**Nodo de hoja:** Un conjunto de elementos creativos asignados a un nodo de destino final.

## Destinos en un árbol de decisión

Cada árbol de decisión puede tener hasta cinco niveles de destinatarios. Los objetivos de nivel de experiencia se aplican junto con las opciones de segmentación de DSP; el comportamiento de la segmentación jerárquica puede variar en DSP. Asegúrese de que las experiencias publicitarias incluyan una segmentación compatible con las campañas en las que la va a implementar.

Cada nivel de destino puede incluir varias ramas, cada una con uno o más nodos con el mismo tipo de destino (segmento de audiencia, tipo de ubicación geográfica, valores para claves de paso de datos especificadas, atributos para un píxel de retargeting especificado o categoría de dispositivo). Puede asignar paquetes creativos en cada tamaño de anuncio para el que haya especificado un creativo de imagen o vídeo predeterminado a los nodos de destino de nivel inferior.

<!-- Add a screen shot of the AI editor -->El siguiente ejemplo muestra los destinos en el editor manual:

![Ejemplo de árbol de decisión con destinos](/help/creative/assets/experience-decision-tree.png "Ejemplo de árbol de decisión con destinos")

Cuando se añade un nodo de destino al nivel final, se especifica el destino para el nuevo nodo. Se crea automáticamente un nodo secundario adicional, &quot;Todo lo demás&quot;, para todos los que no coincidan con el destino especificado. A continuación, puede agregar nodos hermanos adicionales con diferentes destinos del mismo tipo.

Sin embargo, cuando se inserta un nodo de destino entre los niveles existentes, el primer nodo del nuevo nivel se asigna inicialmente a &quot;Todo&quot;. Para identificar un objetivo específico, cree un nodo de destino relacionado en el mismo nivel, para el cual especifique el objetivo real. Esta acción crea el nodo de destino y reemplaza el nodo &quot;Todo&quot; por un nodo &quot;Todo lo demás&quot; (que incluye todos los paquetes creativos asignados previamente a Todo). A continuación, puede agregar nodos hermanos adicionales con diferentes destinos del mismo tipo.

Para todos los nodos principales, puede copiar opcionalmente todos los nodos de destino secundarios y paquetes creativos y pegarlos en otro nodo en el mismo nivel. Puede agregar los nodos pegados al marco de trabajo existente o reemplazar el marco de trabajo existente por ellos.

## Creativos en un árbol de decisión

Asigne paquetes creativos a cada nodo de destino final de la experiencia.

Dentro de cada nodo con paquetes creativos, puede rotar opcionalmente los creativos incluidos a) de forma algorítmica para optimizar la tasa de pulsaciones o un objetivo personalizado, b) según pesos especificados, o c) en una secuencia específica. Si lo desea, también puede rotar los elementos creativos de una secuencia temporal especificada con cualquier combinación de las mismas opciones.

Opcionalmente, puede personalizar las direcciones URL de la página de aterrizaje, las direcciones URL de seguimiento de impresiones y las direcciones URL de seguimiento de clics, según sea necesario para los creativos individuales. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Acerca de las experiencias en Advertising Creative 2.0](experience-about.md)
>* [Crear una experiencia con segmentación](/help/creative/experiences/experience-create-targeting.md)
>* [Configuración de experiencia de destino](/help/creative/experiences/experience-settings-targeting.md)
