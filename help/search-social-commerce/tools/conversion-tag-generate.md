---
title: Generar e implementar una etiqueta de seguimiento de conversión de Adobe Advertising
description: Obtenga información sobre cómo crear una etiqueta de conversión de Adobe Advertising para realizar un seguimiento de los eventos de conversión.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: 1113c9f6ff8446d075dc9b90441f4119eb657598
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Generar e implementar una etiqueta de seguimiento de conversión de Adobe Advertising

*Anunciantes con solo seguimiento de conversión de Adobe Advertising*

Cree una etiqueta de conversión independiente para cada conjunto de métricas que quiera rastrear. Puede generar etiquetas en Search, Social y Commerce o utilizando etiquetas en Adobe Experience Platform (anteriormente conocido como Adobe Experience Platform Launch) con la extensión de Adobe Advertising.

<!--

## (New UI) Generate and implement a conversion-tracking tag within Search, Social, & Commerce

>[!NOTE]
>
>This feature doesn't add image tags or [!DNL JavaScript] tags to the advertiser's webpages. Provide the tags to the advertiser or agency with a list of webpages on which to insert each. The tags must be added according to the advertiser's normal procedure for updating webpages.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversions]**.

1. In the main toolbar, click **[!UICONTROL Conversion Tag]**.

1. Specify the [conversion tag settings](#conversion-tag-settings).

1. Click **[!UICONTROL Generate]**.
   
1. Click **[!UICONTROL Copy]** to copy the tag to your clipboard. Give the tag to the advertiser or agency to implement.

>[!NOTE]
>
>Each metric in the new conversion tag is automatically listed in [!UICONTROL Admin] > [!UICONTROL Conversions], even if it isn't implemented or the webpages that it's on haven't received any clicks. This behavior is different from the behavior of metrics in tags created manually or elsewhere, which aren't listed in [!UICONTROL Admin] > [!UICONTROL Conversions] until one of the webpages that it's on has received a click. In all cases, however, each metric is initially excluded from portfolio objectives, reports, and views until you explicitly make them available. Before you add the metrics to portfolio objectives, consider first making the metrics available and adding them to reports to verify when they receive clicks.

### Adobe Advertising conversion tag settings {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** The type of tag to create:

* *[!UICONTROL JavaScript]:* To create a JavaScript tag.

* *[!UICONTROL Image]:* To create an image tag to display a 1-pixel x 1-pixel transparent image (pixel), which is invisible to end users, on the webpage. The best practice is to use image tags only when the site has a policy against using JavaScript tags.

For more information about the differences between the tag types, see "[FAQs about Adobe Advertising conversion and page view tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)."

**[!UICONTROL Include unique transaction IDs]:** (Optional) Includes a transaction ID property (`ev_transid=<transid>`) in the tag. The option is selected by default.

When you select this option, the advertiser must generate a unique value for `<transid>` (for example, an actual order ID) when the transaction is complete and pass it back to Adobe Advertising, such as `ev_transid=0123`. Adobe Advertising uses the transaction ID to eliminate duplicate transactions with the same transaction ID and property value. The transaction ID can't contain ampersand symbols (`&`), which are reserved as parameter separators. The transaction ID is included in [the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), which you can use to validate data within Search, Social, & Commerce with the advertiser's data.

If the data doesn't include a unique ID per transaction, then Adobe Advertising still generates one based on transaction time.

>[!NOTE]
>
>If you send [transaction ID feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) with conversion data for offline conversions, then you must submit the transaction ID (`ev_transid`) for the online part of the transaction in the feed data for offline parts of the transaction.

**[!UICONTROL JS Version]:** ([!DNL JavaScript] tags only) Which version of the [!DNL JavaScript] tag to create: *[!UICONTROL v2]* (the default) or *[!UICONTROL v3]*.

**[!UICONTROL Security]:** The security protocol for your website create: *[!UICONTROL Standard]* (for websites that use HTTP) or *[!UICONTROL Secure]* (for websites that use HTTPs).

**[!UICONTROL Properties]:** One or more conversion metrics to be tracked when an end user views a page containing the conversion tag. To add a metric to the list, enter the metric name in the "[!UICONTROL Property name]" field and click **[!UICONTROL Add]**.

When multiple metrics are tracked, they're joined by an ampersand (`&`) in the tag, such as `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metrics added to this list aren't saved anywhere or integrated with the client's [!UICONTROL Conversions] list on the [!UICONTROL Admin] tab. However, metrics are added to the client's [!UICONTROL Conversions] list automatically once Adobe Advertising actually gathers data for a metric, which happens when the conversion tag is implemented on a page and an end user completes a transaction that opens that page.

-->
## &#x200B;<!-- (Legacy UI) --> Generar e implementar una etiqueta de seguimiento de conversión en Search, Social y Commerce

>[!NOTE]
>
>Esta característica no agrega etiquetas de imagen ni etiquetas [!DNL JavaScript] a las páginas web del anunciante. Proporcione las etiquetas al anunciante o a la agencia con una lista de páginas web en las que insertar cada una. Las etiquetas deben añadirse según el procedimiento normal del anunciante para actualizar páginas web.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Especifique la [configuración de la etiqueta de conversión](#conversion-tag-settings).

1. Genere la etiqueta:

   * Si el sitio web utiliza HTTP, haga clic en **[!UICONTROL Generate Conversion Tag]**.

   * Si el sitio web se ejecuta en un servidor seguro (HTTPS), haga clic en **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copie la etiqueta del cuadro de diálogo y péguela en las páginas web correspondientes según sea necesario.

>[!NOTE]
>
>Cada métrica de la nueva etiqueta de conversión se muestra automáticamente en [!UICONTROL Admin] > [!UICONTROL Conversions], aunque no esté implementada o las páginas web en las que se encuentra no hayan recibido ningún clic. Este comportamiento es diferente al comportamiento de las métricas en las etiquetas creadas manualmente o en cualquier otra parte, que no aparecen en [!UICONTROL Admin] > [!UICONTROL Conversions] hasta que una de las páginas web en las que se encuentra recibe un clic. Sin embargo, en todos los casos, cada métrica se excluye inicialmente de los objetivos del portafolio, los informes y las vistas hasta que las ponga a disposición explícitamente. Sin embargo, antes de agregar las métricas a los objetivos del portafolio, considere primero la posibilidad de hacer que las métricas estén disponibles y agregarlas a los informes para verificar cuándo reciben clics.

### Configuración de etiquetas de conversión Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Tipo de etiqueta que se va a crear:

* *[!UICONTROL Image]:* Para crear una etiqueta de imagen para mostrar una imagen transparente (píxel) de 1 píxel x 1 píxel, que es invisible para los usuarios finales, en la página web. La práctica recomendada es utilizar etiquetas de imagen solo cuando el sitio tiene una directiva contra el uso de etiquetas de JavaScript.

* *[!UICONTROL JavaScript]:* Para crear una etiqueta JavaScript.

Para obtener más información acerca de las diferencias entre los tipos de etiquetas, consulte &quot;[Preguntas frecuentes acerca de las etiquetas de conversión de Adobe Advertising y de seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)&quot;.

**[!UICONTROL Tag Properties]:** Una o más métricas de conversión se seguirán cuando un usuario final vea una página que contenga la etiqueta de conversión. Para agregar una métrica a la lista, ingrese el nombre de la métrica en el campo &quot;[!UICONTROL Add new property]&quot; y haga clic en **[!UICONTROL Add]**.

Cuando se realiza el seguimiento de varias métricas, se unen mediante un signo &amp; (`&`) en la etiqueta, como `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Las métricas agregadas a esta lista no se guardan en ninguna parte ni se integran con la lista [!UICONTROL Conversions] del cliente en la ficha [!UICONTROL Admin]. Sin embargo, las métricas se agregan automáticamente a la lista [!UICONTROL Conversions] del cliente una vez que Adobe Advertising recopila datos para una métrica, lo que sucede cuando la etiqueta de conversión se implementa en una página y un usuario final completa una transacción que abre esa página.

**[!UICONTROL Include unique transaction IDs]:** (opcional) incluye una propiedad de ID de transacción (`ev_transid=<transid>`) en la etiqueta. La opción está seleccionada de forma predeterminada.

Al seleccionar esta opción, el anunciante debe generar un valor único para `<transid>` (por ejemplo, un identificador de pedido real) cuando se complete la transacción y devolvérsela a Adobe Advertising, como `ev_transid=0123`. Adobe Advertising utiliza el ID de transacción para eliminar las transacciones duplicadas con el mismo ID de transacción y valor de propiedad. El id. de transacción no puede contener símbolos ampersand (`&`), que están reservados como separadores de parámetros. El id. de transacción se incluye en [el [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que puede usar para validar datos en Search, Social y Commerce con los datos del anunciante.

Si los datos no incluyen un ID único por transacción, Adobe Advertising seguirá generando uno en función del tiempo de transacción.

>[!NOTE]
>
>Si envía [fuentes de ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id.md) con datos de conversión para conversiones sin conexión, debe enviar el ID de transacción (`ev_transid`) para la parte en línea de la transacción en los datos de fuente de las partes sin conexión de la transacción.

**[!UICONTROL Page is inside FB app]:** obsoleto

**[!UICONTROL Segment users]:** obsoleto

**[!UICONTROL JS Version]:** ([!DNL JavaScript] etiquetas solamente) Qué versión de la etiqueta [!DNL JavaScript] crear: *[!UICONTROL v2]* (la predeterminada) o *[!UICONTROL v3]*.

Consulte &quot;[Preguntas más frecuentes acerca de las etiquetas de conversión de Adobe Advertising y seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)&quot;. para obtener más información sobre las diferencias.

## Implementar etiquetas de seguimiento de conversión mediante etiquetas de Adobe Experience Platform y la extensión de Adobe Advertising

Puede configurar el seguimiento de conversiones para Search, Social y Commerce mediante etiquetas en Adobe Experience Platform. Las etiquetas están disponibles para los clientes de Adobe CX Enterprise como una función incluida que añade valor.

Se requieren las siguientes tareas para configurar las etiquetas de seguimiento de conversión de Búsqueda, Social y Commerce desde la interfaz de usuario de Experience Platform o desde la interfaz de usuario de Recopilación de datos de Experience Platform. Para obtener información e instrucciones completas para configurar las etiquetas, consulte la Guía de etiquetas de Experience Platform, que comienza con &quot;[Información general sobre etiquetas](https://experienceleague.adobe.com/es/docs/experience-platform/tags/home)&quot; y &quot;[Guía de inicio rápido](https://experienceleague.adobe.com/es/docs/experience-platform/tags/get-started/quick-start)&quot;.

>[!PREREQUISITES]
>
>Para instalar la extensión de etiqueta necesaria, solicite al administrador de la organización acceso a las funciones de recopilación de datos en la interfaz de usuario, incluido el permiso `manage_properties`.

1. En la [IU de recopilación de datos](https://experience.adobe.com/#/data-collection/), instale la [extensión](https://experienceleague.adobe.com/es/docs/experience-platform/tags/ui/extensions/overview) de Adobe Advertising:

   1. En la propiedad aplicable, abra el catálogo de extensiones y seleccione **Adobe Advertising**.

   1. En el menú desplegable, seleccione **SSC** (para Search, Social y Commerce).

   1. En el campo **SSC UserID**, escribe el identificador numérico de usuario para la cuenta de Search, Social y Commerce de tu organización.

      Si no conoce su ID de usuario, póngase en contacto con el equipo de cuenta de Adobe.

   1. Haga clic en **Guardar**.

1. Cree una nueva regla (por ejemplo, &quot;form_completes&quot;) para almacenar en déclencheur la etiqueta de conversión Buscar, Social y Commerce:

   1. En la sección Configuración de eventos:

      1. Seleccione los siguientes valores:

         **Extensión:** `Core`

         **Tipo de evento:** `Library Loaded (Page Top)`

      1. Haga clic en **Conservar cambios**.

   1. En la sección Configuración de condición:

      1. Especifique los siguientes valores:

         **Tipo de lógica:** `Regular`

         **Extensión:** `Core`

         **Tipo de condición:** `Path Without Query String`

         **Devolver verdadero si la ruta de acceso es igual a:** Ruta de acceso donde se debe realizar el seguimiento de la conversión (por ejemplo, `/form_complete`).

      1. Haga clic en **Conservar cambios**.

   1. En la sección Configuración de la acción:

      1. Especifique los siguientes valores:

         **Extensión:** `Adobe Advertising`

         **Tipo de acción:** `AMO Measurement`

         **Nombre de propiedad de conversión:** El nombre de la propiedad de conversión (por ejemplo, `form_completes`).

         **Valor:** Valor numérico de la propiedad de conversión (por ejemplo `1` para realizar el seguimiento de form_completes) o elija un [elemento de datos](https://experienceleague.adobe.com/es/docs/experience-platform/tags/ui/data-elements) existente.

      1. Haga clic en **Conservar cambios**.

   1. Guarde la regla.

1. Publique los cambios.

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Acerca de las herramientas para crear y descodificar etiquetas de seguimiento](tracking-tools-about.md)
>* [Preguntas más frecuentes acerca de las etiquetas de conversión y seguimiento de vista de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato de etiquetas de seguimiento de conversión de imagen](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Etiqueta de asignación de conversión de Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Acerca de la administración de las métricas de conversión de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
