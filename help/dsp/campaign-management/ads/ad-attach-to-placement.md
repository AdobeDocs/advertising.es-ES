---
title: Adjuntar anuncios a ubicaciones
description: Obtenga información sobre cómo adjuntar anuncios a ubicaciones.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Adjuntar anuncios a ubicaciones

Utilice el [!UICONTROL Ad Tools] vea para adjuntar anuncios a ubicaciones, adjuntar píxeles de seguimiento de terceros a los anuncios y desasociar los píxeles de seguimiento de terceros existentes de los anuncios.

>[!NOTE]
>
>Los anuncios de vídeo universales solo se pueden adjuntar a ubicaciones de vídeo universales.

## Abra el [!UICONTROL Ad Tools] Ver {#ad-tools-open}

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. Abra el [!UICONTROL Ad Tools] ver de cualquiera de las siguientes maneras:

   * (Desde el [!UICONTROL Packages] , [!UICONTROL Placements], o [!UICONTROL Ads] (vista) En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (Desde el [!UICONTROL Placements] (vista) Junto al nombre de la ubicación, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (Desde el [!UICONTROL Ads] (ver) Junto al nombre del anuncio, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   El [!UICONTROL Attach Ads] está seleccionada de forma predeterminada.

## Adjuntar anuncios a ubicaciones {#attach-ads-campaign}

1. [Abra el [!UICONTROL Ad Tools] vista](#ad-tools-open).

1. En el [!UICONTROL Edit] Para cada grupo de anuncios que desee adjuntar a las ubicaciones, haga lo siguiente:

   1. (Opcional) Localice ubicaciones y anuncios específicos de cualquiera de las siguientes maneras:

      * Sobre la tabla izquierda, haga clic en ![Filtrar](/help/dsp/assets/filter.png) y filtrar las listas por paquete, tipo de ubicación, estado de ubicación, tipo de anuncio o estado de anuncio.

      * Sobre las tablas derecha e izquierda, busque cadenas de texto específicas en los nombres de ubicación y publicidad.

   1. En la tabla de la izquierda, seleccione la casilla de verificación situada junto a cada ubicación a la que desee adjuntar los anuncios.

   1. En la tabla de la derecha, seleccione la casilla de verificación situada junto a cada anuncio que desee adjuntar a las ubicaciones seleccionadas.

      Solo se pueden seleccionar los anuncios aplicables al tipo de ubicación y que no estén adjuntos a las ubicaciones seleccionadas.

   1. En la parte inferior derecha, haga clic en **[!UICONTROL Attach]**.

1. (Opcional) Para volver a las vistas de detalles de la campaña, haga clic en ![Volver a la carpeta](/help/dsp/assets/breadcrumb-return.png "Volver a la carpeta") a la izquierda de [!UICONTROL Ad Tools] y seleccione el nombre de la campaña.

## Ver anuncios adjuntos a ubicaciones {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Abra el [!UICONTROL Ad Tools] vista](#ad-tools-open).

1. Cambie a la **[!UICONTROL View]** en la esquina superior derecha.

1. (Opcional) Localice ubicaciones y anuncios específicos según sea necesario:

   * Sobre la tabla izquierda, haga clic en ![Filtrar](/help/dsp/assets/filter.png) y filtrar las listas por paquete, tipo de ubicación, estado de ubicación, tipo de anuncio o estado de anuncio.

   * En las tablas derecha e izquierda, busque cadenas de texto específicas en la ubicación o en el nombre del anuncio.

1. Haga clic en cualquier fila de colocación de la tabla izquierda para ver los anuncios adjuntos en la tabla derecha.

1. (Opcional) Para adjuntar más anuncios a las ubicaciones de la campaña, cambie a la **[!UICONTROL Edit]** vista en la esquina superior derecha. Consulte el paso 2 del procedimiento anterior,&quot;[Adjuntar anuncios a ubicaciones](#attach-ads-campaign),&quot; para obtener instrucciones.

## Adjuntar píxeles de seguimiento de terceros a anuncios en una ubicación {#attach-pixels-ads}

1. [Abra el [!UICONTROL Ad Tools] vista](#ad-tools-open).

1. Haga clic en **[!UICONTROL Attach Pixels]** pestaña.

1. En el [!UICONTROL Edit] subvista:

   1. (Opcional) Localice los anuncios y los píxeles de terceros de cualquiera de las siguientes maneras:

      * Sobre la tabla izquierda, haga clic en ![Filtrar](/help/dsp/assets/filter.png) y filtrar las listas por estado de anuncio, tipo de anuncio, evento de integración de píxeles o tipo de píxel.

      * Sobre las tablas derecha e izquierda, busque cadenas de texto específicas en los nombres de anuncios y nombres de píxeles.

   1. (Si no existen píxeles de seguimiento de terceros para la campaña) Cree un píxel:

      1. En la tabla derecha, haga clic en **[!UICONTROL Create pixel]**.

      1. Especifique la configuración:

         **[!UICONTROL Integration Event]:** El evento que almacena en déclencheur el píxel que se va a activar, como *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** La URL de la imagen de píxel, en el formato adecuado para el Tipo de píxel especificado.

         **[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

         **[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, o *[!UICONTROL IAS]*.

      1. Clic **[!UICONTROL Save]**.

   1. En la tabla de la izquierda, active la casilla de verificación situada junto a cada anuncio para el que desee adjuntar píxeles de seguimiento de terceros.

   1. En la tabla de la derecha, seleccione la casilla de verificación situada junto a cada píxel de seguimiento de terceros que desee adjuntar a los anuncios seleccionados.

      Solo se pueden seleccionar los píxeles que aún no estén adjuntos a los anuncios seleccionados.

   1. En la parte inferior derecha, haga clic en **[!UICONTROL Attach]**.

1. (Opcional) Para volver a las vistas de detalles de la campaña, haga clic en ![Volver a la carpeta](/help/dsp/assets/breadcrumb-return.png "Volver a la carpeta") a la izquierda de [!UICONTROL Ad Tools] y seleccione el nombre de la campaña.

## Desasociar píxeles de seguimiento de terceros de anuncios en una ubicación {#detach-pixels-ads}

1. [Abra el [!UICONTROL Ad Tools] vista](#ad-tools-open).

1. Haga clic en **[!UICONTROL Attach Pixels]** pestaña.

1. En el [!UICONTROL Edit] subvista:

   1. (Opcional) Localice los anuncios y los píxeles de terceros de cualquiera de las siguientes maneras:

      * Sobre la tabla izquierda, haga clic en ![Filtrar](/help/dsp/assets/filter.png) y filtrar las listas por estado de anuncio, tipo de anuncio, evento de integración de píxeles o tipo de píxel.

      * Sobre las tablas derecha e izquierda, busque cadenas de texto específicas en los nombres de anuncios y nombres de píxeles.

   1. En la tabla de la izquierda, active la casilla de verificación situada junto a cada anuncio del que desee separar los píxeles de seguimiento de terceros.

   1. En la tabla de la derecha, seleccione la casilla de verificación situada junto a cada píxel de seguimiento de terceros que desee separar de los anuncios seleccionados.

      Solo se pueden seleccionar los píxeles adjuntos a todos los anuncios seleccionados.

   1. En la parte inferior derecha, haga clic en **[!UICONTROL Detach]**.

1. (Opcional) Para volver a las vistas de detalles de la campaña, haga clic en ![Volver a la carpeta](/help/dsp/assets/breadcrumb-return.png "Volver a la carpeta") a la izquierda de [!UICONTROL Ad Tools] y seleccione el nombre de la campaña.

## Ver píxeles adjuntos a anuncios {#view-pixels-ads}

1. [Abra el [!UICONTROL Ad Tools] vista](#ad-tools-open).

1. Haga clic en **[!UICONTROL Attach Pixels]** pestaña.

1. Cambie a la **[!UICONTROL View]** en la esquina superior derecha.

1. (Opcional) Localice los anuncios y los píxeles de terceros según sea necesario:

   * Sobre la tabla izquierda, haga clic en ![Filtrar](/help/dsp/assets/filter.png) y filtrar las listas por estado de anuncio, tipo de anuncio, evento de integración de píxeles o tipo de píxel.

   * Sobre las tablas derecha e izquierda, busque cadenas de texto específicas en los nombres de anuncios y nombres de píxeles.

1. Haga clic en cualquier fila de anuncio de la tabla izquierda para ver los píxeles adjuntos en la tabla derecha.

1. (Opcional) Para adjuntar más píxeles a los anuncios, cambie al **[!UICONTROL Edit]** vista en la esquina superior derecha. Consulte el paso 3 del procedimiento anterior,&quot;[Adjuntar píxeles de seguimiento de terceros a anuncios en una ubicación](#attach-pixels-ads),&quot; para obtener instrucciones.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Creación de varios anuncios de terceros](ad-create-multiple.md)
>* [Editar un anuncio](ad-edit.md)
>* [Enumeración de las ubicaciones asociadas a un anuncio](ad-list-placements.md)
>* [Editar los horarios de anuncios de las ubicaciones](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Preguntas frecuentes sobre Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
