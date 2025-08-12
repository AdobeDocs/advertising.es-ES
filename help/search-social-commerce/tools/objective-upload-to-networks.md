---
title: Habilitar la carga de objetivos en las redes de publicidad
description: Aprenda a cargar los objetivos de sus portafolios híbridos en  [!DNL Google Ads] y [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 3d3031946bb614f2c58b83170473b1394e4a017c
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Habilitar la carga de objetivos en las redes de publicidad

*Anunciantes con [!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas solamente*

*Solo anunciantes habilitados para la optimización híbrida*

Search, Social y Commerce pueden cargar los objetivos de los portafolios de una cuenta de anunciante en [!DNL Google Ads] y [!DNL Microsoft Advertising] para que pueda utilizarlos en la optimización híbrida. Los objetivos cargados están disponibles como acciones de conversión para los objetivos de conversión personalizados de nivel de cuenta y de campaña.

Al habilitar esta opción, se almacenarán automáticamente en déclencheur las cargas para los objetivos de los portafolios que contengan campañas con estrategias de oferta inteligente. Search, Social y Commerce crean una conversión en la red de anuncios para cada objetivo aplicable. La conversión representa todas las métricas de conversión ponderadas en el objetivo a nivel de EF ID (ID de clic). Para [!DNL Google Ads] clics, el identificador EF es [!DNL Google Ads] `gclid`; para [!DNL Microsoft Advertising] clics, el identificador EF es [!DNL Microsoft Advertising] `msclkid`. Debido a este ID de clic, los datos de conversión se pueden asignar a la palabra clave específica y a la hora del clic.

Cada conversión cargada tiene el siguiente nombre:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

donde `<network_ID>` es el identificador numérico que Search, Social y Commerce usa para la red de anuncios, `<objective_id>` es el identificador de objetivo numérico y `<network_account_ID>` es el identificador numérico para la cuenta de administrador o la cuenta de red de anuncios.

Las cargas a [!DNL Google Ads] y [!DNL Microsoft Advertising] se producen a lo largo del día, a veces incluso cada hora. Para anunciantes con cuentas grandes o configuraciones personalizadas, las cargas se realizan al menos tres veces al día.

>[!IMPORTANT]
>
>Las conversiones rastreadas por Google Ads y por la etiqueta de seguimiento universal de eventos (UET) de Microsoft Advertising no se vuelven a cargar en las redes de anuncios. Si los incluye dentro de un objetivo, debe agregarlos a los objetivos de campaña dentro del editor de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Active la casilla de verificación situada junto a **[!UICONTROL Enable Objective Upload]**.

1. (Anunciantes con cuentas de [!DNL Google Ads] que realizan negocios en el Espacio Económico Europeo (EEE) o en el Reino Unido (Reino Unido); opcional) Si ha recopilado el consentimiento de usuarios de EEE y Reino Unido para cargar sus datos con fines publicitarios, active la casilla de verificación situada junto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Haga clic en **[!UICONTROL Save]**.

1. (Si las conversiones se rastrean en el nivel de cuenta de administrador) [Agregue credenciales para la cuenta de administrador](/help/search-social-commerce/admin/manager-accounts.md) en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Compruebe que cada objetivo (denominado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`) aparece en un plazo de dos días en la red publicitaria.

   En el editor [!DNL Google Ads], busque sus [acciones de conversión](https://support.google.com/google-ads/answer/11461796). En el editor [!DNL Microsoft Advertising], busque sus [metas de conversión](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Si es necesario, actualice el intervalo de fechas para incluir la fecha de carga.

## Cálculo del objetivo ponderado

El objetivo ponderado que se pasa a la red de anuncios es la suma de todos los valores de métricas recopilados, con la excepción de las conversiones rastreadas por [!DNL Google Ads] o por la etiqueta de seguimiento universal de eventos (UET) [!DNL Microsoft Advertising]. El valor se calcula mediante el método de atribución configurado para la cuenta de Search, Social y Commerce del anunciante.

Por ejemplo, supongamos que la métrica de objetivos del objetivo es Adiciones al carro de compras con un peso de 25, y las métricas de asistencia incluyen GGL_Lead e Ingresos con pesos de 1 y Descargas con un peso de 0,5.

![Ejemplo de objetivo ponderado](/help/search-social-commerce/assets/objective-example.png "Ejemplo de objetivo ponderado")

Supongamos que una palabra clave resultara en las siguientes acciones para el portafolio:

* 10 Adiciones al carro
* 500 $ en ingresos
* 50 descargas
* 5 GGL_Lead

GGL_Lead no se incluye en el cálculo/carga porque es una métrica rastreada en Google Ads. Por lo tanto, el valor objetivo ponderado se calcula como ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>Puede ver datos de los ingresos ponderados por Adobe Advertising en los informes de la red de publicidad. Se recomienda comparar los ingresos ponderados con los [!DNL Google Ads] &quot;Todos los convertidores. (por conversión. hora)&quot; o la métrica [!DNL Microsoft Advertising] &quot;Todas las conversiones&quot;. ingresos&quot;, segmentado a la métrica O_ACS_OBJ*.<!--clarify -->

## Solución de problemas de objetivos perdidos

Si el objetivo, denominado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`, de uno de sus portafolios no aparece en la red de anuncios, compruebe lo siguiente:

* ([!DNL Google Ads]) Compruebe si las conversiones deben cargarse en el nivel de cuenta o administrador. Si deben cargarse en el nivel de responsable:

   * Compruebe si las credenciales de la cuenta de administrador de [!DNL Google Ads] se proporcionan en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Si es necesario, [agregue las credenciales para la cuenta de administrador](/help/search-social-commerce/admin/manager-accounts.md).

   * Compruebe si la cuenta de red de publicidad ya incluye el mismo nombre de métrica. Si es así, cambie el nombre de la métrica para que se pueda crear la propiedad correcta en el nivel de administrador.

* Compruebe que la opción &quot;híbrida&quot; del portafolio esté seleccionada y que el objetivo tenga ingresos válidos.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de las métricas de conversión de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Cargar métricas de conversión de búsqueda, medios sociales y seguimiento de Commerce a [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
