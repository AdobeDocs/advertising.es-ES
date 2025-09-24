---
title: Configuración creativa estándar
description: Consulte la configuración de los elementos creativos estándar.
feature: Creative Standard Creatives
exl-id: 8eb66310-4860-4ca0-9678-a9e33639c529
source-git-commit: ce716c8dca8410a121858944f0c044423d9dff78
workflow-type: tm+mt
source-wordcount: '2105'
ht-degree: 0%

---

# Configuración creativa estándar

La configuración varía según el tipo creativo.

Cuando edita varios elementos creativos al mismo tiempo:

* Puede editar la configuración de cada creativo al mismo tiempo o de forma individual. De forma predeterminada, se seleccionan todos los elementos creativos que ha elegido y cualquier configuración que especifique se aplica a todos los elementos creativos seleccionados. Para editar la configuración de creativos específicos, anule la selección de cada creativo no aplicable antes de editar los campos; repita la selección para los creativos adicionales si es necesario.

* Algunos ajustes se aplican a todos los elementos creativos seleccionados.

## Configuración creativa flexible de HTML5 {#creative-settings-flexible-html5}

### Pestaña Detalles

**Nombre de Creative:** El nombre del creativo. El nombre de la plantilla o el nombre de archivo cargado se utiliza de forma predeterminada, pero puede cambiarlo. Para varios creativos, puede editar los nombres creativos individuales. **Sugerencia:** Incluya el tamaño del anuncio en el nombre del elemento creativo y use un nombre que pueda encontrar fácilmente cuando incluya el elemento creativo en una experiencia.

**Idioma:** El idioma predeterminado para cada anuncio con el que asocia a los creativos. Cuando se cargan o editan varios creativos, se aplica el mismo valor a cada creativo seleccionado.

**Tamaño de Creative:** (solo lectura para los creativos existentes) Dimensiones del creativo. Si alguna de las imágenes incluidas en el elemento creativo es más grande que el tamaño especificado, se cambia su tamaño en consecuencia.

**[!UICONTROL Click Tags]:** Las variables que permiten redirecciones de rastreo de clics desde los anuncios de banner incluidos. Los nombres de las variables y las direcciones URL de la página de aterrizaje correspondiente se rellenan desde la unidad creativa cargada, pero puede cambiar las direcciones URL predeterminadas. Para varios elementos creativos, puede editar las etiquetas de clic individuales.

<!-- I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**Etiqueta:** (Opcional) Cualquier etiqueta que se aplique a todos los elementos creativos seleccionados. Puede filtrar los elementos creativos por etiqueta en varias vistas dentro de [!DNL Creative] e incluir la dimensión [!UICONTROL Creative Label] en [!UICONTROL Custom Creative Report].

* Para seleccionar etiquetas existentes, haga clic en ![Abajo](/help/creative/assets/chevron-down.png "Abajo") y active la casilla de verificación situada junto a cada etiqueta que desee aplicar.

* Para buscar etiquetas existentes, empiece a introducir una cadena de texto dentro del nombre de la etiqueta.

* Para crear una nueva etiqueta que aplicar a los elementos creativos, abra la lista, haga clic en **+ Agregar etiqueta**, escriba un nuevo nombre de etiqueta en el campo [!UICONTROL Label] y, a continuación, haga clic en **Crear**.

* Para quitar una etiqueta, anule la selección de la casilla de verificación situada junto al nombre de la etiqueta.

### Pestaña Atributos

**\[Todos los atributos de contenido predeterminados aplicables al creativo\]:** Los nombres y valores de atributos predeterminados se rellenan desde la unidad creativa flexible, pero puede cambiar los valores de forma opcional.

>[!NOTE]
>
>También puede reemplazar el valor predeterminado de cualquiera de los atributos creativos con un valor personalizado cuando incluya el elemento creativo en una experiencia. Editar los atributos dentro de una experiencia crea una variación del elemento creativo principal.

Para obtener información acerca de los atributos disponibles en las plantillas predefinidas, consulte &quot;[Plantillas creativas flexibles disponibles](#flexible-creative-templates-available)&quot;.

### Pestaña Plantilla

*Solo creativos existentes*

El archivo de plantilla flexible de HTML5 para el creativo.

Si lo desea, puede reemplazar la plantilla existente por una nueva plantilla que tenga un diseño diferente pero el mismo conjunto de nombres de atributos que la plantilla original. La nueva plantilla debe estar en formato ZIP con un máximo de 2 MB. Cuando el creativo está en un paquete, todas las experiencias que utilizan el paquete utilizan posteriormente el diseño de la nueva plantilla.

Al actualizar la plantilla para un elemento creativo principal con variaciones secundarias, las variaciones se actualizan con cualquier cambio en el diseño de la plantilla, pero los valores de atributo de la variación no cambian.

Para reemplazar la plantilla de publicidad existente:

1. Haga clic en **Actualizar plantilla**.

1. Haga clic en **Continuar**.

1. Especifique un archivo ZIP de cualquiera de las siguientes maneras:

   * Arrastre y suelte un archivo en su dispositivo o red en el cuadro.

   * Haga clic en **[!UICONTROL select a file]** para localizar el archivo en su dispositivo o red.

   Consulte las [especificaciones de anuncios flexibles](#flexible-ad-spec).

1. Edite la nueva [configuración flexible de anuncios de HTML](#flexible-ad-settings) según sea necesario.

1. Haga clic **[!UICONTROL Edit]**

## Configuración creativa de HTML5 {#creative-settings-html5}

## Pestaña Detalles

Para los nuevos creativos, las siguientes configuraciones no están en una pestaña con nombre.

**Nombre de Creative:** El nombre del creativo. Para un nuevo elemento creativo, el nombre de archivo se utiliza de forma predeterminada, pero puede cambiarlo. Para varios creativos, puede editar los nombres creativos individuales. **Sugerencia:** Incluya el tamaño del anuncio en el nombre del elemento creativo y use un nombre que pueda encontrar fácilmente cuando incluya el elemento creativo en una experiencia.

**Idioma:** El idioma predeterminado para cada anuncio con el que asocia a los creativos. Cuando se cargan o editan varios creativos, se aplica el mismo valor a cada creativo seleccionado.

**Tamaño de Creative:** (solo lectura para los creativos existentes) Dimensiones del creativo. Si alguna de las imágenes incluidas en el elemento creativo es más grande que el tamaño especificado, se cambia su tamaño en consecuencia.

**[!UICONTROL Click Tags]:** (solo creativos estáticos de HTML5) Las variables que permiten redirecciones de rastreo de clics desde los anuncios de banner incluidos. Los nombres de las variables y las direcciones URL de la página de aterrizaje correspondiente se rellenan desde la unidad creativa cargada, pero puede cambiar las direcciones URL predeterminadas. Para varios elementos creativos, puede editar las etiquetas de clic individuales.

>[!NOTE]
>
>Al incluir el elemento creativo en una experiencia, puede reemplazar el valor predeterminado de cualquiera de las etiquetas de clic con una dirección URL de página de aterrizaje personalizada para generar una derivación del elemento creativo base.

**URL de página de aterrizaje:** (creativos simples de HTML5 con una sola página de aterrizaje) La URL de la página de aterrizaje predeterminada para cada anuncio con el que asocia los creativos. Debe ser una dirección URL válida que comience por http:// o https://. Puede incluir parámetros de seguimiento de terceros o [[!DNL Creative] macros](/help/creative/creative-macros.md) para su propio uso.

Cuando se incluye un elemento creativo en un paquete y se asigna el paquete a una experiencia, se puede, opcionalmente, cambiar la dirección URL de la página de aterrizaje, así como añadir direcciones URL de rastreo de clics y impresiones y JavaScript para cada elemento creativo del paquete. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Etiqueta:** (Opcional) Cualquier etiqueta que se aplique a todos los elementos creativos seleccionados. Puede filtrar los elementos creativos por etiqueta en varias vistas dentro de [!DNL Creative].

* Para seleccionar etiquetas existentes, haga clic en ![Abajo](/help/creative/assets/chevron-down.png "Abajo") y active la casilla de verificación situada junto a cada etiqueta que desee aplicar.

* Para buscar etiquetas existentes, empiece a introducir una cadena de texto dentro del nombre de la etiqueta.

* Para crear una nueva etiqueta que aplicar a los elementos creativos, abra la lista, haga clic en **+ Agregar etiqueta**, escriba un nuevo nombre de etiqueta en el campo [!UICONTROL Label] y, a continuación, haga clic en **Crear**.

* Para quitar una etiqueta, anule la selección de la casilla de verificación situada junto al nombre de la etiqueta.

### Pestaña Plantilla

*Solo creativos estáticos de HTML5 existentes*

El archivo de plantilla HTML5 para el creativo.

Si lo desea, puede reemplazar la plantilla existente por una nueva plantilla que tenga un diseño diferente pero el mismo conjunto de nombres de atributos que la plantilla original. La nueva plantilla debe estar en formato ZIP con un máximo de 2 MB. Cuando el creativo está en un paquete, todas las experiencias que utilizan el paquete utilizan posteriormente el diseño de la nueva plantilla.

Al actualizar la plantilla para un elemento creativo principal con variaciones secundarias, las variaciones se actualizan con cualquier cambio en el diseño de la plantilla, pero los valores de atributo de la variación no cambian.

Para reemplazar la plantilla de publicidad existente:

1. Haga clic en **Actualizar plantilla**.

1. Haga clic en **Continuar**.

1. Especifique un archivo ZIP de cualquiera de las siguientes maneras:

   * Arrastre y suelte un archivo en su dispositivo o red en el cuadro.

   * Haga clic en **[!UICONTROL select a file]** para localizar el archivo en su dispositivo o red.

   Consulte las [especificaciones del anuncio de HTML](html5-creative-specification.md).

1. Edite la nueva [configuración de anuncios de HTML5](#creative-settings-html5) según sea necesario.

1. Haga clic **[!UICONTROL Edit]**

## Configuración creativa de imagen {#creative-settings-image}

**Nombre de Creative:** El nombre del creativo. Para un nuevo elemento creativo, el nombre de archivo se utiliza de forma predeterminada, pero puede cambiarlo. Para varias imágenes, puede editar los nombres creativos individuales. **Sugerencia:** Use un nombre que pueda encontrar fácilmente cuando incluya al creativo en una experiencia.

**Idioma:** El idioma predeterminado para cada anuncio con el que asocia a los creativos. El mismo valor se aplica a todas las imágenes seleccionadas. Cuando se incluyen los creativos en una experiencia, se pueden personalizar las preferencias de idioma de la experiencia.

**Tamaño de Creative:** (solo lectura) Dimensiones de las imágenes cargadas.

**Dirección URL de la página de aterrizaje:** Dirección URL de la página de aterrizaje predeterminada para cada anuncio con el que asocia a los creativos. La dirección URL de la página de aterrizaje debe ser una dirección URL válida que comience por http:// o https://. Puede incluir parámetros de seguimiento de terceros o [[!DNL Creative] macros](/help/creative/creative-macros.md) para su propio uso. El mismo valor se aplica a todas las imágenes seleccionadas.

Cuando se incluye un elemento creativo en un paquete y, a continuación, se asigna el paquete a una experiencia, se puede, opcionalmente, cambiar la dirección URL de la página de aterrizaje, así como añadir direcciones URL de rastreo de clics y impresiones y JavaScript para cada elemento creativo del paquete. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Etiqueta:** (Opcional) Cualquier etiqueta que se aplique a todos los elementos creativos seleccionados. Puede filtrar los elementos creativos por etiqueta en varias vistas dentro de [!DNL Creative].

* Para seleccionar etiquetas existentes, haga clic en ![Abajo](/help/creative/assets/chevron-down.png "Abajo") y active la casilla de verificación situada junto a cada etiqueta que desee aplicar.

* Para buscar etiquetas existentes, empiece a introducir una cadena de texto dentro del nombre de la etiqueta.

* Para crear una nueva etiqueta que aplicar a los elementos creativos, abra la lista, haga clic en **+ Agregar etiqueta**, escriba un nuevo nombre de etiqueta en el campo [!UICONTROL Label] y, a continuación, haga clic en **Crear**.

* Para quitar una etiqueta, anule la selección de la casilla de verificación situada junto al nombre de la etiqueta.

## Configuración creativa de terceros {#creative-settings-third-party}

**JavaScriptCode:** Una etiqueta de JavaScript (y opcionalmente una etiqueta alternativa para los navegadores que no admiten JavaScript) que señala al elemento creativo en el servidor de publicidad de terceros. La secuencia de comandos puede variar según el servidor de publicidad. Cuando edita varios creativos, se aplica el mismo valor a cada creativo seleccionado.

Todas las [macros disponibles](/help/creative/creative-macros.md) y los datos con los que se han sustituido se muestran debajo del campo de entrada. Para insertar una de las macros en la etiqueta, mantenga el cursor sobre la descripción de la macro y haga clic en ![Copiar al portapapeles](/help/creative/assets/copy-to-clipboard.png "Copiar al portapapeles") y, a continuación, pegue la imagen donde desee dentro de la etiqueta.

Cuando se incluye este elemento creativo en una experiencia que se implementa como anuncio desde un DSP, el DSP utiliza la información de esta etiqueta para mostrar el anuncio y para rastrear impresiones y clics en él. A continuación, DSP inserta la etiqueta en el intercambio de anuncios. Cuando se muestra y se hace clic en el anuncio, el servidor de publicidad, DSP y [!DNL Creative] realizan un seguimiento de los eventos.

**[!UICONTROL Advertiser]:** (solo lectura) El anunciante para el que la biblioteca está disponible.

**Nombre de Creative:** El nombre del creativo. **Sugerencia:** Use un nombre que pueda encontrar fácilmente cuando incluya al creativo en una experiencia.

**Tamaño de Creative:** (solo lectura para anuncios existentes) Dimensiones del elemento creativo. Para nuevos creativos, seleccione de una lista de tamaños de anuncio estándar.

**Idioma:** El idioma predeterminado para cada anuncio con el que asocia a los creativos.

**Dirección URL de la página de aterrizaje:** Dirección URL de la página de aterrizaje utilizada para validar cada anuncio con el que asocia a los creativos. El servidor de publicidad de terceros determina la página de aterrizaje real de cada anuncio.

**Etiqueta:** (Opcional) Cualquier etiqueta que se aplique a todos los elementos creativos seleccionados. Puede filtrar los elementos creativos por etiqueta en varias vistas dentro de [!DNL Creative].

* Para seleccionar etiquetas existentes, haga clic en ![Abajo](/help/creative/assets/chevron-down.png "Abajo") y active la casilla de verificación situada junto a cada etiqueta que desee aplicar.

* Para buscar etiquetas existentes, empiece a introducir una cadena de texto dentro del nombre de la etiqueta.

* Para crear una nueva etiqueta que aplicar a los elementos creativos, abra la lista, haga clic en **+ Agregar etiqueta**, escriba un nuevo nombre de etiqueta en el campo [!UICONTROL Label] y, a continuación, haga clic en **Crear**.

* Para quitar una etiqueta, anule la selección de la casilla de verificación situada junto al nombre de la etiqueta.

## Configuración de creatividad de vídeo {#creative-settings-video}

**Nombre del recurso de Creative:** El nombre del creativo. Para un nuevo elemento creativo, el nombre de archivo se utiliza de forma predeterminada, pero puede cambiarlo. Para varias imágenes, puede editar los nombres creativos individuales. **Sugerencia:** Use un nombre que pueda encontrar fácilmente cuando incluya al creativo en una experiencia.

**Duración:** (solo lectura) La duración del vídeo, que se completa automáticamente.

**Idioma:** El idioma predeterminado para cada anuncio con el que asocia a los creativos. El mismo valor se aplica a todas las imágenes seleccionadas. Cuando se incluyen los creativos en una experiencia, se pueden personalizar las preferencias de idioma de la experiencia.

**Dirección URL de la página de aterrizaje:** Dirección URL de la página de aterrizaje predeterminada para cada anuncio con el que asocia a los creativos. La dirección URL de la página de aterrizaje debe ser una dirección URL válida que comience por http:// o https://. Puede incluir parámetros de seguimiento de terceros o [[!DNL Creative] macros](/help/creative/creative-macros.md) para su propio uso. El mismo valor se aplica a todas las imágenes seleccionadas.

Cuando se incluye un elemento creativo en un paquete y, a continuación, se asigna el paquete a una experiencia, se puede, opcionalmente, cambiar la dirección URL de la página de aterrizaje, así como añadir direcciones URL de rastreo de clics y impresiones y JavaScript para cada elemento creativo del paquete. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Etiqueta:** (Opcional) Cualquier etiqueta que se aplique a todos los elementos creativos seleccionados. Puede filtrar los elementos creativos por etiqueta en varias vistas dentro de [!DNL Creative].

* Para seleccionar etiquetas existentes, haga clic en ![Abajo](/help/creative/assets/chevron-down.png "Abajo") y active la casilla de verificación situada junto a cada etiqueta que desee aplicar.

* Para buscar etiquetas existentes, empiece a introducir una cadena de texto dentro del nombre de la etiqueta.

* Para crear una nueva etiqueta que aplicar a los elementos creativos, abra la lista, haga clic en **+ Agregar etiqueta**, escriba un nuevo nombre de etiqueta en el campo [!UICONTROL Label] y, a continuación, haga clic en **Crear**.

* Para quitar una etiqueta, anule la selección de la casilla de verificación situada junto al nombre de la etiqueta.

>[!MORELIKETHIS]
>
>* [Agregar elementos creativos estándar a una biblioteca creativa](/help/creative/creative-libraries/creative-add-standard.md)
>* [Editar elementos creativos estándar](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Macros disponibles para URL de seguimiento](/help/creative/creative-macros.md)
