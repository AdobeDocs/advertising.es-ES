---
title: Aplicar filtros de datos desde un menú de encabezado de columna
description: Obtenga información sobre cómo filtrar los datos de página desde el menú de encabezado de una columna.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Aplicar un filtro de datos desde un menú de encabezado de columna

<!-- The same in new UI and legacy CM views -->

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

Puede aplicar tantos filtros como desee a una columna, uno a la vez.<!-- True only for entity names, I think: All filters are joined using the AND operator. --> Para agregar más de un filtro a la vez usando todas las métricas disponibles, consulte &quot;[Aplicar filtros de datos de la barra de herramientas](column-filter-apply-from-toolbar.md)&quot;.

1. En el lado derecho del encabezado de la columna, haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flecha abajo") y, a continuación, haga clic en **[!UICONTROL Add Filter]**.

1. Defina el filtro en la columna:

   * (Filtros sin campos de entrada) Seleccione las casillas de verificación situadas junto a cada valor que desee incluir y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Agregar").

   * (Filtros con campos de entrada) Seleccione un operador en el segundo menú, escriba el valor aplicable y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Agregar").

     Por ejemplo, si ha seleccionado la columna &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si filtra por campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.
     >* Solo puede aplicar un filtro numérico simple (como [!UICONTROL Impressions] \> 100) por columna.

>[!MORELIKETHIS]
>
>* [Aplicar filtros de datos de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [Editar filtros de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [Quitar un filtro de columna]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
