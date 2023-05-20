---
title: Acerca de los informes personalizados
description: Obtenga información acerca de las opciones para crear informes personalizados manualmente o mediante plantillas de informe preconfiguradas.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 858b00ec28158ada1edfc70a2efc3540fa46a376
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Acerca de los informes personalizados

Los informes personalizados le permiten personalizar el contenido y el envío de los datos del informe utilizando las dimensiones de la campaña (como el anunciante, la ubicación, los sitios o los geos) y las métricas que más le importan. Puede hacer lo siguiente:

* Configure completamente los informes de rendimiento de campaña a nivel granular.
* Elija entre las plantillas de informe preconfiguradas y, si lo desea, personalícelas más.

Puede generar informes una vez o programarlos para que se generen diariamente, semanalmente o mensualmente a las 03:00 en el huso horario especificado. Una vez generado el informe, se envía a cada destinatario de correo electrónico especificado o a los destinatarios vinculados [destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md) de los siguientes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* SSL de FTP (en versión beta)

>[!NOTE]
>
>También puede ver datos bajo demanda en todos los niveles de una campaña (campaña, paquete, ubicación o anuncio) [dentro de la vista de administración de campañas correspondiente](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipos de informes disponibles

* **[!UICONTROL Custom]:** Este informe es una plantilla en blanco que puede utilizar para crear su propio informe personalizado con la mayoría de las dimensiones y métricas. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], y [!UICONTROL Site] los informes son variaciones de esta plantilla con columnas y dimensiones preseleccionadas para sus respectivos casos de uso.

* Plantillas de informe preconfiguradas

   * **[!UICONTROL Billing]:** Utilice este informe para comprender las métricas de facturación clave como las métricas de gasto para la facturación de medios por campaña.

      >[!NOTE]
      >
      >Este informe incluye datos sobre el segmento de facturación. Si a un usuario o dispositivo se le sirve una impresión que pertenece a varios segmentos, solo se acredita un segmento facturable con la impresión.

   * **[!UICONTROL Conversion]:** Utilice este informe para comprender el rendimiento de sus campañas en función de las métricas de conversión capturadas mediante el seguimiento de conversión de la publicidad de Adobe. Este informe incluye la atribución de múltiples contactos.

   * **[!UICONTROL Device]:** Utilice esta plantilla previamente rellenada para ver las métricas clave por dimensiones relacionadas con el dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Utilice este informe para comprender la distribución de impresiones que se muestran a espectadores únicos (por ejemplo, cuántos espectadores únicos vieron una impresión, dos impresiones, tres impresiones, etc.). Los datos están disponibles por ubicación o campaña.

      >[!NOTE]
      >
      >* Los datos estarán disponibles a partir del 1 de marzo de 2019.
      >* La frecuencia se calcula a partir de una muestra de datos.
      >* En algunos inventarios, los editores no transmiten un identificador de dispositivo, lo que impide el seguimiento de la frecuencia. Este informe incluye solo las impresiones para las que había un identificador de dispositivo disponible.


   * **[!UICONTROL Frequency (by App/Site)]:** Utilice este informe para comprender cuántos usuarios únicos se contactaron por aplicación o por sitio. También puede ver cuántos usuarios únicos se alcanzaron a través de una sola aplicación o sitio en particular (&quot;usuarios únicos distintos&quot;).

      >[!NOTE]
      >
      >* Los datos estarán disponibles a partir del 15 de noviembre de 2018.
      >* En algunos inventarios privados, los editores no transmiten un identificador de dispositivo, lo que impide el seguimiento de la frecuencia.


   * **[!UICONTROL Geo]**: utilice esta plantilla previamente rellenada para ver las métricas clave por dimensiones geográficas.

   * **[!UICONTROL Margin]:** Utilice este informe para ver métricas clave como el margen, los beneficios y otras métricas de gasto por campaña o ubicación.

   * **[!UICONTROL Segment]:** Utilice esta plantilla previamente rellenada para ver las métricas clave por segmento.

      >[!NOTE]
      >
      >* El objetivo de este informe es mostrar el rendimiento de los distintos segmentos segmentados. Utiliza datos de abono de segmentos. Cuando se sirve una impresión a una persona o dispositivo que pertenece a dos o más segmentos de destino, este informe incluye una fila para cada segmento. Por este motivo, es posible que los totales de este informe no coincidan con la entrega real.
      >* Las métricas de conversión y los datos de objetivo personalizados para segmentos están disponibles a partir del 2 de agosto de 2019. El resto de los datos de los segmentos estarán disponibles a partir del 1 de junio de 2018.


   * **[!UICONTROL Site]:** De forma predeterminada, incluye las métricas estándar, el gasto neto total en medios y el gasto neto total facturable por sitio.

   * **[!UICONTROL Household]:** Utilice este informe para ver las impresiones, el alcance y la frecuencia de una sola dimensión en todos los formatos de publicidad a nivel doméstico en función de la dirección IP, en lugar de a nivel de dispositivo/cookie. Utilice las perspectivas para optimizar la combinación de medios, mejorar el rendimiento e identificar oportunidades de alcance incremental. Consulte &quot;[Preguntas frecuentes sobre informes de hogares](/help/dsp/reports/faq-household-report.md)&quot; para obtener más información.

## Informes entre cuentas {#cross-account-reporting}

DSP Cualquier organización con varias cuentas de puede, opcionalmente, habilitar los datos entre cuentas en informes personalizados según las necesidades de la organización. Por ejemplo, puede dar acceso a la cuenta A a los datos de la cuenta B y dar acceso a la cuenta B a los datos de la cuenta C (pero no de la cuenta A). Para habilitar y configurar esta función, póngase en contacto con el equipo de cuenta de Adobe.

Una vez habilitada la función para su organización, puede [filter](report-settings.md) cualquiera de los siguientes tipos de informes por cuenta:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], y [!UICONTROL Conversion].

La configuración de su cuenta en [!UICONTROL Settings] > [!UICONTROL Account] indique a) las otras cuentas cuyos datos estén disponibles para su cuenta y b) las otras cuentas que puedan acceder a los datos de su cuenta.

>[!MORELIKETHIS]
>
>* [Creación de un informe personalizado](/help/dsp/reports/report-create.md)
>* [Configuración de informe personalizada](/help/dsp/reports/report-settings.md)
>* [Preguntas frecuentes sobre [!UICONTROL Household] Informe](/help/dsp/reports/faq-household-report.md)
>* [Acerca de los informes en la plataforma](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)
>* [Acerca de [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)

