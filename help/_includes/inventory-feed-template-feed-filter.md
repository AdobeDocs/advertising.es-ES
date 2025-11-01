---
source-git-commit: 73c9cc7134360e073fc466dda3733cfc9bac8786
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Plantilla de anuncio de texto: filtro de fuente

**\[Filtro de fuente\]:** Qué filas del archivo de fuente se propagarán:

* *[!UICONTROL Propagate all rows found in feed:]* (valor predeterminado) Para propagar los datos de todas las filas.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Para propagar datos sólo para filas que cumplan hasta diez condiciones especificadas. Especifique los filtros que desea aplicar:

   1. Seleccione la operación booleana que se usará para todos los filtros: **[!UICONTROL AND]** o **[!UICONTROL OR]**.

   1. Seleccione un nombre de columna en el primer menú, seleccione un operador en el segundo menú y, a continuación, introduzca los valores aplicables o deje el campo de entrada en blanco para propagar los datos de las filas sin condiciones.

  La lista de columnas incluye todas las columnas disponibles en la fuente.

  Los operadores disponibles incluyen *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (no es igual a), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]* y *[!UICONTROL greater than]*. Al seleccionar el operador &quot;[!UICONTROL in]&quot;, puede introducir una lista de valores separados por comas; si un registro coincide con cualquiera de los valores especificados, los datos se propagan para esas filas. Para el resto de operadores, introduzca solo un valor. Los valores no distinguen entre mayúsculas y minúsculas.

  Por ejemplo, si selecciona la columna &quot;product_type&quot; y desea devolver solo filas para nombres de productos que contengan &quot;zapatos&quot;, seleccione &quot;**[!UICONTROL contains]**&quot; e introduzca `shoes` en el campo de entrada.

   1. (Para aplicar hasta nueve filtros adicionales) Para cada filtro adicional, haga clic en **[!UICONTROL Add Condition]** y, a continuación, especifique el filtro adicional para el paso 2.
