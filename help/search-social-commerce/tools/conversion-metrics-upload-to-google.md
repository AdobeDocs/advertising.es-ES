---
title: Cargar métricas de conversión en [!DNL Google Ads]
description: Obtenga información sobre cómo cargar métricas de conversión de búsqueda, medios sociales y de comercio a [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: 608c1a189017f1a7ebfbccf3d8b3455886c297f9
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Cargar métricas de conversión en [!DNL Google Ads]

*Anunciantes con [!DNL Google Ads] Solo cuentas*

Search, Social y Commerce pueden cargarse de forma opcional en [!DNL Google Ads] todas las métricas de conversión para las que realiza un seguimiento [!DNL Google Ads] campañas que utilizan el servicio de seguimiento de conversión de Adobe Advertising. Esta opción no hace que las conversiones estén disponibles para la optimización híbrida. Si desea utilizar las conversiones de Adobe para la optimización híbrida, consulte &quot;[Habilitar la carga de objetivos en las redes de publicidad](objective-upload-to-networks.md).&quot;

Las cargas diarias incluyen el seguimiento `gclid` , el valor de conversión definido con el modelo de atribución de nivel de anunciante y la marca de tiempo. Si se actualiza el modelo de atribución, la siguiente carga utiliza el nuevo modelo, pero los datos anteriores no se actualizan para utilizar el nuevo modelo.

>[!NOTE]
>
>Las cargas no incluyen métricas de conversión cargadas en el Adobe Advertising desde archivos de fuentes de.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleccione la casilla de verificación situada junto a **[!UICONTROL Upload Conversions to Google Ads]**.

1. Clic **[!UICONTROL Save]**.

1. (Si las conversiones se rastrean en el nivel de cuenta de responsable) [Añadir credenciales para la cuenta de responsable](/help/search-social-commerce/admin/manager-accounts.md) en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Habilitar la carga de objetivos en las redes de publicidad](objective-upload-to-networks.md)
