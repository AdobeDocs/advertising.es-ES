---
title: Administrar [!DNL Microsoft Advertising] audiencias de remarketing dinámico
description: Aprenda a crear y administrar  [!DNL Microsoft Advertising] audiencias de remarketing dinámico.
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Administrar [!DNL Microsoft Advertising] audiencias de remarketing dinámico

*[!DNL Microsoft Advertising]solo cuentas*

Puede crear una audiencia de remarketing dinámico de [!DNL Microsoft Advertising] cuando utilice la etiqueta de seguimiento de conversión y audiencia de JavaScript del motor de búsqueda en sus páginas web. Cada audiencia se crea con una etiqueta especificada que se incluye en las páginas web cuyos usuarios forman la audiencia. Puede crear varias audiencias con la misma etiqueta de seguimiento. También puede cambiar el nombre y la fuente de datos de las audiencias existentes, o eliminar las audiencias existentes.

Las audiencias de remarketing dinámico tienen el tipo de audiencia &quot;[!UICONTROL Dynamic Remarketing] \&lt;Tipo de visitante\>&quot; (como &quot;Remarketing dinámico de compradores anteriores&quot;).

Para obtener más información sobre el remarketing dinámico y cómo implementar la etiqueta de JavaScript necesaria, consulte la [[!DNL Microsoft Advertising] documentación sobre el remarketing dinámico](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Creación de una audiencia de remarketing dinámica

>[!NOTE]
>
>Para las cuentas de [!DNL Microsoft Advertising], la etiqueta de JavaScript debe incluir [ID de producto y parámetros de tipo de página](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifique el nombre de la etiqueta de seguimiento universal de eventos (UET) [!DNL Microsoft Advertising] que se incluye en las páginas web a partir de las cuales se creará la audiencia.

   Necesitará el nombre de la etiqueta en un paso posterior.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Especifique la información de la audiencia:

   1. En el menú **[!UICONTROL Data Source]**, seleccione **[!UICONTROL Dynamic Remarketing List]**.

   1. Escriba **[!UICONTROL Audience Name]**.

   1. De una lista de todas las etiquetas disponibles para la cuenta de motor de búsqueda, seleccione el nombre de la etiqueta UET [!DNL Microsoft Advertising] que se incluye en las páginas web cuyos usuarios forman la audiencia.

   1. Seleccione el tipo de visitante para la audiencia, que se basa en las acciones del visitante en las páginas web relevantes: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* o *[!UICONTROL Shopping Cart Abandoners]*.

   1. Especifique el número de **[!UICONTROL Membership Days]**, que es el número de días que la cookie de un usuario permanece en la audiencia. Los valores pueden variar de uno (1) a 180.

      Utilice el periodo de tiempo durante el cual espera que el anuncio sea relevante para el usuario.

1. Haga clic en **[!UICONTROL Post]**.

>[!NOTE]
>
>Sus listas de remarketing dinámico de [!DNL Microsoft Advertising] pueden utilizarse para el direccionamiento una vez que incluyan al menos 300 usuarios.

## Edición de una audiencia de remarketing dinámico

Puede cambiar el nombre y la fuente de datos de una audiencia de remarketing dinámico de [!DNL Microsoft Advertising]. No puede editar el valor de la configuración [!UICONTROL Membership Days].

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Seleccione la casilla de verificación situada junto a la audiencia que desea editar.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite la información de la audiencia:

   1. En la sección **[!UICONTROL Data Source]**, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

   1. (Opcional) Cambie **[!UICONTROL Audience Name]**.

   1. (Opcional) De una lista de todas las etiquetas disponibles para la cuenta de red de publicidad, cambie el nombre de la etiqueta UET [!DNL Microsoft Advertising] que se incluye en las páginas web cuyos usuarios forman la audiencia.

   1. (Opcional) Cambie el tipo de visitante para la audiencia, que se basa en las acciones del visitante en las páginas web relevantes: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* o *[!UICONTROL Shopping Cart Abandoners]*.

   1. Haga clic en **[!UICONTROL Post]**.

## Eliminación de una audiencia de remarketing dinámico

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Opcional) Filtre la lista para incluir audiencias específicas.

1. Seleccione la casilla de verificación situada junto a cada audiencia que desee eliminar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias](google-audience-from-adobe-audience.md)
>* [Crear una audiencia de  [!DNL Google Ads] customer match a partir de una lista de correo electrónico de Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes](audience-from-customer-data-list.md)
