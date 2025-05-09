---
title: Administrar vistas predeterminadas y personalizadas
description: Aprenda a personalizar las vistas predeterminadas y las vistas personalizadas.
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '2836'
ht-degree: 0%

---

# Administrar vistas predeterminadas y personalizadas

Las vistas predeterminadas y las vistas personalizadas le permiten personalizar los datos de rendimiento que se muestran en las vistas de datos de campaña de búsqueda. La configuración de vista incluye las columnas que se van a incluir, los filtros, el intervalo de fechas, la configuración de atribución de conversión y otros ajustes avanzados, y puede aplicarlos temporalmente o guardarlos. (Excepción: no se pueden guardar filtros para vistas predeterminadas). Cada vista personalizada predeterminada y regular se aplica solo a una vista de entidad específica (como [!UICONTROL Campaigns]) y a una cuenta de anunciante específica. Cada vista personalizada universal se aplica en todas las vistas de entidad de un anunciante específico y, por lo tanto, no puede incluir columnas de propiedad (como nombre de entidad o estado), que varían según el tipo de entidad.

Las vistas predeterminadas se muestran de forma predeterminada cada vez que inicia sesión. Puede crear vistas personalizadas adicionales y aplicarlas en cualquier momento. Opcionalmente, puede compartir cualquier vista personalizada que cree con todos los demás usuarios que puedan ver los datos del anunciante. En las listas de vistas, cada vista que comparte otra persona está en cursiva, como &quot;*Campañas de mayor rendimiento*&quot;. Solo la persona que crea una vista personalizada puede eliminarla.

Cada vista está disponible como acceso directo en la sección [!UICONTROL Custom Views] del panel izquierdo.

## Aplicar una vista predeterminada o personalizada

* (Vistas predeterminadas) En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]** \> **\[tipo de entidad\]**.

* (Vistas personalizadas) Desde el panel de navegación izquierdo:

   1. En el panel izquierdo, haga clic en el menú **[!UICONTROL Custom Views]** para expandirlo.

      Las vistas se ordenan por entidad aplicable.

   1. Expandir los menús disponibles.

      &quot;[!UICONTROL Universal Views]&quot; incluye vistas personalizadas que se pueden usar en todas las vistas de entidades. Todas las demás vistas personalizadas se agrupan por tipo de entidad.

   1. Haga clic en el nombre de la vista.

      Si la vista es universal o se aplica a la entidad actual, la tabla de datos se vuelve a mostrar según la configuración de la vista. Si la vista se aplica a una entidad diferente, los datos de la entidad aplicable se muestran según la configuración de la vista.

## Creación de una vista personalizada {#create-custom-view}

Las vistas personalizadas solo se aplican a las vistas de administración de campañas.

>[!NOTE]
>
>Además de la configuración de vista que especifique para la vista personalizada, también se guarda el orden de clasificación de columnas actual.

1. En el lado derecho de la barra de herramientas sobre la tabla de datos, haga clic en el nombre de la vista actual (que podría ser &quot;[!UICONTROL Default]&quot;).

1. Especifique la [configuración de vista personalizada](#view-settings):

   1. (Opcional) Para que la configuración de datos esté disponible en todas las vistas de entidades (para [!UICONTROL Campaigns], [!UICONTROL Ads], etc.), seleccione **[!UICONTROL Universal View]**.

      Una vez habilitada o deshabilitada esta opción, no se puede guardar el cambio en la vista existente, pero se puede crear una nueva vista con el cambio.

   1. (Opcional) Para que la vista esté disponible para todos los demás usuarios que puedan ver los datos del anunciante, mueva el control deslizante **[!UICONTROL Shared]** a *[!UICONTROL Yes]*.

   1. (Opcional) En la ficha **[!UICONTROL Columns]**, cambie las columnas disponibles para la ficha, su orden y cómo ordenar las filas.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Filters]** y, a continuación, especifique los filtros que desee aplicar.

      La aplicación de filtros devuelve filas únicamente cuando el valor de una métrica cumple los criterios especificados, independientemente de si la métrica se incluye o no como una columna en el informe.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Date]** y cambie la configuración de fecha predeterminada.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Additional Settings]** y cambie la configuración.

1. Haga clic en **[!UICONTROL Save as New]**.

1. Escriba el nombre de la nueva vista y haga clic en **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Utilice un nombre que le ayude a identificar la pestaña y la información a la que se aplica (como &quot;Campañas en pausa&quot; o &quot;Principales 50 anuncios&quot;).

### Edición de una vista predeterminada o personalizada

1. Abra la configuración de vista:

   * (Si ya ha aplicado la vista) En el lado derecho de la barra de herramientas sobre la tabla de datos, haga clic en el nombre de la vista actual (que puede ser &quot;[!UICONTROL Default]&quot;).

   * (Vistas personalizadas que no se aplican) En el panel izquierdo, haga clic en ![Vistas personalizadas](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vistas personalizadas") para expandir el menú [!UICONTROL Custom Views]. Haga clic en el nombre de vista personalizada.

1. Editar la [configuración de vista](#view-settings):

   1. (Opcional) Para habilitar o deshabilitar la configuración de datos en todas las vistas de entidades de búsqueda (para [!UICONTROL Campaigns], [!UICONTROL Ad Groups], etc.), seleccione o deseleccione **[!UICONTROL Universal View]**.

      No puede guardar el cambio en la vista existente, pero puede crear una nueva vista con el cambio.

   1. (Opcional; vistas personalizadas que solo ha creado) Si la vista aún no es pública, haga que esté disponible para todos los demás usuarios que puedan ver los datos del anunciante moviendo el control deslizante **[!UICONTROL Shared]** a *[!UICONTROL Yes]*.

   1. (Opcional) En la ficha **[!UICONTROL Columns]**, cambie las columnas disponibles para la ficha, su orden y cómo ordenar las filas.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Filters]** y, a continuación, edite los filtros que desee aplicar.

      La aplicación de filtros devuelve filas únicamente cuando el valor de una métrica cumple los criterios especificados, independientemente de si la métrica se incluye o no como una columna en el informe.

      >[!NOTE]
      >
      >Puede aplicar, pero no guardar, los cambios en los filtros a la configuración de vista predeterminada.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Date]** y cambie la configuración de fecha predeterminada.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Additional Settings]** y cambie la configuración.

1. Aplique o guarde la configuración:

   * Para aplicar la configuración temporalmente sin guardarla en la vista, haga clic en **[!UICONTROL Apply]**.

     La configuración se aplicará a la ficha hasta que se aleje de la vista de administración de nivel superior o (cuando corresponda) [vea los datos de otro anunciante](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (Para vistas predeterminadas y vistas personalizadas que haya creado) Para guardar la configuración en la vista actual, haga clic en **[!UICONTROL Save]**.

   * Para guardar la configuración en una nueva vista personalizada, haga clic en **[!UICONTROL Save As]**. En la ventana [!UICONTROL Enter New Custom View Name], escriba el nombre de la nueva vista y haga clic en **[!UICONTROL Save]**.

## Restablecer una vista predeterminada a la configuración predeterminada del sistema

Al restaurar la configuración de vista predeterminada, se quitan todas las opciones que se han guardado y se vuelven a aplicar las opciones predeterminadas del sistema.

La configuración predeterminada del sistema varía según la pestaña. En la mayoría de las pestañas, la vista predeterminada del sistema muestra los datos del día anterior de los elementos de cuentas habilitadas y que están activos (por ejemplo, solo grupos de anuncios activos en campañas activas), con los datos ordenados por coste y con los datos de conversión basados en la fecha de transacción.

1. En el panel izquierdo, haga clic en ![Vistas personalizadas](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vistas personalizadas") para expandir el menú [!UICONTROL Custom Views].

   Las vistas se ordenan por entidad aplicable.

1. Junto al nombre de la vista, haga clic en ![Restaurar a la configuración predeterminada](/help/search-social-commerce/assets/restore.png "Restaurar a la configuración predeterminada").

## Eliminar una vista personalizada

Puede eliminar cualquier vista personalizada que haya creado.

Si elimina una vista personalizada que se ha aplicado a la ficha actual, la ficha seguirá mostrando la vista personalizada hasta que salga del conjunto de vistas (por ejemplo, de las vistas del menú [!UICONTROL Search] al menú [!UICONTROL Reports]) o (cuando corresponda) cuando [vea datos de otro anunciante](/help/search-social-commerce/common-tasks/change-advertiser.md).

1. En el panel izquierdo, haga clic en ![Vistas personalizadas](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vistas personalizadas") para expandir el menú [!UICONTROL Custom Views].

1. Mantenga el cursor sobre el nombre de vista personalizada y haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar").

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Continue]**.

## Configuración de vista predeterminada y personalizada {#view-settings}

| **Ficha** | **Campo** | **Descripción** |
| --- | --- | --- |
| [Sobre todas las fichas] | Nombre | Un nombre único para la vista. No puede editar el nombre de una vista predeterminada.<p><b>Sugerencia:</b> Use un nombre que le ayude a identificar la ficha y la información a la que se aplica (como &quot;Campañas en pausa&quot; o &quot;Principales 50 anuncios&quot;). |
|   | Vista universal | Hace que la configuración de datos esté disponible en todas las vistas de entidad (para campañas, anuncios, etc.). Las vistas universales pueden incluir columnas de clasificación de métricas y etiquetas, pero no columnas de propiedad (como nombre y estado de la entidad) porque difieren según el tipo de entidad), así como todos los demás atributos de vista. Cualquier criterio de filtro se aplica a la vista de entidad cuando corresponde y se ignora en caso contrario. Todos los filtros de métricas se evalúan localmente (por ejemplo, para los clics \> 1000, las vistas Campañas muestran campañas con más de 1000 clics y la vista Grupos de anuncios muestra grupos de anuncios con más de 1000 clics).<p>Las columnas de propiedades de una vista universal se extraen de la vista predeterminada de la entidad. Puede cambiar las columnas de propiedad predeterminadas para una entidad específica en la configuración de vista predeterminada.<p>Una vez habilitada o deshabilitada esta opción, no se puede guardar el cambio en la vista existente, pero se puede crear una nueva vista con el cambio. |
|   | Compartir | (Solo vistas personalizadas; opcional) Hace que la vista esté disponible para todos los demás usuarios que puedan ver los datos del anunciante. Otros usuarios no pueden editar ni eliminar la vista, pero sí crear una nueva vista a partir de la configuración. En las listas de vistas, cada vista que comparte otra persona está en cursiva, como &quot;_Campañas de mayor rendimiento_&quot;. |
| Columnas | Columnas seleccionadas y orden | Las columnas de datos que se muestran y su orden:<ul><li> (Para agregar una columna) En la lista Columnas disponibles, haga clic en el nombre de una columna y arrástrela a la lista Columnas y orden seleccionados o haga clic en ![flecha derecha](/help/search-social-commerce/assets/chevron-right.png) para moverla allí.</li><li>(Para cambiar la posición horizontal de una columna) En la lista Columnas y orden seleccionados, haga clic en el nombre de la columna y, a continuación, arrástrela a la posición deseada o haga clic en ![flecha arriba](/help/search-social-commerce/assets/chevron-up.png) o en ![flecha abajo](/help/search-social-commerce/assets/chevron-down.png) para moverla allí. El nombre de la columna superior aparece en la columna izquierda.</li><li>(Para quitar una columna) En la lista Columnas y orden seleccionados, haga clic en el nombre de una columna y arrástrela a la lista Columnas disponibles o haga clic en ![flecha izquierda](/help/search-social-commerce/assets/chevron-left.png) para moverla allí.</li></ul><b>Filtrar datos</b><p>Para enumerar solo un tipo específico de datos, haga clic en cualquiera de los iconos junto a la lista:<ul><li>![icono de propiedades](/help/search-social-commerce/assets/properties-icon.png) para nombres de propiedades e ID para componentes de búsqueda, como Estado</li><li>![icono de tráfico](/help/search-social-commerce/assets/traffic-metrics-icon.png) para métricas de tráfico estándar, como impresiones y clics</li><li>![icono de ingresos](/help/search-social-commerce/assets/revenue-metrics-icon.png) (para métricas de conversión rastreadas para el anunciante, incluidas las métricas de conversión y participación del sitio sincronizadas desde Analytics)</li><li>![icono personalizado](/help/search-social-commerce/assets/custom-metrics-icon.png) (para métricas derivadas personalizadas creadas por el anunciante)</li><li>![icono de clasificación](/help/search-social-commerce/assets/classifications-icon.png) (para clasificaciones de etiquetas).</li></ul> <b>Notas adicionales:</b><ul><li>Para agregar, crear o editar nuevas métricas, consulte &quot;Crear una métrica personalizada&quot;, &quot;Editar una métrica personalizada&quot; y &quot;Eliminar una métrica personalizada&quot;.</li><li>Si el informe incluye datos de cuentas con distintas monedas, los totales no se incluyen en las columnas basadas en la moneda (como Coste y CPC).</li><li>Puede [editar temporalmente el conjunto de columnas desde el menú de encabezados de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md), y [editar y ordenar el conjunto de columnas desde el icono [!UICONTROL Columns]](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Icono Columnas](/help/search-social-commerce/assets/custom-columns.png "Icono Columnas")).</li></ul> |
|   | Ordenar por | Columna por la que ordenar los datos. El valor predeterminado es diferente para cada tipo de informe. |
|   | Orden de clasificación | Si se ordenan los datos en orden **Ascendente** o **Descendente**. Mueva el control deslizante para seleccionar una opción. |
| Filtros | [Definiciones de filtros] | (Opcional) Filtros que se aplicarán a los datos. La aplicación de filtros devuelve filas únicamente cuando el valor de una columna cumple los criterios especificados.<p>Para aplicar cada filtro:<ol><li>En el menú Agregar filtro, seleccione un nombre de columna. La lista incluye todas las columnas disponibles y se ordena por tipo de columna, con las columnas de propiedad primero.</li><li>Defina el filtro en la columna</li></ol>(Filtros con campos de entrada) Seleccione un operador en el segundo menú y, a continuación, introduzca el valor aplicable. Los valores no distinguen entre mayúsculas y minúsculas. Haga clic en ![icono de verificación](/help/search-social-commerce/assets/select.png) cuando haya terminado.<p>Por ejemplo, si ha seleccionado la columna &quot;Clics&quot; y desea devolver solo filas con más de 100 clics, seleccione _\>_ e introduzca `100` en el campo de entrada.<p>Según el tipo de datos, los operadores disponibles pueden incluir <i>greater than</i>, <i>less than</i>, <i>equals</i>, <i>contains</i>, <i>no contiene</i>, <i>starts with</i>, <i>ends with</i>,<i>no value</i> o <i>has value</i> <i>antes de</i>, <i>después de</i> o <i>sin fecha</i>.<p>(Filtros sin campos de entrada) Haga clic en ![flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png) junto al menú Seleccionar elementos de lista y, a continuación, active las casillas de verificación situadas junto a cada valor que desee incluir. Haga clic en ![icono de verificación](/help/search-social-commerce/assets/select.png) cuando haya terminado.<p><b>Notas:</b><ul><li>Puede aplicar, pero no guardar, los cambios en los filtros a la configuración de vista predeterminada.</li><li>También puede [cambiar temporalmente los filtros aplicables](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) dentro de la vista.</li></ul> |
|   | Incluir filas solo con datos de rendimiento | (Solo vistas de Grupos de anuncios, Palabra clave, Grupos de productos, Ubicaciones y Segmentación automática) <p>Incluye sólo filas con datos de rendimiento durante las fechas especificadas. De forma predeterminada, esta opción está seleccionada para reducir el tiempo de carga de la página. <p><b>Advertencia</b>: Si anula la selección de la opción y la vista incluye muchas entidades sin datos de rendimiento, los datos tardan más en mostrarse.<p> <b>Nota</b>: puede aplicar pero no guardar los cambios en los filtros a la configuración de vista predeterminada. Las vistas predeterminadas siempre muestran solo las entidades con datos de rendimiento. |
| Fecha | Intervalo de fechas | (Cuando se selecciona &quot;Incluir intervalo de fechas&quot;)<p>Intervalo de fecha para el que se van a generar datos. Elija una opción:<ul><li><i>[Intervalo preestablecido]</i>: Una lista de incrementos de tiempo comunes, que van desde <i>Hoy</i> hasta <i>Los últimos 180 días</i>. Elija uno de la lista; el valor predeterminado es <i>Ayer</i>. Nota: <i>Mes pasado</i>, <i>Últimos 3 meses</i> y <i>Últimos 6 meses</i> muestran datos de los meses del calendario anterior.</li><li><i>Intervalo de fechas personalizado:</i> Especifique la fecha de inicio y la fecha de finalización. Introduzca las fechas en formato MM/DD/AAAA o M/D/AAAA, o haga clic en ![icono de calendario](/help/search-social-commerce/assets/calendar.png) junto a un campo y seleccione una fecha.</li></ul> |
|   | Comparación | Compara los datos del intervalo de fechas especificado con los datos de un segundo intervalo de fechas. Al seleccionar esta opción, se añaden dos columnas adicionales para cada columna de datos normal. Por ejemplo, en lugar de incluir una sola columna para &quot;Impresiones&quot;, el informe incluye columnas para &quot;Rango de impresiones 1&quot;, &quot;Rango de impresiones 2&quot; y &quot;Diferencia de impresiones&quot;.<p><b>Notas:</b><ul><li>No se muestra la columna de diferencia para las métricas derivadas.</li><li>Los informes que comparan intervalos de fechas grandes pueden tardar más en generarse.</li></ul> |
|   | Formato de comparación | Cómo expresar la diferencia entre los datos de los dos intervalos de fechas seleccionados en la columna &quot;[_Campo de datos_] Diferencia&quot;. Elija una opción:<ul><li><i>Variance</i> (el valor predeterminado): muestra la diferencia como valor numérico.</li><li><i>% de cambio</i>: Muestra la diferencia como porcentaje.</li></ul> |
| Configuración adicional | Usar valor predeterminado | Aplica la configuración de atribución especificada en la configuración de atribución de conversión de nivel de anunciante. |
|   | Regla de atribución | (Anunciantes solo con el servicio de seguimiento de conversión basado en píxeles de Adobe Advertising) En la pestaña, aprenda a atribuir datos de conversión (potencialmente a través de varios canales de publicidad y portafolios) en una serie de eventos que generan una conversión. De forma predeterminada, la regla especificada en la configuración de atribución de conversión de nivel de anunciante está seleccionada.<ul><li> <i>Primer evento</i>: Atribuye la conversión al primer clic de pago de la serie dentro de la ventana retrospectiva de clics del anunciante o, si no se produjeron clics de pago, a la última impresión dentro de la ventana retrospectiva de impresiones del anunciante.</li><li><i>Más peso en el primer evento</i>: Atribuye la conversión a todos los eventos de la serie que se produjeron en la ventana retrospectiva de clics del anunciante y en la ventana retrospectiva de impresiones, pero da mayor peso al primer evento y, sucesivamente, menos peso a los siguientes eventos. Cuando la conversión va precedida de clics e impresiones de pago, el peso de anulación de impresión especificado se aplica aún más a las impresiones. Cuando la conversión solo está precedida por impresiones, las impresiones se ponderan según el peso de visualización del anunciante en lugar de según el peso de anulación de la impresión.</li><li><i>Distribución de eventos</i>: atribuye la conversión de forma equitativa a cada evento de la serie que se produjo en la ventana retrospectiva de clics del anunciante y en la ventana retrospectiva de impresiones. Cuando la conversión va precedida de clics e impresiones de pago, el peso de anulación de impresión especificado se aplica aún más a las impresiones. Cuando la conversión solo está precedida por impresiones, las impresiones se ponderan según el peso de visualización del anunciante en lugar de según el peso de anulación de la impresión.</li><li><i>Más del último evento de peso</i>: atribuye la conversión a todos los eventos de la serie que se produjeron en la ventana retrospectiva de clics del anunciante y en la ventana retrospectiva de impresiones, pero da mayor peso al último evento y, sucesivamente, menos peso a los eventos anteriores. Cuando la conversión va precedida de clics e impresiones de pago, el peso de anulación de impresión especificado se aplica aún más a las impresiones. Cuando la conversión solo está precedida por impresiones, las impresiones se ponderan según el peso de visualización del anunciante en lugar de según el peso de anulación de la impresión.</li><li><i>Último evento</i> (predeterminado): atribuye la conversión al último clic pagado de la serie dentro de la ventana retrospectiva de clics del anunciante o, si no se produjeron clics pagados, a la última impresión dentro de la ventana retrospectiva de impresiones del anunciante.</li><li><i>Forma de U</i>: atribuye la conversión a todos los eventos de la serie que se produjeron en la ventana retrospectiva de clics del anunciante y en la ventana retrospectiva de impresiones, pero da mayor peso al primer evento y a los últimos, con una ponderación sucesivamente menor a los eventos que se producen en medio de la ruta de conversión. Cuando la conversión va precedida de clics e impresiones de pago, el peso de anulación de impresión especificado se aplica aún más a las impresiones. Cuando la conversión solo está precedida por impresiones, las impresiones se ponderan según el peso de visualización del anunciante en lugar de según el peso de anulación de la impresión.</li></ul><p><b>Notas:</b><ul><li>Todas las reglas de atribución, además de Último evento, solo están disponibles para anunciantes con rastreo de clics de Adobe Advertising y con seguimiento de conversión desde Adobe Advertising o Adobe Analytics (con una integración de Analytics).</li><li>Las reglas de atribución se aplican a los clics en anuncios pagados en cualquier canal. No se aplican a las impresiones de anuncios de búsqueda de pago, que no se pueden rastrear en el nivel de evento.</li><li>Cuando se generan informes de los datos de conversión mediante cualquier regla de atribución excepto una de las reglas &quot;Último evento&quot;, los eventos que llevan a la conversión pueden producirse en varios portafolios. Cuando es así, la vista incluye datos para la conversión solo cuando los anuncios o las palabras clave de esos portafolios se incluyen en la vista.</li><li>Para las vistas predeterminadas, recomendamos que mantenga la regla de atribución predeterminada, que se usa para calcular el [valor objetivo](/help/search-social-commerce/glossary.md#o-p) (anteriormente denominado &quot;ingresos ponderados&quot;) para cada unidad de oferta durante la optimización de ofertas.</li></ul> |
|   | Conversiones basadas en | Cómo informar sobre los datos de conversión:<ul><li><i>Fecha de transacción</i> (valor predeterminado): para ver las transacciones cuya fecha de transacción se produjo durante el período de tiempo especificado. Indica cuántos ingresos se obtuvieron en el período de tiempo especificado.</li><li><i>Fecha de clic</i>: para ver las transacciones resultantes de un clic que se produjo durante el período de tiempo especificado. Cuando un portafolio tiene un retraso significativo entre clics y transacciones, esta opción es útil para calcular los ingresos históricos por clic del portafolio, lo que indica los comportamientos de ingresos que se esperan a lo largo del tiempo. |
