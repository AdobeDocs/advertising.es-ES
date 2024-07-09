---
title: Habilitar la carga de objetivos en las redes de publicidad
description: Obtenga información sobre cómo cargar objetivos para sus portafolios híbridos en [!DNL Google Ads] y [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 39936c6834012432447d3216d8463937996b0017
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Habilitar la carga de objetivos en las redes de publicidad

*Anunciantes con [!DNL Google Ads] y [!DNL Microsoft Advertising] solo cuentas*

*Anunciantes habilitados solo para la optimización híbrida*

Search, Social y Commerce pueden cargar los objetivos de los portafolios de una cuenta de anunciante en [!DNL Google Ads] y [!DNL Microsoft Advertising] para que pueda utilizarlos para la optimización híbrida. Los objetivos cargados están disponibles como acciones de conversión para los objetivos de conversión personalizados de nivel de cuenta y de campaña.

Al habilitar esta opción, se almacenarán automáticamente en déclencheur las cargas para los objetivos de los portafolios que contengan campañas con estrategias de oferta inteligente. Search, Social y Commerce crean una conversión en la red de anuncios para cada objetivo aplicable. La conversión representa todas las métricas de conversión ponderadas en el objetivo a nivel de EF ID (ID de clic). Para [!DNL Google Ads] clics, el ID de EF es el [!DNL Google Ads] `gclid`; para [!DNL Microsoft Advertising] clics, el ID de EF es el [!DNL Microsoft Advertising] `msclkid`. Debido a este ID de clic, los datos de conversión se pueden asignar a la palabra clave específica y a la hora del clic.

Cada conversión cargada tiene uno de los siguientes nombres:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  donde `<network_ID>` es el ID numérico que Search, Social y Commerce utilizan para la red de publicidad, `<objective_id>` es el ID de objetivo numérico, y `<network_account_ID>` es el identificador numérico de la cuenta de red de publicidad o de la cuenta de administrador.

* (Formato antiguo que quedará obsoleto en el futuro) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  donde `<portfolio_id>` es el ID de portafolio numérico y `<se_acctid/conversion_manager_se_acctid>` es el identificador numérico de la cuenta de red de publicidad o de la cuenta de administrador.

  El equipo de cuenta de Adobe trabajará con usted para migrar los nombres de acción de conversión existentes dentro de la red de publicidad antes de que el formato antiguo quede obsoleto. Durante el periodo de migración, las cargas de formato antiguo y nuevo se ejecutarán en paralelo. El modelado y la optimización no se ven afectados porque las nuevas acciones de conversión aparecen inicialmente con estado &quot;secundario&quot; (no optimizado) y con 90 días de datos de relleno.

Cargas en [!DNL Google Ads] se producen diariamente a las 06:00 en el huso horario del anunciante. Cargas en [!DNL Microsoft Advertising] se producen diariamente a las 09:00 en el huso horario del anunciante.

>[!IMPORTANT]
>
>Las conversiones rastreadas por Google Ads y por la etiqueta de seguimiento universal de eventos (UET) de Microsoft Advertising no se vuelven a cargar en las redes de anuncios. Si los incluye dentro de un objetivo, debe agregarlos a los objetivos de campaña dentro del editor de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleccione la casilla de verificación situada junto a **[!UICONTROL Enable Objective Upload]**.

1. (Anunciantes con [!DNL Google Ads] cuentas que realizan negocios en el Espacio Económico Europeo (EEE) o en el Reino Unido (Reino Unido); opcional) Si ha obtenido el consentimiento de los usuarios de EEE y del Reino Unido para cargar sus datos con fines publicitarios, active la casilla de verificación situada junto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clic **[!UICONTROL Save]**.

1. (Si las conversiones se rastrean en el nivel de cuenta de responsable) [Añadir credenciales para la cuenta de responsable](/help/search-social-commerce/admin/manager-accounts.md) en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Verificar que cada objetivo (denominado) `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — aparece en un plazo de dos días en la red de anuncios.

   En el [!DNL Google Ads] editor, busque su [acciones de conversión](https://support.google.com/google-ads/answer/11461796). En el [!DNL Microsoft Advertising] editor, busque su [objetivos de conversión](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Si es necesario, actualice el intervalo de fechas para incluir la fecha de carga.

## Cálculo del objetivo ponderado

El objetivo ponderado que se pasa a la red de anuncios es la suma de todos los valores de métricas recopilados, con la excepción de las conversiones rastreadas por [!DNL Google Ads] o por el [!DNL Microsoft Advertising] etiqueta universal event tracking (UET).

Por ejemplo, supongamos que la métrica de objetivos del objetivo es Adiciones al carro de compras con un peso de 25, y las métricas de asistencia incluyen GGL_Lead e Ingresos con pesos de 1 y Descargas con un peso de 0,5.

![Ejemplo de objetivo ponderado](/help/search-social-commerce/assets/objective-example.png "Ejemplo de objetivo ponderado")

Supongamos que una palabra clave resultara en las siguientes acciones para el portafolio:

* 10 Adiciones al carro
* 500 $ en ingresos
* 50 descargas
* 5 GGL_Lead

GGL_Lead no se incluye en el cálculo/carga porque es una métrica rastreada en Google Ads. Por lo tanto, el valor objetivo ponderado se calcula como ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

## Solución de problemas de objetivos perdidos

Si el objetivo — denominado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — si uno de sus portafolios no aparece en la red de anuncios, compruebe lo siguiente:

* ([!DNL Google Ads]) Compruebe si las conversiones deben cargarse en el nivel de cuenta o administrador. Si deben cargarse en el nivel de responsable:

   * Compruebe si las credenciales de la [!DNL Google Ads] la cuenta del responsable se proporciona en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Si es necesario, [añadir las credenciales de la cuenta de responsable](/help/search-social-commerce/admin/manager-accounts.md).

   * Compruebe si la cuenta de red de publicidad ya incluye el mismo nombre de métrica. Si es así, cambie el nombre de la métrica para que se pueda crear la propiedad correcta en el nivel de administrador.

* Compruebe que la opción &quot;híbrida&quot; del portafolio esté seleccionada y que el objetivo tenga ingresos válidos.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de las métricas de conversión de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Cargar métricas de conversión en [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
