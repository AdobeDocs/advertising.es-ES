---
title: Preguntas frecuentes sobre campañas
description: Consulte respuestas a preguntas sobre administración de campañas y vistas de datos de campañas.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# Preguntas frecuentes sobre la administración de campañas

## Información general

+++¿Puedo mover campañas y componentes de una cuenta a otra?

No mueva ni copie un componente de campaña o campaña, que tenga un ID único, a una cuenta con un ID de cuenta diferente. Al hacerlo, se producirán errores de datos.
+++

+++¿Cuándo se actualizan los datos de clics desde las redes de publicidad?

El proceso de extraer los datos de clics del día anterior de los motores de búsqueda comienza a las 06:00 en la zona horaria del anunciante.

Además, [!DNL Google Ads] las métricas de rendimiento de nivel de campaña en la red de búsqueda del día actual se recuperan a las 08:00 y a las 16:00 en el huso horario del anunciante.
+++

+++¿Qué acciones provocan que palabras clave y anuncios pierdan su historial?

>[!NOTE]
>
>(Anunciantes con portafolios) Espere que el rendimiento de las nuevas combinaciones de tipo palabra clave y tipo de coincidencia sea volátil mientras Search, Social y Commerce recopila datos para crear nuevos modelos.

**Acciones en la [!UICONTROL Search] > [!UICONTROL Campaigns] vistas, en el proceso de publicación de hojas de edición masiva y en el propio editor de ad network:**

La palabra clave o anuncio existente se elimina y se crea otro cuando:

* ([!DNL Baidu], [!DNL Google Ads], y [!DNL Yandex]) Puede editar el nombre de una palabra clave.

* ([!DNL Google Ads], [!DNL Microsoft Advertising], y [!DNL Yandex]) Cambia el tipo de coincidencia de una palabra clave.

* Las palabras clave se mueven de un grupo de anuncios a otro.

* ([!DNL Google Ads] anuncios dinámicos de búsqueda, [!DNL Microsoft Advertising] anuncios de texto expandidos y todos los tipos de anuncios en otras redes de publicidad admitidas) Puede editar una copia de anuncio (titular, título o descripción) o una imagen de anuncio.

* Puede mover un anuncio entre grupos de anuncios.

**Eventos en el proceso de registro de fuentes de inventario de productos:**

Se elimina un anuncio o palabra clave existente y se crea otro cuando:

* Un archivo de fuente contiene un nuevo valor para una columna que se utiliza en una variación de anuncio.

* La configuración de la plantilla para un anuncio ha cambiado desde la última propagación.

* Un nuevo archivo de fuente incluye una fila para un anuncio o una palabra clave que a) estaba en un archivo anterior, pero b) se ha omitido desde entonces y se pausó o eliminó según la configuración de los datos de fuente.

Según la variable [configuración de datos de fuente](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), un anuncio o palabra clave existente puede eliminarse cuando:

* Un nuevo archivo de fuente no incluye una fila para un anuncio o palabra clave existente.

* Se produce la fecha de finalización programada de los componentes de un archivo de fuente registrado.

* El nivel de stock de un elemento cae por debajo del mínimo especificado en la configuración de los datos de fuente.
+++

+++()[!DNL Google Ads] campañas) Cambios en los nombres para mostrar de mi [!DNL Google]Se han revertido las conversiones no rastreadas.

Si cambia los nombres para mostrar de las propiedades de transacción en Buscar, Social y Comercio, los cambios se sobrescriben con los nombres configurados en [!DNL Google Ads]. Realice cualquier cambio de nombre en [!DNL Google Ads].
+++

+++(Campañas de Google Ads) ¿Puedo utilizar un presupuesto compartido para campañas en portafolios?

Para obtener los mejores resultados, no agregue [!DNL Google Ads] campañas a un [!DNL Google Ads] presupuesto compartido si se encuentran en portafolios optimizados que están configurados para &quot;[!UICONTROL Auto adjust campaign budget limits].&quot; Si lo hace, [!DNL Google Ads] anula los presupuestos de campaña optimizados para Search, Social y Commerce, lo que puede generar ineficiencias de oferta.
+++

+++()[!DNL Google Ads] campañas de ) ¿Puedo enviar usuarios móviles y no móviles a diferentes páginas de aterrizaje?

Puede usar el complemento [!DNL Google Ads] [!DNL ValueTrack] parámetros `{ifmobile}` y `{ifnotmobile}` para determinar el nombre de dominio de la página de aterrizaje de una de las dos maneras siguientes, según corresponda para sus sitios:

* Incluya la designación móvil como servidor host mediante `{ifmobile:m}{ifnotmobile:www}`.

   Por ejemplo, `http://{ifmobile:m}{ifnotmobile:www}.example.com` lleva a los usuarios móviles a m.example.com y a los usuarios no móviles a www.example.com.

* Incluya la designación móvil como dominio de nivel superior mediante `{ifmobile:mobi}{ifnotmobile:com}`.

   Por ejemplo, `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` lleva los usuarios móviles a www.example.mobi y los usuarios no móviles a www.example.com.

En ambos casos, las direcciones URL base con seguimiento de búsqueda, social y comercial incluyen el código no codificado `{}` y cualquier parámetro adicional anexado a la dirección URL base.

>[!NOTE]
>
>No utilice una dirección URL completa como valor para los parámetros ifnotmobile e ifmobile; utilice solamente la parte variable de la dirección URL (como &quot;m&quot; versus &quot;www&quot; o &quot;mobi&quot; versus &quot;com&quot;).

+++

+++()[!DNL Google Ads] campañas en la red de búsqueda) ¿Qué datos se muestran para hoy?

[!DNL Google Ads] las métricas de rendimiento de nivel de campaña en la red de búsqueda del día actual se recuperan a las 08:00 y a las 16:00 en el huso horario del anunciante.

En el [!UICONTROL Campaigns] en ambas etiquetas [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vista y el [!UICONTROL Optimization] > [!UICONTROL Portfolios] vista, al informar sobre [!UICONTROL Today] Para un intervalo de fechas personalizado que incluya el día actual, los datos incluirán los datos recuperados más recientemente.

>[!NOTE]
>
>Los datos de clics, impresiones y conversiones se retrasan tres horas y no se completan hasta la siguiente extracción de datos.

+++

+++()[!DNL Google Ads] y [!DNL Microsoft Advertising]) ¿Search, Social y Commerce admiten el seguimiento paralelo de anuncios en? [!DNL Google Ads] o [!DNL Microsoft Advertising]?

El seguimiento paralelo envía a los clientes directamente desde su anuncio a la dirección URL final, y la dirección URL de la plantilla de seguimiento (con medición de clics) se carga en segundo plano; como resultado, la página de aterrizaje se carga más rápido.

Search, Social y Commerce admiten el seguimiento paralelo de campañas de búsqueda y compras mediante el identificador de clic ( ) de la red de publicidad`msclkid` para [!DNL Microsoft Advertising]; `gclid` para [!DNL Google Ads]). Utilice un [account-level](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) o [campaign-level](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (llamado &quot;[!DNL final URL suffix]&quot; en las redes de anuncios), que se anexa a las direcciones URL de la página de aterrizaje para rastrear clics en anuncios secundarios de exploradores que admiten el seguimiento paralelo. Consulte la [formatos de sufijo necesarios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y [formatos de sufijo necesarios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Cuando un usuario ve su anuncio en un navegador que no admite el seguimiento paralelo, la red de anuncios utiliza el seguimiento secuencial en su lugar: los clientes se envían primero a la URL de la plantilla de seguimiento, lo que puede redirigir a los clientes a servidores de seguimiento intermedios antes de redirigirlos a la URL final. Todas las plantillas de seguimiento de una cuenta de red de publicidad deben incluir el mismo parámetro de identificador de clic que utiliza en la [!UICONTROL Landing Page Suffix]. Consulte la [formatos de plantilla de seguimiento para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y el [formatos de plantilla de seguimiento para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++¿Por qué las direcciones URL de seguimiento para mis anuncios incluyen?`&EV_HASH={<hash>}`?&quot;

Al cargar anuncios mediante una variable [fuente de inventario de productos](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para una cuenta con el redireccionamiento de píxeles de Search, Social y Commerce y con seguimiento de nivel creativo y de palabra clave, Search, Social y Commerce agrega el parámetro hash y el valor a la plantilla de seguimiento o a la URL de destino del anuncio para identificar que se creó con la función de fuente de inventario.
+++

## Fuentes de inventario

+++(Fuentes de inventario de productos) ¿Debo pausar o eliminar los anuncios que están obsoletos o que son para un producto cuyo nivel de stock está por debajo de un mínimo especificado?

Depende de los requisitos comerciales del anunciante.

Cuando se ponen en pausa los anuncios, se reactivan si se vuelve a enviar el mismo anuncio o si el nivel de stock supera el mínimo. Esto le permite conservar el historial del anuncio.

Cuando elimina anuncios y los vuelve a enviar, se crean nuevos anuncios y es necesario acumular datos históricos. Sin embargo, si no espera volver a enviar los anuncios eliminados, no es importante tener datos históricos.
+++

+++(Fuentes de inventario de productos) Si elimino una plantilla de publicidad y luego creo una nueva idéntica, ¿faltan elementos en el siguiente archivo de fuente en pausa (cuando la configuración del archivo de fuente está configurada para hacerlo)?

Si al siguiente archivo de fuente le faltan elementos de línea y no ha publicado previamente esos elementos de línea de la nueva plantilla a través de un archivo de fuente anterior, los elementos de línea que faltan no se reconocen como &quot;faltantes&quot;, por lo que no se crean. Para evitarlo, propague el archivo de fuente anterior a través de la nueva plantilla y publique los datos antes de propagar y publicar los datos de un nuevo archivo.
+++

+++(Fuentes de inventario de productos) ¿Puedo actualizar los precios de mis productos sin afectar la puntuación de calidad de un anuncio?

Para [!DNL Google Ads] campañas, sí: La [!DNL Google Ads] `{Param 1}` y `{Param 2}` Las variables de permiten insertar dinámicamente valores numéricos en una variación de anuncio sin eliminar ni volver a crear el anuncio y, por lo tanto, sin afectar a la puntuación de calidad.

Para utilizar un `{Param 1}` o `{Param 2}` para los datos de precios, asigne la columna precio del archivo de datos a esa variable en las plantillas de fuentes correspondientes y, a continuación, incluya la variable en las plantillas de variaciones de anuncios.

Por ejemplo, si la columna se llama Precio y abre la plantilla de fuente que crea los anuncios, haga clic en el campo de entrada situado junto a **[!UICONTROL Param 1]** y, a continuación, haga clic en **[!UICONTROL Price]** en la columna [!UICONTROL Feeds/Available Columns] lista, que inserta `[Price]` como el valor de [!UICONTROL Param 1]. A continuación, en la plantilla de variación de anuncio situada en la parte inferior de la plantilla de fuente, inserte `{param1:default text}`, donde &quot;texto predeterminado&quot; es el texto que se debe utilizar si la columna del parámetro en el archivo de fuente está vacía para una fila de anuncio.

Al enviar datos, los campos de datos del [!UICONTROL Param1] y [!UICONTROL Param2] las columnas pueden incluir hasta 25 caracteres, incluidos datos numéricos, símbolos de moneda y códigos de moneda, y los siguientes caracteres no numéricos: `, . % + - /`
+++

+++Mis campañas generadas a partir de fuentes de inventario tienen muchas transacciones huérfanas.

Si la variable [configuración de datos de fuente](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) están configurados para eliminar anuncios en diversas situaciones, cualquier conversión retrasada que se produzca después de hacer clic en el anuncio puede causar [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p). La práctica recomendada es pausar los anuncios en lugar de eliminarlos. Si un anuncio sigue sin recibir ingresos después de un largo periodo, puede eliminarlo mediante una hoja de edición por lotes o la vista de administración de anuncios.
+++

## Problemas de rendimiento relacionados con la cuenta y la campaña

+++Algunas de mis campañas gastan más o menos que los presupuestos de campaña.

* Esto es normal en un portafolio optimizado que se configura con el &quot;[!UICONTROL Auto-adjust campaign budget limits]Opción &quot;. Cuando esta opción está activada, puede gastar hasta *N* multiplicado por el presupuesto de cada campaña, donde *N* es el valor de &quot;[!UICONTROL Multiple]&quot;. Esta opción permite a la capacidad de optimización ajustar el gasto para campañas individuales según sea necesario, al tiempo que dirige todo el portafolio para cumplir con su objetivo.
* If [!DNL Google Ads] Las campañas de utilizan un presupuesto compartido de y [!DNL Google Ads] ajusta el gasto de las campañas individuales según sea necesario para gastar todo el presupuesto compartido.
+++
