---
title: Recopilación de datos de clics e impresiones de campañas de Advertising DSP
description: Aprenda a capturar eventos de impresión y clics basados en cookies desde anuncios de Advertising DSP con píxeles de Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Recopilación de datos de exposición de medios de campañas de Advertising DSP

*Anunciantes solo con Advertising DSP*

*Solo anunciantes con una integración Adobe Advertising-Adobe Audience Manager*

En este documento se explica cómo etiquetar anuncios de Advertising DSP para capturar impresiones y clics basados en cookies mediante píxeles de Audience Manager, así como las tareas adicionales necesarias para utilizar los datos.

Los píxeles de evento no capturan eventos que se producen en entornos sin cookies, como aplicaciones móviles y TV conectada (CTV).

## Paso 1: Configurar una fuente de datos en Audience Manager {#set-up-data-source}

En Audience Manager, cree una [fuente de datos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) para la impresión de DSP y haga clic en datos. Incluya el ID de origen de datos [en cada etiqueta de evento](#implement-dsp-pixels) para que todos los eventos rastreados se atribuyan al origen de datos.

>[!NOTE]
> Es posible recopilar todos los datos de impresiones y clics de campañas publicitarias que se ejecuten en varios DSP dentro de una sola fuente de datos.

## Paso 2: Implementar píxeles de evento de impresión y clics en páginas web {#implement-dsp-pixels}

Los anunciantes pueden crear e implementar etiquetas de evento para sus propias marcas. Si es necesario, póngase en contacto con su consultor de Adobe Audience Manager o con el equipo de cuenta de Adobe para obtener ayuda.

>[!NOTE]
>
>Si su organización utiliza el seguimiento de [!DNL Analytics], es posible que no necesite el rastreo de clics de Audience Manager. Adobe Analytics captura las señales de clic y puede enviarlas a Audience Manager a través de [reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Sintaxis en píxeles

Los píxeles de evento deben incluir los siguientes parámetros.

**Píxeles de seguimiento de impresión:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parámetros adicionales opcionales](#parameters) con el prefijo `&`

**Píxeles de rastreo de clics:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parámetros adicionales opcionales](#parameters) con el prefijo `&`

Donde:

* `[Audience Manager customer domain]` es el nombre de dominio que enviará eventos de impresión o clics a [!DNL Adobe].

* `[source id]` es el identificador de la [fuente de datos](#set-up-data-source) en la que realiza el seguimiento de los datos de impresión y clics de DSP.

* `[redirect URL]` es la URL de redireccionamiento con codificación doble. Si está utilizando una herramienta de codificación en línea, como www.urlencoder.org, ejecute la cadena a través del codificador y vuelva a codificar el resultado.

* `${TM_CAMPAIGN_ID_NUM}` es el ID de campaña numérico en DSP. Si desea codificar un ID de campaña individual en lugar de utilizar la macro de DSP, busque el ID en la configuración de la campaña.

* Cada [parámetro](#key-value-pairs) tiene el prefijo `&` y tiene el formato `d_parameter=parameter_id`, donde `parameter` se reemplaza por el par clave-valor del nuevo campo. Ejemplo: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parámetros como pares clave-valor {#parameters}

**Formato:** `d_parameter=parameter_id`

    donde:
    
    * el parámetro tiene el prefijo `&amp;`
    
    * `parameter` se reemplaza por el par clave-valor del nuevo campo
    
    Ejemplo: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Ambos tipos de píxeles pueden contener parámetros adicionales como *pares clave-valor* para recopilar características o para proporcionar metadatos de campaña (como un nombre de ubicación o un nombre de campaña) para otros informes. Un par clave-valor consta de dos elementos relacionados: una *clave*, que es una constante que define el conjunto de datos, y un *valor*, que es una variable que pertenece al conjunto.

En el par clave-valor, la variable de valor puede ser un identificador codificado de forma rígida o una *macro*, que es una pequeña unidad de código independiente que se reemplaza dinámicamente por los valores correspondientes cuando se carga la etiqueta de anuncio para el seguimiento de campañas y usuarios. Para los parámetros relacionados con la campaña, puede usar [macros de DSP](/help/dsp/campaign-management/macros.md) en lugar de macros de Audience Manager para enviar atributos de campaña junto con los datos de impresiones o clics correspondientes a Audience Manager, usando un solo píxel en todos los anuncios. Las macros de DSP que inserte en los píxeles de evento deben ser valores adecuados para los pares clave-valor que incluya dentro de los píxeles. Por ejemplo, para la clave `d_placement`, utilizaría la macro de DSP `${TM_PLACEMENT_ID_NUM}` como valor para capturar los identificadores de ubicación generados por la macro de Adobe Advertising.

Para obtener una lista de macros compatibles con Audience Manager para los píxeles de evento de impresión, consulte &quot;[Captura de datos de impresión de campaña mediante llamadas en píxeles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs)&quot;.

Para obtener una lista de macros compatibles con Audience Manager para los píxeles de eventos de clic, consulte &quot;[Captura de datos de clics de Campaign mediante llamadas en píxeles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html)&quot;.

>[!TIP]
>
>* Se recomienda incluir la campaña, la ubicación, el creativo (publicidad) y los ID de sitio para poder utilizar los atributos de campaña y crear características de Audience Manager.
>* Para crear informes de Audience Optimization, se requieren parámetros adicionales.
>* En los pares clave-valor, reemplace los valores por las [macros de DSP](/help/dsp/campaign-management/macros.md) relevantes para que pueda usar un solo píxel en todos los anuncios de todas las campañas. Por ejemplo, cambie `d_campaign=[%campaignID%]` a `d_campaign=${TM_CAMPAIGN_ID_NUM}` para capturar los identificadores de campaña generados por la macro de Adobe Advertising.
>* Puede crear sus propios parámetros con valores codificados, si es necesario. Ejemplo: `d_DSP=AdCloud`

Ejemplo de píxel de evento de impresión:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Dónde añadir los píxeles

#### Pixel de seguimiento de impresión

Adjunte un píxel de seguimiento de eventos de impresión a todos los anuncios de sus [!DNL DSP] campañas. Puede hacerlo en cualquiera de los siguientes lugares:

* En el nivel de colocación, que aplica el píxel de forma predeterminada a todos los anuncios de la ubicación. En la sección Seguimiento de la configuración de ubicación, agregue el píxel en el campo [[!UICONTROL Event pixels]](/help/dsp/campaign-management/placements/placement-settings.md).

* En el nivel de anuncio, que anula los píxeles de evento de nivel de ubicación. En la configuración del anuncio, [cree un píxel de evento en la ficha [!UICONTROL Pixel]](/help/dsp/campaign-management/ads/ad-edit.md).

* (Para anuncios en un servidor de publicidad de terceros) A nivel de anuncio dentro del servidor de publicidad.

#### Pixel de rastreo de clics

Dentro del servidor de publicidad, inserte el píxel del evento de clic (con la URL codificada adjunta) donde inserte normalmente la URL de pulsación del anuncio.

## Paso 3: Tareas posteriores a la implementación

Una vez implementadas las etiquetas de evento, los datos fluyen a los servidores de recopilación de datos de Audience Manager. Complete las siguientes tareas para poder utilizar los datos en los informes.

### Crear un bloque de [!DNL Amazon S3] y un origen de datos

Una vez que los datos estén en los servidores de Audience Manager, debe crear un bloque de [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) y, a continuación, un origen de datos al que se envíen todos los datos en píxeles. Póngase en contacto con su asesor de Audience Manager o con el [Servicio de atención al cliente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) si necesita asistencia.

### Creación de rasgos y segmentos de Audience Manager

Los datos del evento se transfieren a Audience Manager como [señales sin usar](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Cree manualmente [rasgos basados en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) a partir de los datos ingeridos y, a continuación, cree [segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) utilizando esos rasgos, para poder usar los datos en los informes.

Característica de ejemplo que rellena datos de nivel de usuario para usuarios expuestos a un elemento creativo específico en DSP:

1. Identifique el evento como `d_event = imp`.
1. Identifique el ID creativo dentro de la campaña de DSP y luego asígnelo al rasgo como `d_creative=[Creative ID]`.

![Pantalla de creación de rasgos](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Macros de DSP](/help/dsp/campaign-management/macros.md)
>* [Información general sobre el envío de datos de exposición de medios de DSP a Adobe Audience Manager](overview.md)
>* [Casos de uso](use-cases.md)
