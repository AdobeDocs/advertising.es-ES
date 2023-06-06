---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Plantilla de anuncio de texto: configuración de palabras clave negativas en el nivel de campaña

**[!UICONTROL Delete negative keywords when omitted from list]:** (Todas las redes de anuncios excepto Yandex; opcional) Elimina las palabras clave negativas existentes a nivel de campaña creadas anteriormente con la plantilla que no se especifican en las listas siguientes. **Nota:** Palabras clave negativas creadas por otros medios (como en hojas de edición masiva simples, [!UICONTROL Campaigns] Las vistas de o en el editor de anuncios de la red de publicidad nunca se eliminan mediante la plantilla de.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Todas las redes de anuncios excepto Yandex; opcional) Permite especificar palabras clave negativas para campañas cuyo nombre incluye una cadena especificada. Al seleccionar esta opción, puede añadir hasta tres cadenas de nombre de campaña y las palabras clave correspondientes.

Haga clic en cada cadena **[!UICONTROL Add (Up to 3)]** e introduzca la siguiente información:

* **[!UICONTROL If campaign name contains]:**  Una cadena de texto para buscar en cualquier lugar dentro del nombre de la campaña. La consulta distingue entre mayúsculas y minúsculas (por ejemplo, &quot;[!DNL Car]&quot; coincide con el nombre de la campaña &quot;[!DNL Car Parts]&quot; pero no &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;).

* **[!UICONTROL Apply these negatives]:**  Cualquier palabra clave negativa estática en el nivel de campaña que se agregue a las campañas cuyo nombre incluya la cadena especificada. Para especificar varias palabras clave o varios tipos de coincidencia para la misma palabra clave, escríbalas en líneas independientes. Utilice la siguiente sintaxis, sin un signo menos:

   * Coincidencia amplia negativa: `keyword` (no compatible con [!DNL Microsoft Advertising])
   * Coincidencia de frase negativa: `"keyword"`
   * Coincidencia exacta negativa: `[keyword]`

La sintaxis habitual para los tipos de frase y coincidencia exacta se utiliza en la hoja de edición masiva que se genera al propagar datos de fuente a través de la plantilla. **Nota:** No puede ver las palabras clave negativas en la [!UICONTROL Keywords] o en la [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vista.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Todas las redes de anuncios excepto [!DNL Yandex]; opcional) Cualquier palabra clave negativa estática en el nivel de campaña que se agregue a las campañas cuyo nombre no coincida con una cadena especificada. Para especificar varias palabras clave o varios tipos de coincidencia para la misma palabra clave, escríbalas en líneas independientes. Utilice la siguiente sintaxis, sin un signo menos:

* Coincidencia amplia negativa: `keyword` (no compatible con [!DNL Microsoft Advertising])
* Coincidencia de frase negativa: `"keyword"`
* Coincidencia exacta negativa: `[keyword]`

La sintaxis habitual para los tipos de frase y coincidencia exacta se utiliza en la hoja de edición masiva que se genera al propagar datos de fuente a través de la plantilla. **Nota:** No puede ver las palabras clave negativas en la [!UICONTROL Keywords] o en la [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vista.
