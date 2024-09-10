---
title: Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2
description: Consulte el formato de las etiquetas de seguimiento de conversión de JavaScript versión 2.
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: f73e91c54fb58cbd165ddf4ca652033435fbbede
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2

El siguiente formato es para sitios que utilizan HTTPS. Para los sitios que utilizan HTTP, las direcciones URL deben comenzar por &quot;http&quot;.

>[!NOTE]
>
>Para obtener información sobre cuándo usar la versión 2 en comparación con la versión 3, consulte las [preguntas frecuentes sobre las etiquetas de seguimiento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
window.id5PartnerId=<Your_ID5_PartnerID>
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

* `<ef-userid>` es un identificador de usuario numérico y único que Search, Social y Commerce asigna al anunciante.

* `<Your_ID5_PartnerID>` es el ID de socio ID5 de la organización, que la organización recibe después de firmar un acuerdo con [!DNL ID5]. DSP Incluya esta variable solo cuando la organización use la función de combinación de datos y tenga [segmentos personalizados que hagan un seguimiento de los usuarios asociados con los ID universales ID5](/help/dsp/audiences/universal-ids.md).

* `<propertyname>` es la conversión para realizar el seguimiento. Por ejemplo, si está realizando el seguimiento de una conversión denominada &quot;registro&quot;, la etiqueta incluiría el parámetro `ev_registration=<registration>` y tendría que pasar los ingresos reales de cada transacción (como `ev_registration=1`). Cuando se realiza el seguimiento de varias propiedades, se unen mediante un signo &amp; (`&`), como `ev_registration=<registration>&ev_sale=<sale>` (por ejemplo, `ev_registration=1&ev_sale=12.99`). **Nota:** El nombre de propiedad no puede incluir caracteres especiales.

* `<transid>` es un identificador de transacción único (como un identificador de pedido real) que el anunciante genera y pasa para identificar una transacción. Solo se incluye cuando se selecciona la opción &quot;[!UICONTROL Include unique transaction IDs]&quot;.

  Search, Social y Commerce utilizan el ID de transacción para eliminar las transacciones duplicadas con el mismo ID de transacción y valor de propiedad. El id. de transacción está incluido en [!UICONTROL Transaction Report], que puede usar para validar los datos dentro del Adobe Advertising con los datos del anunciante. **Nota:** Si los datos del anunciante no incluyen un identificador único por transacción, Search, Social y Commerce seguirán generando uno en función del tiempo de transacción.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generar una etiqueta de conversión de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Preguntas más frecuentes acerca de las etiquetas de conversión y seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](format-conversion-tag-jsv2.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](format-conversion-tag-jsv3.md)
>* [Formato de etiquetas de seguimiento de conversión de imagen](format-conversion-tag-image.md)
