---
title: Acerca de la administración de campañas en Search, Social y Commerce
description: Obtenga información acerca de las funciones de administración de campañas en Search, Social y Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Acerca de la administración de campañas en Search, Social y Commerce

Search, Social y Commerce le permiten rastrear o administrar sus campañas de búsqueda, visualización/contenido, medios sociales, compras, audiencia y rendimiento máximo en un solo lugar. Según la red de publicidad y el tipo de campaña, las funciones disponibles pueden incluir la sincronización con las redes de publicidad, las capacidades de creación y edición, el seguimiento y la atribución de conversión, la creación de informes y la optimización de ofertas y presupuestos. Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

A medida que agrega y edita datos de campaña en las vistas [!UICONTROL Campaigns], Search, Social y Commerce insertan inmediatamente los cambios de datos en la red publicitaria. Search, Social y Commerce también extrae datos de estructura de campañas y datos de clics de cuentas de red de anuncios sincronizadas una vez al día (o con más frecuencia cuando se detectan nuevas campañas) y bajo demanda según se solicita.

## Configuración del acceso a las cuentas de red de publicidad

Para realizar un seguimiento del rendimiento de los anuncios en la cuenta de red de anuncios de un anunciante (y para realizar posibles pujas por los anuncios), el equipo de cuenta de Adobe [crea un registro de cuenta correspondiente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) en Search, Social y Commerce. El registro de cuenta incluye opciones de seguimiento.

En el caso de las cuentas sincronizadas mediante la API de la red de publicidad, el registro de cuentas también incluye las credenciales de acceso a la cuenta. Una vez habilitada la cuenta, los datos de la cuenta se extraen de con la red de publicidad. A continuación, puede ver los datos de cuenta existentes, así como crear y editar la estructura de campañas y los datos de publicidad.

## Rastreo de clics para enlazar los clics con las conversiones

Si utiliza el servicio de seguimiento de conversión de Adobe Advertising, debe incluir el código de seguimiento de clics de Search, Social y Commerce en el sufijo de la página de aterrizaje, en las plantillas de seguimiento y en las direcciones URL de destino final para anuncios, palabras clave y ubicaciones, vínculos de sitios y listas de productos. Para [redes de anuncios compatibles y tipos de campañas](/help/search-social-commerce/introduction/supported-inventory.md) cuya configuración de campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce anexa automáticamente su propio código de redirección y seguimiento al guardar el registro, por lo que no es necesario agregarlo manualmente. De lo contrario, debe agregar manualmente el código a las plantillas de seguimiento o a las direcciones URL finales.

Para obtener más información sobre el seguimiento, consulte el capítulo sobre seguimiento.

## Automatización de la gestión de pujas y presupuestos

Para [redes de anuncios compatibles y tipos de campañas](/help/search-social-commerce/introduction/supported-inventory.md), puede agrupar sus campañas en portafolios, cada uno con un objetivo comercial específico y un presupuesto o un objetivo de rendimiento específico. En portafolios estándar, Search, Social y Commerce optimizan las ofertas de palabras clave CPC y los presupuestos de campaña. Los portafolios híbridos combinan tecnologías de optimización de Search, Social y Commerce con las redes de anuncios.

Para obtener más información sobre las opciones de portafolio disponibles y cómo configurarlas, consulte el capítulo Guía de optimización sobre &quot;Portfolio&quot;, que está disponible en Search, Social y Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Las vistas de administración de campañas

Las vistas de administración de campañas le permiten supervisar y administrar sus cuentas de búsqueda. Estas son las opciones disponibles:

* **[!UICONTROL Campaigns]** — Las vistas [!UICONTROL Campaigns] muestran datos de cada cuenta conectada y de red. Puede ver datos de costes, clics, impresiones e ingresos de todas las cuentas de red de publicidad y de cuentas, campañas, grupos de publicidad, palabras clave, anuncios, grupos de productos de compras, ubicaciones, destinos automáticos (destinos de búsqueda dinámica), audiencias y bibliotecas de extensión de publicidad, así como sus entidades de cuenta asociadas. Para [tipos de campañas compatibles en redes de anuncios compatibles](/help/search-social-commerce/introduction/supported-inventory.md), puede crear y editar datos para campañas individuales y componentes de campaña directamente en la interfaz. Si lo desea, puede exportar los datos de la mayoría de las subvistas a un archivo de hoja de cálculo.

  >[!NOTE]
  >
  >Los datos de nivel de anuncio no están disponibles para [!DNL Google Ads] publicidad de búsqueda dinámica (DSA), rendimiento máximo, compras inteligentes y [!DNL YouTube] campañas.

* **[!UICONTROL Products]** — Las vistas [!UICONTROL Products] muestran datos para cada [[!DNL Google] o [!DNL Microsoft] cuenta de centro comercial sincronizada](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). La subvista predeterminada [!UICONTROL Accounts] enumera todas las cuentas sincronizadas; algunos tipos de usuarios pueden agregar nuevas cuentas desde esta vista. La subvista [!UICONTROL Products] enumera cada producto dentro de la cuenta.

* **[!UICONTROL Advanced (ACM)]**: desde la vista [!DNL Advanced] ([!DNL AMC], para Advanced Campaign Management), puede configurar procesos automatizados para crear [anuncios dinámicos y palabras clave dirigidos a cada elemento del inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) según una plantilla de anuncio específica de la red de anuncios que cree y el contenido de [!DNL Google Merchant Center] cuentas o archivos de datos de inventario que cargue en una ubicación FTP. Las subvistas muestran detalles sobre cada plantilla de fuente del anunciante y cada campaña, grupo de anuncios, palabra clave y anuncio incluido en una fuente que se propagó a través de una plantilla de fuente pero no se publicó en la red de anuncios.

* **[!UICONTROL Bulksheets]**: use la vista [!UICONTROL Bulksheets] para crear [archivos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) que contengan tantos datos como desee para una cuenta en una red de publicidad admitida [y, a continuación, publíquelos en la red de publicidad.](/help/search-social-commerce/introduction/supported-inventory.md)

* **[!UICONTROL Audiences]** — [Las vistas [!UICONTROL Audiences]](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) enumeran todas sus audiencias de [!DNL Google Ads] y [!DNL Microsoft Advertising] generadas a partir de varios tipos de listas de usuarios. Puede crear [!DNL Google Ads] audiencias a partir de las audiencias de Adobe Experience Cloud existentes y las listas de correo electrónico de los clientes. También puede ver y administrar destinos y exclusiones de audiencia para sus anuncios de [!DNL Google Ads] y [!DNL Microsoft Advertising].

* **[!UICONTROL Label Classifications]** — Use esta vista para crear y eliminar [clasificaciones de etiquetas](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), que pueden ayudarle a agrupar las etiquetas en conjuntos significativos.

>[!MORELIKETHIS]
>
>* [Información general sobre la implementación de cuentas y campañas de red de anuncios](campaign-implemention-overview.md)
>* [Supervisar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)
>* [Datos de conversión de Google Ads en Search, Social y Commerce](google-conversion-data.md)
