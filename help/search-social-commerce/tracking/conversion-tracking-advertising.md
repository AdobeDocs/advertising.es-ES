---
title: Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising
description: Obtenga información acerca del uso de las etiquetas de seguimiento de conversión de Adobe Advertising.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising

Adobe Advertising realiza un seguimiento de las conversiones resultantes de los clics en las publicidades utilizando las etiquetas de seguimiento de conversión de Adobe Advertising que se insertan en las páginas web que se abren cuando se produce un evento de conversión, como una página de &quot;éxito&quot;. Las etiquetas incluyen información incrustada para enviar los datos de transacción, junto con la cookie de publicidad de Adobe del usuario, a un servidor de seguimiento, desde el cual la transacción se acredita al clic o impresión del anuncio correspondiente (según la configuración de atribución de conversión del anunciante).

>[!NOTE]
>
>Si el usuario no tiene una cookie válida, la publicidad en Adobe no informa de la conversión.

Para cada conjunto de métricas de conversión que desee rastrear, debe crear una etiqueta de conversión independiente. Proporcione las etiquetas al anunciante o a la agencia con una lista de páginas web en las que insertar cada una. Puede generar cualquiera de los siguientes tipos de etiquetas de conversión. Consulte &quot;[Generación de una etiqueta de conversión de publicidad de Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot; para obtener instrucciones.

* (Recomendado) Etiquetas JavaScript (versión 3 o 2), que no son visibles en las páginas web.

* Las etiquetas de imagen del HTML muestran imágenes transparentes de 1 píxel x 1 píxel (píxeles), que son invisibles para los usuarios finales, en las páginas web. Utilice etiquetas de imagen únicamente cuando la empresa tenga una política de no utilizar etiquetas JavaScript.

Para obtener más información sobre las diferencias entre los tipos de etiquetas, consulte &quot;[Preguntas frecuentes sobre las etiquetas de seguimiento de conversión de Advertising Cloud](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* Esta función no agrega etiquetas de imagen ni etiquetas JavaScript a las páginas web del anunciante. Las etiquetas deben añadirse según el procedimiento normal del anunciante para actualizar páginas web.
>* Asegúrese de tener en cuenta cuánto tiempo se tardará en implementar las etiquetas. Según las políticas de la empresa, la implementación puede tardar semanas o incluso meses.


## Características de las etiquetas de seguimiento de conversión de Adobe Advertising

El píxel de seguimiento de conversión permite a la publicidad de Adobe hacer lo siguiente:

* Rastree e informe de datos de conversión en el nivel de palabra clave para campañas de búsqueda.

* Rastree e informe de datos de conversión a nivel de anuncio (creativo) en todos los canales de marketing (búsqueda de pago y visualización), lo que puede facilitar las pruebas creativas.

* Rastree y genere informes de datos de conversión en el nivel de transacción en todos los canales de marketing.

* Muestre cómo se distribuyen las conversiones entre los distintos canales de marketing para que pueda ver cuál es la más eficaz.

* Informar y optimizar en diferentes niveles de atribución (como la atribución de conversiones al último evento relacionado o la ponderación uniforme de todos los eventos).

* Proporcionar visibilidad sobre las ayudas de clic (palabras clave de búsqueda o ubicaciones que hayan contribuido a un canal de conversión) y las ayudas de canal (eventos de usuario que han contribuido a un canal de conversión, posiblemente en varios canales de marketing).

* Proporcione visibilidad sobre la distribución geográfica y los dominios de referencia del tráfico y las conversiones del sitio, para que pueda refinar la segmentación geográfica y del sitio web.

* Analice las tendencias de día de la semana o dentro del día, que se pueden utilizar para mejorar las tasas de conversión.

>[!MORELIKETHIS]
>
>* [Opciones de seguimiento de conversión](conversion-tracking-about.md)
>* [Generación de una etiqueta de conversión de publicidad de Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](format-conversion-tag-jsv2.md)
>* [Formato de las etiquetas de seguimiento de conversión de imagen](format-conversion-tag-image.md)
>* [Preguntas frecuentes sobre las etiquetas de conversión y seguimiento de vista de página](faqs-conversion-page-view-tracking-tags.md)
>* [La etiqueta de asignación de conversión JavaScript de Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)

