---
source-git-commit: c56a8caf8db4c76a41a96c48cbe3996078924cc6
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---
# ID de Adobe Advertising AMO

## ID de Adobe Advertising AMO {#amo-id}

El ID de AMO realiza un seguimiento de cada combinación de anuncios únicos en un nivel menos granular y se usa para la clasificación de datos de [!DNL Analytics] y Customer Journey Analytics y la ingesta de métricas de publicidad (como impresiones, clics y costes) de Adobe Advertising.

Para [!DNL Analytics], el ID de AMO se almacena en una dimensión [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o rVar (ID de AMO).

Para Customer Journey Analytics, el identificador de AMO se almacena en la propiedad `trackingCode` del objeto `conversionDetails`, que forma parte de [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

El identificador de AMO también se denomina `s_kwcid`, y en ocasiones se pronuncia como &quot;[!DNL squid]&quot;.
