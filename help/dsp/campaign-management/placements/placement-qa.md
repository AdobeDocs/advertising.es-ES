---
title: Revisión y edición de la configuración de ubicación mediante hojas de edición masiva
description: Obtenga información sobre cómo revisar y editar la configuración de ubicación de claves de forma masiva mediante hojas de cálculo.
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Revisión y edición de la configuración de ubicación mediante hojas de edición masiva

Puede descargar la configuración de una o varias ubicaciones, o de todas las ubicaciones de una campaña, en formato XLSX ([!DNL Microsoft Excel] hoja de cálculo) para su revisión. Utilice esta función para revisar rápidamente detalles como los siguientes:

* A qué audiencias se dirige la campaña.
* Cuando las ubicaciones empiezan a entregarse y cuando se detienen.
* Qué anuncios se adjuntan a las ubicaciones.

Para actualizar varias configuraciones a la vez, puede realizar cambios en determinados campos, guardar el archivo y volver a cargar el archivo de hoja de edición masiva en DSP. Los campos editables incluyen la mayoría de las configuraciones editables.

>[!TIP]
>
>Para editar rápidamente más campos para una o más ubicaciones, consulte &quot;[Editar ubicaciones](/help/dsp/campaign-management/placements/placement-edit.md)&quot;.

## Descargar configuración para todas las ubicaciones en una campaña

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Realice una de las acciones siguientes:

   * Junto a la campaña, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   * Haga clic en el nombre de la campaña. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

1. En el cuadro de diálogo [!UICONTROL Bulksheet Download], anule la selección de cualquier componente de campaña cuya configuración desee excluir del archivo descargado y, a continuación, haga clic en **[!UICONTROL Download]**.

De forma predeterminada, se selecciona la configuración de todas las ubicaciones y anuncios asociados con los paquetes.

Un mensaje de notificación indica cuándo está disponible la descarga del archivo.

1. Para descargar el archivo, realice una de las acciones siguientes:

   * En el mensaje de notificación, haga clic en **[!UICONTROL Download].**

   * En la parte derecha de la barra de menú superior, haga clic en ![Trabajos](/help/dsp/assets/downloads.png). Haga clic en **[!UICONTROL Download]** junto al trabajo.

   El archivo se guardará en la carpeta Descargas del explorador.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

## Descargar configuración para ubicaciones específicas

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Seleccione la casilla de verificación situada junto a cada ubicación cuya configuración desee descargar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Un mensaje de notificación indica cuándo está disponible la descarga del archivo de hoja de edición masiva.

1. Para descargar la hoja de edición masiva, siga uno de estos procedimientos:

   * En el mensaje de notificación, haga clic en **[!UICONTROL Download].**

   * En la parte derecha de la barra de menú superior, haga clic en ![Trabajos](/help/dsp/assets/downloads.png). Haga clic en **[!UICONTROL Download]** junto al trabajo.

   El archivo se guardará en la carpeta Descargas del explorador.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

   Para editar cualquiera de las opciones, edite el archivo directamente y, a continuación, cargue los cambios.  Todas las columnas editables se resaltan en azul. Para utilizar el formato correcto para un campo, seleccione y copie el valor de la configuración de paquete o la configuración de ubicación correspondiente. Para algunas configuraciones de Target, como la partición del día, los objetivos personalizados y las métricas de conversión, hay una opción de copia disponible dentro de la configuración.

## Cargar una hoja de edición masiva con configuración de ubicación {#upload-bulksheet-placement}

Puede cargar la configuración de sus ubicaciones, y de los anuncios y paquetes asociados con las ubicaciones, en un archivo de hoja de edición por lotes.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Realice una de las siguientes acciones:

   * Junto a la campaña principal, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Haga clic en el nombre de la campaña. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

     Esta opción está disponible en las fichas [!UICONTROL Packages], [!UICONTROL Placements] o [!UICONTROL Ads].

   * En el submenú, haga clic en **[!UICONTROL Placements]** y seleccione la casilla de verificación de cualquier ubicación. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. En el diálogo [!UICONTROL Upload Bulksheet]:

   1. Arrastre y suelte un archivo en el cuadro o haga clic dentro del cuadro para seleccionar un archivo del dispositivo o de la red.

   1. Haga clic en **[!UICONTROL Upload]**.

1. (Opcional) Para comprobar que las actualizaciones se han procesado, haga clic en ![Trabajos](/help/dsp/assets/downloads.png) en la parte derecha de la barra de menús superior.

Cuando falla cualquier actualización de configuración, puede descargar un archivo de error de hoja de edición masiva con codificación de color para mostrar qué configuración (filas) se guardaron y cuáles fallaron, con un motivo para cada error. A continuación, puede solucionar los problemas dentro del mismo archivo y cargarlo de nuevo para procesar la información corregida.

<!--
## Placement Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded bulksheet, all editable columns are highlighted in blue.

### [!UICONTROL Placements] Sheet

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Any applied labels, for reporting. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | A link to open the placement in Edit mode. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Status] | The placement status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | The placement type. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | The name of the parent package, when applicable. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | The start date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL End Date] | The end date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Whether dayparting is *[!UICONTROL ON]* or *[!UICONTROL OFF]*.<br><b>Note:</b> To check the actual dayparting schedule, open the placement settings in DSP. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Budget] | The placement budget, if there is one. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | The objective of the package. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | The target value of the goal. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Whether the placement is pacing towards the *[!UICONTROL Budget]* or *[!UICONTROL Impressions]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | The maximum bid for the placement. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the placement: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the placement: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Any pre-bid filter criteria to be applied. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Whether bidding rules (deprecated) are *[!UICONTROL ON]* or *[!UICONTROL OFF]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | The primary frequency cap for the placement during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the placement during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | The number of targeted geographical locations, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | The targeted geographical locations, separated by semi-colons,or *[!UICONTROL All Locations]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | The number of excluded geographical locations or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | The excluded geographical locations, separated by semi-colons,  or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | The number of targeted public inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | The number of excluded public inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | The number of targeted private inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | The number of excluded private inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | The number of targeted [!UICONTROL On-Demand Inventory] deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | The number of excluded On-Demand Inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | The targeted type of traffic: *[!UICONTROL Website]* and/or *[!UICONTROL Apps]* | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | The quality of the sites to target: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, or *[!UICONTROL All Sites]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | The number of targeted site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | The number of excluded site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | The excluded sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Language] | The targeted site languages. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Standard display placements only) Whether or not to allow ad delivery on non-audited sites: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. When the placement targets private inventory, this option may deliver ads on blocked sites. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | The number of targeted sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | The targeted audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | The excluded audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Whether or not [!DNL Comscore] demographic segments are enabled for the placement (and other placements in the campaign): *[!UICONTROL ON]* or *[!UICONTROL OFF]*. This feature may be enabled only for campaigns for which the [!DNL Audience Verification] feature is enabled for [!DNL Nielsen] and/or [!DNL Comscore].  It incurs additional fees.  | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Whether or not to extend the ad targeting across devices: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Included # | The number of targeted topic codes, if any are specified, or *[!UICONTROL All]*.   | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | The number of excluded topic codes, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | The number of targeted device targets, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | The number of excluded device targets, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | The number of targeted ISP providers, if any are specified, or *[!UICONTROL All]/i>. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | The number of excluded ISP providers, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | The number of brand safety filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | The number of pre-bid fraud blocking filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | The number of pre-bid viewability filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don't see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |

### [!UICONTROL Placement_AdSchedules] Sheet

| [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Placement Name] | The name of the placement. | &mdash; |
| [!UICONTROL Ad ID] | The numeric ID of the ad. | &mdash; |
| [!UICONTROL Ad Name] | The name of the ad. | Yes |
| [!UICONTROL Start Date] | The start date of the ad. | &mdash; |
| [!UICONTROL End Date] | The end date of the ad. | &mdash; |
| [!UICONTROL Adobe Ad Approval Status] | The status of the Advertising DSP approval process, such as *Approved* or *Incomplete*. | &mdash; |
| [!UICONTROL Flight 1 Start Date] - [!UICONTROL Flight 12 Start Date] | The start date for a specific flight. | Yes |
| [!UICONTROL Flight 1 End Date] - [!UICONTROL Flight 12 End Date] | The end date for a specific flight. | Yes |
| [!UICONTROL Flight 1 Weight] - [!UICONTROL Flight 12 Weight] | How to rotate a specific ad for a specific flight:  *Even* to rotate the ad evenly, or a relative weight by which to rotate the ad, as a percentage (such as `40` for 40%); the total weights for all ads in the flight must equal 100. | Yes |

### [!UICONTROL Placement_BidMultipliers] Sheet

*Available in campaign-level bulksheets only*

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL Country] | The bid multiplier and the name of the country, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL State] | The bid multiplier and the name of the state. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL City] | The bid multiplier and the name of the city, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL DMA] | (U.S. locations only) The bid multiplier and the designated market area, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL Postal code] | The bid multiplier and the postal code, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory Source] | The bid multiplier and the public inventory source, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory Feed] | The bid multiplier and the public inventory feed, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL OnDemand Inventory Source] | The bid multiplier and the OnDemand inventory source, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL OnDemand Inventory Feed] | The bid multiplier and the OnDemand inventory feed, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Sites/Apps] | [!UICONTROL Domains] | The bid multiplier and the domains, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Sites/Apps] | [!UICONTROL Category] | The bid multiplier and the site/app category, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Audience] | [!UICONTROL Daypart] | The bid multiplier and the daypart interval, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Audience] | [!UICONTROL Topics - Comscore] | The bid multiplier and the [!DNL Comscore] topics, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Ads.txt] | The bid multiplier and the level of [Ads.txt](https://iabtechlab.com/ads-txt-about/) pre-bid filtering to use, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |

-->

<!-- LOTS MORE THAN I HAD ORIGINALLY DOCUMENTED -- BELOW ARE THE LAST, BUT NOT ALL:

| Brand Safety | Brand Safety - Contextual Filtering # |  |  |
| Brand Safety | Brand Safety - Pre-Bid Fraud blocking # |  |  |
| Brand Safety | Brand Safety - Pre-Bid Viewability # |  |  |
| Brand Safety | Site Safety Block |  |  |
| Tracking | Tracking Pixels # |  |  |
| Tracking | Conversion Pixels # |  |  |
| Tracking | 3rd-party fees |  |  |
| # of Ads Attached |  |  |
| Ads |  Ad Names |  |  |
| Ads | Attached Ad ID |  |  |
| Environment | Environment |  |  |
-->

<!-- 
Check on Brand Safety - Contextual Filtering # with new DV feature/fct change.
-->

>[!MORELIKETHIS]
>
>* [Revisar y editar la configuración del componente de campaña mediante hojas de edición masiva](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Editar ubicaciones](/help/dsp/campaign-management/placements/placement-edit.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
