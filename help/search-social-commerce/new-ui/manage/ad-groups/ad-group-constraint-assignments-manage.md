---
title: Administrar asignaciones de restricción para grupos de anuncios
description: Obtenga información sobre cómo asignar restricciones a grupos de anuncios.
feature: Search Optimization, Search Campaign Management
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# (Nueva interfaz de usuario) Administrar asignaciones de restricciones para grupos de anuncios

*característica de Beta*

Puede asignar y eliminar restricciones de oferta para las siguientes entidades de búsqueda: campaña, grupo de publicidad, palabra clave, ubicación, grupo de productos de nivel de unidad y destino de búsqueda dinámica. Cada entidad solo puede tener una restricción.

Las restricciones las heredan las entidades secundarias, por lo que no es necesario asignar restricciones para entidades secundarias a menos que desee anular los valores heredados.

Al anular la asignación de una restricción, se elimina la asociación con los componentes de la cuenta y todos sus componentes secundarios, y los datos del informe de la restricción ya no están disponibles para dichos componentes. Al anular la asignación de una restricción, no se eliminan ni la restricción ni los propios componentes de la cuenta.

## Asignar una restricción a los grupos de anuncios seleccionados desde la nueva vista [!UICONTROL Ad Groups]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Active la casilla de verificación situada junto a cada grupo de anuncios al que va a asignar una única restricción.

1. En la barra de herramientas, haga clic en ![Más acciones](/help/search-social-commerce/assets/more-actions.png "Más acciones") **[!UICONTROL More Actions]** > ![Asignar](/help/search-social-commerce/assets/assign.png "Asignar") **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

## Asignar una restricción a las unidades de oferta de búsqueda seleccionadas desde las vistas heredadas de [!UICONTROL Campaigns]

1. En **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, seleccione la vista del componente de cuenta.

1. Seleccione la casilla de verificación situada junto a cada fila correspondiente.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Seleccione la restricción aplicable.

1. (Opcional) Introduzca detalles adicionales:

   1. Junto a [!UICONTROL Additional Details], haga clic en **[!UICONTROL Open]** para expandir los detalles.

   1. Escriba un(a) **[!UICONTROL Project Name]** opcional(a) y/o un(a) **[!UICONTROL Description]** opcional.

1. Haga clic en **[!UICONTROL Save]**.

## Quitar la asignación de restricciones de grupos de anuncios seleccionados de la nueva vista [!UICONTROL Ad Groups]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de anuncios del que anulará la asignación de restricciones.

1. En la barra de herramientas, haga clic en ![Más acciones](/help/search-social-commerce/assets/more-actions.png "Más acciones") **[!UICONTROL More Actions]** > ![Asignar](/help/search-social-commerce/assets/unassign.png "Desasignar") **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

## Quitar la asignación de restricciones de las unidades de oferta de búsqueda de las vistas heredadas de [!UICONTROL Campaigns]

>[!NOTE]
>
>Para eliminar una restricción, de modo que no esté disponible para uso futuro, consulte &quot;Eliminar restricciones para unidades de oferta de búsqueda&quot; en el capítulo Guía de optimización sobre &quot;Restricciones de oferta&quot;, que está disponible en Buscar, Social y Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. En **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, seleccione la vista del componente de cuenta.

1. Seleccione la casilla de verificación situada junto a cada componente del que desea quitar la restricción.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. En el diálogo de confirmación, seleccione **[!UICONTROL Yes, Unassign]**.

>[!MORELIKETHIS]
>
>* [Administrar asignaciones de restricción para campañas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
