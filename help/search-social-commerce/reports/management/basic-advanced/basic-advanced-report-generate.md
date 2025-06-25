---
title: Generar un informe básico o avanzado
description: Obtenga información sobre cómo generar un informe básico o avanzado personalizado.
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Generar un informe básico o avanzado

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Create Report]**, mantenga el cursor sobre **[!UICONTROL Basic Reports]** o **[!UICONTROL Advanced Reports]** y, a continuación, haga clic en [tipo de informe](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Opcional) En la ventana [!UICONTROL Report Settings], cambie la [configuración del informe](basic-advanced-report-settings.md) predeterminada:

   1. (Opcional) Introduzca un nombre personalizado para el informe y para la plantilla (si guarda el informe como plantilla).

   1. (Opcional) Para guardar la configuración del informe como una plantilla, active la casilla de verificación situada junto a **[!UICONTROL Save as template]**.

   1. (Opcional) En la ficha **[!UICONTROL Basic Settings]**, seleccione una plantilla de informe existente para usar o cambiar la configuración básica predeterminada del informe.

   1. (Opcional) Haga clic en **[!UICONTROL Columns tab]** y cambie las columnas predeterminadas del informe.

      De forma predeterminada, todos los datos monetarios de los informes se muestran en formato de dólares estadounidenses (por ejemplo, 1000,00). Para mostrar el valor en el formato de moneda correcto (pero sin símbolos de moneda en los formatos CSV y TSV), agregue la columna &quot;[!UICONTROL Currency]&quot; al informe. Si el informe incluye datos de cuentas con distintas monedas, cualquier valor monetario &quot;[!UICONTROL Total]&quot; será la suma de todos los números de la columna, independientemente de la moneda.

   1. (Opcional; solo [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] y [!UICONTROL Label Classification Report]) Haga clic en la ficha **[!UICONTROL Classifications]** y limite los resultados del informe para incluir solo clasificaciones de etiquetas específicas.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Advanced Filters]** y cambie las opciones avanzadas predeterminadas.

   1. (Opcional) Haga clic en la pestaña **[!UICONTROL Attribution]** y cambie la regla de atribución predeterminada.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Scheduling and Delivery]** y cambie las opciones predeterminadas de programación y envío.

1. (Opcional cuando esté disponible) Para previsualizar las primeras 50 líneas del informe, haga clic en **[!UICONTROL Preview]**. Cuando haya terminado, haga clic en **[!UICONTROL Back]** para regresar a la página de configuración del informe.

   >[!NOTE]
   >
   >El botón Vista previa está disponible para todos los informes básicos y avanzados excepto para [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report] y [!UICONTROL Transaction Report].

1. Haga clic en **[!UICONTROL Create]**.

Si no ha especificado una programación de informes, el informe se ejecuta inmediatamente; de lo contrario, se ejecuta según la programación especificada. El nombre del informe se agrega a la vista [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Si guardó el informe como plantilla, entonces también se agregará a la vista [[!UICONTROL Templates]](/help/search-social-commerce/reports/report-about.md). Cuando se completa el informe, el archivo está disponible para abrirlo o guardarlo; las plantillas están disponibles inmediatamente.

Si ha introducido direcciones de correo electrónico para la notificación, cada destinatario recibe una notificación cuando se completa o falla el trabajo del informe, según la [configuración de notificaciones](/help/search-social-commerce/notifications/notification-edit.md) del usuario para los informes.

>[!MORELIKETHIS]
>
>* [Acerca de los informes básicos y avanzados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Configuración básica y avanzada del informe](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Columnas de informes para informes básicos y avanzados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Eliminar informes](/help/search-social-commerce/reports/management/report-delete.md)
