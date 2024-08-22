---
title: Revisión y edición de la configuración del paquete mediante hojas de cálculo
description: Obtenga información sobre cómo revisar y editar la configuración clave de paquetes mediante hojas de cálculo.
feature: DSP Packages
source-git-commit: 230a169611aa3094365a877476f2e5e1c6b3cb9b
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# Revisión y edición de la configuración del paquete mediante hojas de cálculo

Puede descargar la configuración de uno o más paquetes en formato XLSX ([!DNL Microsoft Excel] hoja de cálculo) para su revisión. La hoja de cálculo incluye una pestaña independiente con información de vuelo. DSP A continuación, puede realizar cambios en los campos de selección de ambas pestañas y cargar los datos de nuevo a todos los campos a la vez, de forma que se devuelvan a los datos a los que se va a realizar la selección. Los campos editables incluyen la mayoría de las configuraciones que normalmente se pueden editar.

>[!TIP]
>
>Para editar más campos para uno o más paquetes, consulte &quot;[Editar paquetes](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Configuración de descarga para uno o más paquetes

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Packages]**.

1. Seleccione la casilla de verificación situada junto a cada paquete cuya configuración desee descargar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

El archivo se guarda automáticamente en la carpeta de descarga del explorador. Consulte &quot;[Columnas del paquete en hojas de cálculo descargadas/cargadas](#qa-sheet-columns-packages)&quot; para obtener una lista de las columnas incluidas.

## Configuración de carga para uno o más paquetes

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Packages]**.

1. Seleccione la casilla de verificación situada junto a cada paquete cuya configuración desee cargar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. En el diálogo [!UICONTROL Edit in Excel]:

   1. Arrastre y suelte un archivo en el cuadro o haga clic dentro del cuadro para seleccionar un archivo del dispositivo o de la red.

   1. Haga clic en **[!UICONTROL Upload]**.

1. (Opcional) Para comprobar que las actualizaciones se han procesado, haga clic en ![Trabajos](/help/dsp/assets/downloads.png) en la parte derecha de la barra de menús superior.

## Columnas de configuración de paquetes en hojas de cálculo descargadas o cargadas{#qa-sheet-columns-packages}

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
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | Una tarifa estática de terceros que se rastreará como un coste no facturable por 1000 impresiones, si corresponde. | Sí |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | Una descripción opcional de la tarifa de la tarifa de terceros, si corresponde. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | La fecha de inicio del paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | La fecha de finalización del paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | Nivel al que se van a espaciar y limitar las ubicaciones en el paquete: *[!UICONTROL Package]* o *[!UICONTROL Placement]*. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | El presupuesto del paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | El intervalo de presupuesto: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Un límite de intervalo presupuestario opcional. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | Intervalo para el límite de intervalo de presupuesto opcional: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | El objetivo del paquete. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | El valor objetivo del objetivo. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Paquetes con los objetivos de optimización &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solamente)Un [objetivo personalizado](/help/dsp/optimization/custom-goal.md) que incluye los eventos de conversión o ingresos usados para calcular la métrica de CPA o ROAS. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Opcional; paquetes con los objetivos de optimización &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solamente) El evento de conversión final o la cantidad de evento/venta de ingresos que se utilizará para calcular el retorno del gasto en publicidad o el coste por adquisición. | Sí |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Solo paquetes con objetivos de optimización personalizados) El propósito del paquete, que ayuda a determinar cómo optimizar el paquete: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* o *[!UICONTROL Other]* | — |
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

### [!UICONTROL Package_Flights] ficha

| Sección | Columna | Descripción | ¿Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | El ID numérico del paquete. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | El ID numérico del vuelo. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | La primera fecha del vuelo. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | La fecha final del vuelo. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | El objetivo gasta la meta para el vuelo. | — |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Paquetes existentes sin la opción &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; habilitada) Una cantidad de presupuesto potencialmente no gastado para agregar al siguiente vuelo. | — |

>[!MORELIKETHIS]
>
>* [Editar paquetes](/help/dsp/campaign-management/packages/package-edit.md)
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
