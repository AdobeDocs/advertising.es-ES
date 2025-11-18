---
title: Administrar informes personalizados
description: Obtenga información sobre cómo generar y administrar la experiencia cruzada [!UICONTROL Custom Creative Report].
feature: Creative Reporting
source-git-commit: 455a63be51ca56610cc15ba498e69eeae52ffdba
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

Puede crear, duplicar, editar, ejecutar, descargar y eliminar informes personalizados.

## Creación de un informe personalizado {#report-create}

1. En el menú principal, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]**.

1. Especifique la [configuración del informe](#report-settings).

1. Haga clic en **[!UICONTROL Create Custom Report]**.

## Duplicación de un informe personalizado

Duplique un informe personalizado para crear un nuevo informe con una configuración similar.

1. En el menú principal, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Junto al nombre del informe, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Copy]**.

1. (Opcional) Edite la [configuración del informe](#report-settings.md) según sea necesario.

   El nombre del informe, de forma predeterminada, es &quot;\&lt;*nombre de informe existente*\> \#2&quot; (o el siguiente número de la secuencia).

## Edición de un informe personalizado {#report-edit}

1. En el menú principal, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Junto al nombre del informe, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Editar la [configuración del informe](#report-settings.md).

1. Haga clic en **[!UICONTROL Edit Custom Report]**.

## Ejecutar un informe personalizado &lbrace;report-run-now&rbrace;

Puede ejecutar cualquier informe que no haya caducado y que no se esté ejecutando actualmente.

>[!NOTE]
>
>También puede ejecutar un informe personalizado al [crearlo](#report-create) o [editarlo](#report-edit).

1. En el menú principal, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Junto al nombre del informe, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Run Now]**.

   Cuando se completa el informe, se envía a los destinos especificados en la configuración del informe.

## Descargar un informe personalizado

Puede descargar cualquier instancia de informe completada de los últimos cuatro meses, que tenga el estado &quot;[!UICONTROL Ready to Download]&quot; o &quot;[!UICONTROL Completed]&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. En la columna [!UICONTROL Download Report] de la fila del informe, haga lo siguiente:

   * Para descargar la última instancia del informe, haga clic en **[!UICONTROL Download]**.

   * (Informes con varias instancias) Haga clic en ![la flecha abajo](/help/dsp/assets/chevron-down.png "la flecha abajo") junto a [!UICONTROL Download] y, a continuación, haga clic en la fecha de finalización del informe que desee descargar. Las instancias de informe descargables se indican con un icono de descarga (![icono de descarga](/help/dsp/assets/indicator-downloadable.png "icono de descarga")).

     Cuando haya muchas instancias disponibles, haga clic en **[!UICONTROL Load More]** en la parte inferior de la lista si es necesario.

     Cuando un informe se ejecuta varias veces en el mismo día, las instancias de informe de ese día se enumeran en orden cronológico, con la instancia más reciente en la parte superior.

     Los trabajos de informe con errores se indican con un icono de error (![indicador de error](/help/dsp/assets/indicator-critical.png "indicador de error")) y no se pueden descargar. Mantenga el cursor sobre el icono de error para ver una descripción del error.

## Eliminación de un informe personalizado

1. En el menú principal, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Junto al nombre del informe, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Configuración de informes {#report-settings}

**[!UICONTROL Name]:** El nombre del informe. La longitud máxima es de 180 caracteres.

**[!UICONTROL Report Type]:** Tipo de informe.

### Sección [!UICONTROL Report Range]

Esta sección determina los datos que se incluyen en el informe. Para configurar las fechas de la programación del informe, consulte la sección &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** Zona horaria para los informes.

**[!UICONTROL Observe Daylight Savings Time]:** considera el horario de verano en los horarios informados.

**Intervalo:** Intervalo de fecha para el que se van a generar datos. El número de días disponibles varía según el informe y las dimensiones seleccionadas. Elija uno:

* **[!UICONTROL Previous Calendar Week]:** Incluye datos de la semana anterior.

* **[!UICONTROL Previous Calendar Month]:** Incluye datos del mes calendario anterior.

* **[!UICONTROL Custom Range]:** Incluye datos entre fechas de inicio y finalización específicas. Para informar desde el día anterior, seleccione **[!UICONTROL Present]**.

### Sección [!UICONTROL Report Run schedule]

Esta sección determina las fechas en las que se ejecuta el informe. Para configurar las fechas en las que se incluirán los datos del informe, consulte la sección &quot;[!UICONTROL Report range]&quot;.

**\[Programación\]:** Cuándo generar el informe:

* *[!UICONTROL Immediately]*: agrega inmediatamente el informe a la cola de informes.

  >[!NOTE]
  >
  >También puede [ejecutar un informe personalizado en cualquier momento](#report-run-now) desde la vista [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\>:* Ejecuta el informe en una fecha especificada para su finalización antes del 09:00 en el huso horario de la cuenta.

* *[!UICONTROL Recurring]:* Ejecuta el informe de acuerdo con una programación durante un período de tiempo especificado.

   * **\[Programación\]:** La frecuencia con la que se ejecutará el informe:

      * *Diario* para ejecutar el informe cada N días. Por ejemplo, para ejecutar el informe cada dos semanas (14 días), seleccione esta opción y escriba **14**.

      * *Semanalmente* para ejecutar el informe en los días de la semana especificados. Por ejemplo, para ejecutar el informe todos los lunes y viernes, selecciona esta opción y las casillas de verificación que aparecen junto a **Lunes** y **Viernes**.

      * *Mensual* para ejecutar el informe en un día numérico específico del mes, del 1 al 30. Por ejemplo, para ejecutar el informe el primer día de cada mes, seleccione esta opción y escriba **1**.

   * **Desde**: Primera fecha en que se puede ejecutar el informe. Según la programación especificada, la primera instancia de informe puede producirse después de esta fecha.

   * **Hasta**: La fecha de caducidad del informe, que puede ser dentro de cuatro meses calendario. Antes de que caduque un informe, todos los destinos de correo electrónico especificados reciben una alerta de correo electrónico siete días y un día antes de la fecha de caducidad. Para mantener el informe más tiempo, cambie esta fecha.

### Sección [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (Opcional) Dimensiones adicionales mediante las cuales filtrar los datos, independientemente de si las dimensiones se incluyen o no como columnas en el informe. Los filtros disponibles varían según el tipo de informe y pueden incluir: *[!UICONTROL Advertiser]*, *[!UICONTROL Experience]*, *[!UICONTROL Creative Library]* y *[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->.

Para aplicar uno o más filtros, haga lo siguiente:

* Seleccione una dimensión, seleccione el operador (*es igual a* o *no es igual a*) y, a continuación, seleccione el valor aplicable. Por ejemplo, para devolver datos solo para anuncios de preroll, especifique &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Opcional) Añada criterios adicionales al filtro.
* (Opcional) Añada filtros adicionales, cada uno con uno o más criterios.

### Sección [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** Las columnas de datos, o encabezados, que se incluirán en el informe. Para agregar una columna, expanda la categoría y active la casilla de verificación situada junto al nombre de la columna. Las columnas disponibles varían según el informe y todas las métricas no disponibles están deshabilitadas.<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** El orden de los encabezados de columna. Puede arrastrar y soltar cualquier columna para personalizar el orden.

**[!UICONTROL Format]:** Indica si se generará un informe en formato *[!UICONTROL CSV]* (valores separados por comas) o *[!UICONTROL Tab]* (valores separados por tabulaciones).

**[!UICONTROL Headers]:** Ya sea para *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* encabezados de columna.

### Sección [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** La configuración varía según el tipo de informe:

* **\[Tipo de regla\]:** (Anunciantes con solo seguimiento de conversión de Adobe Advertising) En el informe, explica cómo atribuir datos de conversión en una serie de eventos que llevan a una conversión. Puede elegir más de una regla si desea comparar las diferencias entre las reglas.

  >[!NOTE]
  >
  >Las rutas de conversión incluyen cualquier impresión y clic dentro de las ventanas retrospectivas de impresiones o clics del anunciante, que están configuradas en [!DNL Advertising Search, Social, & Commerce]. Los clics tienen preferencia sobre las impresiones durante la atribución de conversión. Cualquier clic en una ruta de conversión recibe crédito total según la regla de atribución. Las impresiones solo reciben crédito cuando no se rastrean clics en la ruta de conversión.

   * *[!UICONTROL Last Event]:* Atributos conversiones al último clic o impresión en la ruta de conversión.

   * *[!UICONTROL Weight Last More]:* Atribuye conversiones a todos los eventos de la ruta de conversión, pero da la mayor importancia al último evento y, sucesivamente, menos importancia a los eventos anteriores.

   * *[!UICONTROL Even Distribution]:* Atribuye las conversiones de forma equitativa a cada evento de la ruta de conversión.

   * *[!UICONTROL Weight First More]:* Atribuye conversiones a todos los eventos de la ruta de conversión, pero da la mayor importancia al primer evento y, sucesivamente, menos importancia a los siguientes.

   * *[!UICONTROL First Event]:* Atributos para las conversiones al primer clic o impresión en la ruta de conversión.

   * *[!UICONTROL U-shaped]:*: atribuye la conversión a todos los eventos de la ruta de conversión, pero da la mayor importancia a los eventos primero y último, con sucesivamente menos peso a los eventos en medio de la ruta de conversión.

   * *[!UICONTROL Display Only]:* Atributos convertidos en el último clic o impresión de DSP en la ruta de conversión. Esto incluye vídeo y anuncios de TV conectados, y excluye los clics en [!DNL Advertising Search, Social, & Commerce] anuncios.

   * *[!UICONTROL Social Only]:* obsoleto

Consulte también &quot;[Cómo se calculan las reglas de atribución para Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md)&quot;.

**[!UICONTROL Paths as Columns]:** Qué tipos de conversiones notificar cuando se produjeron eventos anteriores en el mismo dispositivo. Se pueden incluir hasta tres tipos. Para cada tipo seleccionado, se incluye una columna independiente para cada métrica de conversión y se anexa el sufijo especificado ([!UICONTROL (tl)], [!UICONTROL (ct)] o [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Incluye conversiones atribuidas a clics (CT para pulsaciones) y a impresiones (VT para visualizaciones). Las conversiones atribuidas a impresiones se multiplican por el peso de visualización especificado. La ponderación de visualización predeterminada es del 100 %, lo que significa que las conversiones atribuidas a impresiones se cuentan como el 100 % del valor de las conversiones atribuidas a los clics.

* *[!UICONTROL With Clicks (CT)]:* Incluye solo las conversiones atribuidas a los clics.

* *[!UICONTROL Impressions Only (VT)]:* Incluye solo las conversiones que se atribuyeron a impresiones porque no se rastreó ningún clic en la ruta de conversión.

### Sección [!UICONTROL Add Report Destinations]

**[!UICONTROL Destination Type]:** Dónde entregar los informes completados y las notificaciones de error. Una vez guardado el informe, no se puede cambiar el tipo de destino.

>[!NOTE]
>
>Siempre puede descargar los informes completados desde la vista [!UICONTROL Reports] > [!UICONTROL Custom Reports].

* *[!UICONTROL None]:* Para no entregar ningún informe o notificación.

* *[!UICONTROL S3]:* Para enviar el informe completado a una o más [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) ubicaciones, que debe seleccionar en el campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL sFTP]:* Para enviar el informe completado a una o más ubicaciones SFTP, que debe seleccionar en el campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP]:* Para enviar el informe completado a una o varias ubicaciones de FTP, que debe seleccionar en el campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP SSL] (actualmente en Beta):* Para enviar el informe completado a una o más ubicaciones SSL de FTP, que debe seleccionar en el campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL Email]:* Para especificar las direcciones de correo electrónico a las que se enviarán los informes o notificaciones completados si el informe se cancela debido a errores.

**[!UICONTROL Email]:** (solo tipo de destino de correo electrónico) Para cada dirección, ingrese la dirección y haga clic en **+**.

**[!UICONTROL Destination Name]:** (solo tipos de destino SSL de S3, FTP, sFTP y FTP) Los nombres de los [destinos de informes](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} a los que se envía el informe personalizado.

* Para especificar un destino existente, seleccione un nombre de destino de la lista. Puede seleccionar varios nombres de destino por separado.

* Para crear un nuevo destino:

   1. Haga clic en **Agregar nuevo destino**.

   1. Escriba la [configuración de destino del informe](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} y haga clic en **Guardar**.

   1. En la configuración del informe, haga clic en **Actualizar nombres de destino.**

      El nuevo destino ya está disponible en la lista de destinos existentes y, opcionalmente, puede agregarlo al informe.


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [Informes de rendimiento de nivel de experiencia](/help/creative/experiences/experience-performance-details.md)
>* [Acerca de los informes personalizados de DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [Acerca de [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
