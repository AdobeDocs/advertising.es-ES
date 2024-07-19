---
title: Seguimiento de conversión de Adobe Analytics
description: Obtenga información acerca del uso del seguimiento de conversión de Adobe Analytics para sus campañas en Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Seguimiento de conversión de Adobe Analytics

*Anunciantes con una integración de Adobe Advertising-Adobe Analytics solamente*

Para los anunciantes con una integración de Adobe Advertising-Adobe Analytics, Advertising Cloud puede conectar sus clics e impresiones de anuncios con las métricas de participación y conversión del sitio rastreadas por [!DNL Analytics] cuando usa una redirección con token (parámetro `ef_id`) en sus URL de seguimiento de clics para sus [unidades de oferta](/help/search-social-commerce/glossary.md#a-b). Los datos de [!DNL Analytics] se envían automáticamente a Advertising Cloud a través de un archivo de fuente diario.

Consulte &quot;[Información general de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot; para obtener más información sobre la integración.

>[!PREREQUISITES]
>
> Los husos horarios de la cuenta del anunciante de Search, Social y Commerce, los grupos de informes [!DNL Analytics] y las cuentas de red de anuncios deben coincidir. Si no coinciden, se producen variaciones de datos en todos los sistemas.

## Resumen de implementación

1. En [!DNL Analytics], su equipo de implementación de Search, Social y Commerce modifica las siguientes opciones de configuración para cada grupo de informes:

   * La caducidad de `ef_id` [!DNL eVar] se ha cambiado para que coincida con la ventana retrospectiva de clics del anunciante para el Adobe Advertising.

   * El ID de usuario de Adobe Advertising.

   * Eventos estándar y personalizados que se utilizarán para la optimización.

1. En Search, Social y Commerce, su equipo de implementación:

   1. Sincroniza la jerarquía de cuentas de red de anuncios existente en Buscar, Social y Commerce.

   1. Agrega redirecciones con el token &quot;`ef_id`&quot; pasando a las direcciones URL de seguimiento y las publica en la red de anuncios.

   Este paso precede a una redirección al servidor de seguimiento de Adobe Advertising (excepto para los anuncios [!DNL Google Ads] y [!DNL Microsoft Advertising] en los exploradores que admiten el seguimiento paralelo) y agrega un parámetro &quot;ef_id&quot; rellenado dinámicamente a la dirección URL en el momento del clic en el anuncio. Cuando se aplica el seguimiento paralelo, los usuarios finales se envían directamente desde el anuncio a la dirección URL final y la dirección URL de la plantilla de seguimiento (con medición de clics) se carga en segundo plano.

Una vez completada la integración, Search, Social y Commerce reciben automáticamente todos los datos de evento en la página rastreados en [!DNL Analytics] para los grupos de informes que se configuraron.

>[!MORELIKETHIS]
>
>* [Opciones de seguimiento de conversión](conversion-tracking-about.md)
