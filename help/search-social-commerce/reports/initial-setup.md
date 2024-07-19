---
title: Las tareas de configuración iniciales para los informes
description: Obtenga información sobre cómo hacer que las métricas estén disponibles en los informes y cómo automatizar los informes.
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Las tareas de configuración iniciales para los informes

Los nuevos usuarios deben realizar las siguientes tareas de configuración inicial:

* Haga que las métricas de conversión que el Adobe Advertising está rastreando para un anunciante [estén disponibles para informes y otras vistas](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md) y, opcionalmente, [cambie el nombre de cualquiera de las métricas de conversión](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) que se muestran en los encabezados de columna para facilitar la lectura.

  Las propiedades de transacciones no están disponibles para los informes a menos que las ponga a disposición específicamente.

  Si más adelante empieza a rastrear una nueva métrica de conversión, debe repetir esta tarea.

* (Opcional) Automatice la generación de informes:

   * Si desea generar con regularidad datos de informes para un incremento de tiempo específico, como [!UICONTROL Campaign Report] de la última semana o de los últimos 30 días, puede configurar [plantillas de informes](/help/search-social-commerce/reports/automation/templates/template-about.md) y programarlas para que se ejecuten a diario o en un día específico de la semana o del mes. Cada vez que se programa la ejecución del informe, se genera un nuevo informe. Tiene la opción de notificar a las direcciones de correo electrónico de usuarios específicos de Search, Social y Commerce cuando se complete el informe, según la configuración de [notificación establecida en [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si desea ver datos de informes diarios actualizados en una hoja de cálculo con formato personalizado, con o sin tablas dinámicas y cualquier columna adicional que necesite para realizar más cálculos, puede configurar una [fuente de hoja de cálculo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) diaria. Las fuentes de hoja de cálculo se actualizan diariamente con los datos de rendimiento más recientes y siguen conservando los datos de las fechas anteriores. Para configurar las fuentes de hoja de cálculo, primero debe crear una plantilla de hoja de cálculo personalizada en [!DNL Microsoft Excel]. Tiene la opción de notificar a las direcciones de correo electrónico de usuarios específicos de Search, Social y Commerce cuando haya un archivo de fuente disponible, según la configuración de [notificación establecida en [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si desea recibir informes básicos y avanzados en una ubicación FTP, puede configurar [acceso FTP a informes básicos y avanzados](/help/search-social-commerce/reports/automation/ftp-reports.md) solicitando una cuenta FTP y configurando plantillas de informes con una convención de nombres específica.

>[!MORELIKETHIS]
>
>* [Acerca de los informes](report-about.md)
>* [Datos usados para informes](data-used-for-reports.md)
