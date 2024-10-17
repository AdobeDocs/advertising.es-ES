---
title: Acerca de los informes
description: Obtenga información acerca de los informes de rendimiento, incluidos los diferentes tipos de informes disponibles y cómo automatizar los informes.
exl-id: 173d1bad-e3aa-4417-a9b1-4b5d06c304d2
feature: Search Reports
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# Acerca de los informes

Los informes de rendimiento le permiten realizar un seguimiento y administrar el rendimiento de sus portafolios, redes de publicidad y entidades de cuenta de red de publicidad con el nivel de granularidad que desee. La mayoría de los informes proporcionan una visibilidad completa sobre cómo los anuncios de cada canal de marketing contribuyen a la tasa de conversión general.

Los datos de un informe se compilan dinámicamente cada vez que se ejecuta el informe. Si lo desea, puede generar un informe nuevo a partir de uno existente. Los parámetros de informe disponibles varían según el tipo de informe. Para la mayoría de los informes, tiene la opción de previsualizar las primeras 50 líneas en lugar de generar todo el informe. Cuando genere un informe, puede enviar una notificación con vínculos de descarga a una o varias direcciones de correo electrónico cuando se complete el informe y los destinatarios pueden [administrar las notificaciones en [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Todos los informes completados están disponibles en la sección [!UICONTROL Latest Reports] de la vista [!UICONTROL Reports] y puede verlos en formato de tabla en la ventana del explorador o abrirlos o descargarlos como archivos.

## Categorías de informe disponibles

Las siguientes categorías de informes están disponibles en la vista [!UICONTROL Reports]. Es posible que no tenga acceso a todos ellos; los informes disponibles y los datos que generan están determinados por su función y por la forma en que se configura su cuenta de cliente.

| Categoría del informe | Descripción |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Los informes básicos](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md), que están disponibles para todos los usuarios, muestran los datos reales de costos y clics para portafolios, cuentas de red de anuncios, cuentas de red de anuncios específicas, campañas, grupos de anuncios, anuncios, palabras clave, grupos de productos, clasificaciones de etiquetas y valores de etiquetas, restricciones de unidades de oferta y restricciones de red. Se basan en clics facturados por las redes de publicidad aplicables y, opcionalmente, pueden incluir datos de conversión o cualquier otra métrica que cree. |
| [!UICONTROL Advanced Reports] | [Informes avanzados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) proporcionan información adicional sobre la configuración de publicidad, lo que le ayuda a identificar las ventajas de cambiar la segmentación geográfica o la configuración de red. También pueden ayudarle a validar los datos de conversión de las vistas e informes de administración de campañas y portafolios con los datos de seguimiento de conversión internos del anunciante. |
| [!UICONTROL Assist Reports] | [Informes de asistencia](/help/search-social-commerce/reports/management/assist/assist-report-about.md) proporcionan información sobre las rutas de conversión para todas las palabras clave y anuncios del anunciante. Utilizan datos capturados mediante el servicio de seguimiento de conversión de Adobes Advertising y solo se pueden generar para anunciantes con el servicio. |
| [!UICONTROL Specialty Reports] | [Informes especiales](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) constan de datos recopilados por las redes de anuncios (en lugar de por el seguimiento de Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Los informes de precisión del modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indican la precisión de los modelos de costo e ingresos que se usan para optimizar ofertas, presupuestos de campaña y objetivos de estrategia de oferta para un portafolio. |

## Automatización de informes

Programe informes personalizados para que se generen automáticamente de una o ambas de las siguientes maneras:

* Genere informes automáticamente cada día o un día específico de la semana o del mes, usando [plantillas de informes](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Si lo desea, puede configurar el envío por FTP de [informes básicos y avanzados](/help/search-social-commerce/reports/automation/ftp-reports.md) que utilizan una plantilla.

* Siga actualizando las plantillas de hoja de cálculo personalizadas con datos de rendimiento diarios mediante [fuentes de hoja de cálculo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## Las vistas Informes

Las vistas [!UICONTROL Reports] en [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] le permiten crear y administrar informes, plantillas y fuentes de hojas de cálculo. La vista incluye dos pestañas:

* La ficha **[!UICONTROL Latest Reports]** enumera todos los informes disponibles para usted que se solicitaron en los últimos siete días, excepto los que se eliminaron manualmente, con el informe más reciente en la parte superior de forma predeterminada. La información mostrada para cada informe incluye la programación según la cual se ejecuta (cuando corresponde), las fechas de inicio y finalización para las cuales se generaron o se generarán datos, y el estado del informe (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* o *[!UICONTROL Error]*).

  Los vínculos junto a cada informe permiten ver el informe en el explorador web o abrirlo o guardarlo como un archivo de [!DNL Microsoft Excel] libro (XLS) o valores separados por tabulaciones (TSV); algunos tipos de informe también se pueden guardar como [!UICONTROL Excel] libros con una hoja de cálculo independiente para cada campaña aplicable.

  Desde esta pestaña, también puede crear un nuevo informe (que, opcionalmente, puede utilizarse como plantilla), crear un nuevo informe basado en la configuración de un informe existente, cancelar los informes en curso disponibles eliminándolos y eliminar cualquier informe completado disponible. Los informes con más de siete días se eliminan automáticamente.

* La ficha **[!UICONTROL Templates]** enumera todas las plantillas de informe básicas y avanzadas guardadas que tiene a su disposición, incluida la información acerca de las programaciones asociadas a ellas. La plantilla más reciente se encuentra en la parte superior de forma predeterminada.

  Desde esta pestaña, puede crear una nueva plantilla, editar cualquier plantilla que haya creado (incluida la adición, modificación o eliminación de su programación), generar un informe a partir de una plantilla y eliminar cualquier plantilla disponible.

## Uso de los informes

| Finalidad | Informe |
| ---- | ---- |
| Monitorización del rendimiento | <ul><li>[El [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[El [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[El [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[El [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[El [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[El [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Solución de problemas de rendimiento y análisis de tendencias | <ul><li>[El [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[El [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[El [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[El [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[El [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) y [El [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Cualquier informe básico que compare dos períodos de tiempo con la función &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identificación de oportunidades de crecimiento empresarial | <ul><li>(Anunciantes con seguimiento de conversión de Adobe Advertising solamente) [El [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Anunciantes con seguimiento de conversión de Adobe Advertising solamente) [El [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Anunciantes con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Informes personalizados en Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Anunciantes con seguimiento de conversión de Adobe Advertising solamente) [El [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Anunciantes con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Informes personalizados en Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Datos usados para informes](data-used-for-reports.md)
>* [Tareas de configuración iniciales para informes](initial-setup.md)
>* [Generar un informe básico o avanzado](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Generar un informe de precisión de modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Generar informe de especialidad](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Generar un informe de asistencia](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
