---
title: Habilitar la carga de objetivos en las redes de publicidad
description: Obtenga información sobre cómo cargar objetivos para sus portafolios híbridos en [!DNL Google Ads] y [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 1f2ffd65f9341db4492a2796bc82ed0bb42f13ed
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Habilitar la carga de objetivos en las redes de publicidad

*Anunciantes con [!DNL Google Ads] y [!DNL Microsoft® Advertising] solo cuentas*

*Anunciantes habilitados solo para la optimización híbrida*

Search, Social y Commerce pueden cargar los objetivos de los portafolios de una cuenta de anunciante en [!DNL Google Ads] y [!DNL Microsoft® Advertising] para que pueda utilizarlos para la optimización híbrida. Los objetivos cargados están disponibles como acciones de conversión para los objetivos de conversión personalizados de nivel de cuenta y de campaña.

Al habilitar esta opción, se almacenarán automáticamente en déclencheur las cargas para los objetivos de los portafolios que contengan campañas con estrategias de oferta inteligente. Search, Social y Commerce crean una conversión en la red de anuncios para cada objetivo aplicable. La conversión representa todas las métricas de conversión ponderadas en el objetivo. Cada conversión tiene uno de los siguientes nombres:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  donde `<network_ID>` es el ID numérico que Search, Social y Commerce utilizan para la red de publicidad, `<objective_id>` es el ID de objetivo numérico, y `<network_account_ID>` es el identificador numérico de la cuenta de red de publicidad o de la cuenta de administrador.

* (Formato antiguo que quedará obsoleto en el futuro) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  donde `<portfolio_id>` es el ID de portafolio numérico y `<se_acctid/conversion_manager_se_acctid>` es el identificador numérico de la cuenta de red de publicidad o de la cuenta de administrador.

  El equipo de cuenta de Adobe trabajará con usted para migrar los nombres de acción de conversión existentes dentro de la red de publicidad antes de que el formato antiguo quede obsoleto. Durante el periodo de migración, las cargas de formato antiguo y nuevo se ejecutarán en paralelo. El modelado y la optimización no se ven afectados porque las nuevas acciones de conversión aparecerán inicialmente con estado &quot;secundario&quot; (no optimizado) y con 90 días de datos de relleno.

Cargas en [!DNL Google Ads] se producen diariamente a las 06:00 en el huso horario del anunciante. Cargas en [!DNL Microsoft® Advertising] se producen diariamente a las 09:00 en el huso horario del anunciante.

>[!IMPORTANT]
>
>Las conversiones rastreadas por Google Ads y por la etiqueta de seguimiento universal de eventos (UET) de Microsoft Advertising no se vuelven a cargar en las redes de anuncios. Si los incluye dentro de un objetivo, agréguelos a los objetivos de campaña dentro del editor de la red de publicidad.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleccione la casilla de verificación situada junto a **[!UICONTROL Enable Objective Upload]**.

1. (Anunciantes con [!DNL Google Ads] cuentas que realizan negocios en el Espacio Económico Europeo (EEE) o en el Reino Unido (Reino Unido); opcional) Si ha obtenido el consentimiento de los usuarios de EEE y del Reino Unido para cargar sus datos con fines publicitarios, active la casilla de verificación situada junto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clic **[!UICONTROL Save]**.

1. (Si las conversiones se rastrean en el nivel de cuenta de responsable) [Añadir credenciales para la cuenta de responsable](/help/search-social-commerce/admin/manager-accounts.md) en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

Una vez completada la carga diaria, puede verificar que las acciones de conversión aparezcan en la red de anuncios.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de las métricas de conversión de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Cargar métricas de conversión en [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
