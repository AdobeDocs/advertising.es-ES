---
title: Generar un [!DNL Advertising Insight]
description: Obtenga información sobre cómo crear un(a) [!DNL Advertising Insight].
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Generar un [!DNL Advertising Insight]

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Haga clic en la insight que desee generar.

3. Especifique la configuración de insight:

   1. (Algunos informes; opcional) Especifique los intervalos de fechas para insight.

   2. (Más información) Seleccione el portafolio que desea analizar.

      En general, están disponibles todos los portafolios optimizados y activos que contienen campañas activas. Para obtener algunas perspectivas, puede filtrar la lista de portafolios para incluir **[!UICONTROL Only Optimized Portfolios]**.

      Para las perspectivas de [!UICONTROL Day of Week], solo están disponibles los portafolios que tengan gasto suficiente y que también se hayan destinado a objetivos en los últimos dos días.

   3. ([!UICONTROL Event Path Beta] solo insight) Haga lo siguiente:

      1. Seleccione **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (para cargar un [!UICONTROL Channel Assist Report] o [!UICONTROL Campaign Assist Report] y clasificar los eventos de usuario en grupos distintos para su análisis) o *[!UICONTROL Analyze classified events]* (para cargar grupos de eventos y utilizarlos para generar insight).

      1. Haga clic en **[!UICONTROL Select]** para buscar un archivo en formato XLSX y ZIP (XLSX comprimido) y, a continuación, haga clic en **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] solo insight) Haga lo siguiente:

      1. Escriba **[!UICONTROL Advertiser Name]** y **[!UICONTROL Account Name]**.

      1. Seleccione **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* o *[!UICONTROL United Kingdom]*) y **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* o *[!UICONTROL German]*).

      1. Haga clic en **[!UICONTROL Select]** para localizar los informes de campaña, palabra clave e historial de cambios descargados para la cuenta desde la interfaz de usuario web [!DNL Google Ads] y un archivo de hoja de edición masiva descargado para la cuenta desde la aplicación [!DNL Google Ads Editor]. Luego haga clic en **[!UICONTROL Upload]**.

         Todos los archivos deben tener el formato CSV, TSV, TXT o ZIP (CSV comprimido, TSV o TXT).

   5. ([!UICONTROL Location Target Performance] solo insight; opcional) Para agregar los datos diariamente en lugar de como un resumen, seleccione **[!UICONTROL Time Aggregation]** de *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] solo insight) Haga lo siguiente:

      1. En el campo **[!UICONTROL Step]**, especifique el número de niveles de gasto de destino, o pasos, que se incluirán en la insight. El valor puede estar entre tres (3) y 100.

      1. En el campo **[!UICONTROL Type]**, seleccione el tipo de simulación:

         * *[!UICONTROL Optimized Multi-portfolio]*: genera una sola simulación en varios portafolios con el mismo objetivo y moneda.

         * *[!UICONTROL Individual Normalized]*: genera una simulación individual para cada portafolio seleccionado. Las carteras pueden tener diferentes objetivos y monedas.

   7. ([!UICONTROL Portfolio Launch] solo insight; opcional) Para especificar una fecha de inicio futura, especifique una fecha en el campo **[!UICONTROL Optional Date]**.

   8. ([!UICONTROL Quality Score] solo insight) Seleccione la red de anuncios aplicable.

   9. ([!UICONTROL Query Cross Matching] solo insight) En el menú **[!UICONTROL Google Accounts]**, seleccione la cuenta.

4. Haga clic en **[!UICONTROL Generate Insight]**.

   Recibirá una notificación cuando el trabajo se complete o falle según la [configuración de notificaciones](/help/search-social-commerce/notifications/notification-edit.md) para [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Acerca de [!UICONTROL Advertising Insights]](insight-about.md)
>* [Ver o guardar un [!DNL Advertising Insight]](insight-view-save.md)
>* [Eliminar un [!DNL Advertising Insight]](insight-delete.md)
