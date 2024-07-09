---
title: Configuración de paquetes
description: Consulte las descripciones de la configuración del paquete disponible.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 644847918f6f6dd86dec80ad89128c31a0c0284b
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Configuración de paquetes

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** El nombre del paquete. La longitud máxima es de 60 caracteres.

**[!UICONTROL Description]:** (Opcional) Una descripción del paquete.

**[!UICONTROL 3rd Party Billed Fees]:** (Opcional) Una tarifa estática de terceros que se rastreará como un coste no facturable:

* **[!UICONTROL CPM]:** El coste por 1000 impresiones (CPM).

* **[!UICONTROL Description]:** Una descripción de la tarifa del CPM.

>[!NOTE]
>
>Las tarifas facturables se reflejan en la [!UICONTROL Net CPM] métrica.

Puede anular la configuración de nivel de paquete en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Solo lectura para paquetes existentes) En qué nivel espaciar y limitar las ubicaciones en el paquete:

* **[!UICONTROL Package level pacing]:** Esta estrategia de ritmo funciona mediante el ritmo y el límite de todas las ubicaciones incluidas como *grupo*. Esta estrategia garantiza que todas las ubicaciones dentro de un paquete determinado se optimicen de forma integral, distribuyendo el gasto en función del rendimiento y la escala a indicadores clave de rendimiento (KPI) seleccionados.

* **[!UICONTROL Placement level pacing]:**  Esta estrategia de ritmo funciona mediante el ritmo y el límite de todas las ubicaciones incluidas *individualmente*. La práctica recomendada es utilizar esta estrategia solo para ejecutar ofertas de mercado privado garantizadas.

**[!UICONTROL Flight Dates]:** La fecha de inicio y de finalización general del paquete. Las fechas de vuelo deben incluirse dentro de las fechas de vuelo de la campaña.

>[!NOTE]
>
>* Las fechas de vuelo de todas las ubicaciones asignadas a este paquete deben incluirse dentro de estas fechas.
> * No se puede editar la fecha de inicio del paquete cuando se activa el vuelo personalizado.

**[!UICONTROL *Activate Custom Flighting]:** Permite crear vuelos de ritmo desigual para el paquete en el [!UICONTROL Flighting] más abajo. Una vez que habilite el vuelo personalizado y guarde el paquete, no podrá deshabilitar el vuelo personalizado ni editar la fecha de inicio del paquete.

**[!UICONTROL Budget]:** (Paquetes con solo ritmo de nivel de paquete) El límite presupuestario bruto y el intervalo presupuestario.

Para paquetes con vuelo personalizado, el intervalo presupuestario siempre es *[!UICONTROL All time]*. Para los paquetes sin vuelo personalizado, especifique el intervalo presupuestario: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Paquetes con ritmo a nivel de paquete y solo administración dinámica de márgenes) El límite presupuestario bruto durante la duración del paquete.

**[!UICONTROL Optimization Goal]:** (Paquetes con solo ritmo de nivel de paquete) El objetivo de optimización del paquete. Consulte las descripciones de cada objetivo de optimización en [Objetivos de optimización y cómo utilizarlos](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Paquetes con el signo &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solo objetivos de optimización) A [meta personalizada](/help/dsp/optimization/custom-goal.md) que incluye los eventos de ingresos o conversión utilizados para calcular la métrica de CPA o ROAS. El objetivo personalizado puede incluir opcionalmente eventos de canal superior ponderados adicionales (como visitas a la página y adiciones al carro de compras) que se utilizarán además de la métrica de CPA o ROAS para la optimización de paquetes. Para obtener más información sobre las prácticas recomendadas para los objetivos personalizados y las campañas que los utilizan, consulte [Prácticas recomendadas para crear una meta personalizada](/help/dsp/optimization/custom-goal.md#custom-goal-best-practices) y [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md).<!-- At some point, all of the objectives will be prefixed with "ADSP " -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Opcional; paquetes con &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; (Solo objetivos de optimización) Indica al modelo de optimización que aprenda solo de las conversiones basadas en clics. De lo contrario, el modelo de optimización aprende de las conversiones basadas en clics e impresiones.

**[!UICONTROL Conversion Metric]:** (Opcional; paquetes con &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;Solo objetivos de optimización&quot;) El evento de conversión final (como las suscripciones) o el importe de evento/venta de ingresos (como compras y valores de compra) que se utilizará para calcular la rentabilidad del gasto en publicidad o el coste por adquisición. Seleccione de una lista de todos los eventos principales (&quot;métricas de objetivo&quot;) asignados al objetivo personalizado seleccionado. Si la lista está vacía, edite el objetivo personalizado para incluir al menos uno de los eventos subyacentes como métrica de objetivo.

**[!UICONTROL Package Goal Type]:** (Solo paquetes con objetivos de optimización personalizados) El propósito del paquete. Esta configuración ayuda a determinar cómo optimizar el paquete:

* *[!UICONTROL Prospecting]:* Los paquetes de prospección se centran en adquirir nuevos clientes.

* *[!UICONTROL Retargeting]:* Los paquetes de redireccionamiento se centran en volver a exponer a visitantes o clientes anteriores.

* *[!UICONTROL Other]:* Todos los demás propósitos.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Solo paquetes con objetivos de optimización personalizados) Otro paquete cuyos datos históricos se utilizan como entrada para optimizar el paquete.

**[!UICONTROL Target]:** (Paquetes con ritmo solo en el nivel de paquete) El objetivo, que se utiliza para rastrear el rendimiento.

>[!NOTE]
>
>Este campo es solo un punto de referencia y no se utiliza para la toma de decisiones.

**[!UICONTROL Frequency Cap]:** (Paquetes con ritmo de nivel de paquete solamente) El número de veces que un dispositivo único, ID universal o persona (según el especificado) [!UICONTROL Cross Device Level] para la campaña y la ubicación [!UICONTROL Targeting] configuración) se pueden servir anuncios desde el paquete. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
>* Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respeta el límite de frecuencia más estricto de la jerarquía de campañas.
>* La práctica recomendada es establecer límites de frecuencia tanto para la prospección como para la reorientación en el nivel de paquete.
> * Los límites de frecuencia más altos resultan en un mayor gasto e impresiones, pero un menor alcance. Los límites de frecuencia más bajos resultan en un menor gasto e impresiones, pero un mayor alcance.

**[!UICONTROL Pace on]:** (Paquetes con solo ritmo de nivel de paquete) En qué se basa el ritmo:

* *[!UICONTROL Budget]:* (Predeterminado) Esta opción ofrece tantas impresiones como sea posible dentro del presupuesto del paquete asignado.

* *[!UICONTROL Impressions]:* Esta opción envía impresiones hasta que se alcanza una cantidad especificada dentro de un intervalo especificado. Cuando seleccione esta opción, especifique el número de impresiones y el intervalo: *Todo el tiempo,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Paquetes solo con ritmo a nivel de paquete) Cómo realizar el ritmo y la entrega en todo el vuelo:

* *[!UICONTROL Even]:* Rastrea la entrega de forma uniforme en cada vuelo, con un objetivo del 50 % de la entrega en la primera mitad del vuelo.

* *[!UICONTROL Slightly Ahead]:* (Predeterminado) Acelera la entrega de modo que se complete en un 55-65 % a mitad de la duración del vuelo.

* *[!UICONTROL Frontload]:* Acelera la entrega para que esté 65-75% completo a mitad del vuelo.

* *[!UICONTROL Aggressive Frontload]:* Acelera la entrega para que esté entre el 75 y el 85% completo a mitad del vuelo.

**[!UICONTROL Intraday pacing]:** (Paquetes solo con ritmo a nivel de paquete) Cómo realizar el ritmo y la entrega a lo largo de cada día dentro del vuelo:

* *[!UICONTROL Even]:* (El valor predeterminado) Escala el envío según la disponibilidad del inventario. Por lo general, se publican más anuncios por hora durante el día, cuando el volumen de subasta es mayor, y menos anuncios por las mañanas y las noches.

* *[!UICONTROL ASAP]:* Acelera la entrega al doble de la velocidad de *Uniforme*.

  >[!CAUTION]
  >
  >Esta opción puede afectar negativamente al rendimiento. Utilícelo únicamente cuando priorice completamente la entrega y gaste en lugar de optimizar el rendimiento.

## [!UICONTROL Flighting]

(Paquetes con ritmo de nivel de paquete) Los períodos de vuelo del paquete, incluidos los períodos de vuelo personalizados dentro del total [!UICONTROL Flight Dates] para el paquete. Solo puede configurar vuelos personalizados cuando la variable [!UICONTROL Activate Custom Flighting] está activada en la [!UICONTROL Goals & Budget] sección.

**[!DNL Flight N]:** (Disponible solo cuando la variable [!UICONTROL Activate Custom Flighting] (opción activada) Para cada vuelo, especifique la fecha de inicio, la fecha de finalización y la meta de gasto objetivo. Para añadir otro vuelo, haga clic en **[!UICONTROL Add Flight]**.

Para los paquetes existentes, puede introducir un valor en la variable [!UICONTROL Rollover] columna para cualquier vuelo a fin de añadir el posible presupuesto no utilizado al siguiente vuelo. El valor proyectado en [!UICONTROL Adjusted Goal (Goal + Rollover)] se cambia en consecuencia.<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [Acerca de la administración de paquetes](package-about.md)
>* [Crear un paquete](package-create.md)
>* [Edición de un paquete](package-edit.md)
>* [Adjuntar una ubicación a un paquete](package-attach-placement.md)
>* [Visualización del registro de cambios de un paquete](package-change-log.md)
>* [Preguntas frecuentes sobre Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
