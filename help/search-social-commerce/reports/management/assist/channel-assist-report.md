---
title: '[!UICONTROL Channel Assist Report]'
description: Más información acerca de [!UICONTROL Channel Assist Report].
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
source-git-commit: 45920c6ea9d2953c963ddf6472966b3fc3a91395
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# El [!UICONTROL Channel Assist Report]

*Anunciantes con seguimiento de clics de Search, Social y Commerce y con seguimiento de conversiones desde Adobe Advertising, Adobe Analytics (con una integración de [!DNL Analytics]) o proporcionados en fuentes usando solo un token (`ef_id`)*

[!UICONTROL Channel Assist Report] indica cómo varios canales de marketing (búsqueda o social desde Search, Social y Commerce; o visualización o vídeo desde Advertising DSP) han ayudado en el proceso de conversión. El informe muestra cómo cada patrón de tipos de eventos que provocó una o más conversiones ha contribuido a las conversiones generales. Por ejemplo, puede ver cuántas conversiones se produjeron cuando los usuarios vieron una impresión de anuncio en pantalla por primera vez, luego hicieron clic en un anuncio de búsqueda y luego hicieron un pedido, o puede ver cuántas conversiones se produjeron después de que los usuarios interactuaran con más de 10 anuncios. Los tipos de evento incluyen clics de búsqueda, impresiones de visualización y clics, impresiones y clics de vídeo, y otras impresiones y otros clics. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

Los resultados del informe incluyen datos agregados para cada patrón de tipos de evento en la ruta de conversión (hasta los N tipos de evento más antiguos) que se produjeron en la [ventana retrospectiva de clics del anunciante](/help/search-social-commerce/glossary.md#c-d) y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j). Por ejemplo, si selecciona un tamaño de ruta de cinco (5), el informe incluye rutas de conversión que incluyen hasta los cinco eventos más antiguos, con una fila para cada patrón de tipos de eventos rastreados (como &quot;clic en búsqueda&quot; y luego &quot;impresión de visualización&quot;). Cada fila muestra un patrón de eventos, incluido el primer evento de la ruta y el último evento que resultó en conversiones (incluso si el último evento está fuera del tamaño de ruta especificado). De forma predeterminada, las filas están en orden ascendente según el número de eventos de la ruta.

Si lo desea, puede incluir datos de conversión agregados para cada fila. Cuando se incluyen columnas de conversiones/ingresos en el informe, cada tipo de conversión se representa en cuatro columnas, que muestran a) el número total de conversiones, b) el porcentaje de todas las conversiones que se atribuyeron a ese patrón de evento, c) la latencia promedio en días desde el primer evento a una conversión y d) la latencia promedio en días desde el último evento a una conversión. Cuando la ruta de conversión incluye más eventos que el tamaño de ruta especificado, el informe incluye filas adicionales que agregan datos para las conversiones resultantes del mayor número de eventos (como todos los patrones que incluyeron seis tipos de eventos).

Puede ver los datos de los 18 meses anteriores.

## Columnas disponibles

Las siguientes son las columnas disponibles para cada informe. Las columnas predeterminadas se incluyen automáticamente de forma predeterminada. Puede agregar las columnas personalizadas disponibles desde la sección Columnas de la configuración del informe.

| Columna | ¿Predeterminado? | Descripción |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] a [!UICONTROL 5th Event] | Predeterminado | Los cinco tipos de eventos más antiguos en la ruta de conversión que se produjeron en la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Predeterminado | El número de tipos de eventos en la ruta de conversión que se produjeron en la [ventana retrospectiva de clics](/help/search-social-commerce/glossary.md#c-d) del anunciante y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | Predeterminado | El tipo de evento del primer (primer) evento de la ruta de conversión. |
| [!UICONTROL Last Event Type] | Predeterminado | El tipo de evento del último evento que resultó en conversiones (incluso si el último evento está fuera del tamaño de ruta especificado). |
| \[Métricas personalizadas (derivadas) específicas del anunciante\] | Personalizado | El valor de una métrica personalizada que ha creado y que se calcula a partir de las métricas existentes. |
| \[Métricas de conversión específicas del anunciante\] | Personalizado | Número de conversiones de una métrica de conversión o una métrica de participación del sitio especificadas. |
| [!UICONTROL % of Total] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe para cada métrica de conversión incluida) El porcentaje de conversiones generales entre portafolios atribuidas al patrón de eventos. |
| [!UICONTROL 6th Event] a [!UICONTROL 30th Event] | Personalizado | Los tipos de evento del sexto al trigésimo en la ruta de conversión que se produjo en la [ventana retrospectiva de clics del anunciante](/help/search-social-commerce/glossary.md#c-d) y en la [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe para cada métrica de conversión incluida) La latencia promedio en días desde el primer evento a una conversión. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[métrica de conversión\] | Automático | (No disponible en la configuración del informe, pero se incluye automáticamente en el resultado del informe) La latencia promedio en días desde el último evento a una conversión. |
| [!UICONTROL Path Frequency] | Personalizado | El número de veces que la ruta de esta fila se produjo antes de la conversión. |

>[!MORELIKETHIS]
>
>* [Acerca de los informes de asistencia](assist-report-about.md)
>* [El [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [El [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Configuración de informe de asistencia](assist-report-settings.md)
>* [Generar un informe de asistencia](assist-report-generate.md)
