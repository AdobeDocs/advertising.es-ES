---
title: Configuración creativa dinámica
description: Consulte la configuración de los elementos creativos dinámicos.
feature: Creative Dynamic Creatives
source-git-commit: 31651c4e30d22b4d1639ef3fc05d5ff9e02dd040
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Configuración creativa dinámica

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## Configuración de publicidad dinámica<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Detalles básicos

**[!UICONTROL Dynamic Ad Name]:** Un nombre único para el creativo.

**[!UICONTROL Advertiser]:** Anunciante para el que se van a crear los anuncios.

**[!UICONTROL Library]:** Biblioteca creativa en la que se crean los anuncios. Si está creando los anuncios dentro de [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], el nombre de la biblioteca ya estará seleccionado y será de solo lectura.

**[!UICONTROL Ad Template Size]:** [dimensiones de anuncio](/help/creative/creative-libraries/creative-sizes.md) para la plantilla de anuncio a partir de la cual se creará el anuncio. Si selecciona primero un(a) [!UICONTROL Ad Template] específico(a), entonces este valor se selecciona automáticamente.

## Plantilla de anuncio

**[!UICONTROL Ad Template]:** Plantilla de anuncio a partir de la cual se crearán los anuncios. Seleccione una plantilla de anuncio existente o cargue una nueva plantilla de anuncio y seleccione el tipo de plantilla (*Estática* o *Dinámica*). Una plantilla cargada debe estar en formato ZIP y contener archivos HTML5 y archivo de definición de plantilla (template.TDF). <!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]:** El número de productos que se mostrarán en un carrusel.

## Catálogos

**[!UICONTROL Template]:** Plantilla de fuente que se va a usar para crear los anuncios.

**\[Catálogos\]**: Uno o más catálogos a partir de los cuales generar anuncios. Seleccione un catálogo existente o cree un nuevo catálogo descargando una plantilla de fuente existente y creando y cargando el nuevo catálogo.

Los catálogos cargados deben tener el formato ZIP y contener lo siguiente:

* Uno o más archivos de fuente en formato CSV, TSV o hoja de cálculo de Excel de Microsoft (XLSX).<!-- Need to add more specs for that -->

* Recursos de imagen en formato GIF, JPEG, JPG o PNG

* (Opcional) Recursos de vídeo en formato MP4 o WEBM

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->Los tipos de columnas del archivo de fuente cuyos valores deben estar presentes para crear anuncios: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Nota:** Esta configuración funciona de forma independiente de la configuración avanzada de la configuración de la experiencia publicitaria.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Asigne cada atributo (campo de anuncio dinámico) de la plantilla de anuncio especificada a una columna del catálogo especificado (etiqueta de catálogo) o introduzca un valor estático.

>[!MORELIKETHIS]
>
>* [Agregar elementos creativos dinámicos a una biblioteca creativa](creative-add-dynamic.md)
>* [Editar elementos creativos dinámicos en una biblioteca creativa](creative-edit-dynamic.md)
>* [Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
