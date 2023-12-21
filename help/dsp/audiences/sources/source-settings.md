---
title: Configuración de origen de audiencia
description: Obtenga información acerca de la configuración de las fuentes de audiencia.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Configuración de origen de audiencia

**[!UICONTROL Data Visibility Level]:** Si los segmentos están disponibles para un solo anunciante con acceso a la cuenta (*[!UICONTROL Advertiser]*) o a todos los anunciantes con acceso a la cuenta *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Solo visibilidad a nivel de anunciante) El anunciante para el que los segmentos están disponibles. Seleccione uno de la lista de anunciantes con acceso a la cuenta.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] solo fuentes) El ID de organización de Adobe Experience Cloud para [!DNL Adobe Experience Platform] cuenta.

**[!UICONTROL Convert PII to the following IDs]:** ([!DNL ActionIQ] y [!DNL Tealium] (solo fuentes de datos) El tipo de ID al que desea convertir la información de identificación personal (PII). Los cargos por datos se aplican según corresponda.

* *[!DNL RampID]:* Para convertir PII en RampID. Si elige *[!DNL RampID]*, los segmentos se traducen en [!DNL RampIDs] automáticamente.

* *[!DNL Unified ID2.0]:* ([!DNL ActionIQ] (solo fuentes de datos) Para convertir PII en un [ID unificado 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]:** DSP (Solo lectura; se genera automáticamente) La clave de origen que puede utilizar para crear una conexión de destino en la plataforma de datos del cliente para insertar audiencias en Advertising. Puede copiar el valor en el portapapeles para pegarlo en la configuración de conexión de destino o en un archivo.

>[!MORELIKETHIS]
>
>* [Crear una fuente de audiencia para activar audiencias de origen](source-create.md)
>* [Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia](source-about.md)
>* [Activar segmentos autenticados de socios de ID universales](source-universal-id.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
