---
title: Configuración de cuentas y campañas de red de anuncios
description: Siga el flujo de trabajo de configuración para conexiones de red de anuncios, campañas, seguimiento, métricas de conversión y optimización de portafolios opcional.
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%
---
# Configuración de cuentas y campañas de red de anuncios

*característica de Beta*

[!DNL Adobe] y su agencia trabajan con usted para conectar sus cuentas de red de anuncios, preparar campañas, configurar el seguimiento y validar datos de rendimiento. Si desea que Search, Social y Commerce optimicen las campañas aptas, el flujo de trabajo también incluye la configuración del portafolio.

Esta lista de comprobación proporciona los detalles de la cuenta y la campaña para el [flujo de trabajo de implementación](implemention-overview.md) más amplio. Las tareas que puede realizar dependen de sus permisos y de la [funcionalidad admitida para cada tipo de campaña y red de publicidad](/help/search-social-commerce/introduction/supported-inventory.md).

## Configurar flujo de trabajo

1. **Confirmar los requisitos de acceso y cuenta.**

   Póngase en contacto con el administrador para confirmar el acceso al anunciante adecuado y los permisos necesarios para sus tareas. Consulte &quot;[Administración de usuarios para Search, Social y Commerce](/help/search-social-commerce/user-administration.md)&quot;.

   Si es necesario, cree la cuenta de red de anuncios real en el sitio web de la red de anuncios. La creación de un registro de cuenta en Search, Social y Commerce no crea una cuenta en la red de publicidad.

1. **Conectar o registrar cada cuenta de red de publicidad.**

   En [!UICONTROL Manage] > [!UICONTROL Accounts], use el flujo de trabajo para el [tipo de cuenta](/help/search-social-commerce/manage/accounts/ad-network-account-about.md):

   * **Conexión API:** [Cree los detalles de la cuenta](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account), complete la autenticación específica de red, configure las opciones de seguimiento y habilite la cuenta. Compruebe su [estado de autenticación y acceso](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status); la autenticación correcta no significa necesariamente que se hayan concedido todos los permisos necesarios.

   * **Carga de datos:** [Cree los detalles de la cuenta y cargue los datos de campaña y rendimiento](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md). Estas cuentas no se sincronizan con la red de anuncios ni con la optimización del portafolio de soporte.

   * **[!DNL Naver]solo seguimiento:** Sigue el [flujo de trabajo de la cuenta solo seguimiento](/help/search-social-commerce/manage/accounts/template-account-manage.md). Utilice hojas de edición masiva para generar direcciones URL de seguimiento y aplicarlas en el editor de la red de publicidad; la cuenta no se sincroniza ni admite la optimización del portafolios.

1. **Revisar o crear la estructura de la campaña.**

   Para cuentas conectadas a la API, revise las campañas sincronizadas y sus componentes. [Solicite una sincronización manual](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md) cuando sea necesario.

   Para los tipos de campaña admitidos, use [!UICONTROL Manage] > [!UICONTROL Campaigns] para [crear o editar campañas](/help/search-social-commerce/manage/campaigns/campaign-manage.md). Cree los [grupos de anuncios](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md), [anuncios](/help/search-social-commerce/manage/ads/ad-manage.md) necesarios y otros componentes compatibles. También puede usar [hojas de edición masiva](/help/search-social-commerce/set-up/bulksheets/about.md) para operaciones masivas admitidas.

   Complete la configuración específica de red que necesite antes de activar las campañas. Administre los componentes no compatibles en la interfaz de la propia red de publicidad.

1. **Configurar y validar el seguimiento antes del inicio.**

   Seleccione el [método de seguimiento de conversión](/help/search-social-commerce/tracking/conversion-tracking-about.md) que coincida con su implementación. Si es necesario, [genere y aplique URL de seguimiento de clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) y [genere etiquetas de seguimiento de conversiones](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md).

   Configure las [integraciones](/help/integrations/home.md) o [fuentes de conversión](/help/search-social-commerce/tracking/tracking-about.md) necesarias y valide que las conversiones se puedan atribuir según lo esperado. Para las campañas solo de seguimiento, aplique las direcciones URL de seguimiento generadas en el editor de la red de publicidad.

1. **Revisar métricas de conversión.**

   En [!UICONTROL Goals] > [!UICONTROL Conversions], [revise las métricas rastreadas y haga visibles las métricas requeridas](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available) para las vistas de administración, los informes y los objetivos. Cambie los nombres para mostrar cuando sea necesario para distinguir las métricas.

1. **(Opcional) Preparar optimización de portafolios.**

   Confirme que las campañas y sus estrategias de oferta [cumplen los requisitos para la optimización del portafolio](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

   [Cree o seleccione un objetivo](/help/search-social-commerce/goals/objectives/objective-about.md) que use las métricas de conversión adecuadas. En [!UICONTROL Manage] > [!UICONTROL Portfolios], [cree un portafolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md) o [edite un portafolio existente](/help/search-social-commerce/manage/portfolios/portfolio-edit.md) con el objetivo, la estrategia de gasto y la configuración de optimización requeridos.

   [Asigne las campañas al portafolio](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). Cada campaña solo puede pertenecer a un portafolio, y todas las campañas de un portafolio deben utilizar la misma moneda.

1. **Validar datos de campaña y establecer una línea de base de rendimiento.**

   Confirme que los datos de coste, clics y conversión estén disponibles para cada campaña. Comparar datos de conversión con el origen apropiado, incluidos [!DNL Google Ads] y [!DNL Microsoft Advertising] cuando corresponda. Utilice intervalos de fechas y configuraciones de atribución coherentes al comparar informes.

   Para un nuevo portafolio, [actívelo](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) para recopilar y modelar datos. Valide la configuración de los datos y el portafolio antes de activar la optimización.

1. **(Opcional) Iniciar optimización de portafolio.**

   Cuando el portafolio esté listo, [cambie su estado a optimizado](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) y revise los requisitos previos y los mensajes de confirmación. A continuación, Search, Social y Commerce optimizan el portafolio según su configuración y las estrategias de oferta de campaña admitidas.

1. **Configurar supervisión e informes continuos.**

   [Personaliza tus vistas de datos](/help/search-social-commerce/common-tasks/data-views/data-views-about.md), [configura alertas personalizadas](/help/search-social-commerce/common-tasks/alerts-manage.md) y [genera informes programados](/help/search-social-commerce/reports/management/report-manage.md). Cuando sea necesario, automatice la generación de informes usando [plantillas de informes](/help/search-social-commerce/reports/report-templates-manage.md) y [fuentes de hojas de cálculo](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Continúe [supervisando y ajustando campañas y portafolios](/help/search-social-commerce/manage/manage-about.md#monitor-performance) después del lanzamiento.

>[!MORELIKETHIS]
>
>* [Información general sobre la implementación de Search, Social y Commerce](implemention-overview.md)
>* [Acerca de la administración de campañas y portafolios](/help/search-social-commerce/manage/manage-about.md)
>* [[!DNL Google Ads] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
