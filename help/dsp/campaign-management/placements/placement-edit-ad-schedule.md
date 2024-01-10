---
title: Editar horarios de anuncios para ubicaciones
description: Aprenda a cambiar los programas de anuncios de los anuncios adjuntos a las ubicaciones.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: bc45e96cf091cba3872b20f6ea691e369b29982f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Editar horarios de anuncios para ubicaciones

## Editar los horarios de anuncios de una o más ubicaciones

Puede cambiar las fechas de vuelo programadas y la rotación de la publicidad de los anuncios adjuntos a varias ubicaciones mediante una [!DNL Microsoft Excel] hoja de cálculo. Cada anuncio puede estar activo durante varios vuelos.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Seleccione la casilla de verificación situada junto a cada ubicación cuyos datos de publicidad desee descargar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Cuando el archivo esté disponible, haga clic en **[!UICONTROL Download]** en la notificación situada en la parte superior de la página del explorador para descargar un archivo de hoja de cálculo (en formato XLSX) según el procedimiento normal del explorador.

   ![Descargar notificación lista](/help/dsp/assets/download-ready.png "Descargar notificación lista")

1. Abra el archivo descargado, edite los campos de información de vuelo de cada fila de anuncio que desee incluir en el vuelo y guarde el archivo actualizado:

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (como [!UICONTROL Flight 1 Start Date] y [!UICONTROL Flight 1 End Date]): Las primeras y últimas fechas del vuelo. Utilice el formato AAAA-MM-DD para cada fecha. Todos los anuncios con campos de fecha de vuelo vacíos se tratan como anuncios no participantes.

   * **[!UICONTROL Flight N Weight]** (como [!UICONTROL Flight 1 Weight]): Cómo girar los anuncios de un vuelo. Introduzca un valor:

      * Para rotar los anuncios de un vuelo uniformemente, escriba `[!UICONTROL Even]`.

      * Para rotar los anuncios de un vuelo de forma desigual, introduzca el peso relativo por el que desea rotar cada anuncio como porcentaje (por ejemplo, `40` para el 40 %). El peso total del vuelo debe ser igual a 100.

1. Cargue la plantilla de programación de anuncios editada:

   1. Seleccione la casilla situada junto a cada posición aplicable.

   1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]** y especifique el archivo que desea cargar.

## Editar la programación de anuncios de una sola ubicación

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

Puede cambiar las fechas de vuelo programadas y la rotación de la publicidad para los anuncios adjuntos a una ubicación. Cada anuncio puede estar activo durante varios vuelos.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Junto al nombre de la ubicación, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

   1. Realice una de las siguientes acciones:

      * Para añadir un vuelo, haga clic en **[!UICONTROL Add Flight]** y, a continuación, especifique la fecha de inicio y la fecha final.

      * Para añadir un vuelo existente a un anuncio, haga clic en **[!UICONTROL +]** en la fila ad de la columna flight.

      * Para eliminar un vuelo existente de un anuncio, haga clic en **[!UICONTROL x]** en la fila ad de la columna flight.

      * (Cuando varios anuncios tienen el mismo vuelo) Para rotar los anuncios de forma desigual, haga clic en **[!UICONTROL Even Rotation]** en la información de vuelo y, a continuación, introduzca el peso relativo por el que girar cada anuncio, como porcentaje.

        El peso total debe ser igual a 100.

   1. En la esquina superior derecha, haga clic en **[!UICONTROL Continue]**.

   1. Revise los detalles del vuelo y haga clic en **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de ubicación](placement-about.md)
>* [Editar una ubicación](placement-edit.md)
>* [Ver el registro de cambios de una ubicación](placement-change-log.md)
>* [Configuración de ubicación](placement-settings.md)
