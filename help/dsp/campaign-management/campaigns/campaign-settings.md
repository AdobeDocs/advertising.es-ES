---
title: Configuración de campaña
description: Consulte las descripciones de las configuraciones de campaña disponibles.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 4aff26ef50d970b8440e2cf07b5f835d2b5a6599
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 0%

---

# Configuración de campaña

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Nombre de la campaña.

**[!UICONTROL Advertiser]:** (Solo lectura para campañas existentes) El anunciante aplicable (marca). Seleccione un anunciante existente o cree uno nuevo.

**[!UICONTROL Advertiser URL]:** La página oficial del anunciante. Este campo acelera el proceso de aprobación del anuncio con los socios de inventario.

**[!UICONTROL Timezone]:** (Solo lectura para campañas existentes) Zona horaria para informes y ofertas.

**[!UICONTROL Customer PO]:** (Opcional) Un pedido de compra de cliente para el pedido de inserción/pedido de compra.

**[Fechas de campaña]:** Las fechas de inicio y finalización de la campaña.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Si se van a administrar los márgenes de la campaña: *[!UICONTROL Yes]* o *[!UICONTROL No]* (el valor predeterminado).

Al elegir *[!UICONTROL Yes],* especifique el tipo de margen y la cantidad:

* **[!UICONTROL Margin Type]:** El tipo de margen. No puede cambiar el tipo de margen una vez que activa la administración de márgenes y guarda la campaña.

   * *[!UICONTROL Fixed]:* DSP (valor predeterminado) Permite a los usuarios calcular automáticamente el gasto y establecer un límite máximo en función de un porcentaje de margen fijo del valor de [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Permite administrar los márgenes hasta el nivel de colocación especificando una [!UICONTROL Budget Reserve %] y [!UICONTROL Gross Budget] para cada paquete y ubicación en la campaña. DSP La optimización se basa en la eficiencia financiera de cada colocación, sin garantizar un margen específico. Utilícelo para pedidos de inserción que consten de varios artículos de línea para los que haya acordado entregar una cantidad fija de unidades o tipos de unidad a una tasa fija.

* **[!UICONTROL Fixed Margin %]:** (Solo campañas con márgenes fijos) El marcado predeterminado para cada orden de inserción <!-- impression? -->, como porcentaje. Esta cantidad se deduce del [!UICONTROL Gross Budget] para definir el presupuesto de la campaña de red.

* **[!UICONTROL Budget Reserve %]:** (Solo campañas con márgenes fijos; opcional) Reserva un porcentaje especificado del [!UICONTROL Gross Budget] como salvaguardia. Esta cantidad se deduce del [!UICONTROL Gross Budget] para definir el presupuesto de la campaña de red.

**[!UICONTROL Gross Budget]:** (Solo campañas con administración de márgenes) El presupuesto bruto de la campaña, antes de que se apliquen los ajustes marginales especificados.

Si lo desea, puede añadir un presupuesto bruto diario, semanal o mensual adicional:

1. Clic **[!UICONTROL Add an additional Gross Budget]**.

1. Introduzca el **[!UICONTROL Gross Budget]** y seleccione el intervalo presupuestario: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly]*.

El presupuesto neto total, que es el límite de gasto de la campaña, se calcula automáticamente en función de la configuración de los márgenes y se indica debajo de este valor.

**[!UICONTROL Budget]:** (Campañas sin administración de márgenes) El presupuesto general de la campaña.

**[!UICONTROL Estimated Tax Withholding]:** Retiene un porcentaje del gasto total entre tarifas de publicidad, tarifas de servicio de publicidad y/o tarifas de datos a nivel de cuenta para impuestos locales o nacionales. Las tarifas son estimaciones para fines de presupuesto y ritmo, por lo que las tasas de impuestos facturadas pueden variar.

Para calcular los impuestos retenidos:

1. Clic **[!UICONTROL Update rates here]**.

1. Especifique el **[!UICONTROL Estimated tax rate]**, como porcentaje.

1. Active la casilla de verificación situada junto a cada tipo de cuota para el que desee retener impuestos. Los tipos de tarifa incluyen:

   * *[!UICONTROL Include estimated tax - ads fee]:* DSP Se aplica a todos los gastos en medios de Advertising, incluidos los impuestos sobre las tarifas de administración de campañas.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* DSP Se aplica a todos los gastos en publicidad, excepto a los gastos en medios y datos, y a los gastos en publicidad, a excepción de los gastos en publicidad. No incluye impuestos para las tarifas de administración de campañas

   * *[!UICONTROL Include estimated tax - data fee]:* DSP Se aplica a todos los datos gastados en Advertising.

1. Clic **[!UICONTROL Submit]**.

>[!NOTE]
>
>* En Estados Unidos, los estados pueden variar en su inclusión de tasas impositivas entre anuncios, servicios de publicidad y datos. Para las organizaciones de otros países, incluya las tres categorías de tasas fiscales para contabilizar el IVA.
>
>* También puede configurar estos valores en la configuración de tarifas de la cuenta.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** DSP (Solo lectura para las campañas existentes creadas desde el 22 de junio de 2020; no disponible para las campañas creadas antes del 22 de junio de 2020) El nivel de segmentación de anuncios y aplicación de límites de frecuencia: *Mismo dispositivo* para dirigirse a un dispositivo o *People* para dirigirse a una persona en todos sus dispositivos conocidos. **Nota:** La compatibilidad entre dispositivos no está disponible para ubicaciones destinadas a ID universales.

**[!UICONTROL Device Graph]:** (Solo lectura para campañas existentes; campañas con segmentación multidispositivo basada en personas únicamente) El gráfico de dispositivos que se utilizará para la segmentación multidispositivo y la administración de frecuencias:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponible para todos los anunciantes para direccionamiento entre dispositivos a 0,35 $ CPM para impresiones que se entregan mediante el [!DNL LiveRamp] gráfico de dispositivos (es decir, para dispositivos que no se encuentran dentro de los segmentos de audiencia de destino). Puede configurar la segmentación entre dispositivos en el nivel de ubicación.

  Esta opción también está disponible para todos los anunciantes, sin ningún cargo, para la administración de frecuencias y la medición de atribución.

  La compatibilidad entre dispositivos solo se aplica a las ubicaciones que se dirigen a ID heredados, pero no a las ubicaciones que se dirigen a ID universales (como [!DNL LiveRamps]). La segmentación, la administración de frecuencias y la atribución para ID universales se aplican solo en el nivel de ID.

**[!UICONTROL Frequency Cap]:** (Opcional) El número de veces que un dispositivo único, ID universal o persona (según el especificado) [!UICONTROL Cross Device Level] y la ubicación de [!UICONTROL Targeting] configuración) pueden mostrarse como anuncios de la campaña. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
> Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respeta el límite de frecuencia más estricto de la jerarquía de campañas.

**[!UICONTROL Packages]:** El [paquetes](/help/dsp/campaign-management/packages/package-about.md) para incluirlo en la campaña. Seleccione los paquetes existentes o cree los paquetes que desea incluir. Si crea paquetes, consulte las descripciones acerca de [configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md) para obtener más información.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>La siguiente configuración solo habilita las capacidades de medición y creación de informes. La optimización del rendimiento solo se ejecuta en el nivel de paquete y ubicación.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Opcional) Habilita [!DNL IAS] medición e informes de visibilidad, fraude, seguridad de marca y verificación de audiencia con la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Measure On]:** El inventario en el que se va a medir: *[!UICONTROL Display and VPAID video inventory]* (el valor predeterminado) o *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >La visibilidad del vídeo solo se puede medir en el inventario VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Anunciantes con su propio [!DNL IAS] cuentas; opcional) La organización [!DNL IAS] ID de cuenta, que [!DNL IAS] facturará directamente por su uso.

* **[!UICONTROL IAS Team ID]:** (Anunciantes con su propio [!DNL IAS] cuentas; opcional) El ID de equipo del [!DNL IAS] cuenta, que [!DNL IAS] facturará directamente por su uso. <!-- verify -->

**[!UICONTROL MOAT]:** (Opcional) Habilita [!DNL MOAT] medición e informes de visibilidad, fraude, seguridad de marca y verificación de audiencia. Se aplican tarifas adicionales.

#### Verificación de audiencia

**[!UICONTROL comScore Campaign Ratings]:** (Opcional) Habilita [!DNL Comscore] validado [!DNL Campaign Ratings] medición e informes de la verificación de audiencias con la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Target Gender]:** El género al que se dirige: *[!UICONTROL Both]* (el valor predeterminado), *[!UICONTROL Male]*, o *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** El intervalo de edad al que se dirige. Utilice los deslizadores izquierdo y derecho para reducir el rango según sea necesario.

* **[!UICONTROL Target Country]:** (Opcional) Un país de destino. [!DNL Comscore] las impresiones de medidas se sirven únicamente en los países apoyados.

### [!UICONTROL Attention Measurement]

**[!UICONTROL Adelaide]:** Habilita el seguimiento para el nivel de ubicación [!UICONTROL Attention Score] métrica (el número promedio ponderado de unidades de atención entre impresiones) desde [!DNL Adelaide]. Las métricas están disponibles para todos los tipos de ubicación, excepto para [!DNL Roku] TV conectada, pre-roll solo VPAID y audio que no es un podcast. DSP La aplicación adjunta automáticamente una etiqueta JavaScript a todos los creativos asociados, y [!DNL Adelaide] DSP registra los datos de exposición y los envía diariamente a la dirección de correo electrónico de la dirección de correo electrónico de la dirección de correo electrónico Puede usar la fecha para optimizar manualmente el gasto hacia tácticas de colocación con mejores puntuaciones de atención.

El [!UICONTROL Attention Score] está disponible en el campo [!UICONTROL Metrics] sección de informes; dentro de [!UICONTROL Campaigns], [!UICONTROL Packages], y [!UICONTROL Placements] vistas; y en el [!UICONTROL Sites], [!UICONTROL Ads], y [!UICONTROL Inventory] pestañas del [vista de detalles de ubicación](/help/dsp/campaign-management/reports/placement-details-view.md).

Uso de [!DNL Adelaide] Los segmentos para la medición incurren en una tarifa CPM por cada impresión entregada a partir de anuncios con [!DNL Adelaide] etiquetas de medición. Esta tarifa es independiente de las tarifas para [targeting de atención de nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Habilita la medición e informes de origen de la visibilidad mediante [!DNL IAB Open Video Viewability (OpenVV)] basada en el nivel de sensibilidad especificado:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Acerca de Campaign Management](campaign-about.md)
>* [Creación de una campaña](campaign-create.md)
>* [Edición de una campaña](campaign-edit.md)
>* [Visualización del registro de cambios de una campaña](campaign-change-log.md)
