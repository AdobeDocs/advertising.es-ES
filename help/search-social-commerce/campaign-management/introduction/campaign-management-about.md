---
title: Acerca de la administración de campañas en Search, Social y Commerce
description: Obtenga información acerca de las funciones de administración de campañas en Search, Social y Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tgoMzw4DbEY5evC2s1f6mQHfJYYb7DJzMfFUnc-06Bk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 808
ht-degree: 0%

---

# Acerca de la administración de campañas en Search, Social y Commerce

Search, Social y Commerce le permiten rastrear o administrar sus campañas de búsqueda, visualización/contenido, medios sociales, compras, audiencia y rendimiento máximo en un solo lugar. Según la red de publicidad y el tipo de campaña, las funciones disponibles pueden incluir la sincronización con las redes de publicidad, las capacidades de creación y edición, el seguimiento y la atribución de conversión, la creación de informes y la optimización de ofertas y presupuestos. Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

A medida que agrega y edita datos de campaña en las vistas [!UICONTROL Campaigns], Search, Social y Commerce insertan inmediatamente los cambios de datos en la red publicitaria. Search, Social y Commerce también extrae datos de estructura de campañas y datos de clics de cuentas de red de anuncios sincronizadas una vez al día (o con más frecuencia cuando se detectan nuevas campañas) y bajo demanda según se solicita.

## Configuración del acceso a las cuentas de red de publicidad

Para realizar un seguimiento del rendimiento de los anuncios en la cuenta de red de anuncios de un anunciante (y para realizar posibles pujas por los anuncios), el equipo de cuenta de Adobe [crea un registro de cuenta correspondiente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) en Search, Social y Commerce. El registro de cuenta incluye opciones de seguimiento.

En el caso de las cuentas sincronizadas mediante la API de la red de publicidad, el registro de cuentas también incluye las credenciales de acceso a la cuenta. Una vez habilitada la cuenta, los datos de la cuenta se extraen de con la red de publicidad. A continuación, puede ver los datos de cuenta existentes, así como crear y editar la estructura de campañas y los datos de publicidad.

## Rastreo de clics para enlazar los clics con las conversiones

Si utiliza el servicio de seguimiento de conversión de Adobe Advertising, debe incluir el código de seguimiento de clics de Search, Social y Commerce en el sufijo de la página de aterrizaje, en las plantillas de seguimiento y en las URL de destino/final para anuncios, palabras clave y ubicaciones, vínculos de sitios y listas de productos. Para [redes de anuncios compatibles y tipos de campañas](/help/search-social-commerce/introduction/supported-inventory.md) cuya configuración de campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce anexa automáticamente su propio código de redirección y seguimiento al guardar el registro, por lo que no es necesario agregarlo manualmente. De lo contrario, debe agregar manualmente el código a las plantillas de seguimiento o a las direcciones URL finales.

Para obtener más información sobre el seguimiento, consulte el capítulo sobre seguimiento.

## Automatización de la gestión de pujas y presupuestos

Para [redes de anuncios compatibles y tipos de campañas](/help/search-social-commerce/introduction/supported-inventory.md), puede agrupar sus campañas en portafolios, cada uno con un objetivo comercial específico y un presupuesto o un objetivo de rendimiento específico. En portafolios estándar, Search, Social y Commerce optimizan las ofertas de palabras clave CPC y los presupuestos de campaña. Los portafolios híbridos combinan tecnologías de optimización de Search, Social y Commerce con las redes de anuncios.

Para obtener más información acerca de las opciones de portafolios disponibles y cómo configurarlos, consulte el capítulo Guía de optimización sobre &quot;Portafolios&quot;, que está disponible en Search, Social y Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Las vistas de administración de campañas

The campaign management views allow you to monitor and manage your search accounts. The following views are available:

* **[!UICONTROL Campaigns]** — The [!UICONTROL Campaigns] views show data from each connected ad network account. You can view cost, click, impression, and revenue data across all ad network accounts and across individual accounts, campaigns, ad groups, keywords, ads, shopping product groups, placements, auto targets (dynamic search targets), audiences, and ad extension libraries and their associated account entities. For [supported campaign types on supported ad networks](/help/search-social-commerce/introduction/supported-inventory.md), you can create and edit data for individual campaigns and campaign components directly in the interface. You can optionally export the data in most subviews to a spreadsheet file.

  >[!NOTE]
  >
  >Ad-level data isn&#39;t available for [!DNL Google Ads] dynamic search ad (DSA), performance max, smart shopping, and [!DNL YouTube] campaigns.

* **[!UICONTROL Products]** — The [!UICONTROL Products] views show data for each [[!DNL Google] or [!DNL Microsoft] merchant center account that&#39;s synced](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). The default [!UICONTROL Accounts] subview lists all synced accounts; some user types can add new accounts from this view. The [!UICONTROL Products] subview lists each product within the account.

* **[!UICONTROL Advanced (ACM)]** —  From the [!DNL Advanced] ([!DNL AMC], for Advanced Campaign Management) view, you can set up automated processes to create [dynamic ads and keywords targeted to each item in your inventory](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) according to an ad network-specific ad template you create and the contents of [!DNL Google Merchant Center] accounts or inventory data files you upload to an FTP location. Subviews show details about each feed template for the advertiser and each campaign, ad group, keyword, and ad included in a feed that was propagated through a feed template but not posted to the ad network.

* **[!UICONTROL Bulksheets]** — Use the [!UICONTROL Bulksheets] view to create [bulksheet files](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) containing as much data as you want for an account on a [supported ad network](/help/search-social-commerce/introduction/supported-inventory.md), and then post them to the ad network.

* **[!UICONTROL Audiences]** — [The [!UICONTROL Audiences] views](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) lists all of your [!DNL Google Ads] and [!DNL Microsoft Advertising] audiences generated from various types of user lists. You can create [!DNL Google Ads] audiences from your existing Adobe CX Enterprise audiences and your customer email lists. You can also view and manage audience targets and exclusions for your [!DNL Google Ads] and [!DNL Microsoft Advertising] ads.

* **[!UICONTROL Label Classifications]** — Use this view to create and delete [label classifications](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), which can help you group your labels into meaningful sets.

>[!MORELIKETHIS]
>
>* [Overview of implementing ad network accounts and campaigns](campaign-implemention-overview.md)
>* [Monitor and manage the performance of your ad network campaigns](monitor-performance-campaigns.md)
>* [Google Ads conversion data in Search, Social, &amp; Commerce](google-conversion-data.md)
