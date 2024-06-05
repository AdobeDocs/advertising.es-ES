---
title: '''[!DNL Google Ads] configuración de campaña"'
description: Haga referencia a la configuración de [!DNL Google Ads] campañas.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: fd5a78a0eb2982ee85ca2d2b6a3cd79a0821d965
workflow-type: tm+mt
source-wordcount: '2424'
ht-degree: 0%

---

# [!DNL Google Ads] configuración de campaña

## \[Pantalla de creación de campaña\]

**[!UICONTROL Campaign Type]:** (Disponible solo durante la creación de la campaña) Dónde colocar los anuncios y qué tipos de anuncios puede contener la campaña:

* *[!UICONTROL Search Network Only]:* Muestra anuncios en la red de búsqueda, que incluye [!DNL Google] buscar resultados y, opcionalmente, buscar sitios de socios. Debe especificar palabras clave para cada grupo de publicidad.

* *[!UICONTROL Search with Display Select]:* Muestra anuncios en la red de búsqueda (que incluye [!DNL Google] resultados de búsqueda y, opcionalmente, buscar sitios de socios) y muestra anuncios en sitios de red. En la red de visualización, [!DNL Google Ads] muestra sus anuncios de forma selectiva mediante ofertas automatizadas, independientemente de la estrategia de oferta de la campaña. Para los anuncios de búsqueda, especifique palabras clave para cada grupo de anuncios; para los anuncios en pantalla, especifique ubicaciones y, opcionalmente, especifique palabras clave para cada grupo de anuncios.

* *[!UICONTROL Shopping Network]:* Muestra anuncios de productos, que [!DNL Google] genera automáticamente en función de sus productos en [!DNL Google Merchant Center] el [!DNL Google Shopping], el área junto a [!DNL Google] buscar resultados (aparte de anuncios de texto) y (opcionalmente) buscar sitios web de socios. Para cada grupo de publicidad de la campaña, puede especificar los grupos de productos que desea anunciar.

* *[!UICONTROL Display Network Only]:* Muestra anuncios en la red de visualización. Para cada grupo de anuncios, debe especificar ubicaciones y, opcionalmente, puede especificar palabras clave.

* *[!UICONTROL Performance Max]:* Muestra y optimiza las conversiones de las publicidades en los distintos canales mediante [!DNL Google Ads] oferta inteligente. En la configuración de la campaña, debe especificar uno o más grupos de recursos, que incluyen imágenes, logotipos, titulares, descripciones, vídeos opcionales y señales de audiencia. [!DNL Google Ads] combina automáticamente los recursos para publicar anuncios en función del canal (por ejemplo, [!DNL YouTube], [!DNL Gmail], o [!DNL Search]).

  **Notas:**

   * Solo están disponibles las configuraciones necesarias. Para obtener una configuración opcional, inicie sesión en [!DNL Google Ads] editor.

   * Vínculos a [!DNL Google Merchant Center] las fuentes de productos de no son compatibles.

   * La compatibilidad con la lista de grupos no está disponible. Para administrar y ver los datos de los grupos de listas, inicie sesión en [!DNL Google Ads] editor.

   * Se admite la optimización híbrida. Los objetivos de la estrategia de oferta y los presupuestos de campaña se establecen en el nivel de campaña.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Un nombre de campaña único en la cuenta.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Solo campañas de Gmail existentes y de solo lectura) Si se desea:

* *[!UICONTROL Target and Bid]* Para mostrar anuncios solo a usuarios asociados con audiencias de destino que también cumplan cualquier otro objetivo para el grupo de anuncios.

* *[!UICONTROL Bid Only]:*  Para mostrar anuncios incluso a personas que no están asociadas con audiencias de destinatario, siempre y cuando satisfagan otros objetivos de nivel de grupo de anuncios. Sin embargo, puedes aumentar las probabilidades de que se muestren anuncios a audiencias específicas si estableces pujas más altas para esas audiencias.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *Pausado*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campañas dirigidas únicamente a la red de búsqueda, incluidas las campañas de compra) Muestra sus anuncios en las redes de socios de búsqueda de la red de anuncios. De forma predeterminada, esta opción es *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** La estrategia de oferta para la campaña:

* *[!UICONTROL Enhanced CPC]:* (No disponible para rendimiento máximo o existente, solo lectura) [!DNL Gmail] campañas) Utiliza el modelo de coste por clic mejorado (eCPC) de la red de publicidad, que permite que la red de publicidad cambie automáticamente la oferta de coste por clic (CPC) para cada subasta en un intento de maximizar las conversiones, utilizando las conversiones especificadas dentro de la red de publicidad (no en Búsqueda, Social y Commerce), al tiempo que intenta mantener su CPC promedio por debajo de su CPC máximo.

Cuando agrega una campaña con eCPC a un portafolio optimizado de Search, Social y Commerce, Search, Social y Commerce optimiza las ofertas de base y cuando el &quot;[!UICONTROL Auto adjust campaign budget limits]La opción &quot; está activada: el presupuesto de la campaña. La red de anuncios optimiza todos los ajustes de oferta y puede cambiar las ofertas generadas por Search, Social y Commerce en el momento de la consulta del usuario en función de los datos propietarios y las perspectivas. **Precaución:** Utilice campañas eCPC en portafolios solo cuando las conversiones totales rastreadas en la red de publicidad se alineen con el objetivo del portafolio. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (el valor predeterminado): (No disponible para campañas Máximo rendimiento de ) Utiliza el modelo de coste por clic (CPC). Si lo desea, puede permitir que la red de anuncios cambie las ofertas de la campaña:

   * **[!UICONTROL Enable Enhanced CPC]** (desactivado de forma predeterminada): Es lo mismo que usar el &quot;[!UICONTROL Enhanced CPC]Opción &quot;.

* *[!UICONTROL Maximize Clicks]:* (Campañas de búsqueda, visualización y compras) La red de anuncios, no de búsqueda, medios sociales y Commerce, optimiza las ofertas para maximizar los clics. Si lo desea, introduzca un **[!UICONTROL Max CPC]** (coste por clic) para garantizar que la red de publicidad no pague más de una cantidad específica por cada clic. **Precaución:** Al añadir una campaña con esta estrategia a un portafolio, las ofertas se basan en la ponderación de los clics, no en el objetivo del portafolio.

* *[!UICONTROL Maximize Conversion Value]:* (Campañas de búsqueda, rendimiento máximo y compras inteligentes) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para maximizar el valor de conversión. Si lo desea, introduzca un **[!UICONTROL Target Return on Ad Spend]** (ROAS) como porcentaje. **Nota:** Utilice esta opción para campañas en portafolios híbridos, pero no estándar.

* *[!UICONTROL Maximize Conversions]:* (Campañas de búsqueda, visualización y rendimiento máximo) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para maximizar las conversiones. Si lo desea, introduzca un **[!UICONTROL Target CPA]** (coste por adquisición). **Nota:** Utilice esta opción para campañas en portafolios híbridos, pero no estándar.

* *[!UICONTROL Target CPA]:* (Mostrar campañas; campañas de búsqueda existentes) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas según un **[!UICONTROL Target CPA]** (coste por adquisición), que es la cantidad promedio de 30 días que desea pagar por una adquisición (conversión). **Nota:** Utilice esta opción para campañas en portafolios híbridos (pero no estándar) con cualquier estrategia de gasto excepto [!UICONTROL Weekly] o [!UICONTROL Google Target CPA].

  Los datos de oferta de CPC y posición promedio no están disponibles para campañas con esta estrategia de oferta.

  Para nuevas campañas de búsqueda, [!DNL Google Ads] ha sustituido esta estrategia de oferta por la [!UICONTROL Maximize Conversions] estrategia usar un [!UICONTROL Target CPA] valor. Para las campañas de búsqueda existentes con esta estrategia, puede editar solo el valor del objetivo y, al hacerlo, cambia la estrategia a [!UICONTROL Maximize Conversions] estrategia utilizando el especificado [!UICONTROL Target CPA] valor.

* *[!UICONTROL Target Impression Share]:* (Campañas de búsqueda) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas para lograr un porcentaje de impresión y una posición de anuncio objetivo. Si lo desea, introduzca un **[!UICONTROL Target Impression Share]** como porcentaje, la variable **[!UICONTROL Target Ad Position]**, y a **[!UICONTROL Max CPC]** (coste por clic). **Nota:** Esta opción no se admite en portafolios.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campañas de visualización y de compra; campañas de búsqueda existentes) La red de anuncios (no Buscar, Social y Commerce) optimiza las ofertas en función de un determinado **[!UICONTROL Target ROAS]** (retorno de la inversión en publicidad), especificado como porcentaje. **Nota:** Utilice esta opción para campañas en portafolios híbridos (pero no estándar) con cualquier estrategia de gasto excepto [!UICONTROL Weekly] o [!UICONTROL Google Target ROAS].

  Los datos de oferta de CPC y posición promedio no están disponibles para campañas con esta estrategia de oferta.

  Para nuevas campañas de búsqueda, [!DNL Google Ads] ha sustituido esta estrategia de oferta por la [!UICONTROL Maximize Conversion Value] estrategia usar un [!UICONTROL Target Return on Ad Spend value]. Para las campañas de búsqueda existentes con esta estrategia, puede editar solo el valor del objetivo y, al hacerlo, cambia la estrategia a [!UICONTROL Maximize Conversion Value] estrategia utilizando el especificado [!UICONTROL Target Return on Ad Spend] valor.

* *[!UICONTROL Viewable CPM]:* (Existente, solo lectura) [!DNL Gmail] (solo campañas de ) La red de anuncios (no Buscar, Social y Commerce) solo oferta anuncios que se miden como visibles. **Nota:** La optimización para esta estrategia no se admite en ningún tipo de portafolio.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Solo campañas de compra; solo lectura para campañas existentes) El país en el que se venden los productos de la campaña. Dado que los productos están asociados a países de destino, esta configuración determina qué productos se anuncian en la campaña.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Solo campañas de compras; los anunciantes que ya participan en el programa de compras local con [!DNL Google Merchant Center] tiendas en los EE.UU., Reino Unido, DE, FR, JP y AU; opcional) Permite [!DNL Google Ads] para añadir automáticamente la información de inventario local a los anuncios de compra en Google.com.

**Sugerencia:** Si utiliza esta configuración, no excluya los anuncios locales en [!UICONTROL Inventory Filter] configuración.

**Nota:** Los anuncios de inventario local requieren dos fuentes adicionales para [!DNL Google Merchant Center] — uno con los datos del producto local y otro con el inventario del producto local. Consulte la [!DNL Google Ads] para obtener más información acerca de [anuncios de compras locales](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Solo redes de búsqueda y visualización) Uno o más idiomas de destino para los anuncios de la campaña.

[!DNL Google Ads] determina el idioma de un usuario a partir del [!DNL Google] la configuración de idioma o el idioma de la consulta de búsqueda, la página actual o las páginas vistas recientemente en la [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Ubicaciones geográficas específicas de los usuarios que se incluirán o excluirán como destinos. De forma predeterminada, todas las ubicaciones están segmentadas. Puede incluir y excluir usuarios en cualquier combinación de ubicaciones. Las exclusiones siempre anulan las inclusiones.

* Para segmentar todas las ubicaciones, no seleccione ninguna ubicación.

* Para segmentar o excluir ubicaciones específicas:

   * (Países, estados, regiones metropolitanas o ciudades) Haga clic **[!UICONTROL Location Target]** (![Destino de ubicación](/help/search-social-commerce/assets/location-target.png "Destino de ubicación")) y busque las ubicaciones que desea incluir y excluir:

      * Para incluir una ubicación y sus ubicaciones secundarias, haga clic una vez en el círculo adyacente para que aparezca una marca de verificación azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) aparece.

      * Para excluir una ubicación, haga clic dos veces en el círculo adyacente para que la marca de verificación (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) aparece.

      * Para expandir una ubicación en sus subcomponentes (como estados, regiones metropolitanas o ciudades de Estados Unidos), haga clic en el nombre de la ubicación.

      * Para buscar una ubicación, introduzca o pegue al menos los tres primeros caracteres de la ubicación en el campo de entrada. En los resultados de la búsqueda, haga clic en **[!UICONTROL Include]** junto a una ubicación para incluir o **[!UICONTROL Exclude]** situado junto a una ubicación que se excluirá.

   * (Ubicaciones cerca de una dirección; solo destinos incluidos) Haga clic en **[!UICONTROL Radius Target]** (![Destino de radio](/help/search-social-commerce/assets/radius-target.png "Destino de radio")) y haga clic en **[!UICONTROL Address]**. Introduzca la dirección y el radio en millas o kilómetros alrededor de la dirección de destino y, a continuación, haga clic en **[!UICONTROL Add]**.

   * (Ubicaciones cerca de coordenadas geográficas; solo destinos incluidos) Haga clic **[!UICONTROL Radius Target]** (![Destino de radio](/help/search-social-commerce/assets/radius-target.png "Destino de radio")) y haga clic en **[!UICONTROL Coordinate]**. Introduzca la latitud y longitud y el radio en millas o kilómetros alrededor de la ubicación de destino y, a continuación, haga clic en **[!UICONTROL Add]**.

* (Para añadir un ajuste de oferta para una ubicación de destino incluida) Introduzca un valor de ajuste de oferta:

* 0%: para no ajustar las pujas de los anuncios en esta ubicación.

* \[Otros valores del -90% al 300%\]: Para aumentar o reducir la oferta de anuncios en esta ubicación.

**Nota:**

* Search, Social y Commerce no proporcionan ajustes de oferta ajustados automáticamente para los siguientes objetivos de ubicación debido a limitaciones en los datos que [!DNL Google Ads] permite asignar ubicaciones de internauta a destinos de ubicación:

   * Dianas de radio.

   * Algunas ubicaciones por debajo del nivel de estado/provincia/región/condado/prefectura para las que [!DNL Google Ads] no envía una ubicación principal en la dirección URL del internauta, incluidos los aeropuertos y los distritos parlamentarios de Estados Unidos.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Solo red de visualización) Operadores de telefonía móvil específicos que se van a segmentar; los operadores se ordenan por país. Si no selecciona ninguno, todos son de destino.

**[!UICONTROL Mobile Carriers]:** (Mostrar solo la red) Sistemas operativos específicos de destino. Si no selecciona ninguno, todos son de destino.

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

**[!UICONTROL Track Product Group]:** (Para [!UICONTROL EF Redirect] solo) No implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (por grupo de recursos)

**[!UICONTROL Asset Group Name]:** Nombre del grupo de recursos. Vínculos a [!DNL Google Merchant Center] las fuentes de productos de no son compatibles.

**[!UICONTROL Asset Group Status]:** El estado del grupo de recursos: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** La dirección URL final de todos los anuncios creados a partir del grupo de recursos. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Hasta 15 imágenes para el anuncio, incluidos los siguientes tamaños: 1) al menos tres imágenes cuadradas, 2) al menos tres imágenes horizontales y 3) al menos una imagen vertical. Consulte la [[!DNL Google Ads] especificaciones de imagen](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Puede cargar imágenes o seleccionarlas en la [!UICONTROL Asset Library] — pero no ambas en la misma operación.

* Para cargar imágenes:

   1. En el [!UICONTROL Upload from Device] pestaña, haga clic en **[!UICONTROL +]** y seleccione imágenes de su dispositivo o red.

   1. Para cada imagen:

      1. Seleccione la relación de aspecto.

      1. Arrastre y coloque el cuadro de recorte según sea necesario para seleccionar la parte visible de la imagen y cambie el tamaño de la parte visible de la imagen según sea necesario siempre que sea posible.

      1. (Opcional) Seleccione relaciones de aspecto adicionales y, opcionalmente, cambie la posición y el tamaño de la imagen según sea necesario para cada relación de aspecto seleccionada.

         Se crea un recurso para cada relación de aspecto seleccionada.

      1. Clic **[!UICONTROL Proceed]**.

   1. Cuando haya terminado de especificar imágenes, haga clic en **[!UICONTROL Upload]**.

* Para seleccionar imágenes de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione las imágenes.

**[!UICONTROL Logos]:** Al menos un logotipo cuadrado (1:1) y un logotipo horizontal (4:1). Se pueden incluir hasta cinco de cada tamaño. Consulte la [[!DNL Google Ads] especificaciones del logotipo](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Puede cargar imágenes o seleccionarlas en la [!UICONTROL Asset Library] — pero no ambas en la misma operación.

* Para cargar imágenes:

   1. En el [!UICONTROL Upload from Device] pestaña, haga clic en **[!UICONTROL +]** y seleccione imágenes de su dispositivo o red.

   1. Para cada imagen:

      1. Seleccione la relación de aspecto.

      1. Arrastre y coloque el cuadro de recorte según sea necesario para seleccionar la parte visible de la imagen y cambie el tamaño de la parte visible de la imagen según sea necesario siempre que sea posible.

      1. (Opcional) Seleccione relaciones de aspecto adicionales y, opcionalmente, cambie la posición y el tamaño de la imagen según sea necesario para cada relación de aspecto seleccionada.

         Se crea un recurso para cada relación de aspecto seleccionada.

      1. Clic **[!UICONTROL Proceed]**.

   1. Cuando haya terminado de especificar imágenes, haga clic en **[!UICONTROL Upload]**.

* Para seleccionar imágenes de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione las imágenes.

**[!UICONTROL Videos]:** (Opcional) Al menos uno y hasta cinco, [!DNL YouTube] vídeos que tengan una duración mínima de 10 segundos. Puede introducir direcciones URL o seleccionarlas en la [!UICONTROL Asset Library] — pero no ambas en la misma operación.

* Para introducir direcciones URL:

   1. En el [!UICONTROL Enter Video Url] , introduzca una dirección URL.

   1. (Opcional) Para agregar otra dirección URL, haga clic en **[!UICONTROL + Add]** e introduzca la dirección URL.

* Para seleccionar vídeos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los vídeos.

**[!UICONTROL Headlines]:** Al menos tres, y hasta cinco, titulares cortos con un máximo de 30 caracteres cada uno. Al menos un titular debe tener al menos 15 caracteres o menos. Si la opción de nivel de campaña para habilitar la expansión final de la URL se establece en [!DNL Google Ads], entonces [!DNL Google Ads] reemplaza este valor con un titular personalizado basado en el contenido de la página de aterrizaje.

Puede introducir texto o seleccionar recursos de su [!UICONTROL Asset Library] — pero no ambas en la misma operación.

* Para introducir texto:

   1. En el [!UICONTROL Enter Text] , introduzca el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Long Headlines]:** Al menos uno y hasta cinco titulares largos con un máximo de 90 caracteres cada uno. Puede introducir texto o seleccionar recursos de su [!UICONTROL Asset Library] — pero no ambas en la misma operación.

* Para introducir texto:

   1. En el [!UICONTROL Enter Text] , introduzca el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Descriptions]:** Al menos dos y hasta cuatro descripciones con un máximo de 90 caracteres cada una. Al menos una descripción debe tener 30 caracteres o menos. Puede introducir texto o seleccionar recursos de su [!UICONTROL Asset Library] — pero no ambas en la misma operación.

* Para introducir texto:

   1. En el [!UICONTROL Enter Text] , introduzca el texto.

   1. (Opcional) Para agregar otra cadena de texto, haga clic en **[!UICONTROL + Add]** e introduzca la cadena.

* Para seleccionar recursos de su [!UICONTROL Asset Library], haga clic en **[!UICONTROL Asset Library]** y seleccione los recursos.

**[!UICONTROL Call to Action]:** Llamada a acción para incluir en el anuncio. De forma predeterminada, *[!UICONTROL Automated]* está seleccionado, y [!DNL Google Ads] selecciona la llamada a la acción. Si lo desea, puede elegir una acción diferente.

**[!UICONTROL Business Name]:** El nombre comercial, con un máximo de 25 caracteres.

**[!UICONTROL Audience Signal]:** (Opcional) [!DNL Google Ads] audiencias que se utilizarán como señales de audiencia para la campaña. [!DNL Google Ads] los modelos de aprendizaje automático utilizan las audiencias para buscar internautas similares a target y también pueden mostrar anuncios a audiencias que no están especificadas como señales para ayudarle a alcanzar sus objetivos de rendimiento. Elija las audiencias que tienen más probabilidades de convertirse.

>[!NOTE]
>Las señales de audiencia son diferentes de [objetivos de audiencia a nivel de campaña y de grupo de publicidad](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Permite especificar otro grupo de recursos.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Si se desea *[!UICONTROL Use account conversion goals for this campaign]* (el valor predeterminado) o *[!UICONTROL Use campaign specific conversion goals]*. Si decide especificar objetivos de conversión para la campaña, seleccione objetivos estándar o cree un objetivo personalizado para la campaña.

Los objetivos se sincronizan a diario, por lo que es posible que no se incluyan en la lista los objetivos existentes creados en las 24 horas anteriores. Para actualizar la lista, [sincronizar manualmente los datos de red de anuncios](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Para crear un objetivo de conversión personalizado, haga clic en **[!UICONTROL + Add custom goal]**, introduzca el nombre de la meta personalizada, seleccione [acciones de conversión](https://support.google.com/google-ads/answer/6032150) para incluir en el objetivo personalizado y, a continuación, haga clic en **[!UICONTROL Save]**. **Nota:** Cada campaña solo puede tener un objetivo personalizado.

>[!TIP]
>
>Para las campañas en portafolios híbridos para las que carga objetivos en la red de publicidad, la práctica recomendada es utilizar objetivos de nivel de campaña que coincidan con los objetivos de conversión del objetivo del portafolio. Sin embargo, si los objetivos de la campaña incluyen [!DNL Google]Conversiones rastreadas por y, a continuación, agréguelas dentro de [!DNL Google Ads] editor porque no se vuelven a cargar en la red de anuncios con el objetivo. Además, dentro de [!DNL Google Ads] Para eliminar las acciones de conversión de la campaña como objetivos predeterminados de la cuenta, márquelas como objetivos secundarios (no principales).

<!-- Check on this:
>If the campaign is part of a hybrid portfolio, then use only conversion goals that are included in the portfolio's objective for the campaign. Including additional conversion goals may impact portfolio performance.
>
>The objective may include conversion goals or other conversions that aren't included for the campaign, but the campaign can't include conversion goals that aren't included in the objective.
-->

>[!MORELIKETHIS]
>
>* [Administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

