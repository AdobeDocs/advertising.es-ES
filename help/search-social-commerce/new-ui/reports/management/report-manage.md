---
title: Administrar informes programados
description: Obtenga información sobre cómo administrar los informes programados.
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# Administrar informes programados

Los informes de rendimiento le permiten realizar un seguimiento y administrar el rendimiento de sus portafolios, redes de publicidad y entidades de cuenta de red de publicidad con el nivel de granularidad que desee. La mayoría de los informes proporcionan una visibilidad completa sobre cómo los anuncios de cada canal de marketing contribuyen a la tasa de conversión general.

Los datos de un informe se compilan dinámicamente cada vez que se ejecuta el informe. Si lo desea, puede generar un informe nuevo a partir de uno existente. Los parámetros de informe disponibles varían según el tipo de informe. Para la mayoría de los informes, tiene la opción de previsualizar las primeras 50 líneas en lugar de generar todo el informe. Cuando genere un informe, puede enviar una notificación con vínculos de descarga a una o varias direcciones de correo electrónico cuando se complete el informe y los destinatarios pueden [administrar las notificaciones en [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Todos los informes completados están disponibles en la sección [!UICONTROL Latest Reports] de la vista [!UICONTROL Reports] y puede verlos en formato de tabla en la ventana del explorador o abrirlos o descargarlos como archivos.

## Categorías de informe disponibles

Las siguientes categorías de informes están disponibles en la vista [!UICONTROL Reports]. Es posible que no tenga acceso a todos ellos; los informes disponibles y los datos que generan están determinados por su función y por la forma en que se configura su cuenta de cliente.

| Categoría del informe | Descripción |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Los informes básicos](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md), que están disponibles para todos los usuarios, muestran los datos reales de costos y clics para portafolios, cuentas de red de anuncios, cuentas de red de anuncios específicas, campañas, grupos de anuncios, anuncios, palabras clave, grupos de productos, clasificaciones de etiquetas y valores de etiquetas, restricciones de unidades de oferta y restricciones de red. Se basan en clics facturados por las redes de publicidad aplicables y, opcionalmente, pueden incluir datos de conversión o cualquier otra métrica que cree. |
| [!UICONTROL Advanced Reports] | [Informes avanzados](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) proporcionan insight adicional en tu configuración de publicidad, lo que te ayuda a identificar dónde te beneficiarías al cambiar la segmentación geográfica o la configuración de red. También pueden ayudarle a validar los datos de conversión de las vistas e informes de administración de campañas y portafolios con los datos de seguimiento de conversión internos del anunciante. |
| [!UICONTROL Assist Reports] | [Informes de asistencia](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) proporcionan información sobre las rutas de conversión para todas las palabras clave y anuncios del anunciante. Utilizan datos capturados mediante el servicio de seguimiento de conversión de Adobe Advertising y solo se pueden generar para anunciantes con el servicio. |
| [!UICONTROL Specialty Reports] | [Informes especiales](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) constan de datos recopilados por las redes de anuncios (en lugar de por el seguimiento de Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Los informes de precisión del modelo](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) indican la precisión de los modelos de costo e ingresos que se usan para optimizar ofertas, presupuestos de campaña y objetivos de estrategia de oferta para un portafolio. |

## Automatización de informes

Programe informes personalizados para que se generen automáticamente de una o ambas de las siguientes maneras:

* Genere informes automáticamente cada día o un día específico de la semana o del mes, usando [plantillas de informes](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Si lo desea, puede configurar el envío por FTP de [informes básicos y avanzados](/help/search-social-commerce/new-ui/reports/ftp-reports.md) que utilizan una plantilla.

* Siga actualizando las plantillas de hoja de cálculo personalizadas con datos de rendimiento diarios mediante [fuentes de hoja de cálculo](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## Las vistas [!UICONTROL Scheduled Reports]

Las vistas [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] le permiten crear y administrar informes y plantillas de informes:

* La ficha **[!UICONTROL Latest Reports]** enumera todos los informes disponibles para usted<!-- Doesn't seem to be true: that were requested in the last seven days -->, excepto los que se eliminaron manualmente, con el informe más reciente en la parte superior de forma predeterminada. La información mostrada para cada informe incluye la programación según la cual se ejecuta (cuando corresponde), las fechas de inicio y finalización para las que se generaron o se generarán datos, quién creó el informe y el estado del informe (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* o *[!UICONTROL Error]*).

  Los vínculos junto a cada informe permiten abrir o guardar el informe como un libro de [!DNL Microsoft Excel] (XLS), un archivo de valores separados por tabulaciones (TSV) o un archivo de valores separados por comas (CSV). Algunos tipos de informes también se pueden guardar como [!UICONTROL Excel] libros con una hoja de cálculo independiente para cada campaña aplicable.

  Desde esta pestaña, también puede crear un nuevo informe (que, opcionalmente, puede utilizarse como plantilla), crear un nuevo informe basado en la configuración de un informe existente o utilizar una plantilla de informe, cancelar los informes en curso disponibles eliminándolos y eliminar cualquier informe completado disponible.

* La ficha **[!UICONTROL Templates]** enumera todas las plantillas de informe básicas y avanzadas guardadas que tiene a su disposición, incluida la información acerca de las programaciones asociadas a ellas. La plantilla más reciente se encuentra en la parte superior de forma predeterminada.

  Desde esta pestaña, puede crear una nueva plantilla, editar cualquier plantilla que haya creado (incluida la adición, modificación o eliminación de su programación), generar un informe a partir de una plantilla y eliminar cualquier plantilla disponible.

## Uso de los informes

| Finalidad | Informe |
| ---- | ---- |
| Monitorización del rendimiento | <ul><li>[El [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[El [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[El [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[El [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[El [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[El [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Solución de problemas de rendimiento y análisis de tendencias | <ul><li>[El [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[El [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[El [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[El [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[El [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) y [El [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Cualquier informe básico que compare dos períodos de tiempo con la función &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identificación de oportunidades de crecimiento empresarial | <ul><li>(Anunciantes con solo seguimiento de conversión de Adobe Advertising) [El [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Anunciantes con solo seguimiento de conversión de Adobe Advertising) [El [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Anunciantes con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=es)) Informes personalizados en Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Anunciantes con solo seguimiento de conversión de Adobe Advertising) [El [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Anunciantes con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=es)) Informes personalizados en Adobe Analytics Analysis Workspace</li></ul> |

## Generación de informes

### Generación de un nuevo informe

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Haga clic en **[!UICONTROL Create Report]**, haga clic en la categoría del informe en el panel izquierdo y, a continuación, seleccione el tipo de informe.<!-- Add link to list of report categories and report types --> Haga clic en **[!UICONTROL Proceed]**.

1. (Opcional) En la ventana [!UICONTROL Create Report], cambie la configuración predeterminada de los informes de [informes básicos y avanzados](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [informes de asistencia](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [informes de precisión del modelo](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) y [informes especiales](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md):

   1. (Opcional) Introduzca un nombre personalizado para el informe y para la plantilla (si guarda el informe como plantilla).

   1. (Opcional) Para guardar la configuración del informe como una plantilla, habilite la configuración **[!UICONTROL Save as template]**.

   1. (Opcional) Seleccione un informe diferente **[!UICONTROL Type]** dentro de la misma categoría de informe.

   1. (Opcional) En la ficha **[!UICONTROL Basic Settings]**, seleccione una plantilla de informe existente para usar o cambiar la configuración básica predeterminada del informe.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Columns]** y cambie las columnas predeterminadas del informe, incluido el orden de las columnas.

      De forma predeterminada, todos los datos monetarios de los informes se muestran en formato de dólares estadounidenses (por ejemplo, 1000,00). Para mostrar el valor en el formato de moneda correcto (pero sin símbolos de moneda en los formatos CSV y TSV), agregue la columna &quot;[!UICONTROL Currency]&quot; al informe. Si el informe incluye datos de cuentas con distintas monedas, cualquier valor monetario &quot;[!UICONTROL Total]&quot; será la suma de todos los números de la columna, independientemente de la moneda.

   1. (Algunos tipos de informes, opcional) Haga clic en la ficha **[!UICONTROL Filters & Attribution]** o **[!UICONTROL Filters]** y agregue filtros de datos (algunos tipos de informes). Limite los resultados del informe para incluir únicamente clasificaciones de etiquetas específicas y cambie la regla de atribución y la configuración de atribución de conversión predeterminadas.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Scheduling]** y cambie las opciones predeterminadas de programación y envío.

1. Haga clic en **[!UICONTROL Create]**.

Si no ha especificado una programación de informes, el informe se ejecuta inmediatamente; de lo contrario, se ejecuta según la programación especificada. El nombre del informe se agrega a la vista [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Si guardó el informe como plantilla, entonces también se agregará a la vista [[!UICONTROL Templates]](/help/search-social-commerce/reports/report-about.md). Cuando se completa el informe, el archivo está disponible para abrirlo o guardarlo; las plantillas están disponibles inmediatamente.

Si ha introducido direcciones de correo electrónico para la notificación, cada destinatario recibe una notificación cuando se completa o falla el trabajo del informe, según la [configuración de notificaciones](/help/search-social-commerce/notifications/notification-edit.md) del usuario para los informes.

### Generación de un informe a partir de un informe existente

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, que se abre en la ficha **[!UICONTROL Latest Reports]**.

1. Realice una de las acciones siguientes:

   * Mantenga el cursor sobre la fila del informe y haga clic en **...** > **[!UICONTROL Duplicate]**.

   * Seleccione la casilla de verificación situada junto al informe. En la barra de herramientas de acciones masivas, haga clic en [Duplicar](/help/search-social-commerce/assets/duplicate.png "Duplicar").

1. Edite la configuración del informe si es necesario.

1. Haga clic en **[!UICONTROL Create]**.

### Generación de un informe a partir de una plantilla existente

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Realice una de las acciones siguientes:

   * Mantenga el cursor sobre la fila de la plantilla y haga clic en **...** > **[!UICONTROL Duplicate]**.

   * Seleccione la casilla de verificación situada junto a la plantilla existente. En la barra de herramientas de acciones masivas, haga clic en [Duplicar](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**.

1. (Opcional) Cambie el nombre de la plantilla y edite la configuración del informe si es necesario.

   Haga clic en **[!UICONTROL Next]** para desplazarse entre las secciones de configuración.

1. Habilite la configuración **[!UICONTROL Save as Template]**.

1. Haga clic en **[!UICONTROL Create]**.

## Previsualización o guardado de un informe

Puede obtener una vista previa de un informe en el explorador web o abrir o guardar los datos del informe como un libro de [!DNL Microsoft Excel], un archivo de valores separados por tabulaciones (TSV), un archivo de valores separados por comas (CSV) o (algunos tipos de informes) un libro con pestañas [!DNL Microsoft Excel].

>[!NOTE]
>
>Los miembros del equipo de cuenta de Adobe y algunos usuarios administradores pueden ver los informes creados por los usuarios del anunciante y de la agencia.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, que se abre en la ficha **[!UICONTROL Latest Reports]**.

1. Realice una de las acciones siguientes:

   * (Para ver un informe en el explorador web) Realice una de las acciones siguientes:

      * Mantenga el cursor sobre la fila de la plantilla y haga clic en **...** > **[!UICONTROL Preview]**.

      * Seleccione la casilla de verificación situada junto a la plantilla existente. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Preview]**.

   * (Para abrir o guardar los datos del informe en un archivo) En la columna [!UICONTROL Export] junto al nombre del informe, haga clic en el nombre de un formato y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador:

      * **[!UICONTROL XLS]:** Para un libro de [!DNL Excel] con una sola hoja de cálculo (formato XLSX). El informe incluye una hoja de cálculo etiquetada en la parte superior con los parámetros, con una fila para cada componente cuando los datos del componente están disponibles. Se omiten las filas sin datos.

        Los informes básicos incluyen un total para cada columna numérica.

      * **[!UICONTROL TSV]:** Para un archivo TSV. El informe incluye los parámetros y una fila para cada componente incluido en el informe.

      * **[!UICONTROL CSV]:** Para un archivo CSV. El informe incluye los parámetros y una fila para cada componente incluido en el informe.

## Eliminar informes

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, que se abre en la ficha **[!UICONTROL Latest Reports]**.

1. Realice una de las acciones siguientes:

   * (Para eliminar un solo informe):

      1. Mantenga el cursor sobre la fila del informe y haga clic en **...** > **[!UICONTROL Run]**.

      1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

   * (Para eliminar uno o varios informes):

      1. Active la casilla de verificación situada junto a cada informe que desee eliminar.

      1. En la barra de herramientas de acciones masivas, haga clic en [Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar") **[!UICONTROL Delete]**.

      1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
