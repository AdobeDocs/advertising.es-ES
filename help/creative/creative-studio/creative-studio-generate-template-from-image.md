---
title: Generación de una plantilla de anuncio a partir de una imagen mediante IA
description: Aprenda a utilizar IA en Creative Studio para convertir una imagen de anuncio en pantalla estática existente en una plantilla de anuncio editable.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: adc2fdc93f06b5459c19b08306d1e30ce00e7028
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---
# Generación de una plantilla de anuncio a partir de una imagen mediante IA

*característica de Beta*

Use IA en [!UICONTROL Creative Studio] para convertir una imagen de anuncio en pantalla estática existente en una plantilla de anuncio en pantalla editable. Revise la plantilla generada, solicite cambios con lenguaje natural y abra el editor de plantillas para realizar cambios manuales y guardar la plantilla.

## Antes de empezar

Necesita un anuncio de imagen estática existente en una biblioteca de Creative. Este flujo de trabajo selecciona anuncios de las bibliotecas; no carga una imagen nueva directamente en el cuadro de diálogo de generación.

## Generación y revisión de la plantilla {#template-generate}

1. En el menú principal, haga clic en **[!UICONTROL Creative Studio]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. (Opcional) Seleccione un anunciante de la lista de anunciantes en la parte superior de la página para ver las bibliotecas de ese anunciante.

1. En el cuadro **[!UICONTROL Use AI to Generate a New Display Ad Template]**, haga clic en **[!UICONTROL Generate]**.

1. En el cuadro de diálogo **[!UICONTROL Generate New Ad Template]**, seleccione **[!UICONTROL Generate from Existing Standard Ad Image]** si aún no está seleccionado.

1. Seleccione la biblioteca que contiene el anuncio de imagen de la lista **[!UICONTROL Ad Library]**.

1. Mantenga el cursor sobre la imagen y la tarjeta y haga clic en **[!UICONTROL Use this Standard Ad]**.

   La generación comienza automáticamente, utilizando la anchura y altura del anuncio seleccionado.

1. Espere a que finalice la generación y, a continuación, revise la vista previa de la plantilla y el panel **[!UICONTROL Layers]**, cuando esté disponible.

   Compruebe el texto, las imágenes y el diseño antes de utilizar la plantilla. Las capas que se muestran aquí son para revisión; realice cambios manuales en el editor de plantillas.

1. (Opcional) Solicite cambios en la plantilla generada:

   1. En el campo **[!UICONTROL Ask the AI for any changes]**, describa los cambios que desee. Por ejemplo, escriba `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Haga clic en **[!UICONTROL Regenerate]**.

   1. Revise la vista previa actualizada. Repita el proceso según sea necesario.

1. Cuando esté listo para continuar, haga clic en **[!UICONTROL Use this Ad Template]**.

   La plantilla generada se abre en el editor de plantillas de visualización.

## Edite y guarde la plantilla {#template-save}

1. En el editor de plantillas, revise los elementos generados y realice los cambios restantes con los [controles del editor de plantillas](creative-studio-manage-templates.md#template-controls).

1. Haga clic en **[!UICONTROL Save]**.

1. En el cuadro de diálogo **[!UICONTROL Update Template]**, escriba o actualice **[!UICONTROL Template name]**, seleccione **[!UICONTROL Advertiser]** y, opcionalmente, agregue etiquetas.

1. Haga clic en **[!UICONTROL Update]** para guardar la plantilla y volver a la vista **[!UICONTROL Templates]**.

   Para guardar una copia independiente, haga clic en **[!UICONTROL Save As New]**.

Luego puede usar la plantilla para [generar variaciones de anuncios](creative-studio-manage-templates.md#ad-variations-generate).

## Si no puede generar una plantilla {#troubleshooting}

* **No se muestran bibliotecas ni anuncios de imágenes:** Compruebe el anunciante seleccionado y **[!UICONTROL Ad Library]**. Si la biblioteca no tiene imágenes de anuncio estándar, seleccione otra biblioteca que contenga un anuncio de imagen estática existente.

* **La generación falla o no se puede convertir la imagen:** Revise el mensaje mostrado, haga clic en **[!UICONTROL Back to library]** y seleccione un anuncio de imagen para intentarlo de nuevo.

>[!MORELIKETHIS]
>
>* [Administrar plantillas de anuncios en Creative Studio](creative-studio-manage-templates.md)
>* [Administrar anuncios estándar en Creative Studio](creative-studio-manage-standard-ads.md)