---
title: Inventario admitido
description: Haga referencia a las redes de publicidad, los tipos de campaña y los tipos de publicidad admitidos.
source-git-commit: 95c7e67bb6f065567302f266959295ce8125c624
workflow-type: tm+mt
source-wordcount: '2371'
ht-degree: 0%

---

# Inventario admitido

A continuación se indican las redes de anuncios compatibles, los tipos de campaña y los tipos de publicidad, así como la funcionalidad disponible para cada uno.

| Origen | Red | Tipo de campaña | Tipo de anuncio | Sincronizar y ver | Crear/editar | Seguimiento[^1] | Optimización | Informe[^2] | Asistencia de Adobe Analytics[^3] |
|----|----|----|----|----|----|----|----|----|----|----|
| [!DNL Baidu] | Buscar red | Manual | Texto | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) y [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí | Campañas solo con estrategia de oferta de CPC manual | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
| [!DNL Google Ads] | Todo [!DNL Google] fuentes | Descubrimiento (función beta) | Descubrimiento (anuncios de una sola imagen)<br><br>Carrusel de descubrimiento (anuncios de carrusel de varias imágenes) | Automático mediante API | — | Sí | Solo en portafolios híbridos<br><br>Los objetivos de las ofertas y la estrategia de oferta se establecen en el nivel de campaña, junto con los presupuestos de campaña, según corresponda al tipo de optimización. | Datos de nivel de anuncio | Añadir datos de nivel de anuncio a Buscar, Social y Comercio (con el [código de seguimiento s_kwcid](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)[^4]<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Todo | Rendimiento estándar máximo (función beta) | Todos los tipos | Automático mediante API | Cree/edite recursos de campañas y cárguelos dentro de la configuración de campaña en la vista Campañas<br><br>Solo están disponibles las configuraciones necesarias. Para ver la configuración opcional y enumerar grupos, inicie sesión en [!DNL [!DNL Google Ads] Ads] editor. | Sí | Solo en portafolios híbridos<br><br>Los objetivos de la estrategia de oferta se establecen en el nivel de campaña, junto con los presupuestos de campaña. | Datos de nivel de campaña<br><br>Los datos para enumerar grupos no están disponibles y la red de anuncios no proporciona datos de nivel de anuncio. | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de campaña de Search, Social y Commerce a Analytics. Requiere la actualización [código de seguimiento s_kwcid](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md). |
|  | Mostrar red | Pantalla estándar | Imagen | Automático mediante API | Editar URL y estado solo mediante [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí, cuando agrega manualmente etiquetas de rastreo de clics a plantillas de seguimiento dentro de la red de publicidad | — | Datos de nivel de anuncio, pero sin datos de visualización | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics, pero sin datos de visualización |
|  | [!DNL Gmail]/Display red | [!DNL Gmail] campañas (en desuso ) | [!DNL Gmail] | — | — | — | — | Solo datos heredados de nivel de campaña | Datos heredados de Analytics en Search, Social y Commerce<br>Datos de nivel de campaña heredados de Search, Social y Commerce a Analytics |
|  | Buscar red | Búsqueda estándar | Solo llamada | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) | Sí, usando el sufijo de página de aterrizaje de nivel de cuenta y la plantilla de seguimiento, o añadiéndolos manualmente en el nivel de anuncio dentro de [!DNL [!DNL Google Ads] Administrador de anuncios | — | Solo impresiones y clics a nivel de grupo de anuncios desde la red de publicidad; sin ingresos | — |
|  | Buscar red | Búsqueda estándar | \[Expandida\] Búsqueda dinámica Tipo creativo &quot;Edsa&quot; | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) y [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí | Sí<br><br>Para grupos de publicidad cuando la campaña especifica un dominio de sitio web; de lo contrario, para destinos de búsqueda dinámica. | Datos de nivel de campaña y de grupo de publicidad<br><br>La red de anuncios no proporciona datos de nivel de anuncio. | Datos de Analytics para campañas de búsqueda, medios sociales y comercio y datos de nivel de grupo de publicidad desde Buscar, medios sociales y comercio hasta Analytics |
|  | Buscar red | Búsqueda estándar | Texto ampliado (obsoleto en junio de 2022) | Automático mediante API | Eliminación solo mediante [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) | Sí | — | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Búsqueda estándar | Búsqueda interactiva | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) | Sí | Sí | Datos de nivel de anuncio para todos los elementos de anuncio disponibles<br><br><b>Nota:</b> [!DNL [!DNL Google Ads] [Anuncios] no proporciona datos fuera de sus editores nativos sobre las combinaciones de texto que se mostraron como anuncios. Para obtener más información sobre los informes para cada combinación de texto, consulte la [[!DNL [!DNL Google Ads] Ads] documentación](https://support.google.com/google-ads/answer/7684791). | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Búsqueda estándar (obsoleta) | Texto | Automático mediante API | Cambios de estado en anuncios existentes solo mediante [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí | Sí | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Búsqueda estándar | <i>Extensión de anuncio:</i><br><br>Vínculo de sitio (nivel de cuenta, campaña y grupo de publicidad) | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) y [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | —<br><br>Los vínculos de sitio tienen un campo &quot;Plantilla de seguimiento&quot;, pero Search, Social y Commerce asignan clics y conversiones resultantes a la palabra clave asociada, no al vínculo de sitio individual. | — Buscar, Social y Comercio no optimiza el vínculo de sitio. En su lugar, se optimiza según la palabra clave asociada con el anuncio en el que se incluye el vínculo de sitio. | —<br><br>Están disponibles los datos de la palabra clave asociada. Entrada [!DNL Google Ads], puede ver los datos de rendimiento de nivel de vínculo de sitio en la variable [!DNL Campaigns] pestaña > [!DNL Ad Extensions] pestaña.<br><br>Para ver qué conversiones individuales resultaron de un clic en un vínculo a un sitio, genere un [Informe de transacciones](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md). El [!UICONTROL Link Type] el valor de columna para un vínculo de sitio es sl:&lt;sitelink text=&quot;&quot;></code>, como sl:Consulte Ofertas actuales. | Datos solo para la palabra clave asociada de Search, Social y Commerce a Analytics |
|  | Buscar red | Búsqueda estándar | <i>Otras extensiones de publicidad:</i><br><br>Extensión de llamada<br><br>Extensión de ubicación<br><br>Extensión de teléfono | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) | —<br><br>Los vínculos de sitio tienen un campo &quot;Plantilla de seguimiento&quot;, pero Search, Social y Commerce asignan clics y conversiones resultantes a la palabra clave asociada, no al vínculo de sitio individual.<br><br>Los otros tipos de extensiones de publicidad no tienen una dirección URL que rastrear y Search, Social y Commerce no pueden asignarles datos de conversión. | — | —<br><br>[!DNL Google Ads] asigna los clics en una extensión de anuncio a la palabra clave asociada con el anuncio en el que se incluye la extensión.<br><br>No hay datos de coste o clics en el nivel de extensión disponibles en Search, Social y Commerce. Entrada [!DNL Google Ads], puede ver los datos de costes y clics en el nivel de extensión en [!DNL Campaigns] pestaña > [!DNL Ad Extensions] pestaña.<br><br>Para ver qué conversiones individuales resultaron de un clic en un vínculo de sitio, genere un [Informe de transacciones](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md). El [!UICONTROL Link Type] la columna para un vínculo de sitio es sl:&lt;sitelink text=&quot;&quot;></code>, como sl:Consulte Ofertas actuales. | Datos solo para la palabra clave asociada de Search, Social y Commerce a Analytics |
|  | Red de compras | Compras estándar | Compra de productos (tipo creativo &quot;Product&quot;) | Automático mediante API | La copia de anuncio se genera automáticamente para los grupos de productos en el grupo de anuncios. Editar solo el estado del anuncio mediante [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)<br><br>Puede crear las campañas principales, los grupos de publicidad y los grupos de productos, y editar solo su estado mediante [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md). | Sí, cuando agrega manualmente etiquetas de rastreo de clics a plantillas de seguimiento dentro de la red de publicidad | Sí | Datos de nivel de campaña, grupo de anuncios y grupo de productos [!DNL Google Ads] no proporciona datos de rendimiento de nivel de anuncio para campañas de compra. | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de campaña, grupo de anuncios y grupo de productos de Search, Social y Commerce a Analytics |
|  | [!DNL YouTube] | Vídeo | Vídeo | Requiere [adhesión](/help/search-social-commerce/tools/sync-inventory.md); solo a través de API Detalles básicos de publicidad, sin miniaturas | — | Sí, cuando agrega manualmente etiquetas de rastreo de clics a plantillas de seguimiento dentro de la red de publicidad | Campañas con [!UICONTROL Maximize Conversions] estrategia de oferta solo en portafolios híbridos El portafolio híbrido solo debe incluir [!DNL YouTube] campañas. | Datos de nivel de campaña y de grupo de publicidad<br><br>La red de anuncios no proporciona datos de nivel de anuncio. | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de campaña y de grupo de publicidad de Search, Social y Commerce a Analytics |
| [!DNL Microsoft Advertising] | Audience Network | Tipos de campañas de audiencia:<br><br>&quot;Audience (image)&quot; y &quot;Audience (feed)&quot;) | Adaptable<br><br>Incluye anuncios basados en imágenes y anuncios basados en fuentes de productos solo para la red de audiencias | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) y [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí | Sí para campañas CPC (eCPC) mejoradas<br><br>No disponible para campañas CPM | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Audience Network | Buscar | Anuncios de texto expandidos con &quot;[!DNL Prefer Audience Ad Format]&quot; seleccionado | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md)<br><br>No es compatible con extensiones de anuncios de imágenes | Sí | Sí | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Buscar | \[Expandida\] Búsqueda dinámica | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) y [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí | Sí | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Buscar | Texto ampliado (obsoleto en febrero de 2023) | Automático mediante API | Editar estado solo para anuncios existentes utilizando [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) | Sí | Sí | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Buscar | Multimedia | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md). Edite la compatibilidad también para estados y direcciones URL solo en [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí | Sí | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Buscar | Búsqueda interactiva | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) | Sí | Sí | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Buscar | Texto estándar (obsoleto en 2017) | Automático mediante API | Editar solo usando [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) y [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí | Sí | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Búsqueda estándar | <i>Extensión de anuncio:</i><br><br>Vínculo de sitio (nivel de campaña) | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) y [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | —<br><br>Los vínculos de sitio de nivel de campaña tienen un carácter &quot;[!UICONTROL Tracking Template]&quot;, pero los mapas de búsqueda, medios sociales y comercio asignan clics y conversiones resultantes a la palabra clave asociada, no al vínculo de sitio individual. | —<br><br>Search, Social y Commerce no optimizan el vínculo del sitio. En su lugar, se optimiza según la palabra clave asociada con el anuncio en el que se incluye el vínculo de sitio. | —<br><br>Están disponibles los datos de la palabra clave asociada. Para datos de rendimiento de nivel de vínculo de sitio, utilice [!DNL Microsoft Advertising] editor de anuncios.<br><br>Para ver qué conversiones individuales resultaron de un clic en un vínculo a un sitio, genere un [Informe de transacciones](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)Informe. El [!UICONTROL Link Type] la columna para un vínculo de sitio es sl:&lt;sitelink text=&quot;&quot;></code>, como sl:Consulte Ofertas actuales. | Datos solo para la palabra clave asociada de Search, Social y Commerce a Analytics |
|  | Red de compras | Compras estándar | Product | Automático mediante API | Solo líneas de promoción que utilizan [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md) y [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md); los anuncios se generan automáticamente. Puede crear la campaña principal, el grupo de publicidad y los grupos de productos mediante [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md). | Sí, cuando agrega manualmente etiquetas de rastreo de clics a plantillas de seguimiento dentro de la red de publicidad | Sí | Datos de nivel de anuncio<br><br>Para ver qué conversiones individuales resultaron de un clic en un anuncio de compra, genere un [Informe de transacciones](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md); el [!UICONTROL Link Type] La columna para una lista de productos es `pla:&lt;product ID&gt;`, como play:8525822. | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Compras: compras inteligentes | Compras inteligentes (función beta en Search, Social y Commerce) | Product | Automático mediante API de forma predeterminada, pero se puede [excluido](/help/search-social-commerce/tools/sync-inventory.md) | — | Sí, cuando agrega manualmente etiquetas de rastreo de clics a plantillas de seguimiento dentro de la red de publicidad | Buscar campañas con [!UICONTROL Maximize Conversion Value] y [!UICONTROL tROAS] estrategias de oferta solo en portafolios híbridos<br><br>El objetivo solo debe incluir [!DNL Adobe] y debe habilitar la carga de los objetivos de Search, Social y Commerce en [!DNL Microsoft Advertising]. | Datos de nivel de anuncio<br><br>Para ver qué conversiones individuales resultaron de un clic en un anuncio de compra, genere un [Informe de transacciones](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md); el [!UICONTROL Link Type] La columna para una lista de productos es `pla:&lt;product ID&gt;`, como play:8525822. | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
| [!DNL Naver] | Buscar red | Sitio web | Texto | —<br><br>No hay sincronización, pero puede replicar manualmente la estructura de cuentas y cargar las métricas de tráfico diarias para la creación de informes y la atribución de conversión<br><br>Consulte &quot;[Implementación [!DNL Naver] cuentas solo de seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot; | —<br><br>Puede replicar o editar manualmente la estructura de la cuenta mediante [plantillas de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md). | Sí, cuando agrega etiquetas de rastreo de clics a la configuración de palabras clave dentro de la red de anuncios | —<br><br>Sin pujas | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce, pero no viceversa |
| [!DNL Pinterest] (La compatibilidad de sincronización finalizó en 2022) | Buscar red | Campañas de tráfico solo con ubicaciones de búsqueda y grupos de anuncios con segmentación por palabras clave | Pin promocionado | —<br><br>La información de la cuenta heredada hasta el 21 de julio de 2022 está disponible como solo lectura. | — | — | — | Las impresiones y clics heredados a nivel de anuncio solo de Pinterest, pero sin ingresos, se sincronizaron hasta el 21 de julio de 2022. | Datos de Analytics para Search, Social y Commerce, pero no viceversa |
| [!DNL Yahoo! Display Network] | Mostrar red | Mostrar | Titular, imagen interactiva | Automático mediante API, pero de solo lectura | — | Sí, cuando agrega manualmente etiquetas de rastreo de clics a plantillas de seguimiento dentro de la red de publicidad | Campañas con [!UICONTROL Manual CPC] solo estrategia de oferta<br><br>La misma oferta se aplica a todos los anuncios de un grupo de anuncios. | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Buscar | Texto (largo y corto) | Automático mediante API | — | Sí, cuando agrega manualmente etiquetas de rastreo de clics a plantillas de seguimiento dentro de la red de publicidad | Campañas solo con estrategia de oferta de CPC manual<br><br>La misma oferta se aplica a todos los anuncios de un grupo de anuncios. | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
| [!DNL Yahoo! Japan Ads] | Buscar red | Búsqueda patrocinada | Texto extendido<br><br>(Solo anuncios heredados; obsoleto en septiembre de 2022 en lugar de la búsqueda adaptable) | Automático mediante API | Eliminar solo mediante [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) | Sí | Campañas con [!UICONTROL Manual CPC] solo estrategia de oferta | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Búsqueda patrocinada | Búsqueda interactiva | Automático mediante API | — | Sí, cuando agrega manualmente etiquetas de rastreo de clics dentro de la red de publicidad | Campañas con [!UICONTROL Manual CPC] solo estrategia de oferta | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Buscar red | Búsqueda patrocinada | Anuncios de texto estándar (obsoletos en 2017) | Automático mediante API | Eliminar solo mediante [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) | Sí | Campañas con [!UICONTROL Manual CPC] solo estrategia de oferta | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
| [!DNL Yahoo Native] (La compatibilidad de sincronización finalizó en 2022) | Red nativa | Nativo | Texto | —<br><br>La información de la cuenta heredada hasta el 10 de marzo de 2022 está disponible como de solo lectura. | — | — | — | —<br><br>Datos de nivel de anuncio heredados que se sincronizaron hasta el 10 de marzo de 2022. | Datos de Analytics para Search, Social y Commerce, pero no viceversa |
| [!DNL Yandex] | Buscar red | Buscar | Texto | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) | Sí | Campañas solo con estrategia de oferta de CPC | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |
|  | Mostrar red | Visualización/Contenido | Texto | Automático mediante API | Uso de [vistas de administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-management-options.md), [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), y [fuentes de administración de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) | Sí | Campañas solo con estrategia de oferta de CPC | Datos de nivel de anuncio | Datos de Analytics para Search, Social y Commerce<br><br>Datos de nivel de anuncio de Search, Social y Commerce a Analytics |

<table style="table-layout:auto">

[^1]: Para la mayoría de las redes de anuncios y tipos de campañas, al habilitar la opción &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot; configuración de seguimiento para una campaña activa (ya sea establecida en el nivel de campaña o heredada de la configuración de la cuenta), Search, Social y Commerce crea y carga automáticamente direcciones URL de seguimiento para los componentes del grupo de anuncios en la red de anuncios cada vez que se sincroniza con ella. De lo contrario, debe generar direcciones URL de seguimiento y agregarlas a la configuración de la cuenta, la campaña o el componente de campaña. Consulte &quot;[Cuándo y cómo generar URL de seguimiento de clics por red de anuncios y objeto](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

[^2]: consulte &quot;Tipos de portafolios aptos por estrategia de oferta de campaña&quot; en la Guía de optimización, disponible en Buscar, Social y Comercio.

[^3]: Requiere una integración con Adobe Analytics. Consulte &quot;[Descripción general de Analytics para publicidad en Adobe](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html).&quot;

[^4]: [!DNL Analytics] Los datos de se envían a Search, Social y Commerce mediante el parámetro de seguimiento s_kwcid actualizado, independientemente del formato s_kwcid que utilice normalmente para la cuenta. Si normalmente utiliza la versión anterior de s_kwcid, le recomendamos actualizar al nuevo formato s_kwcid para disfrutar de la mejor experiencia. Sin embargo, aunque los datos de clics/costes y los datos de ingresos se rastreen con s_kwcids diferentes, ambos conjuntos de datos se clasifican y agregan completamente en la misma campaña y cuenta.