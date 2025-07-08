---
title: Editar filtros de columna
description: Obtenga información sobre cómo editar filtros de columna.
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Editar filtros de columna

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

## (Nueva IU) Editar un conjunto de filtros en una vista de administración

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

## (IU heredada) Editar un conjunto de filtros en una vista de administración de campañas

1. Haga clic en ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro") en la barra de herramientas.

1. En la configuración del filtro, realice una de las acciones siguientes:

   * Para agregar un filtro, haga clic en ![Agregar filtro](/help/search-social-commerce/assets/add.png "Agregar filtro") **[!UICONTROL ADD FILTER]** y, a continuación, haga lo siguiente:

      1. (Opcional) Para filtrar los nombres de columna por cadena de texto, escriba la cadena de búsqueda en el campo de entrada **[!UICONTROL ADD FILTER]**.

      1. Seleccione un nombre de columna en el menú de columna.

      1. Defina el filtro en la columna:

         * (Filtros sin campos de entrada) Haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha abajo") junto al segundo menú y, a continuación, active las casillas de verificación situadas junto a cada valor que desee incluir.

         * (Filtros con campos de entrada) Seleccione un operador en el segundo menú y, a continuación, introduzca el valor aplicable.

           Por ejemplo, si ha seleccionado la columna &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada.

           Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, o *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

           **Nota:** Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si busca campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.

   * Para editar un filtro existente, haga clic en él y cambie la definición del filtro.

   * Para quitar un filtro existente, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto a la definición del filtro.

1. ([!UICONTROL Keywords] solo vista; opcional) Seleccione o anule la selección de la configuración de &quot;[!UICONTROL Include rows with no performance data]&quot;.

   >[!WARNING]
   >
   >Al seleccionar esta opción, aumenta el tiempo de carga de la página.

1. Haga clic en **[!UICONTROL Apply]**.

## Edición de un solo filtro en una vista de administración

1. Sobre la tabla de datos, haga clic en la definición del filtro.

1. Redefina el filtro en la columna:

   * (Filtros sin campos de entrada) Haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha abajo") junto al segundo menú y active las casillas de verificación situadas junto a cada valor que desee incluir.

   * (Filtros con campos de entrada) Seleccione un operador en el segundo menú y, a continuación, introduzca el valor aplicable.

     Por ejemplo, si ha seleccionado la columna &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada.

     Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *menor que*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *no contiene* o *comienza con.*

     **Nota:** Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si busca campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.

>[!MORELIKETHIS]
>
>* [Aplicar un filtro de datos desde un menú de encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [Aplicar filtros de datos de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [Quitar un filtro de columna]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
