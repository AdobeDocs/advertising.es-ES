---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Mostrar la ruta 1 y la ruta 2 en algunos ajustes de publicidad

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (opcional) Texto que se agrega a la dirección URL para mostrar que se extrae automáticamente de la dirección URL final. Cada ruta de acceso está precedida en la dirección URL por una barra diagonal (`/`). Una ruta de acceso no puede contener caracteres de barra diagonal (`/`) o de nueva línea (`\n`). La longitud máxima de cada ruta es de 15 caracteres o 7 caracteres de doble byte.

Para insertar un personalizador de anuncios, use los siguientes formatos, donde `Default text` es un valor opcional que se debe insertar cuando el archivo de fuente no incluye un valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Por ejemplo, si [!UICONTROL Display Path 1] es &quot;ofertas&quot; y [!UICONTROL Display Path 2] es &quot;local&quot;, la dirección URL para mostrar sería `<display URL>/deals/local`, como www.example.com/deals/local.
