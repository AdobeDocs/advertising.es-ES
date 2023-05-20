---
title: Duplicación de un paquete
description: Obtenga información sobre cómo duplicar un paquete.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Duplicación de un paquete

Duplique un paquete para crear un paquete con una configuración similar. Puede:

* Duplique el paquete dentro del anunciante y la campaña originales o dentro de diferentes
* Opcionalmente, duplicar las ubicaciones dentro del paquete
* (Para paquetes duplicados dentro de las campañas originales) Opcionalmente, duplicar los anuncios originales y los píxeles de evento de nivel de ubicación
* Modificar las fechas de vuelo del nuevo paquete

Consulte &quot;[Qué no está duplicado](#package-not-duplicated)&quot; para obtener una lista de configuraciones de ubicación que no estén duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña para abrir [!UICONTROL Packages] vista.

1. Junto al nombre del paquete, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Especifique la nueva configuración del paquete:

   1. Introduzca el nuevo nombre del paquete.

   1. (Opcional) Cambie la configuración predeterminada.

      De forma predeterminada:

      * El nuevo paquete se asigna al anunciante y a la campaña originales.

      * El nuevo paquete se activa el día actual.<!-- and the flight continues for NN  days. -->

      * Las ubicaciones dentro del paquete original se copian en el nuevo paquete.

      * Los píxeles de evento de nivel de ubicación y de anuncios no se copian en el nuevo paquete.

1. Haga clic **[!UICONTROL Submit]**.

## Qué no está duplicado {#package-not-duplicated}

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
>* [Acerca de la administración de paquetes](package-about.md)
>* [Crear un paquete](package-create.md)
>* [Edición de un paquete](package-edit.md)
>* [Visualización del registro de cambios de un paquete](package-change-log.md)
>* [Configuración de paquetes](package-settings.md)

