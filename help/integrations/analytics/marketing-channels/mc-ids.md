---
title: Uso de ID de publicidad de Adobe para crear [!DNL Marketing Channels] Reglas
description: Obtenga información sobre cómo utilizar los ID de Adobe Advertising para crear reglas de procesamiento para [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Uso de ID de publicidad de Adobe para crear [!DNL Marketing Channels] Reglas de procesamiento

*Anunciantes con una integración de Adobe de Advertising-Adobe Analytics solamente*

Puede utilizar los ID de Adobe Advertising ([ID de AMO e ID de EF](../ids.md)) para configurar [!DNL Marketing Channels] reglas de procesamiento en Adobe Analytics. Utilice los ID de publicidad de Adobe para reglas específicas de sus campañas de publicidad de Adobe.

## El ID de AMO en las reglas de procesamiento

El ID de AMO es el código de seguimiento principal que se utiliza para informar sobre los datos de Adobe Advertising en [!DNL Analytics]. El ID de AMO es una concatenación de valores dinámicos administrados por Adobe para proporcionar informes granulares dentro de [!DNL Analytics]. Se almacena en un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o la dimensión rVar (ID de AMO). El ID de AMO se puede configurar en [!DNL Analytics] de dos maneras:

* Seguimiento de clics: El Adobe Advertising establece el `s_kwcid` parámetro de cadena de consulta en un vínculo, y [!DNL Analytics] recoge el parámetro de la dirección URL de la página de aterrizaje cuando se produce una pulsación.
* Seguimiento de visualización ([!DNL DSP] Solo ): El servicio Último evento detecta una visualización en el servidor y envía el ID de AMO a [!DNL Analytics]. En este caso, la dirección URL no contiene un `s_kwcid` parámetro.

Los valores dinámicos dentro de los ID de AMO indican el canal de marketing que se rastreó:

* El prefijo del ID de AMO se puede utilizar para identificar el canal de nivel superior dentro de [!DNL Marketing Channels].

* Las frases de caracteres del cuerpo del ID de AMO indican un tipo de campaña más específico.

* El sufijo &quot;vt&quot; está presente para [!DNL DSP] tráfico de visualización, y se puede utilizar para crear clics y visualizaciones independientes [!DNL DSP] canales.

El resto del ID de AMO se puede ignorar.

| [!UICONTROL AMO ID] | Canal | Lógica de regla |
|--------|---------|--------------------|
| ¡AL! (prefijo) | [!UICONTROL Paid Search] | Comienza con |
| ¡AC! (prefijo) | [!UICONTROL DSP] | Comienza con |
| !g! (cuerpo) | [!UICONTROL Google Search] | Contains |
| !s! (cuerpo) | [!UICONTROL Search Partner] | Contains |
| !d! (cuerpo) | [!UICONTROL Display Network] | Contains |
| !u! (cuerpo) | [!UICONTROL Smart Shopping Campaign] | Contains |
| !ytv! (cuerpo) | [!UICONTROL YouTube Video Ad] | Contains |
| !yts! (cuerpo) | [!UICONTROL YouTube Search Ad] | Contains |
| !vp! (cuerpo) | [!UICONTROL Google Video Partners] | Contains |
| !vt (sufijo) | [!UICONTROL DSP View-through] | Finaliza con |

### Ejemplos de reglas de procesamiento que utilizan el ID de AMO

El [!DNL Marketing Channels] regla de procesamiento para [!UICONTROL Paid Search] el canal puede tener este aspecto:

![Ejemplo de un [!UICONTROL Paid Search] regla](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

El [!DNL Marketing Channels] regla de procesamiento para [!UICONTROL YouTube Video Ads] el canal puede tener este aspecto:

![Ejemplo de un [!UICONTROL YouTube Video Ads] regla](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Asegúrese de ejecutar las reglas en orden de especificación. Si las dos reglas anteriores se ejecutaron en orden, la variable [!DNL YouTube] el tráfico de anuncios de vídeo entraría dentro del [!UICONTROL Paid Search] porque el ID de AMO empezaría con &quot;AL!&quot; y contienen &quot;!ytv!&quot;.

## El EF ID en las reglas de procesamiento

El AMO EF ID (EF ID) es el segundo código de seguimiento utilizado en la variable [!DNL Analytics for Advertising] integración. Su propósito principal es rastrear y pasar [!DNL Analytics] datos de evento en el Adobe Advertising. Cada vez que se produce una pulsación o una visualización, se genera un ID de EF único, aunque sea el mismo anuncio para el mismo visitante. El EF ID no se utiliza en [!DNL Analytics] interfaz de usuario de informes porque suele superar los 500 000 valores únicos por límite de variable en [!DNL Analytics], inutilizándolo para la creación de informes. Las métricas y los metadatos de la publicidad de Adobe no se aplican al ID de EF; solo se aplican al ID de AMO. Se requiere la granularidad añadida del seguimiento para la optimización de campañas en la publicidad de Adobe, por lo que ambos ID son obligatorios.

Aunque la dimensión EF ID no se utiliza directamente en [!DNL Analytics] En los informes de, el ID de EF puede resultar útil para crear canales de marketing. El sufijo EF ID indica el canal (visualización o búsqueda) y si la visita se debió a un clic o a una visualización. El delimitador del ID de EF es un signo de dos puntos, en lugar del signo de exclamación del ID de AMO.

| Sufijo de ID de EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Ejemplos de reglas de procesamiento que utilizan el ID de EF

#### Mostrar regla de pulsaciones

Cree un canal de marketing de pulsaciones de visualización capturando solo las pulsaciones. Dado que el ID de AMO es el mismo para las pulsaciones y las visualizaciones, esta regla utiliza la variable EF ID y la variable `ef_id` parámetro de cadena de consulta.

A veces, el seguimiento de las pulsaciones se realiza a través de la dirección URL (la predeterminada). En otros casos, los clics se rastrean a través del Servicio de último evento del lado del servidor y, por lo tanto, la URL no contiene el `ef_id` parámetro. Por lo tanto, la regla comprueba las condiciones en las que la variable EF ID o la variable `ef_id` el parámetro de cadena de consulta termina con &quot;:d&quot;. Utilice el &quot;`Any`&quot; porque desea que esta regla se active para cualquiera de las condiciones.

![Ejemplo de una regla de pulsación en pantalla](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Mostrar regla de visualización

Para crear un canal de visualización, cree una regla en la que el EF ID termine con &quot;:i&quot;. Dado que el visitante no hizo clic en el anuncio, el seguimiento de visualización no incluye la variable `ef_id` o `s_kwcid` en la dirección URL, por lo que la regla solo requiere una condición.

![Ejemplo de una regla de visualización](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por qué los datos de canal pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Uso de [!DNL Analytics Marketing Channels] con datos publicitarios de Adobe](mc-ac-data.md)
>* [Vídeo: Uso de [!DNL Marketing Channels] para informes de publicidad de Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ID de publicidad de Adobe utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
