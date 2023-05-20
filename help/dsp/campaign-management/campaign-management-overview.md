---
title: Descripción general de Campaign Management DSP en Advertising
description: Obtenga información acerca de la jerarquía y los componentes de administración de campañas.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Descripción general de Campaign Management DSP en Advertising

DSP Las campañas de tienen la siguiente jerarquía:

* Campaign
   * Paquete(s)
      * Ubicación(ones)
         * Anuncio(s)

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campañas](/help/dsp/campaign-management/campaigns/campaign-about.md) son el marco general de la configuración de vuelo. Cada campaña se configura con un anunciante, fechas de inicio y finalización, un presupuesto general, una opción de segmentación entre dispositivos y un límite de frecuencia predeterminado, y opciones de creación de informes para la visibilidad, el fraude, la seguridad de la marca y la verificación de audiencia. Todas las configuraciones en el nivel de campaña se aplican automáticamente a cada paquete y ubicación dentro de la campaña.

## [!UICONTROL Packages]

Cada campaña puede contener una o más [paquetes](/help/dsp/campaign-management/packages/package-about.md), cada una de las cuales incluye un conjunto de ubicaciones.

Utilice paquetes para agrupar las ubicaciones para la entrega a un presupuesto establecido, un objetivo de rendimiento y una estrategia de ritmo personalizada. DSP La optimización optimiza los paquetes al desplazar los presupuestos a las ubicaciones con mejor rendimiento del paquete. Puede organizar paquetes por formato de ubicación, tipo de inventario, proveedor de datos, persona u otras características distinguibles.

Los paquetes son opcionales pero se recomiendan.

## [!UICONTROL Placements]

A [ubicación](/help/dsp/campaign-management/placements/placement-about.md) almacena parámetros de segmentación para uno o varios anuncios del mismo tipo de anuncio. Puede crear una ubicación para una sola campaña o paquete y luego asignarle anuncios.

## [!UICONTROL Ads]

[Anuncios](/help/dsp/campaign-management/ads/ad-about.md) incluya recursos creativos y direcciones URL de seguimiento. Puede cargar etiquetas de servicios de publicidad de terceros de forma individual o masiva mediante hojas de etiquetas de socios o la plantilla de etiquetas masiva. DSP También puede crear manualmente anuncios en pantalla nativos para que se publiquen los que se van a publicar en el servidor de.

Una vez configurados los anuncios, deberá adjuntar cada anuncio a una ubicación. Puede adjuntar un solo anuncio a una o varias ubicaciones.

Todos los anuncios activos y aprobados de una ubicación activa en una campaña activa pueden ejecutarse en función de los parámetros de segmentación de ubicación.

>[!MORELIKETHIS]
>
>* [Acerca de Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Acerca de la administración de paquetes](/help/dsp/campaign-management/packages/package-about.md)
>* [Acerca de la administración de ubicación](/help/dsp/campaign-management/placements/placement-about.md)
>* [Acerca de la administración de anuncios](/help/dsp/campaign-management/ads/ad-about.md)
>* [Lista de comprobación de Campaign Launch](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Acerca de los informes en la plataforma](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Acerca de las vistas de datos de Campaign](/help/dsp/campaign-management/reports/campaign-data-views-about.md)
>* [DSP Vídeo: Estructura de cuenta y interfaz de usuario de](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)

