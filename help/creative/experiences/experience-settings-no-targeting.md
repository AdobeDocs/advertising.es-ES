---
title: Configuración de experiencias sin objetivo
description: Consulte las descripciones de todas las configuraciones para experiencias de publicidad sin segmentación del árbol de decisiones.
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 0%

---

# Configuración de experiencias sin objetivo

*Beta cerrada*

## [!UICONTROL Experience basics] sección

**[!UICONTROL Ad Type]:** (de solo lectura para experiencias existentes) El tipo de anuncios incluidos en la experiencia: *[!UICONTROL Standard Display]*, *[!UICONTROL Dynamic Display]* o *[!UICONTROL Video]*. Una vez guardada la experiencia, no se puede cambiar el tipo de anuncio.

**[!UICONTROL Advertiser]:** (solo lectura para experiencias existentes) El anunciante que pujará por los creativos incluidos en la experiencia. Una vez guardada la experiencia, no se puede cambiar el anunciante.

**[!UICONTROL Experience Name]:** Un nombre único para la experiencia. **Sugerencia:** Use un nombre que pueda encontrar fácilmente cuando use la experiencia como anuncio en Advertising DSP u otro DSP.

**[!UICONTROL Creative Library]:** (solo lectura para experiencias existentes) Una sola biblioteca creativa para usar en la experiencia. Una vez guardada la experiencia, no se puede cambiar la biblioteca.

## [!UICONTROL Default creatives] sección

**\[Creativos predeterminados especificados\]:** Los creativos predeterminados que se deben usar cuando un explorador no puede mostrar los creativos asignados a la experiencia, como cuando el explorador no está habilitado para JavaScript o el servidor de publicidad no puede personalizar el anuncio debido a retrasos. Para las experiencias de visualización estándar, incluya un creativo de imágenes por tamaño de anuncio al que se aplique la experiencia. Para las experiencias de vídeo estándar, incluya un creativo de vídeo por tamaño de anuncio al que se aplique la experiencia. Las opciones determinan los tamaños creativos que se pueden utilizar para la experiencia.

En el caso de las experiencias sin segmentación en el árbol de decisiones, puede anular los elementos creativos predeterminados con elementos creativos del mismo tamaño en [!UICONTROL Tag Manager].

* Para agregar un elemento creativo predeterminado con diferentes dimensiones, haga clic en **[!UICONTROL + Add Sizes]**, active la casilla de verificación situada junto a cada elemento creativo que desee agregar en el panel derecho y, a continuación, haga clic en **[!UICONTROL Add Creatives]**.

* Para eliminar un elemento creativo predeterminado, mantenga el cursor sobre la miniatura creativa y haga clic en ![Eliminar](/help/creative/assets/delete.png "Eliminar").

* Para eliminar todos los elementos creativos predeterminados, haga clic en ![Eliminar](/help/creative/assets/delete.png "Eliminar") **[!UICONTROL Delete all]**.

* Para mostrar u ocultar el panel Creativos de la derecha, haga clic en ![Mostrar/Ocultar](/help/creative/assets/hide-show-creatives.png "Mostrar/Ocultar") en la parte superior derecha del panel derecho.

## [!UICONTROL Targeting] sección

**[!UICONTROL Targeting]:** (solo lectura para experiencias existentes) No aplicable cuando no habilita el direccionamiento mediante un árbol de decisión; mantenga deshabilitada esta opción. **Nota:** Una vez guardada una experiencia sin segmentación, no se puede agregar la segmentación más adelante.

**[!UICONTROL Language Targeting]:** (solo experiencias con anuncios estándar; opcional; solo lectura para experiencias existentes) Comprueba la configuración de idioma del explorador del usuario y muestra un elemento creativo en el idioma especificado cuando hay un elemento creativo disponible en ese idioma. Cuando un elemento creativo en el idioma especificado por el explorador no está disponible, se utiliza la configuración [!UICONTROL Preferred language] en su lugar. Una vez guardada la experiencia, no se puede cambiar esta configuración.

**[!UICONTROL Preferred language]:** (Experiencias solo con anuncios estándar; solo lectura para experiencias existentes) El idioma para todos los anuncios creados a partir de la experiencia, excepto cuando [!UICONTROL Language Targeting] está habilitado. Una vez guardada la experiencia, no se puede cambiar esta configuración.

## [!UICONTROL Advanced] sección

**Transferencia de datos:** (experiencias solo con anuncios dinámicos; opcional) Para dirigirse a usuarios en función de pares clave-valor específicos que DSP, el editor o el socio transfieren en tiempo real al imprimir (como SKU=01234567890123 o Cart=empty). Puede especificar hasta cinco claves de paso de datos (parámetros).<!-- May move this to just within the decision tree. -->

Cuando se crea una etiqueta de experiencia de anuncio para un tamaño creativo específico, cada clave especificada en este campo se anexa como una macro en la etiqueta. Introduzca el valor de cada par clave-valor dentro de la etiqueta antes de implementar la etiqueta como un anuncio en DSP.

**Radio:** (solo experiencias con anuncios dinámicos; opcional) Un radio de un código postal de Estados Unidos especificado en el archivo de fuente para el destino; seleccione un radio de 0 millas a 200 millas. El archivo de fuente utilizado para crear los anuncios dinámicos para la experiencia debe incluir una columna [!UICONTROL ZIP]<!-- or a user-named column mapped to a ZIP column --> con un valor para cada fila de producto en el archivo. Por ejemplo, para un radio de 10 millas, un anuncio de un producto disponible en 95110 se puede mostrar a los usuarios en un radio de 10 millas de 95110 (determinado por la dirección IP del usuario).

**Píxel RT:** (solo experiencias con anuncios dinámicos; opcional) Un píxel de retargeting de [!UICONTROL Creative] a destino potencial. Al configurar el direccionamiento dentro del árbol de decisión, puede incluir un nivel de nodos de destino de píxeles de RT. Para cada nodo, se especifica el píxel de destino y los valores de los atributos del píxel necesarios para mostrar los elementos creativos en los paquetes de elementos creativos asignados. Si no especifica un píxel en este campo, puede especificar uno dentro del árbol de decisión.<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup." Clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]:**<!-- should be "Labels" --> (Opcional) Cualquier etiqueta específica de [!DNL Creative] que se aplique a la experiencia. Puede filtrar experiencias por etiqueta en la vista Experiencias e incluir la dimensión [!UICONTROL Experience Label] en [!UICONTROL Custom Creative Report].

* Para seleccionar etiquetas existentes, haga clic en ![Abajo](/help/creative/assets/chevron-down.png "Abajo") y active la casilla de verificación situada junto a cada etiqueta que desee aplicar.

* Para buscar etiquetas existentes, empiece a introducir una cadena de texto dentro del nombre de la etiqueta.

* Para crear una etiqueta nueva para aplicar, abra la lista, haga clic en **+ Agregar etiqueta**, escriba un nombre de etiqueta nuevo en el campo [!UICONTROL Label] y, a continuación, haga clic en **Crear**.

* Para quitar una etiqueta, anule la selección de la casilla de verificación situada junto al nombre de la etiqueta.

**[!UICONTROL Impression Tracking URL]:** (opcional) una dirección URL de seguimiento de impresiones de terceros que se anexará a la dirección URL de la página de aterrizaje para cualquier anuncio creado a partir de la experiencia. Se pueden incluir hasta cinco direcciones URL. Para agregar una dirección URL adicional, haz clic en ![icono](/help/creative/assets/create.png) **[!UICONTROL Add More] e ingresa la dirección URL.

Una vez que ingrese una dirección URL, todas las [macros disponibles](/help/creative/creative-macros.md) y los datos con los que se sustituyen se mostrarán más adelante en la página. Para insertar una de las macros en la dirección URL, mantenga el cursor sobre la descripción de la macro y haga clic en ![Copiar al portapapeles](/help/creative/assets/copy-to-clipboard.png "Copiar al portapapeles") y, a continuación, pegue la macro donde desee en el campo URL.

>[!NOTE]
>
>* [!DNL Creative] prefija automáticamente sus propias etiquetas de seguimiento de impresiones a la dirección URL de la página de aterrizaje.
>* Puede omitir esta URL para cualquier creativo de la experiencia.
>* También puede introducir código de seguimiento de impresiones de JavaScript de terceros en el campo [!UICONTROL Client JS]

**[!UICONTROL Click Tracking URL]:** (opcional) (opcional) una dirección URL de seguimiento de clics de terceros que se anexará a la dirección URL de la página de aterrizaje. Se pueden incluir hasta cinco direcciones URL. Para agregar una dirección URL adicional, haz clic en ![icono](/help/creative/assets/create.png) **[!UICONTROL Add More]** e ingresa la dirección URL.

Una vez que ingrese una dirección URL, todas las [macros disponibles](/help/creative/creative-macros.md) y los datos con los que se sustituyen se mostrarán más adelante en la página. Para insertar una de las macros en la dirección URL, mantenga el cursor sobre la descripción de la macro y haga clic en ![Copiar al portapapeles](/help/creative/assets/copy-to-clipboard.png "Copiar al portapapeles") y, a continuación, pegue la macro donde desee en el campo URL.

>[!NOTE]
>
>* [!DNL Creative] prefija automáticamente sus propias etiquetas de seguimiento de impresiones a la dirección URL de la página de aterrizaje.
>* Puede anular esta dirección URL para cualquier <!-- creative bundle for targeted experiences --> creativo de la experiencia.

**[!UICONTROL Client JS]:** (Opcional) Cualquiera de los siguientes:

* (Cuando el anunciante utiliza un proveedor de cumplimiento de OBA para los anuncios) Código JavaScript que señala a la superposición de anuncio que permite a los usuarios excluirse de la segmentación por comportamiento en línea (OBA).

* Cualquier código de seguimiento de impresiones de JavaScript de terceros que se adjunte a la página de aterrizaje. **Nota:** También puede escribir una dirección URL de seguimiento de impresiones de terceros en el campo [!UICONTROL Impression Tracking URL].

>[!MORELIKETHIS]
>
>* [Crear una experiencia sin segmentación de árbol de decisión](experience-create-no-targeting.md)
>* [Editar una experiencia sin segmentación de árbol de decisión](experience-edit-no-targeting.md)
>* [Macros disponibles para URL de seguimiento](/help/creative/creative-macros.md)
>* [Crear manualmente una etiqueta de anuncio para un tamaño creativo aplicable](experience-tag-create-manually.md)
>* [Asignar elementos creativos a una etiqueta de anuncio para experiencias sin segmentación](experience-tag-assign-creatives.md)
>* [Personalizar las direcciones URL de seguimiento para una experiencia sin segmentación](experience-tracking-urls-no-targeting.md)
>* [Personalizar la optimización creativa y la programación de una experiencia sin segmentación](experience-optimization-scheduling-no-targeting.md)
