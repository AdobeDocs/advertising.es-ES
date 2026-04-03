---
title: Formato de las etiquetas de seguimiento de conversión de imagen
description: Haga referencia al formato de las etiquetas de seguimiento de conversión de imagen.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TQMACo5-LkbCU2SiMmUE-ZDBRTb8NERQPQ9ISzU0DdU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 0%

---

# Formato de las etiquetas de seguimiento de conversión de imagen

>[!NOTE]
>
>Para obtener información sobre cuándo usar etiquetas de imagen en comparación con las etiquetas de JavaScript, consulte las [preguntas frecuentes sobre las etiquetas de seguimiento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Etiquetas no seguras para sitios con HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Etiquetas seguras para sitios con HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

donde:

* `<ef-userid>` es un identificador de usuario numérico y único que Search, Social y Commerce asigna al anunciante.

* `<propertyname>` es la conversión para realizar el seguimiento. Por ejemplo, si está realizando el seguimiento de una conversión denominada &quot;registro&quot;, la etiqueta incluiría el parámetro `ev_registration=<registration>` y tendría que pasar los ingresos reales de cada transacción (como `ev_registration=1`). Cuando se realiza el seguimiento de varias propiedades, se unen mediante un signo &amp; (`&`), como `ev_registration=<registration>&ev_sale=<sale>` (por ejemplo, `ev_registration=1&ev_sale=12.99`). **Nota:** El nombre de propiedad no puede incluir caracteres especiales.

* `<transid>` es un identificador de transacción único (como un identificador de pedido real) que el anunciante genera y pasa para identificar una transacción. Solo se incluye cuando se selecciona la opción &quot;[!UICONTROL Include unique transaction IDs]&quot;.

  Search, Social y Commerce utilizan el ID de transacción para eliminar las transacciones duplicadas con el mismo ID de transacción y valor de propiedad. El id. de transacción está incluido en [!UICONTROL Transaction Report], que puede usar para validar datos en Adobe Advertising con los datos del anunciante. **Nota:** Si los datos del anunciante no incluyen un identificador único por transacción, Search, Social y Commerce seguirán generando uno en función del tiempo de transacción.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generar una etiqueta de conversión de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Preguntas más frecuentes acerca de las etiquetas de conversión y seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](format-conversion-tag-jsv2.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](format-conversion-tag-jsv3.md)
