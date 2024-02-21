---
title: Ver alertas
description: Obtenga información sobre cómo ver alertas y resoluciones recomendadas para sus campañas y componentes de campaña.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
source-git-commit: 70592355207ba43341eb208750dcd3fc00db51c1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Ver alertas

*Función beta*

DSP le ayuda a identificar cuándo tienen problemas cualquiera de sus campañas o componentes de campaña. DSP Para cada problema, crea una alerta con una marca de tiempo y la acción recomendada para resolverlo. Los motivos de las alertas incluyen problemas de configuración (por ejemplo, cuando no se adjuntan anuncios a una ubicación o cuando una oferta se configura incorrectamente), rechazo de anuncios y problemas de estado de la campaña (como envío o rendimiento deficientes de la publicidad). Las alertas están disponibles en los niveles de campaña, paquete, ubicación, anuncio y acuerdo.

Las alertas están disponibles en las siguientes ubicaciones:

* A [!UICONTROL Pulse Panel] en el menú [!UICONTROL Campaigns], [!UICONTROL Packages] y detalles del paquete, [!UICONTROL Placements], y [!UICONTROL Ads] vistas indica si hay alertas disponibles para los elementos de esa vista. Cuando el icono tiene un punto azul (![Icono del Panel de pulsos cuando las alertas están disponibles](/help/dsp/assets/alerts-panel.png "Icono del Panel de pulsos cuando las alertas están disponibles")), hay alertas disponibles. Cuando no hay puntos visibles (![Icono del Panel de pulsos cuando no hay alertas disponibles](/help/dsp/assets/alerts-panel-empty.png "Icono del Panel de pulsos cuando no hay alertas disponibles")), no hay alertas disponibles.

* Las tablas de datos de las mismas vistas incluyen un &quot;[!UICONTROL Alerts]&quot; que indica cuándo el elemento (o sus componentes) tiene un problema. Los indicadores de alerta incluyen &quot;Crítico&quot; (![Crítico](/help/dsp/assets/indicator-critical.png "Crítico")), &quot;Advertencia&quot; (![Advertencia](/help/dsp/assets/indicator-warning.png "Advertencia")) e &quot;Información&quot; (![Información](/help/dsp/assets/indicator-information.png "Información")).

Puede abrir la vista de administración de campañas correspondiente a cualquier alerta para poder editar la configuración según sea necesario y resolver el problema.

También puede optar por ignorar una alerta individual, lo que la elimina del [!UICONTROL Pulse] panel.

Las alertas y los indicadores de alerta desaparecen automáticamente cuando se resuelven los problemas subyacentes.

## Ver alertas en [!UICONTROL Pulse Panel]

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Realice una de las siguientes acciones:

   * (Para todas las alertas aplicables a la vista ) A la derecha de la barra de herramientas en cualquier vista de administración de campañas, haga clic en ![Icono del Panel de pulsos cuando las alertas están disponibles](/help/dsp/assets/alerts-panel.png "Icono del Panel de pulsos cuando las alertas están disponibles").

   * (Para todas las alertas de una campaña específica) Haga clic en el indicador de alerta de una fila de campaña y, a continuación, haga clic en **[!UICONTROL View in Pulse panel]**.

   * (Para todas las alertas de un paquete, ubicación o anuncio específicos) Haga lo siguiente:

      1. Haga clic en el nombre de la campaña.

      1. En el submenú, haga clic en **[!UICONTROL Packages]**, **[!UICONTROL Placements]**, o **[!UICONTROL Ads]** para abrir la vista del componente de campaña correspondiente.

      1. Haga clic en el indicador de alerta de un paquete, ubicación o fila de anuncio y, a continuación, haga clic en **[!UICONTROL View in Pulse Panel]**.

   Se muestran todas las alertas asociadas con la campaña y sus componentes, incluidas las ofertas segmentadas. De forma predeterminada, las alertas críticas se muestran primero.

1. (Opcional) Para agrupar las alertas según su primera fecha de detección o para filtrar las alertas por estado de alerta, estado de componente, tipo de componente o con un nombre de campaña específico, haga clic en ![Botón Filtro](/help/dsp/assets/filter.png) en la parte superior derecha del panel, seleccione las opciones de filtro y haga clic en **[!UICONTROL Apply]**.

1. Para ver una lista de todos los componentes de campaña afectados para un tipo de alerta específico, haga clic en el nombre de la alerta, como &quot;[!UICONTROL Package: No Active Placement (*N*)]&quot;. Para ver los detalles de cada componente afectado, incluida la acción recomendada, haga clic en [!UICONTROL EXPAND ALL] o haga clic en el nombre del componente. Para abrir la vista de administración de campañas correspondiente a cualquier componente afectado y realizar los cambios recomendados, mantenga el cursor sobre el nombre del componente y haga clic en ![Ir a la vista](/help/dsp/assets/go-to-view.png "Ir a la vista").

1. (Opcional) Para ignorar (ocultar) una alerta, mantenga el cursor sobre el nombre del componente y haga clic en ![Ignorar](/help/dsp/assets/alert-ignore.png "Ignorar")y haga clic en **[!UICONTROL Ignore indefinitely]**.  <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

Después de pasar por alto una alerta, tiene unos segundos para deshacer la acción. Una vez que se cierra el mensaje de opción, no se puede cancelar la acción.

1. (Opcional) Para recuperar las alertas omitidas, filtre las alertas para mostrar un [!UICONTROL Alert Status] de &quot;[!UICONTROL All]&quot; o &quot;[!UICONTROL Ignored].&quot; Para ignorar una alerta, mantenga el cursor sobre el nombre del componente y haga clic en ![Anular la omisión](/help/dsp/assets/alert-un-ignore.png "Anular la omisión").

## Cierre el [!UICONTROL Pulse Panel]

* A la derecha de la barra de herramientas, haga clic en ![Icono del Panel de pulsos cuando las alertas están disponibles](/help/dsp/assets/alerts-panel.png "Icono del Panel de pulsos cuando las alertas están disponibles") o ![Icono del Panel de pulsos cuando no hay alertas disponibles](/help/dsp/assets/alerts-panel-empty.png "Icono del Panel de pulsos cuando no hay alertas disponibles").

>[!MORELIKETHIS]
>
>* [Tipos de informes de rendimiento en las vistas de Campaign Management](campaign-reports-about.md)
