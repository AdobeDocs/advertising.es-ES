---
title: Disponible [!DNL Google Analytics] métricas
description: Haga referencia a [!DNL Google Analytics] métricas disponibles para fuentes de datos.
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Apéndice: disponible [!DNL Google Analytics] métricas

Las siguientes métricas, excepto las exclusiones mencionadas, están disponibles cuando están habilitadas en la implementación del cliente en [!DNL Google Analytics].

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Categoría | Excluido | Comentarios |
| ---- | ---- | ---- |
| \[Todo\] | Métricas con un tipo de datos de &quot;PORCENTAJE&quot; | Las métricas presentadas como porcentaje siempre se excluyen. |
| Usuario | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionPerUser | — |
| Session | ga:uniqueDimensionCombinations | — |
| Conversiones de metas | — | — |
| Seguimiento de página | ga:entradas, ga:timeOnPage, ga:salidas | — |
| Búsqueda interna | — | Los nombres descriptivos de todas las métricas de la búsqueda interna van precedidos del valor &quot;InternalSearch:&quot; |
| Seguimiento de eventos | — | — |
| Comercio electrónico | — | — |
| Interacciones sociales | — | — |
| Excepciones | — | — |
| Variables o columnas personalizadas | ga:calcMetric_* | Las métricas calculadas siempre se excluyen. |

>[!MORELIKETHIS]
>
>* [Acerca de la sincronización [!DNL Google Analytics] métricas de conversión](data-source-about.md)
>* [Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos](data-source-prerequisites.md)
>* [Configurar un [!DNL Google Analytics] ver como fuente de datos](data-source-configure.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [Volver a autenticar un [!DNL Google Analytics] fuente de datos](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configuración de fuente de datos](data-source-settings.md)
