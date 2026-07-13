---
title: Administración de perfiles de marca en Advertising Creative
description: Obtenga información sobre cómo crear, editar, duplicar y eliminar perfiles de marca en Adobe Advertising Creative.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1085
ht-degree: 0%

---

# Administrar perfiles de marca en [!DNL Advertising Creative]

*característica de Beta*

Un perfil de marca almacena la identidad visual y de mensajería de la marca, incluido el logotipo, la paleta de colores, las directrices de voz, los estándares de imagen y las directrices de copia específicas del canal, de modo que el agente de IA de [!DNL Creative] pueda generar contenido de publicidad que no sobrepase las directrices de marca.

Cuando crea anuncios en [!UICONTROL Creative Studio], el agente de IA utiliza la información del perfil de marca para generar contenido básico en la marca específica. Las recomendaciones de titulares, CTA, imágenes de fondo y colores reflejan el estilo y el tono de su marca sin que sea necesario volver a describirla en cada sesión de creación de anuncios.

## La vista [!UICONTROL Brands]

La vista [!UICONTROL Brands] enumera todos los perfiles de marca asociados con su cuenta de [!DNL Creative]. Cada tarjeta de perfil muestra el nombre de la marca, el logotipo y la fecha de la última modificación del perfil.

### Acciones disponibles

Las siguientes acciones están disponibles para algunos roles de usuario.

* [Crear un perfil de marca](#create-a-brand-profile)

* Para cada perfil de marca:

   * [Edición de un perfil de marca](#edit-a-brand-profile)

   * [Duplicación de un perfil de marca](#duplicate-a-brand-profile)

   * [Cambiar la imagen en miniatura de un perfil de marca](#change-thumbnail-brand-profile)

   * [Eliminar un perfil de marca](#delete-a-brand-profile)

## Crear un perfil de marca {#create-a-brand-profile}

*Sólo usuarios administradores*

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Brands]**.

1. Haga clic en **[!UICONTROL + Add brand]**.

1. Seleccione el anunciante correspondiente, escriba un(a) **[!UICONTROL Brand name]** único(a) y haga clic en **[!UICONTROL Add brand]**.

   Se abre la página de detalles de marca con la ficha **[!UICONTROL Overview]** activa.

1. (Opcional) Escriba la [configuración del perfil de marca](#brand-profile-settings) en cada ficha.

1. Haga clic en **[!UICONTROL Save]**.

## Edición de un perfil de marca {#edit-a-brand-profile}

*Sólo usuarios administradores*

1. En el menú principal, haga clic en **[!UICONTROL Brands]**.

1. Haga clic en el perfil de marca que desee editar.

1. Actualice la [configuración del perfil de marca](#brand-profile-settings) en cualquier pestaña.

1. Haga clic en **[!UICONTROL Save]**.

## Duplicación de un perfil de marca {#duplicate-a-brand-profile}

*Sólo usuarios administradores*

Al duplicar un perfil de marca, se crea un nuevo perfil con la misma configuración, que se puede editar según sea necesario.

1. En el menú principal, haga clic en **[!UICONTROL Brands]**.

1. En la tarjeta de marca, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Duplicate brand]**.

1. (Opcional) Edite la configuración del perfil y haga clic en **[!UICONTROL Save]**.

## Cambiar la imagen en miniatura de un perfil de marca {#change-thumbnail-brand-profile}

*Sólo usuarios administradores*

1. En el menú principal, haga clic en **[!UICONTROL Brands]**.

1. En la tarjeta de marca, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Change thumbnail]**.

1. Busque y especifique la imagen en miniatura en su dispositivo o red.

## Eliminar un perfil de marca {#delete-a-brand-profile}

*Sólo usuarios administradores*

>[!NOTE]
>
>La eliminación de un perfil de marca no afecta las [!UICONTROL Creative Studio] sesiones existentes que ya usaron el perfil.

Puede eliminar un perfil de marca de la lista de marcas o de la página de detalles de marca.

**De la lista de marcas:**

1. En el menú principal, haga clic en **[!UICONTROL Brands]**.

1. En la tarjeta de marca, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

**De la página de detalles de marca:**

1. En el menú principal, haga clic en **[!UICONTROL Brands]**.

1. Haga clic en el perfil de marca que desee eliminar.

1. Haga clic en **[!UICONTROL Brand actions]** y seleccione **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Configuración del perfil de marca {#brand-profile-settings}

La página de detalles de marca está organizada en las siguientes pestañas.

### [!UICONTROL Overview]

Muestra el nombre de la marca. Para agregar una descripción, haga clic en **[!UICONTROL When to use this brand]**, escriba el texto de la descripción y haga clic en **[!UICONTROL Save]**. La descripción se guarda inmediatamente y no es necesario hacer clic en el botón **[!UICONTROL Save]** de nivel de página.

### [!UICONTROL Brand voice guidelines]

(Opcional) Defina los estándares de voz y mensajería de la marca. El agente de IA utiliza estas directrices al generar titulares y copias.

* **[!UICONTROL Tone & Voice]:** (opcional) palabras o frases que describen el tono general. Ejemplos: &quot;profesional&quot;, &quot;autoritario&quot; o &quot;juguetón&quot;.

* **[!UICONTROL Brand Values]:** (Opcional) Valores principales que se reflejarán en los mensajes. Ejemplos: &quot;innovación&quot;, &quot;sostenibilidad&quot; o &quot;comunidad&quot;.

* **[!UICONTROL Editorial Guidelines]:** (Opcional) Escribir reglas a seguir. Ejemplos: &quot;usar siempre la voz activa&quot; o &quot;usar encabezados de mayúsculas y minúsculas&quot;.

* **[!UICONTROL Editorial Restrictions]:** (opcional) escribir reglas para evitar. Ejemplos: &quot;evite la jerga&quot;, &quot;no haga afirmaciones sobre los precios&quot; o &quot;no utilice nunca nombres de competidores&quot;.

### [!UICONTROL Image guidelines]

(Opcional) Defina estándares para las imágenes de fondo y de producto, organizadas en hasta 10 categorías. El agente de IA sigue estas directrices cuando genera solicitudes de imagen de fondo.

Ya se muestran los campos de la primera categoría. Para agregar una categoría, haga clic en **[!UICONTROL Add Category Name]** e introduzca la nueva configuración de categoría.

Para eliminar una categoría, haga clic en ![Eliminar](/help/creative/assets/delete.png "Eliminar") junto al nombre de la categoría. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

* **[!UICONTROL Category Name]:** La categoría de imagen. Ejemplos: &quot;Fotografía de producto&quot; o &quot;Estilo de vida&quot;.

* **[!UICONTROL Description]:** (opcional) Una descripción de la categoría.

* **[!UICONTROL Content Type]:** El tipo de imagen: *[!UICONTROL Art]* (para una generación de imágenes más ilustrativa) o *[!UICONTROL Photo]* (para una generación de imágenes más realista).

* **[!UICONTROL Composition]:** (opcional) Guía de composición. Incluye hasta cinco artículos. Ejemplos: &quot;asunto centrado&quot; o &quot;regla de tercios&quot;.

* **[!UICONTROL Environment]:** (opcional) Guía de configuración o entorno. Incluye hasta cinco artículos. Ejemplos: &quot;exterior&quot;, &quot;fondo de estudio&quot; o &quot;entorno urbano&quot;.

* **[!UICONTROL Color]:** (opcional) Guía de color para este tipo de imagen. Incluye hasta cinco artículos. Ejemplos: &quot;tonos silenciosos&quot; o &quot;evitar colores de neón&quot;.

* **[!UICONTROL Lighting]:** (Opcional) Guía de iluminación. Incluye hasta cinco artículos. Ejemplos: &quot;luz natural suave&quot; o &quot;evitar sombras duras&quot;.

* **[!UICONTROL Mood]:** (Opcional) Guía de estado de ánimo. Incluye hasta cinco artículos. Ejemplos: &quot;aspiracional&quot; o &quot;cálido y accesible&quot;.

* **[!UICONTROL Restrictions]:** (Opcional) Qué se debe evitar. Incluye hasta cinco artículos. Ejemplos: &quot;sin estética de foto de archivo&quot; o &quot;evite fondos ocupados&quot;.

### [!UICONTROL Channel guidelines]

Definir <!-- Just one set of guidelines as of 7/9: channel-specific --> hasta 10 estándares de copia. El agente de IA utiliza las directrices de canal al generar variaciones de copia.

<!-- Just one set of guidelines as of 7/9: The best practice is to add a guideline set for each advertising channel (for example, "Display," "Social Media," or "Connected TV"), and specify the following for each channel: -->

* **[!UICONTROL General]:** (Opcional) Reglas generales de copia<!-- Just one set of guidelines as of 7/9:  for the channel -->.

* **[!UICONTROL Headline]:** (Opcional) Guía para escribir titulares. Ejemplos: límites de caracteres o reglas de estilo.

* **[!UICONTROL Subheadline]:** (Opcional) Guía para escribir subtítulos.

* **[!UICONTROL Body]:** (opcional) guía para la copia de cuerpo.

* **[!UICONTROL CTA]:** (opcional) guía para el texto de call-to-action. Ejemplos: frases preferidas de CTA.

* **[!UICONTROL Examples]:** (opcional) copia de anuncio de muestra (titular, subtítulo, cuerpo y CTA) que ilustra el estilo especificado de <!-- Just one set of guidelines as of 7/9: channel's -->. Para ver ejemplos de la copia de anuncio basados en las directrices, haga clic en **[!UICONTROL Create example]**.

### [!UICONTROL Logos]

(Opcional) Los logotipos se utilizan en anuncios que incluyen un elemento de logotipo y están disponibles para el agente de IA al intercambiar versiones de logotipo. Los tipos de imagen admitidos son JPG, PNG y SVG, y cada archivo puede tener hasta 5 MB. Cada marca puede incluir un máximo de 10 logotipos.

Para cargar uno o varios archivos de logotipo de marca con la misma categoría y descripción:

1. Haga clic en **[!UICONTROL Add Logo].**

1. Para **[!UICONTROL Category]**, especifique si los logotipos son *[!UICONTROL Primary]* o *[!UICONTROL Secondary]*. El agente de IA utiliza considera la categoría para seleccionar un logotipo adecuado.

1. (Opcional) Escriba un **[!UICONTROL Description]** para los logotipos. La longitud máxima es de 500 caracteres.

1. Arrastre archivos al cuadro o haga clic en **[!UICONTROL Browse]** y seleccione los archivos del dispositivo o de la red.

1. Haga clic en **[!UICONTROL Add logos]**.

1. (Opcional) Realice cualquiera de las siguientes acciones para un solo archivo de logotipo:

   * Para ver los detalles del logotipo, haga clic en **[!UICONTROL ...]** > **[!UICONTROL View details]**.

   * Para editar la configuración del logotipo, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]**. Edite la configuración y haga clic en **[!UICONTROL Save]**.

   * Para descargar un archivo de logotipo según la configuración de descarga del explorador, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download]**.*

   * Para quitar un logotipo de la configuración de marca, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete]**. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

### [!UICONTROL Colors]

(Opcional) Defina las paletas de color de la marca. El agente de IA utiliza los colores especificados al generar variaciones de anuncios basadas en colores.

Para crear una paleta:

1. Haga clic en **[!UICONTROL Add palette]**.

1. Introduzca el nombre de la paleta.

1. Incluya al menos dos colores en la paleta antes de guardar la paleta. Para cada color:

   1. Haga clic en **[!UICONTROL Add color]** dentro de la paleta.

   1. Introduzca el nombre del color.

   1. Especifique la función del color (*[!UICONTROL Primary]*, *[!UICONTROL Secondary]* o *[!UICONTROL None]*.

   1. Utilice el cuentagotas o introduzca manualmente un valor hexadecimal (como #1473E6) o un valor RGB (como 20 115 230).

   1. Haga clic en **[!UICONTROL Add]**.

   1. (Opcional) Realice cualquiera de las siguientes acciones para un solo color:

      * Para editar la configuración de color, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]**. Edite la configuración y haga clic en **[!UICONTROL Save]**.

      * Para quitar un color de una paleta, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete]**. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de Creative Studio en Advertising Creative](/help/creative/creative-studio/creative-studio-about.md)
