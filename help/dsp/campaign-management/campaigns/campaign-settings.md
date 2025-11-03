---
title: Configuración de campaña
description: Consulte las descripciones de las configuraciones de campaña disponibles.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9d26e097f007b570c0f0e3b7f02c683a84d5e647
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 0%

---

# Configuración de campaña

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** El nombre de la campaña.

**[!UICONTROL Advertiser]:** (solo lectura para campañas existentes) El anunciante (marca) aplicable. Seleccione un anunciante existente o cree uno nuevo.

**[!UICONTROL Advertiser URL]:** La página oficial del anunciante. Este campo acelera el proceso de aprobación del anuncio con los socios de inventario.

**[!UICONTROL Timezone]:** (solo lectura para campañas existentes) Zona horaria para informes y ofertas.

**[!UICONTROL Customer PO]:** (opcional) un pedido de compra de cliente para el pedido de inserción o el pedido de compra.

**[Fechas de campaña]:** Las fechas de inicio y finalización de la campaña.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** (Cuentas de autoservicio atendidas por agencias que usan márgenes) Opciones para la administración de márgenes:

* **[!UICONTROL Would you like to manage margins for this campaign?]:** Si se van a administrar los márgenes de la campaña: *[!UICONTROL Yes]* o *[!UICONTROL No]* (valor predeterminado). Al elegir *[!UICONTROL Yes],* especifica la configuración adicional. Una vez habilitada la administración de márgenes y guardada la campaña, no se puede deshabilitar la administración de márgenes.

* **[!UICONTROL How would you like to compute agency fees?]:** (Campañas solo con administración de márgenes) Cómo calcular las tarifas de agencia, que son la porción del presupuesto bruto de la campaña que se retiene y no se incluye en el gasto neto:

   * *[!UICONTROL Margin % of Total Budget]:* (predeterminado) Calcular tarifas como porcentaje del gasto bruto. Especifique [!UICONTROL Agency Fee Type] (fijo o compuesto) y [!UICONTROL Margin %] o [!UICONTROL Composite Margin %].

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* Cargos de cómputo como un porcentaje especificado de su costo de medios, datos y otros costos, y/o [!DNL Adobe] cargos de tecnología. Especifique [!UICONTROL Markup %] y seleccione los componentes a los que desea aplicar el marcado.

* **[!UICONTROL Agency Fee Type]:** (Campañas que utilizan [!UICONTROL Margin % of Total Budget]) El tipo de tarifa de agencia.

   * *[!UICONTROL Fixed]:* (valor predeterminado) Permite que DSP retenga un porcentaje fijo del gasto bruto como honorarios de agencia. Especifique [!UICONTROL Margin %].

   * *[!UICONTROL Composite]:* Permite que DSP retenga un porcentaje del gasto bruto para tener en cuenta tanto las tarifas de agencia como las [!DNL Adobe] tarifas técnicas. Especifique [!UICONTROL Composite Margin %].

* **[!UICONTROL Margin %]:** (Campañas que utilizan [!UICONTROL Margin % of Total Budget] con márgenes fijos) El porcentaje del gasto bruto que se retendrá como tarifas de agencia. Cualquier cambio en el valor del margen se aplica solo al gasto bruto futuro y no al gasto bruto histórico de la campaña. El valor [!UICONTROL Estimated Tax Withholding] se excluye del gasto bruto antes de que se aplique el margen. Consulte los siguientes ejemplos, que suponen que la campaña no gasta en exceso ni en exceso.

   * Ejemplo 1: Supongamos que [!UICONTROL Gross Budget] es `100 USD` y [!UICONTROL Margin %] es `5%` durante todo el vuelo. Al final del vuelo de campaña, las tarifas de agencia se calculan como `5 USD` (que es `5% of 100 USD`) y el gasto neto es `95 USD` (que es `campaign budget [100 USD] - agency fees [5 USD]`).

   * Ejemplo 2 con cambios en el margen: Para la misma campaña, suponga que [!UICONTROL Margin %] se cambió de `5%` a `10%` cuando el gasto bruto era `40 USD`. Para el período antes del cambio, las tarifas de agencia se calculan como `2 USD` (que es `5% of 40 USD`); para el período después del cambio, las tarifas de agencia se calculan como `6 USD` (que es `10% of 60 USD`). El total de tarifas de agencia se calcula como `8 USD` (que es `2 USD + 6 USD`) y el gasto neto es `92 USD` (que es `campaign budget [100 USD] - total agency fees [8 USD]`).

   * Ejemplo 3 con retención de impuestos: Supongamos que [!UICONTROL Gross Budget] es `100 USD`, [!UICONTROL Estimated Tax Withholding] al final del vuelo de campaña es `10 USD` y [!UICONTROL Margin %] es `5%` durante todo el vuelo. Al final del vuelo de campaña, las tarifas de agencia se calculan como `4.5 USD` (que es `5% of (campaign budget [100 USD] - tax withholding [USD 10])`) y el gasto neto es `85.5 USD` (que es `campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]`).

* **[!UICONTROL Composite Margin %]:** (Campañas que utilizan [!UICONTROL Margin % of Total Budget] con márgenes compuestos) El porcentaje del gasto bruto que se retendrá como [!DNL Adobe] tarifas de tecnología y tarifas de agencia combinadas. Las tarifas de agencia se calculan restando las tarifas técnicas de Adobe de la cantidad de margen compuesta. Cualquier cambio en el valor del margen compuesto se aplica solo al gasto bruto futuro y no al gasto bruto histórico de la campaña. El valor [!UICONTROL Estimated Tax Withholding] se excluye del gasto bruto antes de que se aplique el margen compuesto.

  Por ejemplo, supongamos que [!UICONTROL Gross Budget] es `100 USD`, que las tarifas técnicas de [!DNL Adobe] al final del vuelo de campaña son `10 USD` y que [!UICONTROL Composite Margin %] es `17%` durante todo el vuelo. Al final del vuelo de la campaña (suponiendo que la campaña no gaste menos de lo debido ni más de lo debido), las tarifas de agencia se calculan como `7 USD` (que es `(17% of 100 USD) - 10`) y el gasto neto es `93 USD` (que es `campaign budget [100 USD] - agency fees [7 USD]`).

* **[!UICONTROL Markup %]:** (Campañas que utilizan [!UICONTROL Apply Markup % on top of individual cost components]) El porcentaje que se aplicará a los componentes de costo especificados para calcular las tarifas de agencia. Cualquier cambio en el valor de marcado se aplica solo a los costes futuros y no a los costes históricos de la campaña.

* **[!UICONTROL Select cost components on which markup will be applied]:** (Campañas que utilizan [!UICONTROL Apply Markup % on top of individual cost components]) Los componentes de costo para los que se aplica [!UICONTROL Markup %]. Seleccione todos los componentes aplicables: *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]* o *[!UICONTROL Adobe tech fees]*. Cualquier cambio en la selección de componentes se aplica solo a los costes futuros y no a los costes históricos de la campaña.

  Por ejemplo, [!UICONTROL Markup %] es `10%` para &quot;[!UICONTROL Media cost]&quot; y &quot;[!UICONTROL Data and Other costs]. Si, en cualquier momento de la campaña, el costo de los medios es `20 USD`, los datos y otros costos son `5 USD` y las tarifas técnicas son [!DNL Adobe] `2 USD`, las tarifas de agencia se calculan como `2.50 USD` (que es `10% of (20 USD + 5 USD)` y el gasto bruto es `29.50 USD` (que es `media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]`).

**[!UICONTROL Gross Budget]:** (Campañas solo con administración de márgenes) El presupuesto bruto de la campaña, antes de que se apliquen los ajustes marginales especificados.

**[!UICONTROL Budget]:** (Campañas sin administración de márgenes) El presupuesto general de la campaña.

**[!UICONTROL Estimated Tax Withholding]:** retiene un porcentaje del gasto total entre tarifas de publicidad, tarifas de servicio de publicidad y/o tarifas de datos en el nivel de cuenta para impuestos locales o nacionales. Las tarifas son estimaciones para fines de presupuesto y ritmo, por lo que las tasas de impuestos facturadas pueden variar.

Para calcular los impuestos retenidos:

1. Haga clic en **[!UICONTROL Update rates here]**.

1. Especifique **[!UICONTROL Estimated tax rate]** como un porcentaje.

1. Active la casilla de verificación situada junto a cada tipo de cuota para el que desee retener impuestos. Los tipos de tarifa incluyen:

   * *[!UICONTROL Include estimated tax - ads fee]:* Se aplica a todo el gasto en medios de Advertising DSP, incluidos los impuestos sobre las tarifas de administración de campañas.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* se aplica a todos los gastos en Advertising DSP excepto en medios y datos. No incluye impuestos para las tarifas de administración de campañas

   * *[!UICONTROL Include estimated tax - data fee]:* se aplica a todos los datos que se gastan en Advertising DSP.

1. Haga clic en **[!UICONTROL Submit]**.

>[!NOTE]
>
>* En Estados Unidos, los estados pueden variar en su inclusión de tasas impositivas entre anuncios, servicios de publicidad y datos. Para las organizaciones de otros países, incluya las tres categorías de tasas fiscales para contabilizar el IVA.
>
>* También puede configurar estos valores en la configuración de tarifas de la cuenta.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (de solo lectura para las campañas existentes creadas desde el 22 de junio de 2020; no disponible para las campañas creadas antes del 22 de junio de 2020) Nivel en el que DSP segmenta los anuncios y aplica límites de frecuencia: *Mismo dispositivo* para segmentar un dispositivo o *Personas* para segmentar a una persona en todos sus dispositivos conocidos. **Nota:** La compatibilidad entre dispositivos no está disponible para las ubicaciones destinadas a los identificadores universales.

**[!UICONTROL Device Graph]:** (de solo lectura para campañas existentes; campañas con segmentación multidispositivo basada en personas solamente) El gráfico de dispositivos que se utilizará para la segmentación multidispositivo y la administración de frecuencias:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponible para todos los anunciantes para segmentación entre dispositivos en $0.35 CPM para impresiones que se entregan mediante el gráfico de dispositivos [!DNL LiveRamp] (es decir, para dispositivos que no se encuentran dentro de los segmentos de audiencia de destino). Puede configurar la segmentación entre dispositivos en el nivel de ubicación.

  Esta opción también está disponible para todos los anunciantes, sin ningún cargo, para la administración de frecuencias y la medición de atribución.

  La compatibilidad entre dispositivos solo se aplica a las ubicaciones que se dirigen a ID heredados, pero no a las ubicaciones que se dirigen a ID universales (incluido [!DNL LiveRamps]). La segmentación, la administración de frecuencias y la atribución para ID universales se aplican solo en el nivel de ID.

**[!UICONTROL Frequency Cap]:** (opcional) la cantidad de veces que un dispositivo único, un identificador universal o una persona (según el [!UICONTROL Cross Device Level] especificado y la configuración [!UICONTROL Targeting] de la ubicación) se pueden publicar anuncios desde la campaña. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
> Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respeta el límite de frecuencia más estricto en la jerarquía de campañas.

**[!UICONTROL Packages]:** Los [paquetes](/help/dsp/campaign-management/packages/package-about.md) que se incluirán en la campaña. Seleccione los paquetes existentes o cree los paquetes que desea incluir. Si crea paquetes, consulte las descripciones acerca de [configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md) para obtener más información.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>La siguiente configuración solo habilita las capacidades de medición y creación de informes. La optimización del rendimiento solo se ejecuta en el nivel de paquete y ubicación.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (opcional) habilita la medición e informes de [!DNL IAS] de la visibilidad, el fraude, la seguridad de marca y la verificación de audiencia mediante la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Measure On]:** El inventario en el que se va a medir: *[!UICONTROL Display and VPAID video inventory]* (predeterminado) o *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >La visibilidad del vídeo solo se puede medir en el inventario VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Anunciantes con sus propias cuentas de [!DNL IAS]; opcional) Identificador de cuenta de [!DNL IAS] de la organización, a la que [!DNL IAS] facturará directamente por su uso.

* **[!UICONTROL IAS Team ID]:** (Anunciantes con sus propias cuentas de [!DNL IAS]; opcional) Identificador de equipo de la cuenta de [!DNL IAS] de la organización, a la que [!DNL IAS] facturará directamente por su uso. <!-- verify -->

#### Verificación de audiencia

**[!UICONTROL Comscore Campaign Ratings]:** (opcional) habilita la medición de [!DNL Comscore] validada por [!DNL Campaign Ratings] y la generación de informes de verificación de audiencia, utilizando la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Target Gender]:** El sexo para el destino: *[!UICONTROL Both]* (el valor predeterminado), *[!UICONTROL Male]* o *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** El intervalo de edad para el destino. Utilice los deslizadores izquierdo y derecho para reducir el rango según sea necesario.

* **[!UICONTROL Target Country]:** (opcional) un país de destino. [!DNL Comscore] mide impresiones servidas solamente en países compatibles.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Habilita el seguimiento para la métrica de nivel de ubicación [!UICONTROL Attention Score] (el promedio ponderado de [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; entre impresiones). Las métricas están disponibles para todos los tipos de ubicación, excepto para la televisión conectada a [!DNL Roku], el anuncio previo a la emisión solo de VPAID y el audio que no es un podcast. DSP adjunta automáticamente una etiqueta JavaScript a todos los creativos asociados y [!DNL Adelaide] realiza un seguimiento de los datos de exposición y los envía a DSP diariamente. Puede usar la fecha para optimizar manualmente el gasto hacia tácticas de colocación con mejores puntuaciones de atención.

El campo [!UICONTROL Attention Score] está disponible en la sección [!UICONTROL Metrics] de informes; en las vistas [!UICONTROL Campaigns], [!UICONTROL Packages] y [!UICONTROL Placements]; y en las pestañas [!UICONTROL Sites], [!UICONTROL Ads] y [!UICONTROL Inventory] de la vista [detalles de ubicación](/help/dsp/campaign-management/reports/placement-details-view.md).

El uso de [!DNL Adelaide] segmentos para la medición implica una tarifa de CPM por cada impresión enviada desde anuncios con [!DNL Adelaide] etiquetas de medición. Esta tarifa es independiente de las tarifas de [segmentación de atención de nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Habilita la medición de origen y la generación de informes de visibilidad mediante la tecnología [!DNL IAB Open Video Viewability (OpenVV)], según el nivel de sensibilidad especificado:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Acerca de la administración de campañas](campaign-about.md)
>* [Crear una campaña](campaign-create.md)
>* [Editar una campaña](campaign-edit.md)
>* [Ver el registro de cambios de una campaña](campaign-change-log.md)
