---
title: Administrar destinatarios de audiencia para campañas y grupos de anuncios
description: Obtenga información sobre cómo configurar y administrar los destinatarios de audiencia para su [!DNL Google Ads] y [!DNL Microsoft® Advertising] campañas y grupos de publicidad.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: 0a858fb9437439d2755f1a9679b0849c614293b7
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Administre los destinatarios de audiencia para sus [!DNL Google Ads] y [!DNL Microsoft® Advertising] campañas y grupos de publicidad

*[!DNL Google Ads]y [!DNL Microsoft® Advertising] solamente*

[!DNL Google Ads] campañas y grupos de publicidad, y [!DNL Microsoft® Advertising] los grupos de anuncios pueden dirigirse a audiencias específicas desde la misma red de anuncios. La red de anuncios determina el tamaño de la audiencia a la que se debe dirigir.

>[!NOTE]
>
>Las exclusiones siempre anulan inclusiones/destinos.

Puede configurar los objetivos de audiencia, editar los modificadores de oferta para los objetivos de audiencia y cambiar el estado de los objetivos de audiencia.

## Configuración de destinatarios de audiencia

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Configure los objetivos de audiencia para campañas y grupos de anuncios específicos:

   1. Seleccione las audiencias aplicables para la red de anuncios especificada.

      Si lo desea, puede buscar audiencias que contengan una cadena de texto específica con un mínimo de tres caracteres. Para cualquier audiencia coincidente, haga clic en **[!UICONTROL Include]** para seleccionarlo.

      [!DNL Google Ads] las audiencias de coincidencia de cliente solo están disponibles para campañas de búsqueda y compra.

   1. Especifique los objetivos:

      1. (Opcional) Para expandir una campaña y sus grupos de anuncios secundarios, haga clic en el nombre de la campaña.

      1. (Opcional) Para filtrar una lista de campañas o de grupos de publicidad por una cadena de texto incluida en el nombre, haga clic en ![Filtrar](/help/search-social-commerce/assets/filter.png "Filtrar") , introduzca o pegue la cadena de texto en el campo de entrada y, a continuación, pulse el botón **[!UICONTROL Enter]** clave.

      1. Especifique el objetivo de cada campaña y grupo de publicidad para la red de publicidad especificada haciendo clic en el círculo vacío adyacente para que la marca de verificación azul (![Seleccionar](/help/search-social-commerce/assets/include.png "Seleccionar")) aparece.

      No se puede configurar un objetivo tanto para una campaña principal como para un grupo de anuncios secundarios (que utiliza automáticamente el objetivo).

1. Clic **[!UICONTROL Post]**.

1. (Opcional) Defina un ajuste de oferta para el objetivo de una de las siguientes maneras desde el [!UICONTROL Targets] ver:

   * Haga clic en en **[!UICONTROL Bid Adjustment]** y escriba un valor.

   * Seleccione la casilla de verificación situada junto a la fila de destino. En la barra de herramientas, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar"), introduzca el modificador de oferta y haga clic en **[!UICONTROL Post]**.

   Los valores pueden incluir:

   * *0 %:* No ajustar las ofertas de anuncios para esta audiencia.

   * /[*Otros valores desde -90% a 900%*/]: Para aumentar o reducir la oferta de anuncios para esta audiencia. Por ejemplo, si la oferta en el nivel de palabra clave es 1 USD y el ajuste de oferta para un objetivo de audiencia específico es del 50 %, la oferta para esa audiencia aumenta a 1,50 USD.

## Editar el modificador de oferta para destinos de audiencia

Puede cambiar el modificador de oferta y el estado de los objetivos de audiencia para todos los tipos de audiencia, excepto para las audiencias de mercado.

>[!NOTE]
>
>Search, Social y Commerce optimizan automáticamente el modificador de oferta cuando la campaña principal utiliza la estrategia de oferta de CPC y está en un portafolio configurado para optimizar automáticamente los valores de ajuste de oferta para los objetivos de audiencia.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Realice una de las acciones siguientes:

   * Para editar un modificador de oferta para un destino, haga clic en en **[!UICONTROL Bid Adjustment]** y editar el ajuste de oferta.

   * Para editar un modificador de oferta para uno o más destinos, haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada destino que desee editar.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

      1. Edite el **[!UICONTROL Bid Modifier]** y/o **[!UICONTROL Status]** campos.

         Para el [!UICONTROL Bid Modifier] , tiene opciones para cambiar los valores existentes a un valor especificado o para aumentar o disminuir el importe en un porcentaje o importe monetario especificados, con un límite.

         Para un valor definido, el valor puede incluir:

         * *0 %:* No ajustar las ofertas de anuncios para esta audiencia.

         * /[*Otros valores desde -90% a 900%*/]: Para aumentar o reducir la oferta de anuncios para esta audiencia. Por ejemplo, si la oferta en el nivel de palabra clave es 1 USD y el ajuste de oferta para un objetivo de audiencia específico es del 50 %, la oferta para esa audiencia aumenta a 1,50 USD.

         Para varios destinos, los cambios se aplican a todos los destinos seleccionados.

      1. (Opcional) Haga clic en **[!UICONTROL Additional Details]** y, opcionalmente, introduzca un nombre y una descripción de proyecto.

      1. Clic **[!UICONTROL Post]**.

## Cambio del estado de los destinatarios de audiencia

Puede pausar un destinatario de audiencia activo para deshabilitar las pujas en él. Más tarde, puedes reanudar las pujas cambiando el estado de nuevo a activo.

También puede eliminar un destinatario de audiencia de búsqueda activo o pausado.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Opcional) Filtre la lista para incluir destinos de audiencia específicos.

1. Seleccione la casilla de verificación situada junto a cada destinatario de audiencia cuyo estado desee cambiar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. En la barra de herramientas, haga clic en el botón de estado:

   * Para activar las filas, haga clic en ![Activar](/help/search-social-commerce/assets/activate.png "Activar").

   * Para pausar las filas, haga clic en ![Pausar](/help/search-social-commerce/assets/pause.png "Pausar").

   * Para eliminar las filas, haga clic en ![Más acciones](/help/search-social-commerce/assets/more.png "Más acciones") y seleccione **[!UICONTROL Delete]**. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Administración de exclusiones de audiencia para campañas y grupos de anuncios](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
