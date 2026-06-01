---
title: (Nueva IU) Acerca de los informes programados
description: Obtenga información acerca de los informes de rendimiento programados, incluidos los diferentes tipos de informes disponibles y cómo automatizar los informes.
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
  - id: c916feea-e212-4773-b673-4daed287b8a3
  - id: adcb1be7-7ed0-464d-a8d4-c905c9d47742
  - id: ff99aaef-142d-4c93-a88c-011e979e3843
  - id: fa0141e5-dc99-4fbd-9c0e-40aff66de606
  - id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664
source-git-commit: bd4246ec79684167254a153d2f3d0b917a493096
workflow-type: tm+mt
source-wordcount: 857
ht-degree: 0%

---

# (Nueva IU) Acerca de los informes programados

Los informes de rendimiento programados permiten realizar un seguimiento y administrar el rendimiento de los portafolios, las redes de anuncios y las entidades de cuenta de red de anuncios con el nivel de granularidad que desee. La mayoría de los informes proporcionan una visibilidad completa sobre cómo los anuncios de cada canal de marketing contribuyen a la tasa de conversión general.

Los datos de un informe se compilan dinámicamente cada vez que se ejecuta el informe. Si lo desea, puede generar un informe nuevo a partir de uno existente. Los parámetros de informe disponibles varían según el tipo de informe. Para la mayoría de los informes, tiene la opción de previsualizar las primeras 50 líneas en lugar de generar todo el informe. Cuando genere un informe, puede enviar una notificación con vínculos de descarga a una o varias direcciones de correo electrónico cuando se complete el informe y los destinatarios pueden [administrar las notificaciones en [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md).

Todos los informes completados están disponibles en la sección [!UICONTROL Latest Reports] de la vista [!UICONTROL Reports] y puede verlos en formato de tabla en la ventana del explorador o abrirlos o descargarlos como archivos.

## Categorías de informe disponibles

Las siguientes categorías de informes están disponibles en la vista [!UICONTROL Scheduled Reports]. Es posible que no tenga acceso a todos ellos; los informes disponibles y los datos que generan están determinados por su función y por la forma en que se configura su cuenta de cliente.

| Categoría del informe | Descripción |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Los informes básicos](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md), que están disponibles para todos los usuarios, muestran los datos reales de costos y clics para portafolios, cuentas de red de anuncios, cuentas de red de anuncios específicas, campañas, grupos de anuncios, anuncios, palabras clave, grupos de productos, clasificaciones de etiquetas y valores de etiquetas, restricciones de unidades de oferta y restricciones de red. Se basan en clics facturados por las redes de publicidad aplicables y, opcionalmente, pueden incluir datos de conversión o cualquier otra métrica que cree. |
| [!UICONTROL Advanced Reports] | [Informes avanzados](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) proporcionan insight adicional en tu configuración de publicidad, lo que te ayuda a identificar dónde te beneficiarías al cambiar la segmentación geográfica o la configuración de red. También pueden ayudarle a validar los datos de conversión de las vistas e informes de administración de campañas y portafolios con los datos de seguimiento de conversión internos del anunciante. |
| [!UICONTROL Assist Reports] | [Informes de asistencia](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) proporcionan información sobre las rutas de conversión para todas las palabras clave y anuncios del anunciante. Utilizan datos capturados mediante el servicio de seguimiento de conversión de Adobe Advertising y solo se pueden generar para anunciantes con el servicio. |
| [!UICONTROL Specialty Reports] | [Informes especiales](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) constan de datos recopilados por las redes de anuncios (en lugar de por el seguimiento de Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Los informes de precisión del modelo](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) indican la precisión de los modelos de costo e ingresos que se usan para optimizar ofertas, presupuestos de campaña y objetivos de estrategia de oferta para un portafolio. |

## Automatización de informes

Programe informes personalizados para que se generen automáticamente de una o ambas de las siguientes maneras:

* Genere informes automáticamente cada día o un día específico de la semana o del mes, usando [plantillas de informes](/help/search-social-commerce/new-ui/reports/report-templates-manage.md).

  Si lo desea, puede configurar el envío por FTP de [informes básicos y avanzados](/help/search-social-commerce/new-ui/reports/ftp-reports.md) que utilizan una plantilla.

* Siga actualizando las plantillas de hoja de cálculo personalizadas con datos de rendimiento diarios mediante [fuentes de hoja de cálculo](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## La vista [!UICONTROL Scheduled Reports]

La vista [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] le permite crear y administrar informes, plantillas y fuentes de hojas de cálculo. La vista incluye dos pestañas:

* La ficha **[!UICONTROL Latest Reports]** enumera todos los informes disponibles para usted que se solicitaron en los últimos siete días, excepto los que se eliminaron manualmente, con el informe más reciente en la parte superior de forma predeterminada. La información mostrada para cada informe incluye la programación según la cual se ejecuta (cuando corresponde), las fechas de inicio y finalización para las cuales se generaron o se generarán datos, y el estado del informe (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* o *[!UICONTROL Error]*).

  Los vínculos junto a cada informe permiten ver el informe en el explorador web o abrirlo o guardarlo como un archivo de [!DNL Microsoft Excel] libro (XLS) o valores separados por tabulaciones (TSV); algunos tipos de informe también se pueden guardar como [!UICONTROL Excel] libros con una hoja de cálculo independiente para cada campaña aplicable.

  Desde esta pestaña, también puede crear un nuevo informe (que, opcionalmente, puede utilizarse como plantilla), crear un nuevo informe basado en la configuración de un informe existente, cancelar los informes en curso disponibles eliminándolos y eliminar cualquier informe completado disponible. Los informes con más de siete días se eliminan automáticamente.

* La ficha **[!UICONTROL Templates]** enumera todas las plantillas de informe básicas y avanzadas guardadas que tiene a su disposición, incluida la información acerca de las programaciones asociadas a ellas. La plantilla más reciente se encuentra en la parte superior de forma predeterminada.

  Desde esta pestaña, puede crear una nueva plantilla, editar cualquier plantilla que haya creado (incluida la adición, modificación o eliminación de su programación), generar un informe a partir de una plantilla y eliminar cualquier plantilla disponible.

## Uso de los informes

| Finalidad | Informe |
| ---- | ---- |
| Monitorización del rendimiento | <ul><li>[El [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[El [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[El [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[El [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[El [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[El [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Solución de problemas de rendimiento y análisis de tendencias | <ul><li>[El [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[El [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[El [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[El [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[El [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) y [El [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Cualquier informe básico que compare dos períodos de tiempo con la función &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identificación de oportunidades de crecimiento empresarial | <ul><li>(Anunciantes con solo seguimiento de conversión de Adobe Advertising) [El [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Anunciantes con solo seguimiento de conversión de Adobe Advertising) [El [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Anunciantes con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=es)) Informes personalizados en Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Anunciantes con solo seguimiento de conversión de Adobe Advertising) [El [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Anunciantes con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=es)) Informes personalizados en Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Las tareas de configuración iniciales para los informes](initial-setup.md)
>* [Los datos utilizados para los informes](data-used-for-reports.md)
>* [Administrar informes programados](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
