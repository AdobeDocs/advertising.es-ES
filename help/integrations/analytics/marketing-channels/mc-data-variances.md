---
title: Por qué los datos de canal pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]
description: Descubra por qué los datos de canal rastreados por el ID de AMO pueden variar de los datos de canal rastreados por [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Por qué los datos de canal pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]

*Anunciantes con una integración de Adobe de Advertising-Adobe Analytics solamente*

Una pregunta habitual de los usuarios que están aprendiendo a integrar el Adobe Publicidad y [!DNL Marketing Channels] Conjuntos de datos de es &quot;Qué causa la variación de datos entre el ID de AMO y [!DNL Marketing Channels]?&quot; O, a veces, &quot;¿Por qué se rompen los datos? Necesito que todas las métricas coincidan en todos los informes&quot;. Afortunadamente, las discrepancias no indican que los datos estén &quot;rotos&quot;, y las discrepancias son esperadas e incluso deseadas. Veamos por qué la integración se diseñó de esta manera.

Los dos conjuntos de datos tienen diferentes casos de uso principales:

* [!DNL Marketing Channels]: el caso de uso principal para [!DNL Marketing Channels] es comparar datos de varios canales con un modelo de atribución común. Los analistas pueden usar el [!UICONTROL Marketing Channel] para obtener una mayor perspectiva de cómo los canales interactúan entre sí. Esta perspectiva puede ayudar a impulsar decisiones a nivel macro sobre cómo invertir en cada canal y puede dar lugar a perspectivas sobre cómo los visitantes de cada canal interactúan con el sitio web.

   El [!DNL Analytics] [!UICONTROL Marketing Channel] por lo tanto, la dimensión está configurada para capturar y rastrear todos los canales. [!DNL Marketing Channels] DSP También se puede configurar para que capture las visualizaciones y los clics de Advertising, y lo hace en relación con los demás canales de marketing.

* ID de AMO de publicidad de Adobe: el caso de uso principal de los datos de ID de AMO de publicidad de Adobe es para alimentar el [!DNL Adobe Sensei]Algoritmos de oferta basados en. Los algoritmos toman automáticamente miles de decisiones de oferta a nivel micro tomadas diariamente para maximizar el gasto en publicidad y lograr los objetivos de la [!DNL DSP] campaign o la [!DNL Search, Social, & Commerce] portafolio. Cuantos más datos de conversión tengan los algoritmos para conectar las campañas, mejores podrán ser las decisiones de oferta de los algoritmos.

   Para recopilar estos datos, la variable [!DNL Analytics for Advertising] La integración pasa los ID de AMO sin procesar que se pueden traducir como códigos de seguimiento de clics y visualizaciones en la dimensión de ID de AMO de Adobe Analytics, que se almacena como variable personalizada (eVar) o reservada (rVar). Las pulsaciones para otros canales no se establecen en la dimensión de ID de AMO, por lo que la dimensión de ID de AMO no puede rastrear la entrada desde estos otros canales. El resultado es que el ID de AMO persiste durante [!DNL Marketing Channels] puntos de entrada.

Para obtener más información sobre posibles variaciones de datos entre los datos de seguimiento de publicidad de Adobe y [!DNL Analytics]Datos de seguimiento automático, consulte &quot;[Variaciones de datos previstas entre [!DNL Analytics] Publicidad de Adobe y](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Variaciones de datos previstas entre [!DNL Analytics] Publicidad de Adobe y](/help/integrations/analytics/data-variances.md)
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de ID de publicidad de Adobe para crear [!DNL Marketing Channels] Reglas de procesamiento](mc-ids.md)
>* [Uso de [!DNL Analytics Marketing Channels] con datos publicitarios de Adobe](mc-ac-data.md)
>* [Vídeo: Uso de [!DNL Marketing Channels] para informes de publicidad de Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)

