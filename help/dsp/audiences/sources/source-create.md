---
title: Crear una fuente de audiencia para activar audiencias de origen
description: Obtenga información sobre cómo crear un origen para importar audiencias a su cuenta de o a una cuenta de anunciante.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Crear una fuente de audiencia para activar audiencias de origen

*Función beta*

<!-- Will this remain for admin users/Adobe Account Team users only? -->

DSP Cree un origen para importar audiencias a su cuenta de o a una cuenta de anunciante. Actualmente, puede importar audiencias de [el [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>Después de crear un origen para [!DNL Real-Time CDP], tendrá que activar su [!DNL Real-Time CDP] audiencias a través del Adobe DSP Publicidad Destino de la publicidad dentro de [!DNL Real-Time CDP] para comenzar a importarlos. Consulte [los pasos del flujo de trabajo de activación](source-about.md#workflow-sources).

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources (BETA)].

1. Haga clic [!UICONTROL Add Source].

1. En el [!UICONTROL Select a Type] , seleccione el tipo de origen.

   *[!UICONTROL RT-CDP]*: este tipo de origen, para [el [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), es la única opción.

1. Especifique el [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Introduzca el resto [configuración de origen](source-settings.md).

   Conserve una copia del [!UICONTROL Source Key] que se genera. Necesitará el valor más tarde.

1. Haga clic **[!UICONTROL Save]**.

1. En Experience Platform DSP, cree una conexión de destino de Advertising con el [!UICONTROL Source Key] DSP que se generó en la configuración de origen de la.

   DSP Para obtener instrucciones sobre cómo activar la conexión de destino de la, seleccionar segmentos y acceder a permisos de control, consulte &quot;[Conexión de Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Configuración de origen de audiencia](source-settings.md)
>* [Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia](source-about.md)
>* [Activar segmentos autenticados de socios de ID duraderos](source-durable-id.md)<!-- title?-->
>* [Conexión de Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)

