---
title: Glosario
description: Consulte las definiciones de términos clave.
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Glosario {#glossary}

*Beta cerrada*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**pulsación:** Un clic en un anuncio que genera una conversión.

**destino de paso de datos:** Los destinos de paso de datos permiten seleccionar elementos de publicidad en función de los datos proporcionados en tiempo real por el DSP, el editor o el socio. Esto puede incluir datos de terceros.

<!-- verify this -->En una experiencia publicitaria, cada destino de paso de datos puede incluir hasta cinco pares clave-valor; se especifican las claves y al menos un valor en el primer nodo de destino de ese nivel y las mismas claves están disponibles para los nodos de destino hermanos. Cada uno de los pares clave-valor se anexa como una macro a la etiqueta de anuncio para esta experiencia. En el momento de la impresión del anuncio, DSP, el editor o el socio son responsables de reemplazar los valores por datos específicos de esa impresión. La información se pasa de nuevo a [!DNL Creative] para que pueda mostrar una experiencia publicitaria adecuada en función de las reglas definidas en la experiencia.

Por ejemplo, para dirigirse a uno o más posibles creativos para visualizadores que son mujeres y están en el segmento 1234, debe configurar los destinos de paso de datos `gender=female` y `segment=1234` para el nodo de destino. La DSP que sirve la impresión rellena la etiqueta con la información de sexo y segmento, y a los visitantes que cumplen los requisitos especificados se les muestra uno de los elementos creativos asociados.

**participación:** Participación en un anuncio (como desplazarse por un anuncio de carrusel o expandir un anuncio) que genera una conversión. Este tipo de evento es independiente de hacer clic en el anuncio para llegar a una página de aterrizaje o a un evento de la página de aterrizaje.

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**visualización:** Una impresión de anuncio o una cadena de impresiones que genera una conversión sin que el usuario haga clic en un anuncio.
