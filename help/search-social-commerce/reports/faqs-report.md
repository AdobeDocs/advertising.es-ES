---
title: Preguntas frecuentes sobre informes personalizados
description: Obtenga respuestas a preguntas comunes acerca de los informes de rendimiento, incluida la resolución de problemas de datos.
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# Preguntas frecuentes sobre informes personalizados

## Preguntas generales

+++¿Qué sucede si el intervalo de fechas del informe comienza antes de que los datos del informe estén disponibles?
El informe se genera, pero solo incluye datos de las fechas para las que hay datos disponibles. Para obtener más información sobre cuándo están disponibles los datos para cada tipo de informe, consulte[Los datos utilizados para los informes](data-used-for-reports.md).&quot;
+++

+++¿Cuál es la diferencia entre los informes basados en fecha de clic y fecha de transacción?
Cuando se informan de las conversiones por fecha de transacción, los datos incluyen transacciones cuya fecha de transacción se produjo durante el período de tiempo especificado. Esta opción es la configuración predeterminada en los informes básicos y avanzados, y muestra cuántos ingresos se obtuvieron en el período de tiempo especificado.

Cuando se informan de las conversiones por fecha de clic, los datos incluyen transacciones que resultaron de un clic que se produjo durante el período de tiempo especificado. Cuando un portafolio tiene retrasos significativos entre clics y transacciones, este tipo de informes muestra los ingresos históricos por clic del portafolio, lo que le da una idea de qué comportamientos de ingresos esperar con el tiempo.

![Comparar informe por fecha de clic con informe por fecha de transacción](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Comparar informe por fecha de clic con informe por fecha de transacción")
+++

+++¿Qué sucede si cambio la ventana retrospectiva de clics o de impresiones?
(Solo anunciantes con un servicio de seguimiento de conversión basado en píxeles de Advertising) Los datos de los eventos resultantes del clic inicial se recopilan durante un período más largo o más corto.

El nombre de un anunciante [haga clic en ventana retrospectiva](/help/search-social-commerce/glossary.md#c-d) y [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j) determine el número de días después de que se produzca un clic de pago o una impresión de visualización (respectivamente) en los que el evento se puede atribuir a una conversión. Cambiar un valor a un periodo más largo o más corto puede ser importante para los anunciantes con periodos especialmente cortos o largos de clic a ingresos o de impresión a ingresos de visualización.

**Práctica recomendada:** Asegúrese de que las ventanas retrospectivas sean más largas que los tiempos de clic a ingresos y de impresión de visualización de la mayoría de las palabras clave o anuncios. Cuando son más cortas, algunas conversiones no están asociadas con el clic o la impresión inicial.
+++

+++¿Cómo sé qué conversiones resultaron de un [!DNL Google Ads] ¿extensión de anuncio o lista de productos?
Puede ver qué conversiones resultaron de un clic en una [!DNL Google Ads] extensión del anuncio (en lugar de en el propio anuncio) o en una lista de productos generando un [!UICONTROL Transaction Report]. El [!UICONTROL Link Type] El valor de columna muestra el tipo y el título de un vínculo en el que se hizo clic:

* Los listados de productos se enumeran como `pla:<product ID>`, como `pla:8525822`.

* Los vínculos de sitio se muestran como `sl:<Sitelink text>`, como `sl:See Current Offers`.

  También puede identificar un vínculo de sitio si incluye la variable [!UICONTROL Tracking URL] en el informe. El [!UICONTROL Tracking URL] para un vínculo de sitio incluye el atributo `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Conversiones de [!DNL Google Ads] las ubicaciones y las extensiones de teléfono se incluyen en los datos de los anuncios que acompañan. No se registran por separado.

+++

+++El &quot;[!UICONTROL Keyword]&quot; en mi informe incluye un valor &quot;(contenido de grupo de anuncios) &lt;*nombre del grupo de publicidad*>.&quot;
Cuando la fila incluye datos para campañas de búsqueda con contenido habilitado, campañas de visualización o campañas sociales (que no incluyen palabras clave), la variable [!UICONTROL Keyword] La columna muestra el nombre del grupo de anuncios aplicable en su lugar.
+++

+++Debido a cambios estacionales o de mercado, mis informes muestran datos atípicos. ¿Afecta esto a las ofertas una vez que cambian las condiciones?
La capacidad de optimización crea diariamente sus modelos de ingresos para cada unidad de oferta para garantizar que identifique las tendencias y responda inmediatamente a ellas, y los modelos incorporan datos históricos a largo plazo para ayudar a predecir el rendimiento estacional. Configuración de la semivida del modelo de ingresos de la cartera<!-- add link to glossary? --> también determina la ponderación de los datos de ingresos recientes. La práctica recomendada es reducir la semivida durante un período de rendimiento atípico, pero aumentarla después de ajustar el modelo de ingresos. Si tiene alguna pregunta sobre si es necesario ajustar la semivida, póngase en contacto con el equipo de cuenta de Adobe.

Si no desea que los datos del periodo afecten a las pujas futuras, puede optar por excluir esas fechas del modelo. Póngase en contacto con el equipo de cuenta de Adobe para excluir las fechas.
+++

+++¿Puedo crear un informe con una métrica de propiedad de una cuenta específica, como [!UICONTROL Device] o [!UICONTROL Objective Name]?
Para informes de entidad de campaña ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], y [!UICONTROL Product Group Report]), los datos de las métricas se agregan dinámicamente mediante las columnas de propiedad que se incluyen en el informe. Si lo desea, puede quitar la columna de clave del informe e incluir solo las columnas de propiedades de las que desea agregar datos.

Por ejemplo, si genera un [!UICONTROL Keyword Report] que incluye el [!UICONTROL Ad Group] y  De forma predeterminada, las columnas Dispositivo agregan métricas para cada palabra clave por grupo de anuncios y tipo de dispositivo. Sin embargo, si elimina el [!UICONTROL Keyword] antes de generar el informe, el informe genera dinámicamente métricas para los grupos de anuncios especificados por tipo de dispositivo.

>[!NOTE]
>
>No puede utilizar esta función para agregar datos por clasificaciones de etiquetas. Se omite cualquier columna de clasificación de etiquetas del informe. En su lugar, utilice el [Informe de clasificación de etiquetas](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Problemas generales de datos

+++Los informes generados mediante diferentes reglas de atribución muestran totales diferentes.
Si genera un informe varias veces utilizando los mismos parámetros de informe pero con reglas de atribución diferentes, los datos pueden diferir por cualquiera de los siguientes motivos:

* Los datos basados en fechas de clic pueden encontrarse fuera del intervalo de fechas especificado.

  Si utiliza el parámetro de informe &quot;[!UICONTROL Conversions based on click date],&quot; entonces el intervalo de fechas especificado se aplica a la fecha del clic en lugar de a la fecha de la transacción. Si el informe también utiliza la regla de atribución &quot;Primer evento&quot; o &quot;Último evento&quot;, el primer o el último evento que provocó la conversión pueden estar fuera del intervalo de fechas especificado. Por ejemplo, supongamos que un usuario hace clic en Palabra clave_1 el 30 de abril, en Palabra clave_2 el 20 de mayo y se convierte el 21 de mayo. Si el informe utiliza el operador &quot;[!UICONTROL First Event]&quot; regla de atribución y un intervalo de fechas del 1 al 21 de mayo, el primer evento (un clic en Keyword_1 el 30 de abril) no se incluye en el informe. Si ejecuta el informe con el mismo intervalo de fechas pero utilizando la variable &quot;[!UICONTROL Last Event]&quot; regla de atribución, la conversión se incluye en el informe porque el último clic se produjo dentro del intervalo de fechas especificado.

* La selección del filtro de portafolio excluye algunos de los eventos que llevaron a la conversión.

  Si crea informes sobre un subconjunto de portafolios, es posible que no incluya las campañas que incluyeron el evento al que se atribuyó la conversión en una de las reglas de atribución. Por ejemplo, supongamos que un usuario hace clic en Palabra clave_1 en Portfolio_1, hace clic en Palabra clave_2 en Portfolio_2 y, a continuación, convierte. Si el informe utiliza el operador &quot;[!UICONTROL First Event]&quot; regla de atribución, entonces Portfolio_1 debe incluirse para que la conversión se incluya en el informe. Sin embargo, si el informe utiliza la regla de atribución &quot;Último evento&quot;, se debe incluir Portfolio_2.

>[!TIP]
>
>Si desea comparar los totales de conversión con reglas de atribución diferentes, ejecute los informes con el parámetro de informe &quot;[!UICONTROL Conversions based on transaction date]&quot; y seleccione todas las redes de anuncios o todos los portafolios. Si no establece otros filtros, los totales de conversión deben coincidir.

+++

+++Los campos de datos individuales son incorrectos, aunque los totales son correctos.
Esta situación se puede producir cuando los formatos de métrica utilizan enteros:

* Si crea un [métrica personalizada](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) con el formato *Número sin decimales* (que muestra los datos como números enteros) y se incluyen en una vista o un informe que usa una regla de atribución de conversión ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], o [!UICONTROL Even Distribution]), el resultado se mostrará en números enteros, no en decimales. En este caso, los campos de datos individuales pueden ser incorrectos, aunque los totales son correctos. Por ejemplo, si un pedido se divide a partes iguales entre tres eventos, se atribuye a cada uno de los tres eventos un pedido (en lugar de un pedido de 0,33). Para resolver el problema, [cambio del formato de la métrica](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) hasta *Número a 2 puntos decimales*.

* Del mismo modo, si tiene una métrica de ingresos que se envía como en entero, se produce el mismo problema. (El formato de ingresos se controla mediante la etiqueta de conversión que envía los datos). Para resolver el problema, [crear una métrica personalizada](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) consiste únicamente en la métrica de ingresos y con el formato *Número a 2 puntos decimales*e inclúyala en vistas e informes en lugar de en la métrica original.
+++

+++Cuando faltan datos de clics o ingresos, ¿cómo puedo evitar que afecten a ofertas futuras?
Los problemas de datos de clics se producen cuando Search, Social y Commerce no están sincronizados con la red de anuncios. Póngase en contacto con el equipo de cuenta de Adobe para sincronizar manualmente la cuenta. Si faltan datos de clics para un día completo, pida al equipo de cuenta de Adobe que excluya ese día de los modelos de coste.

Pueden producirse problemas en los datos de ingresos debido a un problema con el archivo de seguimiento o de fuente. Póngase en contacto con el equipo de cuenta de Adobe para investigar el problema. Si faltan datos de ingresos para un día entero, pida al equipo de cuenta de Adobes que excluya ese día de los modelos de ingresos.
+++

+++Los datos monetarios se muestran en un formato incorrecto.
De forma predeterminada, todos los datos monetarios de los informes se muestran en formato de dólares estadounidenses (por ejemplo, 1000,00). Para mostrar el valor en el formato de moneda correcto (pero sin símbolos de moneda en los formatos CSV y TSV), agregue el símbolo &quot;[!UICONTROL Currency]&quot; al informe. Si el informe incluye datos de cuentas con distintas monedas, cualquier &quot;[!UICONTROL Total]&quot; los valores monetarios son simplemente la suma de todos los números de la columna, independientemente de la moneda.
+++

+++¿Por qué veo valores decimales para una métrica de conversión que debería ser un número natural (1, 2, etc.)?
Puede ver valores decimales en los siguientes casos:

* Si ejecutó el informe utilizando cualquier parámetro de regla de atribución de conversión distinto de [!UICONTROL Last Event] o [!UICONTROL First Event], los ingresos se pueden dividir entre varios eventos en la ruta de conversión.

* En el [!UICONTROL Transaction Report], si hay varios [unidades de oferta](/help/search-social-commerce/glossary.md#a-b) Con tipos de coincidencia diferentes que tienen el mismo ID de transacción, los ingresos del ID de seguimiento se dividen según el número de clics en la fecha de clic especificada.
+++

## Métricas de rendimiento estándar

+++Faltan datos de clics en los informes.
Las siguientes son razones comunes para la falta de datos sobre clics.

| Causa | Detección/análisis | Resolución |
|---|---|---|
| Error en el proceso que recupera los datos de clics de la cuenta de publicidad. | No hay una forma sistemática de detectar este problema, pero es posible que observe que una campaña no muestra información de coste o clics aunque la cuenta de publicidad gastó dinero. | Póngase en contacto con el equipo de cuenta de Adobe.<br><br>Si faltan datos durante más de 24 horas, excluya esas fechas de las previsiones de costes hasta que se recuperen los datos. El equipo de cuenta de Adobe puede excluir las fechas. |
| Un problema de facturación entre el anunciante y la red de anuncios impide que la cuenta de publicidad gaste. | No hay una forma sistemática de detectar este problema, pero puede observar que una campaña no muestra información sobre costos o clics. | Si sabe que una cuenta publicitaria no pudo gastar debido a un problema de facturación, excluya esas fechas de las previsiones de costes. El equipo de cuenta de Adobe puede excluir las fechas. |
+++

+++Los datos de rendimiento son diferentes de los datos del editor de red de publicidad.
Cuando la red de anuncios envía actualizaciones a datos anteriores (a menudo porque han atribuido un fraude de clics a algunos clics), Search, Social y Commerce no actualiza los datos a menos que haya más de un 5 % de discrepancia y el equipo de la cuenta de Adobe presente una solicitud.

Además, cuando compara datos de uso compartido de impresiones agregados en un intervalo de fechas, los datos de los informes Buscar, Social y Commerce pueden diferir de los datos de los informes de la red de anuncios. Esta diferencia se debe a la forma en que la API de la red de publicidad informa los datos, que Search, Social y Commerce utiliza para extraer los datos. Por ejemplo, para [!DNL Google Ads] datos:

* Para la mayoría de las métricas de cuota de impresiones, [!DNL Google Ads] limita el extremo inferior o superior de los valores notificados para valores inferiores al 10 % o superiores al 90 %. Los datos se presentan como 0,0999 para &lt;10% y 0,9001 para >90%

* Cuando hay una combinación de datos restringidos y no restringidos dentro del intervalo de fechas, Buscar, Social y Commerce agregan datos de uso compartido de impresiones utilizando los valores enviados en la API tal cual, con 0,0999 para filas con &lt;10% y 0,9001 para filas con >90%. Esta agregación podría provocar una desviación del [!DNL Google Ads] datos preagregados porque [!DNL Google Ads] puede utilizar valores de porcentaje reales, como 7 % o 97 %.
+++

+++Los datos de rendimiento de los informes son diferentes de los de [!DNL Google Analytics].
Los dos sistemas miden datos diferentes, por lo que debería esperar ver datos diferentes. Por ejemplo:

* Search, Social y Commerce (y Google Ads) rastrean clics, mientras que [!DNL Google Analytics] registra las visitas por sesión de explorador de 30 minutos. Por ejemplo, si un usuario hace clic en el anuncio una vez, hace clic en el botón Atrás y, a continuación, hace clic de nuevo en el anuncio, Buscar, Social y Commerce registra dos clics, pero [!DNL Google Analytics] registra una visita.

* [!DNL Google Analytics] muestra todos los datos de tráfico, mientras que Search, Social y Commerce (y [!DNL Google Ads]) filtra los clics no válidos (como clics excesivos y repetidos).

* [!DNL Google Analytics] incluye datos de clics e ingresos de todos los clics. Search, Social y Commerce no pueden rastrear los datos de clics e ingresos de anuncios y palabras clave con direcciones URL de seguimiento incorrectas o que faltan.
+++

## Métricas de conversión

+++Mi informe no muestra datos de conversión.
Es posible que el informe no incluya métricas de conversión para las que se hayan producido conversiones.
+++

+++Faltan ingresos en los informes.

**Anunciantes que usan etiquetas de conversión de Adobe Advertising**

*Posibles causas:*

* Las palabras clave o los anuncios se han agregado sin anteponer el prefijo de rastreo de clics de Search, Social y Commerce a las plantillas de rastreo o a las URL de destino, o bien el prefijo de rastreo es incorrecto.

* La etiqueta de seguimiento de conversión no se ha implementado correctamente en todas las páginas web aplicables o se ha editado.

* Las métricas de conversión de las que realiza el seguimiento de Search, Social y Commerce se excluyen de los informes y, por lo tanto, no son visibles.

* No se ha implementado el analizador de ingresos para el cliente.

*Posible solución o solución alternativa:*

1. Compruebe que se incluyen las columnas correctas en los informes o en las vistas de datos. Si no se pueden agregar las columnas correctas, usted o su equipo de cuenta de Adobe deben [poner las métricas de conversión a disposición de los informes](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Compruebe que las etiquetas de seguimiento de conversión correctas están implementadas en todas las páginas web aplicables. Si es necesario, pídale al equipo de cuenta de Adobe que cree una transacción de prueba para cada etiqueta de seguimiento de conversión aplicable y que capture los detalles de la transacción, como la `transactionid` y detalles de la cookie (como la `trackingid`, `clickid`, etc.).

1. Si la variable [!UICONTROL Auto Upload] Esta opción está desactivada para la campaña y has añadido palabras clave o anuncios. A continuación, asegúrate de haber creado una plantilla de seguimiento o una URL de destino que incluya el rastreo de clics de Search, Social y Commerce para cada una. El equipo de cuenta de Adobe puede ejecutar un informe interno para ver si faltan direcciones URL de rastreo de clics (plantillas de seguimiento o direcciones URL de destino) o si tienen un formato incorrecto.

   Si es necesario, genere el seguimiento creando un archivo de hoja de edición masiva con las direcciones URL correctas y publique el archivo en la cuenta correspondiente utilizando **Generar URL de seguimiento** opción.

   La dirección URL de destino debe comenzar por &quot;http://pixel.everesttech.net&quot; o &quot;https://pixel.everesttech.net&quot;.

1. Si ninguno de estos pasos resuelve el problema, [Contactar con Atención al cliente](/help/search-social-commerce/get-help.md).

   Si el cliente no se ha iniciado o es nuevo, el Servicio de atención al cliente comprueba si se ha configurado un analizador de ingresos. Si el analizador está configurado, comprueba si Search, Social y Commerce están recibiendo conversiones de píxeles y soluciona el problema.

**Anunciantes que envían fuentes de datos de conversión**

*Posibles causas:*

* El archivo de fuente no se ha entregado, no se ha analizado completamente o la fuente contenía transacciones huérfanas.

* Las métricas de conversión relevantes se excluyen de los informes y, por lo tanto, no son visibles.

>[!NOTE]
>
>Por lo general, los datos no aparecen en la interfaz de usuario hasta 2 a 4 horas después de recibir la fuente.

*Posible solución o solución alternativa:*

1. Compruebe que se incluyen las columnas correctas en los informes o en las vistas de datos. Si no se pueden agregar las columnas correctas, usted o su equipo de cuenta de Adobe deben [poner las métricas de conversión a disposición de los informes](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Ejecute el [!UICONTROL Portfolio Report]. Si está vacío, ejecute el [!UICONTROL Campaign Report] y [!UICONTROL Search Engine Report] para ver si los ingresos aparecen en esos informes. Si es así, es posible que las campañas no se asignen al portafolio adecuado.

1. Compruebe que el archivo se ha enviado al servidor de ingresos y que el archivo sigue el mismo formato y convención de nomenclatura de archivos que los archivos anteriores.

   Si el formato o la convención de nomenclatura de archivos ha cambiado, corrija el archivo y vuelva a enviarlo.

1. Si se envió el archivo, [Contactar con Atención al cliente](/help/search-social-commerce/get-help.md).

   El Servicio de atención al cliente comprobará si el archivo se ha recibido y analizado. Si el archivo se ha procesado sin errores, comprueba si hay transacciones huérfanas.
+++

+++Algunos informes avanzados no incluyen los datos de conversión proporcionados por una fuente del anunciante.
El [!UICONTROL Geo Distribution Report] y [!UICONTROL Domain Referral Report] utilice los datos capturados mediante el servicio de seguimiento de conversión de Adobe Advertising y solo se pueden generar para anunciantes con el servicio. Los informes no incluyen datos de conversión rastreados fuera del sistema de seguimiento de conversiones de Adobe Advertising.
+++

+++Los datos de ingresos son diferentes de los datos de ingresos propios del anunciante.

**Anunciantes que usan etiquetas de conversión de Adobe Advertising**

*Posibles causas:*

* Search, Social y Commerce no tienen en cuenta los ingresos cuando la cookie caduca o se elimina, pero el anunciante puede considerarla una ganancia válida.

* El tráfico a la página del anunciante provino de un marcador o una búsqueda orgánica en lugar de un anuncio.

* La etiqueta de seguimiento de conversión no se ha implementado correctamente en todas las páginas web aplicables o se ha editado.

*Posible solución o solución alternativa:*

1. Ir a **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** y generar un [!UICONTROL Transaction Report]. Compare las transacciones que Search, Social y Commerce recibieron con los datos del anunciante.

1. Si algunas transacciones son incorrectas o faltan, asegúrese de que la etiqueta de seguimiento de conversión correspondiente esté implementada en todas las páginas web aplicables y no se haya editado a menos que el equipo de cuenta de Adobe le haya recomendado hacerlo. Puede que falte una etiqueta o que se haya cambiado si el sitio web se ha actualizado recientemente.

   Search, Social y Commerce esperan direcciones URL bien formadas (con parámetros en pares de nombre-valor) dentro de `ef_transaction_properties` y dentro de la variable `src` elemento de la `img` etiqueta.

1. Si no puede determinar y resolver el problema, [Contactar con Atención al cliente](/help/search-social-commerce/get-help.md).

   El Servicio de atención al cliente intentará identificar las transacciones que faltan y, a continuación, comprobar si hay transacciones huérfanas y transacciones que no proceden de un anuncio (&quot;conversiones no correlacionadas&quot;).

**Anunciantes con fuentes de datos de conversión que utilizan `ef_id` values**

Consulte las posibles causas y soluciones para implementaciones de píxeles más arriba.

**Anunciantes con fuentes de datos de conversión que utilizan ID de transacción**

*Posibles causas:*

* Search, Social y Commerce no tienen en cuenta los ingresos cuando la cookie caduca o se elimina, pero el anunciante puede considerarla una ganancia válida.

* El tráfico a la página del anunciante provino de un marcador o una búsqueda orgánica en lugar de un anuncio.

* Se informó de una conversión sin conexión antes de que se produjera una transacción en línea con el mismo ID de transacción. La transacción en línea debe realizarse primero.

*Posible solución o solución alternativa:*

1. Ir a **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** y generar un [!UICONTROL Transaction Report]. Compare las transacciones que Search, Social y Commerce recibieron con los datos de fuentes del anunciante.

1. Si falta una transacción en el archivo de fuente en el informe, compruebe si se ha producido una transacción en línea con el mismo ID de transacción (rastreado mediante el píxel) antes de la conversión sin conexión.

1. Si no puede determinar y resolver el problema, [Contactar con Atención al cliente](/help/search-social-commerce/get-help.md).

   El Servicio de atención al cliente comprobará si hay errores de análisis de datos y [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p).

**Anunciantes con otros tipos de fuentes de datos de conversión**

*Posibles causas:*

* Search, Social y Commerce no tienen en cuenta los ingresos cuando la cookie caduca o se elimina, pero el anunciante puede considerarla una ganancia válida.

* El tráfico a la página del anunciante provino de un marcador o una búsqueda orgánica en lugar de un anuncio.

* No hay [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p), por lo que Search, Social y Commerce no cuentan todos los ingresos que deberían.

* El anunciante validó un informe de Search, Social y Commerce con un conjunto de datos diferente al que envió en la fuente.

* Los ID de transacción (`ev_transid` valores) no se han enviado, no son únicos o son incorrectos.

* El archivo de fuente contiene ID de seguimiento duplicados.

* Se han producido errores al analizar el archivo.

* La lógica de deduplicación del anunciante difiere de la lógica de búsqueda, social y Commerce.

*Posible solución o solución alternativa:*

1. Ir a **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** y generar un [!UICONTROL Transaction Report]. Compare las transacciones que Search, Social y Commerce recibieron con los datos del anunciante.

1. Si algunas transacciones son incorrectas o faltan, asegúrese de que a) el archivo de fuente contenga todos los ID de transacción necesarios y no haya ID de seguimiento duplicados y b) los ID de transacción sean únicos y correctos.

1. Si no puede determinar y resolver el problema, [Contactar con Atención al cliente](/help/search-social-commerce/get-help.md).

   El Servicio de atención al cliente comprobará si hay errores de análisis de datos y transacciones huérfanas.
+++

+++Los datos de ingresos son diferentes de los datos de Adobe Analytics Consulte [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Informes específicos

+++Si la variable [!UICONTROL Portfolio Report] mostrar las mismas cifras que la variable [!UICONTROL Portfolios] ¿Ver?
El [!UICONTROL Portfolio Report] y el [!UICONTROL Portfolios] vista muestra los mismos datos cuando todos los filtros de la vista, los parámetros del informe y las columnas de datos de la vista y el informe son iguales. Por ejemplo, si la variable [!UICONTROL Portfolios] La vista muestra los portafolios que son &quot;[!UICONTROL All but inactive]&quot; para el intervalo de fechas &quot;[!UICONTROL Last 7 days]&quot; y solo se muestran las columnas de datos predeterminadas y, a continuación, un [!UICONTROL Portfolio Report] el uso de los parámetros predeterminados muestra datos idénticos. Si cambia cualquiera de los parámetros del informe o utiliza diferentes filtros en la variable [!UICONTROL Portfolios] vista, los valores de los datos pueden ser diferentes.
+++

+++Los datos de mi [!UICONTROL Portfolio Report] no coincide con los datos de mi [!UICONTROL Search Engine Report] o [!UICONTROL Search Engine Account Report].
El [!UICONTROL Portfolio Report] muestra datos solo para las campañas asignadas a los portafolios especificados, pero la variable [!UICONTROL Search Engine Report] y [!UICONTROL Search Engine Account Report] también puede incluir datos de campañas que no están asignadas a un portafolio.
+++

+++¿Cómo está el [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] diferente del nivel de portafolio [!UICONTROL Model Accuracy Report]?
(Solo el administrador de cuentas de agencia, el administrador de cuentas de Adobe y los usuarios administradores) La [!UICONTROL Forecast Accuracy Report] disponible desde [!UICONTROL Reports] > [!UICONTROL Model Accuracy] proporciona los mismos datos que el nivel de portafolio [!UICONTROL Model Accuracy Report] excepto que puede ejecutarlo en varios portafolios y puede cambiar la regla de atribución. También puede ejecutar y programar el informe utilizando parámetros personalizados, y puede utilizarlo para crear fuentes de hoja de cálculo. Además, la variable [!UICONTROL Forecast Accuracy Report] es más preciso que el informe a nivel de portafolio heredado, ya que evalúa la precisión de los ingresos utilizando los objetivos históricos para el portafolio en lugar del objetivo actual y representa con mayor precisión los datos para el huso horario aplicable.
+++

+++Los datos a nivel de anuncio no están disponibles para [!DNL Google Ads] anuncio de búsqueda dinámica (DSA), rendimiento máximo, compras inteligentes y [!DNL YouTube] campañas.
Las redes de anuncios no proporcionan el identificador necesario para atribuir ingresos a un anuncio individual para esas campañas. Por lo tanto, los datos de rendimiento de nivel de anuncio no están disponibles para esos tipos de campaña en la [!UICONTROL Ads] ver o en la [!UICONTROL Ad Variation Report]. Se esperan discrepancias entre el total de datos de nivel de anuncio de una campaña y el total de datos de la campaña.
+++

+++En el [!UICONTROL Transaction Report]Sin embargo, ¿cómo sé qué métrica de conversión es de una fuente de datos o se rastrea con el píxel de seguimiento de Adobe Advertising?
En un informe de transacciones, puede saber si el píxel de seguimiento de Adobe Advertising ha rastreado una métrica de conversión incluida si incluye la columna personalizada &quot;[!UICONTROL Tracking URL].&quot; Las direcciones URL de seguimiento con el píxel de seguimiento de Adobe Advertising comienzan por &quot;`http://pixel.everesttech.net`.&quot;
+++

+++Los datos de mi [!UICONTROL Transaction Report] no coincide con los datos de mi [!UICONTROL Keyword Report].
Cuando se generan ambos informes por portafolio, los datos son diferentes si se genera el [!UICONTROL Keyword Report] usar datos históricos (es decir, basados en la configuración del portafolio durante las fechas especificadas) en lugar de usar datos para las campañas actuales. Cuando genere el [!UICONTROL Transaction Report] por portafolio, incluye datos de las campañas actuales del portafolio.
+++

## Fuentes de hoja de cálculo

+++La salida del informe incluye una combinación de intervalos de fechas.
Puede ver diferentes intervalos de fechas si la fuente agrega datos con cualquier nivel de agregación de datos distinto de &quot;[!UICONTROL Daily].&quot;

Para resolver el problema, actualice la fuente de la hoja de cálculo para incluir los datos agregados diariamente. Esta tarea incluye actualizar la plantilla del informe, generar un informe con la plantilla y crear un personalizado [!DNL Microsoft Excel] plantilla mediante el informe y, a continuación, actualizando la configuración de fuente para incluir la nueva plantilla de Excel. Para obtener más información, consulte &quot;[Editar configuración de fuente de informes de hoja de cálculo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++Una fuente de hoja de cálculo provoca un error interno.
Este error puede producirse si cambia las columnas en la plantilla de informe pero no actualiza la variable [!DNL Microsoft Excel] plantilla en consecuencia.

Para resolver el problema, actualice la fuente de la hoja de cálculo para incluir las columnas nuevas. Esta tarea incluye actualizar la plantilla del informe, generar un informe con la plantilla y crear un personalizado [!DNL Excel] plantilla mediante el informe y, a continuación, actualizando la configuración de fuente para incluir la nueva plantilla de Excel. Para obtener más información, consulte &quot;[Editar configuración de fuente de informes de hoja de cálculo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++Cuando intento abrir una fuente de hoja de cálculo en [!DNL Excel], [!DNL Excel] informa de un error de &quot;contenido ilegible&quot; y los datos se eliminan del contenido recuperado.
Si la variable [!DNL Microsoft Excel] La plantilla no ordena los datos por fecha de inicio en orden ascendente, la fuente de la hoja de cálculo puede incluir filas en blanco. En particular, [!DNL Excel] informa del error &quot;Excel ha encontrado contenido ilegible en &#39;&lt;*nombre del informe*>.xlsx.&#39; ¿Desea recuperar el contenido del libro? Si confía en el origen de este libro, haga clic en sí.&quot; Si hace clic en &quot;Sí&quot;, recibe el siguiente mensaje: &quot;Registros eliminados: Información de celda de la parte /xl/worksheets/sheet1.xml&quot; y la fuente de la hoja de cálculo incluye filas en blanco.

Para resolver el problema, edite el [!DNL Excel] plantilla asociada a la fuente por la que ordenar los datos [!DNL Start date in Ascending (Oldest to Newest) order]y, a continuación, cargue la plantilla actualizada a través de la configuración de fuentes de hoja de cálculo. Para obtener más información, consulte &quot;[Editar fuentes de informes de hoja de cálculo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++
