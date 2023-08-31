---
title: Métricas de Adobe Advertising en Analysis Workspace
description: Métricas de Adobe Advertising en Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Métricas de Adobe Advertising en Analysis Workspace

*Anunciantes con solo integración de Adobe Advertising-Adobe Analytics*

>[!NOTE]
>
>* El Adobe Advertising pasa las métricas y dimensiones de tráfico a [!DNL Analytics] diariamente.
>* [!DNL Analytics] registra las pulsaciones del Adobe Advertising y las visualizaciones en tiempo real.
>* Para [!DNL Search, Social, & Commerce]Sin embargo, esta función es compatible con la mayoría de las redes de anuncios y tipos de campañas. Consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot; en el [!DNL Search, Social, & Commerce] Guía para obtener más información.

## Métricas de tráfico del Adobe Advertising

Adobe Advertising de métricas de tráfico en [!DNL Analytics] normalmente comienza con &quot;Adobe Advertising&quot;, excepto &quot;[!UICONTROL AMO ID Instances].&quot; Sin embargo, para los clientes a largo plazo que utilizaban un evento personalizado (en lugar de un evento reservado) para crear originalmente métricas de clics, costes e impresiones, esas métricas siguen empezando con &quot;AMO&quot;.

| Métrica de tráfico | Descripción |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] o (algunos clientes heredados) [!UICONTROL AMO Clicks] | Número total de clics en Adobes Advertising. |
| [!UICONTROL Adobe Advertising Cost] o (algunos clientes heredados) [!UICONTROL AMO Cost] | El gasto en Adobes Advertising en la divisa del grupo de informes. |
| [!UICONTROL Adobe Advertising Impressions] o (algunos clientes heredados) [!UICONTROL AMO Impressions] | El número de impresiones de Adobe Advertising. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | El número de impresiones servidas para las que se inicializó correctamente la instrumentación de visibilidad. Este valor se calcula como (impresiones instrumentadas: el número de impresiones no medibles). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Cantidad de minutos que se vio un vídeo de Adobe Advertising. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | El número de impresiones que se determinó que no eran visibles. Este valor se calcula como ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | El número de impresiones que se midieron para poder verse según la configuración de ubicación. |
| [!UICONTROL Adobe Advertising Views] | Número de vistas de un anuncio. Se cuenta una vista cuando el usuario inicia el vídeo de Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | El número de vistas para las que se vio al menos el 25 % de un vídeo de Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | El número de vistas para las que se vio al menos el 50 % de un vídeo de Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | El número de vistas para las que se vio al menos el 75 % de un vídeo de Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | El número de vistas para las que se vio el 100 % de un vídeo de Adobe Advertising. |
| [!UICONTROL AMO ID Instances] | El número de veces que [!UICONTROL AMO ID] está configurado. |

## DIMENSION DE ADOBE ADVERTISING

>[!NOTE]
>
>Todas las dimensiones de Adobe Advertising en [!DNL Analytics] van seguidos de &quot;[!DNL (AMO ID)].&quot;

| Dimensión | Datos de Adobe Advertising aplicables | Descripción |
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

## Métricas calculadas personalizadas útiles para el Adobe Advertising

Considere la posibilidad de crear las siguientes métricas para los datos de Adobe Advertising.

* Clics hasta la instancia de la página de aterrizaje ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): Es el % de personas que hicieron clic en el anuncio y llegaron a la página de aterrizaje.
* Tasa Medible ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Tasa de impresiones visibles ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Costo por vista ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Costo por clic ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Datos en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
