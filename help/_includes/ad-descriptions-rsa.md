---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---
# Campo Descripciones de anuncio en la configuración de anuncios RSA

**[!UICONTROL Ad Descriptions]:** Al menos dos y hasta cuatro descripciones de anuncios con clavijas de posición opcionales. La red de anuncios muestra anuncios con hasta dos descripciones; escriba al menos dos. La longitud máxima de cada descripción es de 90 caracteres, incluido cualquier texto dinámico (como los valores de palabras clave y personalizadores de anuncios).

Para insertar un personalizador de anuncios, use los siguientes formatos, donde `Default text` es un valor opcional que se debe insertar cuando el archivo de fuente no incluye un valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Para anclar una descripción a una posición específica, seleccione la opción de anclaje (como &quot;[!UICONTROL Pinned at position 1]&quot;). Debe haber al menos una descripción disponible para cada posición. Si fija varias descripciones en la misma posición, el anuncio final siempre incluirá una de esas descripciones en la posición especificada. Las descripciones ancladas a la posición 2 pueden no mostrarse con el anuncio.

Para agregar una descripción adicional, haga clic en **[!UICONTROL + Add]**.
