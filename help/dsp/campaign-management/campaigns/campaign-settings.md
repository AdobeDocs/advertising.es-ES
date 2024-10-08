---
title: Configuración de campaña
description: Consulte las descripciones de las configuraciones de campaña disponibles.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1034'
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

**[!UICONTROL Margin Management]:** Si se van a administrar los márgenes de la campaña: *[!UICONTROL Yes]* o *[!UICONTROL No]* (valor predeterminado).

Al elegir *[!UICONTROL Yes],*, especifique el tipo de margen y la cantidad:

* **[!UICONTROL Margin Type]:** El tipo de margen. No puede cambiar el tipo de margen una vez que activa la administración de márgenes y guarda la campaña.

   * DSP *[!UICONTROL Fixed]:* (valor predeterminado) Permite a los calcular automáticamente y limitar el gasto en función de un porcentaje de margen fijo de [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Permite administrar los márgenes hasta el nivel de ubicación especificando [!UICONTROL Budget Reserve %] y [!UICONTROL Gross Budget] independientes para cada paquete y ubicación en la campaña. DSP La optimización se basa en la eficiencia financiera de cada colocación, sin garantizar un margen específico. Utilícelo para pedidos de inserción que consten de varios artículos de línea para los que haya acordado entregar una cantidad fija de unidades o tipos de unidad a una tasa fija.

* **[!UICONTROL Fixed Margin %]:** (solo campañas con márgenes fijos) El marcado predeterminado para cada orden de inserción <!-- impression? -->, como porcentaje. Esta cantidad se resta del [!UICONTROL Gross Budget] para definir el presupuesto neto de la campaña.

* **[!UICONTROL Budget Reserve %]:** (solo campañas con márgenes fijos; opcional) Reserva un porcentaje especificado de [!UICONTROL Gross Budget] como medida de seguridad. Esta cantidad se resta del [!UICONTROL Gross Budget] para definir el presupuesto neto de la campaña.

**[!UICONTROL Gross Budget]:** (Campañas solo con administración de márgenes) El presupuesto bruto de la campaña, antes de que se apliquen los ajustes marginales especificados.

Si lo desea, puede añadir un presupuesto bruto diario, semanal o mensual adicional:

1. Haga clic en **[!UICONTROL Add an additional Gross Budget]**.

1. Escriba **[!UICONTROL Gross Budget]** y seleccione el intervalo de presupuesto: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly]*.

El presupuesto neto total, que es el límite de gasto de la campaña, se calcula automáticamente en función de la configuración de los márgenes y se indica debajo de este valor.

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

DSP **[!UICONTROL Cross Device Level]:** (de solo lectura para las campañas existentes creadas desde el 22 de junio de 2020; no disponible para las campañas creadas antes del 22 de junio de 2020) Nivel en el que se segmentan los anuncios y se aplican límites de frecuencia: *Mismo dispositivo* para segmentar un dispositivo o *Personas* para segmentar a una persona en todos sus dispositivos conocidos. **Nota:** La compatibilidad entre dispositivos no está disponible para las ubicaciones destinadas a los identificadores universales.

**[!UICONTROL Device Graph]:** (de solo lectura para campañas existentes; campañas con segmentación multidispositivo basada en personas solamente) El gráfico de dispositivos que se utilizará para la segmentación multidispositivo y la administración de frecuencias:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponible para todos los anunciantes para segmentación entre dispositivos a 0,35 $ CPM para impresiones que se entregan mediante el gráfico de dispositivo [!DNL LiveRamp] (es decir, para dispositivos que no se encuentran dentro de los segmentos de audiencia de destino). Puede configurar la segmentación entre dispositivos en el nivel de ubicación.

  Esta opción también está disponible para todos los anunciantes, sin ningún cargo, para la administración de frecuencias y la medición de atribución.

  La compatibilidad entre dispositivos solo se aplica a las ubicaciones que se dirigen a ID heredados, pero no a las ubicaciones que se dirigen a ID universales (incluido [!DNL LiveRamps]). La segmentación, la administración de frecuencias y la atribución para ID universales se aplican solo en el nivel de ID.

**[!UICONTROL Frequency Cap]:** (opcional) la cantidad de veces que un dispositivo único, un identificador universal o una persona (según el [!UICONTROL Cross Device Level] especificado y la configuración [!UICONTROL Targeting] de la ubicación) se pueden publicar anuncios desde la campaña. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
> Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respeta el límite de frecuencia más estricto de la jerarquía de campañas.

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

**[!UICONTROL Comscore Campaign Ratings]:** (opcional) habilita la medición de [!DNL Campaign Ratings] validada por [!DNL Comscore] y la generación de informes de verificación de audiencia, utilizando la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Target Gender]:** El sexo para el destino: *[!UICONTROL Both]* (el valor predeterminado), *[!UICONTROL Male]* o *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** El intervalo de edad para el destino. Utilice los deslizadores izquierdo y derecho para reducir el rango según sea necesario.

* **[!UICONTROL Target Country]:** (opcional) un país de destino. [!DNL Comscore] mide impresiones servidas solamente en países compatibles.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Habilita el seguimiento para la métrica de nivel de ubicación [!UICONTROL Attention Score] (el promedio ponderado de [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; entre impresiones). Las métricas están disponibles para todos los tipos de ubicación, excepto para la televisión conectada a [!DNL Roku], el anuncio previo a la emisión solo de VPAID y el audio que no es un podcast. DSP adjunta automáticamente una etiqueta JavaScript DSP a todos los creativos asociados, y [!DNL Adelaide] rastrea los datos de exposición y los envía a los creativos diariamente. Puede usar la fecha para optimizar manualmente el gasto hacia tácticas de colocación con mejores puntuaciones de atención.

El campo [!UICONTROL Attention Score] está disponible en la sección [!UICONTROL Metrics] de informes; en las vistas [!UICONTROL Campaigns], [!UICONTROL Packages] y [!UICONTROL Placements]; y en las pestañas [!UICONTROL Sites], [!UICONTROL Ads] y [!UICONTROL Inventory] de la vista [detalles de ubicación](/help/dsp/campaign-management/reports/placement-details-view.md).

El uso de [!DNL Adelaide] segmentos para la medición implica una tarifa CPM por cada impresión entregada desde anuncios con [!DNL Adelaide] etiquetas de medición. Esta tarifa es independiente de las tarifas de [segmentación de atención de nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

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
>* [Acerca de Campaign Management](campaign-about.md)
>* [Crear una campaña](campaign-create.md)
>* [Editar una campaña](campaign-edit.md)
>* [Ver el registro de cambios de una campaña](campaign-change-log.md)
