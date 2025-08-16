---
title: El diseño del árbol de decisión
description: Obtenga información acerca del diseño del árbol de decisión para experiencias con segmentación.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Diseño del árbol de decisión para experiencias de [!DNL Creative]

Al habilitar la opción &quot;[!UICONTROL Targeting]&quot; para una experiencia, configura la experiencia mediante un árbol de decisión.

Inicialmente, cada árbol de decisión comienza con el nivel raíz, &quot;Todos&quot;. Puede agregar uno o más nodos de destino y, a continuación, asignar paquetes creativos a los nodos finales en cada rama del árbol de decisión. De forma predeterminada, el árbol de decisión se muestra verticalmente, pero también puede verlo horizontalmente.

![Ejemplo de árbol de decisión vertical sin destinos](/help/creative/assets/experience-decision-tree-no-targets.png "Ejemplo de árbol de decisión vertical sin destinos")

![Ejemplo de árbol de decisión horizontal sin destinos](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Ejemplo de árbol de decisión horizontal sin destinos")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
>-->

## Términos

**Árbol:** La estructura general de toma de decisiones como un árbol con ramas.

**Nodo de destino:** Un destino dentro de una rama.

**Nodo de hoja:** Un conjunto de elementos creativos asignados a un nodo de destino final.

## Destinos en un árbol de decisión

Cada árbol de decisión puede tener hasta cinco niveles de destinatarios. Cada nivel de destino puede incluir varias ramas, cada una con uno o más nodos con el mismo tipo de destino (segmento de audiencia, tipo de ubicación geográfica, valores para claves de paso de datos especificadas, atributos para un píxel de retargeting especificado o categoría de dispositivo). Puede asignar paquetes creativos en cada tamaño de anuncio para el que haya especificado un creativo de imagen o vídeo predeterminado a los nodos de destino de nivel inferior.

![Ejemplo de árbol de decisión con destinos](/help/creative/assets/experience-decision-tree.png "Ejemplo de árbol de decisión con destinos")

Cuando se añade un nodo de destino al nivel final, se especifica el destino para el nuevo nodo. Se crea automáticamente un nodo secundario adicional, &quot;Todo lo demás&quot;, para todos los que no coincidan con el destino especificado. A continuación, puede agregar nodos hermanos adicionales con diferentes destinos del mismo tipo.

Sin embargo, cuando se inserta un nodo de destino entre los niveles existentes, el primer nodo del nuevo nivel se asigna inicialmente a &quot;Todo&quot;. Para identificar un objetivo específico, cree un nodo de destino relacionado en el mismo nivel, para el cual especifique el objetivo real. Esta acción crea el nodo de destino y reemplaza el nodo &quot;Todo&quot; por un nodo &quot;Todo lo demás&quot; (que incluye todos los paquetes creativos asignados previamente a Todo). A continuación, puede agregar nodos hermanos adicionales con diferentes destinos del mismo tipo.

Para todos los nodos principales, puede copiar opcionalmente todos los nodos de destino secundarios y paquetes creativos y pegarlos en otro nodo en el mismo nivel. Puede agregar los nodos pegados al marco de trabajo existente o reemplazar el marco de trabajo existente por ellos.

## Creativos en un árbol de decisión

Asigne paquetes creativos a cada nodo de destino final de la experiencia.

Dentro de cada nodo con paquetes creativos, puede rotar opcionalmente los creativos incluidos: a) según pesos especificados o b) algorítmicamente para optimizar la tasa de pulsaciones o un objetivo personalizado. Si lo desea, también puede rotar los elementos creativos en una secuencia temporal especificada utilizando las mismas opciones.

Opcionalmente, puede personalizar las direcciones URL de la página de aterrizaje, las direcciones URL de seguimiento de impresiones y las direcciones URL de seguimiento de clics, según sea necesario para los creativos individuales. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Acerca de las experiencias en Advertising Creative 2.0](experience-about.md)
>* [Crear una experiencia con segmentación](/help/creative/experiences/experience-create-targeting.md)
>* [Configuración de experiencia de destino](/help/creative/experiences/experience-settings-targeting.md)
