---
title: Opciones de seguimiento de conversión para Search, Social y Commerce
description: Obtenga información acerca de las opciones de seguimiento de conversión para Search, Social y Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opciones de seguimiento de conversión para Search, Social y Commerce

La publicidad de Adobe puede utilizar datos de conversión de los que se realiza un seguimiento de las siguientes maneras:

* **Adobe Conversiones rastreadas por publicidad:** El anunciante inserta una etiqueta de seguimiento de conversión de publicidad de Adobe en cada página de conversión. La etiqueta envía los datos de conversión a un servidor de seguimiento. Puede utilizar el píxel de terceros heredado o el píxel de origen más reciente. Consulte &quot;[Comparación de cada método de seguimiento de conversión](#conversion-tracking-comparison).&quot;

* **Conversiones de Adobe Analytics:** El anunciante utiliza el seguimiento de Adobe Analytics para todas las conversiones. Esta opción requiere una integración de Adobe Advertising-Adobe Analytics. Consulte &quot;[Seguimiento de conversión de Adobe Analytics](conversion-tracking-analytics.md)&quot; para obtener más información.

* **[!DNL Google Analytics]conversiones:** El anunciante utiliza el [!DNL Google Analytics] para rastrear todas las conversiones. Consulte &quot;[[!DNL Google Ads] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; para obtener más información sobre las conversiones que se sincronizan automáticamente.

* **Conversiones rastreadas por el anunciante:** (Solo clientes de Search, Social y Commerce) El anunciante proporciona a Search, Social y Commerce un archivo de fuente con cualquier combinación de datos de conversión en línea y sin conexión. Consulte &quot;[Seguimiento de conversión mediante una fuente de ID de EF](feed-efid.md)&quot; y &quot;[Seguimiento de conversión mediante una fuente de ID de transacción](feed-transaction-id.md).&quot;

## Comparación de cada método de seguimiento de conversión {#conversion-tracking-comparison}

A medida que las políticas de cookies del explorador siguen siendo más estrictas, es importante comprender sus capacidades de seguimiento actuales e identificar sus mejores opciones a largo plazo.

| Método de seguimiento | Descripción | Limitaciones | Ventajas | ¿Recomendado? |
|----|----|----|----|----|
| Adobe Analytics | Anunciantes con [Adobe Analytics para publicidad](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importar automáticamente sus [!DNL Analytics] Eventos estándar y personalizados para Adobe Advertising para la creación de informes y optimización. | <ul><li>[!DNL Safari] solo permite una retrospectiva de conversión de siete días, que se restablece en las visitas repetidas al sitio durante la ventana retrospectiva.</li><li> Se esperan limitaciones similares en [!DNL Chrome] en 2024.</li></ul> | <ul><li>Integración perfecta con [!DNL Analytics]</li> <li>Consulte los datos de búsqueda de pago en [!DNL Analytics] Analysis Workspace</li><li>Ventajas más allá de la búsqueda de pago</li></ul> | Sí |
| Píxel publicitario de Adobe heredado | Los anunciantes añaden píxeles de imagen publicitaria de Adobe heredados o píxeles de JavaScript a sus páginas de conversión. El píxel se activa cuando un usuario que ha hecho clic en un anuncio llega a la página. Este método se basa en cookies de terceros. | <ul><li>[!DNL Safari] bloquea todo el seguimiento de conversión mediante este método.</li><li>Se esperan limitaciones similares en [!DNL Chrome] en 2024.</li></ul> | El píxel ya está implementado. Sin embargo, aún debe [implementar la etiqueta de asignación ITP adicional](itp-conversion-mapping-tag.md).<br><br>Recomendación: cambie al píxel de origen. | No |
| Adobe Publicidad Píxel de origen | Los anunciantes hacen lo siguiente: <ul><li>Implemente la biblioteca JavaScript para [Servicio de Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) en todo el sitio.</li><li>Añadir la publicidad de Adobe [Etiquetas JavaScript con asignación ITP](itp-conversion-mapping-tag.md) a cualquier página que pueda ser una página de aterrizaje desde un clic de búsqueda (idealmente, en todas las páginas, ya que las páginas de aterrizaje pueden cambiar con el tiempo). La etiqueta permite a la publicidad de Adobe realizar un seguimiento de un evento de conversión que se produce en una página que convierte grandes cantidades en notación científica en la página de aterrizaje.</li><li>Añadir la publicidad de Adobe [Etiqueta de seguimiento de conversión de JavaScript v3](format-conversion-tag-jsv3.md) a páginas de conversión.</li></ul> | <ul><li>[!DNL Safari] solo permite una retrospectiva de conversión de siete días, que se restablece en las visitas repetidas al sitio durante la ventana retrospectiva.</li><li>Se esperan limitaciones similares en [!DNL Chrome] en 2022.</li></ul> | [!DNL Safari] rastrea conversiones durante la retrospectiva de siete días. Debido a que la retrospectiva se restablece en visitas repetidas al sitio durante la ventana retrospectiva, la limitación no afecta a todo [!DNL Safari] usuarios. | No |
| Fuente EFID | Las cuentas de búsqueda del anunciante están configuradas para generar direcciones URL de destino o direcciones URL finales con ID únicos de Adobe Advertising (tokens). Cuando un usuario hace clic en un anuncio, la publicidad de Adobe crea un ID único (`EFID`) y lo muestra al final de la dirección URL final. El sistema cliente del anunciante captura el EFID como identificador único para las conversiones que resultan del clic y lo envía a la publicidad de Adobe en una fuente de ingresos que incluye el EFID, la fecha de transacción y la propiedad de conversión. A continuación, la publicidad de Adobe utiliza el EFID para hacer coincidir la conversión con el clic original. | <ul><li>El anunciante debe tener una forma de registrar el EFID y enviar fuentes automatizadas a Adobe Advertising diariamente.</li><li>Las conversiones se pueden rastrear hasta 180 días (por publicidad de Adobe) o según los límites del sistema del anunciante.</li></ul> | <ul><li>Este método utiliza datos de conversión de origen, por lo que no se ve afectado por las limitaciones de cookies de terceros.</li><li>Las conversiones en línea y sin conexión se pueden enviar en una fuente.</li><li>No se requieren cambios de código ni etiquetas para el sitio.</li></ul> | Sí |
| Fuente de ID de transacción [fuente combinada] | Los anunciantes agregan píxeles de publicidad de Adobe que incluyen un parámetro para un ID de transacción único (`ev_transid=&lt;transid&gt;`) a sus páginas web y Adobe Advertising captura el ID de transacción único que se crea cuando se activa el píxel. El sistema cliente del anunciante también captura el [!UICONTROL Transaction ID] y envía a la publicidad de Adobe una fuente de ingresos para las conversiones sin conexión con coincidencias [!UICONTROL Transaction ID] values | <ul><li>Si el anunciante utiliza el píxel heredado, que [!DNL Safari] bloquea la activación y, a continuación, el ID no se captura para utilizarlo con los datos sin conexión.</li><li>La fuente no está automatizada.</li></ul> | <ul><li>Si implementa el píxel de origen, la variable [!UICONTROL Transaction ID] se captura en [!DNL Safari].</li><li>Proporciona seguimiento de eventos de conversión sin conexión/aprobados.</li></ul> | No |
| Conversiones de Google | Conversiones seguidas con [!DNL Google Analytics] Las etiquetas de se importan automáticamente a la publicidad de Adobe de a través de una conexión API. Cada nombre de conversión tiene un `&quot;GGL_&quot;` prefijo. | <ul><li>Google no suele realizar el seguimiento de datos sin conexión.</li><li>No se incluyen las conversiones de publicidad de Microsoft®.</li></ul> | Google utiliza el aprendizaje automático para extrapolar &quot;[conversiones modeladas](https://support.google.com/google-ads/answer/10081327).&quot; | No |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Seguimiento de conversión de Adobe Analytics](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Seguimiento de conversión mediante una fuente de ID de EF](/help/search-social-commerce/tracking/feed-efid.md)
>* [Seguimiento de conversión mediante una fuente de ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id.md)

