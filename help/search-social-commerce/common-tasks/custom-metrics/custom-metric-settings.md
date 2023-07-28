---
title: Configuración de métricas personalizadas
description: Haga referencia a la configuración de las métricas personalizadas, que se calculan a partir de las métricas estándar.
exl-id: f4b8c44e-ecb3-46dc-9a68-c079188e1d75
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Configuración de métricas personalizadas

La configuración de métricas personalizadas es ligeramente diferente en diferentes partes de la interfaz.

## Configuración de métricas personalizadas en las vistas de administración de campañas

| Parámetro/Sección | Descripción |
|----|----|
| Nombre de métrica personalizada | El nombre de la métrica, que aparece como el nombre de la columna. <b>Sugerencia:</b> Utilice un nombre de métrica significativo, pero tenga en cuenta que los nombres más largos hacen que la columna sea más ancha. |
| Insertar métrica | La fórmula matemática utilizada para calcular la nueva métrica (como [Coste]/[Registros]:<ul><li>Para insertar una métrica desde la lista de métricas de tráfico e ingresos, coloque el cursor donde desee insertar la métrica y, a continuación, selecciónela en la lista o introdúzcala manualmente entre corchetes (por ejemplo, `[CPC]`).</li><li>Para insertar un operador, coloque el cursor donde desee insertar el operador y, a continuación, haga clic en el botón o escriba el símbolo manualmente. Los operadores matemáticos disponibles: `+ - * / ( ) ()`</li></ul><b>Nota:</b> Las métricas personalizadas complejas tardan más en calcularse y los informes y las vistas que los incluyen, especialmente cuando incluyen columnas independientes para conversiones de clics y visualizaciones, tardan más en generarse. |
| Formato | Presentación de los datos de esta métrica: *[!UICONTROL Currency]* (un valor monetario), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, o *[!UICONTROL Percentage]* (un porcentaje con dos decimales).<br><br><b>Precaución:</b> Si crea una métrica derivada con el formato [!UICONTROL Number w/out Decimal Points] (que muestra los datos como números enteros) y se incluyen en una vista o un informe que usa una regla de atribución de conversión ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], o [!UICONTROL Even Distribution]), el resultado se mostrará en números enteros, no en decimales. Como resultado, los campos de datos individuales pueden ser incorrectos, aunque los totales sean correctos. Por ejemplo, si un pedido se divide a partes iguales entre tres eventos, se atribuye a cada uno de los tres eventos un pedido (en lugar de un pedido de 0,33). Para evitar el problema, utilice el formato de métrica [!UICONTROL Number to 2 Decimal Points]. |

## Configuración de métricas personalizada en informes y plantillas de informes y en la [!UICONTROL Portfolios] vistas

| Parámetro/Sección | Descripción |
|----|----|
| Nombre de métrica personalizada | El nombre de la métrica, que aparece como el nombre de la columna. <b>Sugerencia:</b> Utilice un nombre de métrica significativo, pero tenga en cuenta que los nombres más largos hacen que la columna sea más ancha. |
| Formato | Presentación de los datos de esta métrica: *[!UICONTROL Currency]* (un valor monetario), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, o *[!UICONTROL Percentage]* (un porcentaje con dos decimales).<br><br><b>Precaución:</b> Si crea una métrica derivada con el formato [!UICONTROL Number w/out Decimal Points] (que muestra los datos como números enteros) y se incluyen en una vista o un informe que usa una regla de atribución de conversión ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], o [!UICONTROL Even Distribution]), el resultado se mostrará en números enteros, no en decimales. Como resultado, los campos de datos individuales pueden ser incorrectos, aunque los totales sean correctos. Por ejemplo, si un pedido se divide a partes iguales entre tres eventos, se atribuye a cada uno de los tres eventos un pedido (en lugar de un pedido de 0,33). Para evitar el problema, utilice el formato de métrica [!UICONTROL Number to 2 Decimal Points]. |
| Insertar métrica | Una lista de métricas existentes a partir de la cual puede crear una fórmula.<br><br>Para insertar una métrica en el campo de entrada de la fórmula, coloque el cursor donde desee insertar la métrica y, a continuación, seleccione la métrica en la lista o introdúzcala manualmente entre corchetes (por ejemplo, `[CPC]`). |
| Insertar operador | Los operadores matemáticos disponibles: `+ - x / ( )`<br><br>Para insertar un operador en el campo de entrada de la fórmula, coloque el cursor donde desee insertar el operador y, a continuación, haga clic en el botón o escriba el símbolo manualmente. |
| [Campo de entrada de fórmula para la métrica] | La fórmula matemática utilizada para calcular la nueva métrica se basa en una o más propiedades existentes o métricas estándar (como `[Cost]/[Registrations]`. Puede incluir cualquier combinación de métricas y operadores.<br><br><b>Nota:</b> Las métricas personalizadas complejas tardan más en calcularse y los informes y las vistas que los incluyen, especialmente cuando incluyen columnas independientes para conversiones de clics y visualizaciones, tardan más en generarse. |

>[!MORELIKETHIS]
>
>* [Acerca de las métricas personalizadas](custom-metric-about.md)
>* [Creación de una métrica personalizada](custom-metric-create.md)
>* [Editar una métrica personalizada](custom-metric-edit.md)
>* [Eliminar una métrica personalizada](custom-metric-delete.md)
