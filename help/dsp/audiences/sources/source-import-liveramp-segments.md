---
title: Importar manualmente segmentos autenticados de  [!DNL LiveRamp]
description: Obtenga información acerca de la activación de audiencias autenticadas mediante  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
TQID: https://experienceleague.adobe.com/ln4e1Jmq7vRhOIeg25UwNR8yToni5CuokxAcmEPMwEQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# Importar manualmente segmentos autenticados de [!DNL LiveRamp]

Puede enviar manualmente [!DNL LiveRamp] segmentos autenticados a DSP mediante el panel [!DNL LiveRamp] [!DNL Connect]. Puede utilizar segmentos importados para la segmentación de ubicación. Para segmentos de origen, las tarifas son de 0,15 USD por impresión de anuncio en pantalla entregada y 0,25 USD por impresión de anuncio de vídeo entregada.

La asignación y carga de segmentos para cada trabajo de importación puede tardar hasta siete días.

<!--
Is this first step relevant for this process?

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
>* [Administrar orígenes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
>* [Importar segmentos de origen desde [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
