---
title: Aplicación de filtros de datos desde la barra de herramientas
description: Obtenga información sobre cómo filtrar los datos de página desde la barra de herramientas.
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Aplicación de filtros de datos desde la barra de herramientas

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

Puede aplicar todos los filtros que desee a una vista.<!-- True only for entity names, I think: All filters are joined using the AND operator. -->

## (Nueva IU) Aplicar filtros de datos de la barra de herramientas en las vistas de administración

1. En la barra de herramientas, haga clic en ![Filtro](/help/search-social-commerce/assets/filter-new.png "Filtro").

1. En la configuración del filtro, realice una de las acciones siguientes:

   * Para agregar un filtro, haga clic en **[!UICONTROL ADD FILTER]** y, a continuación, haga lo siguiente:

      1. (Opcional) Para filtrar los nombres de columna por cadena de texto, escriba la cadena de búsqueda en el campo de entrada **[!UICONTROL ADD FILTER]**.

      1. Seleccione un nombre de columna en el menú de columna.

      1. Defina el filtro en la columna:

         * (Filtros sin campos de entrada) Haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha abajo") junto al segundo menú y, a continuación, active las casillas de verificación situadas junto a cada valor que desee incluir.

         * (Filtros con campos de entrada) Seleccione un operador en el segundo menú y, a continuación, introduzca el valor aplicable.

           Por ejemplo, si ha seleccionado la columna &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada.

           Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

           **Nota:** Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si filtra por campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.

   * Para editar un filtro existente, haga clic en él y cambie la definición del filtro.

   * Para quitar un filtro existente, haga clic en **[!UICONTROL -]** junto a la definición del filtro.

## (IU heredada) Aplicar filtros de datos de la barra de herramientas en una vista de administración de campañas

1. En la barra de herramientas, haga clic en ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro").

1. En la configuración del filtro, realice una de las acciones siguientes:

   * Para agregar un filtro, haga clic en ![Agregar filtro](/help/search-social-commerce/assets/add.png "Agregar filtro") **[!UICONTROL ADD FILTER]** y, a continuación, haga lo siguiente:

      1. (Opcional) Para filtrar los nombres de columna por cadena de texto, escriba la cadena de búsqueda en el campo de entrada **[!UICONTROL ADD FILTER]**.

      1. Seleccione un nombre de columna en el menú de columna.

      1. Defina el filtro en la columna:

         * (Filtros sin campos de entrada) Haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha abajo") junto al segundo menú y, a continuación, active las casillas de verificación situadas junto a cada valor que desee incluir.

         * (Filtros con campos de entrada) Seleccione un operador en el segundo menú y, a continuación, introduzca el valor aplicable.

           Por ejemplo, si ha seleccionado la columna &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada.

           Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

           **Nota:** Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si filtra por campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements] y [!UICONTROL Auto Targets] solo vistas; opcional) Cambie el valor a &quot;[!UICONTROL Include rows with performance data only]&quot;.

           **Advertencia:** Si anula la selección de la opción y la vista incluye muchas entidades sin datos de rendimiento, los datos tardarán más en mostrarse.

   * Para editar un filtro existente, haga clic en él y cambie la definición del filtro.

   * Para quitar un filtro existente, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto a la definición del filtro.

1. Haga clic en **[!UICONTROL Apply]**.

>[!MORELIKETHIS]
>
>* [Aplicar un filtro de datos desde un menú de encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [Editar filtros de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [Quitar un filtro de columna]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
