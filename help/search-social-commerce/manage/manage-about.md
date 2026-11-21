---
title: Acerca de la administración de campañas y portafolios
description: Descubra cómo funcionan juntas las cuentas de red de publicidad, las campañas, el seguimiento y la optimización del portafolio, y cómo monitorizar y mejorar el rendimiento.
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# Acerca de la administración de campañas y portafolios

*característica de Beta*

Search, Social y Commerce aúna la administración de campañas, la creación de informes de rendimiento y la optimización del portafolio en una interfaz. Según la red de anuncios y el tipo de campaña, puede sincronizar los datos de campaña, crear y editar componentes de campaña, realizar un seguimiento de las conversiones y optimizar ofertas, presupuestos o objetivos de estrategia de oferta. Consulte [inventario admitido](/help/search-social-commerce/introduction/supported-inventory.md) para ver las funciones disponibles en cada red de publicidad.

El menú [!UICONTROL Manage] proporciona acceso a sus cuentas, campañas, grupos de anuncios, anuncios, palabras clave, grupos de productos y portafolios. Los permisos determinan qué vistas y acciones están disponibles. Para obtener la organización completa del menú, consulte &quot;[Cómo está organizada la interfaz de usuario](/help/search-social-commerce/getting-started/user-interface.md)&quot;.

## Cómo encajan las cuentas, las campañas y los portafolios

* **Cuentas de red de anuncios** conectan los datos del anunciante a Search, Social y Commerce. [Los tipos de cuenta](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) incluyen cuentas sincronizadas a través de una conexión API, cuentas para las que se cargan datos y cuentas basadas en plantillas de solo seguimiento. El tipo de cuenta determina si puede sincronizar datos, administrar campañas o utilizar la optimización del portafolio.

* **Campañas** contienen los anuncios y otros componentes que se usaron para entregar la publicidad. Para los tipos de campaña admitidos, puede [crear y administrar campañas](/help/search-social-commerce/manage/campaigns/campaign-manage.md) y sus componentes desde las vistas [!UICONTROL Manage]. También puede usar [hojas de edición masiva](/help/search-social-commerce/set-up/bulksheets/about.md) para operaciones masivas admitidas.

* **Portafolios** agrupa campañas elegibles para optimizarlas hacia un objetivo comercial común y un presupuesto o un objetivo de rendimiento. Una campaña solo puede pertenecer a un portafolio y todas las campañas de un portafolio deben utilizar la misma moneda. Consulte &quot;[Acerca de los portafolios](/help/search-social-commerce/manage/portfolios/portfolio-about.md).&quot;

La asignación de Portfolio es opcional. Puede realizar un seguimiento de las campañas e informar sobre ellas sin asignarlas a un portafolio. No todas las redes de anuncios, tipos de campañas ni estrategias de oferta admiten la optimización del portafolio.

## Sincronización de datos de campaña

En el caso de cuentas conectadas a través de una API, Search, Social y Commerce recuperan los datos de rendimiento y estructura de la campaña admitidos de la red de publicidad. Los cambios que realice en los componentes de campaña admitidos en Search, Social y Commerce se enviarán a la red de anuncios.

Si es necesario, [puede solicitar una sincronización manual](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md). Si una cuenta deja de sincronizarse, revisa su [estado de autenticación y acceso](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status).

Las cuentas de carga de datos y las cuentas solo de seguimiento no se sincronizan con la red de publicidad. Siga el flujo de trabajo del [tipo de cuenta](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) para proporcionar datos de campaña y rendimiento.

## Configuración del seguimiento y la optimización

[Seguimiento](/help/search-social-commerce/tracking/tracking-about.md) conecta la actividad de la campaña con las conversiones que importan a su negocio. Según la implementación, los datos de conversión pueden proceder de etiquetas de Adobe Advertising, una integración de Adobe Analytics, un seguimiento de red de publicidad o fuentes de datos. Configure el rastreo de clics y el seguimiento de conversión según sea necesario para la implementación y valide los datos antes de utilizarlos para la optimización.

En [!UICONTROL Goals] > [!UICONTROL Conversions], puede [revisar las métricas de conversión rastreadas para el anunciante y controlar su visibilidad](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md). Use las métricas apropiadas en sus [objetivos](/help/search-social-commerce/goals/objectives/objective-about.md).

Para habilitar la optimización del portafolio, [cree un portafolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md), asigne un objetivo y campañas elegibles, y configure su gasto y configuración de optimización. Un portafolio activo recopila y modela datos de rendimiento. Cuando los datos y la configuración estén listos, [cambie el estado del portafolio a optimizado](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) para comenzar la optimización. Las acciones realizadas dependen del tipo de portafolio y de las [estrategias de oferta de campaña](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

Para ver la secuencia de configuración detallada, consulte &quot;[Configurar cuentas y campañas de red de anuncios](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)&quot;.

## Monitorización del rendimiento de campañas y portafolios {#monitor-performance}

El equipo de la cuenta, la agencia o el anunciante es responsable de supervisar el rendimiento y realizar ajustes, según los términos del contrato de servicio. Rutinariamente:

* Revise el rendimiento de la cuenta y la campaña en las vistas [!UICONTROL Manage]. [Personalice las columnas, los filtros y los intervalos de fechas](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) para que se centren en las métricas y entidades que importan.

* Use [!UICONTROL Dashboard] > [!UICONTROL Overview] para [supervisar las tendencias y los cambios del portafolio en el rendimiento](/help/search-social-commerce/dashboard/dashboard-overview.md).

* Revise [alertas personalizadas](/help/search-social-commerce/common-tasks/alerts-manage.md) para detectar condiciones que requieran investigación.

* [Generar informes](/help/search-social-commerce/reports/management/report-manage.md) para rendimiento de campañas, palabras clave, anuncios y portafolios. Para portafolios, [revise los detalles de rendimiento](/help/search-social-commerce/manage/portfolios/portfolio-details.md), incluido el rendimiento real y la precisión del modelo.

* Utilice [simulaciones](/help/search-social-commerce/plan/simulations/simulation-about.md), cuando estén disponibles, para evaluar los efectos previstos de diferentes niveles de gasto.

* Investigue las diferencias entre las conversiones notificadas y los datos de origen. Consulte las instrucciones para los datos de conversión de [!DNL Google Ads] y [!DNL Microsoft Advertising] en los vínculos relacionados.

## Ajuste de campañas y portafolios

En función del rendimiento y de los cambios en los objetivos de su empresa, es posible que tenga que hacer lo siguiente:

* Editar la configuración de la campaña, crear o pausar componentes de campaña, refinar conjuntos de palabras clave o probar diferentes anuncios. Las acciones disponibles dependen de la red de publicidad y del tipo de campaña.

* Revise la segmentación geográfica, de audiencia y de ubicación utilizando las vistas de administración e informes relevantes.

* [Cambiar asignaciones de campaña](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) cuando una campaña se debe optimizar con un portafolio diferente. Asignar una campaña a otro portafolio la elimina de su portafolio anterior.

* [Editar la configuración del portafolio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md), incluyendo el objetivo, la estrategia de gasto, las restricciones o los controles de optimización, según lo permitido por el perfil del producto.

* Revisar [historial de cambios](/help/search-social-commerce/reports/history-logs.md) al investigar cambios de rendimiento.

>[!MORELIKETHIS]
>
>* [Configurar cuentas y campañas de red de anuncios](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)
>* [[!DNL Google Ads] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
