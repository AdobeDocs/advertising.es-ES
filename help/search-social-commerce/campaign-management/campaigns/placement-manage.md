---
title: Administrar [!DNL Google Ads] ubicaciones
description: Aprenda a crear y administrar ubicaciones que se pueden pujar para  [!DNL Google Ads] grupos de anuncios.
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Administrar [!DNL Google Ads] ubicaciones

*[!DNL Google Ads]solo cuentas*

Puede crear y editar ubicaciones para grupos de anuncios en [tipos de campañas compatibles](/help/search-social-commerce/introduction/supported-inventory.md) que tengan como destino la red de visualización dentro de una [cuenta de red de publicidad sincronizada](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Crear [!DNL Google Ads] ubicaciones

>[!TIP]
>
>Para crear muchas ubicaciones a la vez, use [hojas de edición masiva de Campaign](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. &#x200B;
   1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red de anuncios, la cuenta, la campaña y el grupo de anuncios y haga clic en **[!UICONTROL Continue]**.

1. Configure [la configuración de ubicación](#placement-settings).

1. Haga clic en **[!UICONTROL Post]**.

## Editar [!DNL Google Ads] ubicaciones

>[!TIP]
>
>Para editar muchas ubicaciones a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Seleccione la casilla de verificación situada junto a cada fila que desee editar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar") .

1. Edite la [configuración de ubicación](#placement-settings).

   Para varias ubicaciones, los cambios se aplicarán a todas las ubicaciones seleccionadas. Para algunos campos alfanuméricos, puede cambiar los valores existentes a un valor especificado, reemplazar una cadena existente por una cadena especificada, agregar un prefijo especificado al principio de cada valor o anexar un sufijo al final de cada valor. Para algunos campos monetarios, puede cambiar los valores existentes a un valor especificado o aumentar o disminuir el importe en un porcentaje o importe monetario especificados, con un límite.

1. Guarde los datos:

   * (Ubicaciones únicas) Haga clic en **[!UICONTROL Post]**.

   * (Varias ubicaciones) Haga clic en **[!UICONTROL Post Now]**.

## Configuración de ubicación {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** sitios en la red de contenido en los que puede aparecer el anuncio. Escriba una dirección URL válida, como www.example.com, example.com o www.example.com/shoes/kids. Para especificar varias cadenas, sepárelas con comas o introdúzcalas en líneas independientes. La dirección URL no puede incluir el signo de interrogación (`?`). **Nota:** Puede [excluir las ubicaciones del sitio web](placement-negative-create.md) desde la vista [!UICONTROL Placements] > [!UICONTROL Negatives] y en la configuración del grupo de anuncios y de la campaña.

**[!UICONTROL Status]:** El estado de visualización de la ubicación: *Activa* (para habilitar la oferta; la predeterminada), *En pausa* (para deshabilitar la oferta) o *Eliminada* (para eliminar la ubicación; solo las ubicaciones existentes).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (opcional) coste por clic (CPC) o coste por mil impresiones visibles (vCPM) para el anuncio basado en la ubicación, según la estrategia de oferta de campaña. Este valor anula la oferta de nivel de grupo de anuncios.

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Acerca de las ubicaciones](placement-about.md)
>* [Crear ubicaciones negativas](placement-negative-create.md)
>* [Cambiar el estado de las ubicaciones y las ubicaciones negativas](placement-status-edit.md)
