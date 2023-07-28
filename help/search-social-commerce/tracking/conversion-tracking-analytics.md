---
title: Seguimiento de conversión de Adobe Analytics
description: Obtenga información acerca del uso del seguimiento de conversión de Adobe Analytics para sus campañas en Adobe Advertising.
exl-id: 0ed1d059-829a-4090-950d-41cbcc27b3ac
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Seguimiento de conversión de Adobe Analytics

*Anunciantes solo con una integración de Adobe Advertising y Adobe Analytics*

Para los anunciantes con una integración de Adobe Advertising y Adobe Analytics, Advertising Cloud puede conectar los clics y las impresiones de sus anuncios con las métricas de participación y conversión del sitio rastreadas por [!DNL Analytics] cuando se usa una redirección con el token (`ef_id` ) en las URL de seguimiento de clics de su [unidades de oferta](/help/search-social-commerce/glossary.md#a-b). El [!DNL Analytics] los datos se envían automáticamente a Advertising Cloud mediante un archivo de fuente diario.

Consulte &quot;[Información general de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot; para obtener más información sobre la integración.

>[!PREREQUISITES]
>
> Zonas horarias en la cuenta del anunciante de Search, Social y Commerce, [!DNL Analytics] los grupos de informes y las cuentas de red de publicidad deben coincidir. Si no coinciden, existirán variaciones de datos entre sistemas.

## Resumen de implementación

1. Entrada [!DNL Analytics], su equipo de implementación de Search, Social y Commerce modifica las siguientes opciones de configuración para cada grupo de informes:

   * La caducidad del `ef_id` El eVar se cambia para que coincida con la ventana retrospectiva de clics del anunciante para el Adobe Advertising.

   * El ID de usuario de Adobe Advertising.

   * Eventos estándar y personalizados que se utilizarán para la optimización.

1. En Search, Social y Commerce, su equipo de implementación:

   1. Sincroniza la jerarquía de cuentas de red de anuncios existente en Buscar, Social y Comercio.

   1. Agrega redirecciones con &quot;`ef_id`&quot; pasando a las URL de seguimiento y las publica en la red de publicidad.

   Este paso precede a una redirección al servidor de seguimiento de Adobe Advertising (excepto para [!DNL Google Ads] y [!DNL Microsoft Advertising] añade un parámetro &quot;ef_id&quot; rellenado dinámicamente a la dirección URL en el momento de hacer clic en el anuncio. Cuando se aplica el seguimiento paralelo, los usuarios finales se envían directamente desde el anuncio a la dirección URL final y la dirección URL de la plantilla de seguimiento (con medición de clics) se carga en segundo plano.

Una vez completada la integración, Search, Social y Commerce reciben automáticamente todos los datos de evento en la página rastreados en [!DNL Analytics] para los grupos de informes que se configuraron.

>[!MORELIKETHIS]
>
>* [Opciones de seguimiento de conversión](conversion-tracking-about.md)
