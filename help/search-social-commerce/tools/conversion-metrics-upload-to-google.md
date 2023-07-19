---
title: Cargar métricas de conversión en [!DNL Google Ads]
description: Obtenga información sobre cómo cargar métricas de conversión de búsqueda, medios sociales y de comercio a [!DNL Google Ads].
exl-id: 88db66c2-12db-41cf-b6c4-ed821cb3b8ea
source-git-commit: 00f9e5e3892be305f5d7c69161bdb7609f13f1bf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Cargar métricas de conversión en [!DNL Google Ads]

*Anunciantes con [!DNL Google Ads] Solo cuentas*

Search, Social y Commerce pueden cargarse de forma opcional en [!DNL Google Ads] todas las métricas de conversión para las que realiza un seguimiento [!DNL Google Ads] campañas que utilizan el servicio de seguimiento de conversión de Adobe Advertising y las métricas de conversión sincronizadas desde Adobe Analytics. Esta opción no hace que las conversiones estén disponibles para la optimización híbrida. Si desea utilizar las conversiones de Adobe para la optimización híbrida, consulte &quot;[Habilitar la carga de objetivos en las redes de publicidad](objective-upload-to-networks.md).&quot;

Las cargas diarias incluyen el seguimiento `gclid` , el valor de conversión definido con el modelo de atribución de nivel de anunciante y la marca de tiempo. Si se actualiza el modelo de atribución, la siguiente carga utiliza el nuevo modelo, pero los datos anteriores no se actualizan para utilizar el nuevo modelo.

>[!NOTE]
>
>Las cargas no incluyen métricas de conversión cargadas en el Adobe Advertising desde archivos de fuentes de.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleccione la casilla de verificación situada junto a **[!UICONTROL Upload Conversions to Google Ads]**.

1. Haga clic **[!UICONTROL Save]**.

1. (Si las conversiones se rastrean en el nivel de cuenta de responsable) [Añadir credenciales para la cuenta de responsable](/help/search-social-commerce/admin/manager-accounts.md) en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Habilitar la carga de objetivos en las redes de publicidad](objective-upload-to-networks.md)
