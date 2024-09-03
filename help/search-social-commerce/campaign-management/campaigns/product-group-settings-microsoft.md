---
title: '[!DNL Microsoft Advertising] configuración de grupo de productos'
description: Haga referencia a la configuración de  [!DNL Microsoft Advertising] grupos de productos de compras.
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Configuración del grupo de productos [!DNL Microsoft Advertising]

## Todos los grupos de productos

**[!UICONTROL Condition]:** (solo lectura) Todos los productos

**[!UICONTROL Bid]:** (solo grupos de productos incluidos) El costo máximo por clic (CPC), que es la cantidad más alta que se paga por clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

## Todos los demás grupos de productos

**[!UICONTROL Condition/Value]:** (solo lectura para grupos de productos existentes) Las dimensiones de producto que se van a destinar. Para los grupos de productos nuevos, introduzca la dimensión según la cual se van a segmentar los productos y el atributo correspondiente para la categoría de información seleccionada (como &quot;Acme&quot; cuando se establece el objetivo por marca o &quot;Nuevo&quot; cuando se establece el objetivo por condición).

Una vez creado un grupo de productos para dimensiones de producto específicas (es decir, no &quot;Todos los productos&quot;), Search, Social y Commerce crean automáticamente un grupo de productos para &quot;Todo lo demás&quot;.

Para obtener una lista de las dimensiones de producto disponibles, consulte &quot;[Filtros de productos de campañas de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;. Su lista de dimensiones puede estar limitada en función de la configuración [!UICONTROL Inventory Filter] de la campaña.

**[!UICONTROL Excluded]:** (opcional para los grupos de productos nuevos; solo lectura para los grupos de productos existentes) excluye las ofertas de anuncios para productos coincidentes.

**[!UICONTROL Bid]:** (solo grupos de productos incluidos) El costo máximo por clic (CPC), que es la cantidad más alta que se paga por clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

>[!MORELIKETHIS]
>
>* [Acerca de los grupos de productos de compras](product-group-about.md)
>* [Administrar grupos de productos de compras](product-group-manage.md)
>* [Filtros de productos de campañas de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementar [!DNL Microsoft Advertising] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
