---
title: (Nueva IU) Habilitar la carga de objetivos en las redes de publicidad
description: Obtenga información sobre cómo cargar objetivos para sus portafolios híbridos en Google Ads y Microsoft Advertising.
feature: Search Objectives, Search Optimization
hide: true
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%

---

# (Nueva IU) Habilitar la carga de objetivos en las redes de publicidad

*característica de Beta*

*Anunciantes con [!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas solamente*

*Solo anunciantes habilitados para la optimización híbrida*

Search, Social y Commerce pueden cargar los objetivos de los portafolios de una cuenta de anunciante en [!DNL Google Ads] y [!DNL Microsoft Advertising] para que pueda utilizarlos en la optimización híbrida. Los objetivos cargados están disponibles como acciones de conversión para los objetivos de conversión personalizados de nivel de cuenta y de campaña.

Al habilitar esta opción, se almacenarán automáticamente en déclencheur las cargas para los objetivos de los portafolios que contengan campañas con estrategias de oferta inteligente. Search, Social y Commerce crean una conversión en la red de anuncios para cada objetivo aplicable. La conversión representa todas las métricas de conversión ponderadas en el objetivo a nivel de EF ID (ID de clic). Para [!DNL Google Ads] clics, el identificador EF es [!DNL Google Ads] `gclid`; para [!DNL Microsoft Advertising] clics, el identificador EF es [!DNL Microsoft Advertising] `msclkid`. Debido a este ID de clic, los datos de conversión se pueden asignar a la palabra clave específica y a la hora del clic.

Cada conversión cargada tiene el siguiente nombre:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

donde `<network_ID>` es el identificador numérico que Search, Social y Commerce usa para la red de anuncios, `<objective_ID>` es el identificador de objetivo numérico y `<network_account_ID>` es el identificador numérico para la cuenta de administrador o la cuenta de red de anuncios.

Las cargas a [!DNL Google Ads] y [!DNL Microsoft Advertising] se producen a lo largo del día, generalmente por hora. Para anunciantes con cuentas grandes o configuraciones personalizadas, las cargas se realizan al menos tres veces al día.

>[!IMPORTANT]
>
>Las conversiones rastreadas por [!DNL Google Ads] y por la etiqueta de seguimiento universal de eventos (UET) [!DNL Microsoft Advertising] no se vuelven a cargar en las redes de anuncios. Si los incluye dentro de un objetivo, debe agregarlos a los objetivos de campaña dentro del editor de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Goals]** > **[!UICONTROL Objectives]**.

1. En la barra de herramientas, haga clic en **[!UICONTROL Upload Objective]**.

1. En el cuadro de diálogo [!UICONTROL Objective Upload Setup], establezca la opción **[!UICONTROL Enable Objective Upload]** en **[!UICONTROL On]**.

1. (Anunciantes con cuentas de [!DNL Google Ads] que hacen negocios en el Espacio Económico Europeo (EEE) o en el Reino Unido (Reino Unido); opcional) Si ha recopilado el consentimiento de los usuarios de EEE y Reino Unido para cargar sus datos con fines publicitarios, active la casilla de verificación para confirmar que se ha recopilado el consentimiento del usuario de EEE/Reino Unido. Esto envía el estado de consentimiento como **[!UICONTROL GRANTED]** a [!DNL Google Ads] y [!DNL Microsoft Advertising]. Si no se selecciona, el estado de consentimiento se envía como **[!UICONTROL UNSPECIFIED]**.

1. (Si se hace un seguimiento de las conversiones en el nivel de cuenta de administrador) [Agregue credenciales para la cuenta de administrador](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md) antes de guardar.

1. Haga clic en **[!UICONTROL Save]**.

1. Compruebe que cada objetivo (denominado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`) aparece en un plazo de dos días en la red publicitaria.

   En el editor [!DNL Google Ads], busque sus [acciones de conversión](https://support.google.com/google-ads/answer/11461796){target="_blank"}. En el editor [!DNL Microsoft Advertising], busque sus [metas de conversión](https://help.ads.microsoft.com/#apex/ads/en/56709){target="_blank"}.

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
>Puede ver datos de los ingresos ponderados por Adobe Advertising en los informes de la red de publicidad. Se recomienda comparar los ingresos ponderados con los [!DNL Google Ads] &quot;Todos los convertidores. (por conversión. hora)&quot; o la métrica [!DNL Microsoft Advertising] &quot;Todas las conversiones&quot;. ingresos&quot;, segmentado con la métrica O_ACS_OBJ*.

## Solución de problemas de objetivos perdidos

Si el objetivo, denominado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`, de uno de sus portafolios no aparece en la red de anuncios, compruebe lo siguiente:

* ([!DNL Google Ads]) Compruebe si las conversiones deben cargarse en el nivel de cuenta o administrador. Si deben cargarse en el nivel de responsable:

   * Compruebe si se han proporcionado las credenciales de la cuenta de administrador de [!DNL Google Ads]. Si es necesario, [agregue las credenciales para la cuenta de administrador](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md).

   * Compruebe si la cuenta de red de publicidad ya incluye el mismo nombre de métrica. Si es así, cambie el nombre de la métrica para que se pueda crear la propiedad correcta en el nivel de administrador.

* Compruebe que la opción &quot;híbrida&quot; del portafolio esté seleccionada y que el objetivo tenga ingresos válidos.

>[!MORELIKETHIS]
>
>* [Acerca de los objetivos](objective-about.md)
>* [Administrar y ver datos de rendimiento de las métricas de conversión de un anunciante](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)
>* [Administrar credenciales para [!DNL Google Ads] cuentas de gerente](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
