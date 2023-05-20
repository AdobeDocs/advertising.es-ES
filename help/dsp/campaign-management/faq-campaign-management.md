---
title: Preguntas frecuentes sobre Campaign Management
description: Obtenga más información acerca de la administración de campañas, incluido el período de latencia de los cambios y lo que sucede cuando se realizan cambios de presupuesto durante un vuelo.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: 2fb3f227d74d8c8893a3cb042ea91121a0fae7c0
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Preguntas frecuentes sobre Campaign Management

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latencia de los cambios de configuración

* Cuando cambie una ubicación o una configuración de paquete, ¿cuándo se aplicará el cambio?

   Los cambios de configuración suelen surtir efecto inmediatamente, pero pueden tardar hasta 12 horas.

   DSP Si es el último día de envío, realice cambios al principio del día para que tenga tiempo de sobra para volver a calibrar el paquete en función de los cambios. DSP Por ejemplo, si cambia del ritmo uniforme al ritmo de carga frontal, debe volver a evaluar cómo distribuirá el gasto a lo largo del resto del vuelo, ya que esto se realiza de forma más sencilla y precisa. No realice ese tipo de cambio si solo le queda una hora para entregar en el último día del vuelo.

## Actualizaciones de presupuesto en mitad del vuelo

* DSP Cuando realiza un cambio en una ubicación, ¿cuánto tiempo tarda el usuario en reasignar el presupuesto del paquete?

   La asignación del presupuesto se basa en el rendimiento de la ubicación, que se evalúa con un promedio de 14 días. Los cambios en una ubicación producen cambios en la asignación del presupuesto solo cuando provocan cambios en el rendimiento durante la media de 14 días.

   DSP Cuando se producen cambios de rendimiento, reasigna el presupuesto del paquete entre las ubicaciones en consecuencia durante el siguiente ciclo de optimización del presupuesto, que se produce aproximadamente a medianoche (00:00) en el huso horario de la campaña.

* ¿Cómo se reasigna el presupuesto cuando se elimina una ubicación de un paquete y se agrega a otro paquete?

   Todo el historial de gasto de una ubicación se adjunta a la ubicación y se mueve con ella de paquete en paquete.

   Al eliminar una ubicación de un paquete, el paquete ya no tiene historial de gasto de la ubicación. El presupuesto del paquete pasará a ser (presupuesto del paquete, presupuesto de colocación eliminado) / intervalo de tiempo que queda en vuelo. A continuación, el presupuesto del paquete se asigna a las ubicaciones que quedan en el paquete.

   DSP Del mismo modo, si agrega la misma ubicación a un paquete diferente, considera el historial de gasto de la ubicación cuando asigna el presupuesto para todas las ubicaciones en el nuevo paquete.

* ¿Cómo cambia el ritmo del paquete en el último día de un vuelo?

   El último día de un vuelo, el día se acorta de 24 horas a 23 horas para que no se exceda el presupuesto del paquete. Además, la estrategia de relleno de ritmo del paquete cambia automáticamente a &quot;[!UICONTROL Frontload],&quot; incluso si está configurado en &quot;[!UICONTROL even].&quot; Esto significa que el 65% del presupuesto diario debería entregarse antes de las 11:30 a.m. EST.

>[!MORELIKETHIS]
>
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md)

