---
title: Acerca de la sincronización [!DNL Google Analytics] métricas de conversión
description: Más información sobre la sincronización [!DNL Google Analytics] métricas de conversión para optimización y creación de informes.
role: User, Admin
exl-id: 0c263ced-3774-4d4b-9d61-65289cd74027
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Acerca de la sincronización [!DNL Google Analytics] métricas de conversión

Search, Social y Commerce pueden sincronizar métricas de conversión para un específico. [!DNL Google Analytics] combinación de cuenta, propiedad y vista para optimización y sistema de informes. [Page views](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sesiones](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Tasa de devoluciones](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (calculado como devoluciones/sesiones) y [Duración de sesión](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) se incluyen automáticamente. Puede incluir hasta 16 métricas adicionales por fuente de datos.

>[!NOTE]
>
>DSP Los usuarios de Advertising pueden usar las métricas de conversión como objetivos personalizados y en los informes.

Todo el uso de API para las transferencias de datos se evalúa como un proyecto en el [!DNL Google Analytics] cuenta. Puede ver las cuotas de este proyecto en [el [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consulte [!DNL Google Analytics] para obtener más información acerca de [cuotas y límites de llamadas para informar solicitudes de API](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

Los siguientes pasos describen el proceso para sincronizar datos de conversión de [!DNL Google Analytics].

1. [Realizar las tareas previas necesarias](data-source-prerequisites.md)

   * Implementar un token de Adobe Advertising (`ef_id` parámetro de cadena de consulta) en las direcciones URL de la página de aterrizaje de todas las cuentas publicitarias aplicables.

   * Capture el token de Adobe Advertising (`ef_id` parámetro de cadena de consulta) en una [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (administrador de cuentas de agencia, administrador de cuentas de agencia, [!DNL Adobe] administrador de cuentas, y solo usuarios administradores) [Crear una fuente de datos por [!DNL Google Analytics] combinación de cuenta, propiedad y vista](data-source-configure.md).

   Para integrar métricas de varias propiedades o de varias vistas para una sola propiedad, configure una fuente de datos independiente para cada una.

   Una vez configurada una fuente de datos, Search, Social y Commerce extrae datos diariamente, a partir de las 05:00 en el huso horario del anunciante. Una vez que las métricas estén disponibles, puede incluirlas en las vistas de administración de campañas y portafolios y en los informes, y utilizarlas en los objetivos de optimización, según sea necesario.

>[!MORELIKETHIS]
>
>* [Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos](data-source-prerequisites.md)
>* [Configurar un [!DNL Google Analytics] ver como fuente de datos](data-source-configure.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [Volver a autenticar un [!DNL Google Analytics] fuente de datos](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configuración de fuente de datos](data-source-settings.md)
>* [Apéndice: disponible [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
