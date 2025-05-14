---
title: Duplicación de una campaña
description: Obtenga información sobre cómo duplicar una campaña.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Duplicación de una campaña

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique una campaña para crear una nueva campaña con una configuración similar. Puede:

* Duplique la campaña para el anunciante original o para uno diferente

* Opcionalmente, duplicar los paquetes y las ubicaciones originales

* Modificación de las fechas de vuelo de la nueva campaña

Consulte &quot;[Lo que no está duplicado](#campaign-not-duplicated)&quot; para obtener una lista de configuraciones de ubicación que no están duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Junto al nombre de la campaña, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Especifique la nueva configuración de la campaña:

   1. Introduzca el nuevo nombre de la campaña y la fecha de finalización del vuelo.

   1. (Opcional) Cambie la configuración predeterminada.

      De forma predeterminada, la nueva campaña se asigna al anunciante original, tiene un programa de vuelos que comienza el día actual e incluye los paquetes y las ubicaciones originales.

1. Haga clic en **[!UICONTROL Submit]**.

## Qué no está duplicado {#campaign-not-duplicated}

Todos los ajustes de las ubicaciones originales se duplican, excepto:

* Configuración del experimento
* (Si cambia las fechas de vuelo) Programación de anuncios personalizados
* (Si no adjunta anuncios) Ponderación y programación de anuncios personalizados
* Ubicaciones predeterminadas para ofertas programáticas garantizadas (PG) y ubicaciones para [!UICONTROL Simple Ad Serving] ofertas
* (Si copia ubicaciones en una campaña diferente):
   * Destinos geográficos
   * Píxeles de evento
   * Anuncios
   * Segmentos de nivel de ubicación [!DNL DoubleVerify Authentic Brand Safety] (que anulan los segmentos de nivel de anunciante)

## Prácticas recomendadas para configurar la nueva campaña

>[!TIP]
>
>* Use hojas de edición masiva para [realizar cambios en varios componentes de campaña a la vez](/help/dsp/campaign-management/campaign-components-review-edit.md).
* Use las hojas de etiquetas de anuncios para [cargar varios anuncios de terceros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pause la nueva campaña hasta que esté listo para activarla.

* Tenga en cuenta lo siguiente y edite la nueva configuración de campaña según sea necesario:

   * ¿La cuenta tiene fondos suficientes para dar cabida al nuevo presupuesto de la campaña?

   * ¿La nueva campaña necesita un presupuesto diferente al de la campaña anterior?

   * Cargue elementos creativos, incluida cualquier ponderación y programación personalizadas necesarias, y adjúntelos a las ubicaciones.

   * Adjunte los píxeles de evento según sea necesario a las ubicaciones y los anuncios.

   * Incluya destinos geográficos y segmentos de nivel de ubicación [!DNL DoubleVerify Authentic Brand Safety] según sea necesario para las ubicaciones.

   * Para obtener ofertas garantizadas mediante programación, utilice nuevos ID de acuerdo y cree ubicaciones predeterminadas.

   * Cree nuevas ubicaciones para [!UICONTROL Simple Ad Serving] ofertas según sea necesario.

* Para las campañas de rendimiento (es decir, campañas con paquetes que utilizan objetivos de optimización personalizados), use la configuración [[!UICONTROL Linked Package for Optimization Learnings Carryover] ](/help/dsp/campaign-management/packages/package-settings.md) para cada paquete a fin de usar los datos históricos de la campaña anterior como entrada para optimizar el paquete.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de campañas](campaign-about.md)
>* [Crear una campaña](campaign-create.md)
>* [Editar una campaña](campaign-edit.md)
>* [Ver el registro de cambios de una campaña](campaign-change-log.md)
>* [Configuración de campaña](campaign-settings.md)
