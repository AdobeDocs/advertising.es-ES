---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---
# Campo Títulos de publicidad en la configuración de anuncios RSA

**[!UICONTROL Ad Titles]:** Al menos tres y hasta quince títulos de anuncios (titulares), con pines de posición opcionales. La red de anuncios muestra anuncios con hasta tres titulares; escriba al menos tres. La longitud máxima de cada título es de 30 caracteres, incluido cualquier texto dinámico (como los valores de palabras clave y personalizadores de anuncios).

Para insertar un personalizador de anuncios, utilice los siguientes formatos, donde `Default text` es un valor opcional que se inserta cuando el archivo de fuente no incluye un valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Para anclar un título a una posición específica, seleccione la opción de anclaje (como &quot;[!UICONTROL Pinned at position 1]&quot;). Debe haber al menos un título disponible para cada posición. Si fija varios títulos a la misma posición, el anuncio final siempre incluirá uno de esos títulos en la posición especificada. Es posible que los títulos anclados a la posición 3 no se muestren con el anuncio.

Para añadir un título adicional, haga clic en **[!UICONTROL + Add]**.
