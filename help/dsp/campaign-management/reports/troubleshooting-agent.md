---
title: Diagnosticar problemas de rendimiento y envío con [!UICONTROL Troubleshooting Agent] asistido por IA
description: Aprenda a utilizar el agente de resolución de problemas asistido por IA para diagnosticar problemas de gasto, ritmo y entrega de paquetes y ubicaciones de DSP.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 31ddb7928ca4e43132087b73829af55ae6315b0d
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%
---
# Diagnosticar problemas de rendimiento y envío con [!UICONTROL Troubleshooting Agent] asistido por IA

[!UICONTROL Troubleshooting Agent] con asistencia de IA identifica factores que limitan el rendimiento y proporciona recomendaciones para resolver problemas. [!UICONTROL Troubleshooting Agent] puede:

* Ayuda para diagnosticar problemas de rendimiento y entrega para un paquete o una ubicación en directo seleccionados:

  * (Solo ubicaciones) Problemas de gasto, incluidos exceso de gasto, infrautilización y fallo de gasto. El agente evalúa los factores relacionados con el ritmo, las ofertas, el objetivo y el límite presupuestario como parte del diagnóstico.

  * (Solo paquetes) Problemas de rendimiento, incluido un CPA en aumento o un ROAS en caída. El agente no diagnostica métricas de participación como CTR, CPC, clics o impresiones.

  Cada conversación cubre un único diagnóstico para un solo paquete o ubicación. Una vez que el agente envía un resultado, inicie una nueva conversación para preguntar sobre un problema diferente, o sobre un paquete o ubicación diferente.

  El agente no puede cambiar la configuración ni crear ni editar campañas o componentes de campañas. Tampoco puede diagnosticar problemas para un paquete o una ubicación en pausa, completada, archivada o programada.

* Busque contenido conceptual y explicativo en la [Guía de Advertising DSP](/help/dsp/home.md) y (anunciantes con Advertising Creative) en la [Guía de Advertising Creative](/help/creative/home.md), de la misma manera que en la [interfaz de Agentic Chat](/help/dsp/agent-chat.md). Puede preguntar sobre la administración de campañas, optimización, administración de audiencias, ofertas, informes y otras funciones del producto.

>[!IMPORTANT]
>
>Las respuestas generadas por IA pueden ser inexactas o engañosas. Compruebe siempre las respuestas y las fuentes antes de utilizarlas para tomar decisiones que afecten a los costes o al esfuerzo.

## Consultas de ejemplo

>[!NOTE]
>
>No es necesario especificar un intervalo de fechas. Si no incluye uno, el agente selecciona un valor predeterminado razonable en función del tipo de problema.

### Ubicaciones: problemas de gasto

* Mi colocación dejó de gastar ayer a pesar de que el acuerdo está activo. ¿Por qué?

* ¿Por qué esta colocación ha estado gastando menos de lo previsto durante los últimos 5 días?

* Estamos a mitad de camino en el vuelo y significativamente por detrás en el ritmo. ¿Por qué?

### Paquetes: problemas de rendimiento

* ¿Por qué ha aumentado la CPA para este paquete en la última semana?

* ¿Por qué el ROAS rechaza este paquete?

>[!TIP]
>
>Si tiene en mente un CPA objetivo, inclúyalo en la consulta (por ejemplo, &quot;diagnostique el CPA con un objetivo de 50 $&quot;). Si no especifica ninguno, el agente utilizará un destino predeterminado.

### Características del producto:

* ¿Cómo se crea una ubicación?

* ¿Qué opciones de segmentación están disponibles en Adobe DSP?

* ¿Cómo adjunto un anuncio a una ubicación?

* ¿Cuáles son las consecuencias de utilizar las diferentes opciones de ritmo en la configuración de ubicación?

* ¿Cuándo debo usar cada tipo de objetivo de optimización?

* ¿Por qué las ubicaciones garantizadas mediante programación (PG) no sirven para las impresiones?

* ¿Qué informes incluyen datos a nivel de hogar?

* ¿Cuál es la diferencia entre una experiencia de destino y una experiencia sin destino en [!DNL Creative]?

* ¿Cómo creo una etiqueta de anuncio para una experiencia de [!DNL Creative]?

## Enviar una consulta para un paquete o una ubicación activos

Puede hacer varias preguntas en un mensaje, pero solo un mensaje a la vez. Espere una respuesta antes de enviar otra.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. Realice una de las acciones siguientes:

   * (Para paquetes) En la vista [!UICONTROL Packages], haga clic en **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** junto al nombre del paquete.

   * (Para ubicaciones) En el submenú, haga clic en **[!UICONTROL Placements]**. Junto al nombre de la ubicación, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Escriba su consulta y haga clic en ![Enviar solicitud](/help/dsp/assets/submit-prompt.png "Enviar solicitud").

   <!-- For more information, see "[Writing prompts](#writing-prompts)." -->

   Para las consultas de rendimiento y envío, la respuesta incluye factores que limitan el rendimiento y proporciona recomendaciones para resolver los problemas.

   Para consultas de documentación, la respuesta incluye citas en línea y una lista **[!UICONTROL Documentation Sources]** en la parte inferior. También pueden aparecer preguntas de seguimiento y sugerencias.

1. (Solo consultas de documentación; opcional) Para abrir una página utilizada como fuente de datos, siga uno de estos procedimientos:

   * Haga clic en la cita numerada.

   * Haga clic en **[!UICONTROL Documentation Sources]** para mostrar una lista de todas las páginas citadas en la respuesta y luego haga clic en el vínculo de la página.

1. (Opcional) Clasifique la respuesta con los miniaturas hacia arriba o hacia abajo.

>[!TIP]
>
>Para preguntar sobre un problema diferente, o sobre un paquete o ubicación diferente, inicia una nueva conversación.
