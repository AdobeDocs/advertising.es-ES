---
title: Usar los identificadores de Adobe Advertising para crear  [!DNL Marketing Channels] reglas
description: Obtenga información sobre cómo usar los identificadores de Adobe Advertising para crear reglas de procesamiento para  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Usar los identificadores de Adobe Advertising para crear [!DNL Marketing Channels] reglas de procesamiento

*Solo anunciantes con una integración de Adobe Analytics de Adobe Advertising*

Puede usar los identificadores de Adobe Advertising ([AMO ID y EF ID](../ids.md)) para configurar [!DNL Marketing Channels] reglas de procesamiento en Adobe Analytics. Utilice ID de Adobe Advertising para reglas específicas de sus campañas de Adobe Advertising.

## El ID de AMO en las reglas de procesamiento

El identificador de AMO es el código de seguimiento principal que se usa para informar sobre los datos de Adobe Advertising en [!DNL Analytics]. El ID de AMO es una concatenación de valores dinámicos administrados por el Adobe para proporcionar informes granulares en [!DNL Analytics]. Se almacena en una dimensión [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o rVar (ID de AMO). El identificador de AMO se puede establecer en [!DNL Analytics] de dos maneras:

* Seguimiento de clics: el Adobe Advertising establece el parámetro de cadena de consulta `s_kwcid` en un vínculo y [!DNL Analytics] recoge el parámetro de la dirección URL de la página de aterrizaje cuando se produce una pulsación.
* Seguimiento de visualización ([!DNL DSP] solamente): El servicio Último evento detecta una visualización en el servidor y envía el identificador de AMO a [!DNL Analytics]. En este caso, la dirección URL no contiene un parámetro `s_kwcid`.

Los valores dinámicos dentro de los ID de AMO indican el canal de marketing que se rastreó:

* El prefijo del identificador de AMO se puede usar para identificar el canal de nivel superior dentro de [!DNL Marketing Channels].

* Las frases de caracteres del cuerpo del ID de AMO indican un tipo de campaña más específico.

* El sufijo &quot;vt&quot; está presente para el tráfico de visualización de [!DNL DSP] y se puede usar para crear canales de visualización y clics independientes de [!DNL DSP].

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

La regla de procesamiento [!DNL Marketing Channels] para el canal [!UICONTROL Paid Search] puede tener este aspecto:

![Ejemplo de regla [!UICONTROL Paid Search]](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

La regla de procesamiento [!DNL Marketing Channels] para el canal [!UICONTROL YouTube Video Ads] puede tener este aspecto:

![Ejemplo de regla [!UICONTROL YouTube Video Ads]](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Asegúrese de ejecutar las reglas en orden de especificación. Si las dos reglas anteriores se ejecutaran en orden, el tráfico de anuncios de vídeo [!DNL YouTube] entraría dentro del canal [!UICONTROL Paid Search] porque el ID de AMO empezaría con &quot;AL!&quot; y contienen &quot;!ytv!&quot;.

## El EF ID en las reglas de procesamiento

El AMO EF ID (EF ID) es el segundo código de seguimiento utilizado en la integración de [!DNL Analytics for Advertising]. Su propósito principal es rastrear y pasar datos de evento [!DNL Analytics] al Adobe Advertising. Cada vez que se produce una pulsación o una visualización, se genera un ID de EF único, aunque sea el mismo anuncio para el mismo visitante. El identificador de EF no se usa en la interfaz de usuario de creación de informes [!DNL Analytics] porque, por lo general, supera el límite de 500.000 valores únicos por variable en [!DNL Analytics], por lo que no se puede utilizar para la creación de informes. Las métricas de Adobe Advertising y los metadatos no se aplican al ID de EF; solo se aplican al ID de AMO. Se requiere la granularidad añadida del seguimiento para la optimización de campañas en Adobe Advertising, por lo que ambos ID son obligatorios.

Aunque la dimensión de ID de EF no se usa directamente en los informes de [!DNL Analytics], el ID de EF puede resultar útil para crear canales de marketing. El sufijo EF ID indica el canal (visualización o búsqueda) y si la visita se debió a un clic o a una visualización. El delimitador del ID de EF es un signo de dos puntos, en lugar del signo de exclamación del ID de AMO.

| Sufijo de ID de EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Ejemplos de reglas de procesamiento que utilizan el ID de EF

#### Mostrar regla de pulsaciones

Cree un canal de marketing de pulsaciones de visualización capturando solo las pulsaciones. Dado que el ID de AMO es el mismo para las visualizaciones y las pulsaciones, esta regla utiliza la variable EF ID y el parámetro de cadena de consulta `ef_id`.

A veces, el seguimiento de las pulsaciones se realiza a través de la dirección URL (la predeterminada). En otros casos, los clics se rastrean a través del servicio Último evento del lado del servidor y, por lo tanto, la dirección URL no contiene el parámetro `ef_id`. Por lo tanto, la regla comprueba las condiciones en las que la variable EF ID o el parámetro de cadena de consulta `ef_id` termina con &quot;:d&quot;. Utilice el operador &quot;`Any`&quot; porque desea activar esta regla para cualquiera de las condiciones.

![Ejemplo de una regla de pulsaciones en pantalla](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Mostrar regla de visualización

Para crear un canal de visualización, cree una regla en la que el EF ID termine con &quot;:i&quot;. Como el visitante no hizo clic en el anuncio, el seguimiento de visualización no incluye `ef_id` ni `s_kwcid` en la dirección URL, por lo que la regla solo requiere una condición.

![Ejemplo de una regla de visualización completa](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por qué los datos de canal pueden variar entre el Adobe Advertising y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usando [!DNL Analytics Marketing Channels] con datos de Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para informes de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ID de Adobe Advertising usados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
