---
title: Habilitar la carga de objetivos en las redes de publicidad
description: Obtenga información sobre cómo cargar objetivos para sus portafolios híbridos en [!DNL Google Ads] y [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 7b857f2f75f05685d0776c710a442088a72f590c
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Habilitar la carga de objetivos en las redes de publicidad

*Anunciantes con [!DNL Google Ads] y [!DNL Microsoft® Advertising] solo cuentas*

*Anunciantes habilitados solo para la optimización híbrida*

Si la cuenta del anunciante está configurada para utilizar la optimización híbrida, Adobe Advertising puede, opcionalmente, cargar los objetivos de las carteras de la cuenta en [!DNL Google Ads] y [!DNL Microsoft® Advertising] como conversiones, de modo que pueda utilizarlas para la optimización híbrida.

Al habilitar esta opción, se déclencheur automáticamente la carga de contenido para portafolios que contengan campañas con estrategias de oferta inteligente. Search, Social y Commerce crean una conversión en la red de anuncios para cada combinación de objetivo y portafolio aplicable. Cada conversión tiene el nombre `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, donde `<portfolio_id>` es el ID de portafolio numérico y `<se_acctid/conversion_manager_se_acctid>` es el identificador numérico de la cuenta de red de publicidad o de la cuenta de administrador. La conversión representa todas las métricas de conversión ponderadas en el objetivo.

Cargas en [!DNL Google Ads] se producen diariamente a las 06:00 en el huso horario del anunciante. Cargas en [!DNL Microsoft® Advertising] se producen diariamente a las 09:00 en el huso horario del anunciante.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleccione la casilla de verificación situada junto a **[!UICONTROL Enable Objective Upload]**.

1. (Anunciantes con [!DNL Google Ads] cuentas que realizan negocios en el Espacio Económico Europeo (EEE) o en el Reino Unido (Reino Unido); opcional) Si ha obtenido el consentimiento de los usuarios de EEE y del Reino Unido para cargar sus datos con fines publicitarios, active la casilla de verificación situada junto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clic **[!UICONTROL Save]**.

1. (Si las conversiones se rastrean en el nivel de cuenta de responsable) [Añadir credenciales para la cuenta de responsable](/help/search-social-commerce/admin/manager-accounts.md) en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de las métricas de conversión de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Cargar métricas de conversión en [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
