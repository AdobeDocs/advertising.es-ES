---
title: Ejecutar o volver a ejecutar una simulación personalizada
description: Obtenga información sobre cómo ejecutar o volver a ejecutar una simulación personalizada para un portafolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
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
source-wordcount: '530'
ht-degree: 0%
---
# Ejecutar o volver a ejecutar una simulación personalizada

*característica de Beta*

Puede generar una simulación personalizada para un portafolio [optimizado o activo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status). También puede seleccionar una simulación en la lista para ejecutar una nueva simulación para el mismo portafolio o volver a ejecutar las simulaciones con sus ajustes existentes.

La creación de una simulación personalizada requiere el permiso [!UICONTROL Create Simulation]. Para seleccionar un portafolio se requiere el permiso [!UICONTROL View Portfolios].

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

Los usuarios de [!UICONTROL Admin] y [!UICONTROL Account Manager] pueden ver simulaciones creadas por otros usuarios. El resto de usuarios solo pueden ver las simulaciones personalizadas que crean.

## Creación de una nueva simulación {#simulation-create}

Puede comenzar desde la vista [!UICONTROL Simulations] o [ejecutar una simulación personalizada desde la vista [!UICONTROL Portfolios]](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation).

1. En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Borre las filas de simulación seleccionadas y, a continuación, haga clic en **[!UICONTROL Run Simulation]**.

1. Seleccione el portafolio:

   1. Haga clic en **[!UICONTROL Select Portfolio]**.

   1. Seleccione el portafolio.

      Para buscar portafolios que incluyan una cadena de texto específica, empiece a introducir la cadena de texto dentro del campo de búsqueda. Los valores no distinguen entre mayúsculas y minúsculas.

   1. Haga clic en **[!UICONTROL Proceed]**.

1. Especifique la [configuración de simulación personalizada](#custom-simulation-settings):

   1. (Opcional) Para cambiar el portafolio utilizado para la simulación, haga clic en **[!UICONTROL Change Portfolio]** junto al nombre del portafolio, seleccione el portafolio y, a continuación, haga clic en **[!UICONTROL Proceed]**.

   1. En la ficha [!UICONTROL Basic Settings]:

      1. Escriba un(a) **[!UICONTROL Simulation Name]** único.

      1. (Opcional) Cambie los parámetros básicos de la simulación.

   1. (Opcional) En la pestaña [!UICONTROL Advanced Settings], cambie los parámetros avanzados de la simulación.

   Los parámetros existentes para el portafolio seleccionado se especifican de forma predeterminada. Al cambiar los valores, se muestran los resultados que producirían distintos parámetros sin cambiar los parámetros existentes del portafolio.

1. Haga clic en **[!UICONTROL Next]**.

1. Revise la configuración y edítela según sea necesario.

1. Haga clic en **[!UICONTROL Submit & Run]**.

La solicitud se envía y se abre la vista [!UICONTROL Simulations]. Cuando el informe de simulación esté disponible, usted y los demás destinatarios de correo electrónico especificados recibirán una notificación con un vínculo de descarga. También puede [descargar la simulación desde la vista [!UICONTROL Simulations]](simulation-download.md).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Volver a ejecutar una simulación con la configuración existente {#rerun-a-simulation-with-the-existing-settings}

Puede volver a ejecutar hasta 10 simulaciones a la vez con su configuración existente. Las simulaciones con un estado de [!UICONTROL Queued] o [!UICONTROL In Progress] no se pueden volver a ejecutar. Si la selección incluye estas simulaciones, se omiten y se envían las simulaciones restantes.

1. En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Seleccione las casillas de verificación situadas junto a las simulaciones que desee volver a ejecutar.

1. En la barra de herramientas situada encima de la tabla de datos o en la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Re-Run Simulation]**.

La solicitud se envía y la vista se actualiza.

## Ejecute una nueva simulación para un portafolio de la lista {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

Al seleccionar una simulación antes de hacer clic en [!UICONTROL Run Simulation], se selecciona su portafolio para una nueva simulación. El formulario utiliza la configuración actual del portafolio, no la configuración de la simulación seleccionada. Esta acción no edita la simulación existente.

1. En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Seleccione la casilla de verificación situada junto a una simulación para el portafolio que desee utilizar.

   Si selecciona varias simulaciones, todas deben utilizar el mismo portafolio. La cartera debe estar activa o optimizada.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Run Simulation]**.

1. Especifique la [configuración de simulación personalizada](#custom-simulation-settings), incluida una **[!UICONTROL Simulation Name]** única. Cambie los parámetros en las fichas **[!UICONTROL Basic Settings]** y **[!UICONTROL Advanced Settings]** según sea necesario.

1. Haga clic en **[!UICONTROL Next]**.

1. Revise la configuración y edítela según sea necesario.

1. Haga clic en **[!UICONTROL Submit & Run]**.

La solicitud se envía y se abre la vista [!UICONTROL Simulations]. Puede [descargar la simulación](simulation-download.md) una vez que se haya completado correctamente.

## Ajustes de simulación personalizados {#custom-simulation-settings}

Para obtener más información sobre la configuración de simulación personalizada, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.

>[!MORELIKETHIS]
>
>* [Acerca de las simulaciones](simulation-about.md)
>* [Ver detalles de la simulación](simulation-view.md)
>* [Descargar simulaciones](simulation-download.md)
