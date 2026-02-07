---
title: Configuración de paquetes
description: Consulte las descripciones de la configuración del paquete disponible.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 86d77d23fbec15b1f80f3f9c41e66aab34a46079
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Configuración de paquetes

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** El nombre del paquete. La longitud máxima es de 60 caracteres.

**[!UICONTROL Description]:** (opcional) Una descripción del paquete.

**[!UICONTROL 3rd Party Billed Fees]:** (Opcional) Se rastreará una tarifa estática de terceros como un costo no facturable:

* **[!UICONTROL CPM]:** El costo por 1000 impresiones (CPM).

* **[!UICONTROL Description]:** Una descripción de la tarifa de CPM.

>[!NOTE]
>
>Las tarifas facturables se reflejan en la métrica [!UICONTROL Net CPM].

Puede anular la configuración de nivel de paquete en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (de solo lectura para paquetes existentes) En qué nivel colocar y limitar las ubicaciones en el paquete:

* **[!UICONTROL Package level pacing]:** Esta estrategia de ritmo funciona mediante el ritmo y el límite de todas las ubicaciones incluidas como *grupo*. Esta estrategia garantiza que todas las ubicaciones dentro de un paquete determinado se optimicen de forma integral, distribuyendo el gasto en función del rendimiento y la escala a indicadores clave de rendimiento (KPI) seleccionados.

* **[!UICONTROL Placement level pacing]:** Esta estrategia de ritmo funciona mediante el ritmo y el límite de todas las ubicaciones incluidas *individualmente*. La práctica recomendada es utilizar esta estrategia solo para ejecutar ofertas de mercado privado garantizadas.

**[!UICONTROL Flight Dates]:** La fecha de inicio y finalización general del paquete. Las fechas de vuelo deben incluirse dentro de las fechas de vuelo de la campaña.

>[!NOTE]
>
>* Las fechas de vuelo de todas las ubicaciones asignadas a este paquete deben incluirse dentro de estas fechas.
> * No se puede editar la fecha de inicio del paquete cuando se activa el vuelo personalizado.

**[!UICONTROL Activate Custom Flighting]:** Le permite crear vuelos de ritmo sin par para el paquete en la sección [!UICONTROL Flighting] a continuación. Una vez que habilite el vuelo personalizado y guarde el paquete, no podrá deshabilitar el vuelo personalizado ni editar la fecha de inicio del paquete.

**[!UICONTROL Budget]:** (Paquetes con ritmo de nivel de paquete solamente) El límite presupuestario bruto y el intervalo presupuestario.

Para paquetes con vuelo personalizado, el intervalo de presupuesto siempre es *[!UICONTROL All time]*. Para los paquetes sin vuelo personalizado, especifique el intervalo de presupuesto: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Paquetes con ritmo de nivel de paquete y solo administración dinámica de márgenes) Límite de presupuesto bruto para la duración del paquete.

**[!UICONTROL Optimization Goal]:** (Paquetes con ritmo de nivel de paquete solamente) El objetivo de optimización del paquete. Consulte las descripciones de cada objetivo de optimización en [Objetivos de optimización y cómo usarlos](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Link PG Placements for Incremental Reach Optimization]:** (Paquetes con ritmo a nivel de paquete y con los objetivos de optimización &quot;[!UICONTROL Always Max Bid & Maximize Reach]&quot; y &quot;[!UICONTROL Lowest Cost per Reach]&quot; solamente) Utiliza los datos de alcance doméstico de todas las ubicaciones garantizadas mediante programación en la campaña para optimizar el alcance incremental.

**[!UICONTROL Custom Goal for Model Learning]:** (Paquetes con los objetivos de optimización &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solamente) Un [objetivo personalizado](/help/dsp/optimization/custom-goal.md) que incluye los eventos de ingresos o conversión usados para calcular la métrica de CPA o ROAS. El objetivo personalizado debe incluir eventos de funnel superior ponderados adicionales (como visitas a la página y adiciones al carro de compras) que se utilizarán además de la métrica de CPA o ROAS para la optimización de paquetes. Para obtener más información acerca de los objetivos personalizados, incluidas las prácticas recomendadas para crear objetivos personalizados y campañas que los usen, consulte &quot;[Objetivos personalizados](/help/dsp/optimization/custom-goal.md)&quot; y &quot;[Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md)&quot;.<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Opcional; paquetes con los objetivos de optimización &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solamente) Indica al modelo de optimización que aprenda solamente de las conversiones basadas en clics. De lo contrario, el modelo de optimización aprende de las conversiones basadas en clics e impresiones.

**[!UICONTROL Conversion Metric]:** (Paquetes con los objetivos de optimización &quot;[!UICONTROL Highest Return on Ad Spend]&quot; y &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solamente) El evento de conversión final (como suscripciones) o el importe de evento/venta de ingresos (como compras y valores de compra) que se utilizará para calcular la rentabilidad del gasto en publicidad o el coste por adquisición. Seleccione de una lista de todos los eventos principales (&quot;métricas de objetivo&quot;) asignados al objetivo personalizado seleccionado. Si la lista está vacía, edite el objetivo personalizado para incluir al menos uno de los eventos subyacentes como métrica de objetivo.

**[!UICONTROL Package Goal Type]:** (paquetes con objetivos de optimización personalizados solamente) El propósito del paquete. Esta configuración ayuda a determinar cómo optimizar el paquete:

* *[!UICONTROL Prospecting]:* Los paquetes de prospección se centran en la adquisición de nuevos clientes.

* *[!UICONTROL Retargeting]:* Los paquetes de redireccionamiento se centran en volver a exponer a visitantes o clientes anteriores.

* *[!UICONTROL Other]:* Todos los demás propósitos.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (paquetes con objetivos de optimización personalizados solamente) Otro paquete cuyos datos históricos se usan como entrada para optimizar el paquete.

**[!UICONTROL Target]:** (Paquetes con ritmo de nivel de paquete solamente) El objetivo de destino, que se usa para rastrear el rendimiento.

>[!NOTE]
>
>Este campo es solo un punto de referencia y no se utiliza para la toma de decisiones.

**[!UICONTROL Frequency Cap]:** (paquetes con ritmo a nivel de paquete solamente) El número de veces que un dispositivo único, un identificador universal o una persona (dependiendo del [!UICONTROL Cross Device Level] especificado para la campaña y de la configuración de la ubicación [!UICONTROL Targeting]) se pueden servir anuncios desde el paquete. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
>* Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respeta el límite de frecuencia más estricto en la jerarquía de campañas.
>* La práctica recomendada es establecer límites de frecuencia tanto para la prospección como para la reorientación en el nivel de paquete.
> * Los límites de frecuencia más altos resultan en un mayor gasto e impresiones, pero un menor alcance. Los límites de frecuencia más bajos resultan en un menor gasto e impresiones, pero un mayor alcance.

**[!UICONTROL Pace on]:** (Paquetes con ritmo de nivel de paquete solamente) En qué se basa el ritmo:

* *[!UICONTROL Budget]:* (Predeterminado) Esta opción proporciona tantas impresiones como sea posible dentro del presupuesto del paquete asignado.

* *[!UICONTROL Impressions]:* Esta opción envía impresiones hasta que se alcance una cantidad especificada dentro de un intervalo especificado. Cuando seleccione esta opción, especifique el número de impresiones y el intervalo: *Todo el tiempo,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (paquetes con ritmo de nivel de paquete solamente) Cómo realizar el ritmo y la entrega en todo el vuelo:

* *[!UICONTROL Even]:* Rastrea la entrega de forma uniforme en cada vuelo, con un objetivo del 50% de la entrega en la primera mitad del vuelo.

* *[!UICONTROL Slightly Ahead]:* (El valor predeterminado) Acelera la entrega para que se complete en un 55-65 % a mitad de la duración del vuelo.

* *[!UICONTROL Frontload]:* Acelera la entrega para que se complete en un 65-75% a mitad del vuelo.

* *[!UICONTROL Aggressive Frontload]:* Acelera la entrega para que se complete en un 75-85% a mitad del vuelo.

**[!UICONTROL Intraday pacing]:** (Paquetes con ritmo de nivel de paquete solamente) Cómo realizar el ritmo y la entrega a lo largo de cada día dentro del vuelo:

* *[!UICONTROL Even]:* (El valor predeterminado) Escala el envío según la disponibilidad del inventario. Por lo general, se publican más anuncios por hora durante el día, cuando el volumen de subasta es mayor, y menos anuncios por las mañanas y las noches.

* *[!UICONTROL ASAP]:* Acelera el envío al doble de la velocidad de *Even*.

  >[!CAUTION]
  >
  >Esta opción puede afectar negativamente al rendimiento. Utilícelo únicamente cuando priorice completamente la entrega y gaste en lugar de optimizar el rendimiento.

## [!UICONTROL Flighting]

(Paquetes con ritmo de nivel de paquete) Los períodos de vuelo del paquete, incluidos los períodos de vuelo personalizados dentro del total de [!UICONTROL Flight Dates] para el paquete. Solo puede configurar vuelos personalizados cuando la opción [!UICONTROL Activate Custom Flighting] esté habilitada en la sección [!UICONTROL Goals & Budget].

**[!UICONTROL Automatically rollover remaining flight budget to next flight]:** (disponible solo cuando la opción [!UICONTROL Activate Custom Flighting] está habilitada) Agrega automáticamente cualquier presupuesto restante del vuelo anterior al presupuesto existente para el siguiente vuelo.

En la vista [!UICONTROL Packages] y en la vista [!DNL Package Name] > [!UICONTROL Flights], el campo [!UICONTROL Interval Goal], que muestra la meta de vuelo actual, incluye cualquier presupuesto de rollover.

**[!DNL Flight N]:** (disponible solo cuando la opción [!UICONTROL Activate Custom Flighting] está habilitada) Para cada vuelo, especifique la fecha de inicio, la fecha de finalización y la meta de gasto de destino. Para agregar otro vuelo, haga clic en **[!UICONTROL Add Flight]**.

En el caso de los paquetes existentes sin la opción &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; habilitada, puede volver a abrir la configuración para escribir un valor en la columna **[!UICONTROL Rollover]** para cualquier vuelo a fin de agregar el presupuesto no utilizado potencial al siguiente vuelo.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de paquetes](package-about.md)
>* [Crear un paquete](package-create.md)
>* [Editar un paquete](package-edit.md)
>* [Adjuntar una ubicación a un paquete](package-attach-placement.md)
>* [Ver el registro de cambios de un paquete](package-change-log.md)
>* [Preguntas frecuentes sobre la administración de campañas](/help/dsp/campaign-management/faq-campaign-management.md)
