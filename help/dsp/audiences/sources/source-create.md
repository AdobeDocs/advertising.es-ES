---
title: Crear una fuente de audiencia para activar audiencias de origen
description: Obtenga información sobre cómo crear un origen para importar audiencias a su cuenta de o a una cuenta de anunciante.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Crear una fuente de audiencia para activar audiencias de origen

<!-- Will this remain for admin users/Adobe Account Team users only? -->

DSP DSP Cree una fuente en para importar audiencias de origen en su cuenta de o en una cuenta de anunciante.

Para ver los pasos adicionales necesarios para introducir segmentos de plataformas de datos de clientes específicas, consulte [los flujos de trabajo de activación específicos de audiencia](source-about.md)

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clic **[!UICONTROL Add Source]**.

1. En el [!UICONTROL Select a Type] , seleccione el tipo de origen.

   * *[!UICONTROL RT-CDP]*: [El [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*: La [[!DNL Tealium] plataforma de datos del cliente](source-about.md).

1. Especifique el [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Introduzca el resto [configuración de origen](source-settings.md).

   Conserve una copia del [!UICONTROL Source Key] que se genera. Necesitará el valor más tarde.

1. Clic **[!UICONTROL Save]**.

>[!NOTE]
>
>Después de crear una fuente para la plataforma de datos del cliente, deberá completar los pasos adicionales. Consulte la [flujo de trabajo de activación para [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> y el [flujo de trabajo de activación para [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Configuración de origen de audiencia](source-settings.md)
>* [Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia](source-about.md)
>* [Activar segmentos autenticados de socios de ID universales](source-universal-id.md)<!-- title?-->
>* [Conexión de Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
