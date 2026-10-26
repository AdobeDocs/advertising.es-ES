---
title: Acerca del asistente de IA en Advertising DSP
description: Aprenda a utilizar el asistente de IA de DSP para solucionar problemas de paquetes y ubicaciones, crear informes y buscar ayuda sobre el uso del producto.
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
source-git-commit: 8bab50fe8bf737d208d059d89b2592e16bc40c69
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%
---
# Acerca del asistente de IA en Advertising DSP

El asistente de IA de DSP es una interfaz conversacional que le permite realizar cualquier flujo de trabajo auténtico disponible en DSP desde una sola bandeja de chat. Puede crear una tarea nueva o pedir ayuda para continuar una tarea anterior.

El historial de conversaciones se mantiene para todos los flujos de trabajo, y cada conversación se nombra automáticamente. Las consultas no se comparten con otros usuarios.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Flujos de trabajo admitidos

Los siguientes flujos de trabajo pueden ayudarle a realizar su trabajo de forma más eficaz:

<!-- And links to all sections/pages -->

| Función | Descripción | Consultas de ejemplo | Respuestas |
| --- | --- | --- | --- |
| [Solución de problemas](troubleshooting-agent.md) | Diagnosticar problemas de rendimiento y entrega para un paquete o una ubicación en directo seleccionados.<ul><li>Solo ubicaciones: Diagnosticar el exceso de gasto, la infrautilización y el fallo en el gasto. El agente evalúa los factores de ritmo, oferta, objetivo y límite presupuestario relacionados.</li><li>Solo paquetes: diagnostique problemas de rendimiento, incluido un CPA en aumento o un ROAS en caída. El agente no diagnostica métricas de participación como CTR, CPC, clics o impresiones.</li></ul>Cada conversación cubre un diagnóstico para un paquete o ubicación. Después de recibir un resultado, inicie una nueva conversación para diagnosticar otro problema, paquete o ubicación.<br><br>El agente no puede cambiar la configuración ni crear o editar campañas o componentes de campañas. Tampoco puede diagnosticar paquetes o ubicaciones en pausa, completados, archivados o programados. | Problemas de gasto en colocación:<ul><li>Mi colocación dejó de gastar ayer a pesar de que el acuerdo está activo. ¿Por qué?</li><li>¿Por qué esta colocación ha estado gastando menos de lo previsto durante los últimos 5 días?</li><li>Estamos a mitad de camino en el vuelo y significativamente por detrás en el ritmo. ¿Por qué?</li></ul>Problemas de rendimiento del paquete:<ul><li>¿Por qué ha aumentado la CPA para este paquete en la última semana?</li><li>¿Por qué el ROAS rechaza este paquete?</li></ul> | La respuesta incluye factores que limitan el rendimiento y proporciona recomendaciones para resolver los problemas. |
| [Datos](insights-agent.md) | Obtenga métricas de campaña e informes completos sin crear manualmente un informe. Puede hacer preguntas sencillas sobre una métrica específica, como gasto o CPA para una campaña, o solicitar un informe más complejo para una dimensión específica (como una campaña, ubicación o audiencia únicas) o entre dimensiones (para desgloses por campaña y anunciante). Puede descargar los resultados como archivo CSV. | <ul><li>¿Cuánto gastó [Campaign Name] la semana pasada?<li>¿Cuántas conversiones obtuvo [Campaign Name] este mes?</li><li>¿Qué ubicaciones están detrás del ritmo en más del 20 %?</li></li>Mostrarme el CPA por paquete para [Nombre de campaña]</li></ul> | Se muestran las primeras filas del informe, con vínculos para obtener una vista previa del informe completo y descargar el informe como un archivo de valores separados por comas (.csv) de [!DNL Microsoft Excel]. |
| [Búsqueda de documentación del producto](documentation-search.md) | Busque contenido conceptual y explicativo en la [Guía de Advertising DSP](/help/dsp/home.md) y, para anunciantes con Advertising Creative, en la [Guía de Advertising Creative](/help/creative/home.md). Las respuestas se basan únicamente en lo que se ha documentado para estos productos en [Experience League](https://experienceleague.adobe.com/en/docs/advertising).<br><br>Pregunte por la administración de campañas, la optimización, la administración de audiencias, las ofertas, los informes y otras características del producto. | <ul><li>¿Cómo adjunto un anuncio a una ubicación?</li><li>¿Qué opciones de segmentación están disponibles en Adobe DSP?</li><li>¿Cuáles son las consecuencias de utilizar las diferentes opciones de ritmo en la configuración de ubicación?</li><li>¿Qué informes incluyen datos a nivel de hogar?</li><li>¿Cómo creo una etiqueta de anuncio para una experiencia de [!DNL Creative]?</li></ul> | La respuesta incluye citas en línea y una lista [!UICONTROL Documentation Sources] expansible en la parte inferior. Haga clic en cualquier cita o lista de fuentes para abrir la página correspondiente.<br><br>La respuesta también puede incluir preguntas de seguimiento y sugerencias para ayudarle a refinar la consulta y encontrar más información. |

## Abrir asistente de IA {#ai-assistant-open}

* En la parte superior derecha de cualquier página, haz clic en ![Chat agéntico](/help/dsp/assets/agent-chat.png "Chat agéntico").

## Expandir el cuadro de diálogo

1. En la parte superior de [chatbox](#ai-assistant-open), haz clic en ![Introducir pantalla completa](/help/dsp/assets/fullscreen.png "Introducir pantalla completa") para ingresar al modo de pantalla completa.

1. Para volver al modo de panel, haga clic en **[!UICONTROL < Back>]**.

<!-- 

No ability to narrow down list of child entities for a selected parent as of 10/26/26.

## Submit a query {#query-submit}

1. [Open AI Assistant](#ai-assistant-open).

1. Build the query:

   * To see examples of queries by topic and optionally copy one to use:
   
     1. Click **[!UICONTROL Learn]**, **[!UICONTROL Troubleshoot]**, or **[!UICONTROL Insights]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   * To enter your own query:
   
     1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.
     
        For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.
        
        Available dimensions include:
        
        * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
        * The advertiser: [!UICONTROL Advertiser]
        * Advertising Creative entities: [!UICONTROL Experience]
        * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

     1. Enter your query, and then click ![Submit query](/help/dsp/assets/submit.png "Submit query") or press the **Enter** key on your keyboard.
        
   You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

   >[!NOTE]
   >
   >* (Troubleshooting and insight queries) If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. If AI Assistant asks for additional information, provide it.

1. (Product documentation queries only; optional) To open a page used as a data source for the response, do either of the following:

   * Click the numbered citation.

   * Click **[!UICONTROL Documentation Sources]** to show a list of all pages cited in the response, and then click the page link.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask another query that you want to be saved as a separate thread, [start a new conversation](#conversation-new).

## (Insight queries) Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

 -->

<!--

## Work with previous conversations

### List previous conversations

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

To repeat the same topic verbatim, copy the key details into a new conversation. Otherwise, you can ask AI Assistant to repeat a finite task within a specific conversation.

### Rename a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

-->

## Prácticas recomendadas para escribir consultas e indicaciones {#writing-queries}

* **Sea claro y específico**. Utilice preguntas completas (&quot;¿Cómo puedo suscribirme al inventario a la carta?&quot;), frases de tareas (&quot;suscribirme al inventario a la carta&quot;) o frases de temas (&quot;Inventario a la carta&quot;).

* **No combine distintos tipos de solicitudes en la misma consulta** a menos que desee que se almacenen en la misma conversación.

* **Incluya intervalos de fechas cuando sea relevante** para reducir los datos que desee.

* **Igualar términos de la interfaz de usuario** siempre que sea posible para las características del producto (como &quot;campañas&quot; o &quot;ofertas&quot;).

  Para las acciones comunes (como &quot;agregar&quot;, &quot;adjuntar&quot; o &quot;asignar&quot;), puede utilizar sinónimos.

* **Agregar detalle** para reducir o ampliar los resultados. Refine con preguntas de seguimiento según sea necesario.

* **No te preocupes por la puntuación y el uso de mayúsculas** excepto cuando afectan al significado.

>[!MORELIKETHIS]
>
>* [Crear informes con el asistente de IA](insights-agent.md)
>* [Solucionar problemas de rendimiento y envío con el asistente de IA](troubleshooting-agent.md)
>* [Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md)
>* [Busque documentación del producto mediante el Asistente para IA](documentation-search.md)
>* [Trabajar con conversaciones anteriores del Asistente de IA](previous-conversations.md)
