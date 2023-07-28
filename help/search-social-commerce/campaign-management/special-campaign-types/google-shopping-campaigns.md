---
title: Implementación [!DNL Google Ads] campañas de compra
description: Obtenga información sobre el flujo de trabajo para configurar [!DNL Google Ads] campañas de compras.
exl-id: aab61d94-861f-4072-b044-f9ae6759e028
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Implementación [!DNL Google Ads] campañas de compra

Los anuncios de las campañas de compra utilizan datos sobre productos de [!DNL Google Merchant Center] fuente de productos, en lugar de palabras clave, para decidir cómo y dónde mostrar los anuncios.

[!DNL Google Ads] las campañas pueden segmentar el [!DNL Google Shopping Network] uso del [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; La configuración de [!DNL Google Shopping] las campañas incluyen una prioridad ([!UICONTROL High], [!UICONTROL Medium], o [!UICONTROL Low]). Opcionalmente, puede mostrar la información de inventario local en los anuncios de compra mediante una configuración de nivel de campaña.

Puede controlar qué productos se muestran con los anuncios de compra configurando varios niveles *[grupos de productos](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* en el nivel de grupo de anuncios. Los grupos de productos se basan en atributos de productos (categoría, tipo de producto, marca, condición, ID de producto y etiquetas personalizadas) y se pueden crear hasta siete niveles de grupos de productos para incluirlos o excluirlos de las ofertas. Puede establecer ofertas en el nivel más bajo de grupos de productos, utilizando la misma oferta para todos los productos coincidentes. Cuando el mismo producto se incluye en más de una campaña, [!DNL Google Ads] utiliza primero la prioridad en el nivel de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta.

## Pasos para la configuración [!DNL Google Ads] campañas de compra

Puede configurar campañas de compra utilizando [plantillas de fuente de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para [!DNL Google Shopping], utilizando [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), o individualmente. Las siguientes instrucciones incluyen vínculos para crear entidades individuales.

1. Configure su [!DNL Google Merchant Center] y rellenarla con datos del producto.

1. [Permitir que Search, Social y Commerce descarguen datos de [!DNL Google Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Creación de una campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) en la red de compras.

1. [Crear un grupo de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dentro de la campaña y establezca la oferta predeterminada para todos los anuncios.

Puede anular la oferta predeterminada para grupos de productos individuales.

1. Cree grupos de productos para el grupo de publicidad:

   1. [Crear un grupo de productos &quot;Todos los productos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Opcional) [Crear grupos de productos secundarios](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >No es necesario crear anuncios de compra. Incluso si el grupo de anuncios no incluye entidades de publicidad, [!DNL Google Ads] sigue mostrando anuncios de los productos.

1. (Opcional) Para rastrear clics en el anuncio, [generación de una URL de seguimiento con la herramienta URL de seguimiento](/help/search-social-commerce/tools/click-tracking-url-generate.md)y, a continuación, agréguelo a la configuración de la cuenta, la campaña o el grupo de productos.

1. Monitorización del rendimiento mediante [generando el [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) y [el [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Según sea necesario:

   1. [Editar la configuración de la campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar el presupuesto de la campaña.

      Si la campaña forma parte de un portafolio, la configuración del portafolio es &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permite a Search, Social y Commerce optimizar los presupuestos de todas las campañas del portafolio.

   1. [Ajustar la oferta máxima para grupos de productos existentes](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [eliminar grupos de productos](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) para el que ya no desea crear anuncios o agregar un [nuevo grupo de productos &quot;todos los productos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) o [nuevos grupos de productos secundarios](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) para crear anuncios para productos adicionales.

>[!NOTE]
>
>* Consulte los campos obligatorios para gestionar [!DNL Google Shopping] campañas y grupos de productos que utilizan [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) y [plantillas de fuente de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Para obtener más información acerca de [!DNL Google Shopping] campañas, consulte la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/2454022).
