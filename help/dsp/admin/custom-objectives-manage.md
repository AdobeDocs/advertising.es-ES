---
title: Administrar objetivos personalizados
description: Aprenda a definir los eventos de éxito que le ayudarán a alcanzar los objetivos de optimización de nivel de paquete.
role: User, Admin
feature: DSP Optimization, DSP Packages
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 0%

---

# Administrar objetivos personalizados

*Disponible para cuentas de DSP vinculadas a las cuentas de Search, Social y Commerce*

Los objetivos definen los eventos de éxito que establece un anunciante para alcanzar sus objetivos comerciales. Los objetivos están disponibles para paquetes de DSP como [metas personalizadas](/help/dsp/campaign-management/packages/package-settings.md). Cada paquete que usa el objetivo de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; debe incluir un objetivo personalizado para ayudar a lograr el objetivo de optimización general.

Un objetivo consiste en las métricas (propiedades) que se van a rastrear y optimizar, y los pesos relativos de esas métricas. Cada objetivo puede incluir:

* **[!UICONTROL Goal]métricas**, que representan las métricas de éxito principales de un anunciante. Por lo general, incluyen resultados empresariales principales para un paquete, como ingresos, posibles clientes o ventas. Cada objetivo debe tener al menos una métrica de objetivo.

* Métricas **[!UICONTROL Assist]opcionales** que ayudan, predicen, preceden o contribuyen a impulsar las métricas de objetivo. Algunos ejemplos son las métricas de participación, como Unidades de prueba y Pruebas.

  Puede permitir que [!DNL Adobe AI] asigne y actualice automáticamente eventos de asistencia ponderados para maximizar los eventos de objetivos. Si prefiere asignar sus propias métricas de asistencia ponderada, DSP puede recomendar opcionalmente métricas de asistencia basadas en datos de rendimiento anteriores de Adobe Advertising y Adobe Analytics. Puede elegir si desea aplicar o no las recomendaciones.

Todos los cambios realizados en las opciones de objetivos se rastrean en el nivel de campo y se enumeran en un registro de cambios.

>[!PREREQUISITES]
>
>Para poder crear objetivos, la cuenta de DSP debe estar vinculada a una cuenta de Search, Social y Commerce con el mismo ID de organización de Adobe Experience Cloud, aunque no sea cliente de Search, Social y Commerce. Si su cuenta de DSP no está vinculada a una cuenta de [!DNL Search, Social, & Commerce], póngase en contacto con el equipo de cuenta de Adobe.

>[!NOTE]
>
>* Advertising Search, Social y Commerce también usan objetivos. Cada portafolio de Search, Social y Commerce debe tener un objetivo para que la capacidad de optimización pueda crear modelos de clics e ingresos para el portafolio.
>* Puede utilizar el mismo objetivo para varios paquetes de DSP o varios portafolios de Search, Social y Commerce.

## Métricas disponibles

Puede incluir cualquiera de los siguientes elementos en sus objetivos:

* Métricas que Adobe Advertising rastrea usando el [píxel de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* (Anunciantes con [!DNL Adobe Analytics for Advertising]) [Métricas de conversión y participación del sitio sincronizadas desde Adobe Analytics](/help/integrations/analytics/overview.md).

<!-- Do DSP-only clients have these? * [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).  -->

## Estado de objetivo

La vista [!UICONTROL Settings] > [!UICONTROL Custom Objectives] indica el estado de cada objetivo. Los valores pueden incluir:

* *[!UICONTROL Waiting]*: el objetivo está en estado de borrador hasta que se generen recomendaciones.

* *[!UICONTROL Active]*: el objetivo se ha guardado y se puede utilizar.

## Estado de recomendación

* *[!UICONTROL Not Initiated]*: no se solicitó ninguna recomendación.

* *[!UICONTROL Generating]*: se están generando recomendaciones.

* *[!UICONTROL Ready]*: las recomendaciones están disponibles para su aplicación.

* *[!UICONTROL Error]*: no se pudieron generar las recomendaciones.

## Creación de un objetivo

1. En el menú principal, haga clic en **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]**.

1. Escriba la [configuración del objetivo](#custom-objective-settings).

   Al elegir la oferta automatizada, puede asignar propiedades (métricas) al objetivo como métricas &quot;[!UICONTROL Goal]&quot;. Para las ofertas personalizadas, puede asignar propiedades como &quot;[!UICONTROL Goal]&quot; o como &quot;[!UICONTROL Assist]&quot; métricas ponderadas, pero debe incluir al menos una métrica de objetivo.

   Las etiquetas de objetivo y asistencia no afectan a la optimización. Solo los pesos de las métricas incluidas afectan a la optimización.

1. (Objetivos con oferta personalizada; opcional) Para generar las métricas de asistencia recomendadas basadas en datos de rendimiento anteriores, haga clic en **[!UICONTROL Generate]** en la sección inferior. En **[!UICONTROL Generate Recommendation]**, haga clic en **[!UICONTROL Generate]**.

   Las métricas recomendadas tardan hasta 20 minutos en generarse. Mientras se generan las recomendaciones, el estado del objetivo personalizado es *[!UICONTROL Waiting]*. Una vez generadas las recomendaciones, puede &quot;[ver y aplicar los eventos de asistencia recomendados](#view-apply-recommendations)&quot;.

1. (Si no ha generado recomendaciones) En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

En la [configuración del paquete de DSP](/help/dsp/campaign-management/packages/package-settings.md) para los paquetes que usan los objetivos de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;, el nombre del objetivo ahora se incluye en la lista [!UICONTROL Custom Goals]. Al seleccionar el objetivo como objetivo personalizado para un paquete, la lista [!UICONTROL Conversion Metric] incluye todas las métricas de objetivo del objetivo.

## Editar un objetivo

1. En el menú principal, haga clic en **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. En la fila, haga clic en **...*** > **[!UICONTROL Edit]**.

1. Cambie cualquiera de [los ajustes del objetivo](#custom-objective-settings).

1. (Cuando las recomendaciones están disponibles; opcional) Ver y, opcionalmente, aplicar las métricas recomendadas:

   1. En la sección inferior, haga clic en **[!UICONTROL View Recommendations]**.

   1. Para aplicar una recomendación, realice una de las acciones siguientes:

      * Haga clic en **[!UICONTROL Apply]** junto a la recomendación.

      * Ajuste manualmente la recomendación y haga clic en **[!UICONTROL Apply]** junto a la recomendación.

   1. Haga clic en **[!UICONTROL Close]** para cerrar la lista [!UICONTROL Recommendations].

   Los cambios se aplican después de sincronizar la configuración del objetivo.

1. (Objetivos con oferta personalizada; opcional) Para generar métricas de asistencia recomendadas basadas en datos de rendimiento anteriores, haga clic en **[!UICONTROL Generate]** en la sección inferior. En **[!UICONTROL Generate Recommendation]**, haga clic en **[!UICONTROL Generate]**.

   Las métricas recomendadas tardan hasta 20 minutos en generarse. Mientras se generan las recomendaciones, el estado del objetivo personalizado es *[!UICONTROL Waiting]*. Una vez generadas las recomendaciones, puede &quot;[ver y aplicar los eventos de asistencia recomendados](#view-apply-recommendations)&quot;.

1. (Si no ha generado nuevas recomendaciones) En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

## Ver y aplicar eventos de ayuda recomendados {#view-apply-recommendations}

*Objetivos con oferta personalizada*

Puede ver recomendaciones y, opcionalmente, aplicarlas cuando el estado del objetivo sea *[!UICONTROL Active]* y el [!UICONTROL Recommendation Status] sea *[!UICONTROL Ready]*.

1. En el menú principal, haga clic en **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. En la fila, haga clic en **...*** > **[!UICONTROL Edit]**.

1. En la sección inferior, haga clic en **[!UICONTROL View Recommendations]**.

1. (Opcional) Para aplicar una recomendación, realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL Apply]** junto a la recomendación.

   * Ajuste manualmente la recomendación y haga clic en **[!UICONTROL Apply]** junto a la recomendación.

1. Haga clic en **[!UICONTROL Close]** para cerrar la lista [!UICONTROL Recommendations].

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

   Los cambios se aplican después de sincronizar la configuración del objetivo.

## Ver el registro de cambios de un objetivo personalizado

1. En el menú principal, haga clic en **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. En la fila, haga clic en **...*** > **[!UICONTROL Change Log]**.

<!--

Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## Configuración de objetivos personalizada {#custom-objective-settings}

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| Sección | Parámetro | Descripción |
|---------|-----------|-------------|
| Detalles básicos | AMOClient | El ID único de Adobe Advertising del anunciante. |
| Detalles básicos | Nombre de objetivo | El nombre del objetivo.<br><br>Todos los nombres de objetivos de Advertising DSP deben ir precedidos del nombre por &quot;ADSP_&quot; (no distingue mayúsculas de minúsculas), como &quot;ADSP_Registrations&quot;. Utilice un nombre fácil de identificar cuando desee asignarlo a un paquete. |
|  | Descripción | (Opcional) Una descripción del objetivo. La descripción aparece cuando mantiene el cursor sobre el nombre en la lista Objetivos personalizados. Si no se incluye una descripción, en su lugar se repite el nombre del objetivo. |
| Estrategia de oferta |  | La estrategia de oferta del objetivo, que determina los tipos de eventos que se pueden configurar:<ul><li><b>[!UICONTROL Automated Bidding]:</b> Asignar propiedades (métricas) al objetivo como [!DNL goal] métricas. [!DNL Adobe AI] asigna y actualiza automáticamente los eventos de asistencia ponderados para maximizar los eventos de objetivos mediante un enfoque de funnel equilibrado.</li><li><b>[!UICONTROL Custom Bidding]:</b> Configure su propia estrategia de oferta asignando propiedades como &quot;[!DNL goal]&quot; o eventos &quot;[!DNL assist]&quot; ponderados. Utilice esta opción avanzada para estrategias predefinidas.</li></ul>Al cambiar la estrategia de oferta, se borran todas las métricas seleccionadas anteriormente. |
| Propiedades | [!UICONTROL Available Metrics] | Todas las métricas rastreadas para el anunciante. Para agregar una métrica como objetivo, haga clic en <b>[!UICONTROL Goal]</b> junto al nombre de la métrica. ([!UICONTROL Custom Bidding] solamente) Para agregar una métrica que ayude a las métricas de objetivo asignadas, haga clic en <b>[!UICONTROL Assist]</b> junto al nombre de la métrica.<br><br><b>Notas:</b> [!DNL Analytics] eventos personalizados siguen esta convención de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Ejemplo: `custom_event_16_examplersid.` [!DNL Analytics] dimensiones y segmentos no están disponibles para la optimización de Adobe Advertising.<br><br><b>Sugerencia:</b> Para obtener un rendimiento óptimo, las métricas combinadas en el objetivo personalizado (objetivo) deben sumar al menos diez conversiones al día. Si no es así, se recomienda añadir al objetivo métricas de conversión compatibles adicionales, como páginas de productos o inicios de aplicaciones. Vea [Prácticas recomendadas para crear un objetivo personalizado](#custom-goal-best-practices) para obtener instrucciones. |
|  | Métricas seleccionadas | El nombre de cada métrica de conversión incluida en el objetivo. Realice una de las siguientes acciones:<ul><li>Para agregar una métrica como objetivo, haga clic en <b>[!UICONTROL Goal]</b> junto al nombre de la métrica en la columna [!UICONTROL Available Metrics].</li><li>([!UICONTROL Custom Bidding] solo estrategia) Para agregar una métrica que ayude a las métricas de objetivo asignadas, haga clic en <b>[!UICONTROL Assist]</b> junto al nombre de la métrica en la columna [!UICONTROL Available Metrics]. A continuación, introduzca el peso numérico de la métrica en relación con otras métricas del objetivo. La ponderación debe estar entre 0,001 y 1 y puede incluir decimales. El peso predeterminado es 1.</li><li>([!UICONTROL Custom Bidding] solo estrategia) Para editar el peso de una métrica de asistencia, haga clic dentro del campo e introduzca el peso numérico de la métrica en relación con otras métricas del objetivo. El peso debe ser mayor que cero (0) y puede incluir decimales. El peso predeterminado es 1.</li><li>Para quitar una métrica del objetivo, mantenga el cursor sobre el nombre de la métrica y haga clic en **[!UICONTROL X]**./li></ul>**Notas:**<ul><li>Asegúrese de que las distintas métricas y sus pesos tengan sentido relativamente. Por ejemplo, no se puede comparar directamente un recuento con una cantidad en dólares.</li><li>Los grandes cambios relativos entre las ponderaciones del objetivo pueden causar volatilidad temporal en el rendimiento, por lo que debe monitorizarse el rendimiento después del cambio.</li></ul>. |

>[!MORELIKETHIS]
>
>* [Objetivos de optimización y cómo usarlos](/help/dsp/optimization/optimization-goals.md)
>* [Prácticas recomendadas para las metas personalizadas](/help/dsp/optimization/custom-goal.md)
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
>* [Administrar conversiones](/help/dsp/admin/conversion-metrics-manage.md)
