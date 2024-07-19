---
title: Información general sobre Campaign Management en Advertising DSP
description: Obtenga información acerca de la jerarquía y los componentes de administración de campañas.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Información general sobre Campaign Management en Advertising DSP

DSP Las campañas de tienen la siguiente jerarquía:

* Campaign
   * Paquete(s)
      * Ubicación(ones)
         * Anuncio(s)
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campañas](/help/dsp/campaign-management/campaigns/campaign-about.md) son el marco general de la configuración de vuelos. Cada campaña se configura con un anunciante, fechas de inicio y finalización, un presupuesto general, una opción de segmentación entre dispositivos y un límite de frecuencia predeterminado, y opciones de creación de informes para la visibilidad, el fraude, la seguridad de la marca y la verificación de audiencia. Todas las configuraciones en el nivel de campaña se aplican automáticamente a cada paquete y ubicación dentro de la campaña.

## [!UICONTROL Packages]

Cada campaña puede contener uno o más [paquetes](/help/dsp/campaign-management/packages/package-about.md), cada uno de los cuales incluye un conjunto de ubicaciones.

Utilice paquetes para agrupar las ubicaciones para la entrega a un presupuesto establecido, un objetivo de rendimiento y una estrategia de ritmo personalizada. DSP La optimización optimiza los paquetes al desplazar los presupuestos a las ubicaciones con mejor rendimiento del paquete. Puede organizar paquetes por formato de ubicación, tipo de inventario, proveedor de datos, persona u otras características distinguibles.

Los paquetes son opcionales pero se recomiendan.

## [!UICONTROL Placements]

Una [ubicación](/help/dsp/campaign-management/placements/placement-about.md) almacena parámetros de segmentación para uno o más anuncios del mismo tipo de anuncio. Puede crear una ubicación para una sola campaña o paquete y luego asignarle anuncios.

## [!UICONTROL Ads]

[Los anuncios](/help/dsp/campaign-management/ads/ad-about.md) incluyen recursos creativos y direcciones URL de seguimiento. Puede cargar etiquetas de servicios de publicidad de terceros de forma individual o masiva mediante hojas de etiquetas de socios o la plantilla de etiquetas masiva. DSP También puede crear manualmente anuncios en pantalla nativos para que se publiquen los que se van a publicar en el servidor de.

Una vez configurados los anuncios, debe adjuntar cada anuncio a una ubicación para comenzar a ejecutarlo. Puede adjuntar un solo anuncio a una o varias ubicaciones.

Todos los anuncios activos y aprobados de una ubicación activa en una campaña activa pueden ejecutarse en función de los parámetros de segmentación de ubicación.

>[!MORELIKETHIS]
>
>* [Acerca de Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Acerca de la administración de paquetes](/help/dsp/campaign-management/packages/package-about.md)
>* [Acerca de la administración de ubicaciones](/help/dsp/campaign-management/placements/placement-about.md)
>* [Acerca de la administración de anuncios](/help/dsp/campaign-management/ads/ad-about.md)
>* [Lista de comprobación de inicio de campaña](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Tipos de informes de rendimiento en las vistas de Campaign Management](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Administrar Las Vistas De Datos De Campaign](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* DSP [Vídeo: Estructura de cuenta e interfaz de usuario de la cuenta de usuario](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
