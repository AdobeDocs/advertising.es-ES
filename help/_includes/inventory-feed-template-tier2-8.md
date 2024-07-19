---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# Nivel 2: Campos de nivel 8 en plantillas de anuncios de compras

**[!UICONTROL Tier  2 - Tier 8]:** (cuando agrega niveles de grupos de productos) Un tipo de atributo de producto mediante el cual se van a dirigir los productos y los criterios de calificación para el tipo de atributo seleccionado (por ejemplo, Marca=Acme o Condición=Nueva). Los valores se aplican jerárquicamente para determinar los productos aptos. Seleccione un tipo de atributo e introduzca los criterios de cualificación. Entre los caracteres prohibidos se incluyen los siguientes: `[ ] < > >>` (dos signos &quot;mayor que&quot; consecutivos), que se utilizan para designar nombres de columna en la plantilla, nombres de modificador en la plantilla y separadores de niveles en la columna [!UICONTROL Parent Product Grouping] de las hojas de edición masiva.

Puede incluir hasta ocho niveles de grupos de productos, incluido &quot;[!UICONTROL All Products]&quot; (nivel 1). Cada nivel puede incluir varios grupos de productos, pero deben pertenecer al mismo tipo de atributo (como &quot;Condición&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] solamente) Los valores posibles de [!UICONTROL Channel] son &quot;[!UICONTROL Local]&quot; o &quot;[!UICONTROL Online]&quot;, y los valores posibles de [!UICONTROL ChannelExclusivity] son &quot;[!UICONTROL SingleChannel]&quot; y &quot;[!UICONTROL MultiChannel]&quot;.&quot;
>* Cuando crea un segundo grupo de productos de nivel (secundario) para un grupo de anuncios desde la ficha [!UICONTROL Product Groups] en la vista [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns], se crea automáticamente otro grupo de productos, denominado &quot;[!UICONTROL Everything Else]&quot;, utilizando la oferta de grupo de anuncios predeterminada. Sin embargo, al usar plantillas de fuente de inventario, se excluyen &quot;[!UICONTROL Everything Else]&quot; grupos de productos.
>* Cuando se incluyen varios niveles y no hay ningún valor disponible para el nivel final (el más alto), se utiliza el siguiente nivel más alto como grupo de productos por los que se puede pujar. Por ejemplo, si se incluyen cinco niveles y no hay ningún valor disponible para el nivel 5, entonces el nivel 4 se utiliza como grupo de productos (unidad) a los que se puede pujar. Sin embargo, si no hay ningún valor disponible para una capa media, se ignora la fila. Por ejemplo, si incluye cinco niveles y el Nivel 5 tiene un valor pero el Nivel 4 no, se omite la Fila 4.
