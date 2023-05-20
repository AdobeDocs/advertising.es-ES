---
title: Ver los informes de diagnóstico de ubicación
description: Aprenda a diagnosticar problemas con la configuración y el ritmo de la ubicación.
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Ver los informes de diagnóstico de ubicación

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Las siguientes herramientas pueden ayudarle a diagnosticar problemas con la configuración de ubicación y el ritmo una vez que una campaña está activa:

* **[!UICONTROL Change Log]:** Muestra los cambios realizados en la configuración de colocación de claves, como el nombre, el estado y la oferta máxima. Cada entrada incluye la fecha y el nombre de usuario de la persona que realizó el cambio.
* **[!UICONTROL Ad Approvals]:** Muestra si los proveedores de inventario aprobaron o rechazaron los anuncios. Si lo desea, puede cambiar el estado de cualquier anuncio (por ejemplo, pausar un anuncio rechazado) o abrir la configuración del anuncio.
* **[!UICONTROL Non Bids]:** DSP Muestra por qué no se ha pujado por la ubicación en la que se ha realizado la oferta.

1. Abra el informe Diagnóstico:
   1. Abra la configuración de ubicación:
      1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.
      1. Haga clic en el nombre de la campaña y luego haga clic en **[!UICONTROL Placements]**.
      1. Junto al nombre de la ubicación, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.
   1. En la esquina superior derecha, haga clic en ![Diagnóstico de ubicación](/help/dsp/assets/placement-diagnostics.png) o **[!UICONTROL Diagnostic]**.
1. Realice una de las siguientes acciones:
   * Para ver el registro de cambios:
      1. Haga clic **[!UICONTROL Change Log]**.
      1. (Opcional) Filtre los resultados del informe:
         * En el menú de fecha, cambie el periodo del informe de Últimos 14 días predeterminado a otro periodo (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* o *[!UICONTROL Last 1 year]*).
         * En el menú de la izquierda, filtre el informe por un nombre de usuario específico.
         * En el menú de la derecha, filtre el informe por una configuración de ubicación específica.
   * Para ver el estado de las aprobaciones de anuncios:
      1. En la esquina superior derecha, haga clic en **[!UICONTROL Ad Approvals]**.
      1. (Opcional) Para pausar o activar el anuncio, haga clic en el botón de estado (![Conmutador de estado](/help/dsp/assets/status-switch.png)) en la columna Anuncio ).
      1. (Opcional) Para abrir la configuración de un anuncio, haga clic en **[!UICONTROL View Ad]** junto al anuncio.
   * DSP Para ver por qué no se ha pujado por la ubicación, haga lo siguiente:
      1. En la esquina superior derecha, haga clic en **[!UICONTROL Non Bids]**.
      1. (Opcional) Para cambiar el intervalo de fechas, haga clic en el campo de fecha y seleccione una fecha o un intervalo de fechas diferentes.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Acerca de los informes en la plataforma](campaign-reports-about.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)

