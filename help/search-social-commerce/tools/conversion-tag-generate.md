---
title: Generación de una etiqueta de seguimiento de conversión de Adobe Advertising
description: Obtenga información sobre cómo crear una etiqueta de conversión de Adobe Advertising para realizar un seguimiento de los eventos de conversión.
exl-id: 617cd808-c4ba-4413-89e4-0f52cb44f44b
feature: Search Tools, Search Tracking
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Generación de una etiqueta de seguimiento de conversión de Adobe Advertising

*Anunciantes solo con seguimiento de conversión de Adobe Advertising*

Cree una etiqueta de conversión independiente para cada conjunto de métricas que desee rastrear y proporcione las etiquetas al anunciante o a la agencia con una lista de páginas web en las que insertar cada una.

>[!NOTE]
>
>Esta función no agrega etiquetas de imagen ni [!DNL JavaScript] a las páginas web del anunciante. Las etiquetas deben añadirse según el procedimiento normal del anunciante para actualizar páginas web.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Especifique el [configuración de etiquetas de conversión](#conversion-tag-settings).

1. Genere la etiqueta:

   * Si el sitio web utiliza HTTP, haga clic en **[!UICONTROL Generate Conversion Tag]**.

   * Si el sitio web se ejecuta en un servidor seguro (HTTPS), haga clic en **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copie la etiqueta del cuadro de diálogo y péguela en las páginas web correspondientes según sea necesario.

>[!NOTE]
>
>Cada métrica de la nueva etiqueta de conversión se enumera automáticamente en [!UICONTROL Admin] > [!UICONTROL Transaction Properties], incluso si no está implementado o si las páginas web en las que está no han recibido ningún clic. Este comportamiento es diferente al comportamiento de las métricas en las etiquetas creadas manualmente o en otro sitio, que no aparecen en [!UICONTROL Admin] > [!UICONTROL Transaction Properties] hasta que una de las páginas web en las que se encuentra reciba un clic. Sin embargo, en todos los casos, cada métrica se excluye inicialmente de los objetivos del portafolio, los informes y las vistas hasta que las ponga a disposición explícitamente. Sin embargo, antes de agregar las métricas a los objetivos del portafolio, considere primero la posibilidad de hacer que las métricas estén disponibles y agregarlas a los informes para verificar cuándo reciben clics.

## Configuración de etiquetas de conversión de Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Tipo de etiqueta que se va a crear:

* *[!UICONTROL Image]:* Para crear una etiqueta de imagen para mostrar una imagen transparente (píxel) de 1 píxel x 1 píxel, que es invisible para los usuarios finales, en la página web. La práctica recomendada es utilizar etiquetas de imagen solo cuando el sitio tiene una directiva contra el uso de etiquetas JavaScript.

* *[!UICONTROL JavaScript]:* Para crear una etiqueta JavaScript.

Para obtener más información sobre las diferencias entre los tipos de etiquetas, consulte &quot;[Preguntas frecuentes sobre la conversión de Adobe Advertising y las etiquetas de seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Una o más métricas de conversión que se deben rastrear cuando un usuario final ve una página que contiene la etiqueta de conversión. Para añadir una métrica a la lista, introduzca el nombre de la métrica en la sección &quot;[!UICONTROL Add new property]&quot; y haga clic en **[!UICONTROL Add]**.

Cuando se realiza el seguimiento de varias métricas, se unen mediante un signo &amp; (`&`) en la etiqueta, como `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Las métricas agregadas a esta lista no se guardan en ninguna parte ni se integran con el del cliente [!UICONTROL Conversions] en la lista [!UICONTROL Admin] pestaña. Sin embargo, las métricas se añaden a la variable [!UICONTROL Conversions] enumera automáticamente una vez que el Adobe Advertising de conversión recopila datos para una métrica, lo que sucede cuando la etiqueta de conversión se implementa en una página y un usuario final completa una transacción que abre esa página.

**[!UICONTROL Include unique transaction IDs]:** (Opcional) Incluye una propiedad de ID de transacción (`ev_transid=<transid>`) en la etiqueta. La opción está seleccionada de forma predeterminada.

Al seleccionar esta opción, el anunciante debe generar un valor único para `<transid>` (por ejemplo, un ID de pedido real) cuando se completa la transacción y se devuelve al Adobe Advertising, como `ev_transid=0123`. El Adobe Advertising utiliza el ID de transacción para eliminar las transacciones duplicadas con el mismo ID de transacción y valor de propiedad. El ID de transacción no puede contener símbolos ampersand (`&`), que se reservan como separadores de parámetros. El ID de transacción se incluye en [el [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que puede utilizar para validar datos dentro de Search, Social y Commerce con los datos del anunciante.

Si los datos no incluyen un ID único por transacción, el Adobe Advertising seguirá generando uno en función del tiempo de transacción.

>[!NOTE]
>
>Si envía [fuentes de ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id.md) con los datos de conversión para conversiones sin conexión, debe enviar el ID de transacción (`ev_transid`) para la parte en línea de la transacción en los datos de fuente de las partes sin conexión de la transacción.

**[!UICONTROL Page is inside FB app]:** Obsoleto

**[!UICONTROL Segment users]:** Obsoleto

**[!UICONTROL JS Version]:** ([!DNL JavaScript] (solo etiquetas) Qué versión de [!DNL JavaScript] etiqueta para crear: *[!UICONTROL v2]* (el valor predeterminado) o *[!UICONTROL v3]*.

Consulte &quot;[Preguntas frecuentes sobre la conversión de Adobe Advertising y las etiquetas de seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; para obtener más información sobre las diferencias.

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Acerca de las herramientas para crear y descodificar etiquetas de seguimiento](tracking-tools-about.md)
>* [Preguntas frecuentes sobre las etiquetas de conversión y seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato de las etiquetas de seguimiento de conversión de imagen](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [La etiqueta de asignación de conversión de JavaScript de Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Administración de las propiedades de transacción de un anunciante](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
