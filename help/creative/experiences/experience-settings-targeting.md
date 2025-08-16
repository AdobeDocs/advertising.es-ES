---
title: Configuración de experiencias segmentadas
description: Consulte las descripciones de todos los ajustes para experiencias de anuncios segmentados.
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 0%

---

# Configuración de experiencias publicitarias segmentadas

## [!UICONTROL Experience basics] sección

**[!UICONTROL Ad Type]:** (de solo lectura para experiencias existentes) El tipo de anuncios incluidos en la experiencia: *[!UICONTROL Standard Display]*, *[!UICONTROL Dynamic Display]* o *[!UICONTROL Video]*. Una vez guardada la experiencia, no se puede cambiar el tipo de anuncio.

**[!UICONTROL Advertiser]:** (solo lectura para experiencias existentes) El anunciante que pujará por las combinaciones creativas y de destino incluidas en la experiencia. Una vez guardada la experiencia, no se puede cambiar el anunciante.

**[!UICONTROL Experience Name]:** Un nombre único para la experiencia. **Sugerencia:** Use un nombre que pueda encontrar fácilmente cuando use la experiencia como anuncio en Advertising DSP u otro DSP.

**[!UICONTROL Creative Library]:** (solo lectura para experiencias existentes) Una sola biblioteca creativa para usar en la experiencia. Una vez guardada la experiencia, no se puede cambiar la biblioteca.

## [!UICONTROL Default creatives] sección

**\[Creativos predeterminados especificados\]:** Los creativos predeterminados que se deben usar cuando un explorador no puede mostrar los creativos asignados a la experiencia, como cuando el explorador no está habilitado para JavaScript o el servidor de publicidad no puede personalizar el anuncio debido a retrasos. Para las experiencias de visualización estándar, incluya un creativo de imágenes por tamaño de anuncio al que se aplique la experiencia. Para las experiencias de vídeo estándar, incluya un creativo de vídeo por tamaño de anuncio al que se aplique la experiencia. Las opciones determinan los tamaños creativos que se pueden utilizar para la experiencia.

En el caso de las experiencias con segmentación del árbol de decisión, puede anular los elementos creativos predeterminados con paquetes creativos que contengan elementos creativos del mismo tamaño desde el árbol de decisión.<!-- verify -->

* Para agregar un elemento creativo predeterminado con diferentes dimensiones, haga clic en **[!UICONTROL + Add Sizes]**, active la casilla de verificación situada junto a cada elemento creativo que desee agregar en el panel derecho y, a continuación, haga clic en **[!UICONTROL Add Creatives]**.

* Para eliminar un elemento creativo predeterminado, mantenga el cursor sobre la miniatura creativa y haga clic en ![Eliminar](/help/creative/assets/delete.png "Eliminar").

* Para eliminar todos los elementos creativos predeterminados, haga clic en ![Eliminar](/help/creative/assets/delete.png "Eliminar") **[!UICONTROL Delete all]**.

* Para mostrar u ocultar el panel Creativos de la derecha, haga clic en ![Mostrar/Ocultar](/help/creative/assets/hide-show-creatives.png "Mostrar/Ocultar") en la parte superior derecha del panel derecho.

## [!UICONTROL Targeting] sección

**[!UICONTROL Targeting]:** (solo lectura para experiencias existentes) Habilita el direccionamiento creativo mediante un árbol de decisión y la creación automática de etiquetas. Una vez guardada la experiencia, no se puede cambiar esta configuración.

**[!UICONTROL Language Targeting]:** (solo experiencias con anuncios estándar; opcional; solo lectura para experiencias existentes) Comprueba la configuración de idioma del explorador del usuario y muestra un elemento creativo en el idioma especificado cuando hay un elemento creativo disponible en ese idioma. Cuando un elemento creativo en el idioma especificado por el explorador no está disponible, se utiliza la configuración [!UICONTROL Preferred language] en su lugar.

Una vez guardada la experiencia, no se puede cambiar esta configuración.

**[!UICONTROL Preferred language]:** (Experiencias solo con anuncios estándar; solo lectura para experiencias existentes) El idioma para todos los anuncios creados a partir de la experiencia, excepto cuando [!UICONTROL Language Targeting] está habilitado. Una vez guardada la experiencia, no se puede cambiar esta configuración.

## [!UICONTROL Advanced] sección

**Pase de datos:** (solo lectura para experiencias existentes; opcional) Para dirigirse a usuarios en función de pares clave-valor específicos que DSP, el editor o el socio pasen en tiempo real al momento de la impresión (como SKU=01234567890123 o Cart=empty). Puede especificar hasta cinco claves de paso de datos predeterminadas (parámetros). Al configurar el direccionamiento dentro del árbol de decisión, puede incluir un nivel de datos para pasar los nodos de destino, personalizar opcionalmente las claves y especificar los valores de destino para cada nodo. Si no especifica ninguna clave en este campo al crear la experiencia, aún puede especificarla dentro del árbol de decisión.

Cada clave se anexa como una macro en la etiqueta de experiencia publicitaria, que puede generar para implementarla como anuncio en DSP.

**Radio:** (solo experiencias con anuncios dinámicos; opcional) Un radio de un código postal de Estados Unidos especificado en el archivo de fuente para el destino; seleccione un radio de 0 millas a 200 millas. El archivo de fuente utilizado para crear los anuncios dinámicos para la experiencia debe incluir una columna [!UICONTROL ZIP]<!-- or a user-named column mapped to a ZIP column --> con un valor para cada fila de producto en el archivo. Por ejemplo, para un radio de 10 millas, un anuncio de un producto disponible en 95110 se puede mostrar a los usuarios en un radio de 10 millas de 95110 (determinado por la dirección IP del usuario).

**Píxel RT:** (solo lectura para experiencias existentes; opcional) Un píxel de retargeting de [!UICONTROL Creative] a destino potencial. Al configurar el direccionamiento dentro del árbol de decisión, puede incluir un nivel de nodos de destino de píxeles de RT. Para cada nodo, se especifica el píxel de destino y los valores de los atributos del píxel necesarios para mostrar los elementos creativos en los paquetes de elementos creativos asignados. Si no especifica un píxel en este campo al crear la experiencia, aún puede especificar uno dentro del árbol de decisión.<!-- May move this to just within the decision tree. -->

**Etiqueta:**<!-- should be "Labels" --> (opcional) Cualquier etiqueta específica de [!DNL Creative] que se aplique a la experiencia. Puede filtrar experiencias por etiqueta en la vista Experiencias e incluir la dimensión [!UICONTROL Experience Label] en [!UICONTROL Custom Creative Report].

* Para seleccionar etiquetas existentes, haga clic en ![Abajo](/help/creative/assets/chevron-down.png "Abajo") y active la casilla de verificación situada junto a cada etiqueta que desee aplicar.

* Para buscar etiquetas existentes, empiece a introducir una cadena de texto dentro del nombre de la etiqueta.

* Para crear una etiqueta nueva para aplicar, abra la lista, haga clic en **+ Agregar etiqueta**, escriba un nombre de etiqueta nuevo en el campo [!UICONTROL Label] y, a continuación, haga clic en **Crear**.

* Para quitar una etiqueta, anule la selección de la casilla de verificación situada junto al nombre de la etiqueta.

**URL de seguimiento de impresión:** (opcional) una dirección URL de seguimiento de impresiones de terceros que se anexará a la dirección URL de la página de aterrizaje para cualquier anuncio creado a partir de la experiencia. Se pueden incluir hasta cinco direcciones URL. Para agregar una dirección URL adicional, haz clic en ![icono](/help/creative/assets/create.png) **[!UICONTROL Add More] e ingresa la dirección URL.

Una vez que ingrese una dirección URL, todas las [macros disponibles](/help/creative/creative-macros.md) y los datos con los que se sustituyen se mostrarán más adelante en la página. Para insertar una de las macros en la dirección URL, mantenga el cursor sobre la descripción de la macro y haga clic en ![Copiar al portapapeles](/help/creative/assets/copy-to-clipboard.png "Copiar al portapapeles") y, a continuación, pegue la macro donde desee en el campo URL.

>[!NOTE]
>
>* [!DNL Creative] prefija automáticamente sus propias etiquetas de seguimiento de impresiones a la dirección URL de la página de aterrizaje.
>* Puedes [anular esta URL para cualquier creativo de la experiencia](experience-tracking-urls-targeting.md).
>* También puede introducir código de seguimiento de impresiones de JavaScript de terceros en el campo [!UICONTROL Client JS]

**URL de rastreo de clics:** (opcional) (opcional) Una URL de rastreo de clics de terceros que se anexará a la dirección URL de la página de aterrizaje. Se pueden incluir hasta cinco direcciones URL. Para agregar una dirección URL adicional, haz clic en ![icono](/help/creative/assets/create.png) **[!UICONTROL Add More] e ingresa la dirección URL.

Una vez que ingrese una dirección URL, todas las [macros disponibles](/help/creative/creative-macros.md) y los datos con los que se sustituyen se mostrarán más adelante en la página. Para insertar una de las macros en la dirección URL, mantenga el cursor sobre la descripción de la macro y haga clic en ![Copiar al portapapeles](/help/creative/assets/copy-to-clipboard.png "Copiar al portapapeles") y, a continuación, pegue la macro donde desee en el campo URL.

>[!NOTE]
>
>* [!DNL Creative] prefija automáticamente sus propias etiquetas de seguimiento de impresiones a la dirección URL de la página de aterrizaje.
>* Puedes [anular esta URL para cualquier creativo de la experiencia](experience-tracking-urls-targeting.md).

**JS de cliente:** (opcional) Cualquiera de los siguientes:

* (Cuando el anunciante utiliza un proveedor de cumplimiento de OBA para los anuncios) Código JavaScript que señala a la superposición de anuncio que permite a los usuarios excluirse de la segmentación por comportamiento en línea (OBA).

* Cualquier código de seguimiento de impresiones de JavaScript de terceros que se adjunte a la página de aterrizaje. **Nota:** También puede escribir una dirección URL de seguimiento de impresiones de terceros en el campo [!UICONTROL Impression Tracking URL].

>[!MORELIKETHIS]
>
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Editar una experiencia con segmentación en árbol de decisiones](experience-edit-targeting.md)
>* [Macros disponibles para URL de seguimiento](/help/creative/creative-macros.md)
