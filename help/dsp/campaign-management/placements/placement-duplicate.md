---
title: Ubicaciones duplicadas
description: Obtenga información sobre cómo duplicar una o más ubicaciones.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Ubicaciones duplicadas

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique una o más ubicaciones para crear ubicaciones con una configuración similar. Puede:

* Hacer varios duplicados de ubicaciones
* Duplicar ubicaciones dentro de los anunciantes y campañas originales o dentro de diferentes
* (Para ubicaciones duplicadas dentro de las campañas originales) Si lo desea, puede duplicar los anuncios originales
* Modificar el estado y las fechas de vuelo de las nuevas ubicaciones

Consulte &quot;[Qué no está duplicado](#placement-not-duplicated)&quot; para obtener una lista de configuraciones de ubicación que no estén duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Realice una de las acciones siguientes:

   * Para duplicar una ubicación, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** junto al nombre del paquete.

   * Para duplicar varias ubicaciones:

      1. Seleccione la casilla situada junto a cada posición que desee duplicar.

      1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Duplicate]**.

1. Especifique la nueva configuración de ubicación:

   1. (Ubicaciones únicas) Introduzca el nuevo nombre de ubicación.

   1. En el **[!UICONTROL Choose Package (Required)]** , seleccione el paquete principal o **[!UICONTROL No package]*.

   1. (Opcional) Cambie la configuración predeterminada.

   La configuración se aplica a todas las ubicaciones seleccionadas.

   De forma predeterminada, las nuevas ubicaciones son para el tipo de anuncio original, se asignan a los anunciantes y campañas originales, tienen horarios de vuelos que comienzan el día actual, se pausan y no incluyen los anuncios originales.

   Cuando se crean varias ubicaciones, a los nuevos nombres de ubicación se les anexa un número, en secuencia, utilizando la convención &lt;*#N original_placement_name*>, como &quot;Mi ubicación #2&quot;.

1. Haga clic **[!UICONTROL Submit]**.

## Qué no está duplicado {#placement-not-duplicated}

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
>* [Acerca de la administración de ubicación](placement-about.md)
>* [Crear una ubicación](placement-create.md)
>* [Editar una ubicación](placement-edit.md)
>* [Ver el registro de cambios de una ubicación](placement-change-log.md)
>* [Configuración de ubicación](placement-settings.md)

