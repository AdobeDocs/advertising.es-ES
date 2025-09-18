---
title: Adjuntar y eliminar píxeles de anuncios
description: Aprenda a adjuntar y eliminar píxeles de seguimiento de terceros de los anuncios.
feature: DSP Ads
source-git-commit: a3bd04da6c6f428fdb6e1f05187ea3de0174c9d7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Adjuntar y eliminar píxeles de anuncios

Puede adjuntar y desasociar píxeles de seguimiento de terceros de los anuncios.

## Abrir la vista [!UICONTROL Ad Tools] {#ad-tools-open}

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. Abra la vista [!UICONTROL Ad Tools] de cualquiera de las siguientes maneras:

   * (En la vista [!UICONTROL Campaigns]) Junto al nombre de la campaña, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Ad Tools].**

   * (Desde la vista [!UICONTROL Packages], [!UICONTROL Placements] o [!UICONTROL Ads]) En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

## Adjuntar píxeles de seguimiento de terceros a anuncios en una ubicación {#attach-pixels-ads}

1. [Abrir la vista [!UICONTROL Ad Tools]](#ad-tools-open).

   Se abre la ficha **[!UICONTROL Attach Pixels]**.

1. En la subvista [!UICONTROL Edit]:

   1. (Opcional) Localice los anuncios y los píxeles de terceros de cualquiera de las siguientes maneras:

      * Sobre la tabla de la izquierda, haz clic en ![Filtro](/help/dsp/assets/filter.png) y filtra las listas por estado de anuncio, tipo de anuncio, evento de integración de píxeles o tipo de píxel.

      * Sobre las tablas derecha e izquierda, busque cadenas de texto específicas en los nombres de anuncios y nombres de píxeles.

   1. (Si no existen píxeles de seguimiento de terceros para la campaña) Cree un píxel:

      1. En la tabla derecha, haga clic en **[!UICONTROL Create pixel]**.

      1. Especifique la configuración:

         **[!UICONTROL Integration Event]:** El evento que déclencheur el píxel que se va a activar, como *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Indica si el píxel es *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** Dirección URL de la imagen de píxel, en el formato adecuado para el tipo de píxel especificado.

         **[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

         **[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* o *[!UICONTROL IAS]*.

      1. Haga clic en **[!UICONTROL Save]**.

   1. En la tabla de la izquierda, active la casilla de verificación situada junto a cada anuncio para el que desee adjuntar píxeles de seguimiento de terceros.

   1. En la tabla de la derecha, seleccione la casilla de verificación situada junto a cada píxel de seguimiento de terceros que desee adjuntar a los anuncios seleccionados.

      Solo se pueden seleccionar los píxeles que aún no estén adjuntos a los anuncios seleccionados.

   1. En la parte inferior derecha, haga clic en **[!UICONTROL Attach]**.

1. (Opcional) Para volver a las vistas de detalles de la campaña, haga clic en ![Volver a la carpeta](/help/dsp/assets/breadcrumb-return.png "Volver a la carpeta") a la izquierda de [!UICONTROL Ad Tools] y seleccione el nombre de la campaña.

## Desasociar píxeles de seguimiento de terceros de anuncios en una ubicación {#detach-pixels-ads}

1. [Abrir la vista [!UICONTROL Ad Tools]](#ad-tools-open).

   Se abre la ficha **[!UICONTROL Attach Pixels]**.

1. En la subvista [!UICONTROL Edit]:

   1. (Opcional) Localice los anuncios y los píxeles de terceros de cualquiera de las siguientes maneras:

      * Sobre la tabla de la izquierda, haz clic en ![Filtro](/help/dsp/assets/filter.png) y filtra las listas por estado de anuncio, tipo de anuncio, evento de integración de píxeles o tipo de píxel.

      * Sobre las tablas derecha e izquierda, busque cadenas de texto específicas en los nombres de anuncios y nombres de píxeles.

   1. En la tabla de la izquierda, active la casilla de verificación situada junto a cada anuncio del que desee separar los píxeles de seguimiento de terceros.

   1. En la tabla de la derecha, seleccione la casilla de verificación situada junto a cada píxel de seguimiento de terceros que desee separar de los anuncios seleccionados.

      Solo se pueden seleccionar los píxeles adjuntos a todos los anuncios seleccionados.

   1. En la parte inferior derecha, haga clic en **[!UICONTROL Detach]**.

1. (Opcional) Para volver a las vistas de detalles de la campaña, haga clic en ![Volver a la carpeta](/help/dsp/assets/breadcrumb-return.png "Volver a la carpeta") a la izquierda de [!UICONTROL Ad Tools] y seleccione el nombre de la campaña.

## Ver píxeles adjuntos a anuncios {#view-pixels-ads}

1. [Abrir la vista [!UICONTROL Ad Tools]](#ad-tools-open).

   Se abre la ficha **[!UICONTROL Attach Pixels]**.

1. Cambie a la opción **[!UICONTROL View]** en la esquina superior derecha.

1. (Opcional) Localice los anuncios y los píxeles de terceros según sea necesario:

   * Sobre la tabla de la izquierda, haz clic en ![Filtro](/help/dsp/assets/filter.png) y filtra las listas por estado de anuncio, tipo de anuncio, evento de integración de píxeles o tipo de píxel.

   * Sobre las tablas derecha e izquierda, busque cadenas de texto específicas en los nombres de anuncios y nombres de píxeles.

1. Haga clic en cualquier fila de anuncio de la tabla izquierda para ver los píxeles adjuntos en la tabla derecha.

1. (Opcional) Para adjuntar más píxeles a los anuncios, cambie a la vista **[!UICONTROL Edit]** en la esquina superior derecha. Consulte el paso 3 del procedimiento anterior, &quot;[Adjuntar píxeles de seguimiento de terceros a anuncios en una ubicación](#attach-pixels-ads)&quot;, para obtener instrucciones.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Adjuntar anuncios a ubicaciones](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Crear varios anuncios de terceros](ad-create-multiple.md)
>* [Editar un anuncio](ad-edit.md)
>* [Enumerar las ubicaciones asociadas con un anuncio](ad-list-placements.md)
>* [Editar los horarios de anuncios para las ubicaciones](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Preguntas más frecuentes sobre el vídeo universal](/help/dsp/campaign-management/faq-universal-video.md)

