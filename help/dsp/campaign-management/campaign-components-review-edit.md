---
title: Revisión y edición de la configuración de componentes de Campaign mediante hojas de edición masiva
description: Obtenga información sobre cómo revisar y editar la configuración de paquetes, ubicaciones y anuncios clave de forma masiva mediante hojas de cálculo.
feature: DSP Placements
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Revisión y edición de la configuración de componentes de Campaign mediante hojas de edición masiva

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

Puede descargar la configuración de los paquetes, las ubicaciones y los anuncios en una sola campaña en formato XLSX ([!DNL Microsoft Excel] hoja de cálculo) para su revisión. De forma predeterminada, el archivo descargado incluye pestañas independientes para la configuración del paquete, la información de vuelo del paquete, la configuración de ubicación y las programaciones de anuncios de ubicación. Opcionalmente, puede excluir la configuración de algunos tipos de componentes de campaña.

Para actualizar varias configuraciones a la vez, cargue un archivo de hoja de edición masiva válido con los cambios. Para crear la hoja de edición masiva, puede descargar una plantilla de hoja masiva en blanco que incluya fichas para cada tipo de componente de campaña, introducir o pegar ajustes nuevos o actualizados en el archivo de plantilla y, a continuación, guardar el archivo para cargarlo. Los campos editables incluyen la mayoría de las configuraciones que normalmente se pueden editar.

>[!NOTE]
>
>También puede descargar y editar la configuración solo para paquetes específicos y ubicaciones específicas. Consulte &quot;[Revisar y editar la configuración de paquetes mediante hojas de edición masiva](/help/dsp/campaign-management/packages/package-qa.md)&quot; y &quot;[Revisar y editar la configuración de ubicación mediante hojas de edición masiva](/help/dsp/campaign-management/placements/placement-qa.md).&quot;

## Configuración de descarga para paquetes, ubicaciones y anuncios en una campaña

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. En el cuadro de diálogo [!UICONTROL QA Sheet Download], anule la selección de cualquier componente de campaña cuya configuración desee excluir del archivo descargado y, a continuación, haga clic en **[!UICONTROL Download]**.

De forma predeterminada, la configuración está seleccionada para todos los componentes de la campaña.

Un mensaje de notificación indica cuándo está disponible la descarga del archivo.

1. Para descargar el archivo, realice una de las acciones siguientes:

   * En el mensaje de notificación, haga clic en **[!UICONTROL Download].**

   * En la parte derecha de la barra de menú superior, haga clic en ![Trabajos](/help/dsp/assets/downloads.png). Haga clic en **[!UICONTROL Download]** junto al trabajo.

     El archivo se guarda en la carpeta Descargas del explorador. Consulte &quot;[Columnas de colocación en hojas de cálculo descargadas/cargadas](#qa-sheet-columns)&quot; para obtener una lista de las columnas incluidas.

>[!NOTE]
>
>No puede editar ni volver a cargar archivos de control de calidad de nivel de campaña. Para realizar cambios en la configuración del componente de campaña en estos archivos, [descargue un archivo de plantilla de configuración independiente (archivo de configuración)](#download-template), escriba o pegue filas del archivo QA en la plantilla, guarde el archivo y, a continuación, [cargue el archivo de plantilla rellenado](#upload-bulksheet-campaign-components).

## Descargar una plantilla de hoja de edición masiva para una campaña {#download-template}

Descargue una plantilla de hoja de edición masiva en blanco que incluya fichas para cada tipo de componente de campaña. Más tarde puede agregar filas a cualquier pestaña de la plantilla y [cargar el archivo editado](##upload-bulksheet-campaign-components) para realizar cambios en los componentes de la campaña.

1. Haga clic en el nombre de la campaña.

1. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. En el cuadro de diálogo [!UICONTROL Upload Bulksheet], haga clic en **[!UICONTROL Bulksheet Template].**

   El archivo se guarda en la carpeta Descargas del explorador. Consulte &quot;[Columnas de colocación en hojas de cálculo descargadas/cargadas](#qa-sheet-columns)&quot; para obtener una lista de las columnas incluidas.

## Cargar una hoja de edición masiva con la configuración de paquete, ubicación y publicidad para una campaña{#upload-bulksheet-campaign-components}

Cargue la configuración de paquetes, ubicaciones y publicidades en una sola campaña a la vez en una hoja de edición por lotes rellenada.

1. [Descargue una plantilla de hoja de edición masiva](#download-template) si es necesario, especifique o pegue la configuración del paquete, la ubicación o el anuncio en las fichas correspondientes de una plantilla de hoja de edición masiva y, a continuación, guarde el archivo en su dispositivo o red.

   Consulte las configuraciones disponibles a continuación.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En la esquina superior derecha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. En el diálogo [!UICONTROL Upload Bulksheet]:

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

>[!MORELIKETHIS]
>
>* [Revisar y editar la configuración del paquete mediante hojas de edición masiva](/help/dsp/campaign-management/packages/package-qa.md)
>* [Revisar y editar la configuración de ubicación mediante hojas de edición masiva](/help/dsp/campaign-management/placements/placement-qa.md)
