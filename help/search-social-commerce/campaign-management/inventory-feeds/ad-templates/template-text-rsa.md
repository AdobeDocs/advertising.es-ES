---
title: Configuración de anuncios de texto y plantillas de anuncios de búsqueda adaptables para fuentes de inventario
description: Haga referencia a la configuración de las plantillas de anuncios de búsqueda interactivos y de anuncios de texto para las fuentes de inventario.
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# Configuración de anuncios de texto y plantillas de anuncios de búsqueda adaptables para fuentes de inventario


*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

>[!NOTE]
>
>* Los siguientes caracteres están reservados para designar nombres de columna y nombres de modificador en la plantilla y, por lo tanto, están prohibidos como texto en todos los campos de atributo:  `[ ] < > `
>* Entrada [!DNL Yandex templates], puede utilizar los parámetros dinámicos `{param1}` y `{param2}` solo en direcciones URL y no se puede utilizar la inserción dinámica de precios en las descripciones de los anuncios.

## \[Sobre todas las fichas\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Panel izquierdo\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (Opcional) Asigna todos los grupos de anuncios nuevos (no disponible para [!DNL Yandex]), palabras clave y anuncios a campañas existentes, en lugar de crear campañas. Si activa esta opción, seleccione el método de asignación.

Uso de [!UICONTROL Map Only] a nivel de campaña requiere una estructura de cuentas existente que esté estrechamente vinculada a la taxonomía de productos y se asigne fácilmente a la fuente de datos.

**[!UICONTROL Map Method]:** (Cuándo [!UICONTROL Map Only] está habilitado para la campaña) Método mediante el cual se generan los nuevos grupos de anuncios (no disponible para [!DNL Yandex]), las palabras clave y los anuncios se asignan a campañas existentes:

* *[!UICONTROL Contains Anywhere]:* Agrega datos a una campaña existente cuyo nombre incluye la cadena especificada, si existe.

* *[!UICONTROL Contains Exactly]:* Agrega datos a una campaña existente cuyo nombre incluye la cadena especificada, si existe.

* *[!UICONTROL Exactly Matches]* (predeterminado): Agrega datos a una campaña existente con el mismo nombre, si existe.

Cuando no se encuentran coincidencias, se omiten todos los datos de la campaña. Si se encuentran varias coincidencias de campaña, las palabras clave y los anuncios se asignan a todas ellas.

**[!UICONTROL Campaign Tracking Template]:** (Cuentas solo con direcciones URL finales/avanzadas; opcional) La plantilla de seguimiento de nivel de campaña, que especifica todas las redirecciones de dominios de aterrizaje y los parámetros de seguimiento e incrusta la dirección URL final en un parámetro. Este valor anula la configuración de nivel de cuenta, pero las plantillas de seguimiento a niveles más granulares (con palabra clave como valor más granular) anulan este valor.

* Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload],&quot; Buscar, Social y Commerce anexan automáticamente el código de redireccionamiento y seguimiento al guardar el registro.

* Para incrustar la dirección URL final:

   * ([!DNL Google Ads] y [!DNL Microsoft Advertising] (solo) Para obtener una lista de parámetros que indiquen las direcciones URL finales en las plantillas de seguimiento, consulte el ([!DNL Microsoft Advertising] solo) [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/56799/2) o ([!DNL Google Ads] solo) los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección &quot;Disponible&quot; [!DNL ValueTrack] Parámetros&quot; en el [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] (solo) Utilice el parámetro `!{unescapedurl}` para indicar la dirección URL de la página de aterrizaje.

   * Opcionalmente, puede incluir parámetros de URL y cualquier parámetro personalizado definido para la campaña, separado por el símbolo &amp;, como `{lpurl}?matchtype={matchtype}&device={device}`.

* Para redirecciones y seguimiento de terceros, introduzca un valor.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** (Entrada [!DNL Google Ads] y [!DNL Yandex] configuración de campaña) Las redes en las que se colocarán los anuncios:

* *[!UICONTROL Search]:* Para realizar pujas por anuncios de búsqueda patrocinados.

  ([!DNL Google Ads] campañas) Para incluir pujas en anuncios de [!DNL Google Ads] buscar socios, active la casilla situada junto a **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* Para colocar ofertas de ubicaciones en anuncios de red de contenido (visualización). **Nota:** No se pueden crear ubicaciones con la plantilla. Cuando seleccione esta opción, cree ubicaciones para cada grupo de anuncios y especifique qué páginas de la red de visualización se dirigirán a cada grupo de anuncios mediante <!-- insert link --> hojas de edición masiva <!-- insert links --> configuración de grupo de anuncios y ubicación en [!UICONTROL Search] > [!UICONTROL Campaigns] vistas.

**[!UICONTROL Languages]:** ([!DNL Google Ads] buscar y mostrar solo redes) Uno o más idiomas de destino para los anuncios de la campaña.

[!DNL Google Ads] determina el idioma de un usuario a partir del [!DNL Google] la configuración de idioma o el idioma de la consulta de búsqueda, la página actual o las páginas vistas recientemente en la [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Cuentas solo con direcciones URL finales/avanzadas) La plantilla de seguimiento de nivel de grupo de anuncios, que especifica todas las redirecciones de dominios de aterrizaje y parámetros de seguimiento e incrusta la dirección URL final en un parámetro.

Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload],&quot; Buscar, Social y Commerce anexan automáticamente el código de redireccionamiento y seguimiento al guardar el registro.

Para redirecciones y seguimiento de terceros, introduzca un valor. Para indicar la dirección URL de la página de aterrizaje:

* Para Yahoo! Cuentas de anuncios de Japón, utilice el parámetro {lpurl}.

* Para ver los parámetros disponibles para las cuentas de Microsoft Advertising y Google Ads, consulte la [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/56799) o los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección &quot;Disponible&quot; [!DNL ValueTrack] Parámetros&quot; en el [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/6305348).

Este valor anula la configuración de nivel de cuenta y de campaña, pero las plantillas de seguimiento a niveles más granulares (con palabra clave como valor más granular) anulan este valor.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Palabras clave para el grupo de anuncios especificado (o campaña para [!DNL Yandex] cuentas), que puede consistir en cualquier combinación de texto estático, columnas en el archivo especificado y modificadores. Los nombres y modificadores de columna se sustituyen por datos reales cuando el archivo de fuente especificado se propaga a través de la plantilla.

Para insertar un nombre de columna o un grupo de modificadores como parámetro dinámico, haga clic en el campo de entrada y, a continuación, haga clic en un nombre de columna en la lista de columnas o en un [nombre de modificador](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) en la lista Modificadores. Para especificar varias palabras clave o varios tipos de coincidencia para la misma palabra clave, escríbalas en líneas independientes. Para especificar el tipo de coincidencia de palabra clave, utilice la siguiente sintaxis de tipo de coincidencia alrededor del nombre de la columna:

* Para [!DNL Google Ads], [!DNL Microsoft Advertising], y [!DNL Yahoo! Japan Ads] plantillas:

   * Para parámetros dinámicos: Broad Match = `[keyword]`, Modificador de coincidencia amplia para el primer término de la variable [!UICONTROL Keyword] columna (como +zapatos de ante azul) = `+[keyword]`, Modificador de coincidencia amplia para cada término de la columna Palabra clave (como +azul +ante +zapatos) = `+[keyword]+`, Coincidencia de frase = `"[keyword]"`, Coincidencia exacta = `[[keyword]]`

   * Para palabras clave estáticas: Broad Match = `keyword`, Modificador de coincidencia amplia = `+keyword`, o Coincidencia de frase = `"keyword"`

     Aquí no se pueden escribir palabras clave estáticas con coincidencia exacta y sintaxis de coincidencia estándar porque están entre corchetes (`[]`), al igual que los parámetros dinámicos.

* Para [!DNL Yandex] plantillas:

   * Para parámetros dinámicos: inserte el nombre de la columna, como `[keyword]`. Para indicar el tipo de coincidencia, utilice el [[!DNL Yandex]Sintaxis específica de](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Nota:** Para los términos de coincidencia amplia, utilice la siguiente sintaxis: Modificador de coincidencia amplia para el primer término de la columna Palabra clave (como +zapatos de ante azul) = `+[keyword]`, Modificador de coincidencia amplia para cada término de la columna Palabra clave (como +azul +ante +zapatos) = `+[keyword]+`

   * Para palabras clave estáticas: solo se admiten palabras clave de búsqueda. Utilice el [[!DNL Yandex]Sintaxis específica de](https://yandex.com/support/direct/keywords/symbols-and-operators.html) para la palabra clave. Corchetes (`[]`) para indicar que el orden de las palabras no es compatible.

>[!NOTE]
>
>* Puede incluir manualmente varios valores modificadores en el campo Palabras clave incluyendo entre paréntesis los valores separados por comas antes o después de un parámetro de palabra clave (pero no en ambos lugares). Por ejemplo, `(cheap, discount, affordable)[product]` produce tres anuncios independientes para cada producto.
>* Si no se especifica ningún tipo de coincidencia, se utilizará el tipo de coincidencia predeterminado &quot;broad&quot;.
>* No se admiten coincidencias negativas.
>* Los modificadores de coincidencia amplia de Google ahora tienen el mismo comportamiento de coincidencia de frases para algunos idiomas y no se pueden crear nuevas palabras clave de modificadores de coincidencia amplia. Consulte la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/10286719) para obtener más información.

**[!UICONTROL Map Only]:** Añade anuncios nuevos a grupos de anuncios (o a campañas para [!DNL Yandex] cuentas) en las que se encuentran las palabras clave especificadas, en lugar de crear nuevas palabras clave. Para activar esta opción, marque la casilla de verificación. Cuando esta opción está habilitada, cualquier variable de parámetro 1 y parámetro 2 de las palabras clave especificadas no se aplica porque existen palabras clave.

**[!UICONTROL Keyword Final URL]:** (Cuentas con direcciones URL finales/avanzadas; opcional) Dirección URL de la página de aterrizaje a la que se dirigen los usuarios de la red de anuncios cuando hacen clic en el anuncio. Debe incluir el mismo dominio que la dirección URL mostrada y cualquier parámetro de la dirección URL final debe coincidir con los parámetros de la dirección URL de la página de aterrizaje después de hacer clic en el anuncio. Puede contener redirecciones dentro del dominio o subdominio de la página de aterrizaje, pero no redirecciones fuera de este.

Si usa un [!DNL Google Merchant Center] e incluir este valor en la fuente &quot;[!DNL Link]&quot;, y luego inserte esa columna en este campo.

>[!NOTE]
>
>* Si genera direcciones URL de seguimiento al publicar datos propagados a través de la plantilla, los parámetros de seguimiento se anexan a este valor en función de la configuración de seguimiento de la cuenta.
>* ([!DNL Google Ads] cuentas) Evite utilizar macros que no sustituyan los clics de fuentes que habilitan el seguimiento paralelo. Si el anunciante debe utilizar macros, el equipo de cuenta de Adobe debe trabajar con Asistencia al cliente o con el equipo de implementación para agregarlas.

**[!UICONTROL Keyword Tracking Template]:** (Cuentas con direcciones URL finales/avanzadas; opcional) La plantilla de seguimiento, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, e incrusta la dirección URL final en un parámetro. La plantilla de seguimiento en el nivel más granular (con la palabra clave como valor más granular) anula los valores en todos los demás niveles.

* Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload],&quot; Buscar, Social y Commerce anexan automáticamente el código de redireccionamiento y seguimiento al guardar el registro.

* Si lo desea, puede introducir redirecciones y seguimiento de terceros.

* Para indicar la dirección URL de la página de aterrizaje:

   * ([!DNL Google Ads] y [!DNL Microsoft Advertising] (solo) Para obtener una lista de parámetros que indiquen las direcciones URL finales en las plantillas de seguimiento, consulte el ([!DNL Microsoft Advertising] solo) [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] solo) los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección &quot;Disponible&quot; [!DNL ValueTrack] Parámetros&quot; en el [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] (solo) Utilice el parámetro `!{lpurl}` para indicar la dirección URL de la página de aterrizaje.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] plantillas\]:** ([!DNL Google Ads] sólo plantillas) La columna del archivo especificado que representa el [!DNL Google Ads] `{param1}` o `{param2}` , que puede incluir en la copia del anuncio o mostrar la URL de cualquier anuncio creado a partir de la plantilla. Para insertar el parámetro dinámico, haga clic en el campo de entrada y, a continuación, haga clic en un nombre de columna en la lista de columnas. El nombre de la columna se sustituye por los datos reales cuando el archivo de fuente se propaga a través de la plantilla.

Si utiliza cualquiera de los parámetros, tiene la opción de aplicar el parámetro únicamente a palabras clave nuevas o de actualizar también los valores de palabras clave existentes que no se crearon a partir de la plantilla:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (predeterminado): simplemente inserta el valor del parámetro para las nuevas palabras clave que se crean con la plantilla.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Además de crear nuevas palabras clave a partir de la fuente, Search, Social y Commerce también actualizan el valor del parámetro para todas las palabras clave existentes en el grupo de publicidad que no se crearon con la plantilla. Introduzca un solo valor numérico que se utilice para todas esas palabras clave. La plantilla debe contener al menos una palabra clave.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Además de crear nuevas palabras clave a partir de la fuente, Search, Social y Commerce también actualizan el valor del parámetro para todas las palabras clave existentes en el grupo de anuncios que no se crearon con la plantilla, siempre que el archivo de fuente contenga valores numéricos para el parámetro, con hasta un punto decimal pero sin comas, símbolos o códigos de moneda o cualquier otro carácter. El valor mínimo del parámetro en el archivo de fuente se utiliza para todas las palabras clave existentes. Por ejemplo, si el archivo de fuente tiene [!UICONTROL Param1] valores de 21500 y 22000, luego el [!UICONTROL Param1] Los valores de las palabras clave existentes se cambian a 21500. La plantilla debe contener al menos una palabra clave. **Sugerencia:** Utilice esta opción solo cuando tenga grupos de anuncios con temáticas ajustadas, de modo que tenga sentido que las palabras clave tengan el mismo valor.

Los campos de datos del archivo de fuente pueden tener un máximo de 25 caracteres y solo pueden constar de datos numéricos con los siguientes caracteres no numéricos:

* (Cuando se usa la opción &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; parámetro) Solo hasta un punto decimal.

* (Cuando no se utiliza la opción &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; (parámetro ):

   * El valor puede ir precedido o anexado con un símbolo de moneda o código. Por ejemplo, 2.000,00 £ y 2000 GBP son válidos.

   * El valor puede incluir una coma (,) o un punto (.) como separador, con un punto opcional (.) o una coma (,) para valores fraccionarios. Por ejemplo, 1 000,00 y 2 000,10 son válidos.

   * Al valor se le puede agregar un prefijo o un signo de porcentaje (%), un signo más (+) o un signo menos (-). Por ejemplo, 20%, 208+ y -42,32 son válidos.

   * Se pueden incrustar dos números con una barra diagonal. Por ejemplo, 4/1 y 0.95/0.45 son válidos.

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising] plantillas\]:** ([!DNL Microsoft Advertising] (solo plantillas) La cadena que se utilizará como valor de sustitución en un anuncio si el título, el texto, la URL para mostrar o la URL final contienen el valor `{Param2}` cadena de sustitución dinámica. La longitud máxima es de 70 caracteres, pero tenga en cuenta la longitud máxima de los elementos publicitarios en los que la utiliza (por ejemplo, un título de anuncio puede incluir hasta 25 caracteres).

**[!UICONTROL Param 3]:** ([!DNL Microsoft Advertising] (solo plantillas) La cadena que se utilizará como valor de sustitución en un anuncio si el título, el texto, la URL para mostrar o la URL final contienen el valor `{Param3}` cadena de sustitución dinámica. La longitud máxima es de 70 caracteres, pero tenga en cuenta la longitud máxima de los elementos publicitarios en los que la utiliza (por ejemplo, un título de anuncio puede incluir hasta 25 caracteres).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** La oferta inicial para cada palabra clave con el tipo de coincidencia o tipo de anuncio especificado.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] y [!DNL Microsoft Advertising] (solo campañas de ) El tipo de anuncios: *[!UICONTROL Expanded Search Ads]* o *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Opcional) Rellena previamente todos los campos alternativos y de copia con texto de los campos originales de copia de publicidad.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Solo anuncios de búsqueda interactivos) La posición del anuncio en la que se debe incluir el título/titular (como &quot;[!UICONTROL Pinned at position 1]&quot;). El valor predeterminado es [!UICONTROL Unpinned].

Debe haber al menos un título disponible para cada posición. Si fija varios títulos a la misma posición, el anuncio final siempre incluirá uno de esos títulos en la posición especificada. Es posible que los títulos anclados a la posición 3 no se muestren con el anuncio.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (Solo anuncios de búsqueda interactivos) Los títulos de los anuncios (titulares). Cada variación de anuncio debe incluir al menos tres títulos de anuncio y hasta 15 títulos. La red de anuncios muestra anuncios con hasta tres titulares. La longitud máxima de cada título es de 30 caracteres, incluido cualquier texto dinámico (como los valores de palabras clave y personalizadores de anuncios).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Solo anuncios de texto estándar de Microsoft Advertising existentes; solo lectura) El título, o la primera línea, de un anuncio. Microsoft Advertising ha desaprobado la creación y edición de anuncios de texto estándar.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] y [!DNL Yahoo! Japan Ads] (solo plantillas de anuncios de texto expandidas/extendidas) El titular de un anuncio. La longitud máxima de cada línea (después de reemplazar cualquier parámetro dinámico) es de 30 caracteres o 15 caracteres de doble byte.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] solo plantillas de anuncios de texto expandidas; opcional) Un tercer titular para un anuncio. La longitud máxima (después de reemplazar cualquier parámetro dinámico) es de 30 caracteres o 15 caracteres de doble byte.

**[!UICONTROL Title]:** ([!DNL Yandex] (solo) El título o la primera línea de un anuncio. El máximo es de 33 caracteres.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (Solo anuncios de texto expandidos de Microsoft Advertising) El titular de un anuncio. La longitud máxima de cada línea (después de reemplazar cualquier parámetro dinámico) es de 30 caracteres o 15 caracteres de doble byte.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Solo anuncios de texto expandidos de Microsoft Advertising) Cuerpo de un anuncio. La longitud máxima (después de reemplazar cualquier parámetro dinámico) es de 80 caracteres o 40 caracteres de doble byte (como chino, japonés y coreano).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** El cuerpo del anuncio.

* (Plantillas de anuncios de texto expandido de Google Ads) La longitud máxima (después de reemplazar cualquier parámetro dinámico) es de 90 caracteres o 45 caracteres de doble byte.

* (Yahoo! Plantillas de anuncios de Japón) La longitud máxima (después de reemplazar cualquier parámetro dinámico) es de 80 caracteres o 40 caracteres de doble byte.

* (Plantillas de Yandex) La longitud máxima (después de reemplazar cualquier parámetro dinámico) es de 75 caracteres, y una sola palabra no puede tener más de 22 caracteres.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Solo anuncios de búsqueda interactivos) La posición del anuncio en la que se debe incluir la descripción (como &quot;[!UICONTROL Pinned at position 1]&quot;). El valor predeterminado es [!UICONTROL Unpinned]. Debe haber al menos una descripción disponible para cada posición.

Si fija varias descripciones en la misma posición, el anuncio final siempre incluirá una de esas descripciones en la posición especificada. Las descripciones ancladas a la posición 2 pueden no mostrarse con el anuncio.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (Solo anuncios de búsqueda interactivos) Las descripciones de los anuncios. Cada variación de anuncio debe incluir al menos dos descripciones de anuncio y hasta cuatro descripciones. La red de anuncios muestra anuncios con hasta dos descripciones; escriba al menos dos. La longitud máxima de cada descripción es de 90 caracteres, incluido cualquier texto dinámico (como los valores de palabras clave y personalizadores de anuncios).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Solo plantillas de anuncios de texto expandido de Google; opcional) Una segunda línea del anuncio. La longitud máxima (después de reemplazar cualquier parámetro dinámico) es de 90 caracteres o 45 caracteres de doble byte.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Solo texto expandido y anuncios de búsqueda adaptables; opcional) Una o dos rutas URL para incluirlas consecutivamente después de la dirección URL base. Deben describir el producto o servicio en el anuncio con más detalle. Por ejemplo, si agrega un [!UICONTROL Display Path 1] de &quot;Zapatos&quot; y [!UICONTROL Display Path 2] de &quot;Outdoor&quot; a la URL base www.example.com, la URL es www.example.com/Shoes/Outdoor. La longitud máxima (después de reemplazar cualquier parámetro dinámico) de cada campo es de 15 caracteres o 7 caracteres de doble byte.

Para anuncios adaptables de búsqueda, inserte un personalizador de anuncios con los siguientes formatos, donde `Default text` es un valor opcional que se inserta cuando el archivo de fuente no incluye un valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, como `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, como `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Existente) [!DNL Microsoft Advertising] y [!DNL Yahoo! Japan Ads] solo anuncios de texto estándar; solo lectura) La dirección URL mostrada en un anuncio.

[!DNL Microsoft Advertising] y [!DNL Yahoo! Japan Ads] han desaprobado la creación y edición de anuncios de texto estándar.

**[!UICONTROL Base URL]:** (Cuentas solo con direcciones URL de destino) La página a la que se llevan los usuarios. Puede incluir redirección de terceros y código de seguimiento. Si utiliza el servicio de seguimiento de conversión de Adobe Advertising y la configuración de la campaña incluye el uso del [!UICONTROL EF Redirect] y agregando seguimiento en el nivel de anuncio; a continuación, Search, Social y Commerce añaden automáticamente su propia redirección y código de seguimiento al anuncio.

Para insertar un nombre de columna o un grupo de modificadores como parámetro dinámico, haga clic en el campo de entrada y, a continuación, haga clic en un nombre de columna en la lista de columnas o en un [nombre de modificador](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) en el [!UICONTROL Modifiers] lista.

**[!UICONTROL Final URL]:** (Cuentas con direcciones URL finales/avanzadas) Dirección URL de la página de aterrizaje a la que se llevan los usuarios cuando hacen clic en el anuncio. Debe incluir el mismo dominio que la dirección URL mostrada y cualquier parámetro de la dirección URL final debe coincidir con los parámetros de la dirección URL de la página de aterrizaje después de hacer clic en el anuncio. Puede contener redirecciones dentro del dominio o subdominio de la página de aterrizaje, pero no redirecciones fuera de este.

Si usa un [!DNL Google Merchant] Centrar fuente e incluir este valor en &quot;[!UICONTROL Link]&quot;, y luego inserte esa columna en este campo.

>[!NOTE]
>
>* Si genera direcciones URL de seguimiento al publicar datos propagados a través de la plantilla, los parámetros de seguimiento se anexan a este valor en función de la configuración de seguimiento de cuentas.
>* ([!DNL Google Ads] cuentas ) Evite utilizar macros que no sustituyan los clics de fuentes que habiliten el seguimiento paralelo. Si el anunciante debe utilizar macros, el equipo de cuenta de Adobe debe trabajar con Asistencia al cliente o con el equipo de implementación para agregarlas.

**[!UICONTROL Tracking Template]:** (Cuentas con direcciones URL finales/avanzadas; opcional) La plantilla de seguimiento, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, e incrusta la dirección URL final en un parámetro. La plantilla de seguimiento en el nivel más granular (con la palabra clave como valor más granular) anula los valores en todos los demás niveles.

Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload],&quot; Buscar, Social y Commerce anexan automáticamente el código de redireccionamiento y seguimiento al guardar el registro.

Para redirecciones y seguimiento de terceros, introduzca un valor. Para indicar la dirección URL de la página de aterrizaje:

* Para Yahoo! Cuentas de anuncios de Japón, utilice el parámetro {lpurl}.

* Para ver los parámetros disponibles para las cuentas de Microsoft Advertising y Google Ads, consulte la [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/56799) o los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección &quot;Disponible&quot; [!DNL ValueTrack] Parámetros&quot; en el [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/6305348).

**\[Campos de anuncio alternativos debajo de los campos de anuncio originales\]:** (Opcional) Un conjunto alternativo de copias de anuncio para un anuncio que puede utilizarse si alguna de las líneas del anuncio original supera la longitud máxima permitida una vez que algún parámetro dinámico se rellena con datos durante la propagación.

>[!NOTE]
>
>* Si la variable [!UICONTROL Prefill] está seleccionada, los campos alternativos se rellenan previamente con los campos originales y puede editarlos según sea necesario.
>* Solo los campos de copia de anuncio que superen la longitud máxima se sustituyen por el valor alternativo. Por ejemplo, si solo un titular o título original es demasiado largo, la variación de anuncio generada utiliza el titular o título alternativo y las descripciones originales. Por lo tanto, asegúrese de que la copia de anuncio alternativa tenga sentido cuando se combine con la copia de anuncio original.
>* Si la copia de anuncio original cumple los requisitos de longitud del motor de búsqueda, se descarta la copia de anuncio alternativa.

**\[Componente\] [!UICONTROL Ad Label Classifications] > \[Clasificación de etiquetas y valor\]:** (Opcional) Valores de hasta cinco clasificaciones de etiquetas existentes para asignarlas a las variaciones de anuncios que se crean o editan con la plantilla. Para cada componente de campaña al que desea asignar clasificaciones de etiquetas:

1. Haga clic en la casilla.

1. Configure los valores de clasificación de etiquetas para la plantilla de variación de anuncio:

   * Para cada clasificación de etiqueta y valor que asignar al componente, haga lo siguiente:

      1. Clic **[!UICONTROL Add Label Classification]**.

      1. Seleccione la clasificación de etiquetas existente y, a continuación, seleccione un valor existente o introduzca un nuevo valor.

         La longitud máxima de cada valor es de 100 caracteres, y puede incluir caracteres ASCII y no ASCII.

         Para insertar un nombre de columna como parámetro dinámico para un valor de clasificación de etiqueta, haga clic en el campo de entrada (el segundo campo) y, a continuación, haga clic en un nombre de columna en la lista de columnas.

         Solo puede incluir un valor por clasificación por componente de campaña. Por ejemplo, una campaña puede tener Color=Rojo pero no Color=Rojo y Color=Azul.

         * Para cambiar un valor de clasificación de etiquetas existente, seleccione o introduzca un nuevo valor.

         * Para quitar un valor de clasificación de etiquetas existente, haga clic en **[!UICONTROL X]** junto al valor.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Automatización de la administración de anuncios mediante fuentes de inventario](../inventory-feeds-about.md)
>* [Administración de modificadores](../modifiers-manage.md)
>* [Administrar archivos de fuente de datos de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propagación de datos de fuentes mediante plantillas](../feed-data-propagate.md)
>* [Publicar datos de campaña de fuentes de inventario en redes de publicidad](../propagated-data-post.md)
