---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---
# Mostrar la ruta 1 y la ruta 2 en algunos ajustes de publicidad

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Opcional) Texto que se añade a la dirección URL para mostrar que se extrae automáticamente de la dirección URL final. Cada ruta va precedida en la dirección URL por una barra diagonal (`/`). Una ruta no puede contener una barra diagonal (`/`) o nueva línea (`\n`) caracteres. La longitud máxima de cada ruta es de 15 caracteres o 7 caracteres de doble byte.

Para insertar un personalizador de anuncios, utilice los siguientes formatos, donde `Default text` es un valor opcional que se inserta cuando el archivo de fuente no incluye un valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Por ejemplo, si la Ruta de visualización 1 es &quot;ofertas&quot; y la Ruta de visualización 2 es &quot;local&quot;, la URL de visualización sería `<display URL>/deals/local`, como www.example.com/deals/local.
