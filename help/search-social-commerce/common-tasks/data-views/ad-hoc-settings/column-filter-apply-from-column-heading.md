---
title: Aplicar filtros de datos desde un menú de encabezado de columna
description: Obtenga información sobre cómo filtrar los datos de página desde el menú de encabezado de una columna.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Aplicar un filtro de datos desde un menú de encabezado de columna

Puede aplicar tantos filtros como desee a una columna, uno a la vez. Todos los filtros se unen mediante el operador AND. Para agregar más de un filtro a la vez utilizando todas las métricas disponibles, consulte[Aplicación de filtros de datos desde la barra de herramientas](column-filter-apply-from-toolbar.md).&quot;

1. En el lado derecho del encabezado de la columna, haga clic en ![Flecha hacia abajo](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flecha hacia abajo")y haga clic en **[!UICONTROL Add Filter]**.

1. Defina el filtro en la columna:

   * (Filtros sin campos de entrada) Seleccione las casillas de verificación situadas junto a cada valor que desee incluir y haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

   * (Filtros con campos de entrada) Seleccione un operador en el segundo menú, introduzca el valor aplicable y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

      Por ejemplo, si ha seleccionado la opción &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, luego seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, o *[!UICONTROL no date].*

      >[!NOTE]
      >
      >* Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si filtra por campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.
      >* Solo se puede aplicar un filtro numérico simple (por ejemplo, [!UICONTROL Impressions] \> 100) por columna.

