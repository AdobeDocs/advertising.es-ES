---
title: Administrar catálogos de fuentes
description: Obtenga información sobre cómo administrar los catálogos de fuentes.
feature: Creative Dynamic Creatives
exl-id: d3ee20ba-5359-4dbe-bc76-269dc800843c
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Administrar catálogos de fuentes

Los catálogos de fuentes procesados son conjuntos de variaciones de anuncios potenciales creados a partir de un archivo de fuente especificado y una plantilla de fuente especificada. Los anuncios dinámicos de HTML5 y vídeo, pero no los anuncios estáticos de HTML5, requieren un catálogo para crear anuncios dinámicos.

Antes de crear variaciones de anuncios y [agregar anuncios dinámicos a una biblioteca creativa](/help/creative/creative-libraries/creative-add-dynamic.md), procese el catálogo. Puede actualizar posteriormente el archivo de fuente y volver a procesar el catálogo para crear un nuevo conjunto de variaciones de anuncios.<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

Cada archivo de fuente puede procesar hasta 500 filas con recursos de vídeo.

>[!TIP]
>
>Para todas las cuentas con vídeos dinámicos, la práctica recomendada es [descargar la plantilla de fuente universal [!UICONTROL Adobe Creative Template]](feed-template-manage.md), asignar cada campo del archivo de recursos a un campo del servidor de Advertising Creative y, a continuación, cambiar el nombre de la plantilla de fuente y cargarla. Utilice la nueva plantilla de fuente, junto con el archivo de recursos, para crear un catálogo.

## Creación de un catálogo {#feed-catalog-create}

>[!NOTE]
>
>También puede cargar directamente un catálogo cuando [agregue elementos creativos dinámicos a una biblioteca creativa](/help/creative/creative-libraries/creative-add-dynamic.md). Cualquier catálogo que cree allí estará disponible en la vista [!UICONTROL Catalogs] para su uso futuro.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Catalog]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Especifique la [configuración del catálogo](#catalog-settings) según sea necesario.

1. Haga clic en **[!UICONTROL Next]**.

1. Revise las posibles variaciones de anuncios que se pueden crear para el catálogo.

1. Haga clic en **[!UICONTROL Save]**.

## Edición de un catálogo

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Catalog]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL Edit]**.

1. Edite la [configuración del catálogo](#catalog-settings) según sea necesario.

1. Revise las posibles variaciones de anuncios que se pueden crear para el catálogo.

1. Haga clic en **[!UICONTROL Save]**.

## Procesamiento de un catálogo {#feed-catalog-process}

Al procesar un catálogo, las variaciones de anuncios están disponibles para crear anuncios dinámicos de HTML5.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Catalog]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL Run Now]**.

## Pausar un catálogo activo

Pausar un catálogo para que quede inactivo.<!-- Can you Activate it again? -->

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL Pause]**.

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## Activación de un catálogo en pausa

<!-- Verify if this is available. -->

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL Activate]**.

## Archivar un catálogo

Archivar un catálogo para eliminarlo.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en **[!UICONTROL Archive]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Archive]**.

## Configuración de catálogo {#catalog-settings}

**[!UICONTROL Advertiser]:** El anunciante que puede usar el catálogo.

**[!UICONTROL Asset]:** El archivo de fuente que se va a usar como entrada para el catálogo.

**[!UICONTROL Catalog Name]:** Un nombre de catálogo único para el anunciante especificado. De forma predeterminada, se usa el nombre del archivo de fuente, incluida la extensión de archivo, que es la práctica recomendada para la identificación.<!-- must it have a file extension? -->

**[!UICONTROL Template]:** La plantilla de fuente que se utilizará para asignar campos en el archivo de recursos/fuentes especificado a campos en el servidor de Advertising Creative.

>[!MORELIKETHIS]
>
>* [Rastrear el estado de los trabajos de procesamiento del catálogo](/help/creative/feeds/job-status-track.md)
>* [Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Administrar archivos de recursos](/help/creative/feeds/asset-manage.md)
>* [Administrar plantillas de fuentes](/help/creative/feeds/feed-template-manage.md)
>* [Administrar plantillas de anuncios dinámicos](/help/creative/ad-templates/ad-template-manage.md)
>* [Agregar elementos creativos dinámicos a una biblioteca creativa](/help/creative/creative-libraries/creative-add-dynamic.md)
