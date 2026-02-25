---
title: Quitar valores de clasificación de etiquetas de componentes de cuenta
description: Obtenga información sobre cómo eliminar asociaciones entre valores de clasificación de etiquetas y componentes de cuenta.
exl-id: 8697367b-0bf9-48c9-8dd3-e733360e1df2
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Quitar valores de clasificación de etiquetas de componentes de cuenta

Al eliminar un valor de clasificación, se elimina la asociación con el componente de cuenta y todos sus componentes secundarios. Los datos del informe para el valor de clasificación ya no están disponibles para esos componentes. Al eliminar un valor de clasificación, no se elimina el valor ni los componentes de la cuenta.

>[!NOTE]
>
>Para eliminar un valor de una clasificación de etiquetas, consulte &quot;[Eliminar valores de clasificación de etiquetas](classification-values-delete.md)&quot;.

## (Nueva IU) Quitar los valores de clasificación de etiquetas de los componentes de cuenta

Puede quitar los valores de clasificación de cualquier componente de cuenta aplicable que esté disponible en la nueva interfaz de usuario.

1. Abra la vista de entidades desde el menú **[!UICONTROL Manage]** o **[!UICONTROL Target]**.

1. Seleccione la casilla de verificación situada junto a cada fila correspondiente.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleccione la casilla de verificación situada junto a cada valor de clasificación que desee quitar de las entidades seleccionadas.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Para seleccionar todos los valores asignados, haga clic en **[!UICONTROL Select All]**. Para anular la selección de todos los valores asignados, haga clic en **[!UICONTROL Deselect All]**.

1. Haga clic en **[!UICONTROL Unassign Selected]**.

## (IU heredada) Quitar los valores de clasificación de etiquetas de los componentes de cuenta

1. En **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, seleccione la vista de entidad.

1. Realice una de las acciones siguientes:

   * (Para quitar valores de una sola entidad) Mantenga el cursor sobre el nombre de la entidad, haga clic en ![Botón de menú](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Botón de menú") y, a continuación, seleccione **[!UICONTROL Classification]**.

   * (Para quitar valores de una o varias entidades) Haga lo siguiente:

      * Active la casilla de verificación situada junto a cada fila.

        Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      * En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más") y, a continuación, haga clic en **[!UICONTROL Classification]**.

1. En [!UICONTROL Assignment Details], seleccione **[!UICONTROL Remove]**.

1. Para que se elimine cada valor de clasificación, haga lo siguiente:

   * En la columna **[!UICONTROL Classification]**, haga clic en el nombre de la clasificación para expandirla.

   * En la columna **[!UICONTROL Value Name]**, haga clic en el nombre del valor para seleccionarlo.

1. (Opcional) Introduzca detalles adicionales:

   * Junto a **[!UICONTROL Additional Details]**, haz clic en ![Abrir](/help/search-social-commerce/assets/chevron-up.png "Abrir") para ampliar los detalles.

   * Escriba un(a) **[!UICONTROL Project Name]** opcional(a) y/o un(a) **[!UICONTROL Description]** opcional.

   * Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Acerca de las clasificaciones de etiquetas](classification-about.md)
>* [Crear una clasificación de etiquetas](classification-create.md)
>* [Asignar valores de clasificación a componentes de cuenta desde las vistas de administración de campañas](classification-values-assign-campaign-management.md)
>* [Asignar valores de clasificación a componentes de cuenta mediante hojas de edición masiva](classification-values-assign-bulksheets.md)
>* [Eliminar valores de clasificación de etiquetas](classification-values-delete.md)
>* [Eliminar clasificaciones de etiquetas](classification-delete.md)
