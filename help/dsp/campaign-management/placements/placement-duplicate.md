---
title: Ubicaciones duplicadas
description: Obtenga información sobre cómo duplicar una o más ubicaciones.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Ubicaciones duplicadas

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique una o más ubicaciones para crear ubicaciones con una configuración similar. Puede:

* Hacer varios duplicados de ubicaciones
* Duplicar ubicaciones dentro de los anunciantes y campañas originales o dentro de diferentes
* (Para ubicaciones duplicadas dentro de las campañas originales) Si lo desea, puede duplicar los anuncios originales
* Modificar el estado y las fechas de vuelo de las nuevas ubicaciones

Consulte &quot;[Lo que no está duplicado](#placement-not-duplicated)&quot; para obtener una lista de configuraciones de ubicación que no están duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Realice una de las acciones siguientes:

   * Para duplicar una ubicación, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** junto al nombre del paquete.

   * Para duplicar varias ubicaciones:

      1. Seleccione la casilla situada junto a cada posición que desee duplicar.

      1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Duplicate]**.

1. Especifique la nueva configuración de ubicación:

   1. (Ubicaciones únicas) Introduzca el nuevo nombre de ubicación.

   1. En el menú **[!UICONTROL Choose Package (Required)]**, seleccione el paquete principal o **[!UICONTROL No package]*.

   1. (Opcional) Cambie la configuración predeterminada.

   La configuración se aplica a todas las ubicaciones seleccionadas.

   De forma predeterminada, las nuevas ubicaciones son para el tipo de anuncio original, se asignan a los anunciantes y campañas originales, tienen horarios de vuelos que comienzan el día actual, se pausan y no incluyen los anuncios originales.

   Cuando crea varias ubicaciones, los nuevos nombres de ubicación se anexan con un número, en secuencia, utilizando la convención &lt;*original_placement_name #N*>, como &quot;Mis #2 de ubicación&quot;.

1. Haga clic en **[!UICONTROL Submit]**.

## Qué no está duplicado {#placement-not-duplicated}

Todos los ajustes de las ubicaciones originales se duplican, excepto:

* Configuración del experimento
* Presupuestos mínimos de nivel de ubicación
* (Si cambia las fechas de vuelo) Programación de anuncios personalizados
* (Si no adjunta anuncios) Ponderación y programación de anuncios personalizados
* Ubicaciones predeterminadas para ofertas programáticas garantizadas (PG) y ubicaciones para [!UICONTROL Simple Ad Serving] ofertas
* (Si copia ubicaciones en una campaña diferente):
   * Destinos geográficos
   * Píxeles de evento
   * Anuncios
   * Segmentos de nivel de ubicación [!DNL DoubleVerify Authentic Brand Safety] (que anulan los segmentos de nivel de anunciante)

## Prácticas recomendadas para configurar las nuevas ubicaciones

>[!TIP]
>
>* Use hojas de edición masiva para [realizar cambios en varios componentes de campaña a la vez](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Use las hojas de etiquetas de anuncios para [cargar varios anuncios de terceros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pause las nuevas ubicaciones hasta que esté listo para activarlas.

* Tenga en cuenta lo siguiente y edite las nuevas ubicaciones según sea necesario:

   * ¿La cuenta tiene fondos suficientes para dar cabida a los nuevos presupuestos de colocación?

   * ¿Las nuevas ubicaciones necesitan presupuestos diferentes a los de las ubicaciones anteriores? ¿Son necesarios los presupuestos mínimos?

   * Cargue elementos creativos, incluida cualquier ponderación y programación personalizadas necesarias, y adjúntelos a las ubicaciones.

   * Adjunte los píxeles de evento según sea necesario a las ubicaciones y los anuncios.

   * Incluya destinos geográficos y segmentos de nivel de ubicación [!DNL DoubleVerify Authentic Brand Safety] según sea necesario para las ubicaciones.

   * Para obtener ofertas garantizadas mediante programación, utilice nuevos ID de acuerdo y cree ubicaciones predeterminadas.

   * Cree nuevas ubicaciones para [!UICONTROL Simple Ad Serving] ofertas según sea necesario.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de ubicaciones](placement-about.md)
>* [Crear una ubicación](placement-create.md)
>* [Editar ubicaciones](placement-edit.md)
>* [Ver el registro de cambios de una ubicación](placement-change-log.md)
>* [Configuración de ubicación](placement-settings.md)
