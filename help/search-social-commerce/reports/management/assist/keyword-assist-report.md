---
title: '[!UICONTROL Keyword Assist Report]'
description: Más información acerca de [!UICONTROL Keyword Assist Report].
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# El [!UICONTROL Keyword Assist Report]

*Anunciantes con seguimiento de clics de Search, Social y Commerce y con seguimiento de conversiones desde Adobe Advertising, Adobe Analytics (con una integración de [!DNL Analytics]) o proporcionados en fuentes usando solo un token (`ef_id`)*

[!UICONTROL Keyword Assist Report] indica qué palabras clave o ubicaciones generan clics. El informe muestra cada patrón de palabras clave de búsqueda pagada o ubicaciones que recibieron clics en una ruta de conversión e indica cómo ese patrón contribuyó a las conversiones generales. Por ejemplo, puede ver cuántas conversiones se produjeron cuando los usuarios hicieron clic en un anuncio por primera vez como resultado de una búsqueda de palabra clave de &quot;zapatos de cuero&quot;, luego hicieron clic en un anuncio después de una búsqueda de palabra clave de &quot;zapatos de ante&quot; y luego hicieron un pedido, o puede ver cuántas conversiones se produjeron después de que los usuarios hicieron clic en anuncios que resultaron de más de 10 palabras clave.

Los resultados del informe incluyen datos agregados de hasta N clics de ubicación o palabra clave de búsqueda pagados más antiguos en la ruta de conversión que se produjeron dentro de la del anunciante
haga clic en ventanas retroactivas e retroactivas de impresiones. Por ejemplo, si selecciona un tamaño de ruta de cinco (5), el informe consta de rutas de conversión que incluyen hasta las cinco palabras clave o ubicaciones más antiguas que recibieron clics, con una fila por cada patrón de clics rastreado. Cada fila incluye la primera palabra clave o ubicación en la ruta y la última palabra clave o ubicación que resultó en conversiones (incluso si la última palabra clave está fuera del tamaño de ruta especificado). De forma predeterminada, las filas están en orden ascendente según el número de eventos de la ruta.

>[!NOTE]
>
>Si el informe incluye ubicaciones de campañas de búsqueda con contenido habilitado (que no incluyen palabras clave), la columna [!UICONTROL Keyword] mostrará los nombres de grupos de anuncios aplicables, como &quot;(contenido de grupo de anuncios) su nombre de grupo de anuncios&quot;.

Si lo desea, puede incluir datos de conversión agregados para cada fila. Cuando se incluyen columnas de conversiones/ingresos en el informe, cada tipo de conversión se representa en cuatro columnas, que muestran: a) el número total de conversiones, b) el porcentaje de todas las conversiones que se atribuyeron a ese patrón de palabra clave, c) la latencia promedio en días desde el primer evento (en la primera palabra clave) hasta una conversión, y d) la latencia promedio en días desde el último evento (en la última palabra clave) hasta una conversión. Cuando la ruta de conversión incluye más palabras clave que el tamaño de ruta especificado, el informe incluye filas adicionales que agregan datos para las conversiones resultantes del mayor número de palabras clave (como todos los patrones que incluyeron clics en seis palabras clave).

Puede ver los datos de los 18 meses anteriores.

## Columnas disponibles

Las siguientes son las columnas disponibles para cada informe. Las columnas predeterminadas se incluyen automáticamente de forma predeterminada. Puede agregar las columnas personalizadas disponibles desde la sección Columnas de la configuración del informe.

| Columna | ¿Predeterminado? | Descripción |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] a [!UICONTROL 5th Keyword] | Predeterminado | Los cinco clics de ubicación o palabra clave de búsqueda pagada más antiguos en la ruta de conversión que se produjeron en la ventana retrospectiva de [clics del anunciante](/help/search-social-commerce/glossary.md#c-d) y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Nota:</b> Si el informe incluye ubicaciones de campañas de búsqueda con contenido habilitado (que no incluyen palabras clave), entonces estas columnas mostrarán los nombres de grupos de anuncios aplicables, como &quot;(contenido de grupo de anuncios) su nombre de grupo de anuncios&quot;. |
| [!UICONTROL Path Size] | Predeterminado | Número de palabras clave o ubicaciones en la ruta de conversión que se produjeron en la [ventana retrospectiva de clics del anunciante](/help/search-social-commerce/glossary.md#c-d) y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Predeterminado | La primera palabra clave o ubicación en la ruta de conversión. |
| [!UICONTROL Last Keyword] | Predeterminado | La última palabra clave o ubicación que resultó en conversiones (incluso si la última palabra clave está fuera del tamaño de ruta especificado). |
| \[Métricas personalizadas (derivadas) específicas del anunciante\] | Personalizado | El valor de una métrica personalizada que ha creado y que se calcula a partir de las métricas existentes. |
| \[Métricas de conversión específicas del anunciante\] | Personalizado | Número de conversiones de una métrica de conversión o una métrica de participación del sitio especificadas. |
| [!UICONTROL % of Total] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe para cada métrica de conversión incluida) El porcentaje de conversiones generales entre portafolios atribuido a la palabra clave o al patrón de ubicación. |
| [!UICONTROL 6th Keyword] a [!UICONTROL 10th Keyword] | Personalizado | La ubicación o palabra clave de búsqueda pagada sexta a décima hace clic en la ruta de conversión que se produjo dentro de la [ventana retrospectiva de clics del anunciante](/help/search-social-commerce/glossary.md#c-d) y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Nota:</b> Si el informe incluye ubicaciones de campañas de búsqueda con contenido habilitado (que no incluyen palabras clave), entonces estas columnas mostrarán los nombres de grupos de anuncios aplicables, como &quot;(contenido de grupo de anuncios) su nombre de grupo de anuncios&quot;. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe para cada métrica de conversión incluida) La latencia promedio en días desde el primer evento (en la primera palabra clave o ubicación) a una conversión. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe) La latencia promedio en días desde el último evento (en la última palabra clave o ubicación) hasta una conversión. |
| [!UICONTROL Path Frequency] | Personalizado | El número de veces que la ruta de esta fila se produjo antes de la conversión. |

>[!MORELIKETHIS]
>
>* [Acerca de los informes de asistencia](assist-report-about.md)
>* [El [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [El [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Configuración de informe de asistencia](assist-report-settings.md)
>* [Generar un informe de asistencia](assist-report-generate.md)
