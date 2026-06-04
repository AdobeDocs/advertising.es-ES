---
title: Administrar restricciones para buscar unidades de oferta
description: Obtenga información acerca de las restricciones para restringir ofertas para unidades de oferta en campañas CPC en portafolios de nivel de palabra clave heredados.
feature: Search Campaign Management, Search Optimization
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: c800239a-06eb-4249-9aef-771973d24d35
source-git-commit: 9cc395a6b0fe25435ca6ed022f8da767d525d68e
workflow-type: tm+mt
source-wordcount: 2660
ht-degree: 0%

---

# Administrar restricciones para buscar unidades de oferta

*Aplicable solo para unidades de oferta en campañas CPC en portafolios de nivel de palabra clave heredados*

Las restricciones de unidad de oferta son reglas que restringen las ofertas optimizadas para todas las [unidades de oferta](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html) con modelos de costo e ingresos asociados con la restricción.

## Acerca de las restricciones

Cada restricción se aplica a una moneda específica y, opcionalmente, incluye condiciones de activación que deben cumplirse durante un período de evaluación de datos especificado para que se aplique la regla. Los datos que se van a evaluar pueden incluir tipo de canal, tipo de coincidencia, datos de clic, datos de conversión o métricas derivadas. Por ejemplo, puede restringir las pujas a un rango monetario específico, aumentar o disminuir continuamente las pujas en una cantidad especificada o pujar de acuerdo con la puja promedio de la cartera. Cada restricción tiene una fecha de inicio aplicable y caduca en una fecha específica o se aplica indefinidamente.

Después de configurar una restricción, puede asignarla a unidades de oferta específicas o a todas las unidades de oferta dentro de grupos de anuncios o campañas específicos. Cada unidad de oferta puede tener una restricción. Las restricciones las heredan las entidades secundarias, pero se pueden anular. Una restricción asignada en el nivel inferior siempre anula una restricción asignada en un nivel padre. Cuando se asigna una restricción a una unidad de oferta, la oferta funciona dentro de las restricciones especificadas para esa unidad de oferta, independientemente de los ingresos que genere la unidad de oferta, cuando la unidad de oferta tiene modelos de costes e ingresos.

>[!CAUTION]
>
>Cuando asigna restricciones a una unidad de oferta, anula la decisión del sistema de optimización de ofertas y asume la responsabilidad del ROI de esa unidad de oferta.

>[!NOTE]
>
>* Las restricciones activas restringen las ofertas solo para las unidades de oferta asignadas en portafolios optimizados de nivel de palabra clave heredados. Se ignoran para las unidades de oferta que están en portafolios híbridos, en portafolios activos o que no están en portafolios. **Sugerencia:** En la configuración del portafolio, active la opción del portafolio para &quot;Ajustar automáticamente los límites presupuestarios de la campaña&quot;. El valor &quot;Múltiple&quot; recomendado es &quot;1&quot;.
>* Las restricciones de oferta se omiten para las unidades de oferta sin datos suficientes para generar modelos de costes e ingresos.
>* (Campañas con una estrategia de oferta de CPC o eCPC) Cuando una restricción de oferta entra en conflicto con un límite de oferta de nivel de cartera, la restricción anula el límite de nivel de cartera. Por ejemplo, si la oferta mínima de una cartera es de 5 USD pero restringe una unidad de oferta de la cartera a una oferta mínima de 3 USD, la unidad de oferta se oferta a 3 USD o más. Sin embargo, el gasto general para las unidades de oferta restringidas está determinado por el parámetro [&quot;Restricciones del gasto alrededor&quot; del portafolio](#spend-around-constraints).
>* Las restricciones funcionan en la oferta base. Cualquier tipo de ajuste de la oferta a la oferta base (como aumentar la oferta para usuarios finales en dispositivos móviles) puede hacer que la oferta se sitúe fuera del intervalo permitido para la restricción. Por ejemplo, si la restricción requiere un CPC máximo de 6 USD, la oferta base ya es de 6 USD y la cartera optimiza automáticamente los ajustes de oferta para dispositivos móviles en un 50%-60%, entonces el CPC máximo es de 9,00-9,60 USD, no de 6 USD.

### Tipos de restricción {#constraint-types}

* **[!UICONTROL Bid]:** Restringe las ofertas a un intervalo monetario.

* **[!UICONTROL Bid Shift]:** Cambia continuamente las ofertas optimizadas para todas las unidades de oferta asociadas por una cantidad especificada, dentro de los límites de oferta. Un cambio en la oferta hace que las carteras relevantes gasten más o menos de lo debido a la cantidad total causada por el cambio en la oferta, independientemente de la configuración de la cartera para Restricciones del gasto. Nota: Si la oferta CPC actual ya es igual o mayor que la oferta máxima, o igual o menor que la oferta mínima, la restricción se ignora y la oferta no cambia. Además, las restricciones del cambio de oferta no se aplican a las unidades de oferta sin datos suficientes para generar modelos de costes e ingresos.

* **[!UICONTROL Incremental Bidding]:** (aplicable solo a palabras clave sin impresiones) Aumenta o disminuye la oferta de forma incremental a una tasa especificada hasta que la oferta alcance un objetivo designado.

* **[!UICONTROL Search Engine Min Bid]:** (solo cuentas de [!DNL Google Ads]) Utiliza las ofertas CPC mínimas determinadas por el motor de búsqueda como ofertas mínimas. A medida que el motor de búsqueda cambia sus ofertas mínimas, su oferta cambia en consecuencia. Si lo desea, puede especificar límites de oferta adicionales para todas las unidades de oferta asociadas.

* **[!UICONTROL Impression Share]:** ([!DNL Google Ads] y [!DNL Microsoft Advertising] campañas CPC solo con coincidencia exacta) Restringe las ofertas a un intervalo monetario cuando los anuncios están entre un porcentaje de impresión mínimo y máximo. **Nota:** Cuando la restricción no es rentable, la capacidad de optimización puede anularla.

### Cuándo aplicar restricciones

Algunas razones para restringir las unidades de oferta son las siguientes:

* Para exponer rápidamente palabras clave y anuncios que no se han probado.

* Para mitigar los riesgos de nuevos portafolios, cuentas, campañas y grupos de anuncios. Por ejemplo, antes de lanzar una cartera, puede establecer un máximo de pujas en unidades de pujas de alto tráfico y luego aumentar gradualmente los valores cada día. Esto permite que el modelo de oferta se ajuste cada día sin el riesgo de grandes aumentos de oferta.

* Para asegurarse de que las palabras clave de cola con altas tasas de conversión no se pujen hacia abajo.

* Para ofrecer términos específicos que son fundamentales para su marca o durante las promociones.

### Dónde ver información sobre las restricciones en la interfaz de usuario

Además de abrir la vista [[!UICONTROL Constraints]](#constraints-view), también puede ver información relacionada con sus restricciones de las siguientes maneras:

* Todas las restricciones son valores de etiqueta para una sola [clasificación de etiqueta](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html) denominada &quot;[!UICONTROL Constraints]&quot;.

   * &quot;[!UICONTROL Constraints]&quot; está incluido en la lista &quot;[!UICONTROL Classifications]&quot; de la configuración de vista predeterminada y personalizada y en los informes programados. Puede agregar la columna siempre que desee ver las restricciones asignadas a las entidades relevantes.

   * Cuando descarga una hoja de edición masiva, &quot;[!UICONTROL Constraints]&quot; aparece en la columna &quot;[!UICONTROL Classifications]&quot; para las entidades aplicables en el cuadro de diálogo [!UICONTROL Download Bulksheet]. Cuando se incluye la columna, la hoja de edición masiva descargada incluye todas las restricciones asignadas a las entidades relevantes.

  La clasificación [!UICONTROL Constraints] no se incluye en la vista [!UICONTROL Label Classifications]; la vista [!UICONTROL Constraints] es independiente. La clasificación [!UICONTROL Constraints] tampoco se incluye en el límite de clasificación de 30 etiquetas.

* [El [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md) incluye datos de costo, clics y (opcionalmente) conversión para restricciones que utilizan la arquitectura de clasificación de etiquetas.

### La vista [!UICONTROL Constraints] {#constraints-view}

La vista [!UICONTROL Goals] > [!UICONTROL Constraints] enumera todas sus restricciones. Las columnas disponibles incluyen el estado de restricción; el tipo de restricción, las fechas de inicio y finalización; el número de campañas, grupos de publicidad, palabras clave, anuncios, ubicaciones, destinos automáticos y grupos de productos a los que está asociada la restricción; datos de impresiones, clics y costos; y datos de ingresos para todas las métricas de conversión visibles.<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>Es posible que los datos de rendimiento de una fila en la vista [!UICONTROL Constraints] no coincidan con los datos de rendimiento de la entidad de nivel superior a la que se asigna la restricción. Debido a que una restricción asignada en el nivel inferior siempre anula una restricción asignada en un nivel principal, una restricción asignada a una campaña o grupo de anuncios puede no permanecer asignada a los grupos de anuncios secundarios y a las palabras clave. Por ejemplo, si la Campaña A tiene asignada la Restricción A, todos los grupos de anuncios y las palabras clave de la Campaña A heredarán automáticamente la Restricción A. Sin embargo, esos grupos de anuncios y palabras clave podrían asignarse posteriormente a otras restricciones, como la Restricción B, y perderían su asociación con la Restricción A.

>[!NOTE]
>
>Asigne restricciones a las unidades de oferta y cancele su asignación desde la vista de administración de entidades correspondiente (por ejemplo, desde la vista [!UICONTROL Campaigns] para restricciones de nivel de campaña).

#### Acciones disponibles

* [Crear una restricción](#constraint-create).

* [Editar configuración de restricción](#constraint-edit).

* [Cambiar el estado de las restricciones](#constraint-change-status).

## Crear una restricción {#constraint-create}

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. En la barra de herramientas superior derecha sobre la tabla de datos, haga clic en **[!UICONTROL Create Constraint]**.

1. Escriba la [configuración de restricción](#constraint-settings).

   Para moverse entre la ficha [!UICONTROL Constraint Type] y la ficha [!UICONTROL Conditions], haga clic en la ficha que desee abrir o en los botones [!UICONTROL Next] y [!UICONTROL Back].

1. Haga clic en **[!UICONTROL Review and Save]** para revisar la configuración.

1. Haga clic en **[!UICONTROL Save]**.

Una vez creada una restricción, puede [asignarla](#constraint-assign) a campañas, grupos de anuncios, palabras clave, ubicaciones y grupos de productos de nivel de unidad.

## Editar configuración de restricción {#constraint-edit}

Puede editar la configuración de una restricción a la vez.

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Opcional) Filtre la lista [de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o de un [encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Seleccione la casilla de verificación situada junto a la restricción que desea editar.

1. En la barra de herramientas de acciones masivas, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar").

1. Editar la [configuración de restricción](#constraint-settings).

   Para moverse entre la ficha [!UICONTROL Constraint Type] y la ficha [!UICONTROL Conditions], haga clic en la ficha que desee abrir o en los botones [!UICONTROL Next] y [!UICONTROL Back].

1. Haga clic en **[!UICONTROL Review and Save]** para revisar la configuración.

1. Haga clic en **[!UICONTROL Save]**.

## Cambio del estado de las restricciones {#constraint-change-status}

Puede pausar cualquier restricción activa para deshabilitarla. Puede habilitarlo más tarde si vuelve a cambiar el estado a *activo*.

También puede eliminar una restricción, lo que elimina todas las asociaciones con componentes de cuenta y hace que la restricción no esté disponible para su uso futuro. Los datos del informe para la restricción ya no están disponibles. **Nota:** Para simplemente desasociar una restricción de un componente de cuenta, consulte &quot;[Desasignar restricciones de las unidades de oferta de búsqueda](#constraints-unassign)&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Opcional) Filtre la lista [de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o de un [encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Seleccione la casilla de verificación situada junto a cada restricción cuyo estado desee cambiar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en el botón de estado:

   * Para activar todas las filas seleccionadas, haga clic en ![Activar](/help/search-social-commerce/assets/activate-new.png "Activar").

   * Para pausar todas las filas seleccionadas, haga clic en ![Pausar](/help/search-social-commerce/assets/pause-new.png "Pausar").

   * Para eliminar todas las filas seleccionadas, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar").

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Configuración de restricciones {#constraint-settings}

| Ficha | Parámetro | Descripción |
|---|---|---|
| \[Información básica\] | [!UICONTROL Constraint Name] | Un nombre único para la restricción. |
| | [!UICONTROL Currency] | Divisa en la que se pujan todas las unidades de puja aplicables. Las unidades de oferta para las que se usa una moneda diferente se ignoran. |
| | [!UICONTROL Status] | El estado de la restricción:<ul><li>**Activo:** (el valor predeterminado) La restricción se aplica durante las condiciones especificadas y el intervalo de fechas.</li><li>**En pausa:** La restricción no se ha aplicado.</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | El tipo de restricción. Para obtener descripciones de los tipos de restricción y las redes de anuncios aptas para cada uno, consulte &quot;[Tipos de restricción](#constraint-types)&quot;. |
| | [!UICONTROL Start Date] | Primer día en el que surte efecto la restricción. El valor predeterminado es el día actual. Para cambiar la fecha, escriba una fecha o haga clic en ![Calendario](/help/search-social-commerce/assets/calendar-new.png "Calendario") para abrir el calendario y seleccionar una fecha. |
| | [Fecha de finalización] | Si la restricción no será efectiva en una fecha específica. Para aplicar la restricción indefinidamente, como cuando la unidad de oferta es fundamental para la marca de la empresa, deje vacío el campo. Para finalizar la restricción en una fecha específica, escribe una fecha o haz clic en ![Calendario](/help/search-social-commerce/assets/calendar-new.png "Calendario") para abrir el calendario y seleccionar una fecha. **Nota:** La restricción no puede caducar antes de mañana. |
| | [!UICONTROL Set constraint options for Bid] | (Solo restricciones de [!UICONTROL Bid]) La configuración incluye:<ul><li>**[!UICONTROL Min Bid]:** La oferta base mínima para las unidades de oferta asociadas.</li><li>**[!UICONTROL Max Bid]:** La oferta base máxima para las unidades de oferta asociadas.</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | ([!UICONTROL Bid Shift] restricciones solamente) El tipo y la cantidad de desplazamiento de la oferta que se aplicará continuamente a la oferta base:<ul><li>*[!UICONTROL Increases]:* Aumenta las ofertas en un porcentaje o valor de moneda especificado. Escriba la cantidad que desea cambiar y, a continuación, seleccione *$* o *%*. Escriba también **[!UICONTROL Max Limit]**, que es la oferta (techo) más alta posible cuando se aplica la restricción. **Nota:** Si la oferta CPC actual ya es igual o mayor que [!UICONTROL Max Limit], la restricción se omitirá y la oferta no cambiará.</li><li>*[!UICONTROL Decreases]:* Reduce las ofertas en un porcentaje o valor de moneda especificado. Escriba la cantidad que desea cambiar y, a continuación, seleccione *$ o %*. Escriba también **[!UICONTROL Min Limit]**, que es la oferta (suelo) más baja posible cuando se aplica la restricción. **Nota:** Si la oferta CPC actual ya es igual o menor que [!UICONTROL Min Limit], la restricción se omite y la oferta no cambia.</li></ul>**Notas:**<ul><li>Un cambio de oferta hará que las carteras relevantes gasten más o menos de la cantidad total causada por el cambio de oferta, independientemente de la configuración de la cartera para &quot;[!UICONTROL Spend Around Constraints]&quot;.</li><li>Si especifica una fecha de finalización para la restricción y la capacidad de optimización ajusta automáticamente los límites de gasto para las campañas del portafolio, las ofertas no solo vuelven a las cantidades originales después de la fecha de finalización, sino que se ajustan como óptimas.</li><li>Los turnos de oferta no se aplican a las unidades de oferta sin datos suficientes para generar modelos de costes e ingresos.</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | ([!UICONTROL Incremental Bidding] restricciones solamente) Un objetivo de oferta, y cuánto y con qué frecuencia se aumenta o se reduce la oferta incrementalmente hasta que alcanza el objetivo:<ul><li>**[!UICONTROL Bid target]:** El importe de la oferta de destino.</li><li>**[!UICONTROL Incrementally change bids by]** y **[Type]:** Cuánto se incrementan o disminuyen las ofertas, y si se cambian las ofertas por un valor de moneda (**$**) o porcentaje (*%*).</li><li>**[!UICONTROL Every __ days]:** ¿Con qué frecuencia se incrementan las ofertas?</li></ul>Por ejemplo, supongamos que la oferta actual de una de las palabras clave es de 100 céntimos y que desea cambiar la oferta en un 10 % todos los días hasta alcanzar el objetivo de 500 céntimos. En el día 1, después de establecer la restricción, la oferta para esa palabra clave es de 110 céntimos (oferta actual + 10 %). En el día 2, la puja es de 120 céntimos (oferta actual para el día 1 + 20%), etc. Sin embargo, si el objetivo de la oferta es 50 céntimos y los demás parámetros son los mismos, las ofertas disminuyen gradualmente hasta que alcanzan los 50 céntimos. |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | ([!UICONTROL Search Engine Min Bid] restricciones) Utiliza la oferta mínima necesaria para mostrar una unidad de oferta en la primera página de resultados de búsqueda en Google ([!UICONTROL Google First Page CPC]). Opcionalmente, introduzca un valor **[!UICONTROL Min Bid]** o un valor **[!UICONTROL Max Bid]** para definir el rango de ofertas aptas para la restricción. Por ejemplo, si especifica un(a) [!UICONTROL Min Bid] de 2,50 USD y un(a) [!UICONTROL Max Bid] de 4 USD, entonces no pujará por la unidad de oferta si la oferta de la primera página de [!DNL Google Ads] es inferior a 2,50 USD o superior a 4 USD. |
| | [!UICONTROL Set constraint options for Impression Share] | (Solo restricciones de [!UICONTROL Impression Share]) La configuración incluye:<ul><li>**[!UICONTROL Min Bid]** (opcional) la oferta base mínima para las unidades de oferta asociadas.</li><li>**[!UICONTROL Max Bid]:** (opcional) la oferta base máxima para las unidades de oferta asociadas.</li><li>**[!UICONTROL Min Impression Share]:** El porcentaje de impresión más bajo, como porcentaje, que generará un déclencheur de la restricción para las unidades de oferta aplicables. Debe estar entre 10 y 90. **Nota:** Cuando la restricción no es rentable, la capacidad de optimización puede anularla.</li><li>**[!UICONTROL Max Impression Share]:** El porcentaje de impresión más alto, como porcentaje, que generará un déclencheur de la restricción para las unidades de oferta aplicables. Debe estar entre 10 y 90.**Nota:** Si la restricción no es rentable, la capacidad de optimización puede invalidarla.</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | Si se aplican condiciones a la restricción:<ul><li>*[!UICONTROL No Condition]:* (valor predeterminado) La restricción se aplica incondicionalmente durante el intervalo de fechas especificado.</li><li>*[!UICONTROL Satisfy]:* La restricción se aplica solamente cuando se cumplen las condiciones especificadas durante un período de evaluación de datos especificado.</li></ul> |
| | [!UICONTROL Data Evaluation Period] | (Cuando se establecen las condiciones) Período de tiempo durante el cual se evalúan los datos para los criterios especificados. Si selecciona *[!UICONTROL Custom date range],**, especifique **[!UICONTROL Start Date]** y **[!UICONTROL End Date]**; para ello, introduzca cada fecha en el formato `MM-DD-YYYY` (por ejemplo, 29-03-2026 para el 29 de marzo de 2026) o haga clic en ![botón del calendario](/help/search-social-commerce/assets/calendar-new.png "botón del calendario") para abrir el calendario y seleccionar cada fecha. |
| | [!UICONTROL When to Apply Constraints] | (Cuando se establecen las condiciones) Cuántas condiciones de filtro deben cumplirse para aplicar la restricción:<ul><li>*[!UICONTROL Match All Filters]:* Aplica la restricción cuando se cumplen todas las condiciones de filtro especificadas.</li><li>*[!UICONTROL Match Any Filters]:* Aplica la restricción cuando se cumple al menos una de las condiciones de filtro especificadas.</li></ul> |
| | [!UICONTROL Filters] | (Cuando se establecen las condiciones) Uno o más criterios que deben cumplirse. Para crear un filtro, seleccione una propiedad o métrica de la lista. Para propiedades (como [!UICONTROL Channel Type]), seleccione los valores aplicables en la lista. Para métricas (como [!UICONTROL Clicks]), seleccione un operador y luego introduzca el valor aplicable. Por ejemplo, para devolver solo unidades de oferta con más de 100 clics, seleccione **Clics**, seleccione **mayor que** y, a continuación, escriba `100` en el campo de entrada.</li></ul> |

## Asignar restricciones a las unidades de oferta de búsqueda {#constraint-assign}

Puede aplicar restricciones de unidad de oferta a cualquier campaña, grupo de publicidad, palabra clave, ubicación o destino de búsqueda dinámica (segmentación automática).

Cada entidad solo puede tener una restricción. Se puede asignar una única restricción a una o varias entidades al mismo tiempo.

>[!NOTE]
>
>* Si posteriormente edita una palabra clave o la copia de anuncio de un anuncio (creando así una nueva palabra clave o anuncio), la restricción no se asigna a la nueva entidad.
>* Ver las mismas instrucciones en la vista [[!UICONTROL Campaigns]](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), la vista [[!UICONTROL Ad Groups]](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), la vista [[!UICONTROL Keywords]](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md) o la vista [[!UICONTROL Placements]](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. En el menú principal, abra la vista de administración correspondiente.

   Por ejemplo, para asignar restricciones en el nivel de campaña, vaya a [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. (Opcional) Filtre la lista [de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o de un [encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Seleccione la casilla de verificación situada junto a cada entidad a la que va a asignar una única restricción.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

## Anular la asignación de restricciones de unidades de oferta de búsqueda {#constraints-unassign}

>[!NOTE]
>
>* Para eliminar una restricción, de modo que no esté disponible para un uso futuro, consulte &quot;[Cambiar el estado de las restricciones](#constraint-change-status)&quot;.
>* Ver las mismas instrucciones en la vista [[!UICONTROL Campaigns]](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), la vista [[!UICONTROL Ad Groups]](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), la vista [[!UICONTROL Keywords]](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md) o la vista [[!UICONTROL Placements]](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. En el menú principal, abra la vista de administración correspondiente.

   Por ejemplo, para anular la asignación de restricciones de nivel de campaña, vaya a [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. Seleccione la casilla de verificación situada junto a cada entidad de la que desea anular la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Administrar asignaciones de restricción para campañas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Administrar asignaciones de restricción para grupos de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Administrar asignaciones de restricción para palabras clave](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
>* [Administrar asignaciones de restricción para las ubicaciones](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)
>* [El [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)
