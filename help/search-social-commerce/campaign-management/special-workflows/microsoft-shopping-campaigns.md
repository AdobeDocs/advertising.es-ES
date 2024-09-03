---
title: Implementar  [!DNL Microsoft Advertising] campañas de compras
description: Obtenga información acerca del flujo de trabajo para configurar  [!DNL Microsoft Advertising] campañas de compras.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementar [!DNL Microsoft Advertising] campañas de compras

Los anuncios de las campañas de compras usan datos sobre los productos de la fuente de productos [!DNL Microsoft Merchant Center] existente, en lugar de las palabras clave, para decidir cómo y dónde mostrar los anuncios.

[!DNL Microsoft] campañas de compras se dirigen a [!DNL Microsoft Advertising Shopping Network]. La configuración de las campañas de compras incluye un país especificado en el que se venden los productos y una prioridad ([!DNL High], [!DNL Medium] o [!DNL Low]). Si lo desea, puede filtrar el inventario para anunciar productos con atributos específicos y dirigir o excluir ubicaciones y tipos de dispositivos específicos.

Puede controlar qué productos se muestran con los anuncios de compras configurando *[grupos de productos](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* de varios niveles en el nivel de grupo de anuncios. Los grupos de productos se basan en atributos de productos (categoría, tipo de producto, marca, condición, ID de producto y etiquetas personalizadas) y se pueden crear hasta siete niveles de grupos de productos para incluirlos o excluirlos de las ofertas, sin incluir &quot;[!DNL Add Products]&quot;. Puede establecer ofertas en el nivel más bajo de grupos de productos, utilizando la misma oferta para todos los productos coincidentes. Cuando el mismo producto se incluye en más de una campaña, [!DNL Microsoft Advertising] utiliza primero la prioridad de nivel de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta.

## Pasos para configurar [!DNL Microsoft Advertising] campañas de compras

Puede configurar campañas de compras usando [plantillas de fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para [!DNL Microsoft Advertising], usando [hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) o individualmente. Las siguientes instrucciones incluyen vínculos para crear entidades individuales.

1. Configure su cuenta de [!DNL Microsoft Merchant Center] y rellénela con datos del producto.

1. [Permitir que Search, Social y Commerce descarguen datos de la [!DNL Microsoft Merchant Center] cuenta](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Crear una campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) en la red de compras.

1. [Crea un grupo de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dentro de la campaña y establece la puja predeterminada para todos los anuncios.

   Puede anular la oferta predeterminada para grupos de productos individuales.

1. Cree grupos de productos para el grupo de publicidad:

   1. [Crear un grupo de productos &quot;Todos los productos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Opcional) [Crear grupos de productos secundarios](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Cree [anuncios de productos](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) con [líneas de promociones para incluir potencialmente en cada anuncio de compras](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) dentro del grupo de anuncios.

      Microsoft Advertising genera dinámicamente la copia de anuncio y la dirección URL de la página de aterrizaje para cada anuncio.

      >[!NOTE]
      >
      >Aunque el grupo de anuncios no incluya entidades de publicidad, [!DNL Microsoft Advertising] seguirá mostrando anuncios de los productos.

1. (Opcional) Para rastrear clics en el anuncio, [genere una URL de seguimiento con la herramienta URL de seguimiento](/help/search-social-commerce/tools/click-tracking-url-generate.md). Se recomienda agregar la dirección URL de seguimiento al campo [!UICONTROL Tracking Template] en la configuración de la cuenta, la campaña o el grupo de productos. Para facilitar el mantenimiento, añádalo al nivel más alto posible.

   También puede agregar la dirección URL de seguimiento a los datos del producto en la cuenta [!DNL Microsoft Merchant Center]. Para ello, incluya la dirección URL de seguimiento, junto con el valor en el campo &quot;vínculo&quot; o &quot;vínculo_móvil&quot;, según corresponda, en una columna personalizada &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; dentro de la fuente del producto. El valor del campo &quot;bingads_redirect&quot; reemplaza los valores de los campos &quot;link&quot; y &quot;mobile_link&quot;. Las direcciones URL generadas con este método no incluyen ningún parámetro de seguimiento especificado en la configuración de la cuenta de Search, Social y Commerce o de la campaña.

1. Supervisar el rendimiento de [ al generar [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Según sea necesario:

   1. [Edite la configuración de la campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar el presupuesto de la campaña.

      Si la campaña forma parte de un portafolio, la configuración del portafolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permite que Search, Social y Commerce optimicen los presupuestos de todas las campañas del portafolio.

   1. Ajuste la oferta máxima para grupos de productos existentes, elimine grupos de productos para los que ya no desee crear anuncios, o agregue un nuevo grupo de productos &quot;todos los productos&quot; o nuevos grupos de productos secundarios para crear anuncios para productos adicionales.

>[!NOTE]
>
>* Vea los campos requeridos para administrar [!DNL Microsoft Shopping] campañas y grupos de productos mediante [hojas de edición por lotes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) y [plantillas de fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Para obtener más información acerca de [!DNL Microsoft Shopping] campañas, consulte la [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/50903).
