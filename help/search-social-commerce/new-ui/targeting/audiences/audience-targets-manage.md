---
title: Administrar destinatarios de audiencia para campañas y grupos de anuncios
description: Obtenga información sobre cómo administrar los objetivos de audiencia y sus ajustes de oferta para Google Ads y Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%
---
# Administrar destinatarios de audiencia para campañas y grupos de anuncios

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo cuentas*

[!DNL Google Ads] campañas y grupos de anuncios, y [!DNL Microsoft Advertising] grupos de anuncios, pueden dirigirse a [audiencias](audience-manage.md) específicas desde la misma red de anuncios. La red de anuncios determina el tamaño de la audiencia a la que se debe dirigir.

Un público objetivo asocia una audiencia existente con una campaña o un grupo de publicidad. Puede editar el ajuste de oferta y el estado de los destinos existentes.

>[!NOTE]
>
>[Las exclusiones de audiencia](audience-exclusions.md) siempre anulan los destinos.

## Acerca de la vista [!UICONTROL Targets] {#audience-targets-view-about}

La vista [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets] enumera los destinos de audiencia en la vista filtrada para el anunciante seleccionado.

Para ver los datos se requiere el permiso [!UICONTROL View Audiences]. Editar, cambiar el estado y eliminar destinos requieren el permiso [!UICONTROL Edit Audience Targets].

### Acciones disponibles

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [Editar los ajustes y el estado de las ofertas de audience target](#audience-targets-edit)

* [Cambiar el estado de los objetivos de audiencia o eliminarlos](#audience-targets-status)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## Editar los ajustes y el estado de las ofertas de audience target {#audience-targets-edit}

Puede editar uno o más objetivos de audiencia a la vez. Los cambios se aplican a todos los destinos seleccionados.

>[!NOTE]
>
>Search, Social y Commerce optimizan automáticamente el modificador de oferta cuando la campaña principal utiliza la estrategia de oferta de CPC y está en un portafolio configurado para optimizar automáticamente los valores de ajuste de oferta para los objetivos de audiencia. Los modificadores de oferta para [!DNL Microsoft Advertising] destinos de audiencia de remarketing dinámico no están optimizados.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Audiences]** y luego haga clic en la ficha **[!UICONTROL Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino que desee editar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. Edite **[!UICONTROL Bid Modifier]**, **[!UICONTROL Status]** o ambos. Ver [editar configuración](#audience-targets-edit-settings).

   Deje un campo sin cambiar para conservar el valor existente.

1. (Opcional) Expanda **[!UICONTROL ADDITIONAL DETAILS]** e introduzca **[!UICONTROL Project Name]** y **[!UICONTROL Description]**.

1. Haga clic en **[!UICONTROL Save]**.

También puede editar el ajuste de oferta de un solo destino directamente en la tabla de datos haciendo clic en su valor en la columna **[!UICONTROL Bid Adjustment]**.

## Cambiar el estado de los objetivos de audiencia o eliminarlos {#audience-targets-status}

Puede pausar un público objetivo activo para deshabilitar las pujas por ese destino y luego reanudarlas activándolo. También puede eliminar destinos activos o en pausa.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Audiences]** y luego haga clic en la ficha **[!UICONTROL Targets]**.

1. (Opcional) Filtre la lista para incluir destinos de audiencia específicos.

1. Seleccione la casilla de verificación situada junto a cada destino cuyo estado desee cambiar.

1. En la barra de herramientas de acciones masivas, haga clic en una de las siguientes opciones:

   * **[!UICONTROL Activate]** para activar los destinos seleccionados.

   * **[!UICONTROL Pause]** para pausar los destinos seleccionados.

   * **[!UICONTROL Delete]** para eliminar los destinos seleccionados.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

## Configuración de edición de destino de audiencia {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]:** Cómo cambiar el ajuste de oferta de audiencia:

* *[!UICONTROL Set To]:* Reemplazar el ajuste de oferta existente con el porcentaje especificado.

* *[!UICONTROL Increase]:* Aumente el valor existente en el porcentaje especificado.

* *[!UICONTROL Decrease]:* Reducir el valor existente en el porcentaje especificado.

Para [!UICONTROL Increase] y [!UICONTROL Decrease], escriba un valor no negativo.

Para un valor establecido, el 0 % no ajusta la oferta. Otros valores admitidos van del -90 % al 900 %. Por ejemplo, si la oferta en el nivel de palabra clave es 1 USD y el ajuste de oferta de audiencia es 50 %, la oferta para esa audiencia aumenta a 1,50 USD.

**[!UICONTROL Status]:** Selecciona **[!UICONTROL Active]** para habilitar la puja o **[!UICONTROL Paused]** para deshabilitar la puja para el destino.

>[!MORELIKETHIS]
>
>* [Administrar audiencias](audience-manage.md)
>* [Administrar exclusiones de audiencia para campañas y grupos de anuncios](audience-exclusions.md)
