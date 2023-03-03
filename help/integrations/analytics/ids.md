---
title: ID de publicidad de Adobe utilizados por [!DNL Analytics]
description: ID de publicidad de Adobe utilizados por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# ID de publicidad de Adobe utilizados por [!DNL Analytics]

*Anunciantes con una integración de Adobe de Advertising-Adobe Analytics solamente*

*DSP Aplicable a Advertising y[!DNL Advertising Search]*

Adobe Advertising utiliza dos ID para el seguimiento del rendimiento en el sitio: el *EF ID* y el *ID de AMO*.

Cuando se produce una impresión de un anuncio, Adobe Advertising crea los valores de ID de AMO e ID de EF y los almacena. Cuando un visitante que ha visto un anuncio entra en el sitio sin hacer clic en un anuncio, [!DNL Analytics] llama a estos valores desde Publicidad de Adobe a través de [!DNL Analytics for Advertising] Código JavaScript. Para el tráfico de visualización, [!DNL Analytics] genera un ID suplementario (`SDID`), que se utiliza para unir el EF ID y el AMO ID en [!DNL Analytics]. Para el tráfico de clics, estos ID se incluyen en la dirección URL de la página de aterrizaje utilizando `s_kwcid` y `ef_id` parámetros de cadena de consulta.

Adobe La publicidad distingue entre una entrada de clics o visualizaciones en el sitio web según los siguientes criterios:

* Se registra una entrada de visualización cuando un usuario visita el sitio después de ver un anuncio, pero sin hacer clic en él. [!DNL Analytics] registra una visualización si se cumplen dos condiciones:
   * El visitante no tiene pulsaciones para una [!DNL DSP] o [!DNL Search] anuncio durante la [haga clic en ventana retrospectiva](#lookback-a4adc).
   * El visitante ha visto al menos uno [!DNL DSP] anuncio durante la [ventana retrospectiva de impresiones](#lookback-a4adc). La última impresión se pasa como la visualización.
* Se captura una entrada de pulsación cuando un visitante del sitio hace clic en un anuncio antes de entrar en el sitio. [!DNL Analytics] registra una pulsación cuando se da cualquiera de las siguientes condiciones:
   * La dirección URL incluye un EF ID y un AMO ID, tal como se agregaron a la dirección URL de la página de aterrizaje mediante la publicidad de Adobe.
   * La dirección URL no contiene códigos de seguimiento, pero el código JavaScript de publicidad de Adobe detecta un clic en los últimos dos minutos.

![Adobe Advertising basado en vistas [!DNL Analytics] integración](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Publicidad de Adobe basada en vistas [!DNL Analytics] integración*

![Adobe Advertising click basado en URL [!DNL Analytics] integración](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Adobe en el que se hace clic en URL [!DNL Analytics] integración*

## ID de EF de Adobe Advertising

El EF ID es un token único que Adobe Advertising utiliza para asociar la actividad con un clic en línea o una exposición de publicidad. El EF ID se almacena en un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o la dimensión rVar (eVar reservado) (ID de EF de publicidad de Adobe) y rastrea cada clic o exposición de anuncio en el nivel de navegador o dispositivo individual. Los ID de EF actúan principalmente como claves para el envío [!DNL Analytics] datos a publicidad de Adobe para la creación de informes y la optimización de ofertas dentro de la publicidad de Adobe.

### Formato de ID de EF

>[!NOTE]
>
>Los ID de EF distinguen entre mayúsculas y minúsculas. Si un [!DNL Analytics] La implementación fuerza el seguimiento de URL a minúsculas y, a continuación, la publicidad en Adobe no reconocerá el EF ID. Esto afectará a las ofertas y los informes de publicidad de Adobe, pero no afecta a los informes de publicidad de Adobe dentro de [!DNL Analytics].

#### [!DNL Google Ads] anuncios de búsqueda

```
{gclid}:G:s
```

donde:

* `gclid` es el [!DNL Google Click ID] (GCLID).
* `s` es el tipo de red (&quot;s&quot; para la búsqueda).

#### Anuncios de búsqueda de Microsoft Advertising

```
{msclkid}:G:s
```

donde:

* `msclkid` es el [!DNL Microsoft Click ID] (MSCLKID).
* `s` es el tipo de red (&quot;s&quot; para la búsqueda).

#### Mostrar anuncios y anuncios de búsqueda en otros motores de búsqueda

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

donde:

* &lt;*ID de visitante de Adobe Advertising*> es un ID único por visitante (como UhKVaAAABCkJ0mDt). También se denomina *ID de internauta*.

* &lt;*timestamp*> es la hora con el formato AAAAMMDDHHMMSS (como 20190821192533 para el año 2019, mes 08, día 21, hora 19:25:33).

* &lt;*tipo de canal*> es el tipo de canal responsable del clic o la exposición:

   * `d` DSP para hacer clic en un anuncio en pantalla de la (pulsación en pantalla)
   * `i` DSP para obtener una impresión de un anuncio en pantalla de la aplicación de la impresión de un anuncio en pantalla (visualización completa)
   * `s` para hacer clic en un anuncio de búsqueda (pulsación de búsqueda).

Ejemplo `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### El Dimension EF ID en [!DNL Analytics]

Entrada [!DNL Analytics] de, puede encontrar datos de EF ID buscando la variable [!UICONTROL EF ID] dimensión y uso del [!UICONTROL EF ID Instance] métrica.

Los EF ID están sujetos al límite de 500 000 identificadores únicos en Analysis Workspace. Una vez que se alcanza el valor de 500 000, todos los nuevos códigos de seguimiento se registran con el título de un elemento de línea &quot;[!UICONTROL Low Traffic].&quot; Debido a la posibilidad de que falte fidelidad en los informes, los EF ID no se clasifican y no debe utilizarlos para segmentos o informes en [!DNL Analytics].

## ID de AMO de Adobe Advertising

El ID de AMO realiza un seguimiento de cada combinación de publicidad única en un nivel menos granular y se utiliza para [!DNL Analytics] clasificación de datos e ingesta de métricas de publicidad (como impresiones, clics y costes) de Adobe Advertising. El ID de AMO se almacena en un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o la dimensión rVar (ID de AMO) y se utiliza exclusivamente para la creación de informes en [!DNL Analytics].

El ID de AMO también se denomina `s_kwcid`, que a veces se pronuncia como &quot;[!DNL the squid].&quot;

### Formato de ID de AMO para [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

donde:

* &lt;*ID de canal*> puede ser:

   * `AC` DSP = Advertising
   * `AL` para [!DNL Advertising Search]

* &lt;*ID de anuncio*> se utiliza como identificador único generado por la publicidad de Adobe para un anuncio. Sirve como clave para traducir los metadatos de la entidad de publicidad de Adobe a legibles [!DNL Analytics] dimensiones.

* &lt;*ID de ubicación*> es un identificador único generado por la publicidad de Adobe para una ubicación. Sirve como clave para traducir los metadatos de la entidad de publicidad de Adobe a legibles [!DNL Analytics] dimensiones.

Ejemplo de ID de AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Formato de ID de AMO para [!DNL Search]

ID de AMO para [!DNL Search] siga un formato distinto para cada motor de búsqueda. El formato de todos los motores de búsqueda comienza con lo siguiente:

```
AL!{userid}!{sid}
```

donde:

* `AL` es el ID de canal para la red de publicidad.
* `{userid}` Adobe es el ID de usuario numérico único que Advertising asigna al anunciante.
* `{sid}` es el ID numérico que utiliza Adobe Advertising para la red de publicidad especificada, como `3` para [!DNL Google Ads] o `10` para [!DNL Microsoft Advertising].

A continuación se muestran los formatos de ID de AMO completos para un par de redes de publicidad. Para obtener los formatos de ID de AMO para otras redes de publicidad, póngase en contacto con el equipo de cuenta de Adobe.

Formato de ID de AMO para [!DNL Google Ads]:

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

donde:

* `{creative}` es el [!DNL Google Ads] ID numérico único del creativo.
* `{matchtype}` es el tipo de coincidencia de la palabra clave que activó el anuncio: `e` para obtener información exacta, `p` para la frase, o `b` para amplia.
* `{placement}` es el nombre de dominio del sitio web en el que se hizo clic en el anuncio. Hay un valor disponible para los anuncios de campañas con objetivos de ubicación y para los anuncios de campañas con objetivos de palabras clave que se muestran en sitios de contenido.
* `{network}` indica la red desde la que se produjo el clic:  `g` para [!DNL Google] búsqueda (solo para anuncios segmentados por palabras clave), `s` para un socio de búsqueda (solo para anuncios segmentados por palabras clave), o `d` para Display Network (para anuncios con objetivo de palabras clave o con objetivo de ubicación).
* `{keyword}` es la palabra clave específica que activó el anuncio (en sitios de búsqueda) o la palabra clave que mejor coincide (en sitios de contenido).

Formato de ID de AMO para [!DNL Microsoft Advertising]:

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

donde:

* `{AdId}` es el [!DNL Microsoft Advertising] ID numérico único del creativo.
* `{OrderItemId}` es el [!DNL Microsoft Advertising] ID numérico de la palabra clave.

### DIMENSION de ID de AMO en [!DNL Analytics]

En los informes de Analytics, puede encontrar datos de ID de AMO buscando el [!UICONTROL AMO ID] dimensión y uso del [!UICONTROL AMO ID Instance] métrica. El [!UICONTROL AMO ID] contiene todos los valores de ID de AMO capturados, mientras que la dimensión [!UICONTROL AMO ID Instance] Esta métrica indica la frecuencia con la que el sitio capturó un valor de ID de AMO. Por ejemplo, si se hizo clic en el mismo anuncio de búsqueda cuatro veces, pero Analytics rastreó siete entradas de sitio, [!UICONTROL AMO ID Instance] sería siete (7) y [!UICONTROL Clicks] sería de cuatro (4).

Para cualquier informe o auditoría dentro de [!DNL Analytics]Sin embargo, se recomienda utilizar el ID de AMO junto con su instancia correspondiente. Para obtener más información, consulte &quot;[Validación de datos para [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; en &quot;Variaciones de datos previstas entre [!DNL Analytics] y Adobe Advertising&quot;.

## Acerca de las clasificaciones de Analytics

Entrada [!DNL Analytics], a [clasificación](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) es un fragmento de metadatos para un código de seguimiento determinado, como Cuenta, Campaña o Anuncio. Adobe Advertising categoriza los datos de publicidad de Adobe sin procesar mediante clasificaciones para que pueda mostrar los datos de diferentes maneras (por ejemplo, por tipo de anuncio o campaña) al generar informes. Las clasificaciones forman la base de los informes de publicidad de Adobe en [!DNL Analytics] y se pueden usar con las métricas de AMO, como [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], y [!UICONTROL AMO Clicks], así como con eventos en el sitio personalizados y estándar como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], y [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Variaciones de datos previstas entre [!DNL Analytics] Publicidad de Adobe y](data-variances.md)

