---
title: Crear un [!DNL Excel] plantilla para una fuente de informes de hoja de cálculo
description: Aprenda a crear plantillas de hoja de cálculo con formato especial.
exl-id: d675cb8c-b7a9-4d7b-8435-5dd662d151a3
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Crear un [!DNL Excel] plantilla para una fuente de informes de hoja de cálculo

*Solo para informes básicos e informes de precisión de modelo*

Para crear fuentes de hoja de cálculo, primero debe crear fuentes con formato especial [!DNL Microsoft® Excel] plantillas de hoja de cálculo que utilizan plantillas de informe normales. Si lo desea, puede personalizar [!DNL Excel] para incluir columnas y gráficos adicionales.

1. Entrada **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, genere el tipo de informe deseado con una [!UICONTROL Date Aggregation] unidad de &quot;[!UICONTROL Daily]&quot; y con todos los demás parámetros de datos que desee, guardando el informe como plantilla.

   >[!NOTE]
   >
   > * Puede crear fuentes de hoja de cálculo para [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword], y [!UICONTROL Forecast Accuracy] informes. Si usa el [!UICONTROL Ad Group Report], limite el número de grupos de publicidad incluidos para obtener resultados más rápidos.
   > * El [!UICONTROL Date Range] La unidad definida en la plantilla no se utiliza. Cuando configure la fuente de la hoja de cálculo más adelante, definirá las fechas en las que desea actualizar los datos.

1. Una vez generado el informe, vaya a **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** y exporte una versión TSV o XLS de la salida del informe a un archivo.

1. Entrada [!DNL Excel], cree una plantilla personalizada para el informe:

   1. Abra el archivo de informe en [!DNL Excel].

   1. Prepare el libro:

      1. Elimine las filas superiores que muestran los parámetros del informe. Para archivos XLS, elimine también el &quot;[!UICONTROL Total]&quot; fila. Si lo desea, puede eliminar algunas de las filas de datos, pero mantenga a) la fila del encabezado de datos con todas las columnas en el orden original y b) al menos una fila de datos. No agregue manualmente ningún dato.

         >[!NOTE]
         >
         > La última columna debe incluir valores distintos de cero.

      2. Ordene los datos por fecha de inicio en orden ascendente (de la más antigua a la más reciente).

      3. Cambie el nombre de la pestaña de la hoja de cálculo de &quot;[!UICONTROL Sheet1]&quot; a &quot;[!UICONTROL RAW].&quot;

         Este nombre de ficha específico permite actualizar los datos.

      4. (Opcional) Agregue columnas personalizadas a la derecha de las columnas de la plantilla del informe, según sea necesario.

   1. (Opcional) En una hoja de cálculo independiente, cree una tabla dinámica. Una vez finalizado, haga clic con el botón derecho en cualquier celda de la tabla dinámica y seleccione **[!UICONTROL Pivot Table Options]**, haga clic en **[!UICONTROL Data]** , y luego seleccione **[!UICONTROL Refresh data when opening the file]**.

   1. Guarde el archivo como una [!DNL Excel] hoja de cálculo en formato .XLSX.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de informes](spreadsheet-feed-about.md)
>* [Crear una fuente de informes de hoja de cálculo](spreadsheet-feed-create.md)
>* [Editar configuración de fuente de informes de hoja de cálculo](spreadsheet-feed-edit.md)
>* [Configuración de fuente de informe de hoja de cálculo](spreadsheet-feed-settings.md)
>* [Ver o guardar un archivo de fuente de informes de hoja de cálculo](spreadsheet-feed-view-or-save.md)
>* [Actualizar manualmente fuentes de informes de hoja de cálculo](spreadsheet-feed-refresh.md)
>* [Eliminar fuentes de informes de hoja de cálculo](spreadsheet-feed-delete.md)
