---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---
# Nivel 2: Campos de nivel 8 en plantillas de anuncios de compras

**[!UICONTROL Tier  2 - Tier 8]:** (Cuando se agregan niveles de grupos de productos) Un tipo de atributo de producto por el que dirigirse a los productos y los criterios de calificación para el tipo de atributo seleccionado (por ejemplo, Marca=Acme o Condición=Nuevo). Los valores se aplican jerárquicamente para determinar los productos aptos. Seleccione un tipo de atributo e introduzca los criterios de cualificación. Los caracteres prohibidos incluyen los siguientes: `[ ] < > >>` (dos signos &quot;bueno que&quot; consecutivos), que se utilizan para designar nombres de columna en la plantilla, nombres de modificador en la plantilla y separadores de niveles en la [!UICONTROL Parent Product Grouping] en hojas de edición masiva.

Puede incluir hasta ocho niveles (niveles) de grupos de productos, incluido &quot;[!UICONTROL All Products]&quot; (Nivel 1). Cada nivel puede incluir varios grupos de productos, pero deben pertenecer al mismo tipo de atributo (como &quot;Condición&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] solo) Los valores posibles para [!UICONTROL Channel] son &quot;[!UICONTROL Local]&quot; o &quot;[!UICONTROL Online]y los valores posibles para [!UICONTROL ChannelExclusivity] son &quot;[!UICONTROL SingleChannel]&quot; y &quot;[!UICONTROL MultiChannel].&quot;
>* Cuando crea un segundo grupo de productos de nivel (secundario) para un grupo de anuncios desde el [!UICONTROL Product Groups] en la pestaña [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] ver, otro grupo de productos, llamado &quot;[!UICONTROL Everything Else],&quot; se crea automáticamente mediante la oferta de grupo de anuncios predeterminada. Sin embargo, si utiliza plantillas de fuente de inventario, &quot;[!UICONTROL Everything Else]&quot; se excluyen los grupos de productos.
>* Cuando se incluyen varios niveles y no hay ningún valor disponible para el nivel final (el más alto), se utiliza el siguiente nivel más alto como grupo de productos por los que se puede pujar. Por ejemplo, si se incluyen cinco niveles y no hay ningún valor disponible para el nivel 5, entonces el nivel 4 se utiliza como grupo de productos (unidad) a los que se puede pujar. Sin embargo, si no hay ningún valor disponible para una capa media, se ignora la fila. Por ejemplo, si incluye cinco niveles y el Nivel 5 tiene un valor pero el Nivel 4 no, se omite la Fila 4.

