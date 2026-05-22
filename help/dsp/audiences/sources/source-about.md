---
title: Acerca de las fuentes de audiencia de origen
description: Obtenga información acerca de la conversión de otros identificadores de usuario en segmentos de origen a ID universales para la segmentación sin cookies.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
TQID: https://experienceleague.adobe.com/8wdjwhNF-KDspEa1wSYWwlDOJxc3LiyqnSwEE-Fq9bY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 710
ht-degree: 0%

---

# Acerca de las fuentes de audiencia de origen

La función de fuente de audiencia permite importar segmentos de origen que contengan ID universales tal cual o convertirlos en segmentos que contengan tipos de ID universales especificados:

* Los anunciantes de Australia pueden importar segmentos de origen que ya contengan [!DNL AdFixus] ID universales.

* DSP puede introducir segmentos de origen compuestos de ID de correo electrónico con hash, cookies e ID de publicidad móvil (MAID) creados en plataformas de datos del cliente (CDP) adicionales y convertirlos en segmentos compuestos de [!DNL LiveRamp] [!DNL RampIDs] e [!DNL Unified ID 2.0 (UID2.0)] ID.

Para todos los tipos de ID, cada ID resultante se basa en personas y los límites de frecuencia de anuncio se aplican en el nivel de ID <!-- Move that info. to somewhere else? -->. Los detalles del segmento incluyen el tamaño de cada tipo de ID universal y el tamaño de cada tipo de dispositivo rastreado mediante cookies o ID de dispositivo.

## Tipos de ID universales a los que se pueden traducir segmentos de origen {#universal-id-types}

<!--
  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Puede traducir los segmentos de origen de [!DNL ActionIQ], [!DNL Adobe] [!DNL Real-time CDP], [!DNL Amperity], [!DNL Optimizely] y [!DNL Tealium] a segmentos con ID autenticados (determinísticos) de los siguientes socios de ID universales.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Para redireccionar a usuarios que han iniciado sesión.

     [!DNL RampIDs] están disponibles para los usuarios de Norteamérica, Australia y Nueva Zelanda.

     Las tarifas son de 0,15 USD por impresión de anuncio en pantalla entregada y 0,25 USD por impresión de anuncio de vídeo entregada.

   * Para la medición con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * Para redireccionar a usuarios que han iniciado sesión.

     [!DNL UID2 IDs] no están disponibles para los usuarios del Área Económica Europea y algunos países adicionales. Ver la [lista de países prohibidos](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Las tarifas son de 0,15 USD por impresión de anuncio en pantalla entregada y 0,25 USD por impresión de anuncio de vídeo entregada.

<!--
 Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. Contact your Adobe Account Team for instructions.
-->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Plataformas de datos de clientes compatibles para segmentos de origen

DSP ha establecido conectores en los siguientes CDP para introducir rápidamente segmentos de origen.

DSP también puede conectarse a cualquier CDP adicional mediante el uso compartido de datos por lotes, por streaming o basado en API. Para integrarse con un nuevo CDP, póngase en contacto con su equipo de cuenta de Adobe.

### [!DNL ActionIQ]

Puede compartir los datos de origen de su organización desde la plataforma de datos del cliente [!DNL ActionIQ] con DSP para convertir las direcciones de correo electrónico con hash en ID universales para la publicidad de destino en DSP. Esta integración requiere personalización. Póngase en contacto con el equipo de su cuenta de Adobe para obtener más información.

### [!DNL Adobe Real-Time CDP]

DSP es un *destino* integrado para [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=es), que forma parte de Adobe Experience Platform.

En [!DNL Real-Time CDP], los destinos son conexiones a plataformas de datos externas que permiten la activación de datos sin problemas. Puede utilizar destinos para activar sus direcciones de correo electrónico con hash, cookies e ID de publicidad móvil para la publicidad de destino en DSP. Para obtener más información sobre los destinos, consulte la [Guía de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html?lang=es) de Experience Platform, que incluye una descripción general del producto, instrucciones para [crear espacios de trabajo de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html?lang=es) y [crear conexiones de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=es), y [activar datos en destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html?lang=es).

Para permitir que DSP ingrese sus [!DNL Adobe] [!DNL Real-time CDP] segmentos de origen y convierta sus direcciones de correo electrónico con hash, cookies e ID de publicidad móvil en ID universales, consulte &quot;[Convertir los ID de usuario de [!DNL Adobe Real-Time CDP] a ID universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)&quot;.

### [!DNL AdFixus]

Los anunciantes australianos pueden usar la integración de Advertising DSP con [!DNL AdFixus] para importar segmentos de origen que contengan [!DNL AdFixus] ID universales. Esta ruta es independiente de la traducción de los ID de correo electrónico con hash o MAID dentro de un conector CDP a [!DNL RampIDs] o [!DNL UID2] ID. Para obtener más información, consulte &quot;[Importar segmentos de origen desde [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)&quot;.

### [!DNL Amperity]

Puede compartir los datos de origen de su organización desde la plataforma de datos del cliente [!DNL Amperity] con DSP para convertir las direcciones de correo electrónico con hash en ID universales para la publicidad de destino en DSP. Para obtener más información, consulte &quot;[Convertir los identificadores de usuario de [!DNL Amperity] a identificadores universales](/help/dsp/audiences/sources/source-amperity.md)&quot;.

### [!DNL Optimizely]

Puede compartir los datos de origen de su organización desde la plataforma de datos del cliente [!DNL Optimizely] con DSP para convertir las direcciones de correo electrónico con hash en ID universales para la publicidad de destino en DSP. Para obtener más información, consulte &quot;[Convertir los identificadores de usuario de [!DNL Optimizely] a identificadores universales](/help/dsp/audiences/sources/source-optimizely.md)&quot;.

### [!DNL Tealium]

Puede compartir los datos de origen de su organización desde la plataforma de datos del cliente [!DNL Tealium] mediante [!DNL Amazon Web Services]. Para obtener más información sobre cómo convertir las direcciones de correo electrónico con hash en identificadores universales para publicidad de destino en DSP, consulte &quot;[Convertir los identificadores de usuario de [!DNL Tealium] a identificadores universales](/help/dsp/audiences/sources/source-tealium.md)&quot;.

>[!MORELIKETHIS]
>
>* [Administrar orígenes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Compatibilidad para activar identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Convertir los identificadores de usuario de [!DNL Adobe Real-Time CDP] a identificadores universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir los identificadores de usuario de [!DNL Amperity] a identificadores universales](/help/dsp/audiences/sources/source-amperity.md)
>* [Convertir los identificadores de usuario de [!DNL Optimizely] a identificadores universales](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convertir los identificadores de usuario de [!DNL Tealium] a identificadores universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Importar segmentos de origen desde [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
