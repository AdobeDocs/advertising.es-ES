---
title: Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia
description: Obtenga información acerca de la ingesta de segmentos de origen desde una plataforma de datos de clientes.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: f6308ac9af8019987f4a2e501cba6b019cb032b6
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia

<!-- Doesn't specifically explain what you can do in our UI -->
*Función beta*

DSP puede introducir segmentos de origen compuestos de señales autenticadas creadas dentro de una plataforma de datos del cliente (CDP). Puede utilizar los segmentos ingeridos como destinos para sus ubicaciones.

## [!DNL Adobe Real-Time Customer Data Profile]

DSP La integración de con el se ha integrado con el [el [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), que forma parte de Adobe Experience Platform.

Entrada [!DNL Real-time CDP], *destinos* son conexiones a plataformas de datos externas que permiten la activación de datos sin problemas. DSP Por ejemplo, puede utilizar destinos para activar sus relaciones con los clientes conocidas (como las direcciones de correo electrónico con hash) para la publicidad de destino en todos los formatos digitales admitidos por el servicio de correo electrónico de.

Para obtener más información sobre los destinos, consulte el Experience Platform [Guía de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), incluida una descripción general del producto, instrucciones para [creación de espacios de trabajo de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) y [creación de conexiones de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), y [activación de datos en destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### DSP Flujo de trabajo para usar la integración de la con [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [DSP Permitir la traducción de segmentos de datos de clientes a [!DNL LiveRamp RampIDs]](source-durable-id.md) que son reconocibles en un entorno de oferta.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Crear una fuente de audiencia](source-create.md) DSP para importar audiencias a su cuenta de o a una cuenta de anunciante de.

1. [Configurar un [!DNL Real-Time CDP] conexión de destino en Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

Para obtener soporte adicional, póngase en contacto con el equipo de cuenta de Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Activar segmentos autenticados de socios de ID duraderos](source-durable-id.md)
>* [Crear una fuente de audiencia para activar audiencias de origen](source-create.md)
>* [Configuración de origen de audiencia](source-settings.md)
>* [Conexión de Adobe DSP Advertising](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Resumen del catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)

