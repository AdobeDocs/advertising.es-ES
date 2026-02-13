---
title: Creación de una audiencia reutilizable mediante IA generativa
description: Aprenda a crear audiencias reutilizables en Adobe Advertising DSP mediante el agente de audiencia asistida por IA. Describa la audiencia de destino en mensajes en lenguaje natural; el agente sugiere segmentos de terceros y crea expresiones de audiencia para utilizarlas como objetivos o exclusiones.
feature: DSP Audiences
hidefromtoc: true
hide: true
source-git-commit: c632774e68069ab03f41fb9453a27c6fe63c8168
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 0%

---

# Creación de una audiencia reutilizable mediante IA generativa

*característica de Beta*

*Indicadores solo en inglés*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Utilice el agente de audiencia asistida por IA para generar nuevas audiencias reutilizables utilizando todos los segmentos de terceros disponibles para usted, según sus requisitos declarados. Puede usar las audiencias como destinatarios o exclusiones para varias ubicaciones.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Esta función se encuentra en modo beta y está sujeta a cambios. Asegúrese de que la expresión de audiencia generada representa la audiencia que desea antes de crear la audiencia y utilizarla para sus ubicaciones.

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

1. Escriba un(a) **[!UICONTROL Audience Name]** único.

1. (Opcional) Anule la selección de la opción **[!UICONTROL Share with all advertisers in my account]**.

   Al compartir una audiencia, esta pasa a estar disponible como objetivo o exclusión para todos los anunciantes de la cuenta. Sin embargo, los segmentos individuales de la audiencia solo están disponibles para los usuarios con los que se comparten los segmentos.

1. Haga clic en **[!UICONTROL Save]**.

1. Cree la audiencia:

   Para los usuarios con permisos de versión beta, la opción AI es la predeterminada. Para [montar la audiencia usted mismo](/help/dsp/audiences/reusable-audience-create.md), haga clic en el botón &quot;Cambiar a modo manual&quot; en la parte inferior.

   1. Introduzca uno o más indicadores para describir las características de audiencia que desea incluir y excluir. Para enviar cada solicitud, haga clic en ![Enviar solicitud](/help/dsp/assets/submit-prompt.png "Enviar solicitud").

      Para obtener más información, consulte &quot;[Escribir indicadores](#writing-prompts)&quot; y &quot;[Prácticas recomendadas para crear un resumen de audiencia](#audience-brief-best-practices)&quot;.

      A medida que el agente de IA encuentra segmentos relevantes, crea una expresión de audiencia basada en los criterios. También le pedirá su aprobación antes de buscar segmentos coincidentes para montar la audiencia.

      Si lo desea, puede ignorar la solicitud y continuar especificando criterios de audiencia adicionales.

   1. Cuando el agente de IA presente una expresión de audiencia que describa adecuadamente su audiencia, dígale al agente de IA que proceda a ensamblar la audiencia.

      Puede escribir &quot;continuar&quot;, &quot;bien&quot;, &quot;bien&quot;, &quot;sí&quot; u otra palabra similar.

1. (Si es necesario) Especifique otros criterios. Cuando el agente de IA presente una expresión de audiencia que cumpla todos los criterios, dígale al agente de IA que continúe con la agrupación de la audiencia.

1. Cuando esté satisfecho con la audiencia ensamblada, haga clic en **[!UICONTROL Create]** para crear la audiencia especificada.

   >[!NOTE]
   >
   >Posteriormente, no se puede editar la audiencia con el agente de IA. En su lugar, [edite la expresión de audiencia manualmente](/help/dsp/audiences/reusable-audience-edit.md).

## Escritura de indicadores {#writing-prompts}

### ¿Qué debe incluir un mensaje?

* Utilice un lenguaje claro y descriptivo para describir la audiencia de destino.

* Sea específico y proporcione detalles sobre todas las características de audiencia que desee incluir y cualquier característica que desee excluir específicamente. Cuantos más detalles proporcione, mayores serán las posibilidades de obtener los resultados que satisfagan sus necesidades.

* Identifique ubicaciones, tipos de dispositivos y proveedores de datos para incluir o excluir.

* Proporcione iterativamente detalles para restringir los criterios y la expresión de audiencia generada antes de guardar la audiencia.

* Obtenga información sobre las sugerencias mediante la experimentación.

  El agente de audiencia no guardará automáticamente una expresión de audiencia generada como audiencia. Solo puede guardar una audiencia si hace clic en el botón [!UICONTROL Create], que se encuentra fuera del área de solicitud, para poder deshacer los cambios que no desee conservar.

Consulte &quot;[Prácticas recomendadas para crear un resumen de audiencia](#audience-brief-best-practices)&quot; para obtener más información sobre cómo optimizar las peticiones de datos para las audiencias.

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### ¿Qué no se puede incluir en un mensaje?

* Referencias a expresiones de audiencia existentes.

* Texto en otros idiomas además del inglés.

### Ejemplos de respuestas del agente de IA y cómo responder

Cuando el agente de IA necesite una respuesta de su parte, puede responder utilizando palabras clave en la solicitud o utilizando términos comunes que sean equivalentes.

#### Respuesta del agente de IA que le hace una pregunta

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Su respuesta afirmativa: &quot;continuar&quot;, &quot;bien&quot;, &quot;bien&quot;, &quot;sí&quot; u otra palabra similar

También puede ignorar la solicitud y seguir especificando criterios de audiencia adicionales en su lugar.

#### Respuesta del agente de IA que le pide que elija entre varias opciones

```
Would you like to:
1) Proceed with this expression,
2) Get maximum reach alternatives, or
3) Modify the expression manually?
```

Su respuesta: `1`, `proceed`, `2`, `maximum reach`, etc.

También puede ignorar la solicitud y seguir especificando criterios de audiencia adicionales en su lugar.

## Prácticas recomendadas para crear un resumen de audiencia {#audience-brief-best-practices}

Un informe de audiencia es una escritura estratégica que define el público objetivo de una campaña. Una información bien diseñada ayuda al agente de audiencia de DSP a identificar los segmentos más relevantes para montar la audiencia de destino.

### Componentes esenciales de un resumen de audiencia eficaz

#### Atributos de audiencia

Incluya tantos tipos de atributos como sea posible de la siguiente lista en su informe. Sea específico sobre los atributos que desea excluir.

<!-- What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Datos demográficos**

  Incluye atributos como el intervalo de edad, el sexo, el estado civil, la composición del hogar (tamaño de la familia, presencia de niños, hogares multigeneracionales).

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

### Ejemplo de un resumen de audiencia bien estructurado para una campaña de prospección

El siguiente es un ejemplo de un informe de audiencia sólido para una campaña de concienciación y prueba para un servicio de suscripción a un kit de comida premium:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Duplicar una audiencia reutilizable](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [Editar una audiencia reutilizable](/help/dsp/audiences/reusable-audience-edit.md)
>* [Ver detalles acerca de una audiencia reutilizable](/help/dsp/audiences/reusable-audience-view-details.md)
>* [Compartir una audiencia reutilizable](/help/dsp/audiences/reusable-audience-share.md)
>* [Exportar una audiencia reutilizable](/help/dsp/audiences/reusable-audience-export.md)
>* [Copiar la clave del segmento para una audiencia reutilizable en el portapapeles](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [Eliminar una audiencia reutilizable](/help/dsp/audiences/reusable-audience-delete.md)
