---
title: Formato de las etiquetas de seguimiento de conversión de imagen
description: Haga referencia al formato de las etiquetas de seguimiento de conversión de imagen.
source-git-commit: b230c593d93dfa868b8f075939fc9940ea74fa13
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Formato de las etiquetas de seguimiento de conversión de imagen

>[!NOTE]
>
>Para obtener información sobre cuándo usar etiquetas de imagen y cuándo usar etiquetas de JavaScript, consulte la [Preguntas frecuentes sobre las etiquetas de seguimiento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Etiquetas no seguras para sitios con HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Etiquetas seguras para sitios con HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

donde:

* `<ef-userid>` es un ID de usuario numérico y único que Search, Social y Commerce asigna al anunciante.

* `<propertyname>` es la conversión de la que se realizará un seguimiento. Por ejemplo, si está rastreando una conversión llamada &quot;registro&quot;, la etiqueta incluiría el parámetro `ev_registration=<registration>`y deberá pasar los ingresos reales de cada transacción (por ejemplo, `ev_registration=1`). Cuando se realiza el seguimiento de varias propiedades, se unen mediante un signo &amp; (`&`), como `ev_registration=<registration>&ev_sale=<sale>` (por ejemplo, `ev_registration=1&ev_sale=12.99`). **Nota:**  El nombre de la propiedad no puede incluir caracteres especiales.

* `<transid>` es un ID de transacción único (como un ID de pedido real) que el anunciante genera y pasa para identificar una transacción. Se incluye solo cuando el parámetro &quot;[!UICONTROL Include unique transaction IDs]La opción &quot; está seleccionada.

  Search, Social y Commerce utilizan el ID de transacción para eliminar las transacciones duplicadas con el mismo ID de transacción y valor de propiedad. El ID de transacción se incluye en la [!UICONTROL Transaction Report], que puede utilizar para validar datos dentro del Adobe Advertising con los datos del anunciante. **Nota:** Si los datos del anunciante no incluyen un ID único por transacción, Search, Social y Commerce seguirán generando uno en función del tiempo de transacción.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generación de una etiqueta de conversión de publicidad de Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Preguntas frecuentes sobre las etiquetas de conversión y seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](format-conversion-tag-jsv2.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](format-conversion-tag-jsv3.md)
