---
title: Filtrar datos por intervalo de fechas
description: Aprenda a utilizar el filtro de intervalo de fechas global.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Filtrar datos por intervalo de fechas

El mismo filtro de intervalo de fechas global se aplica a la mayoría de las vistas de datos de campaña, en todos los anunciantes, excepto en las vistas predeterminadas y personalizadas para las que ha guardado intervalos de fechas específicos. El intervalo de fechas predeterminado del sistema para las vistas de administración de campañas es &quot;Ayer&quot;.

La configuración del intervalo de fechas se guarda en una cookie específica del explorador, por lo que todos los cambios en el filtro de intervalo de fechas se utilizan para todos los anunciantes cada vez que inicia sesión con la misma aplicación de explorador hasta que cambia el filtro o elimina la cookie. Cada aplicación de explorador que utilice almacena la configuración del filtro de intervalo de fechas en una cookie diferente.

Cuando se guarda un intervalo de fechas específico para una vista predeterminada o personalizada, ese intervalo se aplica siempre que se aplica la vista, independientemente de la aplicación del explorador que se utilice.

>[!NOTE]
>
>* Puede ver los datos de los 13 meses anteriores, pero cualquier vista personalizada existente puede incluir datos de solo hasta los 180 días anteriores.
>* Para ver datos anteriores, vaya a la vista [[!UICONTROL Reports] ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) y ejecute un informe básico.
>* También puede guardar un intervalo de fechas para una [vista predeterminada o personalizada](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Cambio del filtro de fecha global en las vistas de campaña

1. Sobre cualquier tabla de datos de Buscar \> Campañas \> Campañas, haga clic en el intervalo de fechas actual.

1. En el campo **[!UICONTROL Date Range]**, especifique el intervalo:

   * Para un rango preestablecido: seleccione en la lista de incrementos de tiempo comunes, que van desde *[!UICONTROL Today]* hasta *[!UICONTROL Last 180 Days]*. El valor predeterminado es *[!UICONTROL Yesterday]*.

   * Para un intervalo específico: seleccione **[!UICONTROL Custom Date Range]** y, a continuación, especifique la fecha de inicio y la fecha de finalización.

     Introduzca las fechas en formato MM/DD/AAAA o MM-DD-AAAA, o haga clic en ![Icono del calendario](/help/search-social-commerce/assets/calendar.png "Icono del calendario") junto a cada campo para abrir el calendario y seleccionar una fecha.

1. (Opcional) Compare los datos del intervalo de fechas especificado con los datos de un segundo intervalo de fechas:

   1. Mover el control deslizante **[!UICONTROL Comparison]** a *[!UICONTROL On]*.

      Al seleccionar esta opción, se añaden dos columnas adicionales para cada columna de datos normal. Por ejemplo, en lugar de incluir una sola columna para &quot;[!UICONTROL Impressions]&quot;, la tabla incluye columnas para &quot;[!UICONTROL Impressions R1]&quot;, &quot;[!UICONTROL Impressions R2]&quot; y &quot;[!UICONTROL Impressions Diff]&quot;.&quot;  Si exporta los datos, las mismas columnas se escriben como &quot;[!UICONTROL Impressions Range 1]&quot;, &quot;[!UICONTROL Impressions Range 2]&quot; y &quot;[!UICONTROL Impressions Difference]&quot;.&quot;

   1. Especifique el segundo intervalo de fechas.

   1. Elija cómo expresar la diferencia entre los datos de los dos intervalos de fechas seleccionados en la columna &quot;\[_Campo de datos_\] Diferencia&quot;:

      * *[!UICONTROL Variance]* (valor predeterminado): muestra la diferencia como valor numérico.

      * *[!UICONTROL % Change]:* Muestra la diferencia como porcentaje.

1. Haga clic en **[!UICONTROL Apply]**.
