---
title: Uso de [!DNL Marketing Channels] con datos publicitarios de Adobe
description: Aprenda a utilizar los datos de publicidad de Adobe en [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# Uso de [!DNL Analytics Marketing Channels] con datos publicitarios de Adobe

*Anunciantes con una integración de Adobe de Advertising-Adobe Analytics solamente*

Mediante publicidad de Adobe y [!DNL Analytics Marketing Channels] Con los informes de, puede obtener una valiosa perspectiva de cómo los medios digitales influyen en la actividad del sitio.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

La siguiente ilustración muestra cómo usar la publicidad de Adobe y [!DNL Marketing Channels] realizar un seguimiento de las visitas individuales que comprenden el recorrido de un visitante. Informes de publicidad de Adobe en [!DNL Analytics] se limitan únicamente a la publicidad de canal de comercio, social, de búsqueda y de visualización de pago que se transmite a través de Adobe Advertising mediante el ID de AMO. Sin embargo, [!DNL Marketing Channels] rastrea todos los canales configurados en la [!DNL Marketing Channels] Reglas de procesamiento.

![Cómo utilizar la publicidad de Adobe y [!DNL Marketing Channels] realizar un seguimiento de las visitas individuales en el recorrido de un visitante](/help/integrations/assets/a4adc-mc-sample-journey2.png)

En la primera visita, el usuario accedió al sitio web mediante una campaña de correo electrónico, ejecutó diez vistas de página y, a continuación, se marchó. En la segunda visita, el usuario accedió al sitio mediante un anuncio en pantalla, ejecutó diez vistas de página y, a continuación, se marchó. En la tercera visita, el usuario entró al sitio mediante una búsqueda natural, ejecutó cinco vistas de página, ejecutó una conversión de 250 $ y después se fue. Observe la diferencia en el seguimiento entre [!DNL Marketing Channels] y Publicidad de Adobe. El único canal que rastrea Adobe Advertising en este recorrido es [!UICONTROL Display]. Adobe Advertising realiza el seguimiento de [!UICONTROL Display] visitas al canal y atribuye los datos de participación subsiguientes (como vistas de página) y las conversiones a la influencia de ese anuncio. [!DNL Marketing Channels], por otro lado, ofrece una vista completa de todos los canales.

Dado que el ID de AMO persiste a través del recorrido del visitante, puede utilizar los datos de ID de AMO para ver cómo la publicidad de Adobe influye en otros canales de marketing. El ID de AMO [persiste durante 60 días de forma predeterminada](/help/integrations/analytics/overview.md), pero puede configurar la persistencia según sea necesario.

## Cómo combinar datos de canales de marketing y publicidad de Adobe para analizar el rendimiento de los medios

En [!DNL Analytics], puede combinar los datos de publicidad de pago persistentes de Adobe Advertising y la variable [!DNL Marketing Channels] datos de visitas completos para analizar mejor el rendimiento de los medios y así influir mejor en el recorrido del cliente.

El siguiente análisis utiliza los datos de publicidad de Adobe para mostrar diferentes versiones de cómo afecta un anuncio en pantalla a la conversión del sitio. Las tres columnas utilizan las mismas métricas de conversión, pero cada columna cuenta una historia diferente:

* La columna 1 observa los datos de ID de AMO que persisten en el recorrido del visitante. La columna 1 indica que 641 aplicaciones iniciadas se vincularon, en un momento dado, con un anuncio publicitario de Adobe, ya sea mediante un evento de visualización o de pulsación. Esta vista no toma ninguna otra [!DNL Marketing Channels] atribución en consideración.

* En el [!DNL Marketing Channels] Sin embargo, el conjunto de datos de 641 Inicios de aplicación se atribuye a otros canales de marketing. Las dos últimas columnas toman los 641 Inicios de aplicación y limitan los datos a [!UICONTROL Display Click-Through] y [!UICONTROL Display View-Through] canales, que muestran las conversiones que se producen en un modelo de atribución de último contacto.

![ejemplo de cómo afecta un anuncio en pantalla a la conversión del sitio](/help/integrations/assets/a4adc-mc-display-impact.png)

Puede llevar este análisis un paso más allá. Puede desglosar más la fila Publicidad de Adobe por canal de marketing para ver dónde se atribuyen las conversiones de Publicidad de Adobe a las 641 Aplicaciones iniciadas. Ya sabe que cinco de esas conversiones se atribuyen a un clic en una pantalla de último toque y 19 se atribuyen a una visualización de último toque. Eso aún deja 617 Inicios de aplicaciones atribuidos a otros canales de marketing. DSP Puede arrastrar y soltar la dimensión Canal del último contacto sobre el elemento de línea Advertising para mostrar la atribución de canal para el resto de los inicios de las aplicaciones y mostrar el impacto en canales múltiples del canal de visualización.

![Cómo añadir la dimensión Canal de último contacto](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Ahora puede ver cómo se atribuyen los inicios de aplicaciones restantes. El correo electrónico recibe crédito por 357 inicios de aplicaciones de último contacto para los que persistió un ID de AMO. Con este tipo de análisis, puede ver el impacto que los anuncios en pantalla de Adobe Advertising tuvieron en todos los canales. Con un solo conjunto de datos y un modelo de atribución, este tipo de perspectiva no estaría disponible.

![ejemplo del impacto en canales múltiples de los canales de visualización](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Puede mejorar aún más el análisis si utiliza un gráfico de pila establecido en Apilado al 100 % para mostrar los datos de tendencias a lo largo del tiempo. Esta visualización facilita la monitorización de qué canales de marketing de último contacto se ven más afectados por las campañas de marketing de visualización.

![ejemplo del impacto de tendencias en canales múltiples de los canales de visualización](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de ID de publicidad de Adobe para crear [!DNL Marketing Channels] Reglas de procesamiento](mc-ids.md)
>* [Por qué los datos de canal pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Vídeo: Uso de [!DNL Marketing Channels] para informes de publicidad de Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

