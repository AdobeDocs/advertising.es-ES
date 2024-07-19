---
title: Por qué los datos de canal pueden variar entre el Adobe Advertising y  [!DNL Marketing Channels]
description: Descubra por qué los datos de canal rastreados por el ID de AMO pueden variar de los datos de canal rastreados por  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Por qué los datos de canal pueden variar entre el Adobe Advertising y [!DNL Marketing Channels]

*Solo anunciantes con una integración de Adobe Analytics de Adobe Advertising*

Una pregunta común de los usuarios que están aprendiendo acerca de la integración del Adobe Advertising y los conjuntos de datos de [!DNL Marketing Channels] es &quot;¿Qué causa la variación en los datos entre el ID de AMO y [!DNL Marketing Channels]?&quot; O, a veces, &quot;¿Por qué se rompen los datos? Necesito que todas las métricas coincidan en todos los informes&quot;. Afortunadamente, las discrepancias no indican que los datos estén &quot;rotos&quot;, y las discrepancias son esperadas e incluso deseadas. Veamos por qué la integración se diseñó de esta manera.

Los dos conjuntos de datos tienen diferentes casos de uso principales:

* [!DNL Marketing Channels]: el caso de uso principal de [!DNL Marketing Channels] es comparar datos de varios canales con un modelo de atribución común. Los analistas pueden usar la dimensión [!UICONTROL Marketing Channel] para obtener una mayor perspectiva de cómo los canales interactúan entre sí. Esta perspectiva puede ayudar a impulsar decisiones a nivel macro sobre cómo invertir en cada canal y puede dar lugar a perspectivas sobre cómo los visitantes de cada canal interactúan con el sitio web.

  Por lo tanto, la dimensión [!DNL Analytics] [!UICONTROL Marketing Channel] está configurada para capturar y rastrear todos los canales. [!DNL Marketing Channels] también se puede configurar para capturar las visualizaciones y pulsaciones de Advertising DSP, y lo hace en relación con los demás canales de marketing.

* ID de AMO de Adobe Advertising: el caso de uso principal de los datos de ID de AMO de Adobe Advertising es para alimentar los algoritmos de oferta avanzados de [!DNL Adobe Sensei]. Los algoritmos toman automáticamente miles de decisiones de oferta a nivel micro tomadas diariamente para maximizar el gasto en publicidad y lograr los objetivos de la campaña [!DNL DSP] o el portafolio [!DNL Search, Social, & Commerce]. Cuantos más datos de conversión tengan los algoritmos para conectar las campañas, mejores podrán ser las decisiones de oferta de los algoritmos.

  Para recopilar estos datos, la integración de [!DNL Analytics for Advertising] pasa los ID de AMO sin procesar que se pueden traducir como códigos de seguimiento de clics y visualizaciones en la dimensión de ID de AMO de Adobe Analytics, que se almacena como variable personalizada (eVar) o variable reservada (rVar). Las pulsaciones para otros canales no se establecen en la dimensión de ID de AMO, por lo que la dimensión de ID de AMO no puede rastrear la entrada desde estos otros canales. El resultado es que el ID de AMO persiste a través de [!DNL Marketing Channels] puntos de entrada.

Para obtener más información sobre posibles variaciones de datos entre los datos con seguimiento de Adobe Advertising y los datos con seguimiento de [!DNL Analytics], vea &quot;[Variaciones de datos previstas entre [!DNL Analytics] y el Adobe Advertising](../data-variances.md)&quot;.

>[!MORELIKETHIS]
>
>* [Variaciones de datos previstas entre [!DNL Analytics]  y el Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Usar ID de Adobe Advertising para crear [!DNL Marketing Channels] reglas de procesamiento](mc-ids.md)
>* [Usando [!DNL Analytics Marketing Channels] con datos de Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para informes de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
