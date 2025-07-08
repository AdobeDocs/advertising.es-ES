---
title: Cálculo de las reglas de atribución
description: Descubra cómo Adobe Advertising calcula cada tipo de regla de atribución.
exl-id: 15beeadd-bb65-4efe-8c4f-34c4a48cc775
feature: Search Reports
source-git-commit: b24673e05f95bac404301d71ad9c0d1d0593aafb
workflow-type: tm+mt
source-wordcount: '2716'
ht-degree: 0%

---

# Cálculo de las reglas de atribución para Adobe Advertising

*Anunciantes con solo seguimiento de conversión de Adobe Advertising*

<!-- Verify statements about cross-device events -->

La regla de atribución de nivel de anunciante se utiliza para atribuir datos de conversión (potencialmente en varios canales de publicidad) en una serie de eventos que conducen a una conversión.

En los informes, las vistas predeterminadas y personalizadas para Advertising Search, Social y Commerce (Buscar, Social y Commerce), así como (algunas funciones de usuario) las simulaciones de nivel de portafolio para Search, Social y Commerce, la regla seleccionada solo se utiliza para los datos de vista, informe o simulación. Las distintas reglas de atribución se aplican de la siguiente manera.

>[!NOTE]
>
>* Las reglas de atribución se aplican a los clics en anuncios pagados en cualquier canal y a las impresiones en pantallas y anuncios sociales. No se aplican a las impresiones de anuncios de búsqueda de pago, que no se pueden rastrear en el nivel de evento.
>* Adobe Advertising siempre almacena los siguientes eventos para cada internauta antes de una conversión: a) el primer clic de pago; b) hasta 10 clics para cada canal (búsqueda, red social o visualización), incluido el primer clic; y c) hasta 10 impresiones de visualización.<!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
>* En Advertising DSP y Advertising Creative, las definiciones entre dispositivos solo tienen en cuenta la ruta de acceso del evento de la regla de atribución seleccionada.<!-- cross-device attribution via LiveRamp only -->
>* En las vistas de informes y administración, el número de decimales que se muestran para un valor depende de la moneda, pero Adobe Advertising almacena valores más precisos.

## Último evento (valor predeterminado)

Atribuye la conversión al último clic de pago de la serie dentro de la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante o, si no se produjeron clics de pago, a la última impresión dentro de la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j) del anunciante.

Cuando la conversión solo va precedida de impresiones, la conversión se considera una *visualización*, que se pondera según la [configuración de ponderación de visualización del anunciante](/help/search-social-commerce/glossary.md#uv) o, como se especifique, según el método de valoración de visualización especificado en los parámetros de informe, vista o simulación personalizada.

![Últimos porcentajes de atribución de eventos](/help/search-social-commerce/assets/attribution-percent-last-event.png "Últimos porcentajes de atribución de eventos")

<!-- start examples as collapsible content -->

+++Ejemplos de cálculos de eventos

### Ejemplo con todos los clics

Ruta del evento: Click1, Click2, Click3, Conversión de 120 USD

La conversión se atribuye a Click 3 por un importe de 120 USD.

### Ejemplo con impresiones y clics

**Nota:** Las impresiones solo se aplican a partir de anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, clic 1, impresión 2, conversión de 120 USD

La conversión se atribuye a Click 1 por un importe de 120 USD.

### Ejemplo con todas las impresiones

**Nota:** Solo son aplicables las impresiones para anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, impresión 2, impresión 3, conversión de 120 USD

La conversión se atribuye a la impresión 3. Como la conversión es una visualización, se aplica el método de valoración de visualización seleccionado en la sección &quot;Atribución de conversión&quot; de la configuración del informe:

* Si el parámetro de informe especifica una ponderación de visualización ponderada, dicha ponderación se aplicará a la visualización. Por ejemplo, si la ponderación de visualización del anunciante es del 40 %, entonces 120 USD x 40 % = 48 USD, por lo que 48 USD se atribuye a la impresión 3.

* Si el parámetro de informe especifica el uso de valores sin procesar para las visualizaciones, no se aplica ninguna ponderación de visualización y los 120 USD completos se atribuyen a la impresión 3.

+++

<!-- end examples as collapsible content -->

## Primer evento

Atribuye la conversión al primer clic de pago de la serie dentro de la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante o, si no se produjeron clics de pago, a la primera impresión dentro de la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j) del anunciante. Esta regla solo está disponible para eventos de entre dispositivos únicos.

Cuando la conversión solo va precedida de impresiones, la conversión se considera una *visualización*, que se pondera según la [configuración de ponderación de visualización](/help/search-social-commerce/glossary.md#uv) del anunciante o, como se especifique, según el método de valoración de visualización especificado en los parámetros de informe, vista o simulación personalizada.

![Porcentajes de atribución del primer evento](/help/search-social-commerce/assets/attribution-percent-first-event.png "Porcentajes de atribución del primer evento")

<!-- start examples as collapsible content -->

+++Ejemplos de cálculos de eventos

### Ejemplo con todos los clics

Ruta del evento: Haga clic en 1, Haga clic en 2, Haga clic en 3, Conversión de 120 USD

La conversión se atribuye a Click 1 por un importe de 120 USD.

### Ejemplo con impresiones y clics

**Nota:** Las impresiones solo se aplican a partir de anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, clic 1, impresión 2, conversión de 120 USD

La conversión se atribuye a Click 1 por un importe de 120 USD.

### Ejemplo con todas las impresiones

**Nota:** Solo son aplicables las impresiones para anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, impresión 2, impresión 3, conversión de 120 USD

La conversión se atribuye a la impresión 1. Como la conversión es una visualización, el método de valoración de visualización seleccionado en la Conversión &quot;(Mostrar campañas)
Se aplica la sección &quot;Atribución&quot; de la configuración del informe:

* Si el parámetro de informe especifica una ponderación de visualización ponderada, dicha ponderación se aplicará a la visualización. Por ejemplo, si la ponderación de visualización del anunciante es del 40 %, entonces 120 x 40 % = 48 USD, por lo que 48 USD se atribuye a la impresión 1.

* Si el parámetro de informe especifica el uso de valores sin procesar para las visualizaciones, no se aplica ninguna ponderación de visualización y los 120 USD completos se atribuyen a la impresión 1.

+++

<!-- end examples as collapsible content -->

## Peso Primer evento Más

Atribuye la conversión a todos los eventos de la serie que se produjeron en la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j), pero otorga el mayor peso al primer evento y sucesivamente menos peso a los siguientes eventos. Esta regla solo está disponible para eventos en dispositivos únicos.

Cuando la conversión solo va precedida de impresiones, la conversión se considera una *visualización*, que se pondera según la [configuración de ponderación de visualización](/help/search-social-commerce/glossary.md#uv) del anunciante o, como se especifique, según el método de valoración de visualización especificado en los parámetros de informe, vista o simulación personalizada.

Cuando la ruta de conversión incluye clics de pago e impresiones, los distintos productos de Adobe Advertising tratan las impresiones de forma diferente:

* En Search, Social y Commerce, la ponderación de anulación de impresión [print ](/help/search-social-commerce/glossary.md#i-j), que se especifica en la configuración de ponderación de anulación de impresión del anunciante y en los parámetros de informe, vista o simulación personalizada, se aplica primero a las impresiones.

* En DSP, las impresiones se ignoran y solo se ponderan los clics. DSP no tiene en cuenta las ponderaciones de anulación de impresiones para la atribución.

![Peso del primer evento más porcentajes de atribución](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Peso del primer evento más porcentajes de atribución")

<!-- start examples as collapsible content -->

+++Ejemplos de cálculos de eventos

### Ejemplo con todos los clics

Ruta del evento: Haga clic en 1, Haga clic en 2, Haga clic en 3, Conversión de 120 USD

Atribución: Haga clic 1 = 60 USD, Haga clic 2 = 40 USD, Haga clic 3 = 20 USD (120 USD en total)

### Ejemplos con impresiones y clics

**Nota:** Las impresiones solo se aplican a partir de anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, clic 1, impresión 2, clic 2, conversión de 120 USD

#### (Solo búsqueda, medios sociales y Commerce) Uso del 10 % como &quot;Peso de anulación de impresión&quot; predeterminado

Como la serie de eventos incluye impresiones y clics, el peso de anulación de impresión se aplica a las impresiones.

Atribución: impresión 1 = 8 USD, clic 1 = 72 USD, impresión 2 = 4 USD, clic 2 = 36 USD (120 USD en total)

#### Uso (solo DSP) de una ponderación de anulación de impresión o (solo Search, Social y Commerce) de una &quot;ponderación de anulación de impresión&quot; del 0 %

Como la serie de eventos incluye impresiones y clics, estas se omiten.

Atribución: impresión 1 = 0 USD, clic 1 = 80 USD, impresión 2 = 0 USD, clic 2 = 40 USD (120 USD en total)

### Ejemplo con todas las impresiones

**Nota:** Solo se aplican impresiones para anuncios en pantalla.

Ruta del evento: impresión 1, impresión 2, impresión 3, conversión de 120 USD

Dado que la conversión es una visualización, se aplica el método de valoración de la visualización, en lugar del peso de anulación de la impresión, para determinar el valor de cada impresión:

* Si el parámetro de informe especifica una ponderación de visualizaciones ponderada, dicha ponderación se aplicará a los valores de impresión. Por ejemplo, si la ponderación de visualizaciones es del 40 %, entonces Impresión 1 = 24 USD, Impresión 2 = 16 USD, Impresión 3 = 8 USD (48 USD en total)

* Si el parámetro de informe especifica el uso de valores sin procesar para las visualizaciones, no se aplica ninguna ponderación de visualización a la impresión y se divide el valor completo de 120 USD entre las tres impresiones: Impresión 1 = 60 USD, Impresión 2 = 40 USD, Impresión 3 = 20 USD (120 USD en total)

+++

<!-- end examples as collapsible content -->

## Distribución par

>[!NOTE]
>
>Esta regla solo está disponible para eventos de entre dispositivos únicos.

Atribuye la conversión de forma equitativa a cada evento de la serie que se produjo en la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j).

Cuando la conversión solo va precedida de impresiones, la conversión se considera una *visualización*, que se pondera según la [configuración de ponderación de visualización](/help/search-social-commerce/glossary.md#uv) del anunciante o, como se especifique, según el método de valoración de visualización especificado en los parámetros de informe, vista o simulación personalizada.

Cuando la ruta de conversión incluye clics de pago e impresiones, los distintos productos de Adobe Advertising tratan las impresiones de forma diferente:

* En Search, Social y Commerce, la ponderación de anulación de impresión [print ](/help/search-social-commerce/glossary.md#i-j), que se especifica en la configuración de ponderación de anulación de impresión del anunciante y en los parámetros de informe, vista o simulación personalizada, se aplica primero a las impresiones.

* En DSP, las impresiones se ignoran y solo se ponderan los clics. DSP no tiene en cuenta las ponderaciones de anulación de impresiones para la atribución.

![Porcentajes de atribución par](/help/search-social-commerce/assets/attribution-percent-even.png "Porcentajes de atribución par")

<!-- start examples as collapsible content -->

+++Ejemplos de cálculos de eventos

### Ejemplo con todos los clics

Ruta del evento: Haga clic en 1, Haga clic en 2, Haga clic en 3, Conversión de 120 USD

Ninguna impresión provocó la conversión, por lo que el peso de anulación de la impresión no es aplicable y la conversión se divide a partes iguales entre los tres clics:

Atribución: Haga clic 1 = 40 USD, Haga clic 2 = 40 USD, Haga clic 3 = 40 USD (120 USD en total)

### Ejemplos con impresiones y clics

**Nota:** Las impresiones solo se aplican a partir de anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, clic 1, impresión 2, clic 2, conversión de 120 USD

#### (Solo búsqueda, medios sociales y Commerce) Uso del 10 % como &quot;Peso de anulación de impresión&quot; predeterminado

Como la serie de eventos incluye impresiones y clics, el peso de anulación de impresión se aplica a las impresiones.

Atribución: impresión 1 = 6 USD, clic 1 = 54 USD, impresión 2 = 6 USD, clic 2 = 54 USD (120 USD en total)

#### Uso (solo Adobe Advertising DSP) de una ponderación de anulación de impresión o (solo Search, Social y Commerce) de una &quot;ponderación de anulación de impresión&quot; del 0 %

Como la serie de eventos incluye impresiones y clics, estas se omiten.

Atribución: impresión 1 = 0 USD, clic 1 = 60 USD, impresión 2 = 0 USD, clic 2 = 60 USD (120 USD en total)

## Ejemplo con todas las impresiones

**Nota:** Solo se aplican impresiones para anuncios en pantalla.

Ruta del evento: impresión 1, impresión 2, impresión 3, conversión de 120 USD

Dado que la conversión es una visualización, se aplica el método de valoración de la visualización, en lugar del peso de anulación de la impresión, para determinar el valor de cada impresión:

* Si el parámetro de informe especifica una ponderación de visualizaciones ponderada, dicha ponderación se aplicará a los valores de impresión. Por ejemplo, si la ponderación de visualizaciones es del 40 %, entonces Impresión 1 = 16 USD, Impresión 2 = 16 USD, Impresión 3 = 16 USD (48 USD en total)

* Si el parámetro de informe especifica el uso de valores sin procesar para las visualizaciones, no se aplica ninguna ponderación de visualización a la impresión y se divide el valor completo de 120 USD entre las tres impresiones: Impresión 1 = 40 USD, Impresión 2 = 40 USD, Impresión 3 = 40 USD (120 USD en total)

+++

<!-- end examples as collapsible content -->

## Peso Último evento Más

Atribuye la conversión a todos los eventos de la serie que se produjeron en la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j), pero otorga el mayor peso al último evento y sucesivamente menos peso a los eventos anteriores.

Cuando la conversión solo va precedida de impresiones, la conversión se considera una *visualización*, que se pondera según la [configuración de ponderación de visualización](/help/search-social-commerce/glossary.md#uv) del anunciante o, como se especifique, según el método de valoración de visualización especificado en los parámetros de informe, vista o simulación personalizada.

Cuando la ruta de conversión incluye clics de pago e impresiones, los distintos productos de Adobe Advertising tratan las impresiones de forma diferente:

* En Search, Social y Commerce, la ponderación de anulación de impresión [print ](/help/search-social-commerce/glossary.md#i-j), que se especifica en la configuración de ponderación de anulación de impresión del anunciante y en los parámetros de informe, vista o simulación personalizada, se aplica primero a las impresiones.

* En DSP, las impresiones se ignoran y solo se ponderan los clics. DSP no tiene en cuenta las ponderaciones de anulación de impresiones para la atribución.

![Peso del último evento más porcentajes de atribución](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Peso del último evento más porcentajes de atribución")

<!-- start examples as collapsible content -->

+++Ejemplos de cálculos de eventos

### Ejemplo con todos los clics

Ruta del evento: Haga clic en 1, Haga clic en 2, Haga clic en 3, Conversión de 120 USD

Atribución: Haga clic 3 = 60 USD, Haga clic 2 = 40 USD, Haga clic 1 = 20 USD (120 USD en total)

### Ejemplos con impresiones y clics

**Nota:** Las impresiones solo se aplican a partir de anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, clic 1, impresión 2, clic 2, conversión de 120 USD

#### (Solo búsqueda, medios sociales y Commerce) Uso del 10 % como &quot;Peso de anulación de impresión&quot; predeterminado

Como la serie de eventos incluye impresiones y clics, el peso de anulación de impresión se aplica a las impresiones.

Atribución: impresión 1 = 4 USD, clic 1 = 36 USD, impresión 2 = 8 USD, clic 2 = 72 USD (120 USD en total)

#### Uso (solo DSP) de una ponderación de anulación de impresión o (solo Search, Social y Commerce) de una &quot;ponderación de anulación de impresión&quot; del 0 %

Como la serie de eventos incluye impresiones y clics, estas se omiten.

Atribución: impresión 1 = 0 USD, clic 1 = 40 USD, impresión 2 = 0 USD, clic 2 = 80 USD (120 USD en total)

### Ejemplo con todas las impresiones

**Nota:** Las impresiones solo se aplican a partir de anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, impresión 2, impresión 3, conversión de 120 USD

Dado que la conversión es una visualización, se aplica el método de valoración de la visualización, en lugar del peso de anulación de la impresión, para determinar el valor de cada impresión:

* Si el parámetro de informe especifica una ponderación de visualizaciones ponderada, dicha ponderación se aplicará a los valores de impresión. Por ejemplo, si la ponderación de visualización es del 40 %, multiplique cada valor en el &quot;Ejemplo con todos los clics&quot; por el 40 %: Impresión 3 = 24 USD, Impresión 2 = 16 USD, Impresión 1 = 8 USD (48 USD en total)

* Si el parámetro de informe especifica el uso de valores sin procesar para las visualizaciones, se dividen los 120 USD completos entre las impresiones: Impresión 3 = 60 USD, Impresión 2 = 40 USD, Impresión 1 = 20 USD (120 USD en total)

+++

<!-- end examples as collapsible content -->

## en forma de U

Atribuye la conversión a todos los eventos de la serie que se produjeron en la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j), pero otorga el mayor peso al primer evento y a los últimos, con un peso sucesivamente menor a los eventos que se producen en medio de la ruta de conversión.

Cuando la conversión solo va precedida de impresiones, la conversión se considera una *visualización*, que se pondera según la [configuración de ponderación de visualización](/help/search-social-commerce/glossary.md#uv) del anunciante o, como se especifique, según el método de valoración de visualización especificado en los parámetros de informe, vista o simulación personalizada.

Cuando la ruta de conversión incluye clics de pago e impresiones, los distintos productos de Adobe Advertising tratan las impresiones de forma diferente:

* En Search, Social y Commerce, la ponderación de anulación de impresión [print ](/help/search-social-commerce/glossary.md#i-j), que se especifica en la configuración de ponderación de anulación de impresión del anunciante y en los parámetros de informe, vista o simulación personalizada, se aplica primero a las impresiones.

* En DSP, las impresiones se ignoran y solo se ponderan los clics. DSP no tiene en cuenta las ponderaciones de anulación de impresiones para la atribución.

![Porcentajes de atribución en forma de U](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "Porcentajes de atribución en forma de U")

<!-- start examples as collapsible content -->

+++Ejemplos de cálculos de eventos

### Ejemplo con todos los clics

Ruta del evento: Haga clic en 1, Haga clic en 2, Haga clic en 3, Haga clic en 4, Conversión de 120 USD

Atribución: Haga clic 1 = 36 USD, Haga clic 2 = 24 USD, Haga clic 3 = 24 USD, Haga clic 4 = 36 USD (120 USD en total)

### Ejemplos con impresiones y clics

**Nota:** Las impresiones solo se aplican a partir de anuncios en medios sociales y de visualización.

Ruta del evento: impresión 1, clic 1, impresión 2, clic 2, conversión de 120 USD

#### (Solo búsqueda, medios sociales y Commerce) Uso del 10 % como &quot;Peso de anulación de impresión&quot; predeterminado

Como la serie de eventos incluye impresiones y clics, el peso de anulación de impresión se aplica a las impresiones.

Atribución: impresión 1 = 6 USD, clic 1 = 54 USD, impresión 2 = 6 USD, clic 2 = 54 USD (120 USD en total)

#### Uso (solo DSP) sin peso de anulación de impresión o (solo Search, Social y Commerce) un &quot;peso de anulación de impresión&quot; del 0 %

Como la serie de eventos incluye impresiones y clics, estas se omiten.

Atribución: impresión 1 = 0 USD, clic 1 = 60 USD, impresión 2 = 0 USD, clic 2 = 60 USD (120 USD en total)

### Ejemplo con todas las impresiones

**Nota:** Solo se aplican impresiones para anuncios en pantalla.

Ruta del evento: Impresión 1, Impresión 2, Impresión 3, Impresión 4, Conversión de 120 USD

Dado que la conversión es una visualización, se aplica el método de valoración de la visualización, en lugar del peso de anulación de la impresión, para determinar el valor de cada impresión:

* Si el parámetro de informe especifica una ponderación de visualizaciones ponderada, dicha ponderación se aplicará a los valores de impresión. Por ejemplo, si el peso de visualización es del 40 %, haga clic en 1 = 14,40 USD, haga clic en 2 = 9,60 USD, haga clic en 3 = 9,60 USD, haga clic en 4 = 14,40 USD (48 USD en total)

* Si el parámetro de informe especifica el uso de valores sin procesar para las visualizaciones, se dividen los 120 USD completos entre las impresiones: Haga clic en 1 = 36 USD, Haga clic en 2 = 24 USD, Haga clic en 3 = 24 USD, Haga clic en 4 = 36 USD (120 USD en total)

+++

<!-- end examples as collapsible content -->
