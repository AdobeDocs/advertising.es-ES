---
title: Preguntas frecuentes sobre campañas
description: Consulte respuestas a preguntas sobre administración de campañas y vistas de datos de campañas.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Preguntas frecuentes sobre la administración de campañas

## Información general

+++¿Puedo mover campañas y componentes de una cuenta a otra?

No mueva ni copie un componente de campaña o campaña, que tenga un ID único, a una cuenta con un ID de cuenta diferente. Al hacerlo, se producen errores de datos.
+++

+++¿Cuándo se actualizan los datos de clics desde las redes de publicidad?

El proceso de extraer los datos de clics del día anterior de los motores de búsqueda comienza a las 06:00 en la zona horaria del anunciante.

Además, [!DNL Google Ads] métricas de rendimiento de nivel de campaña en la red de búsqueda del día actual se recuperan a las 08:00 y a las 16:00 en el huso horario del anunciante.
+++

+++¿Qué acciones provocan que palabras clave y anuncios pierdan su historial?

>[!NOTE]
>
>(Anunciantes con portafolios) Espere que el rendimiento de las nuevas combinaciones de tipo palabra clave y tipo de coincidencia sea volátil mientras Search, Social y Commerce recopilan datos para crear modelos para ellas.

**Acciones en las vistas [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns], en el proceso de publicación de hojas de edición masiva y en el editor propio de la red de anuncios:**

La palabra clave o anuncio existente se elimina y se crea otro cuando:

* ([!DNL Baidu], [!DNL Google Ads] y [!DNL Yandex]) Ha editado un nombre de palabra clave.

* ([!DNL Google Ads], [!DNL Microsoft Advertising] y [!DNL Yandex]) Cambia el tipo de coincidencia de una palabra clave.

* Las palabras clave se mueven de un grupo de anuncios a otro.

* ([!DNL Google Ads] anuncios dinámicos de búsqueda, [!DNL Microsoft Advertising] anuncios de texto expandidos y todos los tipos de anuncios en otras redes de anuncios compatibles) Puede editar la copia de anuncio (titular/título o descripción) o una imagen de anuncio.

* Puede mover un anuncio entre grupos de anuncios.

**Eventos en el proceso de registro de fuentes de inventario de productos:**

Se elimina un anuncio o palabra clave existente y se crea otro cuando:

* Un archivo de fuente contiene un nuevo valor para una columna que se utiliza en una variación de anuncio.

* La configuración de la plantilla para un anuncio ha cambiado desde la última propagación.

* Un nuevo archivo de fuente incluye una fila para un anuncio o una palabra clave que a) estaba en un archivo anterior, pero b) se ha omitido desde entonces y se pausó o eliminó según la configuración de los datos de fuente.

Según la configuración de [datos de fuente](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), un anuncio o palabra clave existente se puede eliminar cuando:

* Un nuevo archivo de fuente no incluye una fila para un anuncio o palabra clave existente.

* Se produce la fecha de finalización programada de los componentes de un archivo de fuente registrado.

* El nivel de stock de un elemento cae por debajo del mínimo especificado en la configuración de los datos de fuente.
+++

+++([!DNL Google Ads] campañas) Los cambios en los nombres para mostrar de mis conversiones rastreadas de [!DNL Google] se revirtieron.

Si cambia los nombres para mostrar de las métricas de conversión en Search, Social y Commerce, los cambios se sobrescribirán con los nombres configurados en [!DNL Google Ads]. Realice cualquier cambio de nombre dentro de [!DNL Google Ads].
+++

+++(Campañas de Google Ads) ¿Puedo utilizar un presupuesto compartido para campañas en portafolios?

Para obtener los mejores resultados, no agregue [!DNL Google Ads] campañas a un presupuesto compartido de [!DNL Google Ads] si se encuentran en portafolios optimizados configurados en &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;. Si lo hace, [!DNL Google Ads] anula los presupuestos de campaña optimizados para Search, Social y Commerce, lo que puede generar ineficiencias en las ofertas.
+++

+++([!DNL Google Ads] campañas) ¿Puedo enviar usuarios móviles y no móviles a diferentes páginas de aterrizaje?

Puede usar los parámetros [!DNL Google Ads] [!DNL ValueTrack] `{ifmobile}` y `{ifnotmobile}` para determinar el nombre de dominio de la página de aterrizaje de una de las dos maneras siguientes, según corresponda para sus sitios:

* Incluya la designación móvil como servidor host usando `{ifmobile:m}{ifnotmobile:www}`.

  Por ejemplo, `http://{ifmobile:m}{ifnotmobile:www}.example.com` lleva a usuarios móviles a m.example.com y a usuarios que no son móviles a www.example.com.

* Incluya la designación móvil como dominio de nivel superior mediante `{ifmobile:mobi}{ifnotmobile:com}`.

  Por ejemplo, `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` lleva a los usuarios móviles a www.example.mobi y a los usuarios que no son móviles a www.example.com.

En ambos casos, las direcciones URL base con seguimiento de búsqueda, medios sociales y Commerce incluyen las etiquetas `{}` sin codificar y cualquier parámetro adicional anexado a la dirección URL base.

>[!NOTE]
>
>No utilice una dirección URL completa como valor para los parámetros ifnotmobile e ifmobile; utilice solamente la parte variable de la dirección URL (como &quot;m&quot; versus &quot;www&quot; o &quot;mobi&quot; versus &quot;com&quot;).

+++

+++([!DNL Google Ads] campañas en la red de búsqueda) ¿Qué datos se muestran para hoy?

[!DNL Google Ads] métricas de rendimiento de nivel de campaña en la red de búsqueda para el día actual se recuperan a las 08:00 y a las 16:00 en el huso horario del anunciante.

En la ficha [!UICONTROL Campaigns] tanto en la vista [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] como en la vista [!UICONTROL Optimization] > [!UICONTROL Portfolios], cuando se crea un informe sobre [!UICONTROL Today] o un intervalo de fechas personalizado que incluya el día actual, los datos incluirán los datos sincronizados más recientemente.

>[!NOTE]
>
>Los datos de clics, impresiones y conversiones se retrasan tres horas y no se completan hasta la siguiente extracción de datos.

+++

+++¿Cuál es la diferencia entre una plantilla de seguimiento y un sufijo de página de aterrizaje?

Utilice un sufijo de página de aterrizaje solo para redes de anuncios que admitan el seguimiento paralelo. En Search, Social y Commerce, tanto las plantillas de seguimiento como los sufijos de página de aterrizaje deben incluir un identificador de clic de la red de publicidad, pero las plantillas de seguimiento incluyen parámetros de seguimiento adicionales.

Consulte las siguientes preguntas frecuentes sobre [compatibilidad con el seguimiento paralelo](#parallel-tracking) para obtener más información sobre cómo se cargan las plantillas de seguimiento y los sufijos de página de aterrizaje cuando un usuario hace clic en un anuncio.

+++

+++([!DNL Google Ads] y [!DNL Microsoft Advertising]) ¿Search, Social y Commerce admiten el seguimiento paralelo de anuncios en [!DNL Google Ads] o [!DNL Microsoft Advertising]? {#parallel-tracking}

El seguimiento paralelo envía a los clientes directamente desde su anuncio a la dirección URL final, que puede incluir parámetros añadidos desde un sufijo de dirección URL final o un &quot;sufijo de página de aterrizaje&quot;. La dirección URL de la plantilla de seguimiento (con parámetros adicionales para la medición de clics) se carga por separado en segundo plano; como resultado, la página de aterrizaje se carga más rápido.

Search, Social y Commerce admiten el seguimiento paralelo para campañas de búsqueda y compras mediante el identificador de clic de la red de anuncios (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para [!DNL Google Ads]). Use [nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) o [nivel de campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (denominado &quot;[!DNL final URL suffix]&quot; en las redes de anuncios), que se anexa a las direcciones URL de la página de aterrizaje para rastrear clics en anuncios secundarios de navegadores que admiten el seguimiento paralelo. Vea los [formatos de sufijo necesarios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y [formatos de sufijo necesarios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Cuando un usuario ve su anuncio en un navegador que no admite el seguimiento paralelo, la red de anuncios utiliza el seguimiento secuencial en su lugar: los clientes se envían primero a la URL de la plantilla de seguimiento, lo que puede redirigir a los clientes a servidores de seguimiento intermedios antes de redirigirlos a la URL final (que puede incluir parámetros adicionales en un sufijo de página de aterrizaje). Todas las plantillas de seguimiento de una cuenta de red de anuncios deben incluir el mismo parámetro de identificador de clic que se usa en [!UICONTROL Landing Page Suffix]. Vea los [formatos de plantilla de seguimiento para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y los [formatos de plantilla de seguimiento para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++¿Por qué las direcciones URL de seguimiento de mis anuncios incluyen &quot;`&EV_HASH={<hash>}`?&quot;

Cuando carga anuncios con una [fuente de inventario de productos](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para una cuenta con el redireccionamiento de píxeles de Search, Social y Commerce y con el seguimiento a nivel de palabra clave y creativo, Search, Social y Commerce agregan el parámetro hash y el valor a la plantilla de seguimiento o la dirección URL de destino del anuncio para identificar que se creó con la función de fuente de inventario.
+++

## Fuentes de inventario

+++(Fuentes de inventario de productos) ¿Debo pausar o eliminar los anuncios que están obsoletos o que son para un producto cuyo nivel de stock está por debajo de un mínimo especificado?

Depende de los requisitos comerciales del anunciante.

Cuando se ponen en pausa los anuncios, se reactivan si se vuelve a enviar el mismo anuncio o si el nivel de stock supera el mínimo. Esto le permite conservar el historial del anuncio.

Cuando elimina anuncios y los vuelve a enviar, se crean nuevos anuncios y es necesario acumular datos históricos para los nuevos anuncios. Sin embargo, si no espera volver a enviar los anuncios eliminados, no es importante tener datos históricos.
+++

+++(Fuentes de inventario de productos) Si elimino una plantilla de publicidad y luego creo una nueva idéntica, ¿faltan elementos en el siguiente archivo de fuente en pausa (cuando la configuración del archivo de fuente está configurada para hacerlo)?

Si al siguiente archivo de fuente le faltan elementos de línea y no ha publicado previamente esos elementos de línea de la nueva plantilla a través de un archivo de fuente anterior, los elementos de línea que faltan no se reconocen como &quot;faltantes&quot;, por lo que no se crean. Para evitarlo, propague el archivo de fuente anterior a través de la nueva plantilla y publique los datos antes de propagar y publicar los datos de un nuevo archivo.
+++

+++(Fuentes de inventario de productos) ¿Puedo actualizar los precios de mis productos sin afectar la puntuación de calidad de un anuncio?

Para campañas de [!DNL Google Ads], sí: las variables [!DNL Google Ads] `{Param 1}` y `{Param 2}` le permiten insertar dinámicamente valores numéricos en una variación de anuncio sin eliminar ni volver a crear el anuncio y, por lo tanto, sin afectar la puntuación de calidad.

Para usar una variable `{Param 1}` o `{Param 2}` para los datos de precios, asigne la columna de precio del archivo de datos a esa variable en las plantillas de fuentes correspondientes y, a continuación, incluya la variable en las plantillas de variaciones de anuncios.

Por ejemplo, si la columna se llama &quot;Precio&quot;, abra la plantilla de fuente que crea los anuncios, haga clic en el campo de entrada situado junto a **[!UICONTROL Param 1]** y, a continuación, haga clic en la columna **[!UICONTROL Price]** de la lista [!UICONTROL Feeds/Available Columns], que inserta `[Price]` como valor de [!UICONTROL Param 1]. A continuación, en la plantilla de variación de anuncio situada en la parte inferior de la plantilla de fuente, inserte `{param1:default text}`, donde &quot;texto predeterminado&quot; es el texto que se debe utilizar si la columna de parámetro del archivo de fuente está vacía para una fila de anuncio.

Al enviar datos, los campos de datos de las columnas [!UICONTROL Param1] y [!UICONTROL Param2] pueden incluir hasta 25 caracteres, incluidos datos numéricos, símbolos de moneda y códigos de moneda, así como los siguientes caracteres no numéricos: `, . % + - /`
+++

+++Mis campañas generadas a partir de fuentes de inventario tienen muchas transacciones huérfanas.

Si la [configuración de datos de fuente](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) está configurada para eliminar anuncios en diversas situaciones, cualquier conversión retrasada que ocurra después de hacer clic en el anuncio puede causar [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p). La práctica recomendada es pausar los anuncios en lugar de eliminarlos. Si un anuncio sigue sin recibir ingresos después de mucho tiempo, puede eliminarlo mediante una hoja de edición por lotes o la vista de administración de anuncios.
+++

## Problemas de rendimiento relacionados con la cuenta y la campaña

+++Algunas de mis campañas gastan más o menos que los presupuestos de campaña.

* Esto es normal en un portafolio optimizado que está configurado con la opción &quot;[!UICONTROL Auto-adjust campaign budget limits]&quot;. Si se habilita esta opción, puede gastar hasta *N* veces el presupuesto de cada campaña, donde *N* es el valor de la configuración &quot;[!UICONTROL Multiple]&quot;. Esta opción permite a la capacidad de optimización ajustar el gasto para campañas individuales según sea necesario, al tiempo que dirige todo el portafolio para cumplir con su objetivo.
* Si [!DNL Google Ads] campañas utilizan un presupuesto compartido, [!DNL Google Ads] ajusta el gasto de las campañas individuales según sea necesario para gastar todo el presupuesto compartido.
+++
