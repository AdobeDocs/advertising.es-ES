---
title: Usando [!DNL Roku] inventario
description: Obtenga información acerca de la asociación de DSP con  [!DNL Roku], que incluye opciones de inventario, proveedores de seguimiento de terceros aprobados y prácticas recomendadas para ubicaciones específicas de  [!DNL Roku].
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: 54f69e4c0fa20b918a037cc5d2003d67db889913
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Usando el inventario [!DNL Roku]

Advertising DSP proporciona características para la publicidad de [!DNL Roku].

## Coincidencia de audiencia

La asociación de [!DNL Roku] y DSP hace coincidir las audiencias de [!DNL DSP] con los identificadores de [!DNL Roku] para la segmentación de audiencia determinística de :1 en el inventario de [!DNL Roku].

## [!DNL Roku] opciones de inventario

Puede: a) configurar los ID de acuerdo privados directamente con [!DNL Roku] y luego introducir los datos del ID de acuerdo en DSP o b) visitar la galería [!DNL On Demand] para suscribirse a los perfiles de [!DNL Roku]:

>[!NOTE]
>
>El inventario [!DNL Roku] no está disponible en mercados e intercambios abiertos.

* Para tus ofertas privadas, [configura información sobre los ID de la oferta en DSP](/help/dsp/inventory/deal-id-create.md) y luego dirige &quot;[!UICONTROL Roku Network - Audience]&quot; y &quot;[!UICONTROL The Roku Channel - Audience]&quot; en [!DNL Roku] ubicaciones.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Puedes [suscribirte al siguiente [!DNL Roku] inventario dentro de la [!DNL On Demand] Galería](/help/dsp/inventory/on-demand-inventory-subscribe.md) y luego dirigirte a cualquiera de las ofertas aprobadas dentro de [!DNL Roku] ubicaciones:

   * &quot;[!UICONTROL Roku Network - Audience]&quot; para inventario en el ecosistema [!DNL Roku] con socios de contenido premium, como [!DNL The CW], [!DNL ABC] y [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel - Audience]&quot; para el contenido de la aplicación de [!DNL Roku] de propiedad y funcionamiento (O&amp;O).

### Ventajas de personalizar los mercados privados con [!DNL Roku]

Las ofertas privadas le permiten personalizar los parámetros de la oferta según sus necesidades.

* **Precios negociados:** Trabaje con el equipo de ventas de [!DNL Roku] para negociar y estructurar un acuerdo que satisfaga sus necesidades de campaña.

* **Prioridad de escala:** Los mercados privados (PMP) reciben mayor prioridad que las ofertas permanentes (como [!DNL On Demand] ofertas).

* **Administración de frecuencias:** El límite de frecuencia predeterminado de [!DNL Roku] es de un anuncio por cada usuario (1) cada 30 minutos, pero puede personalizarse por hora, día, semana, mes o período de vuelo completo.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Segmentación de datos:** Las audiencias de [!DNL Roku] se han creado a partir de [!DNL Roku] señales de dispositivo y TV, datos rastreados por [!DNL The Roku Channel] (como afinidad de género de TV, comportamiento de transmisión de TV y estado de suscripción de cable) y datos adicionales del sistema de administración de la relación con los clientes (CRM) de [!DNL Roku].

* **[!DNL Roku]Segmentación de contenido:** Las ofertas privadas pueden segmentar aplicaciones por género, aplicación de lista de bloqueados de aplicaciones, eventos estacionales y de tipología, y programas solo en [!DNL The Roku Channel].

## [!DNL Roku] ubicaciones

En campañas de DSP, [cree  [!DNL Roku] ubicaciones específicas](/help/dsp/campaign-management/placements/placement-create.md) con el tipo de ubicación &quot;[!UICONTROL Connected TV (Roku)]&quot;. Incluir [!DNL Roku] ubicaciones en paquetes específicos de [!DNL Roku] con objetivos definidos.

Cada ubicación de [!DNL Roku] debe estar dirigida al menos a un origen o acuerdo de [!DNL Roku]. Para usar la coincidencia de audiencia de DSP con [!DNL Roku], incluya uno o más segmentos de audiencia que puedan coincidir con el conjunto de datos determinístico [!DNL Roku] (incluido).

### [!DNL Roku] proveedores de seguimiento de terceros aprobados por

Las ubicaciones de [!DNL Roku] pueden incluir píxeles de evento de terceros y píxeles de conversión de los siguientes proveedores: [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] y [!DNL Research Now].

### Prácticas recomendadas por estrategia de ubicación

A continuación se indican las prácticas recomendadas para las ubicaciones específicas de [!DNL Roku].

Para maximizar el alcance incremental:

* Suprimir audiencias expuestas en [!DNL Roku O&O] excluyendo las audiencias a las que ya se ha llegado mediante [!DNL The Roku Channel].

* Suprimir audiencias expuestas en [!DNL All Roku] excluyendo las audiencias a las que ya se ha llegado en la plataforma [!DNL Roku].

Para la configuración más rápida:

* Oriente las ofertas siempre disponibles para [!DNL The Roku Channel] en [[!DNL On Demand] Inventario](/help/dsp/inventory/on-demand-inventory-subscribe.md) para acceder rápidamente a [!DNL Roku] inventario de propiedad y operado.
* Establezca como objetivo las ofertas permanentes existentes de [!DNL Roku Network] en [[!DNL On Demand] Inventario](/help/dsp/inventory/on-demand-inventory-subscribe.md) para lograr rápidamente la escala en la plataforma [!DNL Roku].

A escala máxima:

* Personalice un mercado privado [!DNL Roku] para obtener acceso priorizado a [!DNL Roku] suministro a un precio negociado.

>[!MORELIKETHIS]
>
>* [Crear manualmente los detalles del ID de la oferta](/help/dsp/inventory/deal-id-create.md)
> * [Suscribirse y solicitar acceso a [!DNL On Demand] ofertas de inventario premium](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Crear una ubicación](/help/dsp/campaign-management/placements/placement-create.md)
