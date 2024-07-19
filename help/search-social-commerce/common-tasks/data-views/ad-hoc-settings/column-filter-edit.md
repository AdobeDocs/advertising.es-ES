---
title: Editar filtros de columna
description: Obtenga información sobre cómo editar filtros de columna.
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Editar filtros de columna

## Edición de un conjunto de filtros

1. Haga clic en ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro") en la barra de herramientas.

1. En la configuración del filtro, realice una de las acciones siguientes:

   * Para agregar un filtro, haga clic en ![Agregar filtro](/help/search-social-commerce/assets/add.png "Agregar filtro") **[!UICONTROL ADD FILTER]** y, a continuación, haga lo siguiente:

      1. (Opcional) Para filtrar los nombres de columna por cadena de texto, escriba la cadena de búsqueda en el campo de entrada **[!UICONTROL ADD FILTER]**.

      1. Seleccione un nombre de columna en el menú de columna.

      1. Defina el filtro en la columna:

         * (Filtros sin campos de entrada) Haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha abajo") junto al segundo menú, active las casillas de verificación situadas junto a cada valor que desee incluir y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

         * (Filtros con campos de entrada) Seleccione un operador en el segundo menú, introduzca el valor aplicable y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

           Por ejemplo, si ha seleccionado la columna &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada.

           Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, o *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

           **Nota:** Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si busca campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.

   * Para editar un filtro existente, haga clic en el filtro, cambie la definición del filtro y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

   * Para quitar un filtro existente, haga clic en **[!UICONTROL X]** junto a la definición del filtro.

1. ([!UICONTROL Keywords] solo vista; opcional) Seleccione o anule la selección de la configuración de &quot;[!UICONTROL Include rows with no performance data]&quot;.

   >[!WARNING]
   >
   >Al seleccionar esta opción, aumenta el tiempo de carga de la página.

1. Haga clic en **[!UICONTROL Apply]**.

## Editar un solo filtro

1. (Si es necesario) En el conjunto de filtros situado encima de la tabla de datos, haga clic en ![Más](/help/search-social-commerce/assets/more-filters.png "Más") para expandir el conjunto de filtros.

1. Sobre la tabla de datos, haga clic en la definición del filtro.

1. Edite los filtros que desee aplicar:

   1. (Opcional) Edite el nombre de la columna en el menú de columna.

   1. (Opcional) Redefina el filtro en la columna:

      * (Filtros sin campos de entrada) Haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha abajo") junto al segundo menú, active las casillas de verificación situadas junto a cada valor que desee incluir y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

      * (Filtros con campos de entrada) Seleccione un operador en el segundo menú, introduzca el valor aplicable y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

        Por ejemplo, si ha seleccionado la columna &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada

        Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *menor que*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *no contiene* o *comienza con.*

        **Nota:** Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si busca campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.
