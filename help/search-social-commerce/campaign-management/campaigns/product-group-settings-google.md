---
title: Configuración del grupo de productos [!DNL Google Ads]
description: Haga referencia a la configuración de  [!DNL Google Ads] grupos de productos de compras.
exl-id: 2cfef9de-b265-4fa5-b1bd-84e6cba79914
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/TkiKzm1sNZZdcu1ghpySElcQb7OIjnNZVqsVqzrK2uE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 270
ht-degree: 0%

---

# Configuración del grupo de productos [!DNL Google Ads]

## Todos los grupos de productos

**[!UICONTROL Condition]:** (solo lectura) Todos los productos

**[!UICONTROL Bid]:** (solo grupos de productos incluidos) El costo máximo por clic (CPC), que es la cantidad más alta que se paga por clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

## Todos los demás grupos de productos

**[!UICONTROL Condition/Value]:** (solo lectura para grupos de productos existentes) Las dimensiones de producto que se van a destinar. En el caso de los grupos de productos nuevos, introduzca la dimensión según la cual se van a segmentar los productos y el atributo correspondiente a la categoría de información seleccionada (como &quot;Acme&quot; cuando se establece el objetivo por marca o &quot;Nuevo&quot; cuando se establece el objetivo por condición).

Una vez creado un grupo de productos para dimensiones de producto específicas (es decir, no &quot;Todos los productos&quot;), Search, Social y Commerce crean automáticamente un grupo de productos para &quot;Todo lo demás&quot;.

Para obtener una lista de las dimensiones de producto disponibles, consulte &quot;[Filtros de productos de campañas de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;. Su lista de dimensiones puede estar limitada en función de la configuración [!UICONTROL Inventory Filter] de la campaña.

**[!UICONTROL Excluded]:** (opcional para los grupos de productos nuevos; solo lectura para los grupos de productos existentes) excluye las ofertas de anuncios para productos coincidentes.

**[!UICONTROL Bid]:** (solo grupos de productos incluidos) El costo máximo por clic (CPC), que es la cantidad más alta que se paga por clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

<!-- **[!UICONTROL Tracking Template]:** -->

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

>[!MORELIKETHIS]
>
>* [Acerca de los grupos de productos de compras](product-group-about.md)
>* [Administrar grupos de productos de compras](product-group-manage.md)
>* [Filtros de productos de campañas de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementar [!DNL Google Ads] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
