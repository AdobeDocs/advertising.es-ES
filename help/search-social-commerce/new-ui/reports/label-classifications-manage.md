---
title: Administrar clasificaciones de etiquetas
description: Obtenga información acerca del uso de clasificaciones de etiquetas para agrupar los componentes de la cuenta.
feature: Search Label Classifications
source-git-commit: 639037683053009ce653dee6d7c1e4eb80abf4d8
workflow-type: tm+mt
source-wordcount: '1515'
ht-degree: 0%

---

# Administrar clasificaciones de etiquetas

Las clasificaciones de etiquetas ayudan a agrupar los componentes de la cuenta en conjuntos significativos. Por ejemplo, puede crear una clasificación de etiquetas principal llamada &quot;Geografía&quot;, crear un valor de etiqueta diferente para cada región geográfica (como &quot;Reino Unido&quot; y &quot;Japón&quot;) dentro de la clasificación y luego asignar los valores de etiqueta a sus [unidades de oferta](/help/search-social-commerce/glossary.md#a-b) o campañas principales. A continuación, puede incluir cualquier valor de etiqueta como una columna independiente en las vistas e informes, y subpivotar los informes en diferentes grupos y valores de clasificación.

## Componentes de clasificaciones de etiquetas

### Clasificaciones de etiquetas

Cada anunciante puede tener hasta 30 clasificaciones de etiquetas, que son categorías de nivel superior. Una vez creada una clasificación de etiquetas, puede crear valores de etiqueta específicos para la clasificación.

### Valores de etiqueta

Cada clasificación de etiquetas puede tener hasta 2000 valores. Una vez que haya creado valores de etiqueta específicos para una clasificación, puede asignarlos a campañas, grupos de anuncios, palabras clave, anuncios, ubicaciones y grupos de productos [desde las vistas de administración de campañas](#classification-values-assign-campaign-management) o [mediante hojas de edición por lotes](#classification-values-assign-bulksheets).

Cada entidad elegible puede tener valores de etiqueta para varias clasificaciones, pero solo un valor de etiqueta por clasificación. Las entidades secundarias heredan los valores de las etiquetas, pero se pueden anular. El valor asignado en el nivel inferior siempre anula los valores asignados en los niveles principales.

## La vista Clasificaciones de etiquetas

La vista [!UICONTROL Reports] > [!UICONTROL Labels Classifications] incluye [!UICONTROL Classifications] y [!UICONTROL Label Values] subvistas. De forma predeterminada, los datos se muestran para sus clasificaciones y valores de etiquetas de nivel de palabra clave, pero también puede ver los datos de sus clasificaciones y valores de nivel de anuncio.

## Acciones disponibles

* Vea los datos de sus clasificaciones de etiquetas.

* Vea los datos de los valores de clasificación de etiquetas.

* [Crear una clasificación de etiquetas](#classification-create).

* Asigne valores de clasificación a los componentes de cuenta [desde las vistas de administración de campañas](#classification-values-assign-campaign-management) o [mediante hojas de edición por lotes](#classification-values-assign-bulksheets).

* [Quitar valores de clasificación de etiquetas de los componentes de la cuenta](#classification-values-remove).

* [Eliminar valores de clasificación de etiquetas](#classification-values-delete).

* [Eliminar clasificaciones de etiquetas](#classification-delete).

## Crear una clasificación de etiquetas {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. Haga clic en **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create Classification]**.

1. Escriba un nombre de clasificación de etiqueta único y haga clic en **[!UICONTROL Create]**.

   El nombre debe ser único para la cuenta del anunciante y constar de [caracteres ASCII 32-126](https://www.asciitable.com/), y la longitud máxima es de 27 caracteres de un solo byte. El nombre no puede ser idéntico al nombre de una columna de informe existente o de una columna de hoja de edición masiva existente. Vea los nombres de las columnas de hojas de edición masiva de [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Anuncios de Japón](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), [Yahoo! Mostrar red](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md) y [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md).

## Asignar valores de clasificación a componentes de cuenta desde las vistas de administración de campañas {#classification-values-assign-campaign-management}

Puede asignar y eliminar valores de clasificación para las siguientes entidades de búsqueda desde las vistas de administración de campañas: campaña, grupo de anuncios, palabra clave, anuncio, ubicación, grupo de productos de nivel de unidad y destino de búsqueda dinámica. Si es necesario, puede crear clasificaciones y valores de clasificación durante el proceso de asignación. Cada clasificación de etiquetas puede tener hasta 2000 valores.

Cada entidad puede tener un valor de etiqueta por clasificación. Por ejemplo, Shoes_Campaign puede tener un valor de Color de &quot;rojo&quot; y un valor Geo de &quot;Los Ángeles&quot;, pero no puede tener varios valores para Color o Geo.

Las entidades secundarias heredan los valores de etiquetas, por lo que no introduzca valores para entidades secundarias a menos que desee anular los valores heredados.

>[!NOTE]
>
>Las palabras clave y la copia de anuncios de algunas redes de anuncios y tipos de campañas son [no mutables](/help/search-social-commerce/campaign-management/faqs-campaigns.md), lo que significa que al editarlas se eliminará la entidad existente y se creará una nueva. Cuando se elimina una entidad existente de este modo, la clasificación de etiquetas no se asigna a la nueva entidad.

1. Abra la vista de entidades desde el menú **[!UICONTROL Manage]** o **[!UICONTROL Target]**.

1. Seleccione la casilla de verificación situada junto a cada fila correspondiente.

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

## Asignar valores de clasificación a componentes de cuenta mediante hojas de edición masiva {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

Puede asociar clasificaciones de etiquetas con valores para las siguientes entidades de búsqueda mediante hojas de edición por lotes: campaña, grupo de anuncios, palabra clave, anuncio, ubicación, grupo de productos a nivel de unidad y destino de búsqueda dinámica. Cada clasificación de etiquetas puede tener hasta 2000 valores.

Cada entidad puede tener un valor de etiqueta por clasificación. Por ejemplo, Shoes_Campaign puede tener un valor de Color de &quot;rojo&quot; y un valor Geo de &quot;Los Ángeles&quot;, pero no puede tener varios valores para Color o Geo.

Las entidades secundarias heredan los valores de etiquetas, por lo que no introduzca valores para entidades secundarias a menos que desee anular los valores heredados.

>[!NOTE]
>
>Las palabras clave y la copia de anuncios de algunas redes de anuncios y tipos de campañas son [no mutables](/help/search-social-commerce/campaign-management/faqs-campaigns.md), lo que significa que al editarlas se eliminará la entidad existente y se creará una nueva. Cuando se elimina una entidad existente de este modo, la clasificación de etiquetas no se asigna a la nueva entidad.

1. [Descargar una hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) que incluya las entidades a las que desea asignar valores de clasificación de etiquetas:

   * En la ficha [!UICONTROL Rows and Columns], expanda la lista [!UICONTROL Campaign] en el panel [!UICONTROL Bulksheet Columns].

   * Expanda la lista [!UICONTROL Label Classification].

   * Seleccione cada clasificación para la que desee incluir una columna en el archivo de hoja de edición masiva.

     Por ejemplo, si incluye las clasificaciones de etiquetas &quot;Color&quot; y &quot;Geo&quot;, la hoja de edición masiva incluirá las columnas &quot;Color&quot; y &quot;Geo&quot;.

1. Abra el archivo en un editor y añada valores de etiqueta a las columnas de clasificación de etiquetas de las entidades con las que desea asociarlos. La longitud máxima de cada valor es de 100 caracteres, y puede incluir caracteres ASCII y no ASCII.

   Consulte los valores de ejemplo en la siguiente sección.

   Además de agregar valores, también puede eliminar valores existentes eliminándolos de las filas relevantes. Para eliminar valores tanto de una entidad padre como de sus entidades hijo, a) incluya solo la fila de la entidad padre y elimine el valor de clasificación existente, o b) incluya tanto la entidad padre como sus entidades hijo y elimine el valor de clasificación existente de todas las filas padre y hijo.

1. [Cargue el archivo](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) para crear las asociaciones.<!-- Update once the new bulksheet UI is GA -->

Los valores de etiqueta cargados son visibles en las vistas de entidad relevantes.

### Ejemplo de valores de clasificación de etiquetas para cargar en hojas de edición masiva

Este ejemplo incluye columnas para las clasificaciones de etiquetas &quot;Color&quot; y &quot;Geo&quot;. Para sus propias hojas de edición masiva, sustituya las columnas por sus propios nombres de clasificación de etiquetas.

| Cuenta | Campaign | Grupo de publicidad | Palabra clave | Anuncio | Ubicación | Etiquetas | Color | Geo |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 | | | | | | Verde | |
| Acct1 | C1 | GA1 | | | | | | |
| Acct1 | C1 | GA1 | K1 | | | | | RU |
| Acct1 | C1 | GA1 | K2 | | | | Rojo | AU |
| Acct1 | C1 | GA1 | K3 | | | | Azul | DE |
| Acct1 | C1 | GA1 | | A1 | | | | |
| Acct1 | C1 | GA1 | | A1 | | | Rojo | |
| Acct1 | C1 | GA1 | | | P1 | | Rojo | AU |
| Acct1 | C1 | GA1 | | | P2 | | Azul | DE |

## Quitar valores de clasificación de etiquetas de componentes de cuenta {#classification-values-remove}

Al eliminar un valor de clasificación, se elimina la asociación con el componente de cuenta y todos sus componentes secundarios. Los datos del informe para el valor de clasificación ya no están disponibles para esos componentes. Al eliminar un valor de clasificación, no se elimina el valor ni los componentes de la cuenta.

>[!NOTE]
>
>Para eliminar un valor de una clasificación de etiquetas, consulte &quot;[Eliminar valores de clasificación de etiquetas](#classification-values-delete)&quot;.

1. Abra la vista de entidades desde el menú **[!UICONTROL Manage]** o **[!UICONTROL Target]**.

1. Seleccione la casilla de verificación situada junto a cada fila correspondiente.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleccione la casilla de verificación situada junto a cada valor de clasificación que desee quitar de las entidades seleccionadas.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Para seleccionar todos los valores asignados, haga clic en **[!UICONTROL Select All]**. Para anular la selección de todos los valores asignados, haga clic en **[!UICONTROL Deselect All]**.

1. Haga clic en **[!UICONTROL Unassign Selected]**.

## Eliminar valores de clasificación de etiquetas {#classification-values-delete}

Al eliminar los valores de clasificación de etiquetas, no estarán disponibles para su uso futuro y los datos del informe ya no estarán disponibles para los valores. Se eliminan todas las asignaciones entre los valores y sus clasificaciones de etiquetas principales y componentes de cuenta específicos, pero no se eliminan las clasificaciones de etiquetas principales y los componentes de campaña.

>[!NOTE]
>
>Para simplemente desasociar un valor de clasificación de un componente de cuenta, consulte &quot;[Quitar valores de clasificación de etiquetas de los componentes de cuenta](#classification-values-remove)&quot;.

1. Haga clic en **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. Haga clic en la ficha **[!UICONTROL Label Values]**.

1. (Opcional) Filtre la lista para incluir valores de etiqueta específicos.

1. Seleccione la casilla de verificación situada junto a cada valor de etiqueta que desee eliminar.

   Puede eliminar hasta 200 filas a la vez.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar").

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Eliminar clasificaciones de etiquetas

Al eliminar una clasificación, se eliminan todas las asociaciones entre sus valores secundarios y los componentes de cuenta. Una clasificación eliminada y sus valores no están disponibles para uso futuro. Los datos de informe para los valores de clasificación ya no están disponibles.

>[!NOTE]
>
>Para simplemente desasociar un valor de clasificación de un componente de cuenta, consulte &quot;[Quitar valores de clasificación de etiquetas de los componentes de cuenta](#classification-values-remove)&quot;.

1. Haga clic en **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. (Opcional) Filtre la lista para incluir clasificaciones de etiquetas específicas.

1. Seleccione la casilla de verificación situada junto a cada clasificación de etiquetas que desee eliminar.

   Puede eliminar hasta 200 filas a la vez.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar").

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.
