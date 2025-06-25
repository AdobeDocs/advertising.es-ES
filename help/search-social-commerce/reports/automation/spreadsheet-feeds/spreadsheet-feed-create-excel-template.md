---
title: Crear una  [!DNL Excel] plantilla para una fuente de informes de hoja de cálculo
description: Aprenda a crear plantillas de hoja de cálculo con formato especial.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Crear una plantilla [!DNL Excel] para una fuente de informes de hoja de cálculo

*Solo para informes básicos e informes de precisión de modelo*

Para crear fuentes de hoja de cálculo, primero debe crear [!DNL Microsoft Excel] plantillas de hoja de cálculo con formato especial utilizando plantillas de informe normales. Opcionalmente, puede personalizar la hoja de cálculo [!DNL Excel] para incluir columnas y gráficos adicionales.

1. En **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, genere el tipo de informe deseado con una unidad [!UICONTROL Date Aggregation] de &quot;[!UICONTROL Daily]&quot; y con todos los demás parámetros de datos que desee, guardando el informe como plantilla.

   >[!NOTE]
   >
   > * Puede crear fuentes de hoja de cálculo para los informes [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] y [!UICONTROL Forecast Accuracy]. Si usa el [!UICONTROL Ad Group Report], limite el número de grupos de publicidad incluidos para obtener resultados más rápidos.
   > * No se utiliza la unidad [!UICONTROL Date Range] definida en la plantilla. Cuando configure la fuente de la hoja de cálculo más adelante, definirá las fechas en las que desea actualizar los datos.

1. Una vez generado el informe, vaya a **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** y exporte una versión TSV o XLS del resultado del informe a un archivo.

1. En [!DNL Excel], cree una plantilla personalizada para el informe:

   1. Abra el archivo de informe en [!DNL Excel].

   1. Prepare el libro:

      1. Elimine las filas superiores que muestran los parámetros del informe. Para archivos XLS, elimine también la fila &quot;[!UICONTROL Total]&quot;. Si lo desea, puede eliminar algunas de las filas de datos, pero mantenga a) la fila del encabezado de datos con todas las columnas en el orden original y b) al menos una fila de datos. No agregue manualmente ningún dato.

         >[!NOTE]
         >
         > La última columna debe incluir valores distintos de cero.

      2. Ordene los datos por fecha de inicio en orden ascendente (de la más antigua a la más reciente).

      3. Cambie el nombre de la ficha de hoja de cálculo de &quot;[!UICONTROL Sheet1]&quot; a &quot;[!UICONTROL RAW]&quot;.&quot;

         Este nombre de ficha específico permite actualizar los datos.

      4. (Opcional) Agregue columnas personalizadas a la derecha de las columnas de la plantilla del informe, según sea necesario.

   1. (Opcional) En una hoja de cálculo independiente, cree una tabla dinámica. Una vez finalizado, haga clic con el botón derecho en cualquier celda de la tabla dinámica y seleccione **[!UICONTROL Pivot Table Options]**, haga clic en la ficha **[!UICONTROL Data]** y, a continuación, seleccione **[!UICONTROL Refresh data when opening the file]**.

   1. Guarde el archivo como una hoja de cálculo de [!DNL Excel] en formato .XLSX.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de informes de hoja de cálculo](spreadsheet-feed-about.md)
>* [Crear una fuente de informes de hoja de cálculo](spreadsheet-feed-create.md)
>* [Editar la configuración de fuentes de informes de hoja de cálculo](spreadsheet-feed-edit.md)
>* [Configuración de fuente de informes de hoja de cálculo](spreadsheet-feed-settings.md)
>* [Ver o guardar un archivo de fuente de informes de hoja de cálculo](spreadsheet-feed-view-or-save.md)
>* [Actualizar manualmente las fuentes de informes de hoja de cálculo](spreadsheet-feed-refresh.md)
>* [Eliminar fuentes de informes de hoja de cálculo](spreadsheet-feed-delete.md)
