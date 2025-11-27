---
title: '[!UICONTROL Campaign Assist Report]'
description: Más información acerca de [!UICONTROL Campaign Assist Report].
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---

# El [!UICONTROL Campaign Assist Report]

*Anunciantes con seguimiento de clics de Search, Social y Commerce y con seguimiento de conversiones de Adobe Advertising, Adobe Analytics (con una integración de [!DNL Analytics]) o proporcionados en fuentes usando solo un token (`ef_id`)*

[!UICONTROL Campaign Assist Report] indica qué campañas han ayudado en el proceso de conversión. Los informes muestran cómo cada patrón de campañas cuyos anuncios produjeron una o más conversiones ha contribuido a las conversiones generales. Por ejemplo, puede ver cuántas conversiones se produjeron cuando los usuarios vieron un anuncio por primera vez desde la Campaña A, luego hicieron clic en un anuncio de la Campaña B y, por último, realizaron un pedido. Del mismo modo, puede ver cuántas conversiones se produjeron después de que los usuarios interactuaran con los anuncios de más de 10 campañas.

Los resultados del informe incluyen datos agregados para cada patrón de campañas en la ruta de conversión (hasta las N campañas más antiguas) para eventos que se produjeron dentro de la [ventana retrospectiva de clics del anunciante](/help/search-social-commerce/glossary.md#c-d) y la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j). Por ejemplo, si selecciona un tamaño de ruta de cinco (5), el informe incluye rutas de conversión que incluyen hasta las cinco campañas más antiguas, con una fila para cada patrón de campañas cuyos eventos se rastrearon. Cada fila muestra un patrón de campañas, incluida la primera campaña de la ruta y la última campaña que resultó en conversiones (incluso si la última campaña está fuera del tamaño de ruta especificado). De forma predeterminada, las filas están en orden ascendente según el número de campañas de la ruta.

Si lo desea, puede incluir datos de conversión acumulados, incluidas las métricas personalizadas, de cada fila. Cuando se incluyen columnas de conversiones/ingresos en el informe, cada tipo de conversión se representa en cuatro columnas, que muestran: a) el número total de conversiones, b) el porcentaje de todas las conversiones que se atribuyeron a ese patrón de campaña, c) la latencia promedio en días desde el primer evento (en la primera campaña) a una conversión, y d) la latencia promedio en días desde el último evento (en la última campaña) a una conversión. Cuando la ruta de conversión incluye más campañas que el tamaño de ruta especificado, el informe incluye filas adicionales que agregan datos para las conversiones resultantes del mayor número de campañas (como todos los patrones que incluyeron seis campañas).

Opcionalmente, también puede incluir la red de anuncios o el tipo de evento después del nombre de la campaña, como `<campaign name> (Google) click`.

Puede ver los datos de los 18 meses anteriores.

>[!TIP]
>
>Si las palabras clave de marca están en una campaña diferente a las palabras clave genéricas, el informe indica si las palabras clave de marca contribuyen a las conversiones.

## Columnas disponibles

Las siguientes son las columnas disponibles para cada informe. Las columnas predeterminadas se incluyen automáticamente de forma predeterminada. Puede agregar las columnas personalizadas disponibles desde la sección Columnas de la configuración del informe.

| Columna | ¿Predeterminado? | Descripción |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] a [!UICONTROL 5th Campaign] | Predeterminado | Las cinco campañas más antiguas de la ruta de conversión que se produjeron en la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j).<br><br>Si ha incluido cualquiera de las opciones de informe para indicar la red de anuncios, el nombre de cuenta o el tipo de evento después del nombre de entidad, esa información se incluirá después del nombre de campaña (como `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| [!UICONTROL Path Size] | Predeterminado | Número de campañas en la ruta de conversión que se produjeron en la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Predeterminado | La primera campaña de la ruta de conversión. |
| [!UICONTROL Last Campaign] | Predeterminado | La última campaña que resultó en conversiones (incluso si la última palabra clave está fuera del tamaño de ruta especificado).<br><br>Si ha incluido cualquiera de las opciones de informe para indicar la red de anuncios, el nombre de cuenta o el tipo de evento después del nombre de entidad, esa información se incluirá después del nombre de campaña (como `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| \[Métricas personalizadas (derivadas) específicas del anunciante\] | Personalizado | El valor de una métrica personalizada que ha creado que se calcula a partir de las métricas existentes. |
| \[Métricas de conversión específicas del anunciante\] | Personalizado | Número de conversiones de una métrica de conversión o una métrica de participación del sitio especificadas. |
| [!UICONTROL % of Total] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe para cada métrica de conversión incluida) El número de conversiones para una métrica de conversión especificada que resultó del patrón de campaña. |
| [!UICONTROL 6th Campaign] a [!UICONTROL 20th Campaign] | Personalizado | De la sexta a la vigésima campaña en la ruta de conversión que se produjo en la [ventana retrospectiva de clics del anunciante](/help/search-social-commerce/glossary.md#c-d) y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j).<br><br>Si ha incluido cualquiera de las opciones de informe para indicar la red de anuncios, el nombre de cuenta o el tipo de evento después del nombre de entidad, esa información se incluirá después del nombre de campaña (como `"<"campaign name> [Baidu] [Account1] [click]`&quot;). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe para cada métrica de conversión incluida) La latencia promedio en días desde el primer evento (en la primera campaña) a una conversión. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe) La latencia promedio en días desde el último evento (en la última campaña) hasta una conversión. |
| [!UICONTROL EF Campaign ID] | Personalizado | El ID numérico que Search, Social y Commerce asignan a la campaña. |
| [!UICONTROL EF Portfolio Group ID] | Personalizado | El ID numérico del grupo de portafolios al que pertenece el portafolio. |
| [!UICONTROL EF Search Engine ID] | Personalizado | El identificador numérico que Search, Social y Commerce asigna a la red de anuncios: <i>[!UICONTROL 3]</i> para [!DNL Google Ads], <i>[!UICONTROL 10]</i> para [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> para [!DNL Meta], <i>[!UICONTROL 86]</i> para [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> para [!DNL Naver], <i>[!UICONTROL 88]</i> para [!DNL Baidu], <i>[!UICONTROL 90]</i> para [!DNL Yandex], <i>[!UICONTROL 94]</i> para [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> para [!DNL Yahoo Native] (obsoleto) o <i>[!UICONTROL 106]</i> para [!DNL Pinterest] (obsoleto). |
| [!UICONTROL Portfolio ID] | El ID numérico del portafolio. |  |
| [!UICONTROL User SE Account ID] | El ID numérico que Search, Social y Commerce asignan a la red de anuncios. |  |

>[!MORELIKETHIS]
>
>* [Acerca de los informes de asistencia](assist-report-about.md)
>* [El [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [El [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Configuración de informe de asistencia](assist-report-settings.md)
>* [Generar un informe de asistencia](assist-report-generate.md)
