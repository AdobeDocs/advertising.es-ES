---
title: Administración de plantillas de publicidad dinámicas
description: Más información sobre xxxx.
feature: Creative Templates
source-git-commit: 5828fada55ba9506589df6088ea58b896084700c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Administración de plantillas de publicidad dinámicas

Cree una plantilla de anuncio independiente para cada combinación de tipo de anuncio (HTML5 estático o HTML5 dinámico) y tamaño de anuncio cargando un archivo HTML5 comprimido con el formato de anuncio deseado. Para los anuncios dinámicos de HTML5, también se carga un archivo que contiene los atributos de anuncio <!-- more clarification? -->.

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Creación de una plantilla de publicidad dinámica

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create Ad Template]**

1. Especifique la [configuración de la plantilla de publicidad](#ad-template-settings)

1. Haga clic en **[!UICONTROL Create]**.

## Edición de una plantilla de publicidad dinámica

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla de publicidad y haga clic en **[!UICONTROL Edit]**.

1. Edite la [configuración de la plantilla de publicidad](#ad-template-settings).

1. Haga clic en **[!UICONTROL Save]**.

## Descargar una plantilla de publicidad dinámica

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla de publicidad y haga clic en **[!UICONTROL Download]**.

   El archivo se descarga según el procedimiento normal del explorador.

## Eliminación de una plantilla de publicidad dinámica

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla de publicidad y haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.<!-- Confirm -->

## Creación de anuncios dinámicos a partir de una plantilla de publicidad

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla de publicidad y haga clic en **[!UICONTROL Create Dynamic Ad]**.

   En la pantalla [!UICONTROL New Dynamic Ad], los campos [!UICONTROL Ad Template Size], [!UICONTROL Ad Template Type] y [!UICONTROL Ad Template] se seleccionan automáticamente y son de solo lectura.

1. Especifique la configuración del anuncio dinámico para [crear los anuncios dinámicos](/help/creative/creative-libraries/creative-add-dynamic.md).

## Configuración de plantilla de anuncio {#ad-template-settings}

### Detalles de plantilla de anuncio

**[!UICONTROL Advertiser]**: (solo lectura para plantillas existentes) El anunciante para el que se generarán los anuncios.

**[!UICONTROL Ad Template Name]**: un nombre de plantilla de anuncio único para el anunciante.

**[!UICONTROL Ad Template Type]**: (solo lectura para plantillas existentes) Formato de plantilla de anuncio: *HTML estático5* o *HTML dinámico5*.

**[!UICONTROL Ad Template Size]**: (solo lectura para plantillas existentes) Dimensiones de los anuncios creados por la plantilla.

**[!UICONTROL Description]**: (Opcional) información que resulta útil para cualquiera que utilice la plantilla de anuncio.

<!-- I don't see this on 9/24:

### (Static HTML5 ad templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.

-->

### HTML5 zip

Un archivo HTML5 comprimido con el formato de anuncio deseado. Si ya ha cargado un archivo, se muestra el nombre de archivo.

Consulte la [especificación creativa de HTML5](/help/creative/creative-libraries/html5-creative-specification.md).

Para cargar un archivo:

1. Haga clic en **[!UICONTROL Upload HTML5 zip]**.

1. Busque el archivo en su dispositivo o red.

### (Plantillas de anuncios HTML5 dinámicas) Archivo de atributos

<!-- EXPLAIN -->Archivo que contiene atributos para la plantilla de publicidad. Si ya ha cargado un archivo, se muestra el nombre de archivo.

<!-- Add specs for this file type -->

Para cargar un archivo:

1. Haga clic en **[!UICONTROL Upload Attributes File]**.

1. Busque el archivo en su dispositivo o red.

>[!MORELIKETHIS]
>
>* [Flujo de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Administrar archivos de recursos](/help/creative/feeds/asset-manage.md)
>* [Administrar plantillas de fuentes](/help/creative/feeds/feed-template-manage.md)
>* [Administrar catálogos](/help/creative/feeds/catalog-manage.md)
>* [Agregar elementos creativos dinámicos a una biblioteca creativa](/help/creative/creative-libraries/creative-add-dynamic.md)

