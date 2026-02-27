---
title: Configuración creativa dinámica
description: Consulte la configuración de los elementos creativos dinámicos.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 164ee92f85c0e649dc2bd6c0224a531eb72d1962
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Configuración creativa dinámica

<!-- add a description -->

## Configuración de publicidad dinámica<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Detalles básicos

**[!UICONTROL Creative Type]:** Si el creativo es un anuncio de *[!UICONTROL Display]* (HTML5) o un anuncio de *[!UICONTROL Video]*.

**[!UICONTROL Dynamic Display Ad Name]** o **[!UICONTROL Dynamic Video Ad Name]:** Un nombre único para el creativo.

**[!UICONTROL Advertiser]:** Anunciante para el que se van a crear los anuncios. Si va a crear los anuncios desde [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], el anunciante ya estará seleccionado y será de solo lectura.

**[!UICONTROL Library]:** Biblioteca creativa en la que se crean los anuncios. Si está creando los anuncios dentro de [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], el nombre de la biblioteca ya estará seleccionado y será de solo lectura.

## Plantilla de anuncio

**[!UICONTROL Ad Template]:** Plantilla de anuncio a partir de la cual se crearán los anuncios. Seleccione una plantilla de anuncio existente o cargue una nueva plantilla de anuncio y seleccione el tipo de plantilla (*Estática* o *Dinámica*). La plantilla debe tener el formato ZIP y contener:<!-- Need to add more specs for templates -->

* Mostrar elementos creativos: archivos HTML5 con el formato de anuncio deseado y (solo anuncios dinámicos HTML5) un archivo con los atributos de anuncio (.tdf)

* Creativos de vídeo: un archivo .scene con el formato de anuncio deseado. El archivo ZIP puede tener un máximo de 512 MB.

Para continuar, haga clic en **[!UICONTROL Select Ad Template]**.

**[!UICONTROL Size]:** (solo anuncios dinámicos en pantalla; solo lectura) Las [dimensiones de anuncio](/help/creative/creative-libraries/creative-sizes.md) para la plantilla de anuncio seleccionada, que se usa para crear los anuncios.

**[!UICONTROL Card Count (Max 50)]:** (solo anuncios de visualización) El número de productos que se mostrarán en un carrusel.

**[!UICONTROL Duration]:** (solo anuncios de vídeo; solo lectura) La duración del vídeo derivada de la plantilla de anuncio seleccionada. La duración de cada vídeo debe estar entre 1 y 90 segundos.

## Catálogos

**\[Catálogos\]**: Uno o más catálogos a partir de los cuales generar anuncios. Seleccione un catálogo existente o cree un nuevo catálogo descargando una plantilla de fuente existente y creando y cargando el nuevo catálogo. Haga clic en **[!UICONTROL Select Catalog]**.

Los catálogos cargados deben tener el formato ZIP y contener lo siguiente:

* (Anuncios dinámicos en pantalla y vídeo) Uno o más archivos de fuente en formato CSV, TSV o hoja de cálculo de Excel de Microsoft (XLSX). El tamaño máximo de archivo es 512 MB.<!-- Need to add more specs for the feed files -->

* (Mostrar anuncios) Recursos de imagen en formato GIF, JPEG, JPG o PNG

* (Anuncios de vídeo) Recursos de vídeo en formato MP4, MOV o WEBM. Las plantillas de publicidad admitidas incluyen tarjeta de inicio, tarjeta de finalización, superposición superior, superposición inferior o en forma de L. La duración de cada vídeo debe estar entre 1 y 90 segundos.

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->Los tipos de columnas del archivo de fuente cuyos valores deben estar presentes para crear anuncios: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Nota:** Esta configuración funciona de forma independiente de la configuración avanzada de la configuración de la experiencia publicitaria.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Asigne cada atributo (campo de anuncio dinámico) de la plantilla de anuncio especificada a una columna del catálogo especificado (etiqueta de catálogo) o introduzca un valor estático.

>[!MORELIKETHIS]
>
>* [Agregar elementos creativos dinámicos a una biblioteca creativa](creative-add-dynamic.md)
>* [Editar elementos creativos dinámicos en una biblioteca creativa](creative-edit-dynamic.md)
>* [Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
