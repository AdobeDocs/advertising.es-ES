---
title: '''[!DNL Microsoft® Advertising] configuración de campaña"'
description: Haga referencia a la configuración de [!DNL Microsoft® Advertising] campañas.
exl-id: c6d86fb8-48b0-40fd-bcfc-c4afdccd5283
feature: Search Campaign Management
source-git-commit: 1a4f802c51f29b2d7811ff21a9c7f0f20feb30ba
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] configuración de campaña

## \[Pantalla de creación de campaña\]

**[!UICONTROL Campaign Type]:** (Disponible solo durante la creación de la campaña) Dónde colocar los anuncios y qué tipos de anuncios puede contener la campaña:

* *[!UICONTROL Search]:* Muestra anuncios de texto en la red de búsqueda.

* *[!UICONTROL Shopping Network]:* Muestra anuncios de productos, para sus productos en [!DNL Microsoft® Merchant Center] catálogo de productos: en la red de compras.

* *[!UICONTROL Audience]:* Muestra anuncios nativos/de visualización en [!DNL Microsoft® Audience Network]. Puede: a) generar automáticamente anuncios basados en fuentes vinculando la campaña a una tienda de centro comercial en [!UICONTROL Shopping Settings] o b) cree anuncios adaptables con recursos de texto e imágenes cargadas. Ambas opciones requieren que cree grupos de anuncios con segmentación de usuarios.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Funcionalidad beta) Promociona sus productos a través de minoristas vinculados en las redes de búsqueda y audiencia. Puede crear grupos de anuncios secundarios y grupos de productos (aplicaciones para promocionar), así como anuncios de productos opcionales para la campaña. [!DNL Microsoft® Advertising] crea automáticamente anuncios para los grupos de productos.

* *[!UICONTROL Microsoft® Store Ads Campaign]:* (Funcionalidad beta) Promociona sus aplicaciones y juegos disponibles en el [!DNL Microsoft® Store]. Puede crear grupos de anuncios secundarios, grupos de productos y anuncios de productos opcionales para la campaña; [!DNL Microsoft® Advertising] crea automáticamente anuncios para los grupos de productos.

* *[!UICONTROL Audience Video]:* (Función beta) Muestra anuncios de vídeo en la red de audiencias.

* *[!UICONTROL Audience Video]:* (Funcionalidad beta) Muestra anuncios de vídeo de TV conectada (CTV) en la red de audiencia.

* *[!UICONTROL Performance Max]:* (Función beta) Muestra varios tipos de anuncios en todas las redes. Asigne grupos de recursos por separado en la [!DNL Microsoft® Advertising] editor de anuncios.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Un nombre de campaña único en la cuenta. La longitud máxima es de 128 caracteres.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *Pausado*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** La estrategia de oferta para la campaña:

* *[!UICONTROL CPV]* (Solo campañas de vídeo de Audience CTV) Utiliza el modelo de coste por vista (CPV). <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Campañas en las redes de audiencia, búsqueda y compras) Utiliza el modelo mejorado de coste por clic (eCPC) de la red de publicidad, que permite que la red de publicidad cambie automáticamente la oferta de coste por clic (CPC) para cada subasta en un intento de maximizar las conversiones, utilizando las conversiones especificadas dentro de la red de publicidad (no en Búsqueda, Social y Comercio), a la vez que intenta mantener su CPC promedio por debajo de su CPC máximo.

  Cuando agrega una campaña con eCPC a un portafolio optimizado de Search, Social y Commerce, Search, Social y Commerce optimiza las ofertas de base y — cuando el &quot;[!UICONTROL Auto adjust campaign budget limits]La opción &quot; está activada: el presupuesto de la campaña. La red de anuncios optimiza todos los ajustes de oferta y puede cambiar las ofertas generadas por Search, Social y Commerce en el momento de la consulta del usuario en función de los datos propietarios y las perspectivas. **Precaución:** Utilice campañas eCPC en portafolios solo cuando las conversiones totales rastreadas en la red de publicidad se alineen con el objetivo del portafolio.

* *[!UICONTROL Manual CPC]*: (Campañas de compra para marcas; [!DNL Microsoft Store Ads] campañas; obsoleto por [!DNL Microsoft® Advertising] en 2021 para otros tipos de campaña) Utiliza el modelo de coste por clic (CPC). Para algunos tipos de anuncio, puede permitir que la red de anuncios cambie las ofertas de la campaña:

   * **[!UICONTROL Enable Enhanced CPC]** (desactivado de forma predeterminada): Es lo mismo que usar el &quot;[!UICONTROL Enhanced CPC]Opción &quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campañas de ) Utiliza el modelo de coste por adquisición (CPA).

* *[!UICONTROL Manual CPM]* (Solo campañas de audiencia y campañas de vídeo de audiencia) Utiliza el modelo de coste por mil impresiones (CPM), para el que especifica lo que desea gastar por cada 1000 impresiones vistas. Las campañas con esta estrategia de oferta no están optimizadas cuando se incluyen en portafolios.

* *[!UICONTROL Maximize Clicks]:* (Campañas de búsqueda y compra) La red de anuncios, no de Búsqueda, Social y Comercio, optimiza las ofertas para maximizar los clics. Si lo desea, introduzca un **[!UICONTROL Max CPC]** (coste por clic) para garantizar que la red de publicidad no pague más de una cantidad específica por cada clic. **Precaución:** Al añadir una campaña con esta estrategia a un portafolio, las ofertas se basan en la ponderación de los clics, no en el objetivo del portafolio.

* *[!UICONTROL Maximize Conversion Value]:* (Redes de búsqueda y compras/compras inteligentes, campañas Máximo rendimiento de ). La red de anuncios, no de Búsqueda, Social y Comercio, optimiza las ofertas para maximizar el valor de conversión. Si lo desea, introduzca un **[!UICONTROL Target Return on Ad Spend]** (ROAS) como porcentaje. **Nota:** Utilice esta opción para campañas en portafolios híbridos, pero no estándar.

* *[!UICONTROL Maximize Conversions]:* (Campañas en la red de búsqueda) <!-- future: and audience network -->, campañas de rendimiento máximo) La red de anuncios (no Buscar, Social y Comercio) optimiza las ofertas para maximizar las conversiones. Si lo desea, introduzca un **[!UICONTROL Target CPC]** (coste por clic)<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **Nota:** Utilice esta opción para campañas en portafolios híbridos, pero no estándar.

* *[!UICONTROL Target CPA]:* (Campañas en la red de búsqueda) La red de anuncios (no Buscar, Social y Comercio) optimiza las ofertas en función de un **[!UICONTROL Target CPA]** (coste por adquisición), que es la cantidad promedio de 30 días que desea pagar por una adquisición (conversión). **Nota:** Utilice esta opción para campañas en portafolios híbridos (pero no estándar) con cualquier estrategia de gasto excepto [!UICONTROL Weekly] o [!UICONTROL Google Target CPA].

  Los datos de oferta de CPC y posición promedio no están disponibles para campañas con esta estrategia de oferta.

* *[!UICONTROL Target Impression Share]:* (Campañas en la red de búsqueda) La red de anuncios, no Búsqueda, Social y Comercio, optimiza las ofertas para lograr un porcentaje de impresión y una posición de anuncio objetivo. Si lo desea, introduzca un **[!UICONTROL Target Impression Share]** como porcentaje, la variable **[!UICONTROL Target Ad Position]**, y a **[!UICONTROL Max CPC]** (coste por clic). **Nota:** Esta opción no se admite en portafolios híbridos.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campañas en las redes de búsqueda y compras) La red de anuncios (no en Search, Social y Commerce) optimiza las ofertas según las **[!UICONTROL Target ROAS]** (retorno de la inversión en publicidad), especificado como porcentaje. Si lo desea, introduzca un **[!UICONTROL Max CPC]** (coste por clic) para garantizar que la red de publicidad no pague más de una cantidad específica por cada clic. **Nota:** Utilice esta opción para campañas en portafolios híbridos (pero no estándar) con cualquier estrategia de gasto excepto [!UICONTROL Weekly] o [!UICONTROL Google Target ROAS].

  Los datos de oferta de CPC y posición promedio no están disponibles para campañas con esta estrategia de oferta.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Solo campañas de compra; solo lectura para campañas existentes) El país en el que se venden los productos de la campaña. Dado que los productos están asociados a países de destino, esta configuración determina qué productos se anuncian en la campaña.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]:** (Solo campañas de audiencia; opcional) Vincula la campaña con una tienda de centro comercial específica para anuncios automatizados basados en fuentes en lugar de anuncios adaptables. Cuando seleccione esta opción, especifique el [!UICONTROL Merchant ID] y [!UICONTROL Products]. Debe crear grupos de anuncios para la campaña, pero no es necesario que cree anuncios.

Una vez que vincula la campaña a una tienda y guarda la configuración, no se puede cambiar esta opción.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]:** (Campañas de audiencia vinculadas únicamente a un centro comercial) Los productos que se van a anunciar. De forma predeterminada, *[!UICONTROL All products]* está seleccionado. Para anunciar solo productos con atributos específicos, seleccione *[!UICONTROL Filter products]* y especifique hasta siete combinaciones de dimensión y atributo de producto en las que filtrar sus productos. Todos los valores especificados deben ser aplicables para que aparezcan anuncios para el producto. Por ejemplo, para mostrar anuncios de suministros para mascotas Acme, puede crear los filtros `Custom Label 1=animals`, `Category=pet supplies`, y `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campañas solo en la red de visualización/nativa; opcional) Sitios en la red de visualización en los que no desea que se muestren los anuncios. Introduzca una URL válida, como www.example.com. Para especificar varias cadenas, sepárelas con comas o introdúzcalas en líneas independientes.

Para obtener información sobre la disponibilidad, consulte la Ayuda de Microsoft® Advertising a &quot;[Impedir que aparezcan anuncios en sitios web específicos](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (Para [!UICONTROL EF Redirect] solo) No implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Si se desea *[!UICONTROL Use account conversion goals for this campaign]* (el valor predeterminado) o *[!UICONTROL Use campaign specific conversion goals]*. Si decide especificar las metas de conversión para la campaña, seleccione las metas de la lista de todas las metas disponibles. **Nota:** Las metas se sincronizan a diario, por lo que es posible que no se incluyan en la lista las metas creadas en las 24 horas anteriores. Para actualizar la lista, [sincronizar manualmente los datos de red de anuncios](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Si la campaña forma parte de un portafolio, utilice los mismos objetivos de conversión que el objetivo del portafolio. El uso de diferentes objetivos de conversión puede afectar al rendimiento del portafolio.

>[!MORELIKETHIS]
>
>* [Administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
