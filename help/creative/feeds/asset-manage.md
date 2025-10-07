---
title: Administrar archivos de recursos
description: Obtenga información sobre cómo cargar y administrar archivos de recursos para un anunciante.
feature: Creative Dynamic Creatives
source-git-commit: af29637d42b9932933cd23a64d6a0e2b7084fa31
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Administrar archivos de recursos

Los anuncios dinámicos de HTML5 requieren un archivo de fuente en formato de hoja de cálculo de Excel de Microsoft (XLSX) y los recursos de imagen a los que se hace referencia en la hoja de cálculo. Los anuncios estáticos de HTML5 solo requieren un recurso de imagen por anuncio.


>[!NOTE]
>
> Cada archivo de fuente solo se puede utilizar para un catálogo.

## Requisitos de archivo

* Anuncios dinámicos de HTML5:

   * Archivo de fuente en formato CSV, TSV o hoja de cálculo de Excel de Microsoft (XLSX), con una fila de encabezado y una fila de datos para cada variación de anuncio. Incluya un nombre de imagen en cada fila con el formato `images/image_name` (como `images/300x250_acme_logo.png`).

     Los nombres de campo específicos del anunciante deben asignarse a los [campos disponibles para archivos de fuentes de anuncios dinámicos](/help/creative/appendix-available-feed-fields.md).

   * Los recursos de imagen asociados en formato GIF, JPEG, JPG o PNG.<!-- Is this true: The maximum file size is two (2) MB. --> Ver los [tamaños creativos compatibles](/help/creative/creative-libraries/creative-sizes.md).

  Puede cargar un solo archivo XLSX, un solo archivo de imagen o un solo archivo ZIP que contenga cualquier combinación de archivos XLSX e imagen.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Anuncios HTML5 estáticos:

   * Un recurso de imagen por anuncio en formato GIF, JPG, JPEG o PNG.

     Puede cargar una sola imagen o varias imágenes en un archivo ZIP.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Cargar un archivo de recursos

>[!NOTE]
>
>En lugar de cargar archivos de recursos, también puedes cargar directamente un catálogo cuando [agregues elementos creativos dinámicos a una biblioteca creativa](/help/creative/creative-libraries/creative-add-dynamic.md). Cualquier catálogo que cree allí estará disponible en la vista [!UICONTROL Catalogs] para su uso futuro.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Assets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]** > **[!UICONTROL Asset]**.

1. Configure el archivo de recursos:

   1. Seleccione el anunciante que puede acceder al archivo de recursos.

   1. Especifique el archivo de recursos de una de las siguientes maneras:

      * Arrastre y suelte un archivo en su dispositivo o red en el cuadro.

      * Haga clic en **[!UICONTROL Select a file]** para localizar el archivo en su dispositivo o red.

   1. Haga clic en **[!UICONTROL Upload]**.

Todos los archivos ZIP se descomprimen automáticamente. Al cargar un archivo de hoja de cálculo, el archivo se muestra en la subpestaña [!UICONTROL Feeds]. Al cargar un archivo de imagen, este aparece en la subpestaña [!UICONTROL Images].

## Descargar un archivo de recursos

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Assets]**.

1. Mantenga el cursor sobre la fila del recurso y haga clic en **[!UICONTROL Download]**.

   El archivo se descarga según el procedimiento normal del explorador.

## Eliminar un archivo de recursos

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Assets]**.

1. Mantenga el cursor sobre la fila del recurso y haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Campos disponibles para archivos de fuentes de publicidad dinámica](/help/creative/appendix-available-feed-fields.md)
>* [Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Administrar plantillas de fuentes](/help/creative/feeds/feed-template-manage.md)
>* [Administrar catálogos](/help/creative/feeds/catalog-manage.md)
>* [Administrar plantillas de anuncios dinámicos](/help/creative/ad-templates/ad-template-manage.md)
>* [Agregar elementos creativos dinámicos a una biblioteca creativa](/help/creative/creative-libraries/creative-add-dynamic.md)
