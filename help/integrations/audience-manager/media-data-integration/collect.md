---
title: DSP Recopilación de datos de clics e impresiones de campañas de Advertising
description: DSP Aprenda a capturar eventos de impresión y clics basados en cookies desde anuncios de Advertising utilizando píxeles de Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# DSP Recopilación de datos de exposición de medios de campañas de Advertising

*DSP Solo anunciantes con Advertising*

*Anunciantes con solo integración de Adobe Advertising-Adobe Audience Manager*

DSP En este documento se explica cómo etiquetar anuncios de Advertising para capturar eventos de impresión y clics basados en cookies mediante píxeles de Audience Manager, así como las tareas adicionales necesarias para utilizar los datos.

Los píxeles de evento no capturan eventos que se producen en entornos sin cookies, como aplicaciones móviles y TV conectada (CTV).

## Paso 1: Configurar una fuente de datos en Audience Manager {#set-up-data-source}

En Audience Manager, cree un [fuente de datos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) DSP para obtener los datos de impresión y clics de la. Incluir el ID de la fuente de datos [en cada etiqueta de evento](#implement-dsp-pixels) de forma que todos los eventos rastreados se atribuyan a la fuente de datos.

>[!NOTE]
> DSP Es posible recopilar todos los datos de impresiones y clics de las campañas publicitarias que se ejecutan en varias dentro de una sola fuente de datos.

## Paso 2: Implementar píxeles de evento de impresión y clics en páginas web {#implement-dsp-pixels}

Los anunciantes pueden crear e implementar etiquetas de evento para sus propias marcas. Si es necesario, póngase en contacto con su asesor de Adobe Audience Manager o con el equipo de cuenta de Adobe para obtener ayuda.

>[!NOTE]
>
>Si su organización utiliza [!DNL Analytics] seguimiento, es posible que no necesite el rastreo de clics del Audience Manager. Adobe Analytics captura las señales de clic y las puede enviar al Audience Manager mediante [reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Sintaxis de píxeles

Los píxeles de evento deben incluir los siguientes parámetros.

**Píxeles de seguimiento de impresión:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parámetros adicionales opcionales](#parameters) con el prefijo `&`

**Píxeles de rastreo de clics:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parámetros adicionales opcionales](#parameters) con el prefijo `&`

Donde:

* `[Audience Manager customer domain]` es el nombre de dominio al que se enviarán los eventos de impresión o clics [!DNL Adobe].

* `[source id]` es el ID de [fuente de datos](#set-up-data-source) DSP en el que se rastrean datos de impresiones y clics de la.

* `[redirect URL]` es la URL de redireccionamiento con codificación doble. Si está utilizando una herramienta de codificación en línea, como www.urlencoder.org, ejecute la cadena a través del codificador y vuelva a codificar el resultado.

* `${TM_CAMPAIGN_ID_NUM}` DSP es el ID de campaña numérico en la. DSP Si desea codificar un ID de campaña individual en lugar de utilizar la macro de, busque el ID en la configuración de la campaña.

* Cada [parámetro](#key-value-pairs) tiene el prefijo `&` y tiene el formato `d_parameter=parameter_id`, donde `parameter` se reemplaza por el par clave-valor del nuevo campo. Ejemplo: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parámetros como pares clave-valor {#parameters}

**Formato:**  `d_parameter=parameter_id`

    donde:
    
    * el parámetro tiene el prefijo &quot;&amp;&quot;
    
    * &quot;parameter&quot; se sustituye por el par clave-valor para el nuevo campo
    
    Ejemplo: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Ambos tipos de píxeles pueden contener parámetros adicionales como *pares clave-valor* para recopilar características o proporcionar metadatos de campaña (como un nombre de ubicación o un nombre de campaña) para otros informes. Un par clave-valor consta de dos elementos relacionados: un *key*, que es una constante que define el conjunto de datos, y una *valor*, que es una variable que pertenece al conjunto.

En el par clave-valor, la variable de valor puede ser un ID codificado o un *macro*, que es una pequeña unidad de código independiente que se sustituye dinámicamente por los valores correspondientes cuando se carga la etiqueta de publicidad para el seguimiento de campañas y usuarios. Para los parámetros relacionados con la campaña, puede utilizar [DSP macros de](/help/dsp/campaign-management/macros.md) en lugar de macros de Audience Manager, para enviar atributos de campaña junto con los datos de impresión o clics correspondientes al Audience Manager, utilizando un solo píxel en todos los anuncios. DSP Los píxeles de evento deben tener valores adecuados para los pares clave-valor que se incluyen dentro de los píxeles. Por ejemplo, para `d_placement` DSP tecla, se usaría la macro de `${TM_PLACEMENT_ID_NUM}` como el valor para capturar las ID de posición generadas por la macro de Adobe Advertising.

Para obtener una lista de macros compatibles con los píxeles de eventos de impresión de Audience Manager, consulte &quot;[Captura de datos de impresión de campaña mediante llamadas de píxel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Para obtener una lista de macros compatibles con los píxeles de eventos de clic de Audience Manager, consulte &quot;[Captura de datos de clic de Campaign mediante llamadas de píxel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* Se recomienda incluir la campaña, la ubicación, el creativo (publicidad) y los ID de sitio para poder utilizar los atributos de campaña y crear rasgos de Audience Manager.
>* Para crear informes de Audience Optimization, se requieren parámetros adicionales.
>* En los pares clave-valor, reemplace los valores por los relevantes [DSP macros de](/help/dsp/campaign-management/macros.md) para que pueda usar un solo píxel en todos los anuncios de todas las campañas. Por ejemplo, cambie `d_campaign=[%campaignID%]`hasta `d_campaign=${TM_CAMPAIGN_ID_NUM}` para capturar los ID de campaña generados por la macro de Adobe Advertising.
>* Puede crear sus propios parámetros con valores codificados, si es necesario. Ejemplo: `d_DSP=AdCloud`

Ejemplo de píxel de evento de impresión:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Dónde añadir los píxeles

#### Píxel de seguimiento de impresión

Adjunte un píxel de seguimiento de eventos de impresión a todos los anuncios de su [!DNL DSP] campañas. Puede hacerlo en cualquiera de los siguientes lugares:

* En el nivel de colocación, que aplica el píxel de forma predeterminada a todos los anuncios de la ubicación. En la sección Tracking de la configuración de ubicación, añada el píxel en la [[!UICONTROL Event pixels] campo](/help/dsp/campaign-management/placements/placement-settings.md).

* En el nivel de anuncio, que anula los píxeles de evento de nivel de ubicación. En la configuración del anuncio, [cree un píxel de evento en [!UICONTROL Pixel] pestaña](/help/dsp/campaign-management/ads/ad-edit.md).

* (Para anuncios en un servidor de publicidad de terceros) A nivel de anuncio dentro del servidor de publicidad.

#### Píxel de rastreo de clics

Dentro del servidor de publicidad, inserte el píxel del evento de clic (con la URL codificada adjunta) donde inserte normalmente la URL de pulsación del anuncio.

## Paso 3: Tareas posteriores a la implementación

Una vez implementadas las etiquetas de evento, los datos fluyen a los servidores de recopilación de datos de Audience Manager. Complete las siguientes tareas para poder utilizar los datos en los informes.

### Crear un [!DNL Amazon S3] Contenedor y fuente de datos

Una vez que los datos estén en los servidores de Audience Manager, debe crear un [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), y después una fuente de datos a la que se enviarán todos los datos en píxeles. Póngase en contacto con su consultor Audience Manager o [Atención al cliente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) si necesita asistencia.

### Creación de rasgos y segmentos de Audience Manager

Los datos del evento se transfieren al Audience Manager como [señales no utilizadas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Crear manualmente [rasgos basados en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) a partir de los datos introducidos y, a continuación, cree [segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) con esos rasgos, para poder usar los datos en los informes.

DSP Característica de ejemplo que rellena datos de nivel de usuario para usuarios expuestos a un elemento creativo específico en la aplicación de la aplicación de la siguiente manera

1. Identificar el evento como `d_event = imp`.
1. DSP Identifique el ID creativo dentro de la campaña de la campaña y, a continuación, asígnelo al rasgo como `d_creative=[Creative ID]`.

![Pantalla de creación de rasgos](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP macros](/help/dsp/campaign-management/macros.md)
>* [DSP Información general sobre el envío de datos de exposición de medios de comunicación de a Adobe Audience Manager](overview.md)
>* [Casos de uso](use-cases.md)
