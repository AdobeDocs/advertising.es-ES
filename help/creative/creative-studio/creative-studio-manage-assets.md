---
title: Administración de recursos en Creative Studio
description: Obtenga información sobre cómo cargar, examinar y administrar recursos en la pestaña Assets de Creative Studio en Adobe Advertising Creative.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d4a041529615006a79093dccb8690f3b9f5e8cba
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# Administrar recursos en [!UICONTROL Creative Studio]

*característica de Beta*

Cargue imágenes, vídeo, audio y recursos de fuentes para hacer referencia a en las plantillas de publicidad y adjuntarlos a los mensajes de chat del agente de IA durante las sesiones de generación de anuncios.

## La vista [!UICONTROL Creative Studio] > [!UICONTROL Assets]

La pestaña **[!UICONTROL Assets]** enumera los recursos existentes en una vista de tarjeta.

### Acciones disponibles

<!--  * [Browse and search assets](#assets-search) -->

* [Cargar recursos](#assets-upload)

* [Cambiar el nombre de un recurso](#assets-rename)

* [Descargar un recurso](#assets-download)

* [Eliminar un recurso](#assets-delete)

<!--
Should be in "Common Tasks" chapter

## Browse and search assets {#assets-search}

* Use the **[!UICONTROL Search assets]** field to find assets by name. Enter at least three characters to trigger a search; shorter queries don't filter results.
* Click **[!UICONTROL Filter]** to filter the asset library by type or other attributes.
-->

## Tipos de recursos admitidos

| Tipo | Formatos compatibles | Tamaño máximo de archivo |
| --- | --- | --- |
| Imágenes | JPG/JPEG, PNG, GIF, WebP, SVG | 10 MB |
| Vídeo | MP4, MOV, AVI, WebM | 512 MB |
| Audio | MP3, WAV, AAC, OGG | 50 MB |
| Fuentes | TTF, OTF, WOFF, WOFF2 | 5 MB |

## Cargar recursos {#assets-upload}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Assets]**.

1. Haga clic en **[!UICONTROL Upload Assets]**.

1. Seleccione uno o varios archivos del equipo o de la red.

   Los archivos vacíos y los tipos de archivo no compatibles se rechazan con una notificación de error.

   El nombre del recurso se guarda como el nombre de archivo cargado sin su extensión. Los espacios y los caracteres que no sean ASCII del nombre de archivo se reemplazarán por guiones bajos (por ejemplo, al cargar `My Logo.png` se creará un recurso con el nombre `My_Logo`). Puede cambiar el nombre del recurso posteriormente.

## Editar un nombre de recurso {#asset-rename}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Assets]**.

1. Mantenga el cursor sobre la tarjeta de recursos y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit name]**.

1. Actualice el nombre del recurso.

   Los nombres de los recursos pueden tener hasta 512 caracteres.

1. Haga clic en **[!UICONTROL Update]**.

## Descargar un recurso {#asset-download}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Assets]**.

1. Mantenga el cursor sobre la tarjeta de recursos y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   El recurso se descarga según el procedimiento normal del explorador.

## Eliminar un recurso {#asset-delete}

>[!NOTE]
>
>No puede reactivar un recurso eliminado.

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio].**

1. Haga clic en la ficha **[!UICONTROL Assets]**.

1. Mantenga el cursor sobre la tarjeta de recursos y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de Creative Studio en Advertising Creative](creative-studio-about.md)
>* [Administrar plantillas en Creative Studio](creative-studio-manage-templates.md)
>* [Generar anuncios estándar en Creative Studio](creative-studio-manage-standard-ads.md)
