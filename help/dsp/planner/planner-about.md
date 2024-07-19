---
title: DSP Acerca de la herramienta Planificador de
description: Obtenga información acerca de la herramienta de planificación para prever el alcance único de las ubicaciones de TV conectada (CTV) según el presupuesto especificado y los criterios de segmentación.
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# DSP Acerca de la herramienta Planificador de

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*característica de Beta*

La herramienta de planificación le ayuda a prever el alcance único a nivel doméstico de las ubicaciones de TV conectada (CTV) según el presupuesto especificado y los criterios de objetivo antes de comenzar a gastar en inventario. Después de evaluar varios planes de alcance, puede implementar el plan que mejor se ajuste a los resultados deseados en sus paquetes y ubicaciones.

La herramienta Planificador utiliza datos históricos de oferta, impresión y alcance de los últimos 90 días para estimar el alcance único, el CPM promedio, la frecuencia promedio y las impresiones de una configuración de plan.

## Previsión del planificador

Cada previsión consiste en una curva de previsión de alcance-presupuesto que muestra la cantidad de alcance alcanzable con la configuración del plan. Mueva el cursor sobre la visualización para ver las oportunidades de alcance incremental con presupuestos más altos.

![Previsión del planificador](/help/dsp/assets/planner-forecast.png "Previsión del planificador")

El resultado de la previsión también incluye una sección [!UICONTROL Inventory Breakdown] que muestra cómo los distintos editores contribuyen a un alcance único, lo que ofrece valiosas oportunidades de descubrimiento.

>[!NOTE]
>
>* La sección [!UICONTROL Inventory Breakdown] muestra datos solamente para el inventario privado y de [!UICONTROL On Demand].
>* El alcance único estimado que se muestra para dos editores puede superponerse.

## La vista del planificador

En la vista [!UICONTROL Planner], puede ver los planes de alcance de CTV existentes y crear otros nuevos.

También puede editar, duplicar, exportar, archivar o volver a generar la previsión de cualquier plan.

## Preguntas frecuentes

+++¿Qué tipos de inventario admite la herramienta de planificación?

La herramienta Planificador es compatible con todos los tipos de inventario, incluidos los inventarios programáticos garantizados (PG), mercado privado (PMP), [!UICONTROL On Demand] y público. Para generar previsiones precisas, incluya acuerdos con al menos 50.000 impresiones en los últimos siete días.

+++

+++¿Por qué veo &quot;[!UICONTROL Unable to generate forecast]?&quot;

Una de las razones más comunes de este error es un presupuesto insuficiente o una oferta máxima. Para obtener los mejores resultados, utilice un presupuesto mínimo de 5000 USD. Si se selecciona el tipo de medio [!UICONTROL Connected TV], se debe introducir una puja máxima de al menos 10 dólares estadounidenses.

Además, asegúrese de que los editores u ofertas incluidos estén activos y tengan actividad de impresión reciente.

+++

+++He creado una ubicación basada en el pronóstico, pero no he conseguido la cantidad de alcance único indicado por el pronóstico de alcance. ¿Por qué?

El pronóstico del alcance es solo una estimación, y se espera que los resultados reales varíen debido a múltiples factores que cambian con frecuencia, como la estacionalidad, la competitividad de las ofertas y la oferta y la demanda. No se espera que sea completamente precisa, pero es más útil para obtener perspectivas direccionales sobre las estrategias de campaña que pueden impulsar potencialmente los mejores resultados.

+++

+++¿Puede el planificador generar diferentes resultados de previsión con la misma configuración de entrada?

El planificador genera previsiones basadas en los últimos datos observados, por lo que el resultado previsto puede variar en diferentes momentos aunque la configuración del plan no cambie. Considere la posibilidad de generar varias previsiones para el mismo plan y exportar los resultados de cada una de ellas.

+++

+++¿Puedo guardar el resultado de previsión del planificador?

Sí, puede exportar una previsión a una hoja de cálculo de [!DNL Microsoft Excel] haciendo clic en **[!UICONTROL ...]** > **[!UICONTROL Export]** en la parte superior derecha. La hoja de cálculo captura la información mostrada en la curva de presupuesto de alcance usando dos columnas de datos: [!UICONTROL Budget] y [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* DSP [Acerca de la herramienta Planificador de](planner-about.md)
>* [Crear un plan de alcance de TV conectado](planner-create.md)
>* [Duplicar un plan de alcance de TV conectado](planner-duplicate.md)
>* [Editar un plan de alcance de TV conectado](planner-edit.md)
>* [Exportar un plan de alcance de TV conectado](planner-export.md)
>* [Volver a generar la previsión para un plan de alcance de TV conectado](planner-forecast.md)
>* [Archivar un plan de alcance de TV conectado](planner-archive.md)
>* [Configuración de los planes de alcance de TV conectados](planner-settings.md)
