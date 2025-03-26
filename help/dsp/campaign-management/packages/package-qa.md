---
title: Revisión y edición de la configuración del paquete mediante hojas de edición masiva
description: Obtenga información sobre cómo revisar y editar la configuración clave del paquete de forma masiva mediante hojas de cálculo.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: c482f476de5b79ee9a363791d62ba8c2ada12cbc
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Revisión y edición de la configuración del paquete mediante hojas de edición masiva

Puede descargar la configuración de uno o más paquetes en formato XLSX ([!DNL Microsoft Excel] hoja de cálculo) para su revisión. El archivo *hoja de edición masiva* incluye una ficha independiente con información de vuelo.

Para actualizar varias configuraciones a la vez, puede hacer una de las siguientes acciones:

* Realice cambios en los campos seleccionados, guarde el archivo y vuelva a cargar el archivo de hoja de edición masiva en DSP.

* Para realizar cambios en paquetes, ubicaciones o anuncios adicionales de la campaña, descargue una hoja de edición masiva para la campaña. Introduzca o pegue la configuración actualizada en el archivo y, a continuación, cargue el archivo para realizar los cambios. Para obtener instrucciones, consulte &quot;[Revisar y editar la configuración del componente de campaña mediante hojas de edición masiva](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

Los campos editables incluyen la mayoría de las configuraciones que normalmente se pueden editar.

>[!TIP]
>
>Para editar rápidamente más campos para uno o más paquetes, consulte &quot;[Editar paquetes](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Configuración de descarga para todos los paquetes de una campaña

Al descargar la configuración de todos los paquetes en una campaña, la hoja de edición masiva incluye fichas independientes para la configuración del paquete y para la información de vuelo. Si lo desea, puede incluir la configuración de las ubicaciones y los anuncios asociados con los paquetes; se incluyen pestañas adicionales para la configuración de ubicación y publicidad.

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

     Para editar cualquiera de las opciones, edite el archivo directamente y, a continuación, cargue los cambios. Todas las columnas editables se resaltan en azul.

## Configuración de descarga para paquetes específicos

Al descargar la configuración de paquetes específicos, el archivo de hoja de edición masiva incluye fichas independientes para la configuración del paquete y para la información de vuelo, y el archivo se puede editar.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Packages]**.

1. Seleccione las casillas de verificación de los paquetes cuya configuración desee descargar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Un mensaje de notificación indica cuándo está disponible la descarga del archivo de hoja de edición masiva.

1. Para descargar la hoja de edición masiva, siga uno de estos procedimientos:

   * En el mensaje de notificación, haga clic en **[!UICONTROL Download].**

   * En la parte derecha de la barra de menú superior, haga clic en ![Trabajos](/help/dsp/assets/downloads.png). Haga clic en **[!UICONTROL Download]** junto al trabajo.

     El archivo se guarda en la carpeta Descargas del explorador. Consulte &quot;[Columnas de colocación en hojas de edición masiva descargadas/cargadas](#qa-sheet-columns)&quot; para obtener una lista de las columnas incluidas.

     Para editar cualquiera de las opciones, edite el archivo directamente y, a continuación, cargue los cambios. Todas las columnas editables se resaltan en azul. Para utilizar el formato correcto para un campo, seleccione y copie el valor de la configuración de paquete o la configuración de ubicación correspondiente. Para algunas configuraciones de Target, como la partición del día, los objetivos personalizados y las métricas de conversión, hay una opción de copia disponible dentro de la configuración.

## Cargar una hoja de edición masiva con ajustes del paquete {#upload-bulksheet-package}

Puede cargar la configuración de sus paquetes, incluidas las ubicaciones y las publicidades asociadas con los paquetes, en un archivo de hoja de edición por lotes.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Realice una de las siguientes acciones:

   * Junto a la campaña principal, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Haga clic en el nombre de la campaña. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

     Esta opción está disponible en las fichas [!UICONTROL Packages], [!UICONTROL Placements] o [!UICONTROL Ads].

   * En el submenú, haga clic en **[!UICONTROL Packages]** y seleccione la casilla de verificación de cualquier paquete. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. En el diálogo [!UICONTROL Upload Bulksheet]:

   1. Arrastre y suelte un archivo en el cuadro o haga clic dentro del cuadro para seleccionar un archivo del dispositivo o de la red.

   1. Haga clic en **[!UICONTROL Upload]**.

1. (Opcional) Para comprobar que las actualizaciones se han procesado, haga clic en ![Trabajos](/help/dsp/assets/downloads.png) en la parte derecha de la barra de menús superior.

Cuando falla cualquier actualización de configuración, puede descargar un archivo de error de hoja de edición masiva con codificación de color para mostrar qué configuración (filas) se guardaron y cuáles fallaron, con un motivo para cada error. A continuación, puede solucionar los problemas dentro del mismo archivo y cargarlo de nuevo para procesar la información corregida.

<!--
## Package Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded bulksheet file, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |
-->

>[!MORELIKETHIS]
>
>* [Revisar y editar la configuración del componente de campaña mediante hojas de edición masiva](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Editar paquetes](/help/dsp/campaign-management/packages/package-edit.md)
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
