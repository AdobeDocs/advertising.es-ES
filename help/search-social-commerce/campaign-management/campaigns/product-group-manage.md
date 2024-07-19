---
title: Administrar grupos de productos de compras
description: Obtenga información sobre cómo crear y administrar grupos de productos de compras en campañas de compras.
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Administrar grupos de productos de compras

*[!DNL Google Ads]y [!DNL Microsoft Advertising] campañas de compras solo*

Puede crear y editar grupos de productos y eliminar grupos de productos y sus grupos de productos secundarios en la vista [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

## Crear un grupo de productos [!UICONTROL All Products]

Para poder crear grupos de productos con atributos específicos, primero debe crear un grupo de productos con todo incluido denominado &quot;[!UICONTROL All Products]&quot;. Cada grupo de anuncios solo puede tener un grupo &quot;[!UICONTROL All Products]&quot;.

>[!TIP]
>
>Para crear muchos componentes de cuenta a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red de anuncios, la cuenta, la campaña y el grupo de anuncios y haga clic en **[!UICONTROL Continue]**.

1. Especifique la [[!DNL Google Ads] configuración del grupo de productos](product-group-settings-google.md) o la [[!DNL Microsoft Advertising] configuración del grupo de productos](product-group-settings-microsoft.md).

1. Haga clic en **[!UICONTROL Post]**.

## Crear un nodo de grupo de productos secundario en un grupo de productos existente

Una vez que haya creado al menos un grupo &quot;[!UICONTROL All Products]&quot; inclusivo para un grupo de anuncios, puede crear nodos de grupo de productos secundarios para subconjuntos de productos que se incluyan o excluyan de las ofertas, con uno o más grupos de productos dirigidos al mismo atributo en cada nivel (por ejemplo, [!UICONTROL Brand]=Acme para un grupo de productos y [!UICONTROL Brand]=AcmePlus para otro en el mismo nivel. Puede crear hasta siete niveles de nodos de grupo de productos secundarios, sin incluir &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>No puede crear un grupo de productos secundario para un grupo de productos &quot;[!UICONTROL Everything Else]&quot;.

>[!TIP]
>
>Para crear muchos componentes de cuenta a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Para ver un grupo de productos y sus nodos de grupos de productos secundarios en la vista de árbol, mantenga el cursor sobre el nombre del grupo de productos, haga clic en ![Icono de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icono de menú") y, a continuación, seleccione **[!UICONTROL Tree View]**.

1. Mantenga el cursor sobre el nombre del grupo de productos, haga clic en ![Menú desplegable de flecha](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menú desplegable de flecha") y, a continuación, seleccione **[!UICONTROL + Add Node]**.

1. Especifique la [[!DNL Google Ads] configuración del grupo de productos](product-group-settings-google.md) o la [[!DNL Microsoft Advertising] configuración del grupo de productos](product-group-settings-microsoft.md), incluidos la dimensión y el atributo del producto.

1. Haga clic en **[!UICONTROL Post]**.

## Editar configuración del nodo del grupo de productos

Puede editar la plantilla de oferta y seguimiento para los nodos de grupo de productos de unidades (grupos de productos sin nodos de grupo de productos secundarios) que se incluyen para un grupo de publicidad. No se puede editar ninguna información para grupos de productos de unidades excluidas o para nodos de subdivisiones incluidas o excluidas, que son grupos de productos con nodos de grupos de productos secundarios.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Para ver un grupo de productos y sus nodos de grupos de productos secundarios en la vista de árbol, mantenga el cursor sobre el nombre del grupo de productos, haga clic en ![Icono de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icono de menú") y, a continuación, seleccione **[!UICONTROL Tree View]**.

1. Realice una de las acciones siguientes:

   1. (Para editar la configuración de un solo nodo de grupo de productos) Mantenga el cursor sobre el nombre del grupo de productos, haga clic en ![Icono de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icono de menú") y, a continuación, seleccione **[!UICONTROL + Edit Node]**.

   1. (Para editar la configuración de uno o más grupos de anuncios) Haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada nodo.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite la [[!DNL Google Ads] configuración del grupo de productos](product-group-settings-google.md) o la [[!DNL Microsoft Advertising] configuración del grupo de productos](product-group-settings-microsoft.md).

   Para varios nodos, los cambios se aplican a todos los nodos seleccionados. Para el campo [!UICONTROL Bid], tiene opciones para cambiar los valores existentes a un valor especificado o para aumentar o disminuir la cantidad en un porcentaje o importe monetario especificados, con un límite. Para el campo [!UICONTROL Tracking Template], puede cambiar los valores existentes a un valor especificado, reemplazar una cadena existente por una cadena especificada, agregar un prefijo especificado al principio de cada valor o anexar un sufijo al final de cada valor.

1. (Opcional) Haga clic en **[!UICONTROL Additional Details]** y, opcionalmente, escriba un nombre y una descripción para el proyecto.

1. Haga clic en **[!UICONTROL Post]**.

## Eliminar nodos de grupos de productos

Puede eliminar cualquier grupo de productos (excepto el grupo &quot;Todo lo demás&quot;, cuando existen otros grupos de productos en el mismo nivel) que se utilice para determinar qué productos de la cuenta del centro de comerciantes se incluyen en los anuncios de compra del grupo de anuncios. Al eliminar un grupo de productos, se eliminan todos los grupos de productos secundarios.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Filtre la lista para incluir grupos de productos específicos.

1. Realice una de las acciones siguientes:

   * Para eliminar un grupo de productos, haga clic en la columna **[!UICONTROL Status]** y seleccione **[!UICONTROL Delete]**.

   * Para eliminar uno o varios grupos de productos, haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada grupo de productos que desee eliminar.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. En la barra de herramientas, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más") y seleccione **[!UICONTROL Delete]**.

      1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de los grupos de productos de compras](product-group-about.md)
>* [[!DNL Google Ads] configuración del grupo de productos](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] configuración del grupo de productos](product-group-settings-microsoft.md)
