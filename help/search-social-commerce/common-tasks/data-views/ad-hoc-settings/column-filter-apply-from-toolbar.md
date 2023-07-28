---
title: Aplicación de filtros de datos desde la barra de herramientas
description: Obtenga información sobre cómo filtrar los datos de página desde la barra de herramientas.
exl-id: 922cc148-e6dc-428b-a7f3-1da3780df326
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Aplicación de filtros de datos desde la barra de herramientas

Puede aplicar tantos filtros como desee a una vista. Todos los filtros se unen mediante el operador AND.

1. En la barra de herramientas, haga clic en ![Filtrar](/help/search-social-commerce/assets/filter.png "Filtrar").

1. En la configuración del filtro, realice una de las acciones siguientes:

   * Para añadir un filtro, haga clic en ![Añadir filtro](/help/search-social-commerce/assets/add.png "Añadir filtro") **[!UICONTROL ADD FILTER]** y, a continuación, haga lo siguiente:

      1. (Opcional) Para filtrar los nombres de columna por cadena de texto, introduzca la cadena de búsqueda en la variable **[!UICONTROL ADD FILTER]** campo de entrada.

      1. Seleccione un nombre de columna en el menú de columna.

      1. Defina el filtro en la columna:

         * (Filtros sin campos de entrada) Haga clic en ![Flecha hacia abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha hacia abajo") situado junto al segundo menú y, a continuación, active las casillas de verificación situadas junto a cada valor que desee incluir.

         * (Filtros con campos de entrada) Seleccione un operador en el segundo menú y, a continuación, introduzca el valor aplicable.

           Por ejemplo, si ha seleccionado la opción &quot;[!UICONTROL Clicks]&quot; y desea devolver solo filas con más de 100 clics, luego seleccione *[!UICONTROL greater than]*&quot; e introduzca `100` en el campo de entrada.

           Según el tipo de datos, los operadores disponibles pueden incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, o *[!UICONTROL no date].*

           **Nota:** Los valores de texto no distinguen entre mayúsculas y minúsculas. Por ejemplo, si filtra por campañas con &quot;préstamo&quot; en el nombre, los resultados incluyen &quot;Préstamos al consumidor&quot; y &quot;solicitudes de préstamo&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements], y [!UICONTROL Auto Targets] solo vistas; opcional) Cambie el valor a &quot;[!UICONTROL Include rows with performance data only].&quot;

           **Advertencia:** Si anula la selección de la opción y la vista incluye muchas entidades sin datos de rendimiento, los datos tardan más en mostrarse.

   * Para editar un filtro existente, haga clic en el filtro, cambie la definición del filtro y, a continuación, haga clic en ![Actualizar filtro](/help/search-social-commerce/assets/select.png "Actualizar filtro").

   * Para eliminar un filtro existente, haga clic en **[!UICONTROL X]** junto a la definición del filtro.

1. Haga clic **[!UICONTROL Apply]**.
