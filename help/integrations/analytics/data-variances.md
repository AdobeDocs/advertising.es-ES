---
title: Variaciones de datos previstas entre [!DNL Analytics] Publicidad de Adobe y
description: Variaciones de datos previstas entre [!DNL Analytics] Publicidad de Adobe y
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '3282'
ht-degree: 0%

---

# Variaciones de datos previstas entre [!DNL Analytics] Publicidad de Adobe y

*Anunciantes con una integración de Adobe de Advertising-Adobe Analytics solamente*

Anunciantes con el [!DNL Analytics for Advertising] <!-- (A4AdC) --> Integración de Seguimiento de publicidad de pago mediante Adobe Advertising y Adobe Analytics. Al realizar el seguimiento de medios, campañas y canales a través de varios sistemas, los mismos conjuntos de datos de diferentes sistemas rara vez coinciden por completo. En este documento se explica cómo debería esperar datos para medios que se trafican a través de la publicidad de Adobe para compararlos con datos de los diferentes sistemas en los que se rastrea el medio dentro de [!DNL Analytics].

>[!NOTE]
>
>Este documento se centra en la publicidad de Adobe y Analytics, pero muchos de los puntos clave también se pueden transferir a otras soluciones de seguimiento.

## Diferencias de atribución en informes similares

### Ventanas retrospectivas y modelos de atribución potencialmente diferentes

El [!DNL Analytics for Advertising] La integración de utiliza dos variables (eVars o rVars \[eVars reservadas]\) para capturar el [ID de EF e ID de AMO](ids.md). Estas variables se configuran con una sola ventana retrospectiva (el tiempo en el que se atribuyen las pulsaciones y las visualizaciones) y un modelo de atribución. A menos que se especifique lo contrario, las variables se configuran para que coincidan con la ventana retrospectiva de clics predeterminada y del modelo de atribución en Adobe Advertising.

Sin embargo, las ventanas retrospectivas y los modelos de atribución se pueden configurar tanto en Analytics (a través de las eVars) como en la publicidad de Adobe. Además, en la publicidad de Adobe, el modelo de atribución se puede configurar no solo en el nivel del anunciante (para la optimización de ofertas), sino también dentro de vistas de datos e informes individuales (solo para fines de creación de informes). DSP Por ejemplo, una organización puede preferir utilizar el modelo de atribución de distribución par para la optimización, pero puede utilizar la atribución de último contacto para informes en Advertising o [!DNL Advertising Search, Social, & Commerce]. Al cambiar los modelos de atribución, cambia el número de conversiones atribuidas.

Si se modifica una ventana retrospectiva de creación de informes o un modelo de atribución en un producto y no en el otro, los mismos informes de cada sistema mostrarán datos distintos:

* **Ejemplo de discrepancias causadas por diferentes ventanas retrospectivas:**

   Supongamos que la publicidad de Adobe tiene una ventana retrospectiva de clics de 60 días y [!DNL Analytics] tiene una ventana retrospectiva de 30 días. Y supongamos que un usuario llega al sitio a través de un anuncio con seguimiento publicitario de Adobe, sale, y luego regresa el día 45 y se convierte. Adobe Advertising atribuirá la conversión a la visita inicial porque la conversión se produjo dentro de la ventana retrospectiva de 60 días. [!DNL Analytics]Sin embargo, no puede atribuir la conversión a la visita inicial porque la conversión se produjo después de que caducara la ventana retrospectiva de 30 días. En este ejemplo, la publicidad de Adobe informaría de un número de conversiones mayor que [!DNL Analytics] lo haría.

   ![Ejemplo de una conversión atribuida en la publicidad de Adobe pero no en [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Ejemplo de discrepancias causadas por diferentes modelos de atribución:**

   Supongamos que un usuario interactúa con tres anuncios publicitarios de Adobe diferentes antes de la conversión, con ingresos como tipo de conversión. Si un informe de publicidad de Adobes utiliza un modelo de distribución par para la atribución, atribuirá los ingresos de forma uniforme en todos los anuncios. If [!DNL Analytics] utiliza el modelo de atribución de último contacto; sin embargo, los ingresos se atribuirán al último anuncio. En el ejemplo siguiente, Adobe Advertising atribuye incluso 10 USD de los 30 USD de ingresos capturados a cada uno de los tres anuncios, mientras que [!DNL Analytics] atribuye los 30 USD de ingresos al último anuncio visto por el usuario. Al comparar informes de publicidad de Adobe y [!DNL Analytics], verá el impacto de la diferencia en la atribución.

   ![Ingresos diferentes atribuidos a la publicidad de Adobe y [!DNL Analytics] basado en diferentes modelos de atribución](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La práctica recomendada es utilizar las mismas ventanas retrospectivas y el mismo modelo de atribución tanto en la publicidad de Adobe como en [!DNL Analytics]. Póngase en contacto con el equipo de cuenta de Adobe según sea necesario para identificar la configuración actual y mantenerla sincronizada.

Estos mismos conceptos se aplican a cualquier otro canal similar que utilice diferentes ventanas retrospectivas o modelos de atribución.

#### Diferentes ventanas retrospectivas para el seguimiento de visualización {#impression-lookback}

En la publicidad de Adobe, la atribución se basa en los clics y las impresiones, y puede configurar diferentes ventanas retrospectivas para los clics y las impresiones. Entrada [!DNL Analytics]Sin embargo, la atribución se basa en las pulsaciones y las visualizaciones, y no tiene la opción de establecer ventanas de atribución distintas para las pulsaciones y las visualizaciones; el seguimiento de cada una de ellas comienza en la visita inicial al sitio. Una impresión se puede producir el mismo día o varios días antes de que se produzca una visualización, y esto puede afectar a dónde se inicia la ventana de atribución en cada sistema.

Normalmente, la mayoría de las conversiones de visualización se producen con la rapidez suficiente para que ambos sistemas atribuyan crédito. Sin embargo, algunas conversiones pueden producirse fuera de la ventana retrospectiva de impresión de publicidad de Adobe, pero dentro de la variable [!DNL Analytics] ventana retrospectiva; estas conversiones se atribuyen a la visualización en [!DNL Analytics] pero no a la impresión en Adobe Advertising.

En el siguiente ejemplo, supongamos que a un visitante se le sirvió un anuncio el día 1, realizó una visita de visualización (es decir, visitó la página de aterrizaje del anuncio sin hacer clic anteriormente en él) el día 2 y se convirtió el día 45. En este caso, la publicidad de Adobe rastrearía al usuario entre los días 1 y 14 (con una retrospectiva de 14 días), [!DNL Analytics] rastrearía al usuario entre los días 2 y 61 (con una retrospectiva de 60 días), y la conversión el día 45 se atribuiría al anuncio dentro de [!DNL Analytics] pero no dentro de Adobe Advertising.

![Ejemplo de una conversión de visualización atribuida en [!DNL Analytics] pero no Adobe Publicidad](/help/integrations/assets/a4adc-viewthrough-example.png)

Otra causa de discrepancias es que, en la publicidad de Adobe, puede asignar conversiones de visualización como personalizadas *ponderación de visualizaciones* que es relativo al peso atribuido a una conversión basada en clics. La ponderación de visualizaciones predeterminada es del 40 %, lo que significa que una conversión de visualizaciones se cuenta como el 40 % del valor de una conversión basada en clics. [!DNL Analytics] no proporciona dicha ponderación de las conversiones de visualización. Por ejemplo, un pedido de ingresos de 100 USD capturado en [!DNL Analytics] se descontará a 40 USD en publicidad de Adobes si utiliza el peso de visualización predeterminado: una diferencia de 60 USD.

Tenga en cuenta estas diferencias al comparar las conversiones de visualización entre publicidad de Adobe y [!DNL Analytics] informes.

#### Modelos de atribución disponibles

| Atribución de publicidad de Adobe | [!DNL Analytics] Atribución | Asignación de eVar/eVar |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>No usar* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>Para la asignación lineal, [!DNL Analytics] atribuye los eventos de éxito de forma equitativa en todos los valores de eVar dentro de una sola visita, por lo que debe utilizar la asignación lineal con una caducidad de eVar de &quot;Visita&quot;. Sin embargo, para la publicidad, el uso de la atribución lineal lleva a una asignación que no es realmente lineal y a unos informes inferiores a los ideales. Por ejemplo, si un visitante interactúa con tres anuncios antes de convertirlos en tres visitas separadas, solo el anuncio visto en la última visita se atribuye a la conversión, no los tres anuncios.
>
>Además, si se cambia la asignación de conversión a &quot;Lineal&quot; o de &quot;Lineal&quot;, los datos históricos no se mostrarán, lo que puede llevar a una exposición incorrecta de los datos en los informes. Por ejemplo, la asignación lineal puede dividir los ingresos entre un número de valores de eVar diferentes. Si cambia la asignación a Más reciente, el 100 % de esos ingresos se asocian al valor único más reciente. Esta asociación puede llevarle a conclusiones incorrectas.
>
>Para evitar confusiones, [!DNL Analytics] hace que los datos históricos no estén disponibles en la interfaz de informes. Puede ver los datos históricos si vuelve a cambiar el eVar a la configuración de asignación inicial, aunque no debe cambiar la configuración de asignación de eVar simplemente para acceder a los datos históricos. Adobe recomienda utilizar un eVar nuevo cuando desee aplicar una nueva configuración de asignación para datos que ya se están registrando, en lugar de cambiar la configuración de asignación para un eVar que ya tiene una cantidad significativa de datos históricos.

Ver una lista de [!DNL Analytics] modelos de atribución y sus definiciones en [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Si ha iniciado sesión en [!DNL Search, Social, & Commerce], puede encontrar una lista

* (Usuarios en Norteamérica) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Todos los demás usuarios) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Atribución de fecha de evento en publicidad de Adobe

En la publicidad de Adobe, puede generar informes de los datos de conversión según la fecha y el evento de clic asociados (la fecha del evento de clic o impresión) o según la fecha de la transacción (la fecha de conversión). El concepto de informe de fechas de eventos/clics no existe en [!DNL Analytics]; todas las conversiones rastreadas en [!DNL Analytics] se notifican por fecha de transacción. Como resultado, se puede informar de la misma conversión con diferentes fechas en Publicidad de Adobe y [!DNL Analytics]. Por ejemplo, piense en un usuario que hace clic en un anuncio el 1 de enero y convierte el 5 de enero. Si visualiza los datos de conversión por fecha de evento en la publicidad de Adobe, se enviará un informe de la conversión el 1 de enero, cuando se produjo el clic. Entrada [!DNL Analytics], se informaría de la misma conversión el 5 de enero.

![Ejemplo de una conversión atribuida a diferentes fechas](/help/integrations/assets/a4adc-conversions-based-on.png)

## Atribución en [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] informe](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) permite configurar reglas para identificar diferentes canales de marketing en función de distintos aspectos de la información de la visita. Puede realizar un seguimiento de los canales de Adobe rastreados por publicidad ([!UICONTROL Display Click Through], [!UICONTROL Display View Through], y [!UICONTROL Paid Search]) como [!DNL Marketing Channels] mediante el uso de `ef_id` parámetro de cadena de consulta para identificar el canal. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Sin embargo, aunque la variable [!DNL Marketing Channels] Los informes de pueden realizar un seguimiento de los canales publicitarios de Adobe. Es posible que los datos no coincidan con los informes de publicidad de Adobe por varios motivos. Consulte las secciones siguientes para obtener más información.

>[!NOTE]
>
> Los siguientes conceptos principales también se aplican a cualquier seguimiento de varios canales que implique campañas no rastreadas en la publicidad de Adobe, como la [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (también conocido como el Dimension de &quot;código de seguimiento&quot; o &quot;eVar 0&quot;) y seguimiento de eVar personalizado.

### Modelos de atribución potencialmente diferentes en [!DNL Marketing Channels]

Más [!DNL Marketing Channels] los informes se configuran con [!UICONTROL Last Touch] atribución, para la cual el último canal de marketing detectado tiene asignado el 100 % del valor de conversión. Uso de diferentes modelos de atribución para [!DNL Marketing Channels] Los informes de y los informes de publicidad de Adobe de encontrarán discrepancias en las conversiones atribuidas.

### Una ventana retrospectiva potencialmente diferente en [!DNL Marketing Channels]

La ventana retrospectiva para [!DNL Marketing Channels] se puede personalizar. En la publicidad de Adobe, la ventana retrospectiva de clics es configurable, aunque es común una ventana fija de 60 días. Si los dos productos utilizan ventanas retrospectivas diferentes, puede esperar discrepancias en los datos.

### Atribución de canal diferente en [!DNL Marketing Channels]

Los informes de publicidad de Adobe capturan solo los medios de pago traficados a través de publicidad de Adobe (búsqueda de pago para [!DNL Advertising Search, Social, & Commerce] DSP anuncios y visualización para anuncios de Advertising), mientras que [!DNL Marketing Channels] los informes pueden realizar un seguimiento de todos los canales digitales. Esto puede provocar una discrepancia en el canal para el que se atribuye una conversión.

Por ejemplo, la búsqueda de pago y los canales de búsqueda natural a menudo tienen una relación simbiótica, en la que cada canal ayuda al otro. El [!DNL Marketing Channels] Este informe atribuirá algunas conversiones a la búsqueda natural que Adobe Advertising no atribuirá porque no realiza el seguimiento de la búsqueda natural.

Piense también en un cliente que ve un anuncio en pantalla, hace clic en un anuncio de búsqueda de pago, hace clic dentro de un mensaje de correo electrónico y, a continuación, realiza un pedido de 30 USD. Incluso si Adobe Advertising y [!DNL Marketing Channels] Si ambos utilizan el modelo de atribución de último contacto, la conversión se atribuiría de forma diferente a cada uno. La publicidad de Adobe no tiene acceso a [!UICONTROL Email] canal, de modo que acreditaría la búsqueda de pago de la conversión. [!DNL Marketing Channels], sin embargo, tiene acceso a los tres canales, por lo que tendría crédito [!UICONTROL Email] para la conversión.

![Ejemplo de atribución de conversión diferente en Publicidad de Adobe frente a [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Para obtener más información sobre por qué pueden variar las métricas, consulte[Por qué los datos de canal pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Diferencias de datos en Adobe Analytics [!DNL Paid Search Detection]

El [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) función en [!DNL Analytics] permite a las empresas [defina reglas para rastrear el tráfico de búsqueda orgánica y de pago](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) para motores de búsqueda especificados. El [!DNL Paid Search Detection] las reglas utilizan una cadena de consulta y el dominio de referencia para identificar el tráfico de búsqueda de pago y natural. El [!DNL Paid Search Detection] los informes forman parte del grupo más amplio de [Métodos de búsqueda](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) Los informes de caducan cuando se produce un evento específico (como un cierre de compra del carro de compras) o cuando finaliza la visita.

A continuación se muestra la interfaz para crear un [!DNL Paid Search Detection] conjunto de reglas:

![Ejemplo de una regla de detección de búsqueda paga establecida en [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

El resultante [!DNL Paid Search Detection] Los informes de incluyen [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine], y [!UICONTROL Natural Search Keywords] informes.

Tenga en cuenta las dos limitaciones siguientes con los datos de [!DNL Paid Search Detection] informes:

* El [!UICONTROL Paid Search Keywords] y [!UICONTROL Natural Search Keywords] Los informes de muestran las consultas de búsqueda identificadas por las direcciones URL de referencia, no las palabras clave por las que los usuarios pujan. Adobe Publicidad y [!DNL Analytics] Los informes de muestran las palabras clave reales, por lo que no espere que se alineen con el [!DNL Paid Search Detection] informes de palabras clave.

* Si la variable [!DNL Paid Search Detection] original, la consulta de búsqueda de origen (la cadena de caracteres que el usuario introdujo en la barra de búsqueda del motor de búsqueda) estaba más fácilmente disponible para los anunciantes a través de la dirección URL de referencia. Actualmente, los motores de búsqueda ofuscan en gran medida la consulta de búsqueda y la variable [!DNL Paid Search Detection] los informes de palabras clave tienen un valor limitado porque la mayoría de los datos de consulta se encuentran dentro de &quot;sin especificar&quot;.

   Con [!DNL Analytics for Advertising], los anunciantes aún pueden rastrear palabras clave de pago en [!DNL Analytics]. El dominio de referencia informa al motor de que motor de búsqueda produjo el tráfico. Dado que la información de cuenta específica del anunciante no está vinculada al dominio de referencia, todo el tráfico se enumera en el motor de búsqueda. Los anunciantes con varias cuentas en el mismo motor de búsqueda deben hacer referencia a Publicidad de Adobe o [!DNL Analytics] creación de informes para informes específicos de la cuenta.

### Por qué configurar [!DNL Paid Search Detection]?

El [!DNL Paid Search Detection] Los informes de permiten identificar el tráfico de búsqueda natural en la [[!DNL Analytics Marketing Channels] informes](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). La separación del tráfico de búsqueda de pago y el tráfico de búsqueda natural es una buena manera de comprender el valor que la búsqueda natural aporta al ecosistema de marketing completo.

## Validación de datos de clics para [!DNL Analytics for Advertising] {#data-validation}

Para la integración, debe validar los datos de clics para asegurarse de que todas las páginas del sitio rastrean correctamente los clics.

Entrada [!DNL Analytics], una de las formas más sencillas de validar [!DNL Analytics for Advertising] el seguimiento es comparar los clics con las instancias mediante la métrica calculada &quot;Clics en instancias de ID de AMO&quot;, que se calcula de la siguiente manera:

```
Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)
```

[!UICONTROL AMO ID Instances] representa el número de veces que los ID de AMO (`s_kwcid` parámetros) se rastrean en el sitio. Cada vez que se hace clic en un anuncio, aparece un `s_kwcid` se añade a la dirección URL de la página de aterrizaje. El número de [!UICONTROL AMO ID Instances], por lo tanto, es análogo al número de clics y se puede validar con clics de anuncios reales. Normalmente, vemos una tasa de coincidencia del 80 % para [!DNL Search, Social, & Commerce] y una tasa de coincidencia del 30 % para [!DNL DSP] tráfico (cuando se filtra para incluir solo pulsaciones) [!UICONTROL AMO ID Instances]). La diferencia de expectativas entre la búsqueda y la visualización se puede explicar por el comportamiento de tráfico esperado. La búsqueda captura la intención y, como tal, los usuarios suelen hacer clic en los resultados de búsqueda de su consulta. Sin embargo, es más probable que los usuarios que ven un anuncio en pantalla o en vídeo en línea hagan clic en el anuncio de forma involuntaria y luego reboten en el sitio o abandonen la nueva ventana que se carga antes de que se rastree la actividad de la página.

En los informes de publicidad de Adobe, puede comparar de forma similar los clics con las instancias mediante el icono &quot;[!UICONTROL ef_id_instances]&quot; en lugar de [!UICONTROL AMO ID Instances]:

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

Aunque debería esperar una alta tasa de coincidencia entre el AMO ID y el EF ID, no espere una paridad del 100 % porque el AMO ID y el EF ID rastrean fundamentalmente datos diferentes y esta diferencia puede llevar a ligeras diferencias en el total [!UICONTROL AMO ID Instances] y [!UICONTROL EF ID Instances]. Si el total [!UICONTROL AMO ID Instances] in [!DNL Analytics] diferir de [!UICONTROL EF ID Instances] En la publicidad de Adobe por más del 1%, sin embargo, póngase en contacto con su equipo de cuenta de Adobe para obtener ayuda.

Para obtener más información sobre el AMO ID y el EF ID, consulte [ID de publicidad de Adobe utilizados por Analytics](ids.md).

El siguiente es un ejemplo de un espacio de trabajo para rastrear clics a instancias.

![Ejemplo de un espacio de trabajo para rastrear clics a instancias](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Comparación de conjuntos de datos en [!DNL Analytics for Advertising] Versus en publicidad de Adobe

El [ID de AMO](ids.md) (parámetro de cadena de consulta s_kwcid) se usa para los informes en [!DNL Analytics], y el [EF ID](ids.md) se utiliza para los informes en la publicidad de Adobe. Como son valores distintos, es posible que un valor se dañe o no se añada a la página de aterrizaje.

Por ejemplo, supongamos que tenemos la siguiente página de aterrizaje:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

donde el EF ID es &quot;`test_ef_id`&quot; y el ID de AMO es &quot;`test_amo_id`.&quot;

Si se produce un redireccionamiento del lado del sitio, la dirección URL podría terminar de esta manera:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

donde el EF ID es &quot;`test_ef_id`&quot; y el ID de AMO es &quot;`test_amo_id#redirectAnchorTag`.&quot;

En este ejemplo, la adición de la etiqueta de anclaje agrega caracteres inesperados al ID de AMO, lo que da como resultado un valor que Analytics no reconoce. Este ID de AMO no se clasificaría y las conversiones asociadas a él se incluirían en &quot;[!UICONTROL unspecified]&quot; o &quot;[!UICONTROL none]&quot; en [!DNL Analytics] informes.

Afortunadamente, si bien problemas como este son comunes, por lo general no resultan en un alto porcentaje de discrepancia. Sin embargo, si observa una gran discrepancia entre los ID de AMO en [!DNL Analytics] y EF ID en la publicidad de Adobe, póngase en contacto con su equipo de cuenta de Adobe para obtener ayuda.

## Otras consideraciones de métricas

### Diferencia entre clics y visitas {#clicks-vs-visits}

Parecen análogos, pero los clics y las visitas representan datos diferentes:

* **Haga clic:** [!DNL DSP] o el motor de búsqueda registra un clic cuando un visitante hace clic en un anuncio del sitio web de un publicador.

* **Visita:** [!DNL Analytics] define un [visita](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) como una serie de vistas de página realizadas por un usuario que finalizan según uno de varios criterios, como 30 minutos de inactividad.

Por definición, un clic puede llevar a varias visitas.

Veamos el siguiente ejemplo: el usuario 1 y el usuario 2 acceden a un sitio haciendo clic en un anuncio publicitario de Adobe. El usuario 1 ve cuatro páginas y luego sale por el día, por lo que el clic inicial resulta en una visita. El usuario 2 ve dos páginas, sale para un almuerzo de 45 minutos, regresa, ve dos páginas más y luego sale; en este caso, el clic inicial resulta en dos visitas.

![Ejemplo de la diferencia entre clics y visitas](/help/integrations/assets/a4adc-visits-example.png)

### Diferencia entre clics y pulsaciones

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Los clics y las pulsaciones son dos métricas diferentes:

* **Haga clic:** [!DNL DSP] o el motor de búsqueda registra un clic cuando un visitante hace clic en un anuncio del sitio web de un publicador.

* **Pulsaciones:** [!DNL Analytics] registra un clic cuando el visitante aterriza en el sitio web de destino, se carga la página de aterrizaje y se [!DNL Analytics] al final de la página envía los datos a [!DNL Analytics].

Los clics y las pulsaciones pueden diferir considerablemente debido a los clics accidentales en los anuncios. Hemos observado que la mayoría de los clics en los anuncios en pantalla son clics accidentales, y estos visitantes accidentales pulsan el botón Atrás antes de que se cargue la página de aterrizaje, por lo que [!DNL Analytics] no se puede registrar una pulsación. Esto es especialmente cierto en el caso de los anuncios en los que es más probable un clic accidental, como los anuncios móviles, los anuncios de vídeo y los anuncios que llenan la pantalla, y que deben cerrarse antes de que el usuario pueda ver la página.

También es menos probable que los sitios cargados en dispositivos móviles generen clics debido al menor ancho de banda o la potencia de procesamiento disponible, lo que provoca que las páginas de aterrizaje tarden más en cargarse. No es inusual que entre el 50 y el 70 % de los clics no produzcan proporción de clics. En entornos móviles, la diferencia puede alcanzar el 90 % debido a la combinación de un navegador más lento y a la mayor probabilidad de que el usuario haga clic accidentalmente en el anuncio mientras se desplaza por la página o intenta cerrar el anuncio.

Los datos de clics también se pueden registrar en entornos que no pueden registrar la proporción de clics con los mecanismos de seguimiento actuales (como los clics que entran o salen de una aplicación móvil) o para los que el anunciante solo ha implementado un método de seguimiento (por ejemplo, con el método de visualización de JavaScript, los exploradores que bloquean cookies de terceros rastrean los clics, pero no los clics). Una razón clave por la que Adobe recomienda implementar los enfoques de seguimiento de URL de clics y seguimiento de JavaScript de visualización es maximizar la cobertura de las pulsaciones rastreables.

### Uso de métricas de tráfico de publicidad de Adobe para Dimension de publicidad que no sea de Adobe

Adobe Advertising proporciona a Analytics [métricas de tráfico específicas de la publicidad y las dimensiones relacionadas de [!DNL DSP] y [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Las métricas proporcionadas por la publicidad de Adobe solo son aplicables a las dimensiones especificadas de la publicidad de Adobe y los datos no están disponibles para otras dimensiones en [!DNL Analytics].

Por ejemplo, si ve la variable [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] métricas por cuenta, que es una dimensión de publicidad de Adobe, y verá el total [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] por cuenta.

![Ejemplo de métricas de publicidad de Adobe en un informe con una dimensión de publicidad de Adobe](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Sin embargo, si ve el [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] métricas calculadas por una dimensión en la página (como Página), para la que la publicidad de Adobe no proporciona datos, la variable [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] cada página será cero (0).

![Ejemplo de métricas de publicidad de Adobe en un informe con una dimensión no admitida](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Uso de [!UICONTROL AMO ID Instances] como sustituto de los clics con Dimension de publicidad que no sean de Adobe

Ya que no puede usar [!UICONTROL AMO Clicks] con las dimensiones en el sitio, es posible que desee encontrar un equivalente a clics. Puede que tenga la tentación de utilizar las visitas como sustituto, pero no son la mejor opción, ya que cada visitante puede tener varias visitas. (Consulte &quot;[Diferencia entre clics y visitas](#clicks-vs-visits).&quot; En su lugar, recomendamos utilizar [!UICONTROL AMO ID Instances], que es el número de veces que se captura el ID de AMO. While [!UICONTROL AMO ID Instances] no coincide con [!UICONTROL AMO Clicks] exactamente, son la mejor opción para medir el tráfico de clics en el sitio. Para obtener más información, consulte &quot;[Validación de datos para [!DNL Analytics for Advertising]](#data-validation).&quot;

![Ejemplo de [!UICONTROL AMO ID Instances] en lugar de [!UICONTROL AMO Clicks] para una dimensión no admitida](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [ID de publicidad de Adobe utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Métricas de publicidad de Adobe en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en publicidad de Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Por qué los datos pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

