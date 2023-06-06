---
title: Administrar [!DNL Microsoft Advertising] audiencias de remarketing dinámico
description: Obtenga información sobre cómo crear y administrar [!DNL Microsoft Advertising] audiencias de remarketing dinámico.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Administrar [!DNL Microsoft Advertising] audiencias de remarketing dinámico

*[!DNL Microsoft Advertising]solo cuentas*

Puede crear un [!DNL Microsoft Advertising] audiencia de remarketing dinámico cuando se utiliza la etiqueta de seguimiento de conversión y audiencia de JavaScript del motor de búsqueda en las páginas web. Cada audiencia se crea con una etiqueta especificada que se incluye en las páginas web cuyos usuarios forman la audiencia. Puede crear varias audiencias con la misma etiqueta de seguimiento. También puede cambiar el nombre y la fuente de datos de las audiencias existentes, o eliminar las audiencias existentes.

Las audiencias de remarketing dinámico tienen el Tipo de audiencia &quot;[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>&quot; (como &quot;Remarketing dinámico de compradores anteriores&quot;).

Para obtener más información sobre el remarketing dinámico y cómo implementar la etiqueta JavaScript necesaria, consulte la [[!DNL Microsoft Advertising] documentación sobre remarketing dinámico](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Creación de una audiencia de remarketing dinámica

>[!NOTE]
>
>Para [!DNL Microsoft Advertising] cuentas, la etiqueta JavaScript debe incluir el [Parámetros de ID de producto y tipo de página](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifique el nombre del [!DNL Microsoft Advertising] etiqueta de seguimiento universal de eventos (UET) incluida en las páginas web desde las que se creará la audiencia.

   Necesitará el nombre de la etiqueta en un paso posterior.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Especifique la información de la audiencia:

   1. En el **[!UICONTROL Data Source]** menú, seleccione **[!UICONTROL Dynamic Remarketing List]**.

   1. Introduzca el **[!UICONTROL Audience Name]**.

   1. De una lista de todas las etiquetas disponibles para la cuenta de motor de búsqueda, seleccione el nombre del [!DNL Microsoft Advertising] Etiqueta de UET que se incluye en las páginas web cuyos usuarios formarán la audiencia.

   1. Seleccione el tipo de visitante para la audiencia, que se basa en las acciones del visitante en las páginas web relevantes: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, o *[!UICONTROL Shopping Cart Abandoners]*.

   1. Especifique el número de **[!UICONTROL Membership Days]**, que es el número de días que la cookie de un usuario permanece en la audiencia. Los valores pueden variar de uno (1) a 180.

      Utilice el periodo de tiempo durante el cual espera que el anuncio sea relevante para el usuario.

1. Haga clic **[!UICONTROL Post]**.

>[!NOTE]
>
>Su [!DNL Microsoft Advertising] las listas de remarketing dinámico son aptas para la segmentación una vez que incluyen al menos 300 usuarios.

## Edición de una audiencia de remarketing dinámico

Puede cambiar el nombre y la fuente de datos de una [!DNL Microsoft Advertising] audiencia de remarketing dinámico. No se puede editar el valor de [!UICONTROL Membership Days] configuración.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Seleccione la casilla de verificación situada junto a la audiencia que desea editar.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite la información de la audiencia:

   1. En el **[!UICONTROL Data Source]** , haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

   1. (Opcional) Cambie el **[!UICONTROL Audience Name]**.

   1. (Opcional) Cambie el nombre de la cuenta de red de publicidad de una lista de todas las etiquetas disponibles [!DNL Microsoft Advertising] Etiqueta de UET que se incluye en las páginas web cuyos usuarios formarán la audiencia.

   1. (Opcional) Cambie el tipo de visitante para la audiencia, que se basa en las acciones del visitante en las páginas web relevantes: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, o *[!UICONTROL Shopping Cart Abandoners]*.

   1. Haga clic **[!UICONTROL Post]**.

## Eliminación de una audiencia de remarketing dinámico

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Opcional) Filtre la lista para incluir audiencias específicas.

1. Seleccione la casilla de verificación situada junto a cada audiencia que desee eliminar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Crear [!DNL Google Ads] audiencias de coincidencia de cliente de [!DNL Adobe] audiencias](google-audience-from-adobe-audience.md)
>* [Crear un [!DNL Google Ads] audiencia de customer match de una lista de correo electrónico de Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes](audience-from-customer-data-list.md)

