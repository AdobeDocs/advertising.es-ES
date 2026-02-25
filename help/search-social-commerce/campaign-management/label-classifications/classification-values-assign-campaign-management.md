---
title: Asignar valores de clasificación a componentes de cuenta desde las vistas de administración de campañas
description: Obtenga información sobre cómo asignar valores de clasificación a componentes de cuenta.
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# Asignar valores de clasificación a componentes de cuenta desde las vistas de administración de campañas

Puede asignar y eliminar valores de clasificación para las siguientes entidades de búsqueda desde las vistas de administración de campañas: campaña, grupo de anuncios, palabra clave, anuncio, ubicación, grupo de productos de nivel de unidad y destino de búsqueda dinámica. Si es necesario, puede crear clasificaciones y valores de clasificación durante el proceso de asignación. Cada clasificación de etiquetas puede tener hasta 2000 valores.

Cada entidad puede tener un valor de etiqueta por clasificación. Por ejemplo, Shoes_Campaign puede tener un valor de Color de &quot;rojo&quot; y un valor Geo de &quot;Los Ángeles&quot;, pero no puede tener varios valores para Color o Geo.

Las entidades secundarias heredan los valores de etiquetas, por lo que no introduzca valores para entidades secundarias a menos que desee anular los valores heredados.

>[!NOTE]
>
>Las palabras clave y la copia de anuncios de algunas redes de anuncios y tipos de campañas son [no mutables](/help/search-social-commerce/campaign-management/faqs-campaigns.md), lo que significa que al editarlas se eliminará la entidad existente y se creará una nueva. Cuando se elimina una entidad existente de este modo, la clasificación de etiquetas no se asigna a la nueva entidad.

## (Nueva interfaz de usuario) Asignar valores de clasificación a componentes de cuenta

Puede asignar valores de clasificación a cualquier componente de cuenta aplicable que esté disponible en la nueva interfaz de usuario.

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

## (IU heredada) Asignar valores de clasificación a componentes de cuenta

1. Haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** y, a continuación, seleccione la vista de componente de la cuenta.

1. Realice una de las acciones siguientes:

   * (Para asignar valores a una sola entidad) Mantenga el cursor sobre el nombre de la entidad, haga clic en ![Botón de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Botón de menú") y, a continuación, seleccione **[!UICONTROL Classification]**.

   * (Para asignar valores a una o varias entidades) Haga lo siguiente:

      * Seleccione la casilla de verificación situada junto a cada fila correspondiente.

        Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      * En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más") y, a continuación, haga clic en **[!UICONTROL Classification]**.

1. En [!UICONTROL Assignment Details], realice una de las siguientes acciones:

   * Para cambiar los valores de clasificaciones existentes por valores nuevos, seleccione **[!UICONTROL Set To]**.

     La longitud máxima de cada valor es de 100 caracteres, y puede incluir caracteres ASCII y no ASCII.

   * Para asignar los valores de clasificación especificados sin quitar los valores existentes, seleccione **[!UICONTROL Assign]**.

   * Para quitar valores de clasificación específicos asignados actualmente, seleccione **[!UICONTROL Remove]**.

     Cuando se elimina un valor de clasificación, los datos del informe del valor ya no están disponibles para los componentes de cuenta especificados.

   * Para eliminar los valores de clasificación especificados, seleccione **[!UICONTROL Delete]**.

     Al eliminar un valor de clasificación, no estará disponible para uso futuro y los datos del informe ya no estarán disponibles para el valor. Se eliminan todas las asignaciones entre los valores y los componentes de cuenta específicos, pero no los componentes de cuenta.

1. Para cada valor de clasificación aplicable, haga lo siguiente:

   1. En la columna **[!UICONTROL Classification]**, especifique el nombre de la clasificación:

      * Para utilizar una clasificación existente, haga clic en el nombre de la clasificación para expandirla.

      * Para crear una clasificación, haga clic en [!UICONTROL +]. En el campo de entrada, escriba el nombre de la clasificación y haga clic en ![Guardar](/help/search-social-commerce/assets/select.png "Guardar") para guardar la clasificación inmediatamente.

        El nombre debe contener [caracteres ASCII 32-126](https://www.asciitable.com/) y la longitud máxima es de 27 caracteres de un solo byte.

   1. En la columna **[!UICONTROL Value Name]**, especifique el nombre del valor:

      * Para utilizar un valor existente, haga clic en el nombre del valor para seleccionarlo.

      * Para crear un valor, haga clic en [!UICONTROL +]. En el campo de entrada, escribe el valor y, a continuación, haz clic en ![Guardar](/help/search-social-commerce/assets/select.png "Guardar") para guardar de inmediato el valor.

        La longitud máxima es de 100 caracteres y puede incluir caracteres ASCII y no ASCII.

1. (Opcional) Introduzca detalles adicionales:

   1. Junto a **[!UICONTROL Additional Details]**, haz clic en ![Abrir](/help/search-social-commerce/assets/chevron-up.png "Abrir") para ampliar los detalles.

   1. Escriba un(a) **[!UICONTROL Project Name]** opcional(a) y/o un(a) **[!UICONTROL Description]** opcional.

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Acerca de las clasificaciones de etiquetas](classification-about.md)
>* [Crear una clasificación de etiquetas](classification-create.md)
>* [Asignar valores de clasificación a componentes de cuenta mediante hojas de edición masiva](classification-values-assign-bulksheets.md)
>* [Quitar valores de clasificación de etiquetas de los componentes de la cuenta](classification-values-remove.md)
>* [Eliminar valores de clasificación de etiquetas](classification-values-delete.md)
>* [Eliminar clasificaciones de etiquetas](classification-delete.md)
