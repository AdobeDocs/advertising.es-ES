---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---
# Plantilla de anuncio de texto: fuentes y columnas

**[!UICONTROL Feed & Columns]:** Un [archivo de fuentes](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md) o cuenta de comerciante asociado con la plantilla y las columnas (encabezados) del archivo o cuenta seleccionados:

* *[!UICONTROL Feed File]:* Cargue un archivo o selecciónelo de la lista de archivos de fuentes disponibles.

* *[!UICONTROL Google Merchant Center]:* Seleccione una [cuenta sincronizada [!DNL Google Merchant Center] 4&rbrace;. ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) Search, Social y Commerce solo crean grupos de productos; [!DNL Google Ads] genera automáticamente los anuncios de compra de los grupos de productos. No se admiten columnas personalizadas.

* *[!UICONTROL Microsoft Merchant Center]:* ([!DNL Microsoft Advertising] plantillas de compra solamente) Selecciona una [cuenta sincronizada [!DNL Microsoft Merchant Center] 5&rbrace;. ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) Search, Social y Commerce solo crean grupos de productos; [!DNL Microsoft Advertising] genera automáticamente los anuncios de productos para los grupos de productos. No se admiten columnas personalizadas.

La asociación de la plantilla con un archivo de fuentes o una cuenta de comerciante es opcional hasta que esté listo para crear anuncios con la plantilla.

Cuando se inserta una columna de fuente en un campo de plantilla, el valor insertado se indica como `[field_name]`, donde &quot;field_name&quot; es el nombre de campo especificado, para indicar que el valor es una variable.

>[!NOTE]
>
>* Si cambia el archivo de fuente o la cuenta de una plantilla existente, es posible que tenga que ajustar los parámetros de la plantilla si el nuevo archivo contiene encabezados diferentes.
>* Si se elimina o deshabilita la cuenta o el archivo de fuente asociado con la plantilla, también se eliminará la asociación y deberá seleccionar un nuevo archivo de fuente para poder crear más anuncios con la plantilla. Si el nuevo archivo o cuenta de fuente no incluye los mismos encabezados que el archivo original, es posible que tenga que ajustar los parámetros de plantilla en consecuencia.
