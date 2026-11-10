---
title: Ejecutar y descargar simulaciones desde la vista [!UICONTROL Portfolios]
description: Obtenga información sobre cómo ejecutar una simulación personalizada y descargar simulaciones semanales desde la vista Portafolios.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
source-git-commit: 3e70998ad9547cecc0f3581d6cfd917051d549db
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%
---
# Ejecutar y descargar simulaciones desde la vista [!UICONTROL Portfolios]

*característica de Beta*

Puede ejecutar una simulación personalizada para un único portafolio [optimizado o activo](portfolio-about.md#portfolio-status) y descargar simulaciones semanales automatizadas para hasta 100 portafolios desde la vista [!UICONTROL Portfolios].

La ejecución de una simulación personalizada requiere el permiso [!UICONTROL Create Simulation]. La descarga de simulaciones semanales requiere el permiso [!UICONTROL View Simulation].

>[!NOTE]
>
>También puede [crear o volver a ejecutar una simulación personalizada desde la vista [!UICONTROL Simulations]](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md).

## Ejecutar una simulación personalizada {#run-simulation}

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Realice una de las acciones siguientes:

   * Mantenga el cursor sobre la fila del portafolio. Junto al nombre del portafolio, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**.

   * Seleccione la casilla de verificación situada junto al portafolio. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL More]>[!UICONTROL Run Simulation]**.

1. Especifique la [configuración de simulación personalizada](#custom-simulation-settings):

   1. En la ficha **[!UICONTROL Basic Settings]**, escriba un(a) **[!UICONTROL Simulation Name]** único(a) y cambie los parámetros básicos según sea necesario.

   1. (Opcional) En la ficha **[!UICONTROL Advanced Settings]**, cambie los parámetros avanzados.

   La configuración actual del portafolio seleccionado se utiliza como predeterminada. Cambiar los ajustes de simulación no cambia los ajustes del portafolio.

1. Haga clic en **[!UICONTROL Next]**.

1. Revise la configuración y realice los cambios necesarios.

1. Haga clic en **[!UICONTROL Submit & Run]**.

La solicitud se envía y se abre la vista [!UICONTROL Simulations]. Puede [descargar la simulación](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md) una vez que se haya completado correctamente.

## Descargar simulaciones semanales {#download-simulations}

Puede descargar simulaciones semanales para una fecha de ejecución a la vez como un libro de [!DNL Microsoft Excel] (archivo XLSX). Solo se incluyen los portafolios activos y optimizados con informes de simulación disponibles para esa fecha.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Seleccione la casilla de verificación situada junto a cada portafolio cuya simulación semanal desee descargar. Seleccione hasta 100 portafolios.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL More]>[!UICONTROL Download Simulation]**.

1. En **[!UICONTROL Weekly Simulation]**, seleccione una fecha de ejecución.

   La fecha disponible más reciente está seleccionada de forma predeterminada. Si los informes no están disponibles para algunos portafolios seleccionados, el cuadro de diálogo muestra cuántos portafolios se excluirán. Seleccione otra fecha si es necesario. No se puede descargar un informe cuando ningún portafolio seleccionado tenga una simulación disponible para esa fecha.

1. Haga clic en el botón de descarga, cuya etiqueta incluye el número de portafolios con informes disponibles (por ejemplo, **[!UICONTROL Download 2 portfolios]**).

   El archivo se descarga según el procedimiento normal del explorador. El mensaje de finalización indica cuántos portafolios se incluyeron.

Para descargar simulaciones personalizadas o seleccionar simulaciones semanales individuales, use la vista [[!UICONTROL Simulations] &#x200B;](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md).

## Ajustes de simulación personalizados {#custom-simulation-settings}

Para obtener más información sobre la configuración de simulación personalizada, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.

>[!MORELIKETHIS]
>
>* [(Nueva IU) Ver detalles de rendimiento del portafolio](portfolio-details.md)
>* [Acerca de los portafolios](portfolio-about.md)
>* [Ejecutar o volver a ejecutar una simulación personalizada](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)
>* [Descargar simulaciones](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)
