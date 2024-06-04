---
title: Importar manualmente segmentos autenticados de [!DNL LiveRamp]
description: Obtenga información acerca de la activación de audiencias autenticadas mediante [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: f10a0bd487d641bd150d9ecbefe907b2bf25e5a7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Importar manualmente segmentos autenticados de [!DNL LiveRamp]

*Función beta*

Puede enviar manualmente mensajes autenticados [!DNL LiveRamp] DSP segmentos que se van a con [!DNL LiveRamp] [!DNL Connect] panel. Puede utilizar segmentos importados para la segmentación de ubicación. Para segmentos de origen, las tarifas son de 0,15 USD por impresión de anuncio en pantalla entregada y 0,25 USD por impresión de anuncio de vídeo entregada.

La asignación y carga de segmentos para cada trabajo de importación puede tardar hasta siete días.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Complete los siguientes pasos en la [!DNL Connect] panel:

   1. Activar el mosaico de destino **[!DNL AAC API 1P Onboarding]**.

   1. Establecer [!DNL Identifier Settings] hasta **[!DNL Ramp ID]** solo.

      ![Configuración de identificador](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Opcional) Si desea seguir recibiendo identificadores basados en cookies, cree un segundo [!DNL AAC API 1P Onboarding] mosaico de destino con &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; y &quot;[!DNL AAID]&quot; seleccionado.

   1. Verifique en su biblioteca de audiencias (que está disponible cuando crea o edita una audiencia desde [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) en el que se importó todo el recuento de segmentos.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](source-about.md)
>* [Crear una fuente de audiencia para activar audiencias de ID universal](source-create.md)
>* [Configuración de origen de audiencia](source-settings.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
