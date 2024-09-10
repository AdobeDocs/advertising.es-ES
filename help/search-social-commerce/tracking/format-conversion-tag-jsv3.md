---
title: Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3
description: Consulte el formato de las etiquetas de seguimiento de conversión de JavaScript versión 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
source-git-commit: dda4ff8e7538bc742caa50862575cb4e46a1371d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3

El siguiente formato es para sitios que utilizan HTTPS. Para los sitios que utilizan HTTP, las direcciones URL deben comenzar por &quot;http&quot;.

>[!NOTE]
>
>Para obtener información sobre cuándo usar la versión 2 en comparación con la versión 3, consulte las [preguntas frecuentes sobre las etiquetas de seguimiento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.id5PartnerId=<ID5_PartnerID>
        window.EF = window.EF || {};
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

donde:

* `<ef-userid>` es un identificador de usuario numérico y único que Search, Social y Commerce asigna al anunciante.

* `<ID5_PartnerID>` es el ID de socio ID5 de la organización, que la organización recibe después de firmar un acuerdo con [!DNL ID5]. DSP Incluya esta variable solo cuando la organización use la función de combinación de datos y tenga [segmentos personalizados que hagan un seguimiento de los usuarios asociados con los ID universales ID5](/help/dsp/audiences/universal-ids.md).

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
>* [Formato de etiquetas de seguimiento de conversión de imagen](format-conversion-tag-image.md)
