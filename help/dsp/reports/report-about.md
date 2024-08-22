---
title: Acerca de los informes personalizados
description: Obtenga información acerca de las opciones para crear informes personalizados manualmente o mediante plantillas de informe preconfiguradas.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 44f7f9b31afbe6b863acd389df641057b1e6dea1
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# Acerca de los informes personalizados

Los informes personalizados le permiten personalizar el contenido y el envío de los datos del informe utilizando las dimensiones de la campaña (como el anunciante, la ubicación, los sitios o los geos) y las métricas que más le importan. Puede hacer lo siguiente:

* Configure completamente los informes de rendimiento de campaña a nivel granular.

* Elija entre las plantillas de informe preconfiguradas y, si lo desea, personalícelas más.

Puede generar informes una vez o programarlos para que se generen diariamente, semanalmente o mensualmente a las 03:00 en el huso horario especificado según criterios específicos (por ejemplo, cada 15 días o el 1 de cada mes). Una vez generado el informe, puede descargarlo de [!UICONTROL Reports] > [!UICONTROL Custom Reports] o de [destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md) vinculados de los siguientes tipos:

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

   * **[!UICONTROL Conversion]:** Use este informe para comprender el rendimiento de sus campañas en función de las métricas de conversión capturadas mediante el seguimiento de conversión de Adobe Advertising. Este informe incluye la atribución de múltiples contactos.

   * **[!UICONTROL Device]:** Utilice esta plantilla rellenada previamente para ver las métricas clave según las dimensiones relacionadas con el dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Use este informe para comprender la distribución de impresiones mostradas a espectadores únicos (por ejemplo, cuántos espectadores únicos vieron una impresión, dos impresiones, tres impresiones, etc.). Los datos están disponibles por ubicación o campaña.

     >[!NOTE]
     >
     >* Los datos estarán disponibles a partir del 1 de marzo de 2019.
     >* La frecuencia se calcula a partir de una muestra de datos.
     >* En algunos inventarios, los editores no transmiten un identificador de dispositivo, lo que impide el seguimiento de la frecuencia. Este informe incluye solo las impresiones para las que había un identificador de dispositivo disponible.

   * **[!UICONTROL Frequency (by App/Site)]:** Use este informe para comprender cuántos usuarios únicos se contactaron por aplicación o por sitio. También puede ver cuántos usuarios únicos se alcanzaron a través de una sola aplicación o sitio en particular (&quot;usuarios únicos distintos&quot;).

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

   * **[!UICONTROL Household Reach & Frequency]:** Use este informe para ver las impresiones, el alcance y la frecuencia de una sola dimensión en los formatos de anuncio a nivel doméstico en función de la dirección IP, en lugar de a nivel de dispositivo/cookie. Utilice las perspectivas para optimizar la combinación de medios, mejorar el rendimiento e identificar oportunidades de alcance incremental. Consulte &quot;[Preguntas frecuentes acerca de los informes de hogares](/help/dsp/reports/faq-household-report.md)&quot; para obtener más información. No hay datos disponibles para ubicaciones destinadas a ID universales.

   * **[!UICONTROL Household Conversions]:** Use este informe para ver las conversiones de visualización a nivel doméstico en función de la dirección IP, en lugar de a nivel de dispositivo/cookie. Utilice las perspectivas para medir y optimizar el rendimiento de la campaña. Consulte &quot;[Preguntas frecuentes acerca de los informes de hogares](/help/dsp/reports/faq-household-report.md)&quot; para obtener más información. No hay datos disponibles para ubicaciones destinadas a ID universales.

## Informes entre cuentas {#cross-account-reporting}

DSP Cualquier organización con varias cuentas de puede, opcionalmente, habilitar los datos entre cuentas en informes personalizados según las necesidades de la organización. Por ejemplo, puede dar acceso a la cuenta A a los datos de la cuenta B y dar acceso a la cuenta B a los datos de la cuenta C (pero no de la cuenta A). Para habilitar y configurar esta función, póngase en contacto con el equipo de cuenta de Adobe.

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
>* [Preguntas más frecuentes sobre los informes de hogares](/help/dsp/reports/faq-household-report.md)
>* [Tipos de informes de rendimiento en las vistas de Campaign Management](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)
>* [Acerca de [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
