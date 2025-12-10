---
title: '[!DNL Google Ads] configuración de campaña'
description: Hacer referencia a la configuración de  [!DNL Google Ads] campañas.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '2617'
ht-degree: 0%

---

# [!DNL Google Ads] configuración de campaña

## \[Pantalla de creación de campaña\]

**[!UICONTROL Campaign Type]:** (disponible solo durante la creación de la campaña) Dónde colocar los anuncios y qué tipos de anuncios puede contener la campaña:

* *[!UICONTROL Search Network Only]:* Muestra anuncios en la red de búsqueda, que incluye [!DNL Google] resultados de búsqueda y, opcionalmente, sitios asociados de búsqueda. Debe especificar palabras clave para cada grupo de publicidad.

* *[!UICONTROL Search with Display Select]:* Muestra anuncios en la red de búsqueda (que incluye [!DNL Google] resultados de búsqueda y, opcionalmente, sitios de socios de búsqueda) y potencialmente muestra anuncios en sitios de red de visualización. En la red de visualización, [!DNL Google Ads] muestra tus anuncios de forma selectiva mediante pujas automatizadas, independientemente de la estrategia de puja de la campaña. Para los anuncios de búsqueda, especifique palabras clave para cada grupo de anuncios; para los anuncios en pantalla, especifique ubicaciones y, opcionalmente, especifique palabras clave para cada grupo de anuncios.

* *[!UICONTROL Shopping Network]:* Muestra anuncios de productos, que [!DNL Google] genera automáticamente basándose en los productos de [!DNL Google Merchant Center] en [!DNL Google Shopping], el área junto a [!DNL Google] resultados de búsqueda (separados de los anuncios de texto) y (opcionalmente) sitios web de socios de búsqueda. Para cada grupo de publicidad de la campaña, puede especificar los grupos de productos que desea anunciar.

* *[!UICONTROL Display Network Only]:* Muestra anuncios en la red de visualización. Para cada grupo de anuncios, debe especificar ubicaciones y, opcionalmente, puede especificar palabras clave.

* *[!UICONTROL Performance Max]:* Muestra y optimiza las conversiones de los anuncios en los distintos canales mediante pujas inteligentes de [!DNL Google Ads]. En la configuración de la campaña, debe especificar uno o más grupos de recursos, que incluyen imágenes, logotipos, titulares, descripciones, vídeos opcionales y señales de audiencia. [!DNL Google Ads] combina automáticamente los recursos para publicar anuncios basados en el canal (como [!DNL YouTube], [!DNL Gmail] o [!DNL Search]).

  **Notas:**

   * Solo están disponibles las configuraciones necesarias. Para obtener una configuración opcional, inicie sesión en el editor [!DNL Google Ads].

   * No se admiten vínculos a [!DNL Google Merchant Center] fuentes de productos.

   * La compatibilidad con la lista de grupos no está disponible. Para administrar y ver los datos de los grupos de listas, inicie sesión en el editor [!DNL Google Ads].

   * Se admite la optimización híbrida. Los objetivos de la estrategia de oferta y los presupuestos de campaña se establecen en el nivel de campaña.

## [!UICONTROL Campaign Details]

<!-- left to right -->

**[!UICONTROL Campaign Name]:** Un nombre de campaña único en la cuenta.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *En pausa*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campañas dirigidas únicamente a la red de búsqueda, incluidas las campañas de compras) Muestra sus anuncios en las redes de socios de búsqueda de la red de anuncios. De manera predeterminada, esta opción es *[!UICONTROL Off]*.

**[!UICONTROL Audience Target Method]:**(Existentes, solo campañas de Gmail de solo lectura) Si se desea:

* *[!UICONTROL Target and Bid]* Para mostrar anuncios solamente a usuarios asociados con audiencias de destino que también cumplan otros objetivos para el grupo de anuncios.

* *[!UICONTROL Bid Only]:* Para mostrar anuncios incluso a personas que no están asociadas con audiencias de destino siempre y cuando satisfagan otros objetivos de nivel de grupo de anuncios. Sin embargo, puedes aumentar las probabilidades de que se muestren anuncios a audiencias específicas si estableces pujas más altas para esas audiencias.

**[!UICONTROL Contains EU Political Ads]:**(Aplicable a las campañas destinadas a audiencias en la Unión Europea (UE)) Si la campaña contiene o no publicidad política según los requisitos para los anuncios publicados en la Unión Europea según la normativa de la UE 2024/90: *[!UICONTROL Yes]* o *[!UICONTROL No]*.

**[!UICONTROL AI Max Enabled]:** (Campañas dirigidas solo a la red de búsqueda; solo lectura) Indica si la característica [[!UICONTROL AI Max] &#x200B;](https://support.google.com/google-ads/answer/15910366) está habilitada: *[!UICONTROL On]* o *[!UICONTROL Off]*.

**[!UICONTROL AI Max Bundling]:** (Campañas dirigidas solo a la red de búsqueda; campañas con la función AI Max habilitada; solo lectura) Si se requiere el agrupamiento: *[!UICONTROL Not Required]*, *[!UICONTROL Required]*, *[!UICONTROL Unknown]* o *[!UICONTROL Unspecified]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

**[!UICONTROL Google Recommended Budget]:** (opcional; aplicable para campañas de búsqueda y rendimiento máximo con toda la configuración necesaria y que solo incluyen grupos de anuncios) Haga clic en **[!UICONTROL Show Recommendation]** para ver el presupuesto que recomienda [!DNL Google Ads]. Actualmente, solo son elegibles las campañas con menos de 40 000 palabras clave.

Para las campañas Máximo rendimiento y de búsqueda, se requiere la siguiente configuración para las recomendaciones:

* tipo de estrategia de oferta
* URL final
* grupos de recursos

Para las campañas de búsqueda, también se requiere la siguiente configuración adicional para las recomendaciones:

* objetivo de estrategia de oferta
* país
* idioma
* una ubicación incluida o excluida
* palabras clave

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Estrategia de oferta para la campaña:

* *[!UICONTROL Enhanced CPC]:* obsoleto. [!DNL Google Ads] comenzó a cambiar automáticamente las [estrategias mejoradas de oferta de CPC](https://support.google.com/google-ads/answer/2464964) existentes por CPC manual el 15 de marzo de 2025.

* *[!UICONTROL Manual CPC]* (predeterminado): (no disponible para campañas Máximo rendimiento) Utiliza el modelo de coste por clic (CPC). Si lo desea, puede permitir que la red de anuncios cambie las ofertas de la campaña:

   * **[!UICONTROL Enable Enhanced CPC]** (deshabilitado de forma predeterminada): Es lo mismo que usar la opción &quot;[!UICONTROL Enhanced CPC]&quot;, que está obsoleta. [!DNL Google Ads] comenzó a cambiar automáticamente las [estrategias mejoradas de oferta de CPC](https://support.google.com/google-ads/answer/2464964) existentes por CPC manual el 15 de marzo de 2025.

* *[!UICONTROL Maximize Clicks]:* (campañas de búsqueda, visualización y compras) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para maximizar los clics. De manera opcional, escriba **[!UICONTROL Max CPC]** (costo por clic) para asegurarse de que la red publicitaria no pague más de una cantidad determinada por cada clic. **Precaución:** Al agregar una campaña con esta estrategia a un portafolio, las ofertas dependen de la ponderación de los clics, no del objetivo del portafolio.

* *[!UICONTROL Maximize Conversion Value]:* (campañas de búsqueda, rendimiento máximo y compras inteligentes) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para maximizar el valor de conversión. Si lo desea, escriba un **[!UICONTROL Target Return on Ad Spend]** (ROAS) como porcentaje. **Nota:** Utilice esta opción para campañas en portafolios híbridos, pero no en portafolios estándar. En portafolios híbridos, Search, Social y Commerce optimizan el ROAS de Target a nivel de campaña o (cuando está disponible) a nivel de grupo de anuncios.

* *[!UICONTROL Maximize Conversions]:* (campañas de búsqueda, visualización y rendimiento máximo) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para maximizar las conversiones. Opcionalmente, escriba **[!UICONTROL Target CPA]** (costo por adquisición). **Nota:** Utilice esta opción para campañas en portafolios híbridos, pero no en portafolios estándar. En portafolios híbridos, Search, Social y Commerce optimizan la CPA de Target a nivel de campaña o (cuando está disponible) a nivel de grupo de anuncios.

* *[!UICONTROL Target CPA]:* (Campañas de visualización) La red de anuncios (no Buscar, Social ni Commerce) optimiza las ofertas según un **[!UICONTROL Target CPA]** opcional (coste por adquisición), que es la cantidad promedio de 30 días que desea pagar por una adquisición (conversión). **Nota:** Utilice esta opción para campañas en portafolios híbridos (pero no en portafolios estándar) con cualquier estrategia de gasto excepto [!UICONTROL Weekly] o [!UICONTROL Google Target CPA]. En portafolios híbridos, Search, Social y Commerce optimizan la CPA de Target a nivel de campaña o (cuando está disponible) a nivel de grupo de anuncios.

  Los datos de oferta de CPC y posición promedio no están disponibles para campañas con esta estrategia de oferta.

* *[!UICONTROL Target Impression Share]:* (Campañas de búsqueda) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para lograr un porcentaje de impresión objetivo y una posición de anuncio. De manera opcional, escriba **[!UICONTROL Target Impression Share]** como porcentaje, **[!UICONTROL Target Ad Position]** y **[!UICONTROL Max CPC]** (costo por clic). **Nota:** Esta opción no se admite en portafolios.

* *[!UICONTROL Target Return on Ad Spend]:* (Campañas de visualización y compras) La red de anuncios, no de búsqueda, social y Commerce, optimiza las ofertas según un **[!UICONTROL Target ROAS]** especificado (retorno de la inversión en publicidad), especificado como porcentaje. **Nota:** Utilice esta opción para campañas en portafolios híbridos (pero no en portafolios estándar) con cualquier estrategia de gasto excepto [!UICONTROL Weekly] o [!UICONTROL Google Target ROAS]. En portafolios híbridos, Search, Social y Commerce optimizan el ROAS de Target a nivel de campaña o (cuando está disponible) a nivel de grupo de anuncios.

  Los datos de oferta de CPC y posición promedio no están disponibles para campañas con esta estrategia de oferta.

* *[!UICONTROL Viewable CPM]:* (solo campañas existentes de solo lectura de [!DNL Gmail]) La red de anuncios (no Buscar, Social y Commerce) solo oferta anuncios que se miden como visibles. **Nota:** La optimización de esta estrategia no se admite en ningún tipo de portafolio.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Solo campañas de compras; solo lectura para campañas existentes) El país en el que
se venden los productos de la campaña. Dado que los productos están asociados a países de destino, esta configuración determina qué productos se anuncian en la campaña.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Solo campañas de compras; anunciantes que ya participan en el programa de compras local con [!DNL Google Merchant Center] tiendas en EE. UU., Reino Unido, DE, FR, JP y AU; opcional) Permite que [!DNL Google Ads] agregue automáticamente la información de inventario local a sus anuncios de compras en Google.com.

**Sugerencia:** Si usa esta configuración, no excluya los anuncios locales en la configuración [!UICONTROL Inventory Filter].

**Nota:** Los anuncios de inventario local requieren dos fuentes adicionales para [!DNL Google Merchant Center]: una con los datos del producto local y otra con el inventario del producto local. Consulte la documentación de [!DNL Google Ads] para obtener más información sobre [anuncios de compras locales](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (solo redes de búsqueda y visualización) Uno o más idiomas de destino para los anuncios de la campaña.

[!DNL Google Ads] determina el idioma de un usuario a partir de la configuración de idioma de [!DNL Google] del usuario o del idioma de la consulta de búsqueda, la página actual o las páginas vistas recientemente en [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Ubicaciones geográficas de usuarios específicas para incluir o excluir como destinos. De forma predeterminada, todas las ubicaciones están segmentadas. Puede incluir y excluir usuarios en cualquier combinación de ubicaciones. Las exclusiones siempre anulan las inclusiones.

* Para segmentar todas las ubicaciones, no seleccione ninguna ubicación.

* Para segmentar o excluir ubicaciones específicas:

   * (Países, estados, regiones metropolitanas o ciudades) Haga clic en **[!UICONTROL Location Target]** (![Destinatario de ubicación](/help/search-social-commerce/assets/location-target.png "Destinatario de ubicación")) y busque las ubicaciones que desee incluir y excluir:

      * Para incluir una ubicación y sus ubicaciones secundarias, haga clic una vez en el círculo adyacente para que aparezca una marca de verificación azul (![Include](/help/search-social-commerce/assets/include.png "Include")).

      * Para excluir una ubicación, haga clic dos veces en el círculo adyacente para que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")).

      * Para expandir una ubicación en sus subcomponentes (como estados, regiones metropolitanas o ciudades de Estados Unidos), haga clic en el nombre de la ubicación.

      * Para buscar una ubicación, introduzca o pegue al menos los tres primeros caracteres de la ubicación en el campo de entrada. En los resultados de búsqueda, haga clic en **[!UICONTROL Include]** al lado de la ubicación que desee incluir o en **[!UICONTROL Exclude]** al lado de la ubicación que desee excluir.

   * (Ubicaciones cerca de una dirección; solo destinos incluidos) Haga clic en **[!UICONTROL Radius Target]** (![Destino de radio](/help/search-social-commerce/assets/radius-target.png "Destino de radio")) y, a continuación, haga clic en **[!UICONTROL Address]**. Escriba la dirección y el radio en millas o kilómetros alrededor de la dirección de destino y haga clic en **[!UICONTROL Add]**.

   * (Ubicaciones cerca de coordenadas geográficas; solo destinos incluidos) Haga clic en **[!UICONTROL Radius Target]** (![Destino de radio](/help/search-social-commerce/assets/radius-target.png "Destino de radio")) y, a continuación, haga clic en **[!UICONTROL Coordinate]**. Especifique la latitud, longitud y radio en millas o kilómetros alrededor de la ubicación de destino y, a continuación, haga clic en **[!UICONTROL Add]**.

* (Para añadir un ajuste de oferta para una ubicación de destino incluida) Introduzca un valor de ajuste de oferta:

* 0%: para no ajustar las pujas de los anuncios en esta ubicación.

* \[Otros valores del -90% al 300%\]: Para aumentar o reducir la oferta de anuncios en esta ubicación.

**Nota:**

* Search, Social y Commerce no proporcionan ajustes de oferta ajustados automáticamente para los siguientes destinos de ubicación debido a limitaciones en los datos que [!DNL Google Ads] proporciona para asignar ubicaciones de internauta a destinos de ubicación:

   * Dianas de radio.

   * Algunas ubicaciones por debajo del nivel de estado/provincia/región/condado/prefectura para las cuales [!DNL Google Ads] no envía una ubicación principal en la dirección URL del internauta, incluidos los aeropuertos y los distritos electorales del Congreso de los Estados Unidos.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Solo red de visualización) Operadores de telefonía móvil específicos para el destino; los operadores se ordenan
por país. Si no selecciona ninguno, todos son de destino.

**[!UICONTROL Mobile Carriers]:** (Mostrar solo red) Sistemas operativos específicos de destino. Si no selecciona ninguno, todos son de destino.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Customer Acquisition Goals]

**[!UICONTROL Customer Acquisition]:** (Rendimiento máximo y campañas de búsqueda solamente) Cómo asignar ofertas para clientes nuevos y existentes:

* *[!UICONTROL Bid equally for new and existing customers]*

* *[!UICONTROL Bid higher for new customers than for existing customers]*

  **Nota:** Para usar esta configuración, primero debe activar el nuevo objetivo de adquisición de cliente para la cuenta de [!DNL Google Ads] o, si corresponde, para la cuenta de administrador. El objetivo define las listas de clientes existentes aptas y el valor de conversión adicional para los clientes nuevos en la configuración de conversión. Consulte los pasos 1-2 en la ayuda de [!DNL Google Ads] &quot;[Activar el nuevo objetivo de adquisición de cliente](https://support.google.com/google-ads/answer/14007601)&quot;.

* *[!UICONTROL Only bid for new customers]*

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

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

**[!UICONTROL Asset Group Name]:** Nombre del grupo de recursos. No se admiten vínculos a [!DNL Google Merchant Center] fuentes de productos.

**[!UICONTROL Asset Group Status]:** Estado del grupo de recursos: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** Dirección URL final de todos los anuncios creados a partir del grupo de recursos. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** hasta 15 imágenes para el anuncio, incluidos los siguientes tamaños: 1) al menos tres imágenes cuadradas, 2) al menos tres imágenes horizontales y 3) al menos una imagen vertical. Ver las [[!DNL Google Ads] especificaciones de la imagen](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Puede cargar imágenes o seleccionarlas en su [!UICONTROL Asset Library], pero no ambas en la misma operación.

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

**[!UICONTROL Logos]:** al menos un logotipo cuadrado (1:1) y un logotipo horizontal (4:1). Se pueden incluir hasta cinco de cada tamaño. Ver las [[!DNL Google Ads] especificaciones del logotipo](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Puede cargar imágenes o seleccionarlas en su [!UICONTROL Asset Library], pero no ambas en la misma operación.

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

**[!UICONTROL Videos]:** (opcional) al menos un vídeo de [!DNL YouTube], y hasta cinco vídeos, con una duración mínima de 10 segundos. Puede introducir direcciones URL o seleccionarlas en su [!UICONTROL Asset Library], pero no en ambas operaciones.

* Para introducir direcciones URL:

   1. En la ficha [!UICONTROL Enter Video Url], escriba una dirección URL.

   1. (Opcional) Para agregar otra URL, haga clic en **[!UICONTROL + Add]** e introduzca la URL.

* Para seleccionar vídeos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los vídeos.

**[!UICONTROL Headlines]:** Al menos tres y hasta cinco titulares cortos con un máximo de 30 caracteres cada uno. Al menos un titular debe tener al menos 15 caracteres o menos. Si la opción de nivel de campaña para habilitar la expansión de URL final se establece en [!DNL Google Ads], [!DNL Google Ads] reemplaza este valor con un titular personalizado basado en el contenido de la página de aterrizaje.

Puede escribir texto o seleccionar recursos de su [!UICONTROL Asset Library], pero no ambos en la misma operación.

* Para introducir texto:

   1. En la ficha [!UICONTROL Enter Text], escriba el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Long Headlines]:** Al menos un titular largo, y hasta cinco, con un máximo de 90 caracteres cada uno. Puede escribir texto o seleccionar recursos de su [!UICONTROL Asset Library], pero no ambos en la misma operación.

* Para introducir texto:

   1. En la ficha [!UICONTROL Enter Text], escriba el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Descriptions]:** Al menos dos y hasta cuatro descripciones con un máximo de 90 caracteres cada una. Al menos una descripción debe tener 30 caracteres o menos. Puede escribir texto o seleccionar recursos de su [!UICONTROL Asset Library], pero no ambos en la misma operación.

* Para introducir texto:

   1. En la ficha [!UICONTROL Enter Text], escriba el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Call to Action]:** El call to action que se va a incluir en el anuncio. De manera predeterminada, *[!UICONTROL Automated]* está seleccionado y [!DNL Google Ads] selecciona el call to action. Si lo desea, puede elegir una acción diferente.

**[!UICONTROL Business Name]:** El nombre comercial, con un máximo de 25 caracteres.

**[!UICONTROL Audience Signal]:** (Opcional) [!DNL Google Ads] audiencias para usar como señales de audiencia para la campaña. [!DNL Google Ads] modelos de aprendizaje automático utilizan las audiencias para encontrar internautas similares a los de target y también pueden mostrar anuncios a audiencias que no se especifican como señales que le ayudarán a alcanzar sus objetivos de rendimiento. Elija las audiencias que tienen más probabilidades de convertirse.

>[!NOTE]
>Las señales de audiencia son diferentes de [objetivos de audiencia en el nivel de campaña y de grupo de publicidad](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Primary Status]:** (campo de solo lectura para grupos de recursos existentes en campañas Máximo rendimiento) Por qué el grupo de recursos está sirviendo o no a plena capacidad. Tiene en cuenta el estado del grupo de activos, así como otras señales, como las aprobaciones de políticas y de calidad. Los valores pueden incluir *ELEGIBLE,* *LIMITADO,* *NO APTO,* *PAUSADO,* *PENDIENTE,* *ELIMINADO,* *DESCONOCIDO,* o *NO ESPECIFICADO.*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]:** (campo de solo lectura para grupos de recursos existentes en campañas Máximo rendimiento) Detalles adicionales sobre el estado principal del grupo de recursos. Los valores pueden incluir *ASSET_GROUP_DISAPPROVED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,* *ASSET_GROUP_UNDER_REVIEW,* *CAMPAIGN_ENDED,* *CAMPAIGN_PAUSED,* *CAMPAIGN_PENDING,* *CAMPAIGN_REMOVED,* *UNKNOWN,* o *UNSPECIFIED.*

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Ya sea para *[!UICONTROL Use account conversion goals for this campaign]* (predeterminado) o *[!UICONTROL Use campaign specific conversion goals]*. Si decide especificar objetivos de conversión para la campaña, seleccione objetivos estándar o cree un objetivo personalizado para la campaña.

Los objetivos se sincronizan a diario, por lo que es posible que no se incluyan en la lista los objetivos existentes creados en las 24 horas anteriores. Para actualizar la lista, [sincronice manualmente los datos de la red de anuncios](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Para crear un objetivo de conversión personalizado, haga clic en **[!UICONTROL + Add custom goal]**, escriba el nombre del objetivo personalizado, seleccione las [acciones de conversión](https://support.google.com/google-ads/answer/6032150) que desea incluir en el objetivo personalizado y, a continuación, haga clic en **[!UICONTROL Save]**. **Nota:** Cada campaña solo puede tener un objetivo personalizado.

>[!TIP]
>
>Si la campaña forma parte de un portafolio híbrido, la práctica recomendada es utilizar objetivos de nivel de campaña que coincidan con los objetivos de conversión del objetivo del portafolio; incluir objetivos de conversión adicionales puede afectar al rendimiento del portafolio.
>
>Sin embargo, para las campañas en portafolios híbridos para las que [carga objetivos en la red de anuncios](/help/search-social-commerce/tools/objective-upload-to-networks.md), haz lo siguiente en el editor de la red de anuncios en lugar de aquí: a) agrega la métrica de objetivos de portafolios de Search, Social y Commerce cargada (que comienza con &quot;O_ACS_OBJ&quot;) como una acción de conversión para la campaña, y b) agrega cualquier objetivo de campaña que incluya conversiones rastreadas en [!DNL Google], porque las métricas rastreadas en la red de anuncios no se cargan en la red de anuncios con el objetivo.

>[!MORELIKETHIS]
>
>* [Administrar campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
