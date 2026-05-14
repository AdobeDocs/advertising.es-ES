---
title: Ejecutar o volver a ejecutar una simulación personalizada
description: Obtenga información sobre cómo ejecutar o volver a ejecutar una simulación personalizada para un portafolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2504e6a4eebeab74352606a89a5012ab96c89c47
workflow-type: tm+mt
source-wordcount: 505
ht-degree: 0%

---

# Ejecutar o volver a ejecutar una simulación personalizada

*característica de Beta*

Puede generar una simulación personalizada para un portafolio [optimizado o activo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md). También puede cambiar los parámetros de una simulación existente y regenerarla, o volver a ejecutar una simulación existente con los parámetros existentes.

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

Los usuarios de [!UICONTROL Admin] y [!UICONTROL Account Manager] pueden ver simulaciones creadas por otros usuarios. El resto de usuarios solo pueden ver las simulaciones personalizadas que crean.

## Creación de una nueva simulación

1. Realice una de las acciones siguientes:

* Desde la vista [!UICONTROL Simulations]:

   1. En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Run Simulation]**.

   1. Seleccione el portafolio:

      1. Haga clic en **[!UICONTROL Select Portfolio]**.

      1. Seleccione el portafolio.

         Para buscar portafolios que incluyan una cadena de texto específica, empiece a introducir la cadena de texto dentro del campo de búsqueda. Los valores no distinguen entre mayúsculas y minúsculas.

      1. Haga clic en **[!UICONTROL Proceed]**.

* Desde la vista [!UICONTROL Portfolios]:

   1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

   1. Mantenga el cursor sobre la fila del portafolio. Junto al nombre del portafolio, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**.

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

Cuando el informe de simulación esté disponible, usted y los demás destinatarios de correo electrónico especificados recibirán una notificación con un vínculo para descargar los datos en un archivo ZIP que contenga un libro (archivo XLSX).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Edite los ajustes de una simulación existente y vuelva a ejecutarla

1. En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Seleccione la casilla de verificación situada junto a la simulación que se va a regenerar.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Run Simulation]**.

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

Cuando el informe de simulación esté disponible, usted y los demás destinatarios de correo electrónico especificados recibirán una notificación con un vínculo para descargar los datos en un archivo ZIP que contenga un libro (archivo XLSX).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Volver a ejecutar una simulación con la configuración existente

Puede volver a ejecutar simulaciones que no estén en cola actualmente.

1. En el menú principal, haga clic en **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Seleccione las casillas de verificación situadas junto a las simulaciones que desee volver a ejecutar.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Volver a ejecutar](/help/search-social-commerce/assets/rerun.png "Volver a ejecutar").

## Ajustes de simulación personalizados {#custom-simulation-settings}

Para obtener más información sobre la configuración de simulación personalizada, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.

>[!MORELIKETHIS]
>
>* [Acerca de las simulaciones](simulation-about.md)
>* [Ver detalles de la simulación](simulation-view.md)
>* [Descargar simulaciones](simulation-download.md)
