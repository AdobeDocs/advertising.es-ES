---
title: Aplicar filtros de datos desde un menú de encabezado de columna
description: Obtenga información sobre cómo filtrar los datos de página desde el menú de encabezado de una columna.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Aplicar un filtro de datos desde un menú de encabezado de columna

Puede aplicar tantos filtros como desee a una columna, uno a la vez. Todos los filtros se unen mediante el operador AND. Para agregar más de un filtro a la vez utilizando todas las métricas disponibles, consulte &quot;[Aplicar filtros de datos de la barra de herramientas](column-filter-apply-from-toolbar.md)&quot;.

1. En el lado derecho del encabezado de la columna, haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flecha abajo") y, a continuación, haga clic en **[!UICONTROL Add Filter]**.

1. Defina el filtro en la columna:

   * (Filtros sin campos de entrada) Seleccione las casillas de verificación situadas junto a cada valor que desee incluir y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

   * (Filtros con campos de entrada) Seleccione un operador en el segundo menú, introduzca el valor aplicable y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

     Por ejemplo, si ha seleccionado la columna &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si filtra por campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.
     >* Solo puede aplicar un filtro numérico simple (como [!UICONTROL Impressions] \> 100) por columna.
