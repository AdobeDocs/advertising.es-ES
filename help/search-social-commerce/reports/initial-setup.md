---
title: Las tareas de configuración iniciales para los informes
description: Obtenga información sobre cómo hacer que las métricas estén disponibles en los informes y cómo automatizar los informes.
exl-id: 0f55aae9-6898-4967-a377-190a13dff6fd
feature: Search Reports
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Las tareas de configuración iniciales para los informes

Los nuevos usuarios deben realizar las siguientes tareas de configuración inicial:

* Realizar las métricas de conversión que el Adobe Advertising está rastreando para un anunciante [disponible para informes y otras vistas](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md), y opcionalmente [cambie el nombre de cualquiera de las métricas de conversión](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md que se muestran en encabezados de columna para facilitar la lectura.

  Las propiedades de transacciones no están disponibles para los informes a menos que las ponga a disposición específicamente.

  Si más adelante empieza a rastrear una nueva métrica de conversión, deberá repetir esta tarea.

* (Opcional) Automatice la generación de informes:

   * Si desea generar con regularidad datos de informes para un incremento de tiempo específico, como un [!UICONTROL Campaign Report] durante la última semana o los últimos 30 días, puede configurar [plantillas de informe](/help/search-social-commerce/reports/automation/templates/template-about.md) y programarlos para que se ejecuten a diario o en un día específico de la semana o del mes. Cada vez que se programa la ejecución del informe, se genera un nuevo informe. Tiene la opción de notificar las direcciones de correo electrónico de usuarios específicos de Search, Social y Commerce cuando se complete el informe, según el [configuración de notificaciones en [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si desea ver datos de informes diarios y actualizados en una hoja de cálculo con formato personalizado, con o sin tablas dinámicas y cualquier columna adicional que necesite para realizar más cálculos, puede configurar un informe diario [fuente de hoja de cálculo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Las fuentes de hoja de cálculo se actualizan diariamente con los datos de rendimiento más recientes y siguen conservando los datos de las fechas anteriores. Para configurar las fuentes de hoja de cálculo, primero debe crear una plantilla de hoja de cálculo personalizada en [!DNL Microsoft Excel]. Tiene la opción de notificar las direcciones de correo electrónico de usuarios específicos de Search, Social y Commerce cuando haya un archivo de fuente disponible, según el [configuración de notificaciones en [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si desea recibir informes básicos y avanzados en una ubicación FTP, puede configurar [Acceso mediante FTP a informes básicos y avanzados](/help/search-social-commerce/reports/automation/ftp-reports.md) solicitando una cuenta de FTP y configurando las plantillas de informes según una convención de nombres específica.

>[!MORELIKETHIS]
>
>* [Acerca de los informes](report-about.md)
>* [Datos utilizados para los informes](data-used-for-reports.md)
