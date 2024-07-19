---
title: Generación de una etiqueta de seguimiento de conversión de Adobe Advertising
description: Obtenga información sobre cómo crear una etiqueta de conversión de Adobe Advertising para realizar un seguimiento de los eventos de conversión.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Generación de una etiqueta de seguimiento de conversión de Adobe Advertising

*Anunciantes con solo seguimiento de conversión de Adobe Advertising*

Cree una etiqueta de conversión independiente para cada conjunto de métricas que desee rastrear y proporcione las etiquetas al anunciante o a la agencia con una lista de páginas web en las que insertar cada una.

>[!NOTE]
>
>Esta característica no agrega etiquetas de imagen ni etiquetas [!DNL JavaScript] a las páginas web del anunciante. Las etiquetas deben añadirse según el procedimiento normal del anunciante para actualizar páginas web.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Especifique la [configuración de la etiqueta de conversión](#conversion-tag-settings).

1. Genere la etiqueta:

   * Si el sitio web utiliza HTTP, haga clic en **[!UICONTROL Generate Conversion Tag]**.

   * Si el sitio web se ejecuta en un servidor seguro (HTTPS), haga clic en **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copie la etiqueta del cuadro de diálogo y péguela en las páginas web correspondientes según sea necesario.

>[!NOTE]
>
>Cada métrica de la nueva etiqueta de conversión se muestra automáticamente en [!UICONTROL Admin] > [!UICONTROL Conversions], aunque no esté implementada o las páginas web en las que se encuentra no hayan recibido ningún clic. Este comportamiento es diferente al comportamiento de las métricas en las etiquetas creadas manualmente o en cualquier otra parte, que no aparecen en [!UICONTROL Admin] > [!UICONTROL Conversions] hasta que una de las páginas web en las que se encuentra recibe un clic. Sin embargo, en todos los casos, cada métrica se excluye inicialmente de los objetivos del portafolio, los informes y las vistas hasta que las ponga a disposición explícitamente. Sin embargo, antes de agregar las métricas a los objetivos del portafolio, considere primero la posibilidad de hacer que las métricas estén disponibles y agregarlas a los informes para verificar cuándo reciben clics.

## Configuración de etiquetas de conversión de Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Tipo de etiqueta que se va a crear:

* *[!UICONTROL Image]:* Para crear una etiqueta de imagen para mostrar una imagen transparente (píxel) de 1 píxel x 1 píxel, que es invisible para los usuarios finales, en la página web. La práctica recomendada es utilizar etiquetas de imagen solo cuando el sitio tiene una directiva contra el uso de etiquetas de JavaScript.

* *[!UICONTROL JavaScript]:* Para crear una etiqueta JavaScript.

Para obtener más información acerca de las diferencias entre los tipos de etiquetas, consulte &quot;[Preguntas frecuentes acerca de la conversión de Adobe Advertising y las etiquetas de seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)&quot;.

**[!UICONTROL Tag Properties]:** Una o más métricas de conversión se seguirán cuando un usuario final vea una página que contenga la etiqueta de conversión. Para agregar una métrica a la lista, ingrese el nombre de la métrica en el campo &quot;[!UICONTROL Add new property]&quot; y haga clic en **[!UICONTROL Add]**.

Cuando se realiza el seguimiento de varias métricas, se unen mediante un signo &amp; (`&`) en la etiqueta, como `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Las métricas agregadas a esta lista no se guardan en ninguna parte ni se integran con la lista [!UICONTROL Conversions] del cliente en la ficha [!UICONTROL Admin]. Sin embargo, las métricas se agregan automáticamente a la lista [!UICONTROL Conversions] del cliente una vez que el Adobe Advertising recopila datos para una métrica, lo que sucede cuando la etiqueta de conversión se implementa en una página y un usuario final completa una transacción que abre esa página.

**[!UICONTROL Include unique transaction IDs]:** (opcional) incluye una propiedad de ID de transacción (`ev_transid=<transid>`) en la etiqueta. La opción está seleccionada de forma predeterminada.

Al seleccionar esta opción, el anunciante debe generar un valor único para `<transid>` (por ejemplo, un identificador de pedido real) cuando se complete la transacción y devolverla al Adobe Advertising, como `ev_transid=0123`. El Adobe Advertising utiliza el ID de transacción para eliminar las transacciones duplicadas con el mismo ID de transacción y valor de propiedad. El id. de transacción no puede contener símbolos ampersand (`&`), que están reservados como separadores de parámetros. El id. de transacción se incluye en [el [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que puede usar para validar datos en Search, Social y Commerce con los datos del anunciante.

Si los datos no incluyen un ID único por transacción, el Adobe Advertising seguirá generando uno en función del tiempo de transacción.

>[!NOTE]
>
>Si envía [fuentes de ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id.md) con datos de conversión para conversiones sin conexión, debe enviar el ID de transacción (`ev_transid`) para la parte en línea de la transacción en los datos de fuente de las partes sin conexión de la transacción.

**[!UICONTROL Page is inside FB app]:** obsoleto

**[!UICONTROL Segment users]:** obsoleto

**[!UICONTROL JS Version]:** ([!DNL JavaScript] etiquetas solamente) Qué versión de la etiqueta [!DNL JavaScript] crear: *[!UICONTROL v2]* (la predeterminada) o *[!UICONTROL v3]*.

Consulte &quot;[Preguntas frecuentes acerca de la conversión de Adobe Advertising y las etiquetas de seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)&quot;. para obtener más información sobre las diferencias.

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Acerca de las herramientas para crear y descodificar etiquetas de seguimiento](tracking-tools-about.md)
>* [Preguntas más frecuentes acerca de las etiquetas de conversión y seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato de etiquetas de seguimiento de conversión de imagen](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Etiqueta de asignación de conversión de JavaScript de Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Acerca de la administración de las métricas de conversión de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
