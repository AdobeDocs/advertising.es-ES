---
title: Administración de exclusiones de audiencia para campañas y grupos de anuncios
description: Obtenga información sobre las exclusiones de audiencia de Google Ads y Microsoft Advertising, incluido cómo eliminar las exclusiones de Google Ads.
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
source-wordcount: '269'
ht-degree: 0%
---
# Administración de exclusiones de audiencia para campañas y grupos de anuncios

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo cuentas*

La exclusión de audiencias impide que se muestren anuncios en una campaña o grupo de anuncios a usuarios de una [audiencia](audience-manage.md) específica.

Para las cuentas de [!DNL Google Ads], puede excluir cualquier tipo de audiencia. Para las cuentas de [!DNL Microsoft Advertising], solo puede excluir audiencias de remarketing dinámico.

>[!NOTE]
>
>Las exclusiones siempre anulan [destinos de audiencia](audience-targets-manage.md).

## Acerca de la vista [!UICONTROL Exclusions] {#audience-exclusions-view-about}

La vista [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions] enumera las exclusiones de audiencia en la vista filtrada del anunciante seleccionado.

Para ver los datos se requiere el permiso [!UICONTROL View Audiences]. Para seleccionar filas y eliminar exclusiones compatibles se requiere el permiso [!UICONTROL Edit Audience Exclusions].

### Acciones disponibles

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [Eliminar exclusiones de audiencia](#audience-exclusions-delete)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## Eliminar exclusiones de audiencia {#audience-exclusions-delete}

*[!DNL Google Ads]exclusiones solamente*

Puede eliminar una o más [!DNL Google Ads] exclusiones de audiencia. No se admite la eliminación de [!DNL Microsoft Advertising] exclusiones en esta vista.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Audiences]** y luego haga clic en la ficha **[!UICONTROL Exclusions]**.

1. (Opcional) Filtre la lista para incluir exclusiones de audiencia específicas.

1. Seleccione la casilla de verificación situada junto a cada exclusión [!DNL Google Ads] que desee eliminar. No incluya exclusiones de otra red publicitaria en la selección.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Administrar audiencias](audience-manage.md)
>* [Administrar destinatarios de audiencia para campañas y grupos de anuncios](audience-targets-manage.md)
