---
title: Generación de un [!DNL Advertising Insight]
description: Obtenga información sobre cómo crear un [!DNL Advertising Insight].
exl-id: 242095c9-25f0-4954-b1a8-5ea3db312afd
feature: Search Advertising Insights
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Generación de un [!DNL Advertising Insight]

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Haga clic en la perspectiva que desee generar.

3. Especifique la configuración de perspectivas:

   1. (Algunos informes; opcional) Especifique los intervalos de fechas para la perspectiva.

   2. (Más información) Seleccione el portafolio que desea analizar.

      En general, están disponibles todos los portafolios optimizados y activos que contienen campañas activas. Para obtener algunas perspectivas, puede filtrar la lista de portafolios para incluir **[!UICONTROL Only Optimized Portfolios]**.

      Para [!UICONTROL Day of Week] perspectivas, solo están disponibles los portafolios que tienen gasto suficiente y que también se han gastado en segmentar en los últimos dos días.

   3. ([!UICONTROL Event Path Beta] solo Insight) Haga lo siguiente:

      1. Seleccione el **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (para cargar una [!UICONTROL Channel Assist Report] o [!UICONTROL Campaign Assist Report] y clasificar los eventos de usuario en distintos grupos para su análisis) o *[!UICONTROL Analyze classified events]* (para cargar grupos de eventos y utilizarlos para generar la perspectiva).

      1. Clic **[!UICONTROL Select]** para localizar un archivo en formato XLSX y ZIP (XLSX comprimido), y haga clic en **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] solo Insight) Haga lo siguiente:

      1. Introduzca el **[!UICONTROL Advertiser Name]** y **[!UICONTROL Account Name]**.

      1. Seleccione el **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* o *[!UICONTROL United Kingdom]*) y el **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]*, o *[!UICONTROL German]*).

      1. Clic **[!UICONTROL Select]** para localizar los informes de campaña, palabra clave e historial de cambios descargados para la cuenta desde [!DNL Google Ads] interfaz de usuario web y un archivo de hoja de edición masiva descargado para la cuenta desde el [!DNL Google Ads Editor] aplicación. Luego haga clic en **[!UICONTROL Upload]**.

         Todos los archivos deben tener el formato CSV, TSV, TXT o ZIP (CSV comprimido, TSV o TXT).

   5. ([!UICONTROL Location Target Performance] solo perspectiva; opcional) Para agregar los datos diariamente en lugar de como resumen, seleccione la variable **[!UICONTROL Time Aggregation]** de *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] solo Insight) Haga lo siguiente:

      1. En el **[!UICONTROL Step]** , especifique el número de niveles de gasto de destino, o pasos, que se incluirán en la perspectiva. El valor puede estar entre tres (3) y 100.

      1. En el **[!UICONTROL Type]** , seleccione el tipo de simulación:

         * *[!UICONTROL Optimized Multi-portfolio]*: genera una sola simulación en varios portafolios con el mismo objetivo y moneda.

         * *[!UICONTROL Individual Normalized]*: genera una simulación individual para cada portafolio seleccionado. Las carteras pueden tener diferentes objetivos y monedas.

   7. ([!UICONTROL Portfolio Launch] solo perspectiva; opcional) Para especificar una fecha de lanzamiento futura, especifique una fecha en la variable **[!UICONTROL Optional Date]** field.

   8. ([!UICONTROL Quality Score] solo Insight) Seleccione la red de publicidad aplicable.

   9. ([!UICONTROL Query Cross Matching] solo perspectiva) En el **[!UICONTROL Google Accounts]** , seleccione la cuenta.

4. Haga clic **[!UICONTROL Generate Insight]**.

   Recibirá una notificación cuando el trabajo se complete o falle según sus [configuración de notificaciones](/help/search-social-commerce/notifications/notification-edit.md) para [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Acerca de [!UICONTROL Advertising Insights]](insight-about.md)
>* [Ver o guardar un [!DNL Advertising Insight]](insight-view-save.md)
>* [Eliminar un [!DNL Advertising Insight]](insight-delete.md)
