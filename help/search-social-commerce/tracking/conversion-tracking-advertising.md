---
title: Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising
description: Obtenga información acerca del uso de etiquetas de seguimiento de conversión de Adobe Advertising.
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising

El seguimiento de conversiones mediante Adobe Advertising rastrea las conversiones resultantes de los clics en las publicidades utilizando las etiquetas de seguimiento de conversiones mediante Adobe Advertising que se insertan en las páginas web que se abren cuando se produce un evento de conversión, como una página de &quot;éxito&quot;. Las etiquetas incluyen información incrustada para enviar los datos de la transacción, junto con la cookie de Adobe Advertising del usuario, a un servidor de seguimiento, desde el cual la transacción se acredita al clic o impresión del anuncio correspondiente (según la configuración de atribución de conversión del anunciante).

>[!NOTE]
>
>Si el usuario no tiene una cookie válida, el Adobe Advertising no informa de la conversión.

Para cada conjunto de métricas de conversión que desee rastrear, debe crear una etiqueta de conversión independiente. Proporcione las etiquetas al anunciante o a la agencia con una lista de páginas web en las que insertar cada una. Puede generar cualquiera de los siguientes tipos de etiquetas de conversión. Consulte &quot;[Generar una etiqueta de conversión de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot; para obtener instrucciones.

* (Recomendado) Las etiquetas de JavaScript (versión 3 o 2), que no son visibles en las páginas web.

* Las etiquetas de imagen del HTML muestran imágenes transparentes de 1 píxel x 1 píxel (píxeles), que son invisibles para los usuarios finales, en las páginas web. Utilice etiquetas de imagen únicamente cuando la empresa tenga una política de no utilizar etiquetas de JavaScript.

Para obtener más información sobre las diferencias entre los tipos de etiquetas, consulte &quot;[preguntas frecuentes sobre las etiquetas de seguimiento de conversión de Advertising Cloud](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)&quot;.

>[!NOTE]
>
>* Esta función no agrega etiquetas de imagen ni de JavaScript a las páginas web del anunciante. Las etiquetas deben añadirse según el procedimiento normal del anunciante para actualizar páginas web.
>* Asegúrese de tener en cuenta cuánto tiempo se tarda en implementar las etiquetas. Según las políticas de la empresa, la implementación puede tardar semanas o incluso meses.

## Características de las etiquetas de seguimiento de conversión de Adobe Advertising

El píxel de seguimiento de conversión permite al Adobe Advertising hacer lo siguiente:

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
>* [Generar una etiqueta de conversión de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](format-conversion-tag-jsv2.md)
>* [Formato de etiquetas de seguimiento de conversión de imagen](format-conversion-tag-image.md)
>* [Preguntas más frecuentes acerca de las etiquetas de conversión y seguimiento de vista de página](faqs-conversion-page-view-tracking-tags.md)
>* [Etiqueta de asignación de conversión de JavaScript de Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
