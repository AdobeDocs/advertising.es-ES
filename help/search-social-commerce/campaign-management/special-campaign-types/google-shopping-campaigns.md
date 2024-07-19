---
title: Implementar  [!DNL Google Ads] campañas de compras
description: Obtenga información acerca del flujo de trabajo para configurar  [!DNL Google Ads] campañas de compras.
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 3c702a01df1186e74c4f329a08199ce829be0827
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Implementar [!DNL Google Ads] campañas de compras

Los anuncios de las campañas de compras usan datos sobre los productos de la fuente de productos [!DNL Google Merchant Center] existente, en lugar de las palabras clave, para decidir cómo y dónde mostrar los anuncios.

[!DNL Google Ads] campañas pueden dirigirse a [!DNL Google Shopping Network] mediante [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network]&quot;. La configuración de [!DNL Google Shopping] campañas incluye una prioridad ([!UICONTROL High], [!UICONTROL Medium] o [!UICONTROL Low]). Opcionalmente, puede mostrar la información de inventario local en los anuncios de compra mediante una configuración de nivel de campaña.

Puede controlar qué productos se muestran con los anuncios de compras configurando *[grupos de productos](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* de varios niveles en el nivel de grupo de anuncios. Los grupos de productos se basan en atributos de productos (categoría, tipo de producto, marca, condición, ID de producto y etiquetas personalizadas) y se pueden crear hasta siete niveles de grupos de productos para incluirlos o excluirlos de las ofertas. Puede establecer ofertas en el nivel más bajo de grupos de productos, utilizando la misma oferta para todos los productos coincidentes. Cuando el mismo producto se incluye en más de una campaña, [!DNL Google Ads] utiliza primero la prioridad de nivel de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta.

## Pasos para configurar [!DNL Google Ads] campañas de compras

Puede configurar campañas de compras usando [plantillas de fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para [!DNL Google Shopping], usando [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) o individualmente. Las siguientes instrucciones incluyen vínculos para crear entidades individuales.

1. Configure su cuenta de [!DNL Google Merchant Center] y rellénela con datos del producto.

1. [Permitir que Search, Social y Commerce descarguen datos de la [!DNL Google Merchant Center] cuenta](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Crear una campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) en la red de compras.

1. [Crea un grupo de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dentro de la campaña y establece la puja predeterminada para todos los anuncios.

   Puede anular la oferta predeterminada para grupos de productos individuales.

1. Cree grupos de productos para el grupo de publicidad:

   1. [Crear un grupo de productos &quot;Todos los productos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Opcional) [Crear grupos de productos secundarios](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >No es necesario crear anuncios de compra. Aunque el grupo de anuncios no incluya entidades de publicidad, [!DNL Google Ads] seguirá mostrando anuncios de los productos.

1. (Opcional) Para rastrear clics en el anuncio, [genere una URL de seguimiento con la herramienta URL de seguimiento](/help/search-social-commerce/tools/click-tracking-url-generate.md) y, a continuación, agréguela a la configuración de la cuenta, la campaña o el grupo de productos.

1. Supervise el rendimiento de [generando [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) y [el [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Según sea necesario:

   1. [Edite la configuración de la campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar el presupuesto de la campaña.

      Si la campaña forma parte de un portafolio, la configuración del portafolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permite que Search, Social y Commerce optimicen los presupuestos de todas las campañas del portafolio.

   1. [Ajuste la puja máxima para los grupos de productos existentes](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [elimine grupos de productos](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) para los que ya no desee crear anuncios o agregue un [nuevo grupo de productos &quot;todos los productos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) o [nuevos grupos de productos secundarios](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) para crear anuncios para productos adicionales.

>[!NOTE]
>
>* Vea los campos requeridos para administrar [!DNL Google Shopping] campañas y grupos de productos mediante [hojas de edición por lotes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) y [plantillas de fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Para obtener más información acerca de [!DNL Google Shopping] campañas, consulte la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/2454022).
