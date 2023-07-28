---
title: Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2
description: Consulte el formato de las etiquetas de seguimiento de conversión de JavaScript versión 2.
exl-id: c4845694-10ac-41f8-bafb-ca813e42d190
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2

El siguiente formato es para sitios que utilizan HTTPS. Para los sitios que utilizan HTTP, las direcciones URL deben comenzar por &quot;http&quot;.

>[!NOTE]
>
>Para obtener información sobre cuándo usar la versión 2 frente a la versión 3, consulte la [Preguntas frecuentes sobre las etiquetas de seguimiento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

donde:

* `<ef-userid>` es un ID de usuario numérico y único que Search, Social y Commerce asigna al anunciante.

* `<propertyname>` es la conversión de la que se realizará un seguimiento. Por ejemplo, si está rastreando una conversión llamada &quot;registro&quot;, la etiqueta incluiría el parámetro `ev_registration=<registration>`y deberá pasar los ingresos reales de cada transacción (por ejemplo, `ev_registration=1`). Cuando se realiza el seguimiento de varias propiedades, se unen mediante un signo &amp; (`&`), como `ev_registration=<registration>&ev_sale=<sale>` (por ejemplo, `ev_registration=1&ev_sale=12.99`). **Nota:**  El nombre de la propiedad no puede incluir caracteres especiales.

* `<transid>` es un ID de transacción único (como un ID de pedido real) que el anunciante genera y pasa para identificar una transacción. Se incluye solo cuando el parámetro &quot;[!UICONTROL Include unique transaction IDs]La opción &quot; está seleccionada.

  Search, Social y Commerce utilizan el ID de transacción para eliminar las transacciones duplicadas con el mismo ID de transacción y valor de propiedad. El ID de transacción se incluye en la [!UICONTROL Transaction Report], que puede utilizar para validar datos dentro del Adobe Advertising con los datos del anunciante. **Nota:** Si los datos del anunciante no incluyen un ID único por transacción, Search, Social y Commerce seguirán generando uno en función del tiempo de transacción.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generación de una etiqueta de conversión de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Preguntas frecuentes sobre las etiquetas de conversión y seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](format-conversion-tag-jsv2.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de imagen](format-conversion-tag-image.md)
