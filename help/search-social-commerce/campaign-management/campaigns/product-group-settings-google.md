---
title: "[!DNL Google Ads] configuración de grupo de productos"
description: Haga referencia a la configuración de [!DNL Google Ads] grupos de productos de compras.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Google Ads] configuración de grupo de productos

## Todos los grupos de productos

**[!UICONTROL Condition]:** (Solo lectura) Todos los productos

**[!UICONTROL Bid]:** (Solo grupos de productos incluidos) El coste por clic máximo (CPC), que es la cantidad más alta que se debe pagar por un clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

## Todos los demás grupos de productos

**[!UICONTROL Condition/Value]:** (Solo lectura para grupos de productos existentes) Las dimensiones de producto que se van a segmentar. En el caso de los grupos de productos nuevos, introduzca la dimensión según la cual se van a segmentar los productos y el atributo correspondiente a la categoría de información seleccionada (como &quot;Acme&quot; cuando se establece el objetivo por marca o &quot;Nuevo&quot; cuando se establece el objetivo por condición).

Una vez creado un grupo de productos para dimensiones de producto específicas (es decir, no &quot;Todos los productos&quot;), Search, Social y Commerce crea automáticamente un grupo de productos para &quot;Todo lo demás&quot;.

Para obtener una lista de las dimensiones de producto disponibles, consulte &quot;[Filtros del producto de campaña de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; La lista de dimensiones puede estar limitada en función de la variable de la campaña [!UICONTROL Inventory Filter] configuración.

**[!UICONTROL Excluded]:** (Opcional para nuevos grupos de productos; de solo lectura para los grupos de productos existentes) Excluye las ofertas de anuncios de productos coincidentes.

**[!UICONTROL Bid]:** (Solo grupos de productos incluidos) El coste por clic máximo (CPC), que es la cantidad más alta que se debe pagar por un clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

>[!MORELIKETHIS]
>
>* [Acerca de los grupos de productos](product-group-about.md)
>* [Administrar grupos de productos de compras](product-group-manage.md)
>* [Filtros del producto de campaña de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementación [!DNL Google Ads] campañas de compra](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)

