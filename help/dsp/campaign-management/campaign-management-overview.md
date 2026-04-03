---
title: Información general sobre la administración de campañas en Advertising DSP
description: Obtenga información acerca de la jerarquía y los componentes de administración de campañas.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
TQID: https://experienceleague.adobe.com/w7j86H42OR371vewJM--ep2YUn70XJpMWJQNT92r2CY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 0%

---

# Información general sobre la administración de campañas en Advertising DSP

Las campañas de DSP tienen la siguiente jerarquía:

* Campaign
   * Paquete(s)
      * Ubicación(ones)
         * Anuncio(s)
<!--
 Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campañas](/help/dsp/campaign-management/campaigns/campaign-about.md) son el marco general de la configuración de vuelos. Cada campaña se configura con un anunciante, fechas de inicio y finalización, un presupuesto general, una opción de segmentación entre dispositivos y un límite de frecuencia predeterminado, y opciones de creación de informes para la visibilidad, el fraude, la seguridad de la marca y la verificación de audiencia. Todas las configuraciones en el nivel de campaña se aplican automáticamente a cada paquete y ubicación dentro de la campaña.

## [!UICONTROL Packages]

Cada campaña puede contener uno o más [paquetes](/help/dsp/campaign-management/packages/package-about.md), cada uno de los cuales incluye un conjunto de ubicaciones.

Utilice paquetes para agrupar las ubicaciones para la entrega a un presupuesto establecido, un objetivo de rendimiento y una estrategia de ritmo personalizada. DSP optimiza los paquetes cambiando los presupuestos a las ubicaciones con mejor rendimiento del paquete. Puede organizar paquetes por formato de ubicación, tipo de inventario, proveedor de datos, persona u otras características distinguibles.

Los paquetes son opcionales pero se recomiendan.

## [!UICONTROL Placements]

Una [ubicación](/help/dsp/campaign-management/placements/placement-about.md) almacena parámetros de segmentación para uno o más anuncios del mismo tipo de anuncio. Puede crear una ubicación para una sola campaña o paquete y luego asignarle anuncios.

## [!UICONTROL Ads]

[Los anuncios](/help/dsp/campaign-management/ads/ad-about.md) incluyen recursos creativos y direcciones URL de seguimiento. Puede cargar etiquetas de servicios de publicidad de terceros de forma individual o masiva mediante hojas de etiquetas de socios o la plantilla de etiquetas masiva. También puede crear manualmente anuncios en pantalla nativos para DSP.

Una vez configurados los anuncios, debe adjuntar cada anuncio a una ubicación para comenzar a ejecutarlo. Puede adjuntar un solo anuncio a una o varias ubicaciones.

Todos los anuncios activos y aprobados de una ubicación activa en una campaña activa pueden ejecutarse en función de los parámetros de segmentación de ubicación.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de campañas en Advertising DSP](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Acerca de la administración de paquetes en Advertising DSP](/help/dsp/campaign-management/packages/package-about.md)
>* [Acerca de la administración de ubicaciones en Advertising DSP](/help/dsp/campaign-management/placements/placement-about.md)
>* [Acerca de la administración de anuncios en Advertising DSP](/help/dsp/campaign-management/ads/ad-about.md)
>* [Lista de comprobación de inicio de campaña](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Tipos de informes de rendimiento en vistas de administración de campañas](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Administrar las vistas de datos de tu campaña](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Vídeo: estructura de cuenta de DSP e interfaz de usuario](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html?lang=es)
