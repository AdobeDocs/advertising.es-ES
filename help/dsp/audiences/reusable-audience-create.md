---
title: Crear una audiencia reutilizable
description: Obtenga información sobre cómo crear audiencias reutilizables para utilizarlas como destinos de ubicación o exclusiones. Cree audiencias reutilizables en Adobe Advertising DSP manualmente o con IA generativa en el asistente de IA o en la vista Todas las audiencias.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: 'https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: b4dc2b3d-fdb5-55cd-9190-f1076d8563e4
    internal-label: DSP Audiences
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: fc59d590863f0014c5d0466019f1d7f787b23744
workflow-type: tm+mt
source-wordcount: '2106'
ht-degree: 0%
---
# Crear una audiencia reutilizable

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Puede guardar y administrar audiencias reutilizables, que son grupos de segmentos de audiencia que puede utilizar como destinatarios o exclusiones para varias ubicaciones. Las audiencias reutilizables pueden incluir cualquier segmento de origen y de terceros disponible para usted, e incluso otras audiencias guardadas.

Cree audiencias con el agente de audiencia asistida por IA en la vista unificada de [AI Assistant](/help/dsp/ai-assistant/ai-assistant-about.md), en la vista de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o cree audiencias manualmente.

>[!NOTE]
>
>(Anunciantes para los que DSP convierte ID de correo electrónico con hash en segmentos de RampID de LiveRamp) Los segmentos de RampID de origen que no están adjuntos a una ubicación activa, programada o en pausa se pausan. El segmento se indica en la lista de segmentos como &quot;En pausa automática&quot;.

## Creación de una audiencia reutilizable mediante IA generativa con el asistente de IA

*característica de Beta*

*Sólo soporte en inglés*

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Esta función se encuentra en modo beta y está sujeta a cambios. Asegúrese de que la expresión de audiencia generada representa la audiencia que desea antes de guardar la audiencia y utilizarla en sus ubicaciones.

1. Abrir asistente de IA:

   * En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]>[!UICONTROL Create with AI]**.

   * En la parte superior derecha de cualquier página, haz clic en ![Chat agéntico](/help/dsp/assets/agent-chat.png "Chat agéntico").

1. Defina la audiencia:

   1. Cree una solicitud inicial para definir la audiencia de una de las siguientes maneras:

      * Introduzca su propio informe de audiencia o algunas de las características de audiencia que quiera incluir y excluir.

      * Para ver ejemplos de informes de audiencias de destino y, opcionalmente, copiar uno para utilizarlo:

        1. Haga clic en **[!UICONTROL Build]** para expandir la sección.

        1. (Opcional) Para copiar el texto de un resumen de audiencia de ejemplo en el cuadro de mensaje:

           1. Haga clic en el ejemplo.

           1. (Opcional) Edite el texto para adaptarlo a sus necesidades.

      Consulte &quot;[Conceptos básicos de escritura de mensajes](#writing-prompts)&quot; y &quot;[Prácticas recomendadas para crear un informe de audiencia](#audience-brief-best-practices)&quot;.

   1. Para enviar la solicitud, haga clic en ![Enviar solicitud](/help/dsp/assets/submit-prompt.png "Enviar solicitud").

      Puede hacer varias preguntas de una en una, pero solo una a la vez. Espere una respuesta antes de enviar otra solicitud.

      Se abre un panel en el lateral, con la definición de audiencia en la pestaña [!UICONTROL Step 1: Audience Definition]. La definición incluye todos los filtros de audiencia definidos, criterios de optimización y cualquiera de los segmentos de origen que se van a excluir.

      Cuando corresponde, el asistente de IA sugiere filtros de audiencia adicionales para ayudarle a crear una información de audiencia más eficaz. Puede aceptar o rechazar las sugerencias.

   1. (Opcional) Para excluir cualquiera de los segmentos de origen, pídale al Asistente de IA que lo haga o haga clic en ![Editar](/help/dsp/assets/edit-ai.png "Editar") en la sección **[!UICONTROL First-party segments to exclude]**, seleccione los segmentos que desee excluir para la audiencia y, a continuación, haga clic en **[!UICONTROL Apply]**.

   1. (Opcional) Envíe mensajes de solicitud adicionales según sea necesario para describir las características de audiencia que desea incluir y excluir. Para enviar cada solicitud, haga clic en ![Enviar solicitud](/help/dsp/assets/submit-prompt.png "Enviar solicitud").

1. Cuando la definición de la audiencia cumpla sus criterios, especifique los segmentos que desea incluir:

   1. Solicite al Asistente de IA que busque segmentos coincidentes. Puede decir &quot;ok&quot;, &quot;go&quot;, &quot;continue&quot;, &quot;search&quot; o cualquier término o frase relevante.

      La pestaña [!UICONTROL Step 2: Audience Segments] muestra el nombre de audiencia propuesto, el tamaño y la distribución de la audiencia, la expresión de audiencia booleana y una lista de los segmentos de audiencia incluidos agrupados por característica.

   1. (Opcional) En la sección [!UICONTROL Audience segments] de la parte inferior, realice una de las siguientes acciones:

      * Para expandir cada grupo de segmentos de audiencia, haga clic en **[!UICONTROL >]** junto al recuento.

      * Para copiar los ID de segmento de los segmentos de audiencia incluidos en el portapapeles, haga clic en **[!UICONTROL Copy rule]**.

      * Para quitar segmentos de la audiencia, pídale al Asistente de IA que lo haga o haga clic en ![Editar](/help/dsp/assets/edit-ai.png "Editar"), anule la selección de los segmentos que quiera quitar de la audiencia y haga clic en **[!UICONTROL Apply]**.

1. Cuando esté satisfecho con la audiencia ensamblada, haga clic en **[!UICONTROL Save Audience]** para crear la audiencia especificada.

   >[!NOTE]
   >
   >Para editar la audiencia más adelante, [edite la expresión de audiencia manualmente](/help/dsp/audiences/reusable-audience-edit.md).

## Cree una audiencia reutilizable con IA generativa desde la vista [!UICONTROL Audiences] > [!UICONTROL All audiences]

*característica de Beta*

*Sólo soporte en inglés*

>[!NOTE]
>
>Esta función se encuentra en modo beta y está sujeta a cambios. Asegúrese de que la expresión de audiencia generada representa la audiencia que desea antes de guardar la audiencia y utilizarla en sus ubicaciones.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

1. En la configuración de [!UICONTROL New Audience]:

   1. Escriba un(a) **[!UICONTROL Audience Name]** único.

   1. (Opcional) Anule la selección de la opción **[!UICONTROL Share with all advertisers in my account]**.

      Al compartir una audiencia, esta pasa a estar disponible como objetivo o exclusión para todos los anunciantes de la cuenta. Sin embargo, los segmentos individuales de la audiencia solo están disponibles para los usuarios con los que se comparten los segmentos. Por ejemplo, si comparte una audiencia que contiene segmentos de Adobe Analytics con un anunciante que no está asignado a la misma cuenta de [!DNL Analytics], el segmento no se previsualiza en esa audiencia para ese anunciante. En la audiencia solo se obtiene una vista previa de los segmentos disponibles para ese anunciante.

   1. Haga clic en **[!UICONTROL Save]**.

1. Cree la audiencia:

   1. Introduzca uno o más indicadores para describir las características de audiencia que desea incluir y excluir. Para enviar cada solicitud, haga clic en ![Enviar solicitud](/help/dsp/assets/submit-prompt.png "Enviar solicitud").

      Para obtener más información, consulte &quot;[Instrucciones de escritura](#writing-prompts)&quot; y &quot;[Prácticas recomendadas para crear un informe de audiencia](#audience-brief-best-practices)&quot;.

      Cuando corresponde, el agente sugiere filtros de segmento adicionales para ayudarle a crear una información de audiencia más eficaz. Puede aceptar o rechazar las sugerencias.

      A medida que el agente de audiencia encuentra segmentos relevantes, crea una expresión de audiencia booleana basada en los criterios. También le pedirá su aprobación antes de buscar segmentos coincidentes para montar la audiencia. Si lo desea, puede ignorar la solicitud y continuar especificando criterios de audiencia adicionales.

   1. Cuando el agente de audiencia presente una expresión de audiencia que describa adecuadamente su audiencia, dígale al agente de audiencia que continúe con la reunión de la audiencia.

      Puede escribir &quot;continuar&quot;, &quot;bien&quot;, &quot;bien&quot;, &quot;sí&quot; u otra palabra similar. El agente enumera todos los segmentos sugeridos para cada rasgo (como &quot;Padres&quot;). Para ver detalles sobre los segmentos individuales sugeridos para una característica, expanda la característica.

   1. (Si es necesario) Especifique otros criterios. Cuando el agente de audiencia presente una expresión de audiencia que cumpla todos sus criterios, dígale al agente de audiencia que continúe con la combinación de la audiencia.

      Para reunir la audiencia, escriba &quot;continuar&quot;, &quot;bien&quot;, &quot;bien&quot;, &quot;sí&quot; u otra palabra similar. El agente enumera todos los segmentos sugeridos para cada rasgo (como &quot;Padres&quot;). Para ver detalles sobre los segmentos individuales sugeridos para una característica, expanda cualquier característica.

1. Cuando esté satisfecho con la audiencia ensamblada, haga clic en **[!UICONTROL Create]** para crear la audiencia especificada.

   >[!NOTE]
   >
   >Para editar la audiencia más adelante, [edite la expresión de audiencia manualmente](/help/dsp/audiences/reusable-audience-edit.md).

## Crear manualmente una audiencia reutilizable

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]>[!UICONTROL Create manually]**.

1. En la configuración de [!UICONTROL New Audience]:

   1. Escriba un(a) **[!UICONTROL Audience Name]** único.

   1. (Opcional) Anule la selección de la opción **[!UICONTROL Share with all advertisers in my account]**.

      Al compartir una audiencia, esta pasa a estar disponible como objetivo o exclusión para todos los anunciantes de la cuenta. Sin embargo, los segmentos individuales de la audiencia solo están disponibles para los usuarios con los que se comparten los segmentos. Por ejemplo, si comparte una audiencia que contiene segmentos de Adobe Analytics con un anunciante que no está asignado a la misma cuenta de [!DNL Analytics], el segmento no se previsualiza en esa audiencia para ese anunciante. En la audiencia solo se obtiene una vista previa de los segmentos disponibles para ese anunciante.

   1. Haga clic en **[!UICONTROL Save]**.

1. Haga clic en el botón **[!UICONTROL Switch to manual mode]** en el panel derecho.

   La opción AI es la predeterminada.

1. Cree la audiencia:

   >[!NOTE]
   >
   >A medida que crea la audiencia, se actualizan [datos detallados del tamaño de la audiencia](audience-about.md) en el panel derecho

   * Para crear la lógica del segmento manualmente, mediante los segmentos disponibles en las fichas [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] y [!UICONTROL Saved Audiences]](audience-settings.md), haga lo siguiente.

     * (Opcional) Busque un nombre de segmento, una descripción o una ruta.

       Los resultados de la búsqueda incluyen segmentos basados en los términos exactos que utilice. Cuando introduce varios términos, se deben encontrar todos para un segmento.

     * Para añadir el primer segmento, localícelo en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento.

     * Para agregar un segmento a un grupo de segmentos existente:

       1. Haga clic en el grupo de segmentos en el panel derecho.

       1. (Opcional) Cambie la lógica de grupo a *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, según sea necesario.

          *[!UICONTROL Exclude All]* no está disponible para el primer grupo de segmentos. Para una audiencia que incluya solo exclusiones, genere esta audiencia como *[!UICONTROL Include Any]* y luego, dentro de una ubicación, seleccione esa audiencia en el menú Audiencias excluidas.

       1. Busque el nuevo segmento en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento.

          El grupo de segmentos se actualiza automáticamente con el nuevo segmento.

     * Para agregar un nuevo grupo de segmentos:

       1. Haga clic en **[!UICONTROL + New Group]** en el panel derecho.

          1. (Opcional) Cambie la lógica entre el grupo anterior y el nuevo a *[!UICONTROL And]* o *[!UICONTROL Or]*, según sea necesario.

          1. Busque los segmentos para el nuevo grupo en el panel izquierdo y seleccione las casillas de verificación situadas junto a los nombres de los segmentos.

          1. (Opcional) Cambie la lógica de grupo a *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, según sea necesario.

   * Para usar la lógica de segmento de una audiencia existente:

     1. Copie la lógica de segmento de la audiencia existente de cualquiera de las siguientes maneras:

        * En la vista Todas las audiencias, mantenga el cursor sobre la fila de audiencias y haga clic en **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

        * En la configuración de la audiencia existente, en la parte superior del panel de lógica de segmento, haga clic en **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

        * En un editor de texto, cree manualmente la lógica del segmento usando ID de segmento alfanuméricos y [sintaxis booleana](audience-segment-logic-syntax.md), y cópielo en el portapapeles.

     1. Haga clic en **[!UICONTROL paste in an audience rule to begin building]**, pegue la lógica de segmento existente en el campo de entrada y, a continuación, haga clic en **[!UICONTROL Apply]**.

        >[!NOTE]
        >
        >Si la audiencia ya incluye cualquier lógica de segmento, al pegar la nueva lógica de segmento se sobrescribe la lógica existente.

1. Haga clic en **[!UICONTROL Create]**.

### Conceptos básicos de escritura de indicadores {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### Directrices para escribir mensajes a la audiencia

* Utilice un lenguaje claro y descriptivo para describir la audiencia de destino.

  * Puede introducir frases completas o una cadena de características. La puntuación no es necesaria excepto cuando es necesario para una mayor claridad.

  * En general, los indicadores no distinguen entre mayúsculas y minúsculas.

  * El agente de audiencia reconoce los sinónimos más comunes.

* Sea específico y proporcione detalles sobre todas las características de audiencia que desee incluir y cualquier característica que desee excluir específicamente. Proporcionar más detalles aumenta la probabilidad de obtener resultados que satisfagan sus necesidades.

* Identifique ubicaciones, tipos de dispositivos y proveedores de datos para incluir o excluir.

* Proporcione iterativamente detalles para restringir los criterios y la expresión de audiencia generada antes de guardar la audiencia.

* Obtenga información sobre las sugerencias mediante la experimentación.

  Si el mensaje no está claro, el agente de audiencia solicita otro mensaje para que pueda intentarlo de nuevo.

  El agente de audiencia no guardará automáticamente una expresión de audiencia generada como audiencia. Solo puede guardar una audiencia si hace clic en el botón [!UICONTROL Create], que se encuentra fuera del área de solicitud, para poder deshacer los cambios que no desee conservar.

Consulte &quot;[Prácticas recomendadas para crear un informe de audiencia](#audience-brief-best-practices)&quot; para ver más formas de optimizar las peticiones de datos para audiencias.

<!--
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### ¿Qué no se puede incluir en un mensaje?

* Referencias a expresiones de audiencia existentes.

* Texto en otros idiomas además del inglés.

#### Ejemplos de respuestas del agente de audiencia y cómo responder

Cuando el agente de audiencia necesite una respuesta de su parte, puede responder utilizando palabras clave en la solicitud o utilizando sinónimos comunes.

#### El agente de audiencia le hace una pregunta

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Su respuesta afirmativa: &quot;proceder&quot;, &quot;bien&quot;, &quot;bien&quot;, &quot;sí&quot; u otra palabra similar

También puede ignorar la solicitud y seguir especificando criterios de audiencia adicionales en su lugar.

##### El agente de audiencia le pide que elija entre varias opciones

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Su respuesta: `1`, `proceed`, `2`, `maximum reach`, etc.

También puede ignorar la solicitud y seguir especificando criterios de audiencia adicionales en su lugar.

### Prácticas recomendadas para crear un informe de audiencia {#audience-brief-best-practices}

Un informe de audiencia es una escritura estratégica que define el público objetivo de una campaña. Una información bien diseñada ayuda al agente de audiencia de DSP a identificar los segmentos más relevantes para montar la audiencia de destino.

#### Componentes esenciales de una información de audiencia efectiva

Incluya tantos tipos de atributos de audiencia como sea posible de la siguiente lista en su informe. Sea específico sobre los atributos que desea excluir.

<!--
 What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Datos demográficos**

  Incluye atributos como el intervalo de edad, la identidad de género, el estado civil, la composición del hogar (tamaño de la familia, presencia de niños, hogares multigeneracionales).

* **Indicadores socioeconómicos**

  Establece la capacidad financiera a través de las bandas de ingresos del hogar (HHI), el nivel de educación, la ocupación / títulos de trabajo, el estado laboral y el estado de propiedad de la vivienda.

* **Parámetros geográficos**

  Define el ámbito de ubicación, incluidos país/países, región (EMEA, APAC, NA) y densidad de población (urbana/suburbana/rural).

* **Intereses y afinidades**

  Identifica pasiones y preferencias como aficiones (deportes, artes, actividades al aire libre), patrones de consumo de medios, afinidades de marca y actividades de estilo de vida (viajes, restaurantes, entretenimiento).

* **Psicografía**

  Captura la mentalidad y los valores, incluidas las aspiraciones (búsqueda de estatus, autosuperación), los valores fundamentales (sostenibilidad, innovación, tradición), los rasgos de personalidad (personas que toman riesgos, quienes los adoptan tempranamente) y las motivaciones de compra.

* **Señales de comportamiento**

  Acciones observables, incluido el comportamiento de compra (frecuencia de compra, preferencias de canal, lealtad de marca), comportamiento en línea (visitas al sitio web, participación en el contenido, actividad en los medios sociales) y comportamiento sin conexión (visitas al almacén, asistencia al evento, suscripciones).

* **Intención en el mercado**

  Identifica la preparación para la compra a través de las categorías de producto/servicio que se investigan, el cronograma de compra (inmediato, a corto plazo, a largo plazo) y los eventos de vida relevantes que activan las decisiones de compra.

* **Fase de vida**

  Comprensión de la fase actual, que incluye la etapa profesional (estudiante, nivel de ingreso, mitad de la carrera, ejecutivo, jubilado), etapa familiar (recién casados, nuevos padres, nidos vacíos) y transiciones importantes en la vida.

#### Ejemplo de un informe de audiencia bien estructurado para una campaña de prospección

El siguiente es un ejemplo de un informe de audiencia sólido para una campaña de concienciación y prueba para un servicio de suscripción a un kit de comida premium:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Acerca de la administración de audiencias](audience-about.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Sintaxis de la lógica de segmento de audiencia](audience-segment-logic-syntax.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Crear e implementar un segmento personalizado](custom-segment-create.md)
>* [Crear e implementar un segmento [!UICONTROL CCPA Opt-Out-of-Sale]](ccpa-opt-out-segment-create.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
