---
title: Configuración de informe personalizada
description: Consulte las descripciones de la configuración de informes personalizada.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '1541'
ht-degree: 0%

---

# Configuración de informe personalizada

**[!UICONTROL Name]:** El nombre del informe. La longitud máxima es de 180 caracteres.

**[!UICONTROL Report Type]:** Tipo de informe: *[!UICONTROL Custom]* (que incluye la mayoría de las opciones disponibles), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, *[!UICONTROL Household Conversions]*, *[!UICONTROL Path to Conversions Beta]*, *[!UICONTROL Path Length Beta]* o *[!UICONTROL Time to Conversion Beta]*.

## Sección [!UICONTROL Report Range]

Esta sección determina los datos que se incluyen en el informe. Para configurar las fechas de la programación del informe, consulte la sección &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** Zona horaria para los informes.

**[!UICONTROL Observe Daylight Savings Time]:** considera el horario de verano en los horarios informados.

**Intervalo:** Intervalo de fecha para el que se van a generar datos. El número de días disponibles varía según el informe y las dimensiones seleccionadas. Elija uno:

* **[!UICONTROL Previous Calendar Week]:** Incluye datos de la semana anterior.

* **[!UICONTROL Previous Calendar Month]:** Incluye datos del mes calendario anterior.

* **[!UICONTROL Custom Range]:** Incluye datos entre fechas de inicio y finalización específicas. Para informar desde el día anterior, seleccione **[!UICONTROL Present]**.

## Sección [!UICONTROL Report Run schedule]

Esta sección determina las fechas en las que se ejecuta el informe. Para configurar las fechas en las que se incluirán los datos del informe, consulte la sección &quot;[!UICONTROL Report range]&quot;.

**\[Programación\]:** Cuándo generar el informe:

* *[!UICONTROL Immediately]*: agrega inmediatamente el informe a la cola de informes.

  >[!NOTE]
  >
  >También puede [ejecutar un informe personalizado en cualquier momento](report-run-now.md) desde la vista [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\>:* Ejecuta el informe en una fecha especificada para su finalización antes de las 09:00 en el huso horario de la cuenta.

* *[!UICONTROL Recurring]:* Ejecuta el informe de acuerdo con una programación durante un período de tiempo especificado.

   * **\[Programación\]:** La frecuencia con la que se ejecutará el informe:

      * *Diario* para ejecutar el informe cada N días. Por ejemplo, para ejecutar el informe cada dos semanas (14 días), seleccione esta opción y escriba **14**.

      * *Semanalmente* para ejecutar el informe en los días de la semana especificados. Por ejemplo, para ejecutar el informe todos los lunes y viernes, selecciona esta opción y las casillas de verificación que aparecen junto a **Lunes** y **Viernes**.

      * *Mensual* para ejecutar el informe en un día numérico específico del mes, del 1 al 30. Por ejemplo, para ejecutar el informe el primer día de cada mes, seleccione esta opción y escriba **1**.

   * **Desde**: Primera fecha en que se puede ejecutar el informe. Según la programación especificada, la primera instancia de informe puede producirse después de esta fecha.

   * **Hasta**: La fecha de caducidad del informe, que puede ser dentro de cuatro meses calendario. Antes de que caduque un informe, todos los destinos de correo electrónico especificados reciben una alerta de correo electrónico siete días y un día antes de la fecha de caducidad. Para mantener el informe más tiempo, cambie esta fecha.

## Sección [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (Opcional) Dimensiones adicionales mediante las cuales filtrar los datos, independientemente de si las dimensiones se incluyen o no como columnas en el informe. Los filtros disponibles varían según el tipo de informe y pueden incluir: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* y *[!UICONTROL Video Duration]*.

Para aplicar uno o más filtros, haga lo siguiente:

* Seleccione una dimensión, seleccione el operador (*es igual a* o *no es igual a*) y, a continuación, seleccione el valor aplicable. Por ejemplo, para devolver datos solo para anuncios de preroll, especifique &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Opcional) Añada criterios adicionales al filtro.
* (Opcional) Añada filtros adicionales, cada uno con uno o más criterios.

\* *[!UICONTROL Account]* solo está disponible para los siguientes tipos de informes cuando su organización está configurada para [informes entre cuentas](report-about.md#cross-account-reporting): [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] y [!UICONTROL Conversion]. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información sobre la creación de informes entre cuentas.

**[!UICONTROL Include data from Adobe Advertising SSC]:** (solo informes de Ruta de acceso a la conversión, Longitud de ruta de acceso y Tiempo de conversión) Incluye datos de clics en anuncios de búsqueda de campañas especificadas de Advertising Search, Social y Commerce. Al seleccionar esta opción:

1. Seleccione la cuenta de Search, Social y Commerce con el filtro **Filtrar por[!UICONTROL SSC Account]**.

1. Seleccione las campañas que usan el filtro **Filtrar por[!UICONTROL SSC Campaign]**.

   Para seleccionar varias campañas, haga clic en **[!UICONTROL Add Criteria]** para la segunda campaña y las subsiguientes.

## Sección [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** Las columnas de datos, o encabezados, que se incluirán en el informe. Para agregar una columna, expanda la categoría y active la casilla de verificación situada junto al nombre de la columna. Las columnas disponibles varían según el informe y todas las métricas no disponibles están desactivadas. Las categorías de datos disponibles pueden incluir:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Los informes [!UICONTROL Household Reach & Frequency] y [!UICONTROL Path to Conversion] solo pueden incluir una dimensión.
  > Los informes [!UICONTROL Path Length] y [!UICONTROL Time to Conversion] no incluyen dimensiones.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >El informe [!UICONTROL Household Reach & Frequency] puede incluir métricas superpuestas o no superpuestas, pero no ambas.

* [!UICONTROL Conversion Metrics] (ordenado por anunciante)

* [!UICONTROL Custom Goals] (ordenado por anunciante)

Consulte &quot;[Columnas de informe disponibles](report-columns.md)&quot; para obtener descripciones de todas las opciones.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** El orden de los encabezados de columna. Puede arrastrar y soltar cualquier columna para personalizar el orden.

**[!UICONTROL Format]:** Indica si se generará un informe en formato *[!UICONTROL CSV]* (valores separados por comas) o *[!UICONTROL Tab]* (valores separados por tabulaciones).

**[!UICONTROL Headers]:** Ya sea para *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* encabezados de columna.

## Sección [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** La configuración varía según el tipo de informe:

* **\[Tipo de atribución\]:** ([!UICONTROL Household Conversion] informes con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] columnas; anunciantes con solo seguimiento de conversión de Adobe Advertising) Dentro del informe, cómo atribuir datos de conversión en una serie de eventos que llevan a una conversión:

   * *[!UICONTROL Unique]:* (El valor predeterminado) Cuenta el número de veces que un valor de dimensión (como un dispositivo o una ubicación) estaba en la ruta de conversión.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Distribuye el crédito de cada conversión en función de la frecuencia con que se produjo el valor de dimensión (como un dispositivo o una ubicación) en la ruta de acceso a la conversión. Por ejemplo, si había un total de 10 impresiones antes de la conversión, con 8 en CTV y 2 en Mobile, entonces el 80% del crédito (0,8) se da a las pantallas CTV y 0,2 a Mobile.

* **\[Tipo de regla\]:** (Todos los informes [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] y [!UICONTROL Site] con columnas [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals]; anunciantes con seguimiento de conversión de Adobe Advertising solamente) Dentro del informe, cómo atribuir datos de conversión en una serie de eventos que llevan a una conversión. Puede elegir más de una regla si desea comparar las diferencias entre las reglas.

  >[!NOTE]
  >
  >Las rutas de conversión incluyen cualquier impresión y clic dentro de las ventanas retrospectivas de impresiones o clics del anunciante, que están configuradas en [!DNL Advertising Search, Social, & Commerce]. Los clics tienen preferencia sobre las impresiones durante la atribución de conversión. Cualquier clic en una ruta de conversión recibe crédito total según la regla de atribución. Las impresiones solo reciben crédito cuando no se rastrean clics en la ruta de conversión.

   * *[!UICONTROL Last Event]:* Atributos conversiones al último clic o impresión en la ruta de conversión.

   * *[!UICONTROL Weight Last More]:* Atribuye conversiones a todos los eventos de la ruta de conversión, pero da la mayor importancia al último evento y, sucesivamente, menos importancia a los eventos anteriores.

   * *[!UICONTROL Even Distribution]:* Atribuye las conversiones de forma equitativa a cada evento de la ruta de conversión.

   * *[!UICONTROL Weight First More]:* Atribuye conversiones a todos los eventos de la ruta de conversión, pero da la mayor importancia al primer evento y, sucesivamente, menos importancia a los siguientes.

   * *[!UICONTROL First Event]:* Atributos para las conversiones al primer clic o impresión en la ruta de conversión.

   * *[!UICONTROL U-shaped]:*: atribuye la conversión a todos los eventos de la ruta de conversión, pero da la mayor importancia a los eventos primero y último, con sucesivamente menos peso a los eventos en medio de la ruta de conversión.

   * DSP *[!UICONTROL Display Only]:* Atributos para convertir al último clic o impresión de la ruta de conversión en la que se hizo clic o se produjo la última impresión de la. Esto incluye vídeo y anuncios de TV conectados, y excluye los clics en [!DNL Advertising Search, Social, & Commerce] anuncios.

   * *[!UICONTROL Social Only]:* obsoleto

Consulte también &quot;[Cómo se calculan las reglas de atribución para el Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md)&quot;.

* **Retrospectiva:** ([!UICONTROL Household Conversion] informes con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] columnas, y [!UICONTROL Path to Conversion], [!UICONTROL Path Length] o [!UICONTROL Time to Conversion] informes con [!UICONTROL Conversion Metrics] columnas solamente; anunciantes con seguimiento de conversión de Adobe Advertising solamente) Dentro del informe, el número máximo de días después de un evento de impresión o un evento de clic (para [!UICONTROL Path to Conversion], [!UICONTROL Path Length] o [!UICONTROL Time to Conversion] informes) en los que se puede atribuir un evento de conversión a él. El valor predeterminado es *[!UICONTROL 30 days]* y el máximo es 92 días.

  >[!TIP]
  >
  >Si usa [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), utilice la misma ventana retrospectiva que utilizó en [!DNL Analytics].

**[!UICONTROL Paths as Columns]:** (Todos los informes de [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] y [!UICONTROL Site] con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] columnas) Qué tipos de conversiones notificar cuando se produjeron eventos anteriores en el mismo dispositivo. Se pueden incluir hasta tres tipos. Para cada tipo seleccionado, se incluye una columna independiente para cada métrica de conversión y se anexa el sufijo especificado ([!UICONTROL (tl)], [!UICONTROL (ct)] o [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Incluye conversiones atribuidas a clics (CT para pulsaciones) y a impresiones (VT para visualizaciones). Las conversiones atribuidas a impresiones se multiplican por el peso de visualización especificado. La ponderación de visualización predeterminada es del 100 %, lo que significa que las conversiones atribuidas a impresiones se cuentan como el 100 % del valor de las conversiones atribuidas a los clics.

* *[!UICONTROL With Clicks (CT)]:* Incluye solo las conversiones atribuidas a los clics.

* *[!UICONTROL Impressions Only (VT)]:* Incluye solo las conversiones que se atribuyeron a impresiones porque no se rastreó ningún clic en la ruta de conversión.

**[!UICONTROL Conversion Reporting Based On]:** Cómo informar sobre los datos de conversión:

* *[!UICONTROL Conversion Timestamp]:* (valor predeterminado) Las conversiones están asociadas con la fecha de conversión.

* *[!UICONTROL Event Timestamp]:* Las conversiones se informan en función de la fecha de la impresión o del clic que provocó la conversión, según lo determinado por el [!UICONTROL Attribution Rule Settings] especificado.

## Sección [!UICONTROL Add Report Destinations]

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

**[!UICONTROL Destination Name]:** (solo tipos de destino SSL de S3, FTP, sFTP y FTP) Los nombres de los destinos de informe a los que se envía el informe personalizado.

* Para especificar un destino existente, seleccione un nombre de destino de la lista. Puede seleccionar varios nombres de destino por separado.

* Para crear un nuevo destino:

   1. Haga clic en **Agregar nuevo destino**.

   1. Escriba la [configuración de destino del informe](/help/dsp/reports/report-destinations/report-destination-settings.md) y haga clic en **Guardar**.

   1. En la configuración del informe, haga clic en **Actualizar nombres de destino.**

      El nuevo destino ya está disponible en la lista de destinos existentes y, opcionalmente, puede agregarlo al informe.

>[!MORELIKETHIS]
>
>* [Acerca de los informes personalizados](/help/dsp/reports/report-about.md)
>* [Crear un informe personalizado](/help/dsp/reports/report-create.md)
>* [Duplicar un informe personalizado](/help/dsp/reports/report-copy.md)
>* [Editar un informe personalizado](/help/dsp/reports/report-edit.md)
>* [Descargar un informe personalizado](/help/dsp/reports/report-download.md)
>* [Ejecutar un informe personalizado](/help/dsp/reports/report-run-now.md)
>* [Configuración de informe personalizada](/help/dsp/reports/report-settings.md)
>* [Acerca de los destinos del informe](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)
