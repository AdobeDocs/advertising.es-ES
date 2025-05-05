---
title: Recopilación de datos de clics e impresiones de campañas de Advertising DSP
description: Aprenda a capturar eventos de impresión y clics basados en cookies desde anuncios de Advertising DSP con píxeles de Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Recopilación de datos de exposición de medios de Advertising DSP Campaigns

*Anunciantes solo con Advertising DSP*

*Solo anunciantes con una integración de Adobe Audience Manager de Adobe Advertising*

En este documento se explica cómo etiquetar anuncios de Advertising DSP para capturar impresiones basadas en cookies y eventos de clic mediante píxeles de Audience Manager, así como las tareas adicionales necesarias para utilizar los datos.

Los píxeles de evento no capturan eventos que se producen en entornos sin cookies, como aplicaciones móviles y TV conectada (CTV).

## Paso 1: Configuración de un Source de datos en Audience Manager {#set-up-data-source}

En el Audience Manager DSP, cree una [fuente de datos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=es) para los datos de impresión y de clics de la. Incluya el ID de origen de datos [en cada etiqueta de evento](#implement-dsp-pixels) para que todos los eventos rastreados se atribuyan al origen de datos.

>[!NOTE]
> DSP Es posible recopilar todos los datos de impresiones y clics de las campañas publicitarias que se ejecutan en varias dentro de una sola fuente de datos.

## Paso 2: Implementar píxeles de evento de impresión y clics en páginas web {#implement-dsp-pixels}

Los anunciantes pueden crear e implementar etiquetas de evento para sus propias marcas. Si es necesario, póngase en contacto con su asesor de Adobe Audience Manager o con el equipo de cuenta de Adobe para obtener ayuda.

>[!NOTE]
>
>Si su organización utiliza el seguimiento de [!DNL Analytics], es posible que no necesite el rastreo de clics del Audience Manager. Adobe Analytics captura las señales de clic y puede enviarlas al Audience Manager a través de [reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=es).

### Sintaxis de píxeles

Los píxeles de evento deben incluir los siguientes parámetros.

**Píxeles de seguimiento de impresión:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parámetros adicionales opcionales](#parameters) con el prefijo `&`

**Píxeles de rastreo de clics:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parámetros adicionales opcionales](#parameters) con el prefijo `&`

Donde:

* `[Audience Manager customer domain]` es el nombre de dominio que enviará eventos de impresión o clics a [!DNL Adobe].

* DSP `[source id]` es el identificador de la [fuente de datos](#set-up-data-source) en la que realiza un seguimiento de los datos de impresiones y clics de los datos de los que realiza un seguimiento de los datos de impresión y de los datos de los clics de los que se hace clic en los datos.

* `[redirect URL]` es la URL de redireccionamiento con codificación doble. Si está utilizando una herramienta de codificación en línea, como www.urlencoder.org, ejecute la cadena a través del codificador y vuelva a codificar el resultado.

* DSP `${TM_CAMPAIGN_ID_NUM}` es el identificador numérico de campaña en el. DSP Si desea codificar un ID de campaña individual en lugar de utilizar la macro de, busque el ID en la configuración de la campaña.

* Cada [parámetro](#key-value-pairs) tiene el prefijo `&` y tiene el formato `d_parameter=parameter_id`, donde `parameter` se reemplaza por el par clave-valor del nuevo campo. Ejemplo: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parámetros como pares clave-valor {#parameters}

**Formato:** `d_parameter=parameter_id`

    donde:
    
    * el parámetro tiene el prefijo `&amp;`
    
    * `parameter` se reemplaza por el par clave-valor del nuevo campo
    
    Ejemplo: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Ambos tipos de píxeles pueden contener parámetros adicionales como *pares clave-valor* para recopilar características o para proporcionar metadatos de campaña (como un nombre de ubicación o un nombre de campaña) para otros informes. Un par clave-valor consta de dos elementos relacionados: una *clave*, que es una constante que define el conjunto de datos, y un *valor*, que es una variable que pertenece al conjunto.

En el par clave-valor, la variable de valor puede ser un identificador codificado de forma rígida o una *macro*, que es una pequeña unidad de código independiente que se reemplaza dinámicamente por los valores correspondientes cuando se carga la etiqueta de anuncio para el seguimiento de campañas y usuarios. DSP Para los parámetros relacionados con la campaña, puede usar [macros de](/help/dsp/campaign-management/macros.md) en lugar de macros de Audience Manager para enviar atributos de campaña junto con los datos de impresión o clics correspondientes al Audience Manager, usando un solo píxel en todos los anuncios. DSP Los píxeles de evento deben tener valores adecuados para los pares clave-valor que se incluyen dentro de los píxeles. DSP Por ejemplo, para la clave `d_placement`, se usaría la macro de `${TM_PLACEMENT_ID_NUM}` como valor para capturar los identificadores de ubicación generados por la macro de Adobe Advertising.

Para obtener una lista de macros que admite el Audience Manager para los píxeles de evento de impresión, consulte &quot;[Captura de datos de impresión de campaña mediante llamadas de píxel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=es#supported-key-value-pairs)&quot;.

Para obtener una lista de macros que admite el Audience Manager para los píxeles de evento de clic, consulte &quot;[Captura de datos de clic de campaña mediante llamadas en píxeles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html?lang=es)&quot;.

>[!TIP]
>
>* Se recomienda incluir la campaña, la ubicación, el creativo (publicidad) y los ID de sitio para poder utilizar los atributos de campaña y crear rasgos de Audience Manager.
>* Para crear informes de Audience Optimization, se requieren parámetros adicionales.
>* DSP En los pares clave-valor, reemplace los valores por las [macros de](/help/dsp/campaign-management/macros.md) relevantes para que pueda usar un solo píxel en todos los anuncios de todas las campañas. Por ejemplo, cambie `d_campaign=[%campaignID%]` a `d_campaign=${TM_CAMPAIGN_ID_NUM}` para capturar los identificadores de campaña generados por la macro de Adobe Advertising.
>* Puede crear sus propios parámetros con valores codificados, si es necesario. Ejemplo: `d_DSP=AdCloud`

Ejemplo de píxel de evento de impresión:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Dónde añadir los píxeles

#### Píxel de seguimiento de impresión

Adjunte un píxel de seguimiento de eventos de impresión a todos los anuncios de sus [!DNL DSP] campañas. Puede hacerlo en cualquiera de los siguientes lugares:

* En el nivel de colocación, que aplica el píxel de forma predeterminada a todos los anuncios de la ubicación. En la sección Seguimiento de la configuración de ubicación, agregue el píxel en el campo [[!UICONTROL Event pixels]](/help/dsp/campaign-management/placements/placement-settings.md).

* En el nivel de anuncio, que anula los píxeles de evento de nivel de ubicación. En la configuración del anuncio, [cree un píxel de evento en la ficha [!UICONTROL Pixel]](/help/dsp/campaign-management/ads/ad-edit.md).

* (Para anuncios en un servidor de publicidad de terceros) A nivel de anuncio dentro del servidor de publicidad.

#### Píxel de rastreo de clics

Dentro del servidor de publicidad, inserte el píxel del evento de clic (con la URL codificada adjunta) donde inserte normalmente la URL de pulsación del anuncio.

## Paso 3: Tareas posteriores a la implementación

Una vez implementadas las etiquetas de evento, los datos fluyen a los servidores de recopilación de datos de Audience Manager. Complete las siguientes tareas para poder utilizar los datos en los informes.

### Crear un bloque de [!DNL Amazon S3] y Data Source

Una vez que los datos estén en los servidores de Audience Manager, debe crear un bloque de [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) y, a continuación, un origen de datos al que se envíen todos los datos en píxeles. Póngase en contacto con su asesor Audience Manager o con [Atención al cliente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html?lang=es) si necesita asistencia.

### Creación de rasgos y segmentos de Audience Manager

Los datos del evento se transfieren al Audience Manager como [señales no utilizadas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html?lang=es). Cree manualmente [rasgos basados en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=es) a partir de los datos ingeridos y, a continuación, cree [segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html?lang=es) utilizando esos rasgos, para poder usar los datos en los informes.

DSP Característica de ejemplo que rellena datos de nivel de usuario para usuarios expuestos a un elemento creativo específico en la aplicación de la aplicación de la siguiente manera

1. Identifique el evento como `d_event = imp`.
1. DSP Identifique el ID creativo dentro de la campaña de la campaña y luego asígnelo al rasgo como `d_creative=[Creative ID]`.

![Pantalla de creación de rasgos](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* DSP [Macros de](/help/dsp/campaign-management/macros.md)
>* DSP [Información general sobre el envío de datos de exposición de medios de comunicación de la a Adobe Audience Manager](overview.md)
>* [Casos de uso](use-cases.md)
