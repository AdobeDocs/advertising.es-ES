---
title: Creación de informes con el asistente de IA
description: Aprenda a utilizar el agente de perspectivas del asistente de inteligencia artificial aplicada a Adobe Advertising DSP para consultar las métricas de campaña, generar informes y descargar archivos CSV.
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
source-wordcount: '594'
ht-degree: 0%
---
# Creación de informes con el Asistente de IA

*característica de Beta*

*Sólo soporte en inglés*

Utilice el agente de perspectivas del asistente de IA para obtener métricas e informes completos para sus campañas, componentes de campaña, experiencias de Advertising Creative, anunciantes y objetivos de publicidad, sin necesidad de crear manualmente un informe. Puede hacer preguntas sencillas sobre una métrica específica, como gasto o CPA para una campaña, o solicitar un informe más complejo para una dimensión específica (como una sola campaña o audiencia) o entre dimensiones (para desgloses de cada campaña y anunciante). Puede descargar los resultados como archivo CSV.

>[!IMPORTANT]
>
>Las respuestas generadas por IA pueden ser inexactas o engañosas. Compruebe siempre las respuestas y las fuentes antes de utilizarlas para tomar decisiones que afecten a los costes o al esfuerzo.

## Consultas de ejemplo

* ¿Cuánto gastó [Campaign Name] la semana pasada?

* ¿Cuántas conversiones obtuvo [Campaign Name] este mes?

* Mostrarme el CPA por paquete para [Nombre de campaña].

* ¿Qué ubicaciones están detrás del ritmo en más del 20 %?

* Compare el gasto neto de todas las campañas y paquetes en los últimos 15 días.

## Envío de una consulta

Puede hacer varias preguntas en un mensaje, pero solo un mensaje a la vez. Espere una respuesta antes de enviar otra.

1. En la parte superior derecha de cualquier página, haz clic en ![Chat agéntico](/help/dsp/assets/agent-chat.png "Chat agéntico").

1. Cree la consulta:

   1. Realice una de las acciones siguientes:

      * Introduzca su propia consulta.

      * Para ver ejemplos de consultas:

        1. Haga clic en **[!UICONTROL Insights]** para expandir la sección.

        1. (Opcional) Para copiar el texto de una consulta de ejemplo en el campo de entrada:

           1. Haga clic en el ejemplo.

           1. (Opcional) Edite el texto para adaptarlo a sus necesidades.

   1. (Opcional) Para enfocar la consulta en un valor de dimensión específico (como una campaña específica), si lo desea, inserte el cursor donde desee que aparezca el valor de dimensión, haga clic en ![Mencione una entidad](/help/dsp/assets/prompt-entity.png "Mencione una entidad"), seleccione la dimensión y, a continuación, seleccione el valor de dimensión.

      Por ejemplo, para la dimensión [!UICONTROL Campaign], puede seleccionar de una lista de todas sus campañas para informar.

      Las dimensiones disponibles incluyen:

      * Entidades de campaña: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
      * El anunciante: [!UICONTROL Advertiser]
      * Entidades Advertising Creative: [!UICONTROL Experience]
      * Destinos del anuncio: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

   Para obtener más información acerca de las consultas, vea &quot;[Prácticas recomendadas para escribir consultas y avisos](ai-assistant-about.md#writing-queries)&quot;.

1. Haga clic en ![Enviar consulta](/help/dsp/assets/submit-prompt.png "Enviar consulta") o presione la tecla **Intro** del teclado. Si el agente solicita información adicional, proporcione la información requerida.

   Se muestran las primeras filas del informe, con vínculos para obtener una vista previa del informe completo y descargar el informe.

   Se muestran algunas filas del informe generado.

>[!TIP]
>
>Para preguntar sobre un problema diferente, o sobre un paquete o ubicación diferente, [inicia una nueva conversación](#conversation-new).

## Descargue o previsualice un informe completo desde el chat

* Para descargar una copia del informe completo, haz clic en ![Exportar](/help/dsp/assets/download.png "Exportar").

  El archivo se descarga como un archivo de valores separados por comas (.csv) de [!DNL Microsoft Excel] de acuerdo con el procedimiento normal del explorador. El nombre de archivo es &quot;DSP_Insights_Report_&lt;job_number>&quot;.

* Para obtener una vista previa del informe completo en un panel lateral, haga clic en ![Vista previa](/help/dsp/assets/agent-chat-preview.png "Vista previa"). Para descargar el informe desde la vista previa, haga clic en ![Exportar](/help/dsp/assets/download.png "Exportar").

  Si descarga el informe, se descargará como un archivo de valores separados por comas (.csv) de [!DNL Microsoft Excel] de acuerdo con el procedimiento normal del explorador. El nombre de archivo es &quot;DSP_Insights_Report_&lt;job_number>&quot;.

## Iniciar una nueva conversación {#conversation-new}

Cada conversación, o hilo de consulta, se guarda por separado para que pueda distinguir entre sus conversaciones anteriores.

1. En la parte superior de [chat](#ai-assistant-open), haz clic en ![Iniciar una nueva conversación](/help/dsp/assets/new-selection.png "Iniciar una nueva conversación").

1. [Enviar una consulta](#query-submit).

## Expandir y minimizar el cuadro de diálogo

1. En la parte superior de [chatbox](#ai-assistant-open), haz clic en ![Introducir pantalla completa](/help/dsp/assets/fullscreen.png "Introducir pantalla completa") para ingresar al modo de pantalla completa.

1. Para volver al modo de panel, haga clic en **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [Acerca del Asistente de IA en Advertising DSP](ai-assistant-about.md)
>* [Trabajar con conversaciones anteriores del Asistente de IA](previous-conversations.md)
