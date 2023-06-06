---
title: Filtrar datos por intervalo de fechas
description: Aprenda a utilizar el filtro de intervalo de fechas global.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Filtrar datos por intervalo de fechas

El mismo filtro de intervalo de fechas global se aplica a la mayoría de las vistas de datos de campaña, en todos los anunciantes, excepto en las vistas predeterminadas y personalizadas para las que ha guardado intervalos de fechas específicos. El intervalo de fechas predeterminado del sistema para las vistas de administración de campañas es &quot;Ayer&quot;.

La configuración del intervalo de fechas se guarda en una cookie específica del explorador, por lo que todos los cambios en el filtro de intervalo de fechas se utilizan para todos los anunciantes cada vez que inicia sesión con la misma aplicación de explorador hasta que cambia el filtro o elimina la cookie. Cada aplicación de explorador que utilice almacenará la configuración del filtro de intervalo de fechas en una cookie diferente.

Cuando se guarda un intervalo de fechas específico para una vista predeterminada o personalizada, ese intervalo se aplica siempre que se aplica la vista, independientemente de la aplicación del explorador que se utilice.

>[!NOTE]
>
>* Puede ver los datos de los 13 meses anteriores, pero cualquier vista personalizada existente puede incluir datos de solo hasta los 180 días anteriores.
>* Para ver datos anteriores, vaya a [[!UICONTROL Reports] vista](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) y ejecutar un informe básico.
>* También puede guardar un intervalo de fecha para una [vista predeterminada o vista personalizada](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).


## Cambio del filtro de fecha global en las vistas de campaña

1. Sobre cualquier tabla de datos de Buscar \> Campañas \> Campañas, haga clic en el intervalo de fechas actual.

1. En el **[!UICONTROL Date Range]** , especifique el rango:

   * Para un rango preestablecido: seleccione en la lista de incrementos de tiempo comunes, que van desde *[!UICONTROL Today]* hasta *[!UICONTROL Last 180 Days]*. El valor predeterminado es *[!UICONTROL Yesterday]*.

   * Para un rango específico: seleccione **[!UICONTROL Custom Date Range]** y, a continuación, especifique la fecha inicial y la fecha final.

      Introduzca las fechas en formato MM/DD/AAAA o MM-DD-AAAA, o haga clic en ![Icono de calendario](/help/search-social-commerce/assets/calendar.png "Icono de calendario") junto a cada campo para abrir el calendario y seleccionar una fecha.

1. (Opcional) Compare los datos del intervalo de fechas especificado con los datos de un segundo intervalo de fechas:

   1. Mover el **[!UICONTROL Comparison]** deslizador a *[!UICONTROL On]*.

      Al seleccionar esta opción, se añaden dos columnas adicionales para cada columna de datos normal. Por ejemplo, en lugar de incluir solo una columna para &quot;[!UICONTROL Impressions],&quot; la tabla incluye columnas para &quot;[!UICONTROL Impressions R1],&quot; &quot;[!UICONTROL Impressions R2],&quot; y &quot;[!UICONTROL Impressions Diff].&quot;  Si exporta los datos, las mismas columnas se deletrean como &quot;[!UICONTROL Impressions Range 1],&quot; &quot;[!UICONTROL Impressions Range 2],&quot; y &quot;[!UICONTROL Impressions Difference].&quot;

   1. Especifique el segundo intervalo de fechas.

   1. Elija cómo expresar la diferencia entre los datos de los dos intervalos de fechas seleccionados en la &quot;\[_Campo de datos_\] Diferencia&quot;:

      * *[!UICONTROL Variance]* (el valor predeterminado): Muestra la diferencia como valor numérico.

      * *[!UICONTROL % Change]:*  Muestra la diferencia en forma de porcentaje.

1. Haga clic **[!UICONTROL Apply]**.
