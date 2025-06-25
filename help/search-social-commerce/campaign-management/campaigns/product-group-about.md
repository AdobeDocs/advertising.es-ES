---
title: Acerca de los grupos de productos
description: Obtenga información sobre los grupos de productos de compras en campañas de compras.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Acerca de los grupos de productos

*[!DNL Google Ads]y [!DNL Microsoft Advertising] campañas de compras solo*

En las campañas de compras, los grupos de productos (no las palabras clave) determinan los productos de la cuenta del centro de comerciantes para los que se muestran los anuncios de compras. Cada grupo de productos se basa en un único atributo de producto (como categoría, tipo de producto, marca, condición, ID de producto o etiquetas personalizadas) y utiliza la misma oferta para todos los productos coincidentes. Puede incluir o excluir ofertas para los productos de cada grupo.

Los grupos de productos se configuran en el nivel de grupo de anuncios para determinar qué productos de las cuentas del centro de comerciantes aparecen en los anuncios de compra del grupo de anuncios. Aunque el grupo de anuncios no incluya entidades de publicidad, la red de anuncios seguirá mostrando anuncios de los productos.

Cuando el mismo producto se incluye en más de una campaña, la red de anuncios utiliza primero la prioridad de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta.

Para obtener más información sobre [!DNL Google] campañas de compras y anuncios, consulte &quot;[Implementar [!DNL Google Ads] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; y la [documentación de Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Para obtener más información acerca de [!DNL Microsoft] campañas de compras, consulte &quot;[Implementar [!DNL Microsoft Advertising] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot; y la [[!DNL Microsoft Advertising] documentación](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>La compatibilidad no está disponible para [!DNL Google Ads] grupos de listas en campañas Máximo rendimiento, que están reemplazando a las campañas de compras inteligentes. Para administrar y ver datos de grupos de listas, use el editor [!DNL Google Ads].

## Jerarquía de grupos de productos

Para poder crear grupos de productos con atributos específicos para un grupo de anuncios, primero debe crear un grupo de productos inclusivo denominado &quot;[!UICONTROL All Products]&quot;. Desde este grupo de productos principal, puede crear grupos de productos secundarios para subconjuntos de productos y puede crear nietos a partir de los grupos de productos secundarios. Una vez creado el primer grupo de productos secundario para un grupo de anuncios, se crea automáticamente otro grupo de productos denominado &quot;[!UICONTROL Everything Else]&quot; mediante la oferta de grupo de anuncios predeterminada. A medida que agrega más grupos de productos, el grupo &quot;[!UICONTROL Everything Else]&quot; se ajusta en consecuencia para que constituya todos los productos que no están en otro grupo de productos.

Dentro de un grupo de anuncios, puede crear hasta siete niveles de grupos de productos (sin incluir &quot;[!UICONTROL All Products]&quot;) para incluirlos o excluirlos de ofertas, y uno o más grupos de productos tienen como objetivo el mismo atributo en cada nivel (por ejemplo, [!UICONTROL Brand]=Acme para un grupo de productos y [!UICONTROL Brand]=AcmePlus para otro en el mismo nivel). Los grupos de productos principales se denominan subdivisiones y el nivel más bajo de subdivisión se conoce como unidad. Puedes definir las pujas y las plantillas de seguimiento, o bien excluir por completo las pujas, en el nivel de unidad. Todo el conjunto de grupos de productos activos de un grupo de publicidad se aplica jerárquicamente para determinar los productos aptos. Por ejemplo, si subdivide [!UICONTROL All Products] en [!UICONTROL Brand]=AcmeBasic y [!UICONTROL Brand]=AcmePlus y, a continuación, subdivide cada uno de esos grupos de productos en [!UICONTROL Condition]=Nuevo y establece ofertas, solo se podrán anunciar o excluir de los anuncios los nuevos productos con las marcas AcmeBasic y AcmePlus.

![Ejemplo de un conjunto de grupos de productos](/help/search-social-commerce/assets/product-group-list.png "Ejemplo de un conjunto de grupos de productos")

![Ejemplo de jerarquía de grupos de productos](/help/search-social-commerce/assets/product-group-tree.png "Ejemplo de jerarquía de grupos de productos")

## La vista [!UICONTROL Product Groups]

Puede crear y editar grupos de productos y eliminar grupos de productos y sus grupos de productos secundarios en la vista [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

## Datos de seguimiento y rendimiento para grupos de productos de compras

(Cuentas/campañas con la opción de seguimiento &quot;[!UICONTROL EF Redirect]&quot;) Para permitir que Search, Social y Commerce realicen un seguimiento de las conversiones de los grupos de productos, [genere direcciones URL de seguimiento para los grupos de productos mediante la herramienta URL de seguimiento](/help/search-social-commerce/tools/click-tracking-url-generate.md) y, a continuación, siga uno de estos procedimientos:

* (Necesario para [!DNL Google Ads]; práctica recomendada para [!DNL Microsoft Advertising]) Agregue la dirección URL de seguimiento al campo [!DNL Tracking Template] en la configuración de la cuenta, la campaña o el grupo de productos. Para facilitar el mantenimiento, añádalos al nivel más alto posible. No se incluye ningún parámetro de datos anexados especificado para la cuenta o campaña.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Utilice esta opción solo cuando no incluya las direcciones URL de seguimiento de búsqueda, medios sociales y Commerce en una columna personalizada dentro de la fuente del producto. Si realiza ambas acciones, las direcciones URL incluirán dos redirecciones y provocarán que se rompan los vínculos.

* ([!DNL Microsoft Advertising] solamente) Agregue la URL de seguimiento a los datos del producto dentro de la cuenta [!DNL Microsoft Merchant Center]. Para ello, incluya la dirección URL de seguimiento, junto con el valor en el campo `link` o `mobile_link`, según corresponda, en una columna personalizada denominada [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) dentro de la fuente del producto. Las direcciones URL generadas con este método no incluyen ningún parámetro de seguimiento especificado en la configuración de la cuenta o la campaña en Search, Social y Commerce.

Puede ver datos sobre los grupos de productos en [el [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Administrar grupos de productos de compras](product-group-manage.md)
>* [[!DNL Google Ads] configuración del grupo de productos](product-group-settings-google.md)
>* [Implementar [!DNL Google Ads] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] configuración del grupo de productos](product-group-settings-microsoft.md)
>* [Implementar [!DNL Microsoft Advertising] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
