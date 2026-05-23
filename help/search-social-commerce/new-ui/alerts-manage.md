---
title: (Nueva IU) Administrar alertas personalizadas
description: Obtenga información sobre cómo crear, configurar, pausar, activar, eliminar, ver y exportar alertas personalizadas y plantillas de alertas.
feature: Search Alerts
source-git-commit: 0fddeb8f01bd7c310544973ae2aff78339eb2144
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# (Nueva IU) Administrar alertas personalizadas

Cree plantillas de alerta para identificar cuándo cualquier portafolio, campaña o grupo de publicidad cumple condiciones específicas, como una métrica de rendimiento, durante un período especificado y luego genere una alerta. Las alertas están disponibles para un solo anunciante. Las alertas incluyen todas las columnas en la vista predeterminada relevante. Por ejemplo, las alertas de nivel de campaña incluyen todas las columnas en la vista predeterminada [!UICONTROL Campaigns].

Puede crear plantillas de alerta desde la ficha [!UICONTROL Alert Templates] del panel [!UICONTROL Custom Alerts] o desde la parte superior de cualquier página.

Cuando se activa una instancia de alerta para una plantilla de alerta:

* Los destinatarios especificados reciben un aviso por correo electrónico. Cuando la alerta contiene hasta 1000 registros, el aviso por correo electrónico incluye un archivo [CSV](/help/search-social-commerce/glossary.md#c-d) con los datos de alerta, incluidos los datos de todas las entidades que activaron la alerta.

* La alerta aparece en la ficha [!UICONTROL Triggered Alerts] del panel [!UICONTROL Custom Alert Templates].<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## La vista [!UICONTROL Custom Alerts]

Para abrir el panel [!UICONTROL Custom Alerts], haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada") en la parte superior derecha.

El panel [!UICONTROL Custom Alerts] incluye la vista [!UICONTROL Alert Templates], que enumera todas las plantillas de alerta creadas para la cuenta y desde las cuales puede crear, editar, pausar, reactivar y eliminar plantillas de alerta. La vista [!UICONTROL Triggered Alerts] enumera las instancias de alerta generadas.

## Acciones disponibles

* [Ver alertas activadas](#alert-view)

* [Ver plantillas de alerta personalizadas](#alert-template-view)

* [Crear una plantilla de alerta personalizada](#alert-template-create)

* [Editar una plantilla de alerta personalizada](#alert-template-edit)

* [Pausar una plantilla de alerta personalizada](#alert-template-pause)

* [Activar una plantilla de alerta personalizada](#alert-template-activate)

* [Eliminar una plantilla de alerta personalizada](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## Ver alertas activadas {#alert-view}

1. En la parte superior derecha de cualquier página, haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada").

1. Haga clic en la ficha **[!UICONTROL Triggered Alerts]**.

1. (Opcional) Filtre la lista para incluir alertas para un tipo de entidad específico o busque una cadena de texto dentro del nombre de la plantilla. Las consultas de búsqueda no distinguen entre mayúsculas y minúsculas.

## Ver plantillas de alerta personalizadas {#alert-template-view}

1. En la parte superior derecha de cualquier página, haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada"), que se abre en la ficha [!UICONTROL Alert Templates].

1. (Opcional) Filtre la lista para incluir alertas para un tipo de entidad específico o busque una cadena de texto dentro del nombre de la plantilla. Las consultas de búsqueda no distinguen entre mayúsculas y minúsculas.

1. (Opcional) Para ver todos los criterios de una plantilla de alerta, haga clic en el número de criterios (como ![Ejemplo de botón de criterios de alerta personalizados](/help/search-social-commerce/assets/custom-alert-criteria.png "Ejemplo de botón de criterios de alerta personalizados").

## Crear una plantilla de alerta personalizada {#alert-template-create}

Las nuevas plantillas de alerta tienen el estado &quot;[!UICONTROL Active]&quot;.

1. Realice una de las acciones siguientes:

   * En la parte superior derecha de cualquier página, haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada") > **[!UICONTROL Create Custom Alert]**.

   En la parte superior derecha de cualquier página, haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada") > **[!UICONTROL View Custom Alerts]**, que se abre en la ficha [!UICONTROL Alert Templates]. Haga clic en **[!UICONTROL Create Alert]**.

1. Especifique la [configuración de alertas](#alert-template-settings) en las fichas **[!UICONTROL Entity]**, **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** y **[!UICONTROL Scheduling and Delivery]**.

   Puede moverse entre las fichas haciendo clic en el nombre de la ficha (por ejemplo, &quot;Filtros&quot;) o haciendo clic en **[!UICONTROL Next]** en la parte inferior derecha.

1. En la ficha [!UICONTROL Summary], haga clic en **[!UICONTROL Create Alert]**.

## Editar una plantilla de alerta personalizada {#alert-template-edit}

1. En la esquina superior derecha, haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada") > **[!UICONTROL View Custom Alerts]**, que se abre en la ficha [!UICONTROL Alert Templates].

1. (Opcional) Filtre la lista para incluir alertas para un tipo de entidad específico o busque una cadena de texto dentro del nombre de la plantilla. Las consultas de búsqueda no distinguen entre mayúsculas y minúsculas.

1. Junto al nombre de la plantilla, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar").

1. En la ventana [!UICONTROL Edit Custom Alert], edite la [configuración de alertas](#alert-template-settings) en las fichas **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** y **[!UICONTROL Scheduling and Delivery]**.

   Puede moverse entre las fichas haciendo clic en el nombre de la ficha (por ejemplo, &quot;Filtros&quot;) o haciendo clic en **[!UICONTROL Next]** en la parte inferior derecha.

1. En la ficha [!UICONTROL Summary], haga clic en **[!UICONTROL Update Alert]**.

## Pausar una plantilla de alerta personalizada {#alert-template-pause}

1. En la esquina superior derecha, haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada") > **[!UICONTROL View Custom Alerts]**, que se abre en la ficha [!UICONTROL Alert Templates].

1. (Opcional) Filtre la lista para incluir alertas para un tipo de entidad específico o busque una cadena de texto dentro del nombre de la plantilla. Las consultas de búsqueda no distinguen entre mayúsculas y minúsculas.

1. En la fila de la plantilla, seleccione *[!UICONTROL Paused]*.

## Activar una plantilla de alerta personalizada {#alert-template-activate}

1. En la esquina superior derecha, haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada") > **[!UICONTROL View Custom Alerts]**, que se abre en la ficha [!UICONTROL Alert Templates].

1. (Opcional) Filtre la lista para incluir alertas para un tipo de entidad específico o busque una cadena de texto dentro del nombre de la plantilla. Las consultas de búsqueda no distinguen entre mayúsculas y minúsculas.

1. En la fila de la plantilla, seleccione *[!UICONTROL Active]*.

## Eliminar una plantilla de alerta personalizada {#alert-template-delete}

Sólo puede eliminar las plantillas de alerta que ha creado.

1. En la esquina superior derecha, haga clic en ![Alerta personalizada](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizada") > **[!UICONTROL View Custom Alerts]**, que se abre en la ficha [!UICONTROL Alert Templates].

1. (Opcional) Filtre la lista para incluir alertas para un tipo de entidad específico o busque una cadena de texto dentro del nombre de la plantilla. Las consultas de búsqueda no distinguen entre mayúsculas y minúsculas.

1. En la fila de la plantilla, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar").

1. En el cuadro del mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Configuración de plantilla de alerta personalizada {#alert-template-settings}

| Ficha | Parámetro | Descripción |
|--- |--- |--- |
|  | [!UICONTROL Name] | El nombre de la alerta. Debe incluir al menos cinco caracteres. |
| [!UICONTROL Date Range] | [!UICONTROL Select Entity] | El tipo de entidad que se va a evaluar: <i>[!UICONTROL Portfolio]</i>, <i>[!UICONTROL Campaign]</i> o <i>[!UICONTROL Ad Group]</i>. |
| [!UICONTROL Date Range] | [!UICONTROL Period] | Intervalo de fecha para el que evaluar las condiciones de la alerta. Las métricas se evalúan en conjunto en todo el intervalo de fechas. Las opciones van de *[!UICONTROL Yesterday]* a *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] | \[Filtros definidos\] | Condiciones para activar la alerta a la hora especificada en la ficha [!UICONTROL Scheduling and Delivery]. Las columnas disponibles varían según el tipo de entidad. Todos los filtros se unen mediante la función booleana AND, lo que significa que se deben cumplir todas las condiciones especificadas.<ul><li><p>Para agregar un filtro, haga lo siguiente:<p><ol><li><p>(Opcional) Para filtrar los nombres de columna por cadena de texto, escriba la cadena de búsqueda en el campo de entrada [!UICONTROL ADD FILTER].</p></li><li><p>En la lista de columnas, seleccione un nombre de columna.</p></li><li><p>Defina el filtro en la columna:</p></li><ul><li><p>(Filtros sin campos de entrada) Haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha abajo") junto al segundo menú y, a continuación, active las casillas de verificación situadas junto a cada valor que desee incluir.</p></li><li><p>(Todos los demás filtros con campos de entrada) Seleccione un operador en el segundo menú y, a continuación, introduzca el valor aplicable.</p><p>Por ejemplo, si ha seleccionado la columna &quot;Clics&quot; y desea devolver solo filas con más de 100 clics, seleccione &quot;mayor que&quot; e introduzca 100 en el campo de entrada.</p><p>Según el tipo de datos, los operadores disponibles pueden incluir <i>greater than</i>, <i>less than</i>, <i>equals</i>, <i>contains</i>, <i>does&#39;t contain</i>, <i>starts with</i>, <i>ends with</i>, <i>no value</i>, <i>has value</i>, <i>before</i>, <i>after</i> o <i>no fecha</i>.</p><p>**Nota:** Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si filtra por campañas con &quot;préstamo&quot; en el nombre, los resultados podrían incluir &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.</p></li></ol><li><p>Para quitar un filtro, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto a la definición del filtro.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[cuando\] | La frecuencia con la que la alerta comprueba los filtros de condición especificados y, cuando se cumplen todas las condiciones, envía notificaciones por correo electrónico:<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*Día de la semana*> a las &lt;*N*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*Día NN*> a las &lt;*NN*> `[AM\|PM]`]</p></li></ul>**Nota:** Este valor no afecta al período de evaluación. |
|  | [!UICONTROL Email Recipients] | (Editable solo por el creador de la plantilla de alerta; solo lectura para todos los demás) Usuarios de búsqueda registrada, medios sociales y Commerce a los que enviar notificaciones cuando se activa una alerta. De forma predeterminada, el nombre de la cuenta de usuario está seleccionado. Si lo desea, puede agregar o eliminar usuarios con acceso a los datos del anunciante.<br><br>Cuando la alerta incluye hasta 1000 registros, se adjunta una versión CSV de la alerta al mensaje de correo electrónico. |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
