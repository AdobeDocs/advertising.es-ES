---
title: Duplicación de un paquete
description: Obtenga información sobre cómo duplicar un paquete.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Duplicación de un paquete

Duplique un paquete para crear un paquete con una configuración similar. Puede:

* Duplique el paquete dentro del anunciante y la campaña originales o dentro de diferentes

* Opcionalmente, duplicar las ubicaciones dentro del paquete

* (Para paquetes duplicados dentro de las campañas originales) Opcionalmente, duplicar los anuncios originales y los píxeles de evento de nivel de ubicación

* Modificar las fechas de vuelo del nuevo paquete

Consulte &quot;[Lo que no está duplicado](#package-not-duplicated)&quot; para obtener una lista de configuraciones de ubicación que no están duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña para abrir la vista [!UICONTROL Packages].

1. Junto al nombre del paquete, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Especifique la nueva configuración del paquete:

   1. Introduzca el nuevo nombre del paquete.

   1. (Opcional) Cambie la configuración predeterminada.

      De forma predeterminada:

      * El nuevo paquete se asigna al anunciante y a la campaña originales.

      * El nuevo paquete se activa el día actual.<!-- and the flight continues for NN  days. -->

      * Las ubicaciones dentro del paquete original se copian en el nuevo paquete.

      * Los píxeles de evento de nivel de ubicación y de anuncios no se copian en el nuevo paquete.

1. Haga clic en **[!UICONTROL Submit]**.

## Qué no está duplicado {#package-not-duplicated}

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

## Prácticas recomendadas para configurar el nuevo paquete

>[!TIP]
>
>* Use hojas de edición masiva para [realizar cambios en varios componentes de campaña a la vez](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Use las hojas de etiquetas de anuncios para [cargar varios anuncios de terceros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pause el nuevo paquete hasta que esté listo para activarlo.

* Tenga en cuenta lo siguiente y edite el nuevo paquete según sea necesario:

   * ¿Cuenta la cuenta con fondos suficientes para dar cabida al nuevo presupuesto del paquete?

   * ¿Necesita el nuevo paquete un presupuesto diferente al paquete anterior?

   * ¿Se necesitan presupuestos mínimos para alguna de las ubicaciones?

   * Cargue elementos creativos, incluida cualquier ponderación y programación personalizadas necesarias, y adjúntelos a las ubicaciones.

   * Adjunte los píxeles de evento según sea necesario a las ubicaciones y los anuncios.

   * Incluya destinos geográficos y segmentos de nivel de ubicación [!DNL DoubleVerify Authentic Brand Safety] según sea necesario para las ubicaciones.

   * Para obtener ofertas garantizadas mediante programación, utilice nuevos ID de acuerdo y cree ubicaciones predeterminadas.

   * Cree nuevas ubicaciones para [!UICONTROL Simple Ad Serving] ofertas según sea necesario.

* Para los paquetes que utilizan objetivos de optimización personalizados, use la configuración [[!UICONTROL Linked Package for Optimization Learnings Carryover] &#x200B;](/help/dsp/campaign-management/packages/package-settings.md) para cada paquete a fin de usar los datos históricos de la campaña anterior como entrada para optimizar el paquete.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de paquetes](package-about.md)
>* [Crear un paquete](package-create.md)
>* [Editar un paquete](package-edit.md)
>* [Ver el registro de cambios de un paquete](package-change-log.md)
>* [Configuración del paquete](package-settings.md)
