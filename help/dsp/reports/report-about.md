---
title: Acerca de los informes personalizados
description: Obtenga información acerca de las opciones para crear informes personalizados manualmente o mediante plantillas de informe preconfiguradas.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: ae75e6110443d8b744f141df370160e02e4d725e
workflow-type: tm+mt
source-wordcount: '1578'
ht-degree: 0%

---

# Acerca de los informes personalizados

Los informes personalizados le permiten personalizar el contenido y el envío de los datos del informe utilizando las dimensiones de la campaña (como el anunciante, la ubicación, los sitios o los geos) y las métricas que más le importan. Puede hacer lo siguiente:

* Configure completamente los informes de rendimiento de campaña a nivel granular.

* Elija entre las plantillas de informe preconfiguradas y, si lo desea, personalícelas más.

Puede generar informes una vez o programarlos diariamente, semanalmente o mensualmente a las 03:00 en el huso horario especificado según criterios específicos (como cada 15 días o el 1 de cada mes). Una vez generado el informe, puede descargarlo de [!UICONTROL Reports] > [!UICONTROL Custom Reports] o de [destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md) vinculados de los siguientes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SSL de FTP <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>También puede ver datos bajo demanda en todos los niveles de una campaña (campaña, paquete, ubicación o anuncio) [dentro de la vista de administración de campañas correspondiente](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipos de informes disponibles

* **[!UICONTROL Custom]:** Este informe es una plantilla en blanco que puede usar para crear su propio informe personalizado con la mayoría de las dimensiones y métricas. Los informes [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo] y [!UICONTROL Site] son variaciones de esta plantilla con columnas y dimensiones preseleccionadas para sus respectivos casos de uso.

* Plantillas de informe preconfiguradas

   * **[!UICONTROL Billing]:** Use este informe para comprender las métricas de facturación clave, como las métricas de gasto para la facturación de medios por campaña. No hay datos disponibles para ubicaciones destinadas a ID universales.

     >[!NOTE]
     >
     >Este informe incluye datos sobre el segmento de facturación. Si a un usuario o dispositivo se le sirve una impresión que pertenece a varios segmentos, solo se acredita un segmento facturable con la impresión.

   * **[!UICONTROL Conversion]:** Use este informe para comprender el rendimiento de sus campañas en función de las métricas de conversión capturadas mediante el seguimiento de conversiones de Adobe Advertising. Este informe incluye la atribución de múltiples contactos.

   * **[!UICONTROL Custom Creative Report]:** (Anunciantes con Advertising Creative; función beta) Use este informe para supervisar el rendimiento en las experiencias publicitarias de Advertising Creative.

   * **[!UICONTROL Device]:** Utilice esta plantilla rellenada previamente para ver las métricas clave según las dimensiones relacionadas con el dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Use este informe para comprender la distribución de impresiones mostradas a espectadores únicos (por ejemplo, cuántos espectadores únicos vieron una impresión, dos impresiones, tres impresiones, etc.). Los datos están disponibles por ubicación o campaña.

     >[!NOTE]
     >
     >* Los datos estarán disponibles a partir del 1 de marzo de 2019.
     >* La frecuencia se calcula a partir de una muestra de datos.
     >* En algunos inventarios, los editores no transmiten un identificador de dispositivo, lo que impide el seguimiento de la frecuencia. Este informe incluye solo las impresiones para las que había un identificador de dispositivo disponible.

   * **[!UICONTROL Frequency (by App/Site)]:** Use este informe para comprender a cuántos usuarios únicos llegaron sus anuncios por aplicación o por sitio. También puede ver a cuántos usuarios únicos llegaron sus anuncios a través de una aplicación o sitio en particular (&quot;usuarios únicos distintos&quot;).

     >[!NOTE]
     >
     >* Los datos estarán disponibles a partir del 15 de noviembre de 2018.
     >* En algunos inventarios privados, los editores no transmiten un identificador de dispositivo, lo que impide el seguimiento de la frecuencia.

   * **[!UICONTROL Geo]**: utilice esta plantilla previamente completada para ver métricas clave por dimensiones geográficas.

   * **[!UICONTROL Margin]:** Use este informe para ver métricas clave como margen, ganancias y otras métricas de gasto por campaña o ubicación. No hay datos disponibles para ubicaciones destinadas a ID universales.

   * **[!UICONTROL Segment]:** Utilice esta plantilla rellenada previamente para ver las métricas clave por segmento.

     >[!NOTE]
     >
     >* El objetivo de este informe es mostrar el rendimiento de los distintos segmentos segmentados. Utiliza datos de abono de segmentos. Cuando se sirve una impresión a una persona o dispositivo que pertenece a dos o más segmentos de destino, este informe incluye una fila para cada segmento. Por este motivo, es posible que los totales de este informe no coincidan con la entrega real.
     >* Las métricas de conversión y los datos de objetivo personalizados para segmentos están disponibles a partir del 2 de agosto de 2019. El resto de los datos de los segmentos estarán disponibles a partir del 1 de junio de 2018.

   * **[!UICONTROL Site]:** De forma predeterminada, incluye las métricas estándar, el gasto neto total de medios y el gasto neto total facturable por sitio.

   * **[!UICONTROL Household Reach & Frequency]:** Use este informe para ver las impresiones, el alcance y la frecuencia de una sola dimensión en los formatos de anuncio a nivel doméstico en función de la dirección IP, en lugar de a nivel de dispositivo/cookie. Utilice las perspectivas para optimizar la combinación de medios, mejorar el rendimiento e identificar oportunidades de alcance incremental. Consulte &quot;[Preguntas frecuentes acerca de los informes de hogares](/help/dsp/reports/faq-reports.md)&quot; para obtener más información. No hay datos disponibles para ubicaciones destinadas a ID universales.

   * **[!UICONTROL Household Conversions]:** Use este informe para ver las conversiones de visualización a nivel doméstico en función de la dirección IP, en lugar de a nivel de dispositivo/cookie. Utilice las perspectivas para medir y optimizar el rendimiento de la campaña. Consulte &quot;[Preguntas frecuentes acerca de los informes de hogares](/help/dsp/reports/faq-reports.md)&quot; para obtener más información. No hay datos disponibles para ubicaciones destinadas a ID universales.

   * **[!UICONTROL Path to Conversion]:** Use este informe para identificar cómo optimizar presupuestos y personalizar anuncios en función de secuencias de interacción de anuncios de alto rendimiento. El informe muestra la secuencia de puntos de interacción en el mismo hogar que llevan a cada una de las métricas de conversión seleccionadas en el rango de datos especificado. El informe utiliza un periodo retrospectivo especificado entre la primera interacción y una conversión y puede incluir una dimensión:

      * [!UICONTROL Channel Assist Type]: muestra cómo los siguientes canales de marketing han ayudado en el proceso de conversión: [!UICONTROL Audio Impression], [!UICONTROL CTV Impression], [!UICONTROL Display Click], [!UICONTROL Display Impression], [!UICONTROL Native Click], [!UICONTROL Native Impression], [!UICONTROL Search Click], [!UICONTROL Video Click] o [!UICONTROL Video Impression].

      * [!UICONTROL Campaign ID] o [!UICONTROL Campaign Name]: muestra qué campañas han ayudado en el proceso de conversión.

      * [!UICONTROL Ad ID] o [!UICONTROL Ad Name] muestra qué anuncios de DSP han resultado en conversiones.

      * [!UICONTROL Ad ID & Paid Keyword (SSC)] o [!UICONTROL Ad Name & Paid Keyword (SSC)] muestra qué palabras clave de Search, Social y Commerce han resultado en conversiones.

     Las columnas del informe incluyen &quot;[!UICONTROL Event #1]&quot; hasta &quot;[!UICONTROL Event #10],&quot;[!UICONTROL Path Length],&quot; &quot;% \&lt;Nombre de métrica de conversión 1\>,&quot; &quot;% \&lt;Nombre de métrica de conversión 2\>,&quot; etc.

     Se incluyen hasta los 10 puntos de interacción más recientes. Las filas de ruta están ordenadas por el número de conversiones.

     Para ver una comparación de este informe con los informes creados por [!DNL Advanced Measurement Services] y Adobe Analytics, consulte &quot;[Preguntas más frecuentes acerca de informes personalizados](/help/dsp/reports/faq-reports.md)&quot;.

   * **[!UICONTROL Path Length]:** Use este informe para hacer un seguimiento de la cantidad de puntos de interacción del usuario necesarios para las conversiones a lo largo del tiempo, de modo que pueda elegir la frecuencia de anuncio óptima. El informe muestra el número de conversiones por longitud de ruta (puntos de interacción); por ejemplo, cuántas conversiones se produjeron después de que los usuarios solo tuvieran una interacción de publicidad, dos interacciones de publicidad, etc. El informe puede incluir datos de varias métricas de conversión y utiliza un periodo retrospectivo especificado entre la primera interacción y una conversión. Las columnas del informe incluyen &quot;[!UICONTROL Path Length]&quot;, &quot;[!UICONTROL Number of] \&lt;Nombre de métrica de conversión 1\>&quot;, &quot;% \&lt;Nombre de métrica de conversión 1\>&quot;, \&lt;Nombre de métrica de conversión 2\>&quot;, &quot;% \&lt;Nombre de métrica de conversión 2\>&quot;, etc.

     Se muestran datos para cada longitud de ruta de hasta 10; los datos para las longitudes de ruta superiores a 10 se agrupan.

   * **[!UICONTROL Time to Conversion]:** Use este informe para determinar la ventana retrospectiva de atribución óptima y para identificar las campañas con tiempos de conversión más largos, que pueden beneficiarse de la retargeting. El informe muestra el número de conversiones por el periodo en días desde la última interacción (exposición del anuncio o clic) hasta la conversión. El informe puede incluir datos de varias métricas de conversión y utiliza un periodo retrospectivo especificado entre la primera interacción y una conversión. Las columnas del informe incluyen &quot;[!UICONTROL Time Taken (in days)]&quot;, &quot;[!UICONTROL Number of] \&lt;Nombre de métrica de conversión 1\>&quot;, &quot;% \&lt;Nombre de métrica de conversión 1\>&quot;, \&lt;Nombre de métrica de conversión 2\>&quot;, &quot;% \&lt;Nombre de métrica de conversión 2\>&quot;, etc. Las conversiones que tardan más tiempo que el período retroactivo se agrupan en una fila (por ejemplo, si el informe utiliza un período retroactivo de 30 días, todas las conversiones que tardan más de 30 días en producirse se agrupan en una fila con un valor &quot;[!UICONTROL Time Taken (in days)]&quot; de &quot;30+&quot;).

   * **[!UICONTROL Content]:** Use este informe para comprender la entrega de impresiones y otras métricas según dimensiones de contenido especificadas (como género, calidad de producción y clasificación de contenido), de modo que pueda optimizar el direccionamiento y garantizar la seguridad de la marca. Además de las dimensiones de contenido, el informe incluye la mayoría de las dimensiones, métricas y filtros estándar. Los datos por dimensión de contenido están disponibles para [!DNL Freewheel], [!DNL Index], [!DNL Magnite], [!DNL Microsoft], [!DNL Nexxen], [!DNL Pubmatic], [!DNL Sharethrough] y [!DNL Triplelift]. Los editores pasan las señales de contenido durante el flujo de ofertas y están sujetas a disponibilidad.

## Informes entre cuentas {#cross-account-reporting}

Cualquier organización con varias cuentas de DSP puede, opcionalmente, habilitar los datos entre cuentas en informes personalizados según las necesidades de la organización. Por ejemplo, puede dar acceso a la cuenta A a los datos de la cuenta B y dar acceso a la cuenta B a los datos de la cuenta C (pero no de la cuenta A). Para habilitar y configurar esta función, póngase en contacto con el equipo de cuenta de Adobe.

Una vez habilitada la característica para su organización, puede [filtrar](report-settings.md) cualquiera de los siguientes tipos de informes por cuenta: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] y [!UICONTROL Conversion].

La configuración de su cuenta en [!UICONTROL Settings] > [!UICONTROL Account] indica a) las otras cuentas cuyos datos están disponibles para su cuenta y b) las demás cuentas que pueden acceder a los datos de su cuenta.

## La vista [!UICONTROL Custom Reports]

[!UICONTROL Reports] > [!UICONTROL Custom Reports] enumera los informes existentes, incluidos los que se generaron, los que se programaron para una generación futura y los que no se pudieron generar. La columna &quot;[!UICONTROL Report Run]&quot; muestra las fechas en las que se activó el informe a partir del 22 de agosto de 2024. De forma predeterminada, se muestran todos los informes no archivados creados por el usuario, con los más recientes en la parte superior. Puede filtrar aún más la lista por estado, ya sea que el informe sea recurrente o único, el tipo de informe, el tipo de destino y el creador del informe.

Puede crear nuevos informes personalizados, editar los informes existentes o duplicarlos para crear nuevos informes, ejecutar informes inmediatamente, descargar cualquier instancia de informe de los últimos cuatro meses y eliminar informes.

## Estados de informes {#custom-report-status}

* **[!UICONTROL Yet to start]:** El informe nunca se ha ejecutado.

* **[!UICONTROL Report generating]:** El informe se está creando en este momento.

* **[!UICONTROL Ready to download]:** (solo informes recurrentes) Una o más instancias del informe están disponibles para descargar y se han programado más instancias de informe.

* **[!UICONTROL Failed]:** Error en el trabajo de informe. Para ver por qué las instancias de informe individuales fallaron en un grupo de informes, haga clic en ![la flecha abajo](/help/dsp/assets/chevron-down.png "la flecha abajo") junto a [!UICONTROL Download]. Los trabajos de informe con errores se indican con un icono de error (![indicador de error](/help/dsp/assets/indicator-critical.png "indicador de error")). Mantenga el cursor sobre el icono de error para ver una descripción del error.

* **[!UICONTROL Completed]:** Para informes no recurrentes, el informe se ha completado. En los informes recurrentes, todas las instancias de informe se finalizan. Puede descargar todos los informes completados en los últimos cuatro meses.

* **[!UICONTROL Archived]:** El informe está archivado y no se puede ejecutar. Este estado se establece cuando la generación de informes falla varias veces en un informe. Actualmente, no puede establecer este estado desde la interfaz de usuario.

>[!MORELIKETHIS]
>
>* [Crear un informe personalizado](/help/dsp/reports/report-create.md)
>* [Descargar un informe personalizado](/help/dsp/reports/report-download.md)
>* [Configuración de informe personalizada](/help/dsp/reports/report-settings.md)
>* [Preguntas más frecuentes sobre los informes de hogares](/help/dsp/reports/faq-reports.md)
>* [Tipos de informes de rendimiento en las vistas de administración de campañas](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)
>* [Acerca de [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
