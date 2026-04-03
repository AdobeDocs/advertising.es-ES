---
title: Por qué los datos de canal pueden variar entre Adobe Advertising y  [!DNL Marketing Channels]
description: Descubra por qué los datos de canal rastreados por el ID de AMO pueden variar de los datos de canal rastreados por  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
TQID: https://experienceleague.adobe.com/zzYKrbiwvW9Ysf7baDfKGsETmSvYbXDY7-lIygorXH8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: dba482e5-29a8-4127-afa2-c4b913512ef8id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 0%

---

# Por qué los datos de canal pueden variar entre Adobe Advertising y [!DNL Marketing Channels]

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

Una pregunta común de los usuarios que están aprendiendo acerca de la integración de los conjuntos de datos de Adobe Advertising y [!DNL Marketing Channels] es &quot;¿Qué causa la variación en los datos entre el ID de AMO y [!DNL Marketing Channels]?&quot; O, a veces, &quot;¿Por qué se rompen los datos? Necesito que todas las métricas coincidan en todos los informes&quot;. Afortunadamente, las discrepancias no indican que los datos estén &quot;rotos&quot;, y las discrepancias son esperadas e incluso deseadas. Veamos por qué la integración se diseñó de esta manera.

Los dos conjuntos de datos tienen diferentes casos de uso principales:

* [!DNL Marketing Channels]: el caso de uso principal de [!DNL Marketing Channels] es comparar datos de varios canales con un modelo de atribución común. Los analistas pueden usar la dimensión [!UICONTROL Marketing Channel] para obtener una mayor perspectiva de cómo los canales interactúan entre sí. Esta insight puede ayudar a impulsar las decisiones a nivel macro sobre cómo invertir en cada canal y puede dar lugar a perspectivas sobre cómo los visitantes de cada canal interactúan con el sitio web.

  Por lo tanto, la dimensión [!DNL Analytics] [!UICONTROL Marketing Channel] está configurada para capturar y rastrear todos los canales. [!DNL Marketing Channels] también se puede configurar para capturar las visualizaciones y pulsaciones de Advertising DSP, y lo hace en relación con los demás canales de marketing.

* ID de Adobe Advertising AMO: El caso de uso principal de los datos de ID de Adobe Advertising AMO es para alimentar los algoritmos de oferta avanzados con tecnología [!DNL Adobe AI]. Los algoritmos toman automáticamente miles de decisiones de oferta a nivel micro tomadas diariamente para maximizar el gasto en publicidad y lograr los objetivos de la campaña [!DNL DSP] o el portafolio [!DNL Search, Social, & Commerce]. Cuantos más datos de conversión tengan los algoritmos para conectar las campañas, mejores podrán ser las decisiones de oferta de los algoritmos.

  Para recopilar estos datos, la integración de [!DNL Analytics for Advertising] pasa los ID de AMO sin procesar que se pueden traducir como códigos de seguimiento de clics y visualizaciones en la dimensión de ID de AMO de Adobe Analytics, que se almacena como variable personalizada (eVar) o variable reservada (rVar). Las pulsaciones para otros canales no se establecen en la dimensión de ID de AMO, por lo que la dimensión de ID de AMO no puede rastrear la entrada desde estos otros canales. El resultado es que el ID de AMO persiste a través de [!DNL Marketing Channels] puntos de entrada.

Para obtener más información sobre posibles variaciones de datos entre los datos rastreados por Adobe Advertising y los datos rastreados por [!DNL Analytics], consulte &quot;[Variaciones de datos previstas entre [!DNL Analytics] y Adobe Advertising](../data-variances.md)&quot;.

>[!MORELIKETHIS]
>
>* [Variaciones de datos previstas entre [!DNL Analytics]  y Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de Adobe Advertising ID para crear [!DNL Marketing Channels] reglas de procesamiento](mc-ids.md)
>* [Usando [!DNL Analytics Marketing Channels] con datos de Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para los informes de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
