---
title: Acerca de las fuentes de audiencia de origen
description: Obtenga información acerca de la conversión de otros identificadores de usuario en segmentos de origen a ID universales para la segmentación sin cookies.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 78ee6ddbfb87915475bcf84bd7cd405a58eccf14
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Acerca de las fuentes de audiencia de origen

*característica de Beta*

DSP Puede introducir segmentos de origen compuestos de ID de correo electrónico con hash creados dentro de su plataforma de datos del cliente (CDP) y convertirlos en segmentos compuestos de ID universales. Cada ID resultante se basa en personas y los límites de frecuencia de anuncios se aplican en el nivel de ID <!-- Move that info. to somewhere else? -->.

Los detalles del segmento incluyen el tamaño de cada tipo de ID universal, así como el tamaño de cada tipo de dispositivo rastreado mediante cookies o ID de dispositivo.

## Tipos de ID universales {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Puede traducir sus segmentos de origen a segmentos con ID autenticados (deterministas) de los siguientes socios de ID universales.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Para redireccionar a usuarios que han iniciado sesión.

     [!DNL RampIDs] están disponibles para los usuarios de Norteamérica, Australia y Nueva Zelanda.

     Las tarifas son de 0,15 USD por impresión de anuncio en pantalla entregada y 0,25 USD por impresión de anuncio de vídeo entregada.

   * Para la medición con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * Para redireccionar a usuarios que han iniciado sesión.

     [!DNL UID2 IDs] no están disponibles para los usuarios del Área Económica Europea y algunos países adicionales. Ver la [lista de países prohibidos](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Las tarifas son de 0,15 USD por impresión de anuncio en pantalla entregada y 0,25 USD por impresión de anuncio de vídeo entregada.

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Plataformas de datos del cliente compatibles para segmentos de origen

DSP ha establecido conectores en los siguientes CDP para introducir rápidamente segmentos de origen.

DSP También puede conectarse a cualquier CDP adicional mediante el uso compartido de datos por lotes, por streaming o basado en API. Para integrarse con un nuevo CDP, póngase en contacto con su equipo de cuenta de Adobe.

### [!DNL Adobe Real-Time Customer Data Platform]

DSP El es un *destino* integrado para [the [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=es), que forma parte de Adobe Experience Platform.

En [!DNL Real-Time CDP], los destinos son conexiones a plataformas de datos externas que permiten la activación de datos sin problemas. DSP Puede utilizar destinos para activar las direcciones de correo electrónico con hash para la publicidad de destino en el sector de la publicidad en el sector de la. Para obtener más información sobre los destinos, consulte la [Guía de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html) del Experience Platform, que incluye información general sobre el producto, instrucciones para [crear espacios de trabajo de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) y [crear conexiones de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) y [activar datos en destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

DSP Para permitir que los usuarios introduzcan sus [!DNL Adobe] [!DNL Real-time CDP] segmentos de origen y conviertan sus direcciones de correo electrónico con hash en identificadores universales, consulte &quot;[Convertir los identificadores de usuario de [!DNL Adobe Real-Time CDP]  a identificadores universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)&quot;.

### [!DNL ActionIQ]

DSP DSP Puede compartir los datos de origen de su organización desde la plataforma de datos del cliente [!DNL ActionIQ] con para convertir sus direcciones de correo electrónico con hash en ID universales para la creación de publicidad de destino en el. Esta integración requiere personalización. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

### [!DNL Amperity]

DSP DSP Puede compartir los datos de origen de su organización desde la plataforma de datos del cliente [!DNL Amperity] con para convertir sus direcciones de correo electrónico con hash en ID universales para la creación de publicidad de destino en el. Para obtener más información, consulte &quot;[Convertir los identificadores de usuario de [!DNL Amperity] a identificadores universales](/help/dsp/audiences/sources/source-amperity.md)&quot;.

### [!DNL Optimizely]

DSP DSP Puede compartir los datos de origen de su organización desde la plataforma de datos del cliente [!DNL Optimizely] con para convertir sus direcciones de correo electrónico con hash en ID universales para la creación de publicidad de destino en el. Para obtener más información, consulte &quot;[Convertir los identificadores de usuario de [!DNL Optimizely] a identificadores universales](/help/dsp/audiences/sources/source-optimizely.md)&quot;.

### [!DNL Tealium]

Puede compartir los datos de origen de su organización desde la plataforma de datos del cliente [!DNL Tealium] mediante [!DNL Amazon Web Services]. DSP Para obtener más información sobre cómo convertir las direcciones de correo electrónico con hash en identificadores universales para la publicidad de destino en el sitio web de, consulte &quot;[Convertir los identificadores de usuario de [!DNL Tealium] a identificadores universales](/help/dsp/audiences/sources/source-tealium.md)&quot;.

>[!MORELIKETHIS]
>
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Convertir los identificadores de usuario de [!DNL Adobe Real-Time CDP] a identificadores universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir los identificadores de usuario de [!DNL Amperity] a identificadores universales](/help/dsp/audiences/sources/source-amperity.md)
>* [Convertir los identificadores de usuario de [!DNL Optimizely] a identificadores universales](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convertir los identificadores de usuario de [!DNL Tealium] a identificadores universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
