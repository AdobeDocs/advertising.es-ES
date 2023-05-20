---
title: Duplicación de una campaña
description: Obtenga información sobre cómo duplicar una campaña.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Duplicación de una campaña

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique una campaña para crear una nueva campaña con una configuración similar. Puede:

* Duplique la campaña para el anunciante original o para uno diferente
* Opcionalmente, duplicar los paquetes y las ubicaciones originales
* Modificación de las fechas de vuelo de la nueva campaña

Consulte &quot;[Qué no está duplicado](#campaign-not-duplicated)&quot; para obtener una lista de configuraciones de ubicación que no estén duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Junto al nombre de la campaña, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Especifique la nueva configuración de la campaña:

   1. Introduzca el nuevo nombre de la campaña y la fecha de finalización del vuelo.

   1. (Opcional) Cambie la configuración predeterminada.

      De forma predeterminada, la nueva campaña se asigna al anunciante original, tiene un programa de vuelos que comienza el día actual e incluye los paquetes y las ubicaciones originales.

1. Haga clic **[!UICONTROL Submit]**.

## Qué no está duplicado {#campaign-not-duplicated}

Todos los ajustes de las ubicaciones originales se duplican, excepto:

* Configuración del experimento
* (Si cambia las fechas de vuelo) Programación de anuncios personalizados
* (Si no adjunta anuncios) Ponderación y programación de anuncios personalizados
* Ubicaciones predeterminadas para ofertas y ubicaciones programáticas garantizadas (PG) para [!UICONTROL Simple Ad Serving] ofertas
* (Si copia ubicaciones en una campaña diferente):
   * Destinos geográficos
   * Píxeles de evento
   * Anuncios
   * Placement-level [!DNL DoubleVerify Authentic Brand Safety] segmentos (que anulan los segmentos de nivel de anunciante)

>[!MORELIKETHIS]
>
>* [Acerca de Campaign Management](campaign-about.md)
>* [Creación de una campaña](campaign-create.md)
>* [Edición de una campaña](campaign-edit.md)
>* [Visualización del registro de cambios de una campaña](campaign-change-log.md)
>* [Configuración de campaña](campaign-settings.md)

