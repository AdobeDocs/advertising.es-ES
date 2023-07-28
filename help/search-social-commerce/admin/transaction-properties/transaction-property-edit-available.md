---
title: Cambiar las propiedades de transacción disponibles en vistas de administración e informes
description: Obtenga información sobre cómo hacer que las propiedades de transacción estén disponibles en las vistas de administración y en los informes.
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
feature: Search Admin, Search Transaction Properties
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Cambiar las propiedades de transacción disponibles en vistas de administración e informes

Cuando el Adobe Advertising rastrea un [propiedad de transacción](/help/search-social-commerce/glossary.md#s-t) para un anunciante, inicialmente se excluye de los objetivos del portafolio, los informes y las vistas de administración. Para que una propiedad esté visible, debe habilitarla explícitamente y, opcionalmente, cambiar el nombre para mostrar predeterminado, que es el nombre que se muestra. La única excepción es que las conversiones rastreadas por [!DNL Google Ads], [!DNL Google Analytics], y [!DNL Microsoft® Advertising] las etiquetas de seguimiento de eventos universales están disponibles y son visibles automáticamente.

Del mismo modo, puede ocultar una propiedad de los objetivos del portafolio, los informes y las vistas de administración. Si oculta una propiedad que anteriormente estaba visible, se elimina de cualquier métrica derivada que contenga la propiedad.

De la lista de propiedades disponibles, cada usuario con acceso a los datos del anunciante puede personalizar las propiedades que ve para las vistas de administración y los informes, incluidas u omitiendo las propiedades específicas que elija.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   Se muestran todas las propiedades de transacción que se han recopilado para el anunciante y cualquier nombre diferente que se haya especificado para mostrar.

1. (Opcional) Filtre la lista:

   * Para buscar un nombre de propiedad específico o un nombre para mostrar, haga clic en ![Buscar](/help/search-social-commerce/assets/search.png "Buscar"), introduzca la palabra o cadena en el campo de entrada y, a continuación, pulse la tecla **[!DNL Enter]** clave.

     Puede buscar cadenas que aparezcan en cualquier lugar dentro de la frase (como la primera letra o las últimas tres letras) y los términos de búsqueda no [distinguir entre mayúsculas y minúsculas](/help/search-social-commerce/glossary.md#c-d).

   * Para buscar propiedades por su disponibilidad en vistas de administración e informes, haga clic en ![Filtrar](/help/search-social-commerce/assets/filter.png "Filtrar")y seleccione el filtro **[!UICONTROL Show in UI and Reports]**. A continuación, seleccione **[!UICONTROL Show]** (para ver las propiedades disponibles para incluir en informes y vistas de administración) o **[!UICONTROL Hide]** (para ver las propiedades que no están disponibles en las vistas Informes y Administración).

1. Cambie las propiedades disponibles para las vistas de administración y los informes:

   * Para mostrar u ocultar una sola propiedad, haga clic en el modificador en **[!UICONTROL Show in UI and Reports]** para cambiar la configuración.

   * Para mostrar u ocultar varias propiedades, haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada propiedad.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Mostrar](/help/search-social-commerce/assets/show.png "Mostrar") para mostrar las propiedades o ![Hide](/help/search-social-commerce/assets/hide.png "Hide") para ocultar las propiedades.

      1. (Para ocultar propiedades) En el mensaje de confirmación, haga clic en **[!UICONTROL Yes]** para ocultar las propiedades, incluso eliminándolas de cualquier métrica derivada que contenga las propiedades.

1. (Opcional) [Cambiar el nombre que aparece en los encabezados de columna](transaction-property-edit-display-name.md) para cualquiera de las propiedades.

   El nombre para mostrar predeterminado de cada propiedad visible es el nombre de la propiedad tal como se escribe en los datos recuperados.

>[!NOTE]
>
>Si el Adobe Advertising recopila datos para nuevas propiedades, entonces las nuevas propiedades, excepto para las conversiones rastreadas por [!DNL Google Ads], [!DNL Google Analytics], y [!DNL Microsoft® Advertising] etiquetas universales de seguimiento de eventos: se excluyen automáticamente de las vistas de administración y de los informes hasta que se incluyen. Nuevas conversiones rastreadas por [!DNL Google Ads], [!DNL Google Analytics], y [!DNL Microsoft® Advertising] las etiquetas de seguimiento de eventos universales siempre están disponibles automáticamente.

>[!MORELIKETHIS]
>
* [Administración de las propiedades de transacción de un anunciante](transaction-property-about.md)
* [Ver las propiedades de transacción rastreadas de un anunciante](transaction-property-view-tracked.md)
* [Cambiar el nombre para mostrar de una propiedad de transacción](transaction-property-edit-display-name.md)
