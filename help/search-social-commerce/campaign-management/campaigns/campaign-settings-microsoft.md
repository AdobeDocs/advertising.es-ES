---
title: '[!DNL Microsoft Advertising] configuración de campaña'
description: Hacer referencia a la configuración de  [!DNL Microsoft Advertising] campañas.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: b8aa2461d261af50e1bf66c4ae29e4e453dfd182
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configuración de campaña

## \[Pantalla de creación de campaña\]

**[!UICONTROL Campaign Type]:** (disponible solo durante la creación de la campaña) Dónde colocar los anuncios y qué tipos de anuncios
la campaña puede contener:

* *[!UICONTROL Search]:* Muestra anuncios de texto en la red de búsqueda.

* *[!UICONTROL Shopping Network]:* Muestra anuncios de productos — para sus productos en su catálogo de productos [!DNL Microsoft Merchant Center] — en la red de compras.

* *[!UICONTROL Audience]:* Muestra anuncios nativos/de visualización en [!DNL Microsoft Audience Network]. Puede: a) generar automáticamente anuncios basados en fuentes vinculando la campaña a una tienda del centro comercial en la sección [!UICONTROL Shopping Settings] o b) crear anuncios adaptables con recursos de texto e imágenes cargadas. Ambas opciones requieren que cree grupos de anuncios con segmentación de usuarios.

* *[!UICONTROL Shopping Campaigns for Brands]:* Promociona sus productos a través de minoristas vinculados en las redes de búsqueda y audiencia. Puede crear grupos de anuncios secundarios y grupos de productos (aplicaciones para promocionar), así como anuncios de productos opcionales para la campaña; [!DNL Microsoft Advertising] crea automáticamente anuncios para los grupos de productos. Para campañas de compra de marcas, use la estrategia de oferta [!UICONTROL Manual CPC]; para promociones de compra de marcas, use la estrategia de oferta [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft Store Ads Campaign]:* Promociona tus aplicaciones y juegos disponibles en [!DNL Microsoft Store]. Puede crear grupos de anuncios secundarios, grupos de productos y anuncios de productos opcionales para la campaña; [!DNL Microsoft Advertising] crea automáticamente anuncios para los grupos de productos.

* *[!UICONTROL Audience CTV Video]:* Muestra anuncios de vídeo de TV (CTV) conectados en la red de audiencia.

* *[!UICONTROL Audience Video]:* Muestra anuncios de vídeo estándar en la red de audiencias.

* *[!UICONTROL Performance Max]:* Muestra varios tipos de anuncios en todas las redes mediante pujas inteligentes de [!DNL Microsoft Advertising]. En la configuración de la campaña, debe especificar uno o más grupos de recursos, que incluyen imágenes, logotipos, titulares, descripciones, una llamada a la acción opcional y señales de audiencia. La red de anuncios combina automáticamente los recursos para publicar anuncios en función del canal.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Un nombre de campaña único en la cuenta. La longitud máxima es de 128 caracteres.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *En pausa*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Estrategia de oferta para la campaña:

* *[!UICONTROL Cost per Sale]:* (solo campañas de compras) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas según [!UICONTROL Target CPS] (coste por venta). Usted paga solamente cuando un clic en su producto y resulta en una venta dentro de las 24 horas. **Nota:** No incluya campañas con esta estrategia de oferta en portafolios. La optimización de búsqueda, social y Commerce no está disponible para campañas con esta estrategia de oferta.

  Una vez guardada una campaña de compra para marcas con esta estrategia de oferta, no se puede cambiar la estrategia de oferta. Para otros tipos de campañas de compra, esta estrategia solo está disponible para nuevas campañas.

* *[!UICONTROL CPV]* (solo campañas de vídeo de Audience CTV) Utiliza el modelo de coste por vista (CPV). Search, Social y Commerce no proporcionan optimización para las campañas con esta estrategia de oferta que se incluyen en los portafolios.

* *[!UICONTROL Enhanced CPC]:* (Campañas en las redes de audiencia, búsqueda y compras) Utiliza el modelo mejorado de coste por clic (eCPC) de la red de anuncios, que permite que la red de anuncios cambie automáticamente la oferta de coste por clic (CPC) para cada subasta en un intento de maximizar las conversiones, utilizando las conversiones especificadas dentro de la red de anuncios (no en Buscar, Social y Commerce), al tiempo que intenta mantener su CPC promedio por debajo de su CPC máximo.

  Al agregar una campaña con eCPC a un portafolio optimizado de Search, Social y Commerce, Search, Social y Commerce optimiza las ofertas de base y, cuando la opción &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; está habilitada, el presupuesto de la campaña. La red de anuncios optimiza todos los ajustes de oferta y puede cambiar las ofertas generadas por Search, Social y Commerce en el momento de la consulta del usuario en función de los datos propietarios y las perspectivas. **Precaución:** Use campañas eCPC en portafolios solamente cuando las conversiones totales rastreadas en la red de anuncios se alineen con el objetivo del portafolio.

* *[!UICONTROL Manual CPC]*: (Campañas de compra para marcas; [!DNL Microsoft Store Ads] campañas; obsoleto para otros tipos de campaña) Utiliza el modelo de coste por clic (CPC). Para algunos tipos de anuncio, puede permitir que la red de anuncios cambie las ofertas de la campaña:

   * **[!UICONTROL Enable Enhanced CPC]** (deshabilitado de forma predeterminada): Esta opción es la misma que se usa la opción &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campañas) Utiliza el modelo de coste por adquisición (CPA).

* *[!UICONTROL Manual CPM]* (solo campañas de audiencia y campañas de vídeo de audiencia) Utiliza el modelo de coste por mil impresiones (CPM), para el cual especifica lo que desea gastar por cada 1000 impresiones vistas. Las campañas con esta estrategia de oferta no están optimizadas cuando se incluyen en portafolios.

* *[!UICONTROL Maximize Clicks]:* (campañas de búsqueda y compras) La red de anuncios, no de búsqueda, social y Commerce, optimiza las ofertas para maximizar los clics. De manera opcional, escriba **[!UICONTROL Max CPC]** (costo por clic) para asegurarse de que la red publicitaria no pague más de una cantidad determinada por cada clic. **Precaución:** Al agregar una campaña con esta estrategia a un portafolio, la ponderación de los clics (no el objetivo del portafolio) genera ofertas.

* *[!UICONTROL Maximize Conversion Value]:* (redes de búsqueda y compras/compras inteligentes, campañas de rendimiento máximo) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para maximizar el valor de conversión. Opcionalmente, escriba un **[!UICONTROL Target Return on Ad Spend]** (ROAS) como porcentaje. **Nota:** Utilice esta opción para campañas en portafolios híbridos, pero no en portafolios estándar. En portafolios híbridos, Search, Social y Commerce optimizan el ROAS de Target.

* *[!UICONTROL Maximize Conversions]:* (Campañas y campañas de rendimiento máximo en la red de búsqueda o en la red de audiencia (pero no en vídeos de audiencia o TV conectada)) La red de anuncios (no en Buscar, Social y Commerce) optimiza las ofertas para maximizar las conversiones. Opcionalmente, escriba **[!UICONTROL Target CPC]** (costo por clic). Para las campañas de audiencia, también puede especificar un **[!UICONTROL Target CPA]** opcional (costo por adquisición). **Nota:** Utilice esta opción para campañas en portafolios híbridos, pero no en portafolios estándar. En portafolios híbridos, Search, Social y Commerce optimizan la CPA de Target.

* *[!UICONTROL Target CPA]:* (Campañas en la red de búsqueda) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas según un **[!UICONTROL Target CPA]** opcional (coste por adquisición), que es la cantidad promedio de 30 días que desea pagar por una adquisición (conversión). **Nota:** Utilice esta opción para campañas en portafolios híbridos (pero no en portafolios estándar) con cualquier estrategia de gasto excepto [!UICONTROL Weekly] o [!UICONTROL Google Target CPA]. En portafolios híbridos, Search, Social y Commerce optimizan la CPA de Target.

  Los datos de oferta de CPC y posición promedio no están disponibles para campañas con esta estrategia de oferta.

* *[!UICONTROL Target Impression Share]:* (Campañas en la red de búsqueda) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para lograr un porcentaje de impresión objetivo y una posición de anuncio. De manera opcional, escriba **[!UICONTROL Target Impression Share]** como porcentaje, **[!UICONTROL Target Ad Position]** y **[!UICONTROL Max CPC]** (costo por clic). **Nota:** Esta opción no se admite en portafolios híbridos.

* *[!UICONTROL Target Return on Ad Spend]:* (Campañas en las redes de búsqueda y compras) La red de anuncios (no en Buscar, Social y Commerce) optimiza las ofertas según tu **[!UICONTROL Target ROAS]** (retorno de la inversión en publicidad), especificado como porcentaje. De manera opcional, escriba **[!UICONTROL Max CPC]** (costo por clic) para asegurarse de que la red publicitaria no pague más de una cantidad determinada por cada clic. **Nota:** Utilice esta opción para campañas en portafolios híbridos (pero no en portafolios estándar) con cualquier estrategia de gasto excepto [!UICONTROL Weekly] o [!UICONTROL Google Target ROAS]. En portafolios híbridos, Search, Social y Commerce optimizan el ROAS de Target.

  Los datos de oferta de CPC y posición promedio no están disponibles para campañas con esta estrategia de oferta.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Solo campañas de compras; solo lectura para campañas existentes) El país en el que
se venden los productos de la campaña. Dado que los productos están asociados a países de destino, esta configuración determina qué productos se anuncian en la campaña.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (solo campañas de audiencia; opcional) Vincula la campaña con un almacén del centro de comerciantes específico para anuncios automatizados basados en fuentes en lugar de anuncios adaptables. Cuando seleccione esta opción, especifique [!UICONTROL Merchant ID] y [!UICONTROL Products]. Debe crear grupos de anuncios para la campaña, pero no es necesario que cree anuncios.

Una vez que vincula la campaña a una tienda y guarda la configuración, no se puede cambiar esta opción.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (Campañas de audiencia vinculadas únicamente a un almacén del centro de comerciantes) Los productos que se van a anunciar. De manera predeterminada, *[!UICONTROL All products]* está seleccionado. Para anunciar solo productos con atributos específicos, seleccione *[!UICONTROL Filter products]* y especifique hasta siete combinaciones de dimensión y atributo de producto en las que filtrar los productos. Todos los valores especificados deben ser aplicables para que aparezcan anuncios para el producto. Por ejemplo, para mostrar anuncios de artículos para mascotas Acme, puede crear los filtros `Custom Label 1=animals`, `Category=pet supplies` y `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Solo campañas Máximo rendimiento) El idioma del anuncio, que debe coincidir con el idioma de los sitios en los que puede aparecer. [!DNL Microsoft Advertising] determina el idioma de un usuario a partir de diversas señales, como la consulta del usuario, el país del editor y la configuración de idioma del usuario.

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

**[!UICONTROL Negative Websites]:** (solo campañas en la red nativa/de visualización; opcional) Sitios en la red de visualización en los que no desea que se muestren los anuncios. Introduzca una URL válida, como www.example.com. Para especificar varias cadenas, sepárelas con comas o introdúzcalas en líneas independientes.

Para obtener información acerca de la disponibilidad, consulte la ayuda de Microsoft Advertising para &quot;[evitar que aparezcan anuncios en sitios web específicos](https://help.ads.microsoft.com/#apex/bae/en/14061/0)&quot;.

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

**[!UICONTROL Track Product Group]:** (solo para [!UICONTROL EF Redirect]) No implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (por grupo de recursos)

**[!UICONTROL Asset Group Name]:** El nombre de la carpeta de recursos (grupo de recursos).

**[!UICONTROL Asset Group Status]:** Estado del grupo de recursos: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Dirección URL final de todos los anuncios creados a partir del grupo de recursos.

**[!UICONTROL Images]:** Hasta 20 imágenes para el anuncio, incluida al menos una imagen cuadrada y una imagen horizontal. Consulte las [[!DNL Microsoft Advertising] directrices de imágenes](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Puede cargar imágenes o seleccionarlas en su [!UICONTROL Asset Library], pero no ambas en la misma operación.

* Para cargar imágenes:

   1. En la ficha [!UICONTROL Upload from Device], haga clic en **[!UICONTROL +]** y seleccione imágenes de su dispositivo o red.

   1. Para cada imagen:

      1. Seleccione la relación de aspecto.

      1. Arrastre y coloque el cuadro de recorte según sea necesario para seleccionar la parte visible de la imagen y cambie el tamaño de la parte visible de la imagen según sea necesario siempre que sea posible.

      1. (Opcional) Seleccione relaciones de aspecto adicionales y, opcionalmente, cambie la posición y el tamaño de la imagen según sea necesario para cada relación de aspecto seleccionada.

         Se crea un recurso para cada relación de aspecto seleccionada.

      1. Haga clic en **[!UICONTROL Proceed]**.

   1. Cuando termine de especificar imágenes, haga clic en **[!UICONTROL Upload]**.

* Para seleccionar imágenes de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione las imágenes.

**[!UICONTROL Logos]:** al menos un logotipo. Se pueden incluir hasta cinco. Consulte las [[!DNL Microsoft Advertising] directrices de recursos](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Puede cargar imágenes o seleccionarlas en su [!UICONTROL Asset Library], pero no ambas en la misma operación.

* Para cargar imágenes:

   1. En la ficha [!UICONTROL Upload from Device], haga clic en **[!UICONTROL +]** y seleccione imágenes de su dispositivo o red.

   1. Para cada imagen:

      1. Seleccione la relación de aspecto.

      1. Arrastre y coloque el cuadro de recorte según sea necesario para seleccionar la parte visible de la imagen y cambie el tamaño de la parte visible de la imagen según sea necesario siempre que sea posible.

      1. (Opcional) Seleccione relaciones de aspecto adicionales y, opcionalmente, cambie la posición y el tamaño de la imagen según sea necesario para cada relación de aspecto seleccionada.

         Se crea un recurso para cada relación de aspecto seleccionada.

      1. Haga clic en **[!UICONTROL Proceed]**.

   1. Cuando termine de especificar imágenes, haga clic en **[!UICONTROL Upload]**.

* Para seleccionar imágenes de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione las imágenes.

**[!UICONTROL Headlines]:** Al menos tres y hasta 15 titulares cortos con un máximo de 30 caracteres cada uno. Puede escribir texto o seleccionar recursos de su [!UICONTROL Asset Library], pero no ambos en la misma operación.

* Para introducir texto:

   1. En la ficha [!UICONTROL Enter Text], escriba el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Long Headlines]:** Al menos un titular largo, y hasta cinco, con un máximo de 90 caracteres cada uno. Puede escribir texto o seleccionar recursos de su [!UICONTROL Asset Library], pero no ambos en la misma operación.

* Para introducir texto:

   1. En la ficha [!UICONTROL Enter Text], escriba el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Descriptions]:** Al menos dos y hasta cinco descripciones con un máximo de 90 caracteres cada una. Puede escribir texto o seleccionar recursos de su [!UICONTROL Asset Library], pero no ambos en la misma operación.

* Para introducir texto:

   1. En la ficha [!UICONTROL Enter Text], escriba el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Call to Action]:** Llamada a la acción para incluir en el anuncio. De manera predeterminada, *[!UICONTROL Act Now]* está seleccionado.

**[!UICONTROL Business Name]:** El nombre comercial, con un máximo de 25 caracteres. No puede contener secuencias de comandos, HTML u otro lenguaje de marcado.

**[!UICONTROL Audience Signal]:** (Opcional) [!DNL Microsoft Advertising] audiencias para usar como señales de audiencia para la campaña. [!DNL Microsoft Advertising] modelos de aprendizaje automático utilizan las audiencias para encontrar internautas similares a los de target y también pueden mostrar anuncios a audiencias que no se especifican como señales que le ayudarán a alcanzar sus objetivos de rendimiento. Elija las audiencias que tienen más probabilidades de convertirse.

>[!NOTE]
>Las señales de audiencia son diferentes de [los destinos de audiencia a nivel de grupo de anuncios](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Permite especificar otro grupo de recursos.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Ya sea para *[!UICONTROL Use account conversion goals for this campaign]* (predeterminado) o *[!UICONTROL Use campaign specific conversion goals]*. Si decide especificar las metas de conversión para la campaña, seleccione las metas de la lista de todas las metas disponibles. **Nota:** Las metas se sincronizan a diario, por lo que es posible que no se incluyan en la lista las metas creadas en las 24 horas anteriores. Para actualizar la lista, [sincronice manualmente los datos de la red de anuncios](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

>[!TIP]
>
>Si la campaña forma parte de un portafolio híbrido, la práctica recomendada es utilizar objetivos de nivel de campaña que coincidan con los objetivos de conversión del objetivo del portafolio; incluir objetivos de conversión adicionales puede afectar al rendimiento del portafolio.
>
> Sin embargo, para las campañas en portafolios híbridos para las que [carga objetivos en la red de anuncios](/help/search-social-commerce/tools/objective-upload-to-networks.md), haz lo siguiente en el editor de la red de anuncios en lugar de aquí: a) agrega la métrica de objetivos de portafolios de Search, Social y Commerce cargada (que comienza con &quot;O_ACS_OBJ&quot;) como objetivo de conversión para la campaña, y b) agrega cualquier objetivo de campaña que incluya conversiones rastreadas por la etiqueta de seguimiento universal de eventos (UET) de [!DNL Microsoft Advertising] porque las métricas rastreadas en la red de anuncios no se cargan en la red de anuncios con el objetivo.

>[!MORELIKETHIS]
>
>* [Administrar campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
