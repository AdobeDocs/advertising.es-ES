---
title: Ver el informe de ubicación [!UICONTROL Diagnostics]
description: Aprenda a diagnosticar problemas con la configuración y el ritmo de la ubicación.
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: db8e4bd75063216c27a7e14c8d7699e2f4e09ba4
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Ver el informe de ubicación [!UICONTROL Diagnostics]

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Los informes de diagnóstico pueden ayudarle a diagnosticar problemas con la configuración de ubicación y el ritmo una vez que una campaña está activa.

## Información en el informe de ubicación [!UICONTROL Diagnostics]

* **[!UICONTROL Change Log]:** Muestra cambios en la configuración de ubicación de claves, como el nombre, el estado y la oferta máxima. Cada entrada incluye la fecha y el nombre de usuario de la persona que realizó el cambio.

* **[!UICONTROL Ad Approvals]:** Muestra si los proveedores de inventario aprobaron o rechazaron los anuncios. Si lo desea, puede cambiar el estado de cualquier anuncio (por ejemplo, pausar un anuncio rechazado) o abrir la configuración del anuncio.

* **[!UICONTROL Non Bids]:** Muestra por qué DSP no pujó en la ubicación.

## Abrir el informe de ubicación [!UICONTROL Diagnostics]

1. Abrir el informe [!UICONTROL Diagnostics]:

   1. Abra la configuración de ubicación:

      1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

      1. Haga clic en el nombre de la campaña y luego haga clic en **[!UICONTROL Placements]**.

      1. Junto al nombre de la ubicación, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   1. En la esquina superior derecha, haga clic en ![Diagnóstico de ubicación](/help/dsp/assets/placement-diagnostics.png).

1. Realice una de las siguientes acciones:

   * Para ver el registro de cambios:

      1. Haga clic en **[!UICONTROL Change Log]**.

      1. (Opcional) Filtre los resultados del informe:

         * En el menú de fecha, cambie el período del informe de los Últimos 14 días predeterminados a otro período (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* o *[!UICONTROL Last 1 year]*).

         * En el menú de la izquierda, filtre el informe por un nombre de usuario específico.

         * En el menú de la derecha, filtre el informe por una configuración de ubicación específica.

   * Para ver el estado de las aprobaciones de anuncios:

      1. En la esquina superior derecha, haga clic en **[!UICONTROL Ad Approvals]**.

      1. (Opcional) Para pausar o activar el anuncio, haga clic en el modificador de estado (![Modificador de estado](/help/dsp/assets/status-switch.png)) en la columna Anuncio).

      1. (Opcional) Para abrir la configuración de un anuncio, haga clic en **[!UICONTROL View Ad]** junto al anuncio.

   * Para ver por qué DSP no pujó por la ubicación:

      1. En la esquina superior derecha, haga clic en **[!UICONTROL Non Bids]**.

      1. (Opcional) Para filtrar la colocación por un destino de acuerdo privado específico, seleccione la oferta. <!-- Admin users only: Optionally filter the deal by one or more regions ([!UICONTROL US-EAST], [!UICONTROL US-WEST]) [!UICONTROL EU-WEST], [!UICONTROL HKG]) by selecting the regions. -->

      1. (Opcional) Para cambiar el intervalo de fechas, haga clic en el campo de fecha y seleccione una fecha o un intervalo de fechas diferentes.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Tipos de informes de rendimiento en las vistas de administración de campañas](campaign-reports-about.md)
>* [Ver el informe de previsión de ubicación](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
