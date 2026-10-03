---
title: (Nueva IU) Las tareas de configuración iniciales de los informes
description: Obtenga información sobre cómo hacer que las métricas estén disponibles en los informes y cómo automatizar los informes.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
    internal-label: Reports
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%
---
# (Nueva IU) Las tareas de configuración iniciales de los informes

Los nuevos usuarios deben realizar las siguientes tareas de configuración inicial:

* Ponga a disposición de los informes y otras vistas las métricas de conversión que Adobe Advertising está rastreando para un anunciante y, opcionalmente, cambie el nombre de cualquiera de las métricas de conversión que se muestran en los encabezados de columna para facilitar la lectura. Consulte &quot;[Administrar las métricas de conversión de un anunciante](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)&quot;.

  Las propiedades de transacciones no están disponibles para los informes a menos que las ponga a disposición específicamente.

  Si más adelante empieza a rastrear una nueva métrica de conversión, debe repetir esta tarea.

* (Opcional) Automatice la generación de informes:

  * Si desea generar con regularidad datos de informes para un incremento de tiempo específico, como [!UICONTROL Campaign Report] de la última semana o de los últimos 30 días, puede configurar [plantillas de informes](report-templates-manage.md) y programarlas para que se ejecuten a diario o en un día específico de la semana o del mes. Cada vez que se programa la ejecución del informe, se genera un nuevo informe. Tiene la opción de notificar a las direcciones de correo electrónico de usuarios específicos de Search, Social y Commerce cuando se complete el informe, según la configuración de [notificación establecida en [!UICONTROL Notification Center]][Manage custom alerts]&#x200B;(/help/search-social-commerce/new-ui/notifications-manage.md).

  * Si desea ver datos de informes diarios actualizados en una hoja de cálculo con formato personalizado, con o sin tablas dinámicas y cualquier columna adicional que necesite para realizar más cálculos, puede configurar una [fuente de hoja de cálculo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) diaria. Las fuentes de hoja de cálculo se actualizan diariamente con los datos de rendimiento más recientes y siguen conservando los datos de las fechas anteriores. Para configurar las fuentes de hoja de cálculo, primero debe crear una plantilla de hoja de cálculo personalizada en [!DNL Microsoft Excel]. Tiene la opción de notificar a las direcciones de correo electrónico de usuarios específicos de Search, Social y Commerce cuando haya un archivo de fuente disponible, según la configuración de [notificación establecida en [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md).

  * Si desea recibir informes básicos y avanzados en una ubicación FTP, puede configurar [acceso FTP a informes básicos y avanzados](/help/search-social-commerce/new-ui/reports/ftp-reports.md) solicitando una cuenta FTP y configurando plantillas de informes con una convención de nombres específica.

>[!MORELIKETHIS]
>
>* [Acerca de los informes](report-about.md)
>* [Datos usados para informes](data-used-for-reports.md)
