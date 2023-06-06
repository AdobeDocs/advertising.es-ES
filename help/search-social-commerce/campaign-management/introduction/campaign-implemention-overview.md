---
title: Información general sobre la implementación de cuentas y campañas de red de publicidad
description: Obtenga información acerca de las tareas relacionadas con la configuración, sincronización y administración de las cuentas de red de anuncios.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Información general sobre la implementación de cuentas y campañas de red de publicidad

Adobe trabaja con cada anunciante para configurar sus cuentas y campañas de red de anuncios. Esto incluye configurar Search, Social y Commerce para conectarse y sincronizarse con las cuentas del anunciante, crear nuevas campañas y componentes de campaña según sea necesario, configurar el seguimiento de los anuncios de componentes, añadir opcionalmente las campañas a portafolios para permitir que Search, Social y Commerce optimicen las ofertas en los anuncios y validar los datos iniciales de coste, clics e ingresos.

Después de activar una campaña y, opcionalmente, agregarla a un portafolio, el equipo de administración de cuentas de Adobe, el equipo de la agencia o el anunciante (según los términos del acuerdo de nivel de servicio) deberán supervisar cada campaña y cambiar los componentes y la configuración relevantes según sea necesario para cumplir los objetivos del anunciante.

Esta página incluye información sobre todos los tipos de cuenta, incluido cómo configurar la estructura de campaña para las cuentas sincronizadas. Para obtener instrucciones adicionales sobre la configuración de cuentas de solo seguimiento para [!DNL Naver], consulte &quot;[Implementación [!DNL Naver] cuentas solo de seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

## Tareas de configuración iniciales para cuentas y campañas

[!DNL Adobe] y/o su agencia trabajará con usted para hacer lo siguiente:

1. (Nuevas cuentas de anunciante) Configurar cuentas administrativas:

   1. Configure la cuenta del anunciante.

   1. (Si es necesario) Cree cuentas de usuario para que el anunciante vea y administre sus datos de campaña y genere informes.

1. (Algunas redes de publicidad) Obtenga autorización para que Search, Social y Commerce accedan a cada cuenta mediante la API de la red de publicidad y la interfaz de usuario de Search, Social y Commerce.

1. Para cada cuenta de red de publicidad:

   1. (Si es necesario) Configure la cuenta en la red de anuncios.

   1. Integrar con la cuenta mediante [crear un registro de cuenta correspondiente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) en Buscar, Social y Comercio, que contiene las credenciales de acceso a la cuenta y las opciones de seguimiento, y establezca el estado de la cuenta en habilitado.

      Search, Social y Commerce se sincronizan con la red de publicidad. Si la cuenta ya contiene datos de campaña, estarán disponibles en unas 24 horas.

   1. ([Tipos de anuncios que puede crear o editar](/help/search-social-commerce/introduction/supported-inventory.md) en Search, Social y Commerce) Si la cuenta aún no contiene datos de campaña, cree la estructura de la campaña y los componentes de campaña desde Search, Social y Commerce mediante cualquiera de los siguientes métodos disponibles para el tipo de anuncio:

      * (Google Ads, Microsoft Advertising, Yahoo! Anuncios y solo cuentas de Yandex) Configure un [proceso automatizado para crear anuncios dinámicos y palabras clave dirigidos a cada elemento del inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) según una plantilla de publicidad específica de la red de anuncios que cree y el contenido de los archivos de datos de inventario que cargue en una ubicación FTP.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads y solo cuentas de Yandex) Cargar [archivos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) que contenga tantos datos como desee para una cuenta y, a continuación, los publique en las redes de anuncios.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads y solo cuentas de Yandex) Introduzca datos de componentes individuales directamente en la interfaz. Para la mayoría de las campañas y tipos de publicidad, puede crear datos en los niveles de campaña, grupo de publicidad y palabra clave, ubicación y nivel de publicidad individuales.
      Sin embargo, algunos tipos de campañas y anuncios requieren flujos de trabajo únicos. Consulte las instrucciones para configurar [[!DNL Microsoft Advertising] campañas de compra](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md), [[!DNL Google Ads] anuncios dinámicos de búsqueda](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md), [[!DNL Google Ads] campañas de rendimiento máximo](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md), y [[!DNL Google Ads] campañas de compra](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] solo cuentas de solo seguimiento) Cargar [archivos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) con datos para replicar las campañas, grupos de anuncios y palabras clave existentes en Search, Social y Commerce sin publicarlos en [!DNL Naver].


1. Configure el seguimiento para todos los anuncios para los que la publicidad de Adobe realizará un seguimiento de las conversiones:

   1. (Anunciantes con el servicio de seguimiento de conversión de publicidad de Adobe) Si es necesario, [configuración del rastreo de clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) para los anuncios y, opcionalmente, para las palabras clave, las ubicaciones y las extensiones de publicidad, generando y cargando URL de seguimiento de clics de Search, Social y Commerce.

      Para [!DNL Google Ads] campañas de rendimiento máximo, configure todo el seguimiento en la [configuración de seguimiento de la campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Para las campañas solo de seguimiento, debe generar direcciones URL de destino mediante hojas de edición por lotes y, a continuación, añadir las direcciones URL de destino generadas a las entidades relevantes mediante el editor nativo de la red de publicidad.

   1. Configure el seguimiento de conversiones. Según la implementación, esto puede implicar la adición de etiquetas de seguimiento de conversión a las páginas web del anunciante o la configuración de una entrega diaria de fuentes para los datos de conversión que el anunciante haya recopilado por separado.

      Si utiliza el servicio de seguimiento de conversiones de Adobe Advertising, puede generar etiquetas de seguimiento de conversiones [dentro de Search, Social y Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md) o [uso de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. Valide los datos de los que se realiza un seguimiento.

   Para obtener más información sobre la configuración del seguimiento, consulte el capítulo sobre seguimiento.

1. (Anunciantes con Adobe Analytics) [Integración de Adobe Advertising and Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) para que puedan intercambiar datos.

1. (Para permitir que Search, Social y Commerce optimicen las ofertas o los presupuestos de campaña; [tipos de campaña admitidos](/help/search-social-commerce/introduction/supported-inventory.md) solo) [Asignar la campaña a un portafolio](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Si el portafolio aún no se ha iniciado (optimizando ofertas o presupuestos), permita que la capacidad de optimización recopile datos suficientes para poder crear modelos de costes e ingresos que le permitan establecer el rendimiento de línea de base del portafolio antes de iniciarlo.

   Si el portafolio ya se ha lanzado, habilite el aprendizaje para el portafolio. Para obtener más información, consulte &quot;Ajuste de las estrategias del portafolio&quot;. Debería esperar que el portafolio sea volátil después de agregar nuevas campañas, mientras que la capacidad de optimización recopila datos sobre las unidades de oferta de la campaña. Las pujas se ajustan automáticamente en un plazo de una a tres semanas.

   Para obtener más información sobre los portafolios, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (Si se rastreará alguna nueva conversión para el anunciante) [Hacer que las conversiones estén disponibles](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) para informes, vistas de administración de campañas y objetivos de portafolio.

1. Para cada campaña, compruebe que Search, Social y Commerce reciben datos de clics y costes de la red de anuncios y valide los datos de ingresos que se muestran en Search, Social y Commerce con los datos de ingresos propios del anunciante.

1. (Opcional) Automatice la creación de informes configurando plantillas de informes, fuentes de hojas de cálculo y el envío por FTP de informes programados.

   Para obtener instrucciones, consulte el capítulo sobre Informes.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de campañas en Search, Social y Commerce](campaign-management-about.md)
>* [Monitorizar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)
>* [Datos de conversión de Google Ads en Search, Social y Commerce](google-conversion-data.md)
>* [Inventario admitido](/help/search-social-commerce/introduction/supported-inventory.md)

