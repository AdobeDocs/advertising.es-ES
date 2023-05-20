---
title: Métricas de publicidad de Adobe en Analysis Workspace
description: Métricas de publicidad de Adobe en Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 5dd3772de945660e76321dac935de5ebcab5979a
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Métricas de publicidad de Adobe en Analysis Workspace

*Anunciantes con una integración de Adobe de Advertising-Adobe Analytics solamente*

>[!NOTE]
>
>* Adobe Advertising pasa las métricas y dimensiones de tráfico a [!DNL Analytics] diariamente.
>* [!DNL Analytics] registra los clics y visualizaciones de Adobe de Advertising en tiempo real.
   > Para [!DNL Search, Social, & Commerce]Sin embargo, esta función es compatible con la mayoría de las redes de anuncios y tipos de campañas. Consulte &quot;Inventario admitido&quot; en la [!DNL Search, Social, & Commerce] Guía para obtener más información.<!-- add link when that's published in ExL -->


## Métricas de tráfico de la publicidad de Adobe

>[!NOTE]
>
>Todas las métricas de tráfico de publicidad de Adobe en [!DNL Analytics] empiece con &quot;AMO&quot;.

| Métrica de tráfico | Descripción |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | El número de impresiones de publicidad de Adobe. |
| [!UICONTROL AMO Clicks] | El número total de clics en publicidad de Adobe. |
| [!UICONTROL AMO Cost] | El Adobe en publicidad en la divisa del grupo de informes. |
| [!UICONTROL AMO ID Instance] | El número de veces que se establece el ID de publicidad de Adobe. |
| [!UICONTROL AMO Minutes Viewed] | Cantidad de minutos que se vio un vídeo de publicidad de Adobe. |
| [!UICONTROL AMO Views] | Número de vistas de un anuncio. Se cuenta una vista cuando el usuario inicia el vídeo de publicidad de Adobe. |
| [!UICONTROL AMO Views 25% Complete] | El número de vistas para las que se vio al menos el 25 % de un vídeo de publicidad de Adobe. |
| [!UICONTROL AMO Views 50% Complete] | El número de vistas para las que se vio al menos el 50 % de un vídeo de publicidad de Adobe. |
| [!UICONTROL AMO Views 75% Complete] | El número de vistas para las que se vio al menos el 75 % de un vídeo de publicidad de Adobe. |
| [!UICONTROL AMO Views 100% Complete] | El número de vistas para las que se vio el 100 % de un vídeo de publicidad de Adobe. |
| [!UICONTROL AMO Viewable Impressions] | El número de impresiones que se midieron para poder verse según la configuración de ubicación. |
| [!UICONTROL AMO Not Viewable Impressions] | El número de impresiones que se determinó que no eran visibles. Este valor se calcula como ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable]). |
| [!UICONTROL AMO Measurable Impressions] | El número de impresiones servidas para las que se inicializó correctamente la instrumentación de visibilidad. Este valor se calcula como (impresiones instrumentadas: el número de impresiones no medibles). |

## Dimension de publicidad de Adobe

>[!NOTE]
>
>Todas las dimensiones de publicidad de Adobe en [!DNL Analytics] van seguidas de &quot;(ID de AMO)&quot;.

| Dimension | Datos de publicidad de Adobe aplicables | Descripción |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | DSP Nombre del motor de búsqueda o de Advertising |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | El nombre de la cuenta. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | RTB ([!DNL DSP]) o el nombre de la red de publicidad ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | Nombre de la campaña. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | El paquete ([!DNL DSP]) o portafolio ([!DNL Search, Social, & Commerce]) nombre. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] datos | El nombre de la ubicación. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] datos | El nombre del grupo de publicidad. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] datos | La palabra clave. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] datos | El tipo de coincidencia de búsqueda. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] datos | La palabra clave y el tipo de coincidencia. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | El tipo de anuncio, como `text`, `video`, `display`, o `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | El tipo de anuncio ([!DNL DSP]) o título del anuncio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | La descripción del anuncio ([!DNL DSP]) o cuerpo del anuncio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] datos | Dirección URL mostrada en el anuncio. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] datos | La URL de destino del anuncio. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] y [!DNL Search, Social, & Commerce] datos | Si la entrada de la página de aterrizaje fue una visualización o un clic. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] datos | El destino de un producto para un anuncio de lista de productos. |

## Métricas calculadas personalizadas útiles para la publicidad de Adobe

Considere la posibilidad de crear las siguientes métricas para los datos de publicidad de Adobe.

* Clics hasta la instancia de la página de aterrizaje ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Es el % de personas que hicieron clic en el anuncio y llegaron a la página de aterrizaje.
* Tasa Medible ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Tasa de impresiones visibles ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Costo por vista ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Costo por clic ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Datos en publicidad de Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)

