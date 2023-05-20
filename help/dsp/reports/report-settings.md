---
title: Configuración de informe personalizada
description: Consulte las descripciones de la configuración de informes personalizada.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 2e0240ff1b342d5a0564e01ebec3ee313b488b59
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# Configuración de informe personalizada

**[!UICONTROL Name]** Nombre del informe. La longitud máxima es de 180 caracteres.

**[!UICONTROL Report Type]** El tipo de informe: *[!UICONTROL Custom]* (que incluye la mayoría de las opciones disponibles), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]*, o *[!UICONTROL Household]*.

## [!UICONTROL Apply Filters] Sección

**[!UICONTROL Timezone]:** Zona horaria de los informes.

**[!UICONTROL Observe Daylight Savings Time]:** Considera el horario de verano en los tiempos informados.

**\[Intervalo de fecha\]:** Intervalo de fecha para el que se van a generar datos. El número de días disponibles varía según el informe y las dimensiones seleccionadas. Elija uno:

* **[!UICONTROL Previous N days]:** Incluye datos de un número determinado de días antes de hoy.

* **[!UICONTROL Custom]:** Incluye datos entre fechas de inicio y finalización específicas. Para informar sobre los datos hasta el día anterior, seleccione **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Incluye datos del mes natural anterior.

**[!UICONTROL Add Filters]:** (Opcional) Dimensiones adicionales mediante las cuales filtrar los datos, independientemente de si las dimensiones se incluyen o no como columnas en el informe. Los filtros disponibles varían según el tipo de informe y pueden incluir los siguientes: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]*, y *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* solo está disponible para los siguientes tipos de informes cuando su organización está configurada para [creación de informes entre cuentas](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], y [!UICONTROL Conversion]. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información sobre la creación de informes entre cuentas.

Para aplicar uno o más filtros, haga lo siguiente:

* Seleccione una dimensión, seleccione el operador (*igual a* o *no igual a*) y, a continuación, seleccione el valor aplicable. Por ejemplo, para devolver datos solo de anuncios preroll, especifique &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Opcional) Añada criterios adicionales al filtro.
* (Opcional) Añada filtros adicionales, cada uno con uno o más criterios.

## [!UICONTROL Build Your Report] Sección

**[!UICONTROL Select To Add As Report Headers]:**  Las columnas de datos, o encabezados, que se incluirán en el informe. Para agregar una columna, expanda la categoría y active la casilla de verificación situada junto al nombre de la columna. Las columnas disponibles varían según el informe y todas las métricas no disponibles están desactivadas. Las categorías de datos disponibles incluyen:

* [!UICONTROL Dimensions]

   >[!NOTE]
   >
   > El [!UICONTROL Household] El informe solo puede incluir una dimensión.

* [!UICONTROL Metrics]

   >[!NOTE]
   >
   >El [!UICONTROL Household] El informe puede incluir métricas de superposición o métricas que no sean de superposición, pero no ambas.

* [!UICONTROL Conversion Metrics] (ordenado por anunciante)

* [!UICONTROL Custom Goals] (ordenado por anunciante)

Consulte &quot;[Columnas de informe disponibles](report-columns.md)&quot; para obtener descripciones de todas las opciones.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Orden de los encabezados de columna. Puede arrastrar y soltar cualquier columna para personalizar el orden.

## [!UICONTROL Multi-Touch Conversion Options] Sección

**[!UICONTROL Format]:** Si se genera un informe en *[!UICONTROL CSV]* (valores separados por comas) o *[!UICONTROL Tab]* formato (valores separados por tabulaciones).

**[!UICONTROL Report Headers]:** Si se desea *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* encabezados de columna.

**[!UICONTROL Attribution Rule Settings]:** (Todos) [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], y [!UICONTROL Site] informes con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] columnas; anunciantes con seguimiento de conversión de publicidad de Adobe únicamente) En el informe, se explica cómo atribuir datos de conversión en una serie de eventos que generan una conversión. Puede elegir más de una regla si desea comparar las diferencias entre las reglas.

>[!NOTE]
>
>Las rutas de conversión incluyen cualquier impresión y clic dentro de las ventanas retrospectivas de impresiones o clics del anunciante, que se configuran en [!DNL Advertising Search, Social, & Commerce]. Los clics tienen preferencia sobre las impresiones durante la atribución de conversión. Cualquier clic en una ruta de conversión recibe crédito total según la regla de atribución. Las impresiones solo reciben crédito cuando no se rastrean clics en la ruta de conversión.

* *[!UICONTROL Last Event]:* Atribuye las conversiones al último clic o impresión de la ruta de conversión.

* *[!UICONTROL Weight Last More]:* Atribuye las conversiones a todos los eventos de la ruta de conversión, pero da el mayor peso al último evento y sucesivamente menos peso a los eventos anteriores.

* *[!UICONTROL Even Distribution]:* Atribuye las conversiones de forma equitativa a cada evento de la ruta de conversión.

* *[!UICONTROL Weight First More]:* Atribuye las conversiones a todos los eventos de la ruta de conversión, pero da el mayor peso al primer evento y sucesivamente menos peso a los siguientes eventos.

* *[!UICONTROL First Event]:* Atribuye las conversiones al primer clic o impresión de la ruta de conversión.

* *[!UICONTROL U-shaped]:* Atribuye la conversión a todos los eventos de la ruta de conversión, pero da el mayor peso a los eventos primero y último, sucesivamente con menos peso a los eventos en medio de la ruta de conversión.

* *[!UICONTROL Display Only]:*  DSP Atribuye las conversiones al último clic o impresión de la en la ruta de conversión. Esto incluye vídeo y anuncios de TV conectados y excluye clics en [!DNL Advertising Search, Social, & Commerce] anuncios.

* *[!UICONTROL Social Only]:* Obsoleto

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]:**  (Todos) [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], y [!UICONTROL Site] informes con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] columnas) Qué tipos de conversiones se notificarán cuando se produjeron eventos anteriores en el mismo dispositivo. Se pueden incluir hasta tres tipos. Para cada tipo seleccionado, se incluye una columna independiente para cada métrica de conversión y se anexa el sufijo especificado ([!UICONTROL (tl)], [!UICONTROL (ct)], o [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Incluye las conversiones atribuidas a los clics (CT para pulsaciones) y a las impresiones (VT para visualizaciones). Las conversiones atribuidas a impresiones se multiplican por el peso de visualización especificado. La ponderación de visualización predeterminada es del 100 %, lo que significa que las conversiones atribuidas a impresiones se cuentan como el 100 % del valor de las conversiones atribuidas a los clics.

* *[!UICONTROL With Clicks (CT)]:* Incluye solo las conversiones atribuidas a los clics.

* *[!UICONTROL Impressions Only (VT)]:* Incluye solo las conversiones que se atribuyeron a impresiones porque no se rastreó ningún clic en la ruta de conversión.

**[!UICONTROL Conversion Reporting Based On]:**  Cómo informar sobre los datos de conversión:

* *[!UICONTROL Conversion Timestamp]:* (Valor predeterminado) Las conversiones se asociarán con la fecha de conversión.

* *[!UICONTROL Event Timestamp]:* Las conversiones se registrarán en función de la fecha de la impresión o del clic que provocó la conversión, según lo determinado por el especificado [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Sección

**[!UICONTROL Destination Type]:** Elija uno de los siguientes tipos de destino:

* *[!UICONTROL S3]:* Para enviar el informe completado a uno o varios [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) ubicaciones, que especificará en la variable **[!UICONTROL Destination Name]** field.
* *[!UICONTROL sFTP]:* Para enviar el informe completado a una o varias ubicaciones SFTP, especifique en la variable **[!UICONTROL Destination Name]** field.
* *[!UICONTROL FTP]:* Para enviar el informe completado a una o varias ubicaciones de FTP, especifique en la variable **[!UICONTROL Destination Name]** field.
* *[!UICONTROL FTP SSL](Actualmente en versión beta):* Para enviar el informe completado a una o varias ubicaciones SSL de FTP, especifique en la variable **[!UICONTROL Destination Name]** field.
* *[!UICONTROL Email]:* Para especificar las direcciones de correo electrónico a las que se enviarán los informes o las notificaciones completados si el informe se cancela debido a errores. Para especificar varias direcciones, sepárelas con comas o espacios.

>[!NOTE]
>
> Una vez guardado el informe, no se puede cambiar el tipo de destino.

**[!UICONTROL Destination Name]:** (Solo tipos de destino S3, FTP, sFTP y FTP SSL) Los nombres de los destinos de informes a los que se enviará el informe personalizado.

* Para especificar un destino existente, seleccione un nombre de destino de la lista. Puede seleccionar varios nombres de destino por separado.

* Para crear un nuevo destino:

   1. Clic **Añadir nuevo destino**.

   1. Introduzca el [configuración de destino del informe](/help/dsp/reports/report-destinations/report-destination-settings.md)y haga clic en **Guardar**.

   1. Vuelva a la configuración del informe y haga clic en **Actualizar nombres de destino.**

      El nuevo destino ya está disponible en la lista de destinos existentes y, opcionalmente, puede agregarlo al informe.

**[!UICONTROL Frequency]:** (Para cada [!UICONTROL Destination Name] La frecuencia con la que se envía el informe al destino: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, o *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Sección

**[!UICONTROL Send & Save]:** Cuándo enviar el informe: *[!UICONTROL On Schedule]* o *[!UICONTROL Run Now]*. Los informes programados se entregarán a las 09:00 en el huso horario de la cuenta.

>[!NOTE]
>
>Puede [ejecutar un informe personalizado en cualquier momento](report-run-now.md) desde el [!UICONTROL Reports] vista.

>[!MORELIKETHIS]
>
>* [Acerca de los informes personalizados](/help/dsp/reports/report-about.md)
>* [Creación de un informe personalizado](/help/dsp/reports/report-create.md)
>* [Duplicación de un informe personalizado](/help/dsp/reports/report-copy.md)
>* [Edición de un informe personalizado](/help/dsp/reports/report-edit.md)
>* [Ejecutar un informe personalizado](/help/dsp/reports/report-run-now.md)
>* [Configuración de informe personalizada](/help/dsp/reports/report-settings.md)
>* [Acerca de los destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)

