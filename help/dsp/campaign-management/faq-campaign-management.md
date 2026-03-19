---
title: Preguntas frecuentes sobre la administración de campañas
description: Obtenga más información acerca de la administración de campañas, incluido el período de latencia de los cambios y lo que sucede cuando se realizan cambios de presupuesto durante un vuelo.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: dad30b0bd24c0286c1de6520471cb90707046ff3
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Preguntas frecuentes sobre la administración de campañas

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latencia de los cambios de configuración

* Al cambiar una configuración de ubicación o paquete, ¿cuándo se aplica el cambio?

  Los cambios de configuración suelen surtir efecto inmediatamente, pero pueden tardar hasta 12 horas.

  Si es el último día de envío, realice cambios al principio del día para que DSP tenga tiempo de sobra para volver a calibrar el paquete en función de los cambios. Por ejemplo, si cambia del ritmo uniforme al ritmo de carga frontal, DSP debe volver a evaluar cómo distribuir el gasto durante el resto del vuelo. No realice ese tipo de cambio si solo le queda una hora para entregar en el último día del vuelo.

## Actualizaciones presupuestarias a mitad del vuelo

* Cuando realiza un cambio en una ubicación, ¿cuánto tiempo tarda DSP en reasignar el presupuesto del paquete?

  La asignación del presupuesto se basa en el rendimiento de la ubicación, que se evalúa con un promedio de 14 días. Los cambios en una ubicación producen cambios en la asignación del presupuesto solo cuando provocan cambios en el rendimiento durante la media de 14 días.

  Cuando se producen cambios de rendimiento, DSP reasigna el presupuesto del paquete entre las ubicaciones en consecuencia durante el siguiente ciclo de optimización del presupuesto, que se produce aproximadamente a medianoche (00:00) en el huso horario de la campaña.

* ¿Cómo se reasigna el presupuesto cuando se elimina una ubicación de un paquete y se agrega a otro paquete?

  Todo el historial de gasto de una ubicación se adjunta a la ubicación y se mueve con ella de paquete en paquete.

  Al eliminar una ubicación de un paquete, el paquete ya no tiene historial de gasto de la ubicación. El presupuesto del paquete se convierte en (presupuesto del paquete: presupuesto de ubicación eliminado) / intervalo de tiempo que permanece en vuelo. A continuación, el presupuesto del paquete se asigna a las ubicaciones que quedan en el paquete.

  Del mismo modo, si agrega la misma ubicación a un paquete diferente, DSP tiene en cuenta el historial de gastos de la ubicación al asignar el presupuesto para todas las ubicaciones del nuevo paquete.

* ¿Cómo cambia el ritmo del paquete en el último día de un vuelo?

  El último día de un vuelo, el día se acorta de 24 horas a 23 horas para que no se exceda el presupuesto del paquete. Además, la estrategia de relleno de ritmo del paquete cambia automáticamente a &quot;[!UICONTROL Frontload]&quot;, aunque esté establecida en &quot;[!UICONTROL even]&quot;. Esto significa que el 65% del presupuesto diario debería entregarse antes de las 11:30 a.m. EST.

>[!MORELIKETHIS]
>
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md)
