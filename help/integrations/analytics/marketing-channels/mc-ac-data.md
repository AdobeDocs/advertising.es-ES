---
title: Usando [!DNL Marketing Channels] con datos de Adobe Advertising
description: Aprenda a utilizar los datos de Adobe Advertising en  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Usando [!DNL Analytics Marketing Channels] con datos de Adobe Advertising

*Solo anunciantes con una integración de Adobe Analytics de Adobe Advertising*

Si usa los informes Adobe Advertising y [!DNL Analytics Marketing Channels], obtendrá información valiosa sobre cómo los medios digitales influyen en la actividad del sitio.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

La siguiente ilustración muestra cómo el Adobe Advertising y [!DNL Marketing Channels] rastrean las visitas individuales que comprenden el recorrido de un visitante. Los informes de Adobe Advertising de [!DNL Analytics] se limitan únicamente a la publicidad de canal comercial, social, de búsqueda y de visualización de pago que se transmite a través del Adobe Advertising mediante el identificador de AMO. Sin embargo, [!DNL Marketing Channels] hace un seguimiento de todos los canales configurados en las reglas de procesamiento de [!DNL Marketing Channels].

![Cómo el Adobe Advertising y [!DNL Marketing Channels] rastrean las visitas individuales en el recorrido de un visitante](/help/integrations/assets/a4adc-mc-sample-journey2.png)

En la primera visita, el usuario accedió al sitio web mediante una campaña de correo electrónico, ejecutó diez vistas de página y, a continuación, se marchó. En la segunda visita, el usuario accedió al sitio mediante un anuncio en pantalla, ejecutó diez vistas de página y, a continuación, se marchó. En la tercera visita, el usuario entró al sitio mediante una búsqueda natural, ejecutó cinco vistas de página, ejecutó una conversión de 250 $ y después se fue. Observe la diferencia en el seguimiento entre [!DNL Marketing Channels] y el Adobe Advertising. El único canal que el Adobe Advertising rastrea en este recorrido es [!UICONTROL Display]. El Adobe Advertising hace un seguimiento de la visita al canal [!UICONTROL Display] y atribuye los datos de participación subsiguientes (como las vistas de página) y las conversiones al efecto de ese anuncio. [!DNL Marketing Channels], por otro lado, ofrece una vista completa de todos los canales.

Dado que el ID de AMO persiste a través del recorrido del visitante, puede utilizar los datos de ID de AMO para ver cómo el Adobe Advertising influye en otros canales de marketing. El identificador de AMO [persiste durante 60 días de forma predeterminada](/help/integrations/analytics/overview.md), pero puede configurar la persistencia según sea necesario.

## Cómo combinar datos de canales de Adobe Advertising y marketing para analizar el rendimiento de los medios

En [!DNL Analytics], puede combinar los datos de publicidad de pago persistente de Adobes Advertising con los datos de visita completa de [!DNL Marketing Channels] para analizar mejor el rendimiento de los medios y poder influir mejor en el recorrido del cliente.

El siguiente análisis utiliza los datos de Adobe Advertising para mostrar diferentes versiones de cómo afecta un anuncio de visualización a la conversión del sitio. Las tres columnas utilizan las mismas métricas de conversión, pero cada columna cuenta una historia diferente:

* La columna 1 observa los datos de ID de AMO que persisten en el recorrido del visitante. La columna 1 indica que 641 aplicaciones iniciadas se vincularon, en un momento dado, con un anuncio de Adobe Advertising, ya sea mediante un evento de visualización o de clic. Esta vista no tiene en cuenta ninguna otra atribución [!DNL Marketing Channels].

* Sin embargo, en el conjunto de datos [!DNL Marketing Channels], los inicios de 641 aplicaciones se atribuyen a otros canales de marketing. Las dos últimas columnas toman los 641 Inicios de aplicaciones y limitan los datos a los canales [!UICONTROL Display Click-Through] y [!UICONTROL Display View-Through], mostrando las conversiones que ocurren en un modelo de atribución de último contacto.

![ejemplo de cómo afecta un anuncio en pantalla a la conversión del sitio](/help/integrations/assets/a4adc-mc-display-impact.png)

Puede llevar este análisis un paso más allá. Puede desglosar más la fila de Adobes Advertising por canal de marketing para ver dónde se atribuyen las conversiones de Adobes Advertising a los inicios de aplicaciones 641. Ya sabe que cinco de esas conversiones se atribuyen a un clic en una pantalla de último toque y 19 se atribuyen a una visualización de último toque. Eso aún deja 617 Inicios de aplicaciones atribuidos a otros canales de marketing. Puede arrastrar y soltar la dimensión Canal del último contacto sobre el elemento de línea de Advertising DSP para mostrar la atribución de canal para el resto de los inicios de aplicaciones y mostrar el impacto en canales múltiples del canal de visualización.

![cómo agregar la dimensión Canal de último contacto](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Ahora puede ver cómo se atribuyen los inicios de aplicaciones restantes. El correo electrónico recibe crédito por 357 inicios de aplicaciones de último contacto para los que persistió un ID de AMO. Con este tipo de análisis, puede ver el impacto que los anuncios de visualización de Adobe Advertising tuvieron en todos los canales. Con un solo conjunto de datos y un modelo de atribución, este tipo de perspectiva no estaría disponible.

![ejemplo del impacto en canales múltiples de los canales de visualización](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Puede mejorar aún más el análisis si utiliza un gráfico de pila establecido en Apilado al 100 % para mostrar los datos de tendencias a lo largo del tiempo. Esta visualización facilita la monitorización de qué canales de marketing de último contacto se ven más afectados por las campañas de marketing de visualización.

![ejemplo del impacto de tendencias en canales múltiples de los canales de visualización](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Usar ID de Adobe Advertising para crear [!DNL Marketing Channels] reglas de procesamiento](mc-ids.md)
>* [Por qué los datos de canal pueden variar entre el Adobe Advertising y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para informes de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
