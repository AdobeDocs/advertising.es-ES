---
title: Acerca de las fuentes de audiencia de origen
description: Obtenga información acerca de la conversión de otros identificadores de usuario en segmentos de origen a ID universales para la segmentación sin cookies.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: bd0586516c2457e4dfcd1a23046707e8bf652e3b
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Acerca de las fuentes de audiencia de origen

*Función beta*

DSP Puede introducir segmentos de origen compuestos de ID de correo electrónico con hash creados dentro de su plataforma de datos del cliente (CDP) y convertirlos en segmentos compuestos de ID universales. Cada ID resultante se basa en personas y los límites de frecuencia de anuncio se aplican al nivel de ID<!-- Move that info. to somewhere else? -->.

Los detalles del segmento incluyen el tamaño de cada tipo de ID universal, así como el tamaño de cada tipo de dispositivo rastreado mediante cookies o ID de dispositivo.

## Tipos de ID universales {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Puede traducir sus segmentos de origen a segmentos con ID autenticados (deterministas) de los siguientes socios de ID universales.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Para redireccionar a usuarios que han iniciado sesión.

     [!DNL RampIDs] están disponibles para usuarios de Norteamérica, Australia y Nueva Zelanda.

     Las tarifas son de 0,15 USD por impresión de anuncio en pantalla entregada y 0,25 USD por impresión de anuncio de vídeo entregada.

   * Para la medición utilizando [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * Para redireccionar a usuarios que han iniciado sesión.

     [!DNL UID2 IDs] no están disponibles para los usuarios del Espacio Económico Europeo y de otros países. Consulte la [lista de países prohibidos](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

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

DSP es un integrado de la *destino* para [el [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=es), que forma parte de Adobe Experience Platform.

Entrada [!DNL Real-Time CDP], los destinos son conexiones a plataformas de datos externas que permiten la activación de datos sin problemas. DSP Puede utilizar destinos para activar las direcciones de correo electrónico con hash para la publicidad de destino en el sector de la publicidad en el sector de la. Para obtener más información sobre los destinos, consulte el Experience Platform [Guía de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), incluida una descripción general del producto, instrucciones para [creación de espacios de trabajo de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) y [creación de conexiones de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), y [activación de datos en destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

DSP Para permitir a los usuarios de la ingesta de su [!DNL Adobe] [!DNL Real-time CDP] segmentos de origen y convierta sus direcciones de correo electrónico con hash en ID universales, consulte &quot;[Conversión de ID de usuario [!DNL Adobe Real-Time CDP] a los ID universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

### [!DNL ActionIQ]

Puede compartir los datos de origen de su organización desde el [!DNL Action IQ] DSP DSP plataforma de datos del cliente con el fin de convertir las direcciones de correo electrónico con hash en ID universales para la publicidad de destino en el sector de la publicidad de la. Esta integración requiere personalización. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

### [!DNL Tealium]

Puede compartir los datos de origen de su organización desde el [!DNL Tealium] plataforma de datos del cliente mediante [!DNL Amazon Web Services]. DSP Para obtener más información sobre la conversión de las direcciones de correo electrónico con hash a ID universales para la publicidad de destino en el mundo de los anuncios, consulte &quot;[Conversión de ID de usuario [!DNL Tealium] a los ID universales](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [Conversión de ID de usuario [!DNL Adobe Real-Time CDP] a los ID universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Conversión de ID de usuario [!DNL Tealium] a los ID universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Crear una fuente de audiencia para activar audiencias de ID universal](source-create.md)
>* [Configuración de origen de audiencia](source-settings.md)
>* [Compatibilidad con la activación de ID universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
