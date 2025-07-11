---
title: Cargar métricas de conversión de búsqueda, medios sociales y seguimiento de Commerce en  [!DNL Google Ads]
description: Aprenda a cargar métricas de conversión de búsqueda, medios sociales y seguimiento de Commerce en  [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Cargar métricas de conversión de búsqueda, medios sociales y seguimiento de Commerce en [!DNL Google Ads]

*Anunciantes con [!DNL Google Ads] cuentas y solo seguimiento de conversión de Adobe Advertising*

Search, Social y Commerce pueden cargar opcionalmente en [!DNL Google Ads] todas las métricas de conversión que rastrea para [!DNL Google Ads] campañas que usan el servicio de seguimiento de conversión de Adobe Advertising. Esta opción no hace que las conversiones estén disponibles para la optimización híbrida. Si desea usar las conversiones de Adobe para la optimización híbrida, consulte &quot;[Habilitar la carga de objetivos en las redes de anuncios](objective-upload-to-networks.md)&quot;.

Las cargas diarias incluyen el valor `gclid` rastreado, el valor de conversión definido mediante el modelo de atribución de nivel de anunciante y la marca de tiempo. Si se actualiza el modelo de atribución, la siguiente carga utiliza el nuevo modelo, pero los datos anteriores no se actualizan para utilizar el nuevo modelo.

>[!NOTE]
>
>Las cargas no incluyen métricas de conversión cargadas en Adobe Advertising desde archivos de fuentes.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Active la casilla de verificación situada junto a **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Anunciantes que realizan negocios en el Espacio Económico Europeo (EEE) o en el Reino Unido (Reino Unido); opcional) Si ha obtenido el consentimiento de usuarios de EEE y Reino Unido para cargar sus datos con fines publicitarios, active la casilla de verificación situada junto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Haga clic en **[!UICONTROL Save]**.

1. (Si las conversiones se rastrean en el nivel de cuenta de administrador) [Agregue credenciales para la cuenta de administrador](/help/search-social-commerce/admin/manager-accounts.md) en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Habilitar la carga de objetivos en las redes de anuncios](objective-upload-to-networks.md)
