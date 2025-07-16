---
title: Acerca de sus bibliotecas creativas
description: Obtenga información sobre cómo administrar los elementos creativos para sus experiencias publicitarias.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 85f89ef480ee938c7dbac0f3a1d5b9a5db0bef8f
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# Acerca de sus bibliotecas creativas

*Característica beta cerrada*

Las bibliotecas creativas le permiten administrar los elementos creativos que utilizará en las experiencias publicitarias. Puede crear varias bibliotecas, cada una con un conjunto de elementos creativos y *paquetes creativos*, que son grupos de elementos creativos que puede agregar a una experiencia como una sola unidad.

Las bibliotecas pueden incluir lo siguiente:

* **Creativos individuales:** Puede incluir creativos individuales directamente dentro de las experiencias publicitarias que no tengan objetivos de usuario definidos. También puede usar sus elementos creativos para crear paquetes, que puede incluir en [experiencias publicitarias](/help/creative/experiences/experience-about.md) de destino.

   * **Creativos estándar:** Puede cargar y administrar creativos en [varios formatos](#creative-creative-formats). Para cada elemento creativo, se especifica el idioma predeterminado para cada anuncio con el que se asocia el elemento creativo y la página de aterrizaje predeterminada que se abre cuando un usuario hace clic en un anuncio que incluye el elemento creativo. Si lo desea, puede especificar etiquetas para utilizarlas como filtros en varias vistas dentro de [!DNL Creative] y como valores de columna en [!UICONTROL Custom Creative Report] cuando incluya mediante la dimensión [!UICONTROL Creative Label].

   * **Creativos dinámicos:** (solo clientes existentes de Adobe Advertising DCO) Los usuarios administradores pueden crear creativos generados dinámicamente asignando variables dinámicas en una plantilla de anuncio a los valores de un archivo de fuente. Todos los usuarios pueden obtener una vista previa de los anuncios dinámicos existentes, duplicarlos y eliminarlos.

* **Paquetes creativos:** Agrupe los elementos creativos en paquetes para usarlos en varias experiencias con objetivos de usuario definidos. Puede crear *paquetes de pantalla estándar* que consten de anuncios en pantalla estándar, *paquetes de vídeo estándar* que consten de anuncios de vídeo estándar y *paquetes de pantalla dinámica* que consten de anuncios en pantalla generados dinámicamente.

## Formatos de Creative compatibles {#creative-creative-formats}

### Formatos para creativos estándar

Puede agregar y administrar los siguientes tipos creativos en los [tamaños creativos admitidos](creative-sizes.md).

>[!IMPORTANT]
>
>* Incluso si tiene intención de utilizar HTML5, Flexible HTML5 o creativos de terceros para sus experiencias publicitarias en pantalla estándar, también debe añadir creativos de imagen para cada tamaño creativo que utilice.
>* Cada experiencia de visualización estándar requiere un creativo de imagen predeterminado para cada tamaño creativo asignado a la experiencia. Los elementos creativos de imagen predeterminados se utilizan cuando un explorador no está habilitado para JavaScript o cuando el servidor de publicidad no puede personalizar el anuncio debido a retrasos.
>* Cada experiencia de vídeo estándar requiere un creativo de vídeo predeterminado para cada duración creativa asignada a la experiencia.<!-- when is it used? -->

#### HTML flexible5

Los creativos flexibles de HTML5 son creativos de HTML5 con todas sus imágenes y otros atributos como etiquetas estándar de HTML, que se pueden editar directamente en [!DNL Creative], ya sea en una biblioteca creativa o en una experiencia individual (lo que crea una variación del creativo original). En DSP, los elementos creativos flexibles de HTML5 son para un solo tamaño de anuncio específico (en píxeles). Si lo desea, puede cambiar los valores por defecto de los atributos especificados en un creativo flexible de HTML5. Posteriormente, puede especificar valores personalizados para los atributos dentro de una experiencia específica, lo que crea una variación del elemento creativo principal.

Puede cargar material creativo flexible de HTML5 como archivos ZIP o utilizar una de las plantillas disponibles en su cuenta como punto de partida. Vea las [especificaciones para creativos flexibles de HTML5](html5-creative-specification.md).

#### Creativos de HTML5

Puede cargar archivos creativos de HTML5 simples o estáticos, con todos los atributos e imágenes especificados, como archivos ZIP. No se puede editar ningún atributo ni añadir imágenes; en su lugar, cargue un nuevo archivo ZIP para añadir un nuevo elemento creativo. Vea las [especificaciones para creativos HTML5 simples y estáticos](html5-creative-specification.md).

#### Creativos de imagen

Puede incluir creativos de imagen en formato GIF, JPEG, JPG o PNG. Puede cargar imágenes aprobadas desde sus cuentas de Adobe Experience Manager o imágenes desde su dispositivo o red.

Cada experiencia de anuncio en pantalla estándar requiere un creativo de imagen predeterminado para cada tamaño creativo asignado a la experiencia.

#### Creativos de terceros

Introduzca las etiquetas de seguimiento de JavaScript para creativos alojados en servidores de publicidad de terceros. La secuencia de comandos varía según el servidor de publicidad; a continuación se muestra un ejemplo:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### Creativos de vídeo {#creative-video-specs}

Puede cargar vídeos creativos de origen para la web, el móvil o la TV conectada desde su dispositivo o red. Cada experiencia de anuncio de vídeo estándar requiere un creativo de vídeo predeterminado para cada duración creativa asignada a la experiencia. DSP transcodifica automáticamente todos los creativos de vídeo como etiquetas VAST 2.0 para que pueda previsualizarlos. En [!UICONTROL Tag Manager], opcionalmente, puede [aplicar transcodificación específica del editor](/help/creative/experiences/experience-tag-video-transcoding.md) a cualquier etiqueta de experiencia de anuncio de vídeo.

Consulte los siguientes requisitos creativos de vídeo.

**Tipo de archivo:** .mov, .mp4, .webm

**Tamaño de archivo:** máximo de 512 MB

**Proporción de aspecto del vídeo:** 16:9, 4:3

**Resolución de vídeo:** 640 x 360 para 360p, 1280 x 720 para 720p, 1920 x 1080 para 1080p

**Longitud del vídeo:** Máximo de 90 segundos

**Velocidad de bits:** 600-1200 kbps para 360p, 1500-2500 kbps para 720p, 3000-5000+ kbps para 1080p

**Velocidad de fotogramas de vídeo:** 23,98 FPS. Se pueden aceptar frecuencias de cuadro adicionales según los requisitos regionales o de editor

**Códec de vídeo:** H.264 (estándar del sector), AV1, H.265

**Formato de audio:** ACC (estándar del sector/MP4), Opus (WebM/AV1)

**Velocidad de bits de audio:** 16-512 kbps

**Velocidad de muestreo de audio:** 44100-48000 Hz

**Velocidad de audio:** 44,1kHz o 48 kHz

**Otro audio:** El archivo cargado debe ser no entrelazado, mezclado y contener una pista de audio. Puede que no haya sonido, pero se debe incluir una pista de audio en el archivo de vídeo.

### Formato para anuncios dinámicos

Los usuarios administradores pueden generar de forma dinámica elementos creativos en formato HTML5 estático y HTML5 dinámico asignando variables dinámicas en una plantilla de anuncio a valores de un archivo de fuente. Los elementos creativos dinámicos pueden incluir elementos creativos de las experiencias heredadas de Adobe Advertising Dynamic Creative Optimization (DCO).

## Las vistas [!UICONTROL Creative Libraries]

Consulte &quot;[Personalizar las vistas de datos](/help/creative/introduction/customize-data-views.md)&quot; para obtener más información sobre cómo personalizar cada vista.

### Vista principal de [!UICONTROL Creative Libraries]

La vista principal [!UICONTROL Creative Libraries] muestra todas las bibliotecas creativas. Los datos de cada biblioteca incluyen el número de experiencias a las que se asignan los paquetes de la biblioteca, el número de paquetes, el número de creativos, el número de tamaños creativos, el número de destinos de idioma predeterminados, la fecha de creación y la fecha de la última modificación de cualquier elemento de la biblioteca. El modo de tabla también incluye una columna para el anunciante.

Cuando esté en el modo de tarjeta, puede desplazarse por las imágenes de una biblioteca con varios elementos creativos mediante los botones &lt; y >.

#### Acciones disponibles

* [Crear una nueva biblioteca](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* Para cada biblioteca creativa:

   * [Edición del nombre de una biblioteca](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Abra una biblioteca para ver los creativos y los paquetes asignados a la biblioteca](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [Eliminar bibliotecas](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### Las vistas [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

La ficha [!UICONTROL Standard Ads] muestra todos los elementos creativos estándar que ha creado. Los datos de cada elemento creativo incluyen el tamaño, el tipo y la fecha de creación del elemento creativo. El modo de tabla también incluye columnas para el idioma predeterminado y la página de aterrizaje predeterminada.

##### Acciones disponibles

* [Añadir elementos creativos estándar a una biblioteca](creative-add-standard.md)

* [Edición de un elemento creativo estándar](creative-edit-standard.md)

* [Previsualización de un elemento creativo estándar](creative-preview.md)

* [Añada elementos creativos estándar a paquetes de visualización estándar y elimine elementos creativos estándar de un paquete de visualización estándar](creative-attach-detach-bundles.md)

* [Agregue elementos creativos de vídeo a paquetes de vídeo estándar y elimine elementos creativos de vídeo de un paquete de vídeo estándar](creative-attach-detach-bundles.md)

* [Duplicar creativos estándar](creative-duplicate.md)

* [Descargar creativos estándar](creative-download.md)

* [Eliminar elementos creativos estándar](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

La pestaña [!UICONTROL Dynamic Ads] muestra todos los elementos creativos dinámicos que se crearon dinámicamente para sus catálogos creativos, excepto los elementos creativos dinámicos que [eliminó manualmente](creative-delete.md) de la pestaña [!UICONTROL Dynamic Ads]. Si [duplicó manualmente](creative-duplicate.md) cualquier elemento creativo dinámico desde la última vez que se procesó un catálogo, entonces la lista de elementos creativos para ese catálogo también incluye los elementos creativos duplicados.

Los datos de cada creativo incluyen el tipo de creativo, el tamaño de creativo, el número de catálogos a los que pertenece el creativo y la fecha de creación. El modo de tabla también incluye columnas para la plantilla a través de la cual se generó el creativo y el recuento de ofertas.

>[!NOTE]
>
>Cada vez que se procesa un catálogo, se actualizan los datos de los elementos creativos dinámicos existentes para ese catálogo.

##### Acciones disponibles

Actualmente, la capacidad de crear y editar elementos creativos dinámicos solo está disponible para el equipo de cuenta de Adobe. Sin embargo, todos los usuarios pueden:

* [Previsualizar elementos creativos dinámicos](creative-preview.md)

* [Agregue elementos creativos dinámicos a los paquetes de visualización dinámica y elimine elementos creativos dinámicos de un paquete de visualización dinámica](creative-attach-detach-bundles.md)

* [Creativos dinámicos duplicados](creative-duplicate.md)

* [Eliminar elementos creativos dinámicos](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### La vista [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

La vista [!UICONTROL Bundles] muestra todos los contenedores de paquete estándar y dinámico. Puede ver los nombres creativos, los tamaños creativos y los idiomas de los creativos incluidos en cada paquete. Cuando esté en el modo de tarjeta, puede desplazarse por las imágenes en un paquete con varios elementos creativos mediante los botones &lt; y >.

#### Acciones disponibles

* Añadir paquetes de visualización estándar, vídeo estándar y visualización dinámica a una biblioteca

* Enumere y previsualice los creativos en un paquete

* Editar un nombre de paquete

* Añada elementos creativos de visualización estándar a paquetes de visualización estándar y elimine elementos creativos de visualización estándar de un paquete de visualización estándar

* Agregue creativos de vídeo estándar a paquetes de vídeo estándar y elimine creativos de vídeo estándar de un paquete de vídeo estándar

* Paquetes duplicados

* Eliminar paquetes

>[!MORELIKETHIS]
>
>* [Administrar bibliotecas creativas](/help/creative/creative-libraries/creative-library-manage.md)
>* [Agregar elementos creativos estándar a una biblioteca creativa](creative-add-standard.md)
>* [Administrar paquetes creativos](bundle-manage.md)
>* [Personalizar las vistas de datos](/help/creative/introduction/customize-data-views.md)
