---
title: Administrar [!DNL Google Ads] destinos de búsqueda dinámica
description: Obtenga información sobre cómo crear y administrar [!DNL Google Ads] destinos de búsqueda dinámica.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Administrar [!DNL Google Ads] destinos de búsqueda dinámica

*[!DNL Google Ads]solo cuentas*

Puede crear, editar y cambiar el estado de los destinos de búsqueda dinámica para las campañas que utilizan la red de búsqueda.

>[!NOTE]
>
>Puede crear y editar grandes cantidades de datos de destino a la vez cargando [archivos de hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) y publicarlos en la red publicitaria.

## Crear un [!DNL Google Ads] destino de búsqueda dinámica

Puede crear objetivos de búsqueda dinámica para definir páginas en sus sitios web (es decir, los dominios utilizados en las URL de visualización de sus anuncios) cuyo contenido se utilice para segmentar los anuncios de búsqueda dinámica en el mismo grupo de anuncios.

Puede segmentar todos los criterios o hasta tres criterios individuales.

>[!NOTE]
>
>Para realizar el mejor seguimiento del rendimiento, cree un &quot;[!UICONTROL All Targets]&quot; destinatario solo para un grupo de anuncios por campaña.

>[!TIP]
>
>Para crear muchos componentes de cuenta a la vez, utilice [hojas de campaña](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red de anuncios, la cuenta, la campaña y el grupo de anuncios y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Especifique el [configuración de dynamic search target](#dynamic-search-target-settings).

1. Haga clic **[!UICONTROL Post]**.

## Editar [!DNL Google Ads] configuración de dynamic search target

Puede editar el estado o la puja máxima de un [!DNL Google Ads] destino de búsqueda dinámica. No puede cambiar los criterios a los que se dirige.

>[!TIP]
>
>Para editar grandes cantidades de datos a la vez, utilice [hojas de campaña](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada fila que desee editar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Especifique el [configuración de dynamic search target](#dynamic-search-target-settings).

   Para varios destinos, los cambios se aplican a todos los destinos seleccionados. Para el [!UICONTROL Bid field], tiene opciones para cambiar los valores existentes a un valor especificado o para aumentar o disminuir el importe en un porcentaje o importe monetario especificados, con un límite.

1. Guarde los datos:

   * (Destinos únicos) Haga clic en **[!UICONTROL Post]**.

   * (Varios grupos de anuncios) Haga clic en **[!UICONTROL Post Now]**.

## Cambiar el estado de [!DNL Google Ads] destinos de búsqueda dinámica

Puede pausar cualquier destino de búsqueda dinámica activo en un tipo de campaña compatible para que no se utilicen para los anuncios de búsqueda dinámica en el mismo grupo de anuncios. Más adelante, podrá utilizarlos como objetivos cambiando el estado del anuncio de nuevo a Activo.

También puede eliminar cualquier destino dinámico.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Opcional) Filtre la lista para incluir destinos dinámicos específicos.

1. Realice una de las acciones siguientes:

   * Para cambiar el estado de un destino dinámico, haga clic en en **[!UICONTROL Status]** y cambie el estado.

   * Para eliminar uno o más destinos dinámicos, haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada destino dinámico que desee eliminar.
      Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. En la barra de herramientas, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más") y seleccione **[!UICONTROL Delete]**.

      1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.


## [!DNL Google Ads] configuración de dynamic search target {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Necesario cuando no se especifica un dominio de sitio web ni un idioma en la [!UICONTROL DSA Options] sección; solo lectura para destinos existentes) Destinos de búsqueda dinámica para el grupo de anuncios:

* *[!UICONTROL All Targets]* (valor predeterminado): Segmenta todas las páginas indexadas.

* *\[Destinos específicos\]:* Selecciona hasta tres criterios para las páginas indizadas. Al seleccionar esta opción, se deben especificar los criterios especificando las categorías de información y los valores específicos a los que se deben dirigir los anuncios (por ejemplo, &quot;la URL contiene zapatos.ejemplo.com&quot;). Para especificar varios criterios, haga clic en **[!UICONTROL + And]**. Los criterios de destino incluyen:

   * *[!UICONTROL Category]:* Para mostrar anuncios de páginas indexadas con un [!DNL Google Ads] categoría de contenido.

   * *[!UICONTROL URL]:* Para mostrar anuncios de páginas indexadas con una dirección URL específica, donde el valor puede incluirse en cualquier lugar de la dirección URL.

   * *[!UICONTROL Page Title]:* Para mostrar anuncios para páginas indizadas con texto específico en el título de la página.

   * *[!UICONTROL Page Content]:* Para mostrar anuncios para páginas indizadas con contenido específico.

**Estado:** El estado de la configuración de destinatario:

* *[!UICONTROL Active]* (el valor predeterminado): Habilita las ofertas.

* *[!UICONTROL Paused]:* Desactiva las pujas.

* *[!UICONTROL Deleted]* (solo destinos existentes): elimina la configuración de destinos.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** El coste por clic (CPC) máximo de un anuncio o el coste por 1000 impresiones (CPM) de un anuncio, según corresponda para el modelo de precios de la campaña y la red de anuncios. Este valor anula el valor de nivel de grupo de anuncios.

>[!NOTE]
>
>Si el objetivo está en un portafolio optimizado, la oferta CPC especificada se aplica por un día. Después, la capacidad de optimización coloca las ofertas según sus propios cálculos.

>[!MORELIKETHIS]
>
>* [Acerca de [!DNL Google Ads] destinos de búsqueda dinámica](dynamic-search-target-about.md)

