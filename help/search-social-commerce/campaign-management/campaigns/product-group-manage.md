---
title: Administrar grupos de productos de compras
description: Obtenga información sobre cómo crear y administrar grupos de productos de compras en campañas de compras.
exl-id: 25912abd-1ddb-443f-a16d-7efe57093677
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Administrar grupos de productos de compras

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo campañas de compra*

Puede crear y editar grupos de productos y eliminar grupos de productos y sus grupos de productos secundarios en la [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] vista.

## Crear un &quot;[!UICONTROL All Products]&quot; grupo de productos

Antes de poder crear grupos de productos con atributos específicos, primero debe crear un grupo de productos inclusivo llamado &quot;[!UICONTROL All Products].&quot; Cada grupo de anuncios solo puede tener un &quot;[!UICONTROL All Products]&quot; grupo.

>[!TIP]
>
>Para crear muchos componentes de cuenta a la vez, utilice [hojas de campaña](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red de publicidad, la cuenta, la campaña y el grupo de publicidad y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Especifique el [[!DNL Google Ads] configuración de grupo de productos](product-group-settings-google.md) o [[!DNL Microsoft Advertising] configuración de grupo de productos](product-group-settings-microsoft.md).

1. Haga clic **[!UICONTROL Post]**.

## Crear un nodo de grupo de productos secundario en un grupo de productos existente

Una vez que hayas creado al menos un todo incluido &quot;[!UICONTROL All Products]&quot; para un grupo de publicidad, puede crear nodos de grupo de productos secundarios para subconjuntos de productos que se incluirán o excluirán de las ofertas, con uno o más grupos de productos dirigidos al mismo atributo en cada nivel (por ejemplo, [!UICONTROL Brand]=Acme para un grupo de productos y [!UICONTROL Brand]=AcmePlus para otro en el mismo nivel. Puede crear hasta siete niveles de nodos de grupo de productos secundarios, sin incluir &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>No se puede crear un grupo de productos secundario para un &quot;[!UICONTROL Everything Else]&quot; grupo de productos.

>[!TIP]
>
>Para crear muchos componentes de cuenta a la vez, utilice [hojas de campaña](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Para ver un grupo de productos y sus nodos secundarios en la vista de árbol, mantenga el cursor sobre el nombre del grupo de productos y haga clic en ![Icono de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icono de menú"), y luego seleccione **[!UICONTROL Tree View]**.

1. Mantenga el cursor sobre el nombre del grupo de productos y haga clic en ![Menú desplegable de flecha](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menú desplegable de flecha"), y luego seleccione **[!UICONTROL + Add Node]**.

1. Especifique el [[!DNL Google Ads] configuración de grupo de productos](product-group-settings-google.md) o [[!DNL Microsoft Advertising] configuración de grupo de productos](product-group-settings-microsoft.md), incluidas la dimensión y el atributo del producto.

1. Haga clic **[!UICONTROL Post]**.

## Editar configuración del nodo del grupo de productos

Puede editar la plantilla de oferta y seguimiento para los nodos de grupo de productos de unidades (grupos de productos sin nodos de grupo de productos secundarios) que se incluyen para un grupo de publicidad. No se puede editar ninguna información para grupos de productos de unidades excluidas o para nodos de subdivisiones incluidas o excluidas, que son grupos de productos con nodos de grupos de productos secundarios.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Para ver un grupo de productos y sus nodos secundarios en la vista de árbol, mantenga el cursor sobre el nombre del grupo de productos y haga clic en ![Icono de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icono de menú"), y luego seleccione **[!UICONTROL Tree View]**.

1. Realice una de las acciones siguientes:

   1. (Para editar la configuración de un solo nodo de grupo de productos) Mantenga el cursor sobre el nombre del grupo de productos y haga clic en ![Icono de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icono de menú"), y luego seleccione **[!UICONTROL + Edit Node]**.

   1. (Para editar la configuración de uno o más grupos de anuncios) Haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada nodo.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite el [[!DNL Google Ads] configuración de grupo de productos](product-group-settings-google.md) o [[!DNL Microsoft Advertising] configuración de grupo de productos](product-group-settings-microsoft.md).

   Para varios nodos, los cambios se aplican a todos los nodos seleccionados. Para el [!UICONTROL Bid] , tiene opciones para cambiar los valores existentes a un valor especificado o para aumentar o disminuir el importe en un porcentaje o importe monetario especificados, con un límite. Para el [!UICONTROL Tracking Template] , puede cambiar los valores existentes a un valor especificado, reemplazar una cadena existente por una cadena especificada, agregar un prefijo especificado al principio de cada valor o anexar un sufijo al final de cada valor.

1. (Opcional) Haga clic en **[!UICONTROL Additional Details]** y, opcionalmente, introduzca un nombre y una descripción de proyecto.

1. Haga clic **[!UICONTROL Post]**.

## Eliminar nodos de grupos de productos

Puede eliminar cualquier grupo de productos (excepto el grupo &quot;Todo lo demás&quot;, cuando existen otros grupos de productos en el mismo nivel) que se utilice para determinar qué productos de la cuenta del centro de comerciantes se incluyen en los anuncios de compra del grupo de anuncios. Al eliminar un grupo de productos, se eliminan todos los grupos de productos secundarios.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Filtre la lista para incluir grupos de productos específicos.

1. Realice una de las acciones siguientes:

   * Para eliminar un grupo de productos, haga clic en **[!UICONTROL Status]** y seleccione **[!UICONTROL Delete]**.

   * Para eliminar uno o varios grupos de productos, haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada grupo de productos que desee eliminar.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. En la barra de herramientas, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más") y seleccione **[!UICONTROL Delete]**.

      1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de los grupos de productos](product-group-about.md)
>* [[!DNL Google Ads] configuración de grupo de productos](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] configuración de grupo de productos](product-group-settings-microsoft.md)
