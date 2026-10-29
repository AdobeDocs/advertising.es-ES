---
title: Resolución de problemas de rendimiento y entrega mediante el asistente de IA
description: Utilice el agente de resolución de problemas del asistente de IA de Adobe Advertising DSP para diagnosticar problemas de gasto, ritmo y entrega de paquetes y ubicaciones de DSP.
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
source-git-commit: 0f6d32b5409cc95f09d0b0f28cdeee72a7861892
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%
---
# Solución de problemas de rendimiento y envío mediante el Asistente de IA

*característica de Beta*

*Sólo soporte en inglés*

El agente de solución de problemas del asistente de IA identifica los factores que limitan el rendimiento de los paquetes y las ubicaciones activos y proporciona instrucciones paso a paso y recomendaciones basadas en datos históricos para resolver problemas. El agente de solución de problemas puede ayudar a diagnosticar los siguientes tipos de problemas de rendimiento y envío:

* (Solo ubicaciones) Problemas de gasto, incluidos exceso de gasto, infrautilización y fallo de gasto. El agente evalúa los factores relacionados con el ritmo, las ofertas, el objetivo y el límite presupuestario como parte del diagnóstico.

* (Solo paquetes) Problemas de rendimiento, incluido un CPA en aumento o un ROAS en caída. El agente no diagnostica métricas de participación como CTR, CPC, clics o impresiones.

Cada conversación cubre un único diagnóstico para un solo paquete o ubicación. Una vez que el agente envía un resultado, inicie una nueva conversación para preguntar sobre un problema diferente, o sobre un paquete o ubicación diferente.

El agente no puede cambiar la configuración, crear o editar campañas o componentes de campaña, ni diagnosticar problemas para un paquete o ubicación en pausa, completada, archivada o programada.

>[!IMPORTANT]
>
>Las respuestas generadas por IA pueden ser inexactas o engañosas. Compruebe siempre las respuestas y las fuentes antes de utilizarlas para tomar decisiones que afecten a los costes o al esfuerzo.

## Consultas de ejemplo

### Resolución de problemas de gasto de colocación

* Mi colocación dejó de gastar ayer a pesar de que el acuerdo está activo. ¿Por qué?

* ¿Por qué esta colocación ha estado gastando menos de lo previsto durante los últimos 5 días?

* Estamos a mitad de camino en el vuelo y significativamente por detrás en el ritmo. ¿Por qué?

### Solución de problemas de rendimiento del paquete

* ¿Por qué ha aumentado la CPA para este paquete en la última semana?

* ¿Por qué el ROAS rechaza este paquete?

## Enviar una consulta desde el Asistente de IA

Puede hacer varias preguntas en un mensaje, pero solo un mensaje a la vez. Espere una respuesta antes de enviar otra.

1. En la parte superior derecha de cualquier página, haz clic en ![Chat agéntico](/help/dsp/assets/agent-chat.png "Chat agéntico").

1. Cree la consulta:

   * Introduzca su propia consulta.

   * Para ver ejemplos de consultas, haga clic en **[!UICONTROL Troubleshoot]** para expandir la sección.

     1. (Opcional) Para copiar el texto de una consulta de ejemplo en el campo de entrada:

        1. Haga clic en el ejemplo.

        1. (Opcional) Edite el texto para adaptarlo a sus necesidades.

   Para obtener más información acerca de las consultas, vea &quot;[Prácticas recomendadas para escribir consultas y avisos](ai-assistant-about.md#writing-queries)&quot;.

   >[!NOTE]
   >
   >* Si no especifica un intervalo de fechas, el agente selecciona un valor predeterminado razonable en función del tipo de problema. Por ejemplo, si pregunta por las métricas de campaña sin especificar un intervalo de fechas, los resultados son para la duración de la campaña.
   >* Si tiene en mente un CPA objetivo, inclúyalo en la consulta (por ejemplo, &quot;diagnostique el CPA con un objetivo de 50 $&quot;). Si no especifica ninguno, el agente utilizará un destino predeterminado.

1. Haga clic en ![Enviar consulta](/help/dsp/assets/submit-prompt.png "Enviar consulta") o presione la tecla **Intro** del teclado.

1. Si el Asistente de IA solicita información adicional, proporciónelo.

>[!TIP]
>
>Para preguntar sobre un problema diferente, o sobre un paquete o ubicación diferente, [inicia una nueva conversación](#conversation-new).

## Enviar una consulta desde la vista [!UICONTROL Packages] o [!UICONTROL Placements]

Puede hacer varias preguntas en un mensaje, pero solo un mensaje a la vez. Espere una respuesta antes de enviar otra.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. Realice una de las siguientes acciones:

   * (Para paquetes) En la vista [!UICONTROL Packages], haga clic en **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** junto al nombre del paquete.

   * (Para ubicaciones) En el submenú, haga clic en **[!UICONTROL Placements]**. Junto al nombre de la ubicación, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Cree la consulta:

   * Introduzca su propia consulta.

   * Para ver ejemplos de consultas, haga clic en **[!UICONTROL Troubleshoot]** para expandir la sección.

     1. (Opcional) Para copiar el texto de una consulta de ejemplo en el campo de entrada:

        1. Haga clic en el ejemplo.

        1. (Opcional) Edite el texto para adaptarlo a sus necesidades.

   Para obtener más información acerca de las consultas, vea &quot;[Prácticas recomendadas para escribir consultas y avisos](ai-assistant-about.md#writing-queries)&quot;.

   >[!NOTE]
   >
   >* Si no especifica un intervalo de fechas, el agente selecciona un valor predeterminado razonable en función del tipo de problema. Por ejemplo, si pregunta por las métricas de campaña sin especificar un intervalo de fechas, los resultados son para la duración de la campaña.
   >* Si tiene en mente un CPA objetivo, inclúyalo en la consulta (por ejemplo, &quot;diagnostique el CPA con un objetivo de 50 $&quot;). Si no especifica ninguno, el agente utilizará un destino predeterminado.

1. Haga clic en ![Enviar consulta](/help/dsp/assets/submit-prompt.png "Enviar consulta") o presione la tecla **Intro** del teclado.

1. Si el Asistente de IA solicita información adicional, proporciónelo.

>[!TIP]
>
>Para preguntar sobre un problema diferente, o sobre un paquete o ubicación diferente, [inicia una nueva conversación](#conversation-new).

## Iniciar una nueva conversación {#conversation-new}

Cada conversación (o hilo de consulta) se guarda por separado para que pueda distinguir entre sus conversaciones anteriores.

1. En la parte superior de [chat](#ai-assistant-open), haz clic en ![Iniciar una nueva conversación](/help/dsp/assets/new-selection.png "Iniciar una nueva conversación").

1. [Enviar una consulta](#query-submit).

## Expandir y minimizar el cuadro de diálogo

1. En la parte superior de [chatbox](#ai-assistant-open), haz clic en ![Introducir pantalla completa](/help/dsp/assets/fullscreen.png "Introducir pantalla completa") para ingresar al modo de pantalla completa.

1. Para volver al modo de panel, haga clic en **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [Acerca del Asistente de IA en Advertising DSP](ai-assistant-about.md)
>* [Trabajar con conversaciones anteriores del Asistente de IA](previous-conversations.md)
