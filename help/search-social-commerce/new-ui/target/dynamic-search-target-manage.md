---
title: Administrar  [!DNL Google Ads] destinos de búsqueda dinámica
description: Aprenda a crear y administrar  [!DNL Google Ads] destinos de búsqueda dinámica.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
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
source-wordcount: 702
ht-degree: 0%

---

# Administrar [!DNL Google Ads] destinos de búsqueda dinámica

*[!DNL Google Ads]solo cuentas*

Puede crear, editar y cambiar el estado de los destinos de búsqueda dinámica de [!DNL Google Ads] campañas que usan la red de búsqueda.

## ¿Qué son los destinos de búsqueda dinámica?

Los objetivos de búsqueda dinámica definen si la red de anuncios utiliza todas las páginas del sitio web o un subconjunto de ellas para segmentar los anuncios de búsqueda dinámica. Configure los objetivos de búsqueda dinámica en el nivel de grupo de anuncios; se aplican a todos los anuncios de búsqueda dinámica en el mismo grupo de anuncios.

Según la configuración de la campaña, los destinos de búsqueda dinámica pueden ser obligatorios u opcionales:

* Debe crear destinos de búsqueda dinámica cuando no especifique un dominio de sitio web ni un idioma en la sección &quot;[!UICONTROL DSA Options]&quot; de la campaña.

* Si lo desea, puede crear destinos de búsqueda dinámica cuando especifique un dominio de sitio web y un idioma en la sección &quot;[!UICONTROL DSA Options]&quot; de la campaña.

  [!DNL Google Ads] muestra automáticamente sus anuncios dinámicos de búsqueda en función del contenido de un sitio web especificado con esta configuración.

Para realizar el mejor seguimiento del rendimiento, configure la campaña con un grupo de anuncios por cada destino de búsqueda dinámica e incluya un grupo de anuncios que se ajuste a todos los criterios.

Para obtener más información sobre [!DNL Google Ads] anuncios dinámicos de búsqueda, consulte https://support.google.com/google-ads/answer/2471185.

## La vista [!UICONTROL Auto Targets]

La vista [!UICONTROL Target] > [!UICONTROL Auto Targets] enumera todos los destinos de búsqueda dinámica en la vista filtrada de la cuenta de anunciante seleccionada. También puede administrar sus destinos de búsqueda dinámica.

### Acciones disponibles

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [Asignar restricciones](#constraint-assign) a los destinos de búsqueda dinámica y [quitar restricciones](#constraint-unassign) de los destinos de búsqueda dinámica

* [Asignar clasificaciones de etiquetas](#classification-values-assign) a destinos de búsqueda dinámica y [quitar clasificaciones de etiquetas](#classification-values-remove) de destinos de búsqueda dinámica

>[!NOTE]
>
>Puede crear y editar grandes cantidades de datos de destino (incluidas asignaciones de etiquetas y restricciones) de una sola vez cargando [archivos de hojas de edición masiva](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) y publicándolos en la red publicitaria.

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## Asignar una restricción a los destinos de búsqueda dinámica seleccionados desde la nueva vista [!UICONTROL Auto Targets] {#constraint-assign}

1. En el menú principal, haga clic en **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino de búsqueda dinámica al que desee asignar una única restricción.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

## Quitar restricciones de los destinos de búsqueda dinámica seleccionados de la nueva vista [!UICONTROL Auto Targets] {#constraint-unassign}

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino de búsqueda dinámica del que anulará la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

## Asignar valores de clasificación a destinos de búsqueda dinámica {#classification-values-assign}

>[!NOTE]
>
>Las entidades secundarias heredan los valores de etiquetas, por lo que no introduzca valores para entidades secundarias a menos que desee anular los valores heredados.

1. En el menú principal, haga clic en **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino de búsqueda dinámica al que desee asignar un valor de etiqueta.

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

## Quitar valores de clasificación de etiquetas de destinos de búsqueda dinámica {#classification-values-remove}

Al eliminar un valor de clasificación, se elimina la asociación con el componente de cuenta y todos sus componentes secundarios. Los datos del informe para el valor de clasificación ya no están disponibles para esos componentes. Al eliminar un valor de clasificación, no se elimina el valor ni los componentes de la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino de búsqueda dinámica desde la que desea quitar un valor de etiqueta.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleccione la casilla de verificación situada junto a cada valor de clasificación que desee eliminar de las entidades seleccionadas.

   Para seleccionar todos los valores asignados, haga clic en **[!UICONTROL Select All]**. Para anular la selección de todos los valores asignados, haga clic en **[!UICONTROL Deselect All]**.

1. Haga clic en **[!UICONTROL Unassign Selected]**.

>[!MORELIKETHIS]
>
>* [(Nueva IU) Administrar restricciones para buscar unidades de oferta](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nueva IU) Administrar clasificaciones de etiquetas](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
