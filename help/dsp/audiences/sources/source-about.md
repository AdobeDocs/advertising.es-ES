---
title: Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia
description: Obtenga información acerca de la ingesta de segmentos de origen desde una plataforma de datos de clientes.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: f01cfbf22628cec0510f4a860ad927b333d5946a
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia

DSP Puede introducir segmentos de origen compuestos de ID de correo electrónico con hash o ID universales creados dentro de una plataforma de datos del cliente (CDP). Puede utilizar los segmentos ingeridos como destinos para sus ubicaciones.

DSP Los siguientes CDP tienen conectores establecidos, pero el usuario también puede conectarse a cualquier CDP mediante el uso compartido de datos por lotes, por streaming o basados en API. Para integrarse con un nuevo CDP, póngase en contacto con su equipo de cuenta de Adobe.

## [!DNL Adobe Real-Time Customer Data Platform]

DSP está integrado con [el [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=es), que forma parte de Adobe Experience Platform.

Entrada [!DNL Real-Time CDP], *destinos* son conexiones a plataformas de datos externas que permiten la activación de datos sin problemas. DSP Por ejemplo, puede utilizar destinos para activar sus relaciones con los clientes conocidas (como las direcciones de correo electrónico con hash) para la publicidad de destino en todos los formatos digitales admitidos por el servicio de correo electrónico de. Para obtener más información sobre los destinos, consulte el Experience Platform [Guía de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), incluida una descripción general del producto, instrucciones para [creación de espacios de trabajo de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) y [creación de conexiones de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), y [activación de datos en destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Para obtener más información, consulte &quot;[DSP Flujo de trabajo para usar la integración de la con [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

## [!DNL ActionIQ]

Puede compartir los datos de origen de su organización desde el [!DNL Action IQ] DSP plataforma de datos del cliente con la plataforma de datos de. DSP A continuación, puede segmentar las ubicaciones de los segmentos mediante el uso de la variable [!DNL RampIDs] o [!DNL Unified IDs 2.0].

Esta integración requiere personalización. Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

## [!DNL Tealium]

Puede compartir los datos de origen de su organización desde el [!DNL Tealium] plataforma de datos del cliente mediante [!DNL Amazon Web Services]. DSP A continuación, puede segmentar las ubicaciones de los segmentos mediante el uso de la variable [!DNL RampIDs]. Para obtener más información, consulte &quot;[DSP Flujo de trabajo para usar la integración de la con [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [DSP Flujo de trabajo para usar la integración de la con [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [DSP Flujo de trabajo para usar la integración de la con [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Crear una fuente de audiencia para activar audiencias de origen](source-create.md)
>* [Configuración de origen de audiencia](source-settings.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
