---
title: Usar Adobe Advertising ID para crear  [!DNL Marketing Channels] reglas
description: Aprenda a utilizar los Adobe Advertising ID para crear reglas de procesamiento para  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Usar los Adobe Advertising ID para crear [!DNL Marketing Channels] reglas de procesamiento

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

Puede usar los Adobe Advertising ID ([AMO ID y EF ID](../ids.md)) para configurar [!DNL Marketing Channels] reglas de procesamiento en Adobe Analytics. Utilice los Adobe Advertising ID para reglas específicas de sus campañas de Adobe Advertising. El orden en que se procesan las reglas determina si todos los datos posibles se capturan correctamente.

## El ID de AMO en las reglas de procesamiento

El identificador de AMO es el código de seguimiento principal que se usa para informar los datos de Adobe Advertising en [!DNL Analytics]. El ID de AMO es una concatenación de valores dinámicos administrados por Adobe para proporcionar informes granulares en [!DNL Analytics]. Se almacena en una dimensión [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o rVar (ID de AMO). El identificador de AMO se puede establecer en [!DNL Analytics] de dos maneras:

* Seguimiento de clics: Adobe Advertising establece el parámetro de cadena de consulta `s_kwcid` en un vínculo y [!DNL Analytics] lo recoge de la dirección URL de la página de aterrizaje cuando se produce una pulsación.

* Seguimiento de visualización ([!DNL DSP] solamente): [!DNL Last Event Service] detecta una visualización en el servidor y envía el identificador de AMO a [!DNL Analytics]. En este caso, la dirección URL no contiene un parámetro `s_kwcid`.

Los valores dinámicos dentro de los ID de AMO indican el canal de marketing que se rastreó:

* El prefijo del identificador de AMO se puede usar para identificar el canal de nivel superior dentro de [!DNL Marketing Channels].

* Las frases de caracteres del cuerpo del ID de AMO indican un tipo de campaña más específico.

* El sufijo &quot;vt&quot; está presente para el tráfico de visualización de [!DNL DSP] y se puede usar para crear canales de visualización y clics independientes de [!DNL DSP].

El resto del ID de AMO se puede ignorar.

| [!UICONTROL AMO ID] | Canal | Lógica de regla |
|--------|---------|--------------------|
| !ctv (sufijo) | [!UICONTROL DSP Connected TV ViewThrough] | Finaliza con |
| !d! (cuerpo) | [!UICONTROL Display Network] | Contiene |
| !g! (cuerpo) | [!UICONTROL Google Search] | Contiene |
| !s! (cuerpo) | [!UICONTROL Search Partner] | Contiene |
| !u! (cuerpo) | [!UICONTROL Smart Shopping Campaign] | Contiene |
| !ytv! (cuerpo) | [!UICONTROL YouTube Video Ad] | Contiene |
| !yts! (cuerpo) | [!UICONTROL YouTube Search Ad] | Contiene |
| !vp! (cuerpo) | [!UICONTROL Google Video Partners] | Contiene |
| !vt (sufijo) | [!UICONTROL DSP ViewThrough] | Finaliza con |
| ¡AL! (prefijo) | [!UICONTROL Paid Search] | Comienza con |
| ¡AC! (prefijo) | [!UICONTROL DSP Display] | Comienza con |

## El EF ID en las reglas de procesamiento

El AMO EF ID (EF ID) es el segundo código de seguimiento utilizado en la integración de [!DNL Analytics for Advertising]. Su propósito principal es rastrear y pasar datos de evento [!DNL Analytics] a Adobe Advertising. Cada vez que se produce una pulsación o una visualización, se genera un ID de EF único, aunque sea el mismo anuncio para el mismo visitante. El identificador de EF no se usa en la interfaz de usuario de creación de informes [!DNL Analytics] porque, por lo general, supera el límite de 500.000 valores únicos por variable en [!DNL Analytics], por lo que no se puede utilizar para la creación de informes. Las métricas y los metadatos de Adobe Advertising no se aplican al ID de EF; solo se aplican al ID de AMO. Se requiere la granularidad añadida del seguimiento para la optimización de campañas en Adobe Advertising, por lo que ambos ID son obligatorios.

Aunque la dimensión de ID de EF no se usa directamente en los informes de [!DNL Analytics], el ID de EF puede resultar útil para crear canales de marketing. El sufijo EF ID indica el canal (visualización o búsqueda) y si la visita se debió a un clic o a una visualización. El delimitador del ID de EF es un signo de dos puntos, en lugar del signo de exclamación del ID de AMO.

| Sufijo de ID de EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Ejemplos de reglas de procesamiento para Adobe Advertising

El siguiente conjunto de reglas de ejemplo se centra en las reglas de los canales publicitarios (Búsqueda de pago, Mostrar clic y Mostrar visualización). También se muestran la regla recomendada para la detección de búsqueda de pago (incluido cómo interactúa esa regla con la lógica del canal de marketing de búsqueda natural) y una actualización opcional de la regla de dominios de referencia naturales.

**Nota:** La pantalla puede separarse como dos canales o combinarse en un solo canal según las preferencias del anunciante.

En la captura de pantalla de ejemplo se incluyen otros canales para ilustrar el orden recomendado de operaciones de los canales publicitarios frente a otros canales en una implementación típica.

>[!IMPORTANT]
>
>Consulte &quot;[Orden de las operaciones para [!DNL Marketing Channels] reglas](#rule-order)&quot; para obtener información sobre el orden en que se deben procesar las reglas.

![Ejemplo de un conjunto de reglas de procesamiento](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### Regla de búsqueda de pago

Se recomienda incluir dos condiciones con el operador &quot;Any&quot; para una regla [!UICONTROL Paid Search]:

* Los datos de coste/clic/impresión contienen el ID de AMO, por lo que debe incluir el ID de AMO. El ID de AMO debe comenzar con &quot;AL!&quot; para asignar correctamente los datos de clics, costes e impresiones a [!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* Las direcciones URL para pulsaciones de [!UICONTROL Paid Search] siempre incluyen el parámetro de cadena de consulta `s_kwcid`, de modo que inclúyalo para garantizar que se produzca la deduplicación adecuada si el visitante vuelve a la página de aterrizaje. Incluir &quot;AL!&quot; antes de `s_kwcid` para asignar correctamente los datos de clics, costes e impresiones a [!UICONTROL Paid Search].

No establezca el valor del canal en el ID de AMO. En su lugar, configúrelo en algo como el Dominio de referencia, Motor de búsqueda + Palabra clave o Página. (Esto es relevante para todos los [!DNL Marketing Channels]).

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![Ejemplo de regla de búsqueda de pago](/help/integrations/assets/a4adc-mc-rule-paid-search.png "Ejemplo de regla de búsqueda de pago")

### Regla de búsqueda natural

Para [!UICONTROL Natural Search], asegúrese de que las reglas de detección [[!UICONTROL Paid Search]](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection) incluyan los parámetros de cadena de consulta `ef_id` y `s_kwcid`. (Normalmente, esto se configura automáticamente cuando Advertising Search, Social y Commerce están integrados en [!DNL Analytics], pero verifíquelo en caso de que un administrador de [!DNL Analytics] cambie la lógica después de configurar la integración).

Establezca la regla en &quot;Coincide con las reglas de detección de búsqueda natural&quot; (que suele ser la configuración predeterminada para este canal).

![Ejemplo de regla de búsqueda natural](/help/integrations/assets/a4adc-mc-rule-natural-search.png "Ejemplo de regla de búsqueda natural")

### Mostrar #1 de reglas de pulsación

Cree un canal de marketing Mostrar clic capturando solo las pulsaciones. Dado que el ID de AMO es el mismo para las visualizaciones y las pulsaciones, esta regla utiliza la variable EF ID y el parámetro de cadena de consulta `ef_id`.

A veces, el seguimiento de las pulsaciones se realiza a través de la dirección URL (la predeterminada). En otros casos, los clics se rastrean a través del servicio Último evento del lado del servidor y, por lo tanto, la dirección URL no contiene el parámetro `ef_id`. Por lo tanto, la regla comprueba las condiciones en las que la variable de ID de EF o el parámetro de cadena de consulta `ef_id` termina con &quot;:d&quot;. Utilice el operador &quot;`Any`&quot; porque desea activar esta regla para cualquiera de las condiciones.

![Ejemplo de una primera regla de clic en pantalla](/help/integrations/assets/a4adc-mc-rule-display-ct.png "Ejemplo de una primera regla de clic en pantalla")

### Regla de dominios de referencia naturales

(Opcional) Una práctica recomendada es agregar la condición &quot;Es la primera página de la visita&quot; con el operador &quot;Cualquiera&quot; a la regla estándar [!UICONTROL Natural Referring Domains]. Aunque esta regla es opcional, puede ayudar a evitar que el caso límite de los referentes naturales se establezca cuando el usuario hace clic en el botón Atrás para regresar a la página de aterrizaje.

![Ejemplo de regla de dominios de referencia naturales](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "Ejemplo de regla de dominios de referencia naturales")

### Mostrar regla de visualización de CTV

Para realizar el seguimiento de [!DNL DSP] visualizaciones de TV (CTV) conectadas, cree una regla en la que el identificador de AMO termine en `"!ctv"`. Dado que el visitante no hizo clic en el anuncio, el seguimiento de visualización no incluye `ef_id` ni `s_kwcid` en la dirección URL, y la regla solo requiere una condición.

![Ejemplo de regla de visualización de CTV](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png "Ejemplo de regla de visualización de CTV")

### Mostrar regla de visualización

Para crear un canal de visualización de visualización, cree una regla en la que el ID de EF termine con &quot;:i&quot;. Dado que el visitante no hizo clic en el anuncio, el seguimiento de visualización no incluye `ef_id` ni `s_kwcid` en la dirección URL, y la regla solo requiere una condición.

![Ejemplo de una regla Display ViewThrough](/help/integrations/assets/a4adc-mc-rule-display-vt.png "Ejemplo de una regla Display ViewThrough")

### Mostrar #2 de reglas de pulsación

Para la segunda regla Mostrar clic, establezca **AMO ID empieza por &quot;AC!&quot;**. Esta segunda regla existe para capturar los datos de clics, costos e impresiones del canal de visualización que llega directamente de Adobe Advertising a [!DNL Analytics]. Estos datos se atribuyen a un ID de AMO, pero no incluyen una dirección URL con la cadena de consulta `ef_id`, por lo que estas visitas no están conectadas con un ID de AMO EF, que es lo que captura la primera regla de clic en mostrar.

![Ejemplo de una segunda regla Display ClickThrough](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "Ejemplo de una segunda regla Display ClickThrough")

## Orden de operaciones para las reglas [!DNL Marketing Channels] {#rule-order}

![Orden ideal de operaciones para reglas relacionadas con Adobe Advertising](/help/integrations/assets/a4adc-mc-rule-order.png "Orden ideal de operaciones para reglas relacionadas con Adobe Advertising")

* Poner [!UICONTROL Paid Search] *antes de* [!UICONTROL Natural Search]. De lo contrario, los datos de búsqueda de pago se pueden asignar a la búsqueda natural.

* Ponga **first** [!UICONTROL Display ClickThrough] *antes que* [!UICONTROL Natural Referring Domains] y [!UICONTROL Natural Social].

* Cuando use [!UICONTROL CTV view-throughs], póngalo *antes de* [!UICONTROL Display ViewThroughs]. De lo contrario, las visualizaciones de CTV se capturarán como visualizaciones de visualizaciones.

* Coloque [!UICONTROL Display ViewThroughs] *después de* otros canales, pero antes de [!UICONTROL Internal] y [!UICONTROL Direct], porque es posible que se produzca una visualización y una pulsación que no sea de [!DNL Advertising] en el mismo evento de aterrizaje. Por ejemplo: un visitante puede ver un anuncio de Adobe Advertising, tener una impresión y luego visitar el sitio a través de [!UICONTROL Natural Search].

  Se recomienda priorizar los demás canales (excepto [!UICONTROL Internal] y [!UICONTROL Direct]) sobre las visualizaciones.

* Algunos anunciantes pueden optar por priorizar [!UICONTROL Display ViewThroughs] sobre [!UICONTROL Natural Referring Domains]. Para ello, intercambie el orden de procesamiento de las dos reglas.

* La regla **second** [!UICONTROL Display ClickThrough] está ahí para capturar los datos de clics, costos e impresiones que llegan directamente de Adobe Advertising a [!DNL Analytics]. Dado que estos datos solo se atribuyen a un ID de AMO, estas visitas no están conectadas con un ID de AMO EF. Si no establece esta regla, todos los datos de clics, costes e impresiones caerán dentro del canal [!UICONTROL Direct], que es el canal predeterminado para cualquier dato que no coincida con [!DNL Marketing Channel]. Esta regla debe venir *después* de la regla de visualización o detectará cualquier visualización.

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por qué los datos de canal pueden variar entre Adobe Advertising y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usando [!DNL Analytics Marketing Channels] con datos de Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para los informes de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ID de Adobe Advertising usados por [!DNL Analytics]](/help/integrations/analytics/ids.md)