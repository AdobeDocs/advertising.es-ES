---
title: Glosario
description: Consulte las definiciones de términos clave.
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Glosario {#glossary}

*Beta cerrada*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**pulsación:** Un clic en un anuncio que genera una conversión.

DSP **destino de paso de datos:** Los destinos de paso de datos permiten seleccionar elementos de anuncio en función de los datos proporcionados en tiempo real por el administrador, el editor o el socio. Esto puede incluir datos de terceros.

<!-- verify this -->En una experiencia publicitaria, cada destino de paso de datos puede incluir hasta cinco pares clave-valor; se especifican las claves y al menos un valor en el primer nodo de destino de ese nivel y las mismas claves están disponibles para los nodos de destino hermanos. Cada uno de los pares clave-valor se anexa como una macro a la etiqueta de anuncio para esta experiencia. DSP En el momento de la impresión del anuncio, el editor o socio es el responsable de reemplazar los valores por datos específicos de esa impresión. La información se pasa de nuevo a [!DNL Creative] para que pueda mostrar una experiencia publicitaria adecuada en función de las reglas definidas en la experiencia.

Por ejemplo, para dirigirse a uno o más posibles creativos para visualizadores que son mujeres y están en el segmento 1234, debe configurar los destinos de paso de datos `gender=female` y `segment=1234` para el nodo de destino. DSP La etiqueta que sirve la impresión rellena la etiqueta con la información de género y segmento, y a los visitantes que cumplen los requisitos especificados se les muestra uno de los creativos asociados.

**participación:** Participación en un anuncio (como ver un vídeo o expandir un anuncio) que genera una conversión.

<!-- or flexible html5 creative variation? -->
**variación de un recurso creativo flexible de HTML5:** Derivación de un recurso creativo flexible de HTML5 en su [!UICONTROL Creative Libraries], que se genera al asignar el recurso creativo a una experiencia y al cambiar cualquiera de los atributos predeterminados dentro de la experiencia.

<!-- Not sure if this will be implemented, and how:
You can view all derived creatives, including not only the base creatives you've added but also each child creative derivation, in the card view in [!UICONTROL Creative] > [!UICONTROL Libraries]. In the toolbar, click __?__ , and then select Derived Creatives. [Clarify how to tell which have variations. I can't find any now.]
-->

**visualización:** Una impresión de anuncio o una cadena de impresiones que genera una conversión sin que el usuario haga clic en un anuncio.
