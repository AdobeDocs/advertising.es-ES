---
title: Información general sobre la implementación de Search, Social y Commerce
description: Obtenga información sobre el flujo de trabajo general para iniciar y mantener un portafolio.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%
---
# Información general sobre la implementación de Search, Social y Commerce

[!DNL Adobe] o una de sus agencias afiliadas trabaja con cada anunciante para lanzar sus portafolios de publicidad en línea y rastrear cualquier campaña de publicidad adicional. Después del primer inicio, las tareas continuas adicionales garantizan que se sigan cumpliendo los objetivos del anunciante.

A continuación se muestra el flujo de trabajo general para implementar y utilizar Search, Social y Commerce.

## Lanzamiento inicial

[!DNL Adobe] y/o su agencia trabajan con usted para lo siguiente:

1. Evalúe sus objetivos empresariales de alto nivel y diseñe estrategias para alcanzarlos:

   1. Identifique el modelo empresarial y los objetivos de marketing.

   1. Identificar los requisitos de seguimiento de conversión

   1. Analice las estructuras de cuenta de publicidad en línea existentes.

   1. Identifique las métricas para la optimización y la creación de informes de portafolios.

1. (Usuarios del administrador o del administrador de cuentas) Configurar cuentas administrativas:

   1. Configure la cuenta del anunciante. Si una agencia administra los datos del anunciante, la cuenta del anunciante debe asociarse a la cuenta de la agencia.

   1. (Si es necesario) Cree cuentas de usuario para que el anunciante vea y administre sus datos de campaña y genere informes.

   Póngase en contacto con el administrador para configurar el acceso mediante Adobe Admin Console y los perfiles de producto adecuados. Consulte &quot;[Administración de usuarios para Search, Social y Commerce](/help/search-social-commerce/user-administration.md)&quot;.

1. Sincronice o cree campañas para cada una de las cuentas de red de publicidad:

   * Para las cuentas conectadas a la API, [cree los detalles de la cuenta](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account) en [!UICONTROL Manage] > [!UICONTROL Accounts], complete la autenticación específica de la red, configure las opciones de seguimiento y habilite la cuenta.

   * Para las cuentas sin compatibilidad con API, siga el flujo de trabajo [carga de datos](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md) o [cuenta solo de seguimiento](/help/search-social-commerce/manage/accounts/template-account-manage.md), según corresponda. Estas cuentas no se sincronizan con la red de anuncios ni con la optimización del portafolio de soporte.

   * Si las cuentas aún no contienen datos de campaña, agregue campañas, grupos de anuncios, palabras clave, anuncios y ubicaciones desde Buscar, Social y Commerce o desde la red de anuncios.

     Para ver la lista de comprobación detallada de la configuración, consulte &quot;[Configurar cuentas y campañas de red de anuncios](campaign-implementation-overview.md)&quot;. Para los tipos de campaña admitidos, use [!UICONTROL Manage] > [!UICONTROL Campaigns] para [crear y administrar campañas](/help/search-social-commerce/manage/campaigns/campaign-manage.md).

1. Configure el seguimiento para todos los anuncios para los que desee que Adobe Advertising rastree conversiones:

   1. (Si es necesario) [Configure el rastreo de clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) para los anuncios y, opcionalmente, para las palabras clave, las ubicaciones de [!DNL Google Ads] y las extensiones de [!DNL Google Ads] mediante la generación y carga de direcciones URL de rastreo de clics.

      Las URL de rastreo de clics para anunciantes con el servicio de seguimiento de conversiones basado en píxeles de Adobe Advertising incluyen una redirección a [!DNL Adobe] servidores.

   1. [Configurar el seguimiento de conversión](/help/search-social-commerce/tracking/conversion-tracking-about.md). Según la implementación, esto puede implicar agregar etiquetas de seguimiento de conversión a las páginas web adecuadas o configurar una colocación diaria de fuentes para los datos de conversión que haya recopilado con su propio método. Puede [generar etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md) desde [!UICONTROL Goals] > [!UICONTROL Conversions].

      Para obtener más información, consulte &quot;[Acerca del seguimiento para Search, Social y Commerce](/help/search-social-commerce/tracking/tracking-about.md)&quot;.

1. Configurar integraciones con productos adicionales:

   1. (Anunciantes con Adobe Analytics o Adobe Audience Manager) Configure integraciones entre las distintas cuentas para que Adobe Advertising pueda intercambiar datos con ellas.

      Consulte la guía de &quot;[Integraciones con CX Enterprise](/help/integrations/home.md)&quot;.

   1. (Anunciantes con [!DNL Google Analytics]) Sincronizar las métricas de conversión de una cuenta, propiedad y combinación de vistas de [!DNL Google Analytics] para la optimización y la creación de informes.

      Esta configuración utiliza la interfaz de usuario heredada. Ver &quot;[Acerca de la sincronización [!DNL Google Analytics] métricas de conversión](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md)&quot; y, cuando sea necesario, [cambiar a la interfaz heredada](ui-switch.md).

1. (Opcional) Configurar e iniciar portafolios:

   1. En [!UICONTROL Goals] > [!UICONTROL Conversions], [revise las métricas de conversión y haga visibles las métricas requeridas](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available). En [!UICONTROL Goals] > [!UICONTROL Objectives], [cree o seleccione un objetivo](/help/search-social-commerce/goals/objectives/objective-about.md) para la optimización.

   1. En [!UICONTROL Manage] > [!UICONTROL Portfolios], [cree portafolios](/help/search-social-commerce/manage/portfolios/portfolio-create.md) configurados para cumplir con sus objetivos y metas empresariales, con las [campañas elegibles](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) apropiadas. [Activar los portafolios](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) para recopilar y modelar datos. A continuación, el equipo de implementación recopila y valida los datos de clics e ingresos durante al menos 14 días y valida la configuración del portafolio.

      >[!NOTE]
      >
      >Search, Social y Commerce siguen realizando un seguimiento de los datos de las campañas que no están asignadas a los portafolios, y los informes correspondientes, pero no les proporcionan una optimización.

   1. Una vez que se disponga de datos suficientes para crear una línea de base, el equipo puede [cambiar el estado del portafolio a optimizado](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), lo que permite que Search, Social y Commerce optimicen las ofertas, los presupuestos o los objetivos de estrategia de oferta del portafolio, según el tipo de portafolio y las estrategias de oferta de la campaña.

   Consulte &quot;[Acerca de los portafolios](/help/search-social-commerce/manage/portfolios/portfolio-about.md)&quot; para obtener soporte de optimización y estados del portafolio.

1. Monitorice el rendimiento de sus portafolios:

   1. Use [!UICONTROL Dashboard] > [!UICONTROL Overview] para [revisar las tendencias del portafolio](/help/search-social-commerce/dashboard/dashboard-overview.md) y [ver los detalles del rendimiento del portafolio](/help/search-social-commerce/manage/portfolios/portfolio-details.md) para investigar los resultados y la precisión del modelo.

   1. [Configurar alertas personalizadas](/help/search-social-commerce/common-tasks/alerts-manage.md) y [generar informes personalizados](/help/search-social-commerce/reports/management/report-manage.md) para supervisar el rendimiento. Cuando sea necesario, automatice la generación de informes usando [plantillas de informes](/help/search-social-commerce/reports/report-templates-manage.md) y [fuentes de hojas de cálculo](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Para obtener más información, consulte &quot;[Monitorizar el rendimiento de la campaña y del portafolio](/help/search-social-commerce/manage/manage-about.md#monitor-performance)&quot;.

1. (Opcional) Configure sus [vistas de datos de rendimiento](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) para que muestren los datos que desea ver.

## Tareas en curso

Después del primer inicio, se requieren las siguientes tareas en curso. Según las condiciones de participación, [!DNL Adobe], una agencia afiliada o el anunciante realizan las siguientes tareas:

* Continúe monitorizando y analizando el rendimiento de cada portafolio mediante la visualización de alertas, datos de rendimiento para cada portafolio y sus campañas de componentes, informes personalizables y simulaciones (algunas funciones).

* Ajuste las distintas estrategias y configuraciones que utilice para administrar el conjunto de portafolios, según sea necesario, en función del rendimiento real y previsto del portafolio y de las oportunidades de crecimiento:

  * Ajuste los presupuestos, los objetivos y otros ajustes del portafolio.

  * Ajuste las estructuras de cuenta/campaña para adaptarse a los cambios en la estrategia de marketing.

  * Adición, pausa o eliminación de componentes de campaña. Esto puede incluir la expansión de conjuntos de palabras clave basados en el análisis de términos de búsqueda y la prueba de copias de anuncios y páginas de aterrizaje.

  * Actualice las estrategias de segmentación geográfica y de sitio basadas en informes de rendimiento avanzados.

  * (Opcional) Añada restricciones de oferta a palabras clave de búsqueda individuales o a todas las palabras clave de un grupo de anuncios, una campaña o un portafolios.

  * Agregar nuevos portafolios.

Para obtener instrucciones sobre cómo supervisar campañas y portafolios y ajustar su configuración, consulte &quot;[Acerca de la administración de campañas y portafolios](/help/search-social-commerce/manage/manage-about.md)&quot; y &quot;[Editar detalles del portafolio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)&quot;.
