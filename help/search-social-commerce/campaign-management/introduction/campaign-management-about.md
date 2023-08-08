---
title: Acerca de la administración de campañas en Search, Social y Commerce
description: Obtenga información acerca de las funciones de administración de campañas en Search, Social y Commerce.
exl-id: e6fca48d-1f6c-4d36-a10d-e1a5db859a37
feature: Search Campaign Management
source-git-commit: d23b5a3c56c35fc5abbeafde681b9f584bf1c905
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Acerca de la administración de campañas en Search, Social y Commerce

Search, Social y Commerce le permite realizar un seguimiento o administrar sus campañas de búsqueda, visualización/contenido, medios sociales, compras, audiencia y rendimiento máximo en un solo lugar. Según la red de publicidad y el tipo de campaña, las funciones disponibles pueden incluir la sincronización con las redes de publicidad, las capacidades de creación y edición, el seguimiento y la atribución de conversión, la creación de informes y la optimización de ofertas y presupuestos. Para obtener más información sobre las funciones disponibles para cada red de publicidad, consulte[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

A medida que agrega y edita datos de campaña en la [!UICONTROL Campaigns] Vistas de, Búsqueda, Social y Comercio insertan inmediatamente los cambios de datos en la red de anuncios. Search, Social y Commerce también extrae datos de estructura de campañas y datos de clics de cuentas de red de anuncios sincronizadas una vez al día (o con más frecuencia cuando se detectan nuevas campañas) y bajo demanda según se solicita.

## Configuración del acceso a las cuentas de red de publicidad

Para realizar un seguimiento del rendimiento de los anuncios en la cuenta de red de anuncios de un anunciante (y para realizar posibles pujas por los anuncios), el equipo de cuenta de Adobe [crea un registro de cuenta correspondiente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) en Search, Social y Commerce. El registro de cuenta incluye opciones de seguimiento.

En el caso de las cuentas sincronizadas mediante la API de la red de publicidad, el registro de cuentas también incluye las credenciales de acceso a la cuenta. Una vez habilitada la cuenta, los datos de la cuenta se extraen de con la red de publicidad. A continuación, puede ver los datos de cuenta existentes, así como crear y editar la estructura de campañas y los datos de publicidad.

## Rastreo de clics para enlazar los clics con las conversiones

Si utiliza el servicio de seguimiento de conversión de Adobe Advertising, debe incluir el código de seguimiento de clics de Search, Social y Commerce en el sufijo de la página de aterrizaje, en las plantillas de seguimiento y en las URL de destino/final para anuncios, palabras clave y ubicaciones, vínculos de sitios y listas de productos. Para [redes de anuncios compatibles y tipos de campañas](/help/search-social-commerce/introduction/supported-inventory.md) cuya configuración de campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload],&quot; Search, Social y Commerce anexa automáticamente su propio código de seguimiento y redirección al guardar el registro, por lo que no es necesario agregarlo manualmente. De lo contrario, debe agregar manualmente el código a las plantillas de seguimiento o a las direcciones URL finales.

Para obtener más información sobre el seguimiento, consulte el capítulo sobre seguimiento.

## Automatización de la gestión de pujas y presupuestos

Para [redes de anuncios compatibles y tipos de campañas](/help/search-social-commerce/introduction/supported-inventory.md), puede agrupar sus campañas en portafolios, cada uno con un objetivo comercial específico y un presupuesto o objetivo de rendimiento específico. En portafolios estándar, Search, Social y Commerce optimiza las ofertas de palabras clave CPC y los presupuestos de campaña. Los portafolios híbridos combinan tecnologías de optimización de Search, Social y Commerce con las redes de anuncios.

Para obtener más información sobre las opciones de portafolio disponibles y cómo configurarlas, consulte el capítulo Guía de optimización sobre &quot;Portfolio&quot;, que está disponible en Search, Social y Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Las vistas de administración de campañas

Las vistas de administración de campañas le permiten supervisar y administrar sus cuentas de búsqueda. Estas son las opciones disponibles:

* **[!UICONTROL Campaigns]** — El [!UICONTROL Campaigns] las vistas muestran datos de cada cuenta conectada a ad network. Puede ver datos de costes, clics, impresiones e ingresos de todas las cuentas de red de publicidad y de cuentas, campañas, grupos de publicidad, palabras clave, anuncios, grupos de productos de compras, ubicaciones, destinos automáticos (destinos de búsqueda dinámica), audiencias y bibliotecas de extensión de publicidad, así como sus entidades de cuenta asociadas. Para [tipos de campaña admitidos en redes de publicidad admitidas](/help/search-social-commerce/introduction/supported-inventory.md), puede crear y editar datos para campañas individuales y componentes de campaña directamente en la interfaz. Si lo desea, puede exportar los datos de la mayoría de las subvistas a un archivo de hoja de cálculo.

  >[!NOTE]
  >
  >Los datos de nivel de anuncio no están disponibles para [!DNL Google Ads] anuncio de búsqueda dinámica (DSA), rendimiento máximo, compras inteligentes y [!DNL YouTube] campañas.

* **[!UICONTROL Products]** — El [!UICONTROL Products] vistas mostrar datos de cada [[!DNL Google] or [!DNL Microsoft] cuenta del centro de comerciantes sincronizada](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). El valor predeterminado [!UICONTROL Accounts] la subvista enumera todas las cuentas sincronizadas; algunos tipos de usuarios pueden agregar nuevas cuentas desde esta vista. El [!UICONTROL Products] la subvista enumera cada producto dentro de la cuenta.

* **[!UICONTROL Advanced (ACM)]** — Desde el [!DNL Advanced] ([!DNL AMC], para la vista Avanzada (Campaign Management) , puede configurar procesos automatizados para crear [anuncios dinámicos y palabras clave dirigidos a cada elemento del inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) según una plantilla de publicidad específica de la red de publicidad que cree y el contenido de [!DNL Google Merchant Center] cuentas o archivos de datos de inventario que se cargan en una ubicación FTP. Las subvistas muestran detalles sobre cada plantilla de fuente del anunciante y cada campaña, grupo de anuncios, palabra clave y anuncio incluido en una fuente que se propagó a través de una plantilla de fuente pero no se publicó en la red de anuncios.

* **[!UICONTROL Bulksheets]** — Utilice el [!UICONTROL Bulksheets] vista para crear [archivos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) que contenga tantos datos como desee para una cuenta de un [red de publicidad admitida](/help/search-social-commerce/introduction/supported-inventory.md)y, a continuación, publíquelas en la red publicitaria.

* **[!UICONTROL Audiences]** — [El [!UICONTROL Audiences] vistas](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) enumera todas las [!DNL Google Ads] y [!DNL Microsoft Advertising] audiencias generadas a partir de varios tipos de listas de usuarios. Puede crear [!DNL Google Ads] audiencias de audiencias de Adobe Experience Cloud existentes y listas de correo electrónico de clientes. También puede ver y administrar los objetivos y las exclusiones de audiencia de su [!DNL Google Ads] y [!DNL Microsoft Advertising] anuncios.

* **[!UICONTROL Label Classifications]** — Utilice esta vista para crear y eliminar [clasificaciones de etiquetas](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), que puede ayudarle a agrupar sus etiquetas en conjuntos significativos.

>[!MORELIKETHIS]
>
>* [Información general sobre la implementación de cuentas y campañas de red de publicidad](campaign-implemention-overview.md)
>* [Monitorizar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)
>* [Datos de conversión de Google Ads en Search, Social y Commerce](google-conversion-data.md)
