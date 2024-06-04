---
title: Crear una fuente de audiencia para activar audiencias de ID universal
description: Obtenga información sobre cómo crear una fuente para importar audiencias desde la plataforma de datos del cliente y convertirlas en segmentos que contengan ID universales.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Crear una fuente de audiencia para activar audiencias de ID universal

*Función beta*

DSP Cree una fuente de datos en los segmentos para cada audiencia de origen en la plataforma de datos del cliente que desee convertir en segmentos que contengan tipos de ID universales especificados. DSP Puede importar los segmentos a la cuenta de usuario de la organización o a una cuenta de anunciante de la cuenta de la organización de que se trate. Los cargos por datos se aplican en función de los tipos de ID universal seleccionados.

Se requieren pasos adicionales para introducir las audiencias de cada plataforma de datos del cliente. Consulte la nota al final del procedimiento.

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clic **[!UICONTROL Add Source]**.

1. En el [!UICONTROL Select a Type] menú, seleccione la plataforma de datos del cliente:

   * *[!UICONTROL RT-CDP]*: [El [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: La [[!DNL ActionIQ] plataforma de datos del cliente](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (solo usuarios configurados) El [[!DNL Tealium] plataforma de datos del cliente](source-about.md).

1. Especifique el [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Introduzca el resto [configuración de origen](source-settings.md).

   Conserve una copia del [!UICONTROL Source Key] que se genera. Necesitará el valor más tarde.

1. Clic **[!UICONTROL Save]**.

>[!NOTE]
>
>Después de crear una fuente para la plataforma de datos del cliente, deberá completar los pasos adicionales. Consulte la [flujo de trabajo para importar audiencias desde [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> y el [flujo de trabajo para importar audiencias desde [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Configuración de origen de audiencia](source-settings.md)
>* [Acerca de las fuentes de audiencia de origen](source-about.md)
>* [Conexión de Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
