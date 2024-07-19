---
title: Información general sobre la implementación de cuentas y campañas de red de publicidad
description: Obtenga información acerca de las tareas relacionadas con la configuración, sincronización y administración de las cuentas de red de anuncios.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# Información general sobre la implementación de cuentas y campañas de red de publicidad

Adobe trabaja con cada anunciante para configurar sus cuentas y campañas de red de anuncios. Esto incluye configurar Search, Social y Commerce para conectarse y sincronizar con las cuentas del anunciante, crear nuevas campañas y componentes de campaña según sea necesario, configurar el seguimiento de los anuncios de componentes, añadir opcionalmente las campañas a portafolios para permitir que Search, Social y Commerce optimicen las ofertas en los anuncios y validar los datos iniciales de coste, clics e ingresos.

Después de activar una campaña y, opcionalmente, agregarla a un portafolio, el equipo de administración de cuentas de Adobe, el equipo de la agencia o el anunciante (según los términos del acuerdo de nivel de servicio) deberán supervisar cada campaña y cambiar los componentes y la configuración relevantes según sea necesario para cumplir los objetivos del anunciante.

Esta página incluye información sobre todos los tipos de cuenta, incluido cómo configurar la estructura de campaña para las cuentas sincronizadas. Para obtener instrucciones adicionales sobre la configuración de cuentas de solo seguimiento para [!DNL Naver], consulte &quot;[Implementar [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)&quot;.

## Tareas de configuración iniciales para cuentas y campañas

[!DNL Adobe] y/o su agencia trabajarán con usted para hacer lo siguiente:

1. (Nuevas cuentas de anunciante) Configurar cuentas administrativas:

   1. Configure la cuenta del anunciante.

   1. (Si es necesario) Cree cuentas de usuario para que el anunciante vea y administre sus datos de campaña y genere informes.

1. (Algunas redes de anuncios) Obtenga autorización para que Search, Social y Commerce accedan a cada cuenta mediante la API de la red de anuncios y la interfaz de usuario de Search, Social y Commerce.

1. Para cada cuenta de red de publicidad:

   1. (Si es necesario) Configure la cuenta en la red de anuncios.

   1. Integre con la cuenta [creando un registro de cuenta correspondiente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) en Search, Social y Commerce que contenga las credenciales de acceso a la cuenta y las opciones de seguimiento, y establezca el estado de la cuenta como habilitado.

      A continuación, Search, Social y Commerce se sincronizan con la red de publicidad. Si la cuenta ya contiene datos de campaña, estarán disponibles en unas 24 horas.

   1. ([Tipos de anuncio que puede crear o editar](/help/search-social-commerce/introduction/supported-inventory.md) en Search, Social y Commerce) Si la cuenta aún no contiene datos de campaña, cree la estructura de campaña y los componentes de campaña desde Search, Social y Commerce mediante cualquiera de los siguientes métodos disponibles para el tipo de anuncio:

      * (Google Ads, Microsoft Advertising, Yahoo! Sólo anuncios y cuentas de Yandex) Configure un [proceso automatizado para crear palabras clave y anuncios dinámicos dirigidos a cada elemento del inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) según la plantilla de anuncio específica de la red de anuncios que cree y el contenido de los archivos de datos de inventario que cargue en una ubicación FTP.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Solo cuentas de Japan Ads y Yandex) Cargue [archivos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) que contengan tantos datos como desee para una cuenta y, a continuación, publíquelos en las redes de anuncios.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads y solo cuentas de Yandex) Introduzca datos de componentes individuales directamente en la interfaz. Para la mayoría de las campañas y tipos de publicidad, puede crear datos en los niveles de campaña, grupo de publicidad y palabra clave, ubicación y nivel de publicidad individuales.

      Sin embargo, algunos tipos de campañas y anuncios requieren flujos de trabajo únicos. Vea las instrucciones para configurar [[!DNL Microsoft Advertising] campañas de compras](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md), [[!DNL Google Ads] anuncios dinámicos de búsqueda](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md), [[!DNL Google Ads] campañas de rendimiento máximo](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md) y [[!DNL Google Ads] campañas de compras](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] solo cuentas de solo seguimiento) Cargue [archivos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) con datos para replicar las campañas, los grupos de anuncios y las palabras clave existentes en Search, Social y Commerce sin publicarlos en [!DNL Naver].

1. Configure el seguimiento de todos los anuncios para los que el Adobe Advertising realizará un seguimiento de las conversiones:

   1. (Anunciantes con el servicio de seguimiento de conversión de Adobes Advertising) Si es necesario, [configure el rastreo de clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) para las publicidades y, opcionalmente, para las palabras clave, las ubicaciones y las extensiones de publicidad mediante la generación y carga de direcciones URL de rastreo de clics de Search, Social y Commerce.

      Para [!DNL Google Ads] campañas con rendimiento máximo, configure todo el seguimiento en la [configuración de seguimiento de la campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Para las campañas solo de seguimiento, debe generar direcciones URL de destino mediante hojas de edición por lotes y, a continuación, añadir las direcciones URL de destino generadas a las entidades relevantes mediante el editor nativo de la red de publicidad.

   1. Configure el seguimiento de conversiones. Según la implementación, esto puede implicar la adición de etiquetas de seguimiento de conversión a las páginas web del anunciante o la configuración de una entrega diaria de fuentes para los datos de conversión que el anunciante haya recopilado por separado.

      Si usa el servicio de seguimiento de conversión de Adobe Advertising, puede generar las etiquetas de seguimiento de conversión [en Search, Social y Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md) o [mediante Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. Valide los datos de los que se realiza un seguimiento.

   Para obtener más información sobre la configuración del seguimiento, consulte el capítulo sobre seguimiento.

1. (Anunciantes con Adobe Analytics) [Integrar Adobe Advertising y Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) para que puedan intercambiar datos.

1. (Para permitir que Search, Social y Commerce optimicen ofertas o presupuestos de campaña; [solo tipos de campaña admitidos](/help/search-social-commerce/introduction/supported-inventory.md)) [Asigne la campaña a un portafolio](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Si el portafolio aún no se ha iniciado (optimizando ofertas o presupuestos), deje que la capacidad de optimización recopile datos suficientes para poder crear modelos de costes e ingresos que le permitan establecer el rendimiento de línea de base del portafolio antes de iniciarlo.

   Si el portafolio ya se ha lanzado, habilite el aprendizaje para el portafolio. Para obtener más información, consulte &quot;Ajuste de las estrategias del portafolio&quot;. Debería esperar que el portafolio sea volátil después de agregar nuevas campañas, mientras que la capacidad de optimización recopila datos sobre las unidades de oferta de la campaña. Las pujas se ajustan automáticamente en un plazo de una a tres semanas.

   Para obtener más información acerca de los portafolios, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (Si se realizará el seguimiento de las nuevas conversiones para el anunciante) [Ponga las conversiones a disposición](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) de los informes, las vistas de administración de campañas y los objetivos del portafolio.

1. Para cada campaña, compruebe que Search, Social y Commerce están recibiendo datos de clics y costes de la red de anuncios y valide los datos de ingresos que se muestran en Search, Social y Commerce con los datos de ingresos propios del anunciante.

1. (Opcional) Automatice la creación de informes configurando plantillas de informes, fuentes de hojas de cálculo y el envío por FTP de informes programados.

   Para obtener instrucciones, consulte el capítulo sobre Informes.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de campañas en Search, Social y Commerce](campaign-management-about.md)
>* [Supervisar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)
>* [Datos de conversión de Google Ads en Search, Social y Commerce](google-conversion-data.md)
>* [Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)
