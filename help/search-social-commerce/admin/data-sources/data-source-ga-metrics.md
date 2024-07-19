---
title: ' [!DNL Google Analytics] métricas disponibles'
description: Haga referencia a las  [!DNL Google Analytics] métricas disponibles para las fuentes de datos.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Apéndice: Métricas [!DNL Google Analytics] disponibles

Las siguientes métricas, excepto las exclusiones anotadas, están disponibles cuando están habilitadas en la implementación del cliente en [!DNL Google Analytics].

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
>* [Configurar una [!DNL Google Analytics] vista como fuente de datos](data-source-configure.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [Volver a autenticar un [!DNL Google Analytics] origen de datos](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configuración de origen de datos](data-source-settings.md)
