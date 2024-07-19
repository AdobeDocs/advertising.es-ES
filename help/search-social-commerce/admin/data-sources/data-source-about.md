---
title: Acerca de la sincronización de  [!DNL Google Analytics] métricas de conversión
description: Obtenga información sobre cómo sincronizar  [!DNL Google Analytics] métricas de conversión para la optimización y la generación de informes.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Sincronizar [!DNL Google Analytics] métricas de conversión

Search, Social y Commerce pueden sincronizar métricas de conversión para una cuenta, propiedad y combinación de vistas de [!DNL Google Analytics] específica para la optimización y la creación de informes. Se incluyen automáticamente [vistas de página](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sesiones](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Tasa de salida hacia otro sitio](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (calculada como salidas hacia otro sitio/sesiones) y [Duración de la sesión](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration). Puede incluir hasta 16 métricas adicionales por fuente de datos.

>[!NOTE]
>
>Los usuarios de Advertising DSP pueden usar las métricas de conversión como objetivos personalizados y en los informes.

Todo el uso de API para las transferencias de datos se evalúa como un proyecto en la cuenta de [!DNL Google Analytics] aplicable. Puede ver las cuotas de este proyecto en [the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consulte la documentación de [!DNL Google Analytics] para obtener más información sobre [cuotas y límites de llamadas para informar solicitudes de API](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

Los pasos siguientes describen el proceso de sincronización de datos de conversión de [!DNL Google Analytics].

1. [Realizar las tareas previas necesarias](data-source-prerequisites.md)

   * Implemente un token de Adobe Advertising (parámetro de cadena de consulta `ef_id`) en las direcciones URL de la página de aterrizaje para todas las cuentas publicitarias aplicables.

   * Capture el token de Adobe Advertising (parámetro de cadena de consulta `ef_id`) en un [!DNL Custom Dimension] en [!DNL Google Analytics].

1. (Solo el administrador de cuentas de agencia, el administrador de cuentas de agencia, el administrador de cuentas de [!DNL Adobe] y los usuarios administradores) [Cree una fuente de datos por  [!DNL Google Analytics] cuenta, propiedad y combinación de vistas](data-source-configure.md).

   Para integrar métricas de varias propiedades o de varias vistas para una sola propiedad, configure una fuente de datos independiente para cada una.

   Una vez que se configura una fuente de datos, Search, Social y Commerce extraen datos diariamente, a partir de las 05:00 en el huso horario del anunciante. Una vez que las métricas estén disponibles, puede incluirlas en las vistas de administración de campañas y portafolios y en los informes, y utilizarlas en los objetivos de optimización, según sea necesario.

>[!MORELIKETHIS]
>
>* [Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos](data-source-prerequisites.md)
>* [Configurar una [!DNL Google Analytics] vista como fuente de datos](data-source-configure.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [Volver a autenticar un [!DNL Google Analytics] origen de datos](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configuración de origen de datos](data-source-settings.md)
>* [Apéndice:  [!DNL Google Analytics] métricas disponibles](data-source-ga-metrics.md)
