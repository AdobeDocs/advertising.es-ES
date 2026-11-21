---
title: Filtrar datos por intervalo de fechas
description: Aprenda a utilizar el filtro de intervalo de fechas global.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%
---
# Filtrar datos por intervalo de fechas

Utilice el filtro de intervalo de fechas para especificar el período durante el cual desea mostrar los datos de rendimiento. En las vistas que admiten la comparación de fechas, también puede comparar el rendimiento durante dos períodos.

## (Nueva IU) Cambiar el intervalo de fechas {#date-filter-new-ui}

1. En el encabezado de la página, haga clic en el control de intervalo de fechas con el icono de calendario.

1. Especifique el intervalo de fecha:

   * Para usar un intervalo preestablecido, seleccione una opción del menú situado encima del primer calendario, como **[!UICONTROL Yesterday]** o **[!UICONTROL Last 7 Days]**.

   * Para usar un intervalo personalizado, seleccione **[!UICONTROL Custom Date Range]** y las fechas de inicio y finalización en el calendario. Utilice las flechas del calendario para desplazarse entre meses.

1. Haga clic en **[!UICONTROL Apply]**.

## (Nueva interfaz de usuario) Comparar datos de dos períodos {#compare-periods-new-ui}

*Vistas que solo admiten comparación de fechas*

1. En el encabezado de la página, haga clic en el control de intervalo de fechas con el icono de calendario.

1. Activar **[!UICONTROL Compare Periods]**.

   Se muestran dos paneles de calendario en paralelo. El primer período tiene un marcador verde azulado y el período de comparación tiene un marcador morado.

1. En el primer panel, especifique el intervalo de fecha:

   * Para usar un intervalo preestablecido, seleccione una opción del menú situado encima del primer calendario, como **[!UICONTROL Yesterday]** o **[!UICONTROL Last 7 Days]**.

   * Para usar un intervalo personalizado, seleccione **[!UICONTROL Custom Date Range]** y las fechas de inicio y finalización en el calendario. Utilice las flechas del calendario para desplazarse entre meses.

1. En el segundo panel, seleccione un ajuste preestablecido de comparación o haga clic en una fecha de inicio en el calendario.

   El periodo de comparación tiene el mismo número de días que el primer periodo. Revise los intervalos de fechas completos por encima de ambos calendarios.

1. En **[!UICONTROL Comparison Format]**, seleccione cómo desea mostrar la diferencia:

   * **[!UICONTROL As percentage]:** Mostrar la diferencia como porcentaje.

   * **[!UICONTROL As variance]:** Mostrar la diferencia como valor numérico.

1. Haga clic en **[!UICONTROL Apply]**.

   El control de intervalo de fechas muestra tanto los intervalos de fechas completos con sus etiquetas de período como los marcadores de color. Cada métrica comparable se agrupa en dos columnas de período y una columna **[!UICONTROL Change]**. Los campos que no son comparables permanecen como columnas únicas. Los marcadores de punto de los encabezados de columna identifican los intervalos de fechas correspondientes.

Para detener la comparación de periodos, abra el control de intervalo de fechas, desactive **[!UICONTROL Compare Periods]** y haga clic en **[!UICONTROL Apply]**. Al desactivar la comparación, se borran los filtros según los datos de comparación.

### Cambiar el formato de comparación desde un menú de columna

1. Con la comparación de fechas habilitada, abra el menú de encabezado de columna de una columna **[!UICONTROL Change]** o cualquier columna de punto de una métrica comparable.

1. Seleccione **[!UICONTROL As percentage]** o **[!UICONTROL As variance]**.

   La selección se aplica a todas las métricas de comparación de la tabla de datos, no solo a la columna seleccionada. El control de intervalo de fechas se sincroniza con la selección y el formato se comparte en todas las páginas aplicables para el anunciante actual, incluidas las vistas con intervalos de fechas guardados.

   Aparecerá un mensaje de confirmación después de que la tabla de datos se actualice correctamente. Si la tabla de datos no se puede actualizar con el formato seleccionado, aparecerá un mensaje de error; intente seleccionar el formato de nuevo.

Las opciones de ordenación y filtrado siguen estando disponibles en los menús de columna donde se admiten.

## (IU heredada) Configuración del intervalo de fechas

El mismo filtro de intervalo de fechas global se aplica a la mayoría de las vistas de datos en todos los anunciantes, excepto en las vistas predeterminadas y personalizadas para las que ha guardado intervalos de fechas específicos. El intervalo de fechas predeterminado del sistema para las vistas de administración de campañas es &quot;Ayer&quot;.

La configuración del intervalo de fechas se guarda en una cookie específica del explorador, por lo que todos los cambios en el filtro de intervalo de fechas se utilizan para todos los anunciantes cada vez que inicia sesión con la misma aplicación de explorador hasta que cambia el filtro o elimina la cookie. Cada aplicación de explorador que utilice almacena la configuración del filtro de intervalo de fechas en una cookie diferente.

Cuando se guarda un intervalo de fechas específico para una vista predeterminada o personalizada, ese intervalo se aplica siempre que se aplica la vista, independientemente de la aplicación del explorador que se utilice.

>[!NOTE]
>
>* Puede ver los datos de los 13 meses anteriores, pero cualquier vista personalizada existente puede incluir datos de solo hasta los 180 días anteriores.
>* Para ver datos anteriores, vaya a la vista [[!UICONTROL Reports] ](/help/search-social-commerce/legacy-ui/reports/management/basic-advanced/basic-advanced-report-about.md) y ejecute un informe básico.
>* También puede guardar un intervalo de fechas para una [vista predeterminada o personalizada](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## (IU heredada) Cambiar el filtro de fecha global en las vistas de campaña

1. Sobre cualquier tabla de datos de Buscar \> Campañas \> Campañas, haga clic en el intervalo de fechas actual.

1. En el campo **[!UICONTROL Date Range]**, especifique el intervalo:

   * Para un rango preestablecido: seleccione en la lista de incrementos de tiempo comunes, que van desde *[!UICONTROL Today]* hasta *[!UICONTROL Last 180 Days]*. El valor predeterminado es *[!UICONTROL Yesterday]*.

   * Para un intervalo específico: seleccione **[!UICONTROL Custom Date Range]** y, a continuación, especifique la fecha de inicio y la fecha de finalización.

     Introduzca las fechas en formato MM/DD/AAAA o MM-DD-AAAA, o haga clic en ![Icono del calendario](/help/search-social-commerce/assets/calendar.png "Icono del calendario") junto a cada campo para abrir el calendario y seleccionar una fecha.

1. (Opcional) Compare los datos del intervalo de fechas especificado con los datos de un segundo intervalo de fechas:

   1. Mueva el control deslizante **[!UICONTROL Comparison]** a la posición &quot;Activado&quot;.

      Al seleccionar esta opción, se añaden dos columnas adicionales para cada columna de datos normal. Por ejemplo, en lugar de incluir una sola columna para &quot;[!UICONTROL Impressions]&quot;, la tabla incluye columnas para &quot;[!UICONTROL Impressions R1]&quot;, &quot;[!UICONTROL Impressions R2]&quot; y &quot;[!UICONTROL Impressions Diff]&quot;.&quot;  Si exporta los datos, las mismas columnas se escriben como &quot;[!UICONTROL Impressions Range 1]&quot;, &quot;[!UICONTROL Impressions Range 2]&quot; y &quot;[!UICONTROL Impressions Difference]&quot;.&quot;

   1. Especifique el segundo intervalo de fechas.

   1. Elija cómo expresar la diferencia entre los datos de los dos intervalos de fechas seleccionados en la columna &quot;\[_Campo de datos_\] Diferencia&quot;:

      * *[!UICONTROL Variance]* (valor predeterminado): muestra la diferencia como valor numérico.

      * *[!UICONTROL % Change]:* Muestra la diferencia como porcentaje.

1. Haga clic en **[!UICONTROL Apply]**.
