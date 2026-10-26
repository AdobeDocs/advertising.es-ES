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
source-git-commit: ffe7424d4e225a95b279b06a7df3b85bf0cbcdbf
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%
---
# Acerca del asistente de IA en Advertising DSP

El asistente de IA de DSP es una interfaz conversacional que le permite realizar cualquier flujo de trabajo auténtico disponible en DSP desde una sola bandeja de chat. Puede crear una tarea nueva o pedir ayuda para continuar una tarea anterior.

El historial de conversaciones se mantiene para todos los flujos de trabajo, y cada conversación se nombra automáticamente. Las consultas no se comparten con otros usuarios.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Flujos de trabajo admitidos

Los siguientes flujos de trabajo pueden ayudarle a realizar su trabajo de forma más eficaz:

<!-- And links to all sections/pages -->

| Función | Descripción | Respuestas |
| --- | --- | --- |
| [Solución de problemas](troubleshooting-agent.md) | (Función de Beta) Diagnosticar problemas de rendimiento y entrega de un paquete o una ubicación en directo seleccionados.<ul><li>Solo ubicaciones: Diagnosticar el exceso de gasto, la infrautilización y el fallo en el gasto. El agente evalúa los factores de ritmo, oferta, objetivo y límite presupuestario relacionados.</li><li>Solo paquetes: diagnostique problemas de rendimiento, incluido un CPA en aumento o un ROAS en caída. El agente no diagnostica métricas de participación como CTR, CPC, clics o impresiones.</li></ul>Cada conversación cubre un diagnóstico para un paquete o ubicación. Después de recibir un resultado, inicie una nueva conversación para diagnosticar otro problema, paquete o ubicación.<br><br>El agente no puede cambiar la configuración ni crear o editar campañas o componentes de campañas. Tampoco puede diagnosticar paquetes o ubicaciones en pausa, completados, archivados o programados. | La respuesta incluye factores que limitan el rendimiento y proporciona recomendaciones para resolver los problemas. |
| [Datos](insights-agent.md) | (Función de Beta) Obtenga métricas de campaña e informes completos sin crear manualmente un informe. Puede hacer preguntas sencillas sobre una métrica específica, como gasto o CPA para una campaña, o solicitar un informe más complejo para una dimensión específica (como una campaña, ubicación o audiencia únicas) o entre dimensiones (para desgloses por campaña y anunciante). Puede descargar los resultados como archivo CSV. | Se muestran las primeras filas del informe, con vínculos para obtener una vista previa del informe completo y descargar el informe como un archivo de valores separados por comas (.csv) de [!DNL Microsoft Excel]. |
| [Búsqueda de documentación del producto](documentation-search.md) | Busque contenido conceptual y explicativo en la [Guía de Advertising DSP](/help/dsp/home.md) y, para anunciantes con Advertising Creative, en la [Guía de Advertising Creative](/help/creative/home.md). Las respuestas se basan únicamente en lo que se ha documentado para estos productos en [Experience League](https://experienceleague.adobe.com/es/docs/advertising).<br><br>Pregunte por la administración de campañas, la optimización, la administración de audiencias, las ofertas, los informes y otras características del producto. | La respuesta incluye citas en línea y una lista [!UICONTROL Documentation Sources] expansible en la parte inferior. Haga clic en cualquier cita o lista de fuentes para abrir la página correspondiente.<br><br>La respuesta también puede incluir preguntas de seguimiento y sugerencias para ayudarle a refinar la consulta y encontrar más información. |

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
