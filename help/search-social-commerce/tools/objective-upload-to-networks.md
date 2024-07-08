---
title: Permitir la carga de objetivos en redes de anuncios
description: Aprenda a cargar objetivos para sus portafolios híbridos a [!DNL Google Ads] y [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Permitir la carga de objetivos en redes de anuncios

*Anunciantes con [!DNL Google Ads] y [!DNL Microsoft Advertising] solo cuentas*

*Anunciantes habilitados solo para la optimización híbrida*

Search, Social &amp; Commerce puede cargar los objetivos de las carteras de un anunciante cuenta y [!DNL Google Ads] [!DNL Microsoft Advertising] , por lo tanto, puede usarlos para la optimización híbrida. Los objetivos cargados se muestran como acciones de Conversión para los objetivos de Conversión personalizados de cuenta y campaña niveles.

Al habilitar esta opción, se activa automáticamente una cargar para objetivos en portafolios que contienen campañas con estrategias de oferta inteligente. Search, Social y Comercio crea un Conversión sobre el red de anuncios para cada objetivo aplicable. El Conversión representa todas las métricas Conversión ponderadas del objetivo. Cada Conversión tiene uno de los siguientes nombres:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  donde `<network_ID>` es el ID numérica que Search, Social &amp; Commerce utiliza para el red de anuncios, `<objective_id>` es el ID objetivo numérica y `<network_account_ID>` es el ID numérica para el red de anuncios cuenta o administrador cuenta.

* (formato antiguas que quedarán obsoletas en el futuro) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  donde `<portfolio_id>` es el ID de numérica catálogo de productos y `<se_acctid/conversion_manager_se_acctid>` es el ID de numérica para el cuenta red de anuncios cuenta o administrador.

  El equipo de Adobe Systems cuenta trabajará con usted para migrar los nombres de acción de Conversión existentes dentro de la red de anuncios antes de que el formato antiguo quede obsoleto. Durante el período de migración, tanto la carga de formato antigua como la nueva se ejecutarán en paralelo. El modelado y la optimización no se ven afectados porque las nuevas acciones de Conversión aparecen inicialmente con estado &quot;secundario&quot; (no optimizado) y con 90 días de datos relleno.

Las cargas se [!DNL Google Ads] producirán diariamente a las 06:00 en la zona horaria del anunciante. Las cargas se [!DNL Microsoft Advertising] producirán diariamente a las 09:00 en la zona horaria del anunciante.

>[!IMPORTANT]
>
>Las conversiones rastreadas por Google Ads y por el etiqueta de evento seguimiento universal (UET) de Microsoft Advertising no se vuelven a cargar en las redes anuncios. Si los incluyes dentro de un objetivo, agrégalos a los objetivos campaña dentro del editor del red de anuncios.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleccione la casilla de verificación situada junto a **[!UICONTROL Enable Objective Upload]**.

1. (Anunciantes con [!DNL Google Ads] cuentas que hacen negocios en el Espacio Económico Europeo (EEA) o Reino Unido (UK); opcional) Si has recopilado el consentimiento de usuarios de EEA y del Reino Unido para cargar sus datos con fines publicitarios, selecciona la casilla situada junto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Haga clic en **[!UICONTROL Save]**.

1. (Si se realiza un seguimiento de las conversiones a nivel de administrador cuenta de administración) [añadir credenciales de su cuenta](/help/search-social-commerce/admin/manager-accounts.md) de administrador en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Verifique que cada objetivo, nombrado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` , aparezca dentro de los dos días del red de anuncios.

   [!DNL Google Ads] Al editor, busque sus [Conversión acciones](https://support.google.com/google-ads/answer/11461796). [!DNL Microsoft Advertising] Al editor, busca tus [metas](https://help.ads.microsoft.com/#apex/ads/en/56709) Conversión.

   Si es necesario, actualice el intervalo de fecha para incluir la fecha cargar.

## Resolución de problemas de objetivos faltantes

Si el objetivo, nombrado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` , para uno de sus portafolios no aparece en la red de anuncios, verifique lo siguiente:

* ([!DNL Google Ads]) Compruebe si las conversiones deben cargarse a nivel cuenta o de administrador. Si deben cargarse a nivel de administrador:

   * Compruebe si las credenciales para el [!DNL Google Ads] cuenta de administrador se proporcionan en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Si es necesario, [agregue las credenciales para el administrador cuenta](/help/search-social-commerce/admin/manager-accounts.md).

   * Compruebe si el red de anuncios cuenta ya incluye el mismo nombre Métrica. Si es así, cambie el nombre de la Métrica para que se puedan crear los Propiedad correctos a nivel de administrador.

* Compruebe que la opción &quot;híbrida&quot; del catálogo de productos esté seleccionada y que el objetivo tenga ingresos válidos.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de las métricas de Conversión de una anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Cargar métricas de Conversión en [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
