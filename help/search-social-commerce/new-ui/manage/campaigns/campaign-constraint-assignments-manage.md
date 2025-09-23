---
title: Administrar asignaciones de restricción para campañas
description: Aprenda a asignar restricciones a las campañas.
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: d886a228-24d7-4d8e-b68a-76e56b4304ed
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# (Nueva IU) Administrar asignaciones de restricciones para campañas

*característica de Beta*

Puede asignar y eliminar restricciones de oferta para las siguientes entidades de búsqueda: campaña, grupo de publicidad, palabra clave, ubicación, grupo de productos de nivel de unidad y destino de búsqueda dinámica. Cada entidad solo puede tener una restricción.

Las restricciones las heredan las entidades secundarias, por lo que no es necesario asignar restricciones para entidades secundarias a menos que desee anular los valores heredados.

Al anular la asignación de una restricción, se elimina la asociación con los componentes de la cuenta y todos sus componentes secundarios, y los datos del informe de la restricción ya no están disponibles para dichos componentes. Al anular la asignación de una restricción, no se eliminan ni la restricción ni los propios componentes de la cuenta.

>[!NOTE]
>
>* Si posteriormente edita una palabra clave o la copia de anuncio de un anuncio (creando así una nueva palabra clave o anuncio), la restricción no se asigna a la nueva entidad.
>* Las restricciones activas restringen las ofertas solo para las unidades de oferta asignadas en portafolios optimizados de nivel de palabra clave heredados. Se ignoran para las unidades de oferta que están en portafolios activos, en portafolios híbridos o que no están en portafolios.

## Asignar una restricción a las campañas seleccionadas desde la nueva vista [!UICONTROL Campaigns]

Puede asignar una sola restricción a una o varias campañas.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña a la que desea asignar una sola restricción.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

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

## Quitar la asignación de restricciones de campañas seleccionadas de la nueva vista [!UICONTROL Campaigns]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña para anular la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

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
>* [Administrar asignaciones de restricción para grupos de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
