---
title: Acerca de los grupos de productos
description: Obtenga información sobre los grupos de productos de compras en campañas de compras.
exl-id: c91e6fb5-3be1-4d21-b508-09f974058fc7
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# Acerca de los grupos de productos

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo campañas de compra*

En las campañas de compras, los grupos de productos (no las palabras clave) determinan los productos de la cuenta del centro de comerciantes para los que se muestran los anuncios de compras. Cada grupo de productos se basa en un único atributo de producto (como categoría, tipo de producto, marca, condición, ID de producto o etiquetas personalizadas) y utiliza la misma oferta para todos los productos coincidentes. Puede incluir o excluir ofertas para los productos de cada grupo.

Los grupos de productos se configuran en el nivel de grupo de anuncios para determinar qué productos de las cuentas del centro de comerciantes aparecen en los anuncios de compra del grupo de anuncios. Aunque el grupo de anuncios no incluya entidades de publicidad, la red de anuncios seguirá mostrando anuncios de los productos.

Cuando el mismo producto se incluye en más de una campaña, la red de anuncios utiliza primero la prioridad de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta.

Para obtener más información acerca de [!DNL Google] campañas de compras y anuncios, consulte &quot;[Implementación [!DNL Google Ads] campañas de compra](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; y el [Documentación de Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Para obtener más información sobre las campañas de compra de Microsoft, consulte &quot;[Implementación [!DNL Microsoft® Advertising] campañas de compra](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)&quot; y el [Documentación de Microsoft Advertising](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>La compatibilidad no está disponible para [!DNL Google Ads] enumerar grupos en campañas de rendimiento máximo, que reemplazan a las campañas de compras inteligentes. Para administrar y ver los datos de los grupos de listas, use [!DNL Google Ads] editor.

## Jerarquía de grupos de productos

Antes de poder crear grupos de productos con atributos específicos para un grupo de publicidad, primero debe crear un grupo de productos inclusivo llamado &quot;[!UICONTROL All Products].&quot; Desde este grupo de productos principal, puede crear grupos de productos secundarios para subconjuntos de productos y puede crear nietos a partir de los grupos de productos secundarios. Una vez creado el primer grupo de productos secundario para un grupo de publicidad, otro grupo de productos denominado &quot;[!UICONTROL Everything Else]&quot; se crea automáticamente mediante la oferta de grupo de anuncios predeterminada. A medida que agregue más grupos de productos, la variable &quot;[!UICONTROL Everything Else]&quot; grupo se ajusta en consecuencia para que constituya todos los productos que no están en otro grupo de productos.

Dentro de un grupo de anuncios, puede crear hasta siete niveles de grupos de productos (sin incluir &quot;[!UICONTROL All Products]&quot;) para incluir o excluir de las ofertas, con uno o más grupos de productos dirigidos al mismo atributo en cada nivel (por ejemplo, [!UICONTROL Brand]=Acme para un grupo de productos y [!UICONTROL Brand]=AcmePlus para otro en el mismo nivel). Los grupos de productos principales se denominan subdivisiones y el nivel más bajo de subdivisión se conoce como unidad. Puedes definir las pujas y las plantillas de seguimiento, o bien excluir por completo las pujas, en el nivel de unidad. Todo el conjunto de grupos de productos activos de un grupo de publicidad se aplica jerárquicamente para determinar los productos aptos. Por ejemplo, si se subdivide [!UICONTROL All Products] en [!UICONTROL Brand]=AcmeBasic y [!UICONTROL Brand]=AcmePlus y, a continuación, subdivide cada uno de estos grupos de productos en [!UICONTROL Condition]=Nuevo y establecer ofertas, a continuación, solo los nuevos productos con las marcas AcmeBasic y AcmePlus se pueden anunciar o excluir de los anuncios.

![Ejemplo de un conjunto de grupos de productos](/help/search-social-commerce/assets/product-group-list.png "Ejemplo de un conjunto de grupos de productos")

![Ejemplo de jerarquía de grupos de productos](/help/search-social-commerce/assets/product-group-tree.png "Ejemplo de jerarquía de grupos de productos")

## El [!UICONTROL Product Groups] vista

Puede crear y editar grupos de productos y eliminar grupos de productos y sus grupos de productos secundarios en la [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] vista.

## Datos de seguimiento y rendimiento para grupos de productos de compras

(Cuentas/campañas con la variable &quot;[!UICONTROL EF Redirect]&quot; opción de seguimiento) Para permitir que Search, Social y Commerce realicen un seguimiento de las conversiones de los grupos de productos, [genere direcciones URL de seguimiento para grupos de productos con la herramienta URL de seguimiento](/help/search-social-commerce/tools/click-tracking-url-generate.md)y, a continuación, siga uno de estos procedimientos:

* (Necesario para [!DNL Google Ads]; práctica recomendada para [!DNL Microsoft Advertising]) Añada la URL de seguimiento a [!DNL Tracking Template] en la configuración de cuenta, campaña o grupo de productos. Para facilitar el mantenimiento, añádalos al nivel más alto posible. No se incluye ningún parámetro de datos anexados especificado para la cuenta o campaña.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Utilice esta opción solo cuando no incluya direcciones URL de seguimiento de búsqueda, medios sociales y comercio en una columna personalizada dentro de la fuente del producto. Si realiza ambas acciones, las direcciones URL incluirán dos redirecciones y provocarán vínculos rotos.

* ([!DNL Microsoft Advertising] solo) Añada la URL de seguimiento a los datos del producto dentro de la variable [!DNL Microsoft Merchant Center] cuenta. Para ello, incluya la dirección URL de seguimiento junto con el valor en la variable `link` o `mobile_link` , según corresponda, en una columna personalizada denominada [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) en la fuente del producto. Las direcciones URL generadas con este método no incluyen ningún parámetro de seguimiento especificado en la configuración de la cuenta o la campaña en Search, Social y Commerce.

Puede ver datos sobre grupos de productos en [el [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Administrar grupos de productos de compras](product-group-manage.md)
>* [[!DNL Google Ads] configuración de grupo de productos](product-group-settings-google.md)
>* [Implementación [!DNL Google Ads] campañas de compra](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] configuración de grupo de productos](product-group-settings-microsoft.md)
>* [Implementación [!DNL Microsoft® Advertising] campañas de compra](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
