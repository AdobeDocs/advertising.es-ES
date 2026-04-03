---
title: Seguimiento de conversión de Adobe Analytics
description: Obtenga información acerca del uso del seguimiento de conversión de Adobe Analytics para sus campañas en Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
TQID: https://experienceleague.adobe.com/CM0S4RvR4RJ5Ylta5EJTdZh-VDDHYIfa7Qsd1Dm4D78
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 0%

---

# Seguimiento de conversión de Adobe Analytics

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

Para los anunciantes con una integración Adobe Advertising-Adobe Analytics, Advertising Cloud puede conectar sus clics e impresiones de anuncios con las métricas de participación y conversión del sitio rastreadas por [!DNL Analytics] cuando utiliza una redirección con token (parámetro `ef_id`) en sus URL de seguimiento de clics para sus [unidades de oferta](/help/search-social-commerce/glossary.md#a-b). Los datos de [!DNL Analytics] se envían automáticamente a Advertising Cloud mediante un archivo de fuente diario.

Consulte &quot;[Información general de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview){target="_blank"}&quot; para obtener más información sobre la integración.

>[!PREREQUISITES]
>
> Los husos horarios de la cuenta del anunciante de Search, Social y Commerce, los grupos de informes [!DNL Analytics] y las cuentas de red de anuncios deben coincidir. Si no coinciden, se producen variaciones de datos en todos los sistemas.

## Resumen de implementación

1. En [!DNL Analytics], su equipo de implementación de Search, Social y Commerce modifica las siguientes opciones de configuración para cada grupo de informes:

   * La caducidad de `ef_id` [!DNL eVar] se ha cambiado para que coincida con la ventana retrospectiva de clics del anunciante para Adobe Advertising.

   * El ID de usuario de Adobe Advertising.

   * Eventos estándar y personalizados que se utilizarán para la optimización.

1. En Search, Social y Commerce, su equipo de implementación:

   1. Sincroniza la jerarquía de cuentas de red de anuncios existente en Buscar, Social y Commerce.

   1. Agrega redirecciones con el token &quot;`ef_id`&quot; pasando a las direcciones URL de seguimiento y las publica en la red de anuncios.

   Este paso antepone una redirección al servidor de seguimiento de Adobe Advertising (excepto para los anuncios [!DNL Google Ads] y [!DNL Microsoft Advertising] en los exploradores que admiten el seguimiento paralelo) y agrega un parámetro &quot;ef_id&quot; rellenado dinámicamente a la dirección URL en el momento de hacer clic en el anuncio. Cuando se aplica el seguimiento paralelo, los usuarios finales se envían directamente desde el anuncio a la dirección URL final y la dirección URL de la plantilla de seguimiento (con medición de clics) se carga en segundo plano.

Una vez completada la integración, Search, Social y Commerce reciben automáticamente todos los datos de evento en la página rastreados en [!DNL Analytics] para los grupos de informes que se configuraron.

>[!MORELIKETHIS]
>
>* [Opciones de seguimiento de conversión](conversion-tracking-about.md)
