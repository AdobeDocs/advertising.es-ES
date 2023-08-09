---
title: Cambiar las métricas de conversión disponibles en las vistas de administración y en los informes
description: Obtenga información sobre cómo hacer que las métricas de conversión estén disponibles en sus vistas de administración e informes.
feature: Conversions
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
source-git-commit: af32aea1c50edb6b22b0b15c920cb8c2dcdc37e9
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Cambiar las métricas de conversión disponibles en las vistas de administración y en los informes

Cuando el Adobe Advertising rastrea un [conversión](/help/search-social-commerce/glossary.md#c-d) para un anunciante, inicialmente se excluye de los objetivos del portafolio, los informes y las vistas de administración. Para que una métrica de conversión sea visible, debe habilitarla explícitamente y, opcionalmente, cambiar el nombre para mostrar predeterminado, que es el nombre que se muestra. La única excepción es que las conversiones rastreadas por [!DNL Google Ads], [!DNL Google Analytics], y [!DNL Microsoft® Advertising] las etiquetas de seguimiento de eventos universales están disponibles y son visibles automáticamente.

Del mismo modo, puede ocultar una métrica de conversión de objetivos de portafolio, informes y vistas de administración. Si oculta una métrica de conversión que anteriormente era visible, se elimina de cualquier métrica derivada que contenga la métrica de conversión.

De la lista de métricas de conversión disponibles, cada usuario con acceso a los datos del anunciante puede personalizar las métricas que ve para las vistas de administración y los informes, incluidas u omitiendo las métricas específicas que elija.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Se muestran todas las métricas de conversión que se han recopilado para el anunciante y todos los nombres diferentes que se han especificado para mostrarlos.

1. (Opcional) Filtre la lista:

   * Para buscar un nombre de métrica o de visualización específico, haga clic en ![Buscar](/help/search-social-commerce/assets/search.png "Buscar"), introduzca la palabra o cadena en el campo de entrada y, a continuación, pulse la tecla **[!DNL Enter]** clave.

     Puede buscar cadenas que aparezcan en cualquier lugar dentro de la frase (como la primera letra o las últimas tres letras) y los términos de búsqueda no [distinguir entre mayúsculas y minúsculas](/help/search-social-commerce/glossary.md#c-d).

   * Para buscar métricas de conversión por su disponibilidad en vistas de administración e informes, haga clic en ![Filtrar](/help/search-social-commerce/assets/filter.png "Filtrar")y seleccione el filtro **[!UICONTROL Show in UI and Reports]**. A continuación, seleccione **[!UICONTROL Show]** (para ver las métricas de conversión disponibles para incluir en informes y vistas de administración) o **[!UICONTROL Hide]** (para ver las métricas de conversión que no están disponibles en las vistas informes y administración).

1. Cambie las métricas de conversión disponibles para las vistas de administración y los informes:

   * Para mostrar u ocultar una sola métrica, haga clic en el conmutador en la **[!UICONTROL Show in UI and Reports]** para cambiar la configuración.

   * Para mostrar u ocultar varias métricas, haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada métrica de conversión.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Mostrar](/help/search-social-commerce/assets/show.png "Mostrar") para mostrar las métricas o ![Hide](/help/search-social-commerce/assets/hide.png "Hide") para ocultar las métricas.

      1. (Para ocultar las métricas) En el mensaje de confirmación, haga clic en **[!UICONTROL Yes]** para ocultar las métricas, incluido el hecho de eliminarlas de cualquier métrica derivada que las contenga.

1. (Opcional) [Cambiar el nombre que aparece en los encabezados de columna](conversion-metric-edit-display-name.md) para cualquiera de las métricas de conversión.

   El nombre para mostrar predeterminado de cada métrica de conversión visible es el nombre de la métrica tal como se escribe en los datos recuperados.

>[!NOTE]
>
>Si Adobe Advertising recopila datos para las nuevas métricas de conversión, entonces las nuevas métricas, excepto para las conversiones rastreadas por [!DNL Google Ads], [!DNL Google Analytics], y [!DNL Microsoft® Advertising] etiquetas universales de seguimiento de eventos: se excluyen automáticamente de las vistas de administración y de los informes hasta que se incluyen. Nuevas conversiones rastreadas por [!DNL Google Ads], [!DNL Google Analytics], y [!DNL Microsoft® Advertising] las etiquetas de seguimiento de eventos universales siempre están disponibles automáticamente.

>[!MORELIKETHIS]
>
* [Acerca de la administración de las métricas de conversión de un anunciante](conversion-metric-about.md)
* [Ver las métricas de conversión rastreadas de un anunciante](conversion-metric-view-tracked.md)
* [Cambiar el nombre para mostrar de una métrica de conversión](conversion-metric-edit-display-name.md)
