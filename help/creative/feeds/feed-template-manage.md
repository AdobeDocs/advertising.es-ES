---
title: Administrar plantillas de fuentes
description: Obtenga información sobre cómo administrar las plantillas de fuentes.
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Administrar plantillas de fuentes

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

Las plantillas de fuentes asignan campos en los archivos de fuentes con campos en el backend de Advertising Creative. Los anuncios dinámicos de HTML5, pero no los anuncios estáticos de HTML5, requieren una plantilla de fuente para crear anuncios dinámicos.

Puede utilizar una plantilla de fuente con varias plantillas de publicidad.

## Crear una plantilla de fuente

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Especifique la [configuración de la plantilla de fuente](#feed-template-settings).

1. Haga clic en **[!UICONTROL Save]**.

## Editar una plantilla de fuente

**Nota:** Solo puede editar las plantillas de fuentes que haya creado.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL Duplicate]**.

1. Edite la [configuración de la plantilla de fuente](#feed-template-settings) según sea necesario.

1. Haga clic en **[!UICONTROL Save]**.

## Ver una plantilla de fuente

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL View]**.

## Duplicación de una plantilla de fuente

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL Duplicate]**.

1. En la pantalla [!UICONTROL Duplicate Template], escriba un(a) **[!UICONTROL Template Name]** único(a). Si va a duplicar una plantilla creada por otra persona, seleccione **[!UICONTROL Advertiser]**. Si lo desea, puede editar otras [configuraciones de plantilla de fuente](#feed-template-settings) según sea necesario.

1. Haga clic en **[!UICONTROL Save]**.

## Descargar una plantilla de fuente

Las plantillas de fuentes descargadas están en formato comprimido de hoja de cálculo de Excel de Microsoft (XLSX).

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL Download]**.

   El archivo se descarga según el procedimiento normal del explorador.

## Configuración de plantilla de fuente {#feed-template-settings}

### Configuración de [!UICONTROL General]

**[!UICONTROL Template Name]:** Un nombre de plantilla único para el anunciante especificado.

**[!UICONTROL Advertiser]:** El anunciante que puede usar la plantilla.

**[!UICONTROL Description]:** (opcional) Información útil para cualquiera que use la plantilla de fuente.

### Configuración de [!UICONTROL Field Mapping]

Asigne cada campo del archivo de fuente a un campo del backend de Advertising Creative.<!-- Check w/product: What is displayed where in the UI/reports and published ads? --> Al menos un campo de archivo de fuente debe marcarse como &quot;[!UICONTROL Is Unique]&quot;. Para agregar una asignación de campo, haga clic en **[!UICONTROL +]**. Para quitar la última asignación de campo, haga clic en **[!UICONTROL +]**.

**[!UICONTROL Field Name]:** El campo en el archivo de fuente.

**[!UICONTROL Description]:** (opcional) Información útil para cualquiera que use la plantilla de fuente.

**[!UICONTROL Is Unique]:** Indica que el campo es un identificador único (clave). Al menos un campo por plantilla de fuente debe ser único. Para seleccionar esta opción, haga clic en el botón para moverla a la derecha.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** Campo del servidor de Advertising Creative que se asigna al [!UICONTROL Field Name] especificado en el archivo de fuente.

>[!MORELIKETHIS]
>
>* [Flujo de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Administrar archivos de recursos](/help/creative/feeds/asset-manage.md)
>* [Administrar catálogos](/help/creative/feeds/catalog-manage.md)
>* [Rastrear el estado de los trabajos de procesamiento del catálogo](/help/creative/feeds/job-status-track.md)
>* [Administrar plantillas de anuncios dinámicos](/help/creative/ad-templates/ad-template-manage.md)
>* [Agregar elementos creativos dinámicos a una biblioteca creativa](/help/creative/creative-libraries/creative-add-dynamic.md)
