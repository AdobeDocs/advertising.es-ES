---
title: Administrar destinatarios de audiencia para campañas y grupos de anuncios
description: Aprenda a configurar y administrar los objetivos de audiencia para sus  [!DNL Google Ads] campañas y grupos de anuncios [!DNL Microsoft Advertising] y.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Administrar destinos de audiencia para sus campañas y grupos de anuncios [!DNL Google Ads] y [!DNL Microsoft Advertising]

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solamente*

[!DNL Google Ads] campañas y grupos de anuncios, y [!DNL Microsoft Advertising] grupos de anuncios, pueden dirigirse a audiencias específicas desde la misma red de anuncios. La red de anuncios determina el tamaño de la audiencia a la que se debe dirigir.

>[!NOTE]
>
>Las exclusiones siempre anulan inclusiones/destinos.

Puede configurar los objetivos de audiencia, editar los modificadores de oferta para los objetivos de audiencia y cambiar el estado de los objetivos de audiencia.

## Configuración de destinatarios de audiencia

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Configure los objetivos de audiencia para campañas y grupos de anuncios específicos:

   1. Seleccione las audiencias aplicables para la red de anuncios especificada.

      Si lo desea, puede buscar audiencias que contengan una cadena de texto específica con un mínimo de tres caracteres. Para cualquier audiencia que coincida, haga clic en **[!UICONTROL Include]** para seleccionarlo.

      Las audiencias de coincidencia de cliente de [!DNL Google Ads] solo están disponibles para campañas de búsqueda y compras.

   1. Especifique los objetivos:

      1. (Opcional) Para expandir una campaña y sus grupos de anuncios secundarios, haga clic en el nombre de la campaña.

      1. (Opcional) Para filtrar una lista de campañas o de grupos de anuncios por una cadena de texto incluida en el nombre, haga clic en ![Filtrar](/help/search-social-commerce/assets/filter.png "Filtrar") , escriba o pegue la cadena de texto en el campo de entrada y, a continuación, presione la tecla **[!UICONTROL Enter]**.

      1. Especifique el destino de cada campaña y grupo de anuncios para la red de anuncios especificada haciendo clic en el círculo vacío adyacente para que aparezca una marca de verificación azul (![Select](/help/search-social-commerce/assets/include.png "Select")).

      No se puede configurar un objetivo tanto para una campaña principal como para un grupo de anuncios secundarios (que utiliza automáticamente el objetivo).

1. Haga clic en **[!UICONTROL Post]**.

1. (Opcional) Defina un ajuste de oferta para el destino de una de las siguientes maneras desde la vista [!UICONTROL Targets]:

   * Haga clic en la columna **[!UICONTROL Bid Adjustment]** e introduzca un valor.

   * Seleccione la casilla de verificación situada junto a la fila de destino. En la barra de herramientas , haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar"), escriba el modificador de oferta y, a continuación, haga clic en **[!UICONTROL Post]**.

   Los valores pueden incluir:

   * *0%:* Para no ajustar las ofertas de anuncios para esta audiencia.

   * /[*Otros valores del -90% al 900%*/]: Para aumentar o reducir la oferta de anuncios para esta audiencia. Por ejemplo, si la oferta en el nivel de palabra clave es 1 USD y el ajuste de oferta para un objetivo de audiencia específico es del 50 %, la oferta para esa audiencia aumenta a 1,50 USD.

## Editar el modificador de oferta para destinos de audiencia

Puede cambiar el modificador de oferta y el estado de los objetivos de audiencia para todos los tipos de audiencia, excepto para las audiencias de mercado.

>[!NOTE]
>
>Search, Social y Commerce optimizan automáticamente el modificador de oferta cuando la campaña principal utiliza la estrategia de oferta de CPC y está en un portafolio configurado para optimizar automáticamente los valores de ajuste de oferta para los objetivos de audiencia.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Realice una de las acciones siguientes:

   * Para editar un modificador de oferta para un destino, haga clic en la columna **[!UICONTROL Bid Adjustment]** y edite el ajuste de oferta.

   * Para editar un modificador de oferta para uno o más destinos, haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada destino que desee editar.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

      1. Edite los campos **[!UICONTROL Bid Modifier]** o **[!UICONTROL Status]**.

         Para el campo [!UICONTROL Bid Modifier], tiene opciones para cambiar los valores existentes a un valor especificado o para aumentar o disminuir la cantidad en un porcentaje o importe monetario especificados, con un límite.

         Para un valor definido, el valor puede incluir:

         * *0%:* Para no ajustar las ofertas de anuncios para esta audiencia.

         * /[*Otros valores del -90% al 900%*/]: Para aumentar o reducir la oferta de anuncios para esta audiencia. Por ejemplo, si la oferta en el nivel de palabra clave es 1 USD y el ajuste de oferta para un objetivo de audiencia específico es del 50 %, la oferta para esa audiencia aumenta a 1,50 USD.

         Para varios destinos, los cambios se aplican a todos los destinos seleccionados.

      1. (Opcional) Haga clic en **[!UICONTROL Additional Details]** y, opcionalmente, escriba un nombre y una descripción para el proyecto.

      1. Haga clic en **[!UICONTROL Post]**.

## Cambio del estado de los destinatarios de audiencia

Puede pausar un destinatario de audiencia activo para deshabilitar las pujas en él. Más tarde, puedes reanudar las pujas cambiando el estado de nuevo a activo.

También puede eliminar un destinatario de audiencia de búsqueda activo o pausado.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Opcional) Filtre la lista para incluir destinos de audiencia específicos.

1. Seleccione la casilla de verificación situada junto a cada destinatario de audiencia cuyo estado desee cambiar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas, haga clic en el botón de estado:

   * Para activar las filas, haga clic en ![Activar](/help/search-social-commerce/assets/activate.png "Activar").

   * Para pausar las filas, haga clic en ![Pausar](/help/search-social-commerce/assets/pause.png "Pausar").

   * Para eliminar las filas, haga clic en ![Más acciones](/help/search-social-commerce/assets/more.png "Más acciones") y seleccione **[!UICONTROL Delete]**. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Administrar exclusiones de audiencia para campañas y grupos de anuncios](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
