---
title: Importar manualmente segmentos autenticados de  [!DNL LiveRamp]
description: Obtenga información acerca de la activación de audiencias autenticadas mediante  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Importar manualmente segmentos autenticados de [!DNL LiveRamp]

*característica de Beta*

DSP Puede enviar manualmente [!DNL LiveRamp] segmentos autenticados a mediante el panel [!DNL LiveRamp] [!DNL Connect] para que se puedan usar los segmentos de autenticación que se han autenticado con el panel . Puede utilizar segmentos importados para la segmentación de ubicación. Para segmentos de origen, las tarifas son de 0,15 USD por impresión de anuncio en pantalla entregada y 0,25 USD por impresión de anuncio de vídeo entregada.

La asignación y carga de segmentos para cada trabajo de importación puede tardar hasta siete días.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Complete los siguientes pasos en el panel [!DNL Connect]:

   1. Activar el mosaico de destino **[!DNL AAC API 1P Onboarding]**.

   1. Establezca [!DNL Identifier Settings] solo en **[!DNL Ramp ID]**.

      ![Configuración del identificador](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Opcional) Si desea seguir recibiendo identificadores basados en cookies, cree un segundo mosaico de destino [!DNL AAC API 1P Onboarding] con &quot;[!DNL Cookies]&quot;, &quot;[!DNL IDFA]&quot; y &quot;[!DNL AAID]&quot; seleccionados.

   1. Compruebe en su biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o en la configuración de ubicación) que se importó todo el recuento de segmentos.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=es)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
