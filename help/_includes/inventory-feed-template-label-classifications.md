---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---
# Plantilla de anuncio de texto - Clasificaciones de etiquetas

**\[Componente\] [!UICONTROL Label Classifications] > \[Clasificación de etiquetas y valor\]:** (Opcional) Valores de hasta cinco clasificaciones de etiquetas existentes para asignarlas a los diferentes componentes de campaña creados o editados con la plantilla. Las entidades secundarias heredan los valores de etiquetas (incluidas las entidades secundarias que se crean posteriormente), por lo que no es necesario introducir valores para entidades secundarias a menos que desee anular los valores heredados. Las clasificaciones de etiquetas para los grupos de productos se aplican al nivel de unidad (más granular).

Para cada componente de campaña al que desea asignar clasificaciones de etiquetas:

1. Haga clic en la casilla de verificación situada junto a **\[Componente\][!UICONTROL Label Classifications]**.

1. Configure los valores de clasificación de etiquetas para la plantilla:

   * Para cada clasificación de etiqueta y valor que asignar al componente, haga lo siguiente:

      1. Haga clic **[!UICONTROL Add Label Classification]**.

      1. Seleccione la clasificación de etiquetas existente y, a continuación, seleccione un valor existente o introduzca un nuevo valor.

         La longitud máxima de cada valor es de 100 caracteres, y puede incluir caracteres ASCII y no ASCII.

         Para insertar un nombre de columna como parámetro dinámico para un valor de clasificación de etiqueta, haga clic en el campo de entrada (el segundo campo) y, a continuación, haga clic en un nombre de columna en la lista de columnas.

         Solo puede incluir un valor por clasificación por componente de campaña. Por ejemplo, una campaña puede tener Color=Rojo pero no Color=Rojo y Color=Azul.
   * Para cambiar un valor de clasificación de etiquetas existente, seleccione o introduzca un nuevo valor.

   * Para quitar un valor de clasificación de etiquetas existente, haga clic en **[!UICONTROL X]** junto al valor.
