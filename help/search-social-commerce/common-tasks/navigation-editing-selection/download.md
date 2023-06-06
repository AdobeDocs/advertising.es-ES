---
title: Descarga de datos desde una vista de administración de campañas
description: Obtenga información sobre cómo descargar datos de la mayoría de las vistas de administración de campañas.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Descarga de datos desde una vista de administración de campañas

Puede descargar datos desde el [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vistas, excepto la [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences], y [!UICONTROL Extensions] vistas. Puede descargar lo siguiente:

* Un informe en [!DNL XLSM] (habilitado para macros [!DNL Microsoft® Excel] hoja de cálculo). Si selecciona filas específicas en la vista, el informe incluye una fila para cada fila seleccionada. Si no selecciona ninguna fila, se crea una fila para cada fila de la vista.

* Archivo de hoja de edición masiva en formato TXT que incluye todas las entidades secundarias relevantes. Si selecciona filas para entidades en varias redes de publicidad, se crea un archivo para cada red de publicidad relevante. Si no selecciona ninguna fila, se crea un archivo para cada red de publicidad representada en la vista. Los archivos de hojas de edición masiva generados para diferentes redes de anuncios incluyen diferentes columnas de datos.

   Si genera datos para varias campañas y los datos combinados constan de más de 500 000 filas, los datos se dividen además por campaña en dos o más archivos, según sea necesario, con el nombre `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`, etc.

   Cada archivo de hoja de edición masiva del [!UICONTROL Downloads] el panel también aparece en la [!UICONTROL Bulksheets] vista. Cuando se crea el archivo, recibe una notificación por correo electrónico con un vínculo desde el que puede descargar el archivo; según la cantidad de datos que se compile, la notificación puede tardar varios minutos o más. Sin embargo, si falla la generación del archivo, aparece un archivo de error en la vista Hojas de edición masiva y recibe una notificación por correo electrónico con un vínculo al archivo de error. Eliminación de un archivo de hoja de edición masiva desde [!UICONTROL Download] o el [!UICONTROL Bulksheets] La pestaña lo elimina de ambas ubicaciones.

1. (Opcional) Seleccione las filas individuales que desea incluir en el archivo.

   De lo contrario, se incluyen todos los datos de la vista.

1. En la parte derecha de la barra de herramientas, haga clic en ![Descarga de informe](/help/search-social-commerce/assets/download.png "Descarga de informe").

1. Clic ![Crear](/help/search-social-commerce/assets/add.png "Crear") **[!UICONTROL Create]**, si lo desea, agregue el nombre del archivo y haga clic en **[!UICONTROL Report]** o **[!UICONTROL Bulksheet]**.

1. (Opcional) Una vez completado el trabajo del informe, haga clic en ![Descarga de informe](/help/search-social-commerce/assets/download.png "Descarga de informe") para ver la [!UICONTROL Available Reports] y, a continuación, descargue o elimine el informe:

   * Para abrir o guardar el archivo según el procedimiento normal del explorador, haga clic en ![Descargar hoja de cálculo](/help/search-social-commerce/assets/download-spreadsheet.png "Descargar hoja de cálculo").

      Para obtener más información sobre el procedimiento del explorador, consulte la ayuda en línea del explorador.

   * Para eliminar el archivo, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar").

>[!MORELIKETHIS]
>
>[Elimine un informe de datos de rendimiento o un archivo de hoja de edición masiva del [!UICONTROL Downloads] menú](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
