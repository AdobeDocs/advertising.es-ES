---
title: Administrar grupos de productos de compras
description: Obtenga información, cree, edite y elimine grupos de productos de compras y haga referencia a la configuración de grupos de productos para Google Ads y Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---


# Administrar grupos de productos de compras

*[!DNL Google Ads]y [!DNL Microsoft Advertising] campañas de compras solo*

Puede crear y administrar grupos de productos en la vista [!UICONTROL Product Groups] en [!UICONTROL Assets] > [!UICONTROL Shopping].

Puede ver datos sobre los grupos de productos en [el [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md).

## ¿Qué son los grupos de productos?

En las campañas de compras, los grupos de productos (no las palabras clave) determinan los productos de la cuenta del centro de comerciantes para los que se muestran los anuncios de compras. Cada grupo de productos se basa en un único atributo de producto (como categoría, tipo de producto, marca, condición, ID de producto o etiquetas personalizadas) y utiliza la misma oferta para todos los productos coincidentes. Puede incluir o excluir ofertas para los productos de cada grupo.

Los grupos de productos se configuran en el nivel de grupo de anuncios para determinar qué productos de las cuentas del centro de comerciantes aparecen en los anuncios de compra del grupo de anuncios. Aunque el grupo de anuncios no incluya entidades de publicidad, la red de anuncios seguirá mostrando anuncios de los productos.

Cuando el mismo producto se incluye en más de una campaña, la red de anuncios utiliza primero la prioridad de campaña para determinar qué campaña (y oferta asociada) es elegible para la subasta de anuncio. Cuando todas las campañas tienen la misma prioridad, es elegible la campaña con la oferta más alta.

Para obtener más información sobre [!DNL Google] campañas de compras y anuncios, consulte &quot;[Implementar [!DNL Google Ads] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; y la [documentación de Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Para obtener más información acerca de [!DNL Microsoft] campañas de compras, consulte &quot;[Implementar [!DNL Microsoft Advertising] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot; y la [[!DNL Microsoft Advertising] documentación](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>No se ofrece soporte técnico para [!DNL Google Ads] grupos de listas en campañas Máximo rendimiento. Para administrar y ver datos de grupos de listas, use el editor [!DNL Google Ads].

### Jerarquía de grupos de productos

Para poder crear grupos de productos con atributos específicos para un grupo de anuncios, primero debe crear un grupo de productos inclusivo denominado &quot;[!UICONTROL All Products]&quot;. Desde este grupo de productos principal, puede crear grupos de productos secundarios para subconjuntos de productos y puede crear nietos a partir de los grupos de productos secundarios. Una vez creado el primer grupo de productos secundario para un grupo de anuncios, se crea automáticamente otro grupo de productos denominado &quot;[!UICONTROL Everything Else]&quot; mediante la oferta de grupo de anuncios predeterminada. A medida que agrega más grupos de productos, el grupo &quot;[!UICONTROL Everything Else]&quot; se ajusta en consecuencia para que constituya todos los productos que no están en otro grupo de productos.

Dentro de un grupo de anuncios, puede crear hasta siete niveles de grupos de productos (sin incluir &quot;[!UICONTROL All Products]&quot;) para incluirlos o excluirlos de ofertas, y uno o más grupos de productos tienen como objetivo el mismo atributo en cada nivel (por ejemplo, [!UICONTROL Brand]=Acme para un grupo de productos y [!UICONTROL Brand]=AcmePlus para otro en el mismo nivel). Los grupos de productos principales se denominan subdivisiones y el nivel más bajo de subdivisión se conoce como unidad. Puedes definir las pujas y las plantillas de seguimiento, o bien excluir por completo las pujas, en el nivel de unidad. Todo el conjunto de grupos de productos activos de un grupo de publicidad se aplica jerárquicamente para determinar los productos aptos. Por ejemplo, si subdivide [!UICONTROL All Products] en [!UICONTROL Brand]=AcmeBasic y [!UICONTROL Brand]=AcmePlus y, a continuación, subdivide cada uno de esos grupos de productos en [!UICONTROL Condition]=Nuevo y establece ofertas, solo se podrán anunciar o excluir de los anuncios los nuevos productos con las marcas AcmeBasic y AcmePlus.

![Ejemplo de un conjunto de grupos de productos](/help/search-social-commerce/assets/product-group-list-new.png "Ejemplo de un conjunto de grupos de productos")

![Ejemplo de jerarquía de grupos de productos](/help/search-social-commerce/assets/product-group-tree-new.png "Ejemplo de jerarquía de grupos de productos")

### Filtros de productos {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

Consulte también la ayuda de [!DNL Google Ads] &quot;[Administrar una campaña de compras con grupos de productos](https://support.google.com/google-ads/answer/6275317)&quot; y la ayuda de [!DNL Microsoft Advertising] &quot;[Comprender y usar grupos de productos](https://help.ads.microsoft.com/#apex/bae/en/56782)&quot;.

| Red de compras | Product Dimension | Atributos | Notas |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Category=]<br><br>Microsoft: [!UICONTROL Category 1=] a [!UICONTROL Category 5=] | \[Id. de categoría\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[La marca\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[Id. del elemento\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Product Type (1st level)=] a [!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]: [!UICONTROL Product Type=] | \[El tipo de producto\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=] a [!UICONTROL Custom Label 4=] | \[Atributo de la etiqueta personalizada\] | — |
| [!DNL Google Ads] | Channel= | [!UICONTROL Local], [!UICONTROL Online] | Para mostrar solo anuncios de productos locales o productos en línea.<br><br><b>Nota:</b> Para crear anuncios de productos locales, debe habilitarse la opción &quot;Anuncios de inventario local&quot; y debe participar en el programa de compras local con [!DNL Google Merchant Center]. |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | Si se desea mostrar anuncios para productos que solo están disponibles para un único canal (local o solo en línea) o para varios canales (locales y en línea). |

## La vista [!UICONTROL Product Groups]

La vista [!UICONTROL Product Groups] en la vista [!UICONTROL Assets] > [!UICONTROL Shopping] enumera todos los grupos de productos en la vista filtrada para la cuenta de anunciante seleccionada. También puede crear y administrar grupos de productos.

### Acciones disponibles <!-- Go through all -->

* [Crear un grupo de productos [!UICONTROL All Products]](#product-group-create-all-products)

* [Crear un nodo de grupo de productos secundario en un grupo de productos existente](#node-add)

* Editar la configuración de un nodo de grupo de productos:

  * [Editar cualquier configuración](#node-edit)

  * [Editar solo [!UICONTROL Tracking Template]](#node-edit-tracking-template)

  * [Editar solo [!UICONTROL Max CPC]](#node-edit-maxcpc)

* [Eliminar un nodo de grupo de productos](#node-delete)

* [Asignar restricciones](#constraint-assign) a grupos de productos y [quitar restricciones](#constraint-unassign) de grupos de productos

* [Asignar clasificaciones de etiquetas](#classification-values-assign) a grupos de productos y [quitar clasificaciones de etiquetas](#classification-values-remove) de grupos de productos

>[!NOTE]
>
>Puede crear y editar grandes cantidades de datos de grupos de productos (incluidas etiquetas y asignaciones de restricciones) a la vez cargando [archivos de hojas de edición masiva](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) y publicándolos en la red publicitaria.

## Crear un grupo de productos [!UICONTROL All Products] {#product-group-create-all-products}

Para poder crear grupos de productos con atributos específicos, primero debe crear un grupo de productos con todo incluido denominado &quot;[!UICONTROL All Products]&quot;. Cada grupo de anuncios solo puede tener un grupo &quot;[!UICONTROL All Products]&quot;.

>[!TIP]
>
>Para crear muchos componentes de cuenta a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Create Product Group]**.

1. Seleccione la red de anuncios, la cuenta, la campaña y el grupo de anuncios y haga clic en **[!UICONTROL Continue]**.

1. Especifique la [configuración del grupo de productos Google Ads](#google-ads-product-group-settings) o la [configuración del grupo de productos Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haz clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") y cambia la [configuración del grupo de productos de Google Ads](#google-ads-product-group-settings) o la [configuración del grupo de productos de Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Haga clic en **[!UICONTROL Create]**.

## Crear un nodo de grupo de productos secundario en un grupo de productos existente {#product-group-create-child}

Una vez que haya creado al menos un grupo &quot;[!UICONTROL All Products]&quot; inclusivo para un grupo de anuncios, puede crear nodos de grupo de productos secundarios para subconjuntos de productos que se incluyan o excluyan de las ofertas, con uno o más grupos de productos dirigidos al mismo atributo en cada nivel (por ejemplo, [!UICONTROL Brand]=Acme para un grupo de productos y [!UICONTROL Brand]=AcmePlus para otro en el mismo nivel. Puede crear hasta siete niveles de nodos de grupo de productos secundarios, sin incluir &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>No puede crear un grupo de productos secundario para un grupo de productos &quot;[!UICONTROL Everything Else]&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Opcional) Para ver un grupo de productos y sus nodos secundarios en la vista de árbol, mantenga el cursor sobre el nombre del grupo de productos y haga clic en **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Mantenga el cursor sobre el nombre del grupo de productos y haga clic en **[!UICONTROL ...]>[!UICONTROL + Add Node]**.

1. Especifique la [configuración del grupo de productos Google Ads](#google-ads-product-group-settings) o la [configuración del grupo de productos Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Haga clic en **[!UICONTROL Center]**.

## Editar la configuración de un nodo de grupo de productos {#node-edit}

Puede editar la plantilla de oferta y seguimiento para los nodos de grupo de productos de unidades (grupos de productos sin nodos de grupo de productos secundarios) que se incluyen para un grupo de publicidad. No se puede editar ninguna información para grupos de productos de unidades excluidas o para nodos de subdivisiones incluidas o excluidas, que son grupos de productos con nodos de grupos de productos secundarios.

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Opcional) Para ver un grupo de productos y sus nodos secundarios en la vista de árbol, mantenga el cursor sobre el nombre del grupo de productos y haga clic en **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Mantenga el cursor sobre el nombre del grupo de productos y haga clic en **[!UICONTROL ...]>[!UICONTROL + Edit Node]**.

1. Edite la [configuración del grupo de productos Google Ads](#google-ads-product-group-settings) o la [configuración del grupo de productos Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Haga clic en **[!UICONTROL Update]**.

## Editar solo [!UICONTROL Tracking Template] para un nodo de grupo de productos {#node-edit-tracking-template}

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Mantenga el cursor sobre el nombre del grupo de productos y haga clic en **[!UICONTROL ...]>[!UICONTROL Tree View]** para ver el grupo de productos y sus nodos de grupo de productos secundarios en la vista de árbol.

1. En la columna **[!UICONTROL Tracking Template]**, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar").

1. Cambie el valor **[!UICONTROL Tracking Template]** y haga clic en **[!UICONTROL Save]**.

## Editar solo [!UICONTROL Max CPC] para un nodo de grupo de productos {#node-edit-maxcpc}

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Mantenga el cursor sobre el nombre del grupo de productos y haga clic en **[!UICONTROL ...]>[!UICONTROL Tree View]** para ver el grupo de productos y sus nodos de grupo de productos secundarios en la vista de árbol.

1. En la columna **[!UICONTROL Max CPC]**, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar").

1. Cambie el valor **[!UICONTROL Max CPC]** y haga clic en **[!UICONTROL Save]**.

## Eliminar un nodo de grupo de productos {#node-delete}

Puede eliminar cualquier grupo de productos (excepto el grupo &quot;Todo lo demás&quot;, cuando existen otros grupos de productos en el mismo nivel) que se utilice para determinar qué productos de la cuenta del centro de comerciantes se incluyen en los anuncios de compra del grupo de anuncios. Al eliminar un grupo de productos, se eliminan todos los grupos de productos secundarios.

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Mantenga el cursor sobre el nombre del grupo de productos y haga clic en **[!UICONTROL ...]>[!UICONTROL Tree View]** para ver el grupo de productos y sus nodos de grupo de productos secundarios en la vista de árbol.

1. Haga clic en la columna **[!UICONTROL Status]** y seleccione **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Asignar una restricción a los grupos de productos seleccionados {#constraint-assign}

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de productos al que va a asignar una única restricción.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

## Eliminar restricciones de los grupos de productos seleccionados {#constraint-unassign}

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de productos del que anulará la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

## Asignar valores de clasificación a grupos de productos {#classification-values-assign}

>[!NOTE]
>
>Las entidades secundarias heredan los valores de etiquetas, por lo que no introduzca valores para entidades secundarias a menos que desee anular los valores heredados.

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de productos al que desea asignar un valor de etiqueta.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Para cada valor de clasificación aplicable, haga lo siguiente:

   1. En la columna **[!UICONTROL Classifications]**, especifique la clasificación:

      * Para utilizar una clasificación existente, haga clic en el nombre de la clasificación para expandirla.

      * Para crear una clasificación, haga clic en [!UICONTROL +] en el encabezado de la columna. En el campo de entrada, escriba el nombre de la clasificación y haga clic en ![Guardar](/help/search-social-commerce/assets/save-checkmark.png "Guardar") para guardar la clasificación inmediatamente. Para utilizar la nueva clasificación, haga clic en el nombre de la clasificación para expandirla.

        El nombre debe contener [caracteres ASCII 32-126](https://www.asciitable.com/) y la longitud máxima es de 27 caracteres de un solo byte.

   1. En la columna **[!UICONTROL Value Name]**, especifique el valor de la clasificación seleccionada:

      * Para utilizar un valor existente, seleccione el valor.

      * Para crear un valor, haga clic en [!UICONTROL +] en el encabezado de la columna. En el campo de entrada, escriba el valor y, a continuación, haga clic en ![Guardar](/help/search-social-commerce/assets/save-checkmark.png "Guardar") para guardar inmediatamente el valor y seleccionarlo de forma predeterminada.

        La longitud máxima es de 100 caracteres y puede incluir caracteres ASCII y no ASCII.

1. Haga clic en **+[!UICONTROL Assign Now]**.

## Quitar valores de clasificación de etiquetas de grupos de productos {#classification-values-remove}

Al eliminar un valor de clasificación, se elimina la asociación con el componente de cuenta y todos sus componentes secundarios. Los datos del informe para el valor de clasificación ya no están disponibles para esos componentes. Al eliminar un valor de clasificación, no se elimina el valor ni los componentes de la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de productos del que va a quitar un valor de etiqueta.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleccione la casilla de verificación situada junto a cada valor de clasificación que desee eliminar de las entidades seleccionadas.

   Para seleccionar todos los valores asignados, haga clic en **[!UICONTROL Select All]**. Para anular la selección de todos los valores asignados, haga clic en **[!UICONTROL Deselect All]**.

1. Haga clic en **[!UICONTROL Unassign Selected]**.

## Configuración del grupo de productos [!DNL Google Ads] {#google-ads-product-group-settings}

### Todos los grupos de productos

**[!UICONTROL Network]:** (solo para grupos de productos nuevos) La red de anuncios.

**[!UICONTROL Account]:** (solo para grupos de productos nuevos) El nombre de cuenta de red de anuncios.

**[!UICONTROL Campaign]:** (solo para grupos de productos nuevos) La campaña.

**[!UICONTROL Ad Group]:** (solo para grupos de productos nuevos) El grupo de anuncios.

**[!UICONTROL Condition]** o **[!UICONTROL Condition Type]:** (solo lectura) Todos los productos

**[!UICONTROL Condition Value]:** (solo grupos de productos existentes)  

**[!UICONTROL Bid]** o **[!UICONTROL Max CPC]:** (solo grupos de productos incluidos) El costo por clic (CPC) máximo, que es la cantidad más alta que se debe pagar por un clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

{{$include /help/_includes/tracking-template-google.md}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios. No se incluye ningún parámetro de datos anexados especificado para la cuenta o campaña. No se incluye ningún parámetro de datos anexados especificado para la cuenta o campaña.

### Todos los demás grupos de productos

**[!UICONTROL Condition Type]** y **[!UICONTROL Condition Value]:** (solo lectura para grupos de productos existentes) Las dimensiones de producto que se van a destinar. En el caso de los grupos de productos nuevos, introduzca la dimensión según la cual se van a segmentar los productos y el atributo correspondiente a la categoría de información seleccionada (como &quot;Acme&quot; cuando se establece el objetivo por marca o &quot;Nuevo&quot; cuando se establece el objetivo por condición).

Una vez creado un grupo de productos para dimensiones de producto específicas (es decir, no &quot;Todos los productos&quot;), Search, Social y Commerce crean automáticamente un grupo de productos para &quot;Todo lo demás&quot;.

Para obtener una lista de las dimensiones de producto disponibles, consulte &quot;[Filtros de producto](#product-filters)&quot;. Su lista de dimensiones puede estar limitada en función de la configuración [!UICONTROL Inventory Filter] de la campaña.

**[!UICONTROL Excluded]:** (opcional para los grupos de productos nuevos; solo lectura para los grupos de productos existentes) excluye las ofertas de anuncios para productos coincidentes.

**[!UICONTROL Max CPC]:** (solo grupos de productos incluidos) El costo máximo por clic (CPC), que es la cantidad más alta que se paga por clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

## Configuración del grupo de productos [!DNL Microsoft Advertising] {#microsoft-advertising-product-group-settings}

### Todos los grupos de productos

**[!UICONTROL Network]:** (solo para grupos de productos nuevos) La red de anuncios.

**[!UICONTROL Account]:** (solo para grupos de productos nuevos) El nombre de cuenta de red de anuncios.

**[!UICONTROL Campaign]:** (solo para grupos de productos nuevos) La campaña.

**[!UICONTROL Ad Group]:** (solo para grupos de productos nuevos) El grupo de anuncios.

**[!UICONTROL Condition]** o **[!UICONTROL Condition Type]:** (solo lectura) Todos los productos

**[!UICONTROL Condition Value]:** (solo grupos de productos existentes)  

**[!UICONTROL Bid]** o **[!UICONTROL Max CPC]:** (solo grupos de productos incluidos) El costo por clic (CPC) máximo, que es la cantidad más alta que se debe pagar por un clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

**[!UICONTROL Base URL]:** (solo para grupos de productos nuevos) No utilizado<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

### Todos los demás grupos de productos

**[!UICONTROL Condition Type]** y **[!UICONTROL Condition Value]:** (solo lectura para grupos de productos existentes) Las dimensiones de producto que se van a destinar. Para los grupos de productos nuevos, introduzca la dimensión según la cual se van a segmentar los productos y el atributo correspondiente para la categoría de información seleccionada (como &quot;Acme&quot; cuando se establece el objetivo por marca o &quot;Nuevo&quot; cuando se establece el objetivo por condición).

Una vez creado un grupo de productos para dimensiones de producto específicas (es decir, no &quot;Todos los productos&quot;), Search, Social y Commerce crean automáticamente un grupo de productos para &quot;Todo lo demás&quot;.

Para obtener una lista de las dimensiones de producto disponibles, consulte &quot;[Filtros de producto](#product-filters)&quot;. Su lista de dimensiones puede estar limitada en función de la configuración [!UICONTROL Inventory Filter] de la campaña.

**[!UICONTROL Excluded]:** (opcional para los grupos de productos nuevos; solo lectura para los grupos de productos existentes) excluye las ofertas de anuncios para productos coincidentes.

**[!UICONTROL Max CPC]:** (solo grupos de productos incluidos) El costo máximo por clic (CPC), que es la cantidad más alta que se paga por clic en un anuncio. Este valor solo se utiliza para unidades sin grupos de productos secundarios y se utiliza en lugar del valor de nivel de grupo de anuncios.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Esta plantilla anula las plantillas de los niveles superiores y se utiliza sólo para unidades sin grupos de productos secundarios.

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Google Ads] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [Implementar [!DNL Microsoft Advertising] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [El [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
