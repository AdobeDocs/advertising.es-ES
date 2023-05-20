---
title: Adjuntar un anuncio a una ubicación
description: Obtenga información sobre cómo adjuntar un anuncio a una ubicación.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 1f35711c5543974f97ce2a9c35427636c1e5a6a9
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 1%

---

# Adjuntar un anuncio a una ubicación

>[!NOTE]
>
>Los anuncios de vídeo universales solo se pueden adjuntar a ubicaciones de vídeo universales.

## Adjuntar un anuncio nuevo desde el [!UICONTROL Ads] Ver

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Ads]**.

1. Junto al nombre del anuncio, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

1. En la pantalla Colocar anuncio, realice una de las acciones siguientes:

   * Para crear una nueva ubicación para el anuncio:

      1. Haga clic **[!UICONTROL Create New Placement]**.

      1. Introduzca el [configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)y haga clic en **[!UICONTROL Create Placement]**.
   * Para agregar el anuncio a una o varias ubicaciones existentes:

      1. Haga clic **[!UICONTROL Select a Placement].**

      1. Realice una de las acciones siguientes:

         * Para agregar un anuncio a la vez:

            1. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**

            1. (Opcional) Para cada anuncio adicional que desee adjuntar, haga clic en **[!UICONTROL Attach to Other Placement]**. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**
         * Para adjuntar el anuncio hasta 20 ubicaciones a la vez:

            1. Seleccione la casilla de verificación situada junto a **Selección masiva&quot;.

            1. Seleccione la casilla de verificación situada junto a cada ubicación a la que desea adjuntar el anuncio.

            1. Haga clic **[!UICONTROL Attach]**.
      1. En la ficha Completar y revisar, seleccione una de las siguientes opciones:

         * Para volver a la vista Anuncios, haga clic en **[!UICONTROL I'm done for now]**.

         * Para adjuntar el anuncio a otra ubicación, haga clic en **[!UICONTROL Attach To Other Placement]**.




## Adjuntar un anuncio nuevo o existente desde el [!UICONTROL Placements] Ver

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Junto al nombre de la ubicación, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

1. En el [!UICONTROL Add Ad to Placement] , realice una de las acciones siguientes:

   * Para crear un anuncio nuevo:

      1. Haga clic **[!UICONTROL Create a New Ad]**.

      1. Introduzca la configuración de publicidad para [anuncios de audio](ad-settings-audio.md), [televisión conectada](ad-settings-connected-tv.md), [anuncios de display](ad-settings-display.md), [anuncios móviles](ad-settings-mobile.md), [anuncios nativos](ad-settings-native.md), o [anuncios previos a la emisión](ad-settings-pre-roll.md).

      1. Haga clic **[!UICONTROL Save & Submit for Review]**.

         El [revisión de anuncio](ad-about.md) para el nuevo anuncio tarda de 24 a 48 horas e incluye comprobaciones de categorías confidenciales, haga clic en funcionalidad de URL y previsualice procesamiento. El [!UICONTROL Status] DSP indica si el anuncio ha sido aprobado por el usuario. Los anuncios rotos pueden tener un estado pendiente durante más de 24 a 48 horas, por lo que tiene tiempo para corregir los errores antes de que se rechacen.

         >[!NOTE]
         >
         >DSP Su anuncio solo se publicará si tanto la SSP como el administrador de la plataforma de marketing han aprobado el creativo. Cada SSP tiene sus propios requisitos y procesos de aprobación.
   * Para seleccionar anuncios existentes:

      1. Haga clic **[!UICONTROL Select an Ad].**

      1. Especifique los anuncios:

         * Para agregar un anuncio a la vez:

            1. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**

            1. (Opcional) Para cada anuncio adicional que desee adjuntar, haga clic en **[!UICONTROL Add Another Ad]**. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**
         * Para agregar hasta 20 anuncios a la vez:

            1. Seleccione la casilla de verificación situada junto a **[!UICONTROL Bulk Select]**.&quot;

            1. Seleccione la casilla de verificación situada junto a cada anuncio que desee añadir.

            1. Haga clic **[!UICONTROL Attach]**.
      1. (Opcional) Para anular el período de vuelo y la rotación de publicidad predeterminados para anuncios específicos de la ubicación:

         1. Haga clic **[!UICONTROL Custom Schedule Ads]**.

         1. Realice una de las siguientes acciones:

            * Para añadir un vuelo, haga clic en **[!UICONTROL Add Flight]** y, a continuación, especifique la fecha de inicio y la fecha final.

            * Para añadir un vuelo existente a un anuncio, haga clic en **[!UICONTROL +]** en la fila ad de la columna flight.

            * Para eliminar un vuelo existente de un anuncio, haga clic en **[!UICONTROL x]** en la fila ad de la columna flight.

            * (Cuando varios anuncios tienen el mismo vuelo) Para rotar los anuncios de forma desigual, haga clic en **[!UICONTROL Even Rotation]** en la información de vuelo y, a continuación, introduzca el peso relativo por el que girar cada anuncio, como porcentaje.

               El peso total debe ser igual a 100.
         1. En la esquina superior derecha, haga clic en **[!UICONTROL Continue]**.

         1. Revise los detalles del vuelo y haga clic en **[!UICONTROL Save & Finish]**.
      1. Haga clic **[!UICONTROL I'm done for now]**.






>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Creación de varios anuncios de terceros](ad-create-multiple.md)
>* [Editar un anuncio](ad-edit.md)
>* [Enumeración de las ubicaciones asociadas a un anuncio](ad-list-placements.md)
>* [Editar la programación de anuncios de una ubicación](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Preguntas frecuentes sobre Universal Video](/help/dsp/campaign-management/faq-universal-video.md)

