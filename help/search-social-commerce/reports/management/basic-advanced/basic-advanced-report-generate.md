---
title: Generar un informe básico o avanzado
description: Obtenga información sobre cómo generar un informe básico o avanzado personalizado.
exl-id: cad5183c-cd21-439a-ab3e-033b2bb187ec
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Generar un informe básico o avanzado

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Create Report]**, mantenga el cursor sobre **[!UICONTROL Basic Reports]** o **[!UICONTROL Advanced Reports]** y, a continuación, haga clic en [tipo de informe](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Opcional) En el [!UICONTROL Report Settings] ventana, cambie el valor predeterminado [configuración de informes](basic-advanced-report-settings.md):

   1. (Opcional) Introduzca un nombre personalizado para el informe y para la plantilla (si guarda el informe como plantilla).

   1. (Opcional) Para guardar la configuración del informe como una plantilla, active la casilla de verificación situada junto a **[!UICONTROL Save as template]**.

   1. (Opcional) En el **[!UICONTROL Basic Settings]** , seleccione una plantilla de informe existente para usar o cambiar la configuración básica predeterminada del informe.

   1. (Opcional) Haga clic en **[!UICONTROL Columns tab]** y cambie las columnas predeterminadas en el informe.

      De forma predeterminada, todos los datos monetarios de los informes se muestran en formato de dólares estadounidenses (por ejemplo, 1000,00). Para mostrar el valor en el formato de moneda correcto (pero sin símbolos de moneda en los formatos CSV y TSV), agregue el símbolo &quot;[!UICONTROL Currency]&quot; al informe. Si el informe incluye datos de cuentas con distintas monedas, cualquier &quot;[!UICONTROL Total]&quot; los valores monetarios son la suma de todos los números de la columna, independientemente de la moneda.

   1. (Opcional; [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], y [!UICONTROL Label Classification Report] (solo) Haga clic en **[!UICONTROL Classifications]** y limite los resultados del informe para incluir solo clasificaciones de etiquetas específicas.

   1. (Opcional) Haga clic en **[!UICONTROL Advanced Filters]** y cambie las opciones avanzadas predeterminadas.

   1. (Opcional) Haga clic en **[!UICONTROL Attribution]** y cambie la regla de atribución predeterminada.

   1. (Opcional) Haga clic en **[!UICONTROL Scheduling and Delivery]** y cambie las opciones predeterminadas de programación y envío.

1. (Opcional cuando esté disponible) Para previsualizar las primeras 50 líneas del informe, haga clic en **[!UICONTROL Preview]**. Cuando haya terminado, haga clic en **[!UICONTROL Back]** para volver a la página configuración del informe.

   >[!NOTE]
   >
   >El botón Vista previa está disponible para todos los informes básicos y avanzados, excepto para el [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report], y [!UICONTROL Transaction Report].

1. Haga clic **[!UICONTROL Create]**.

Si no ha especificado una programación de informes, el informe se ejecuta inmediatamente; de lo contrario, se ejecuta según la programación especificada. El nombre del informe se agrega al [[!UICONTROL Latest Reports] vista](/help/search-social-commerce/reports/report-about.md). Si guardó el informe como plantilla, también se agregará al [[!UICONTROL Templates] vista](/help/search-social-commerce/reports/report-about.md). Cuando se completa el informe, el archivo está disponible para abrirlo o guardarlo; las plantillas están disponibles inmediatamente.

Si ha introducido direcciones de correo electrónico para la notificación, cada destinatario recibe una notificación cuando se completa o falla el trabajo del informe, según el [configuración de notificaciones](/help/search-social-commerce/notifications/notification-edit.md) para informes.

>[!MORELIKETHIS]
>
>* [Acerca de los informes básicos y avanzados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Configuración de informes básica y avanzada](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Columnas de informes para informes básicos y avanzados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Eliminar informes](/help/search-social-commerce/reports/management/report-delete.md)
