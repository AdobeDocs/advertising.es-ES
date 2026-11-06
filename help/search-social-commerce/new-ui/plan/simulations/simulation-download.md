---
title: Descarga de simulaciones
description: Aprenda a descargar simulaciones como archivos de hoja de cálculo individuales o combinados.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 46c8c9de-b558-486e-9453-feb5d359aaec
autotag-review: '2026-04-14T00:04:41.270Z'
TQID: 'https://experienceleague.adobe.com/5FVQv17adrIz6OJU1K3ftG8NRO-0evlIzc1tGIFoHfY'
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
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: Admin
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%
---
# Descarga de simulaciones

<!-- No subfeature tag for simulations or portfolios -->

*característica de Beta*

Puede descargar hasta 10 simulaciones semanales o personalizadas a la vez desde la vista [!UICONTROL Simulations]. Una sola simulación se descarga como un libro de trabajo [!DNL Microsoft Excel] (archivo XLSX). Para varias simulaciones, se puede descargar un libro combinado o un archivo ZIP que contenga un libro independiente para cada simulación.

La descarga de simulaciones requiere acceso a la vista [!UICONTROL Simulations] con el permiso [!UICONTROL View Simulation].

>[!NOTE]
>
>* También puede [ver los resultados de la simulación en pantalla](simulation-view.md).
>* Puede [personalizar la vista [!UICONTROL Simulations]](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) para incluir columnas para muchas métricas adicionales y la mayoría de los ajustes de simulación. Consulte la sección &quot;Acciones disponibles&quot; en &quot;[Acerca de las simulaciones](simulation-about.md#simulations-actions)&quot; para obtener más información acerca de las columnas que puede incluir.
>* También puedes [descargar simulaciones semanales de hasta 100 portafolios desde la vista [!UICONTROL Portfolios]](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#download-simulations).

1. En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Seleccione las casillas de verificación situadas junto a un máximo de 10 simulaciones que desee descargar.

   Seleccione solo simulaciones con un estado de [!UICONTROL Successful]. Si alguna de las simulaciones seleccionadas tiene un estado de [!UICONTROL Failed], [!UICONTROL Queued] o [!UICONTROL In Progress], no se inicia ninguna descarga. Borre esas selecciones antes de descargar.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Download Simulation]**.

1. (Cuando se seleccionan varias simulaciones) Seleccione una opción de descarga:

   * **[!UICONTROL Download as Single File]**: descargar un libro que contenga todas las simulaciones seleccionadas.

   * **[!UICONTROL Download as Multiple Files]**: descargue un archivo ZIP que contenga un libro independiente para cada simulación seleccionada.

El archivo se descarga según el procedimiento normal del explorador. Si descarga un archivo ZIP, descomprímalo para ver los libros.

>[!MORELIKETHIS]
>
>* [Acerca de las simulaciones](simulation-about.md)
>* [Ejecutar o volver a ejecutar una simulación](simulation-create.md)
>* [Ver detalles de la simulación](simulation-view.md)
