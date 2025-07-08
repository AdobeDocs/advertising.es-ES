---
title: Configuración de métricas personalizadas
description: Haga referencia a la configuración de las métricas personalizadas, que se calculan a partir de las métricas estándar.
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Configuración de métricas personalizadas

La configuración de métricas personalizadas es ligeramente diferente en diferentes partes de la interfaz.

## Configuración de métricas personalizadas en la mayoría de las vistas de administración

| Parámetro/Sección | Descripción |
|----|----|
| Nombre de métrica personalizada | El nombre de la métrica, que aparece como el nombre de la columna. <b>Sugerencia:</b> Use un nombre de métrica significativo, pero tenga en cuenta que los nombres más largos hacen que la columna sea más ancha. |
| Insertar métrica | La fórmula matemática utilizada para calcular la nueva métrica (como [Costo]/[Registros]:<ul><li>Para insertar una métrica de la lista de métricas de tráfico e ingresos, coloque el cursor donde desee insertar la métrica y, a continuación, selecciónela en la lista o introdúzcala manualmente entre corchetes (por ejemplo, `[CPC]`).</li><li>Para insertar un operador, coloque el cursor donde desee insertar el operador y, a continuación, haga clic en el botón o escriba el símbolo manualmente. Los operadores matemáticos disponibles: `+ - * / ( ) ()`</li></ul><b>Nota:</b> Las métricas personalizadas complejas tardan más en calcularse, y los informes y vistas que las incluyen (especialmente cuando incluyen columnas independientes para conversiones de clics y visualizaciones) tardan más en generarse. |
| Formato | Cómo presentar los datos de esta métrica: *[!UICONTROL Currency]* (un valor monetario), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* o *[!UICONTROL Percentage]* (un porcentaje con dos decimales).<br><br><b>Precaución:</b> Si crea una métrica derivada con el formato [!UICONTROL Number w/out Decimal Points] (que muestra los datos como enteros) y la incluye en una vista o en un informe que usa una regla de atribución de conversión ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] o [!UICONTROL Even Distribution]), el resultado se mostrará en números enteros, no en decimales. Como resultado, los campos de datos individuales pueden ser incorrectos, aunque los totales sean correctos. Por ejemplo, si un pedido se divide a partes iguales entre tres eventos, se atribuye a cada uno de los tres eventos un pedido (en lugar de un pedido de 0,33). Para evitar el problema, use el formato de métrica [!UICONTROL Number to 2 Decimal Points]. |

## Configuración de métricas personalizadas en informes y plantillas de informes y en las vistas heredadas de [!UICONTROL Portfolios]

| Parámetro/Sección | Descripción |
|----|----|
| Nombre de métrica personalizada | El nombre de la métrica, que aparece como el nombre de la columna. <b>Sugerencia:</b> Use un nombre de métrica significativo, pero tenga en cuenta que los nombres más largos hacen que la columna sea más ancha. |
| Formato | Cómo presentar los datos de esta métrica: *[!UICONTROL Currency]* (un valor monetario), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* o *[!UICONTROL Percentage]* (un porcentaje con dos decimales).<br><br><b>Precaución:</b> Si crea una métrica derivada con el formato [!UICONTROL Number w/out Decimal Points] (que muestra los datos como enteros) y la incluye en una vista o en un informe que usa una regla de atribución de conversión ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] o [!UICONTROL Even Distribution]), el resultado se mostrará en números enteros, no en decimales. Como resultado, los campos de datos individuales pueden ser incorrectos, aunque los totales sean correctos. Por ejemplo, si un pedido se divide a partes iguales entre tres eventos, se atribuye a cada uno de los tres eventos un pedido (en lugar de un pedido de 0,33). Para evitar el problema, use el formato de métrica [!UICONTROL Number to 2 Decimal Points]. |
| Insertar métrica | Una lista de métricas existentes a partir de la cual puede crear una fórmula.<br><br>Para insertar una métrica en el campo de entrada de fórmula, coloque el cursor donde desee insertar la métrica y, a continuación, seleccione la métrica en la lista o escríbala manualmente y encerrada entre corchetes (por ejemplo, `[CPC]`). |
| Insertar operador | Operadores matemáticos disponibles: `+ - x / ( )`<br><br>Para insertar un operador en el campo de entrada de fórmula, coloque el cursor donde desee insertar el operador y, a continuación, haga clic en el botón o escriba el símbolo manualmente. |
| [Campo de entrada de fórmula para la métrica] | La fórmula matemática utilizada para calcular la nueva métrica se basa en una o más propiedades existentes o métricas estándar (como `[Cost]/[Registrations]`). Puede incluir cualquier combinación de métricas y operadores.<br><br><b>Nota:</b> Las métricas personalizadas complejas tardan más en calcularse, y los informes y vistas que las incluyen (especialmente cuando incluyen columnas independientes para conversiones de clics y visualizaciones) tardan más en generarse. |

>[!MORELIKETHIS]
>
>* [Acerca de las métricas personalizadas](custom-metric-about.md)
>* [Crear una métrica personalizada](custom-metric-create.md)
>* [Editar una métrica personalizada](custom-metric-edit.md)
>* [Eliminar una métrica personalizada](custom-metric-delete.md)
