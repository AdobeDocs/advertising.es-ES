---
title: '[!UICONTROL Custom Creative Report]'
description: Obtenga información sobre cómo generar la experiencia cruzada [!UICONTROL Custom Creative Report].
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: 03d3f3c43bfe58f2dcab998e1d95f1e512f54b20
workflow-type: tm+mt
source-wordcount: '2019'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*característica de Beta*

[!UICONTROL Custom Creative Report] le permite personalizar el contenido y el envío de los datos del informe para todas sus experiencias publicitarias.

Puede generar informes una vez o programarlos diariamente, semanalmente o mensualmente a las 03:00 en el huso horario especificado según criterios específicos (como cada 15 días o el 1 de cada mes). Una vez generado el informe, puede descargarlo de [!UICONTROL Reports] > [!UICONTROL Custom Reports] o de [destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md) vinculados de los siguientes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SSL de FTP <!-- (in beta) -->
* SFTP

## Crear un(a) [!UICONTROL Custom Creative Report]

1. En el menú principal, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]**.

1. Especifique la [configuración del informe](#report-settings).

1. Haga clic en **[!UICONTROL Create Custom Report]**.

## Configuración de informes {#report-settings}

**[!UICONTROL Name]:** El nombre del informe. La longitud máxima es de 180 caracteres.

**[!UICONTROL Report Type]:** El tipo de informe: *[!UICONTROL Custom Creative Beta]*.

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
  >También puede [ejecutar un informe personalizado en cualquier momento](/help/dsp/reports/report-run-now.md) desde la vista [!UICONTROL Reports].

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

**[!UICONTROL Select To Add As Report Headers]:** Las columnas de datos, o encabezados, que se incluirán en el informe. Para agregar una columna, expanda la categoría y active la casilla de verificación situada junto al nombre de la columna. Las columnas disponibles varían según el informe y todas las métricas no disponibles están desactivadas. Consulte &quot;[Columnas de informe disponibles](#report-custom-creative-columns)&quot; para obtener descripciones de todas las opciones.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** El orden de los encabezados de columna. Puede arrastrar y soltar cualquier columna para personalizar el orden.

**[!UICONTROL Format]:** Indica si se generará un informe en formato *[!UICONTROL CSV]* (valores separados por comas) o *[!UICONTROL Tab]* (valores separados por tabulaciones).

**[!UICONTROL Headers]:** Ya sea para *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* encabezados de columna.

### Sección [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** La configuración varía según el tipo de informe:

* **\[Tipo de atribución\]:** (Anunciantes con seguimiento de conversión de Adobe Advertising solamente) En el informe, cómo atribuir datos de conversión en una serie de eventos que llevan a una conversión:

   * *[!UICONTROL Unique]:* (El valor predeterminado) Cuenta el número de veces que un valor de dimensión (como un dispositivo o una ubicación) estaba en la ruta de conversión.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Distribuye el crédito de cada conversión en función de la frecuencia con que se produjo el valor de dimensión (como un dispositivo o una ubicación) en la ruta de acceso a la conversión. Por ejemplo, si había un total de 10 impresiones antes de la conversión, con 8 en CTV y 2 en Mobile, entonces el 80% del crédito (0,8) se da a las pantallas CTV y 0,2 a Mobile.

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

* *[!UICONTROL FTP SSL](actualmente en Beta):* Para enviar el informe completado a una o más ubicaciones SSL de FTP, que debe seleccionar en el campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL Email]:* Para especificar las direcciones de correo electrónico a las que se enviarán los informes o notificaciones completados si el informe se cancela debido a errores.

**[!UICONTROL Email]:** (solo tipo de destino de correo electrónico) Para cada dirección, ingrese la dirección y haga clic en **+**.

**[!UICONTROL Destination Name]:** (solo tipos de destino SSL de S3, FTP, sFTP y FTP) Los nombres de los [destinos de informes](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} a los que se envía el informe personalizado.

* Para especificar un destino existente, seleccione un nombre de destino de la lista. Puede seleccionar varios nombres de destino por separado.

* Para crear un nuevo destino:

   1. Haga clic en **Agregar nuevo destino**.

   1. Escriba la [configuración de destino del informe](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} y haga clic en **Guardar**.

   1. En la configuración del informe, haga clic en **Actualizar nombres de destino.**

      El nuevo destino ya está disponible en la lista de destinos existentes y, opcionalmente, puede agregarlo al informe.

## Columnas de informe disponibles {#report-custom-creative-columns}

| Tipo de métrica | Subtipo | Nombre de columna | Descripción |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | Las dimensiones del anuncio publicado. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | Si el anuncio publicado era un anuncio de imagen o un anuncio de vídeo predeterminado para la experiencia. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | Si los anuncios se giraron según pesos relativos (*Ponderados*) o algorítmicamente (*Algoritmos*). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | El identificador que [!UICONTROL Creative] asignó al creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | El nombre del creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | El tipo de elemento creativo (como [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | Identificador que [!UICONTROL Creative] asignó al creativo principal. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | El nombre del creativo principal. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | El tipo de elemento creativo principal (como [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | La dirección URL de la página de aterrizaje. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | El tipo específico de interacción del usuario. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | El flujo direccional o la ruta de navegación de la interacción de clic del usuario dentro de la experiencia creativa. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | Explorador en el que se mostró el anuncio (como [!UICONTROL Chrome] o [!UICONTROL Firefox]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | El sistema operativo en el que se mostró el anuncio (como [!UICONTROL Windows]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | El tipo de dispositivo en el que se mostró el anuncio (como [!UICONTROL Desktop]). |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | Nombre del DSP en el que se ejecutaron los anuncios. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | El ID de la ubicación para la que se ejecutaron los anuncios. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | El nombre de la ubicación para la que se ejecutaron los anuncios. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | El ID del sitio en el que se ejecutaron los anuncios. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | El nombre del sitio en el que se ejecutaron los anuncios. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | Identificador que [!UICONTROL Creative] asignó a la etiqueta de experiencia de anuncio. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | El nombre del anunciante. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | La fecha y la hora del evento. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | Identificador que [!UICONTROL Creative] asignó a la experiencia. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | El nombre de la experiencia. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | La ruta específica a través del árbol de decisión de direccionamiento que determinó qué variante de experiencia creativa se proporcionó al usuario. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | Nombre de la etiqueta de publicidad. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | Ciudad a la que se atribuyen los datos notificados. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | El código del país al que se atribuyen los datos notificados. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | El área de mercado designada (DMA) a la que se atribuyen los datos notificados. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | El código de estado del estado al que se atribuyen los datos del informe. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | El código postal al que se atribuyen los datos notificados. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | (Anuncios dinámicos) El ID de categoría de producto de destino. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | (Anuncios dinámicos) El nombre de la categoría de producto de destino. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | (Anuncios dinámicos) El primer atributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | (Anuncios dinámicos) El segundo atributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | (Anuncios dinámicos) El tercer atributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | (Anuncios dinámicos) El cuarto atributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | (Anuncios dinámicos) El quinto atributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | (Anuncios dinámicos) El ID del producto de destino. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | (Anuncios dinámicos) El nombre del producto de destino. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | ID de hasta cinco segmentos de usuario que coincidían con el tema del anuncio. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | El ID de un píxel de resegmentación al que se atribuyen los datos del informe. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | Nombre de un píxel de resegmentación al que se atribuyen los datos del informe. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | Atributos de un segmento de audiencia al que se atribuyen los datos del informe. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | La suma de todos los clics en un anuncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | La tasa de clics, que es el porcentaje de clics dividido por las impresiones de publicidad. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | El porcentaje de impresiones servidas que dieron como resultado la participación del usuario. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | El número de interacciones en un anuncio publicado. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | Número total de impresiones de publicidad. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | El porcentaje de impresiones con una cookie de redireccionamiento. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | (Solo anuncios dinámicos) La suma de todos los clics en los anuncios de un producto. Cuando el producto es nulo, este valor es cero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | (Solo anuncios dinámicos) La suma de todas las conversiones en anuncios de un producto. Cuando el producto es nulo, este valor es cero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | (Solo anuncios dinámicos) El porcentaje de anuncios de un producto que generaron conversiones. Cuando el producto es nulo, este valor es cero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | (Solo anuncios dinámicos) Tasa de clics para anuncios de un producto, que es el porcentaje de clics dividido por impresiones de publicidad. Cuando el producto es nulo, este valor es cero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | (Solo anuncios dinámicos) El número total de impresiones de un producto. Cuando el producto es nulo, este valor es cero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | (Solo anuncios dinámicos) Ingresos totales en anuncios publicados de un producto. Cuando el producto es nulo, este valor es cero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | Ingresos totales de los anuncios publicados. |
| [!UICONTROL Conversion Metrics] | [Agrupado por anunciante en la configuración del informe] | [Conversión específica del anunciante] | El total de una métrica de conversión o un evento de Adobe Analytics específico del anunciante. |
| [!UICONTROL Custom Goals] | [Agrupado por anunciante en la configuración del informe] | [Objetivo personalizado específico del anunciante] | (Anunciantes con Advertising DSP) La suma ponderada de todas las conversiones incluidas en el [objetivo personalizado de Advertising DSP](/help/dsp/optimization/custom-goal.md) especificado. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Informes de rendimiento de nivel de experiencia](/help/creative/experiences/experience-performance-details.md)
>* [Acerca de los informes personalizados de DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [Acerca de [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
