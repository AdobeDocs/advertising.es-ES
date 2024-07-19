---
title: Revisar y editar la configuración de ubicación mediante hojas de cálculo
description: Obtenga información sobre cómo revisar y editar la configuración de ubicación de claves mediante hojas de cálculo.
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---

# Revisar y editar la configuración de ubicación mediante hojas de cálculo

Puede descargar la configuración de una o varias ubicaciones, o de todas las ubicaciones de una campaña, en formato XLSX (hoja de cálculo de Excel) para su revisión. Utilice esta función para revisar rápidamente detalles como los siguientes:

* A qué audiencias se dirige la campaña.
* Cuando las ubicaciones empiezan a entregarse y cuando se detienen.
* Qué anuncios se adjuntan a las ubicaciones.

DSP A continuación, puede realizar cambios en los campos seleccionados y cargarlos de nuevo en todos los campos a la vez, para que se puedan cargar de nuevo en todos los campos a la vez. Los campos editables incluyen los nombres de ubicación, los estados, las ofertas, los presupuestos, las estrategias de ritmo y los límites de frecuencia.

>[!TIP]
>
>Para editar más campos para una o más ubicaciones, consulte &quot;[Editar ubicaciones](/help/dsp/campaign-management/placements/placement-edit.md)&quot;.

## Descargar configuración para todas las ubicaciones en una campaña

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Realice una de las acciones siguientes:

   * Junto al nombre de la campaña, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   * Haga clic en el nombre de la campaña para ver los detalles de la campaña. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   Un mensaje de notificación indica cuándo está disponible la descarga del archivo.

1. Realice una de las acciones siguientes:

   * En el mensaje de notificación, haga clic en **[!UICONTROL Download].**

   * En la parte derecha de la barra de menú superior, haga clic en ![Trabajos](/help/dsp/assets/downloads.png). Haga clic en **[!UICONTROL Download]** junto al trabajo.

   El archivo se guarda en la carpeta Descargas del explorador. Consulte &quot;[Columnas en hojas de cálculo descargadas/cargadas](#qa-sheet-columns)&quot; para obtener una lista de las columnas incluidas.

## Descargar configuración para una o más ubicaciones

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Seleccione la casilla de verificación situada junto a cada ubicación cuya configuración desee descargar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

El archivo se guarda automáticamente en la carpeta de descarga del explorador. Consulte &quot;[Columnas en hojas de cálculo descargadas/cargadas](#qa-sheet-columns)&quot; para obtener una lista de las columnas incluidas.

## Configuración de carga para todas las ubicaciones en una campaña

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Realice una de las acciones siguientes:

   * Junto al nombre de la campaña, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

   * Haga clic en el nombre de la campaña para ver los detalles de la campaña. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

1. En el diálogo [!UICONTROL Edit in Excel]:

   1. Arrastre y suelte un archivo en el cuadro o haga clic dentro del cuadro para seleccionar un archivo del dispositivo o de la red.

   1. Haga clic en **[!UICONTROL Upload]**.

1. (Opcional) Para comprobar que las actualizaciones se han procesado, haga clic en ![Trabajos](/help/dsp/assets/downloads.png) en la parte derecha de la barra de menús superior.

## Configuración de carga para una o varias ubicaciones

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Seleccione la casilla de verificación situada junto a cada ubicación cuya configuración desee cargar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. En el diálogo [!UICONTROL Edit in Excel]:

   1. Arrastre y suelte un archivo en el cuadro o haga clic dentro del cuadro para seleccionar un archivo del dispositivo o de la red.

   1. Haga clic en **[!UICONTROL Upload]**.

1. (Opcional) Para comprobar que las actualizaciones se han procesado, haga clic en ![Trabajos](/help/dsp/assets/downloads.png) en la parte derecha de la barra de menús superior.

## Columnas de configuración de ubicación en hojas de cálculo descargadas/cargadas{#qa-sheet-columns}

>[!TIP]
>
> En una hoja de cálculo descargada, todas las columnas editables se resaltan en azul.

### Hojas de cálculo a nivel de campaña

| Sección | Columna | Descripción | ¿Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | El ID numérico de la ubicación. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Nombre de la ubicación. | Sí |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Cualquier etiqueta aplicada para los informes. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Un vínculo para abrir la ubicación en modo de edición. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | El estado de la ubicación: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | Sí |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | El tipo de ubicación. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | El nombre del paquete principal, cuando corresponda. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | La fecha de inicio de la ubicación. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | La fecha de finalización de la ubicación. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Si dayparting es *[!UICONTROL ON]* o *[!UICONTROL OFF]*.DSP <br><b>Nota:</b> Para comprobar la programación real de la partición de día, abra la configuración de ubicación en el espacio de trabajo de la parte de día de la. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | El presupuesto de colocación, si lo hay. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | El intervalo de presupuesto: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | El objetivo del paquete. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | El valor objetivo del objetivo. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Si la ubicación se está desplazando hacia *[!UICONTROL Budget]* o *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | La puja máxima de la ubicación. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | Estrategia de ritmo de vuelo para la ubicación: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* o *[!UICONTROL aggressive frontload]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | Estrategia de ritmo intradía para la ubicación: *[!UICONTROL Even]* o *[!UICONTROL ASAP]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Cualquier criterio de filtro de oferta previa que se deba aplicar. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Si las reglas de oferta (obsoletas) son *[!UICONTROL ON]* o *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Límite de frecuencia principal de la ubicación durante el [!UICONTROL Frequency Cap Interval] especificado. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervalo para el límite de frecuencia principal: *[!UICONTROL Day]*, *[!UICONTROL Week]* o *[!UICONTROL Month]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Límite de frecuencia secundario para la ubicación durante el [!UICONTROL Secondary Frequency Cap Interval] especificado | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | El tipo de intervalo para el límite de frecuencia secundario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* o *[!UICONTROL Minute]*. El número aplicable de semanas, días, horas o minutos está indicado por [!UICONTROL Secondary Frequency Cap Interval Value]. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Número de semanas, días, horas o minutos durante los cuales se aplica [!UICONTROL Secondary Frequency Cap]. Por ejemplo, si el límite secundario es de tres impresiones por seis horas, el valor aquí sería `6`. | Sí |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Número de ubicaciones geográficas de destino *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Ubicaciones geográficas de destino, separadas por punto y coma o *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Número de ubicaciones geográficas excluidas o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Las ubicaciones geográficas excluidas, separadas por punto y coma o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | El número de ofertas de inventario público de destino, si se especifica alguno, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | El número de contratos de inventario público excluidos, si se especifican, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | El número de ofertas de inventario privado de destino, si se especifica alguno, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | El número de ofertas de inventario privado excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | El número de ofertas [!UICONTROL On-Demand Inventory] de destino, si se especifica alguna, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | El número de ofertas de inventario a petición excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | El tipo de tráfico de destino: *[!UICONTROL Website]* o *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Si la opción de segmentación de inventario para excluir el tráfico de salida es &lt;i[!UICONTROL >ON]* o *[!UICONTROL OFF]*.<br>Por lo general, los anuncios externos aparecen sobre el contenido como elementos emergentes o insertados en el contenido (en la experiencia nativa), en lugar de como anuncios de vídeo normales en un reproductor de vídeo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | La calidad de los sitios de destino: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* o *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | El número de categorías de sitios de destino, si se especifican, o *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | El número de categorías de sitios excluidos, si se especifican, o *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Los sitios excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Los idiomas del sitio de destino. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Solo ubicaciones de visualización estándar) Si se permite o no la entrega de anuncios en sitios no auditados: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Cuando la ubicación se dirige al inventario privado, esta opción puede enviar anuncios en sitios bloqueados. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | El número de sitios de destino, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Las audiencias de destino, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Las audiencias excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Indica si [!DNL Comscore] segmentos demográficos están habilitados para la ubicación (y otras ubicaciones en la campaña): *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Esta característica solo se puede habilitar para campañas en las que la característica [!DNL Audience Verification] esté habilitada para [!DNL Nielsen] y/o [!DNL Comscore].  Se cobran cargos adicionales. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Indica si se debe extender o no la segmentación de anuncios entre dispositivos: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. La segmentación entre dispositivos amplía la segmentación en todos los dispositivos conocidos de una persona, según el gráfico del dispositivo especificado en la configuración de la campaña. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - N.º incluido | El número de códigos de tema de destino, si los hay, o *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | El número de códigos de tema excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | El número de destinos de dispositivo de destino, si se especifica alguno, o *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | El número de destinos de dispositivo excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | El número de proveedores de ISP de destino, si se especifica alguno, o *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | El número de proveedores de ISP excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | El número de filtros de seguridad de marca aplicados, si se especifican, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | El número de filtros de bloqueo de fraude de oferta previa aplicados, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | El número de filtros de visibilidad de ofertas previas aplicados, si se especifican, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Indica si el bloque de seguridad del sitio está habilitado: *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | El número de píxeles de seguimiento de eventos de terceros adjuntos a la ubicación o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | El número de píxeles de seguimiento de conversión adjuntos a la ubicación o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Una tarifa estática de terceros que se rastreará como un coste no facturable por 1000 impresiones, si corresponde. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | El número de anuncios adjuntos a la ubicación, si los hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Nombres de los anuncios adjuntos a la ubicación o *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | DSP Los ID de anuncio únicos generados por el usuario de cualquier anuncio adjunto a la ubicación, separados por punto y coma. Para descargar una lista de nombres de anuncios e ID de anuncios asociados desde la vista [!UICONTROL Ads], cree una vista personalizada que incluya la métrica [!UICONTROL Ad ID] y, a continuación, [exporte los datos](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sí |

### Hojas de cálculo de nivel de ubicación

| Columna | Descripción | ¿Editable? |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | El ID numérico de la ubicación. | — |
| [!UICONTROL Placement Name] | Nombre de la ubicación. | Sí |
| [!UICONTROL Package Name] | El nombre del paquete principal, cuando corresponda. | — |
| [!UICONTROL Start Date] | La fecha de inicio de la ubicación. | — |
| [!UICONTROL End Date] | La fecha de finalización de la ubicación. | — |
| [!UICONTROL Status] | El estado de la ubicación: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | — |
| [!UICONTROL Max Bid] | La puja máxima de la ubicación. | Sí |
| [!UICONTROL Budget] | El presupuesto de colocación, si lo hay. | Sí |
| [!UICONTROL Budget Interval] | El intervalo de presupuesto: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sí |
| [!UICONTROL Primary Frequency Cap] | Límite de frecuencia principal de la ubicación durante el [!UICONTROL Primary Frequency Cap Interval] especificado. | Sí |
| [!UICONTROL Primary Frequency Cap Interval] | Intervalo para el límite de frecuencia principal: *[!UICONTROL Day]*, *[!UICONTROL Week]* o *[!UICONTROL Month]*. | Sí |
| [!UICONTROL Secondary Frequency Cap] | Límite de frecuencia secundario para la ubicación durante el [!UICONTROL Secondary Frequency Cap Interval] especificado | Sí |
| [!UICONTROL Secondary Frequency Cap Interval] | El tipo de intervalo para el límite de frecuencia secundario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* o *[!UICONTROL Minute]*. El número aplicable de semanas, días, horas o minutos está indicado por [!UICONTROL Secondary Frequency Cap Interval Value]. | Sí |
| [!UICONTROL Secondary Frequency Cap Interval Value] | Número de semanas, días, horas o minutos durante los cuales se aplica [!UICONTROL Secondary Frequency Cap]. Por ejemplo, si el límite secundario es de tres impresiones por seis horas, el valor aquí sería `6`. | Sí |
| [!UICONTROL Attached Ad ID] | DSP Los ID de anuncio únicos generados por el usuario de cualquier anuncio adjunto a la ubicación, separados por punto y coma. Para descargar una lista de nombres de anuncios e ID de anuncios asociados desde la vista [!UICONTROL Ads], cree una vista personalizada que incluya la métrica [!UICONTROL Ad ID] y, a continuación, [exporte los datos](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sí |

>[!MORELIKETHIS]
>
>* [Editar ubicaciones](/help/dsp/campaign-management/placements/placement-edit.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
