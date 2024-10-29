---
title: Revisión y edición de la configuración del paquete mediante hojas de edición masiva
description: Aprenda a revisar y editar la configuración de los paquetes clave de forma masiva mediante hojas de cálculo.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Revisión y Editar paquetes Configuración utilizando hojas de edición en bloque

Puede descargar la configuración de uno o más paquetes en XLSX ([!DNL Microsoft Excel] hoja de cálculo) formato para su revisión. La hoja de cálculo incluye un pestaña separado con información de vuelo.

Para actualizar varias configuraciones a la vez, puede hacer una de las siguientes acciones:

* DSP Realice cambios en los campos seleccionados, guarde el archivo y vuelva a cargar el archivo de hoja de edición masiva en el archivo de hoja de edición de la hoja de cálculo de la hoja de cálculo de la hoja de cálculo de la hoja de cálculo de la hoja de cálculo de la hoja de cálculo de la hoja de datos de la hoja de cálculo de.

* Para realizar cambios en paquetes adicionales y en la configuración de cualquier ubicación o publicidad, descargue una plantilla de hoja de edición masiva en blanco que incluya pestañas para cada tipo de componente de campaña, introduzca o pegue la configuración nueva o actualizada en el archivo de plantilla y, a continuación, cargue el archivo para realizar los cambios. Para obtener instrucciones, consulte &quot;[Revisar y editar la configuración del componente de campaña mediante hojas de edición masiva](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

Los campos editables incluyen la mayoría de las configuraciones que normalmente se pueden editar.

>[!TIP]
>
>Para editar rápidamente más campos para uno o más paquetes, consulte &quot;[Editar paquetes](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Configuración de descarga para todos los paquetes de una campaña

Al descargar la configuración de todos los paquetes en una campaña, la hoja de cálculo incluye pestañas independientes para la configuración del paquete y para la información de vuelo. Si lo desea, puede incluir la configuración de las ubicaciones y los anuncios asociados con los paquetes; se incluyen pestañas adicionales para la configuración de ubicación y publicidad.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. En el cuadro de diálogo, anule la [!UICONTROL QA Sheet Download] selección de cualquier componente campaña cuya configuración desee excluir del archivo descargado y, a continuación, haga clic en **[!UICONTROL Download]**.

De forma predeterminada, se selecciona la configuración de todas las colocaciones y anuncios asociados con los paquetes.

Un mensaje notificación indica cuándo el archivo está disponible para descargar.

1. Para descargar el archivo, realice una de las acciones siguientes:

   * En el mensaje de notificación, haga clic en **[!UICONTROL Download].**

   * En la parte derecha de la barra de menú superior, haga clic en ![Trabajos](/help/dsp/assets/downloads.png). Haga clic en **[!UICONTROL Download]** junto al trabajo.

     El archivo se guarda en la carpeta Descargas del explorador. Consulte &quot;[Columnas de colocación en hojas de cálculo descargadas/cargadas](#qa-sheet-columns)&quot; para obtener una lista de las columnas incluidas.

>[!NOTE]
>
>No puede editar y volver a cargar hojas de control de calidad a nivel de campaña. Para realizar cambios en la configuración del componente de campaña en estos archivos, descargue una plantilla de hoja de edición masiva independiente, introduzca o pegue filas de la hoja de control de calidad en la plantilla de hoja de edición masiva y guarde el archivo, y luego cargue la hoja de edición masiva rellenada. Para obtener instrucciones, consulte &quot;[Revisar y editar la configuración del componente de campaña mediante hojas de edición masiva](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

## Configuración de descarga para uno o más paquetes

Al descargar la configuración de paquetes específicos, el archivo de hoja de edición masiva incluye fichas independientes para la configuración del paquete y para la información de vuelo, y el archivo se puede editar.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Packages]**.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Un mensaje de notificación indica cuándo está disponible la descarga del archivo de hoja de edición masiva.

1. Para descargar la hoja de edición masiva, siga uno de estos procedimientos:

   * En el mensaje de notificación, haga clic en **[!UICONTROL Download].**

   * En la parte derecha de la barra de menú superior, haga clic en ![Trabajos](/help/dsp/assets/downloads.png). Haga clic en **[!UICONTROL Download]** junto al trabajo.

     El archivo se guarda en la carpeta Descargas del explorador. Consulte &quot;[Columnas de colocación en hojas de cálculo descargadas/cargadas](#qa-sheet-columns)&quot; para obtener una lista de las columnas incluidas.

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Cargar una hoja de edición masiva con ajustes del paquete {#upload-bulksheet-package}

Puede cargar la configuración de sus paquetes, incluidas las ubicaciones y las publicidades asociadas con los paquetes, en un archivo de hoja de edición por lotes.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. En el diálogo [!UICONTROL Upload Bulksheet]:

   1. Arrastre y suelte un archivo en el cuadro o haga clic dentro del cuadro para seleccionar un archivo del dispositivo o de la red.

   1. Haga clic en **[!UICONTROL Upload]**.

1. (Opcional) Para comprobar que se han procesado las actualizaciones, haga clic ![en Trabajos](/help/dsp/assets/downloads.png) en la parte derecha de la barra de menú superior.

## Columnas de configuración de paquetes en hojas de cálculo descargadas/cargadas{#qa-sheet-columns-packages}

>[!TIP]
>
> En una hoja de cálculo descargada, todas las columnas editables se resaltan en azul.

### [!UICONTROL Package] ficha

| Sección | Columna | Descripción | ¿Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | El ID numérico del paquete. | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | El nombre del paquete. | Sí |
| [!UICONTROL Basic details] | [!UICONTROL Status] | El estado del paquete: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | Sí |
| [!UICONTROL Basic details] | [!UICONTROL Description] | Una descripción opcional del paquete. | Sí |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | Una tarifa estática de terceros que se registrará como un costo no facturable por cada 1000 impresiones, si corresponde. | Sí |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | Una descripción opcional de la tarifa de terceros, si corresponde. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | La fecha de inicio del paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | La fecha de finalización del paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | Nivel al que se van a espaciar y limitar las ubicaciones en el paquete: *[!UICONTROL Package]* o *[!UICONTROL Placement]*. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | El presupuesto del paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | El intervalo de presupuesto: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Un límite de intervalo presupuestario opcional. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | El intervalo para el límite del intervalo de presupuesto opcional: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, o *[!UICONTROL All Time]*. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | El objetivo del paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | El valor objetivo del objetivo. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Paquetes con los objetivos de optimización &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solamente)Un [objetivo personalizado](/help/dsp/optimization/custom-goal.md) que incluye los eventos de conversión o ingresos usados para calcular la métrica de CPA o ROAS. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Opcional; paquetes con los objetivos de optimización &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solamente) El evento de conversión final o la cantidad de evento/venta de ingresos que se utilizará para calcular el retorno del gasto en publicidad o el coste por adquisición. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Solo paquetes con objetivos de optimización personalizados) El propósito del paquete, que ayuda a determinar cómo optimizar el paquete: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* o *[!UICONTROL Other]* | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Solo paquetes con objetivos de optimización personalizados) El ID del paquete de otro paquete cuyos datos históricos se utilizan como entrada para optimizar el paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Solo paquetes con objetivos de optimización personalizados) Otro paquete cuyos datos históricos se utilizan como entrada para optimizar el paquete. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Si el paquete se está desplazando hacia *[!UICONTROL budget]* o *[!UICONTROL primary_goal]* (para impresiones). | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (Cuando coloca el paquete en impresiones) El número de destino de las impresiones durante el intervalo de tiempo especificado. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (Cuando coloca el paquete en impresiones) El intervalo de tiempo para el número de destino de impresiones. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | Estrategia de ritmo de vuelo del paquete: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* o *[!UICONTROL aggressive frontload]*. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | La estrategia de ritmo intradía para el paquete: *[!UICONTROL Even]* o *[!UICONTROL ASAP]*. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | Límite de frecuencia principal del paquete durante el [!UICONTROL Frequency Cap Interval] especificado. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | Intervalo para el límite de frecuencia principal: *[!UICONTROL Day]*, *[!UICONTROL Week]* o *[!UICONTROL Month]*. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | Número de semanas, días, horas o minutos durante los cuales se aplica la [!UICONTROL Frequency Cap] principal. Por ejemplo, si el límite principal es de 12 impresiones por mes, el valor aquí sería `12`. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | Límite de frecuencia secundario del paquete durante el [!UICONTROL Secondary Frequency Cap Interval] especificado | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | El tipo de intervalo para el límite de frecuencia secundario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* o *[!UICONTROL Minute]*. El número aplicable de semanas, días, horas o minutos está indicado por [!UICONTROL Secondary Frequency Cap Interval Value]. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | Número de semanas, días, horas o minutos durante los cuales se aplica [!UICONTROL Secondary Frequency Cap]. Por ejemplo, si el límite secundario es de tres impresiones por seis horas, el valor aquí sería `6`. | Sí |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Indica si se crearán o no vuelos de ritmo sin par para el paquete *T* (true) o *F* (false). Una vez que habilite el vuelo personalizado y guarde el paquete, no podrá deshabilitar el vuelo personalizado ni editar la fecha de inicio del paquete. | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Disponible solo cuando la opción [!UICONTROL Activate Custom Flighting] está habilitada) Indica si se debe o no agregar automáticamente cualquier presupuesto restante del vuelo anterior al presupuesto existente para el siguiente vuelo: *T* (true) o *F* (false). | Sí |
| [!UICONTROL Error] | [!UICONTROL Error] | Cualquier error relevante. | — |

### [!UICONTROL Package_Flights] Pestaña {#qa-sheet-columns-package-flights}

| Sección | Columna | Descripción | ¿Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | El ID numérico del paquete. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | El ID numérico del vuelo. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | La primera fecha del vuelo. | Sí |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | La fecha final del vuelo. | Sí |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | El objetivo de gasto destino para el vuelo. | Sí |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Paquetes existentes sin la opción &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; habilitada) Una cantidad de presupuesto potencialmente no gastado para agregar al siguiente vuelo. | Sí |

>[!MORELIKETHIS]
>
>* [Revisar y editar la configuración del componente de campaña mediante hojas de edición masiva](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Editar paquetes](/help/dsp/campaign-management/packages/package-edit.md)
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
