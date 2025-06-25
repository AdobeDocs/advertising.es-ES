---
title: Descarga de datos desde una vista de administración de campañas
description: Obtenga información sobre cómo descargar datos de la mayoría de las vistas de administración de campañas.
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Descarga de datos desde una vista de administración de campañas

Puede descargar datos de las vistas [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns], excepto las vistas [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences] y [!UICONTROL Extensions]. Puede descargar lo siguiente:

* Un informe en formato [!DNL XLSM] (hoja de cálculo [!DNL Microsoft Excel] habilitada para macros). Si selecciona filas específicas en la vista, el informe incluye una fila para cada fila seleccionada. Si no selecciona ninguna fila, se crea una fila para cada fila de la vista.

* Archivo de hoja de edición masiva en formato TXT que incluye todas las entidades secundarias relevantes. Si selecciona filas para entidades en varias redes de publicidad, se crea un archivo para cada red de publicidad relevante. Si no selecciona ninguna fila, se crea un archivo para cada red de publicidad representada en la vista. Los archivos de hojas de edición masiva generados para diferentes redes de anuncios incluyen diferentes columnas de datos.

  Si genera datos para varias campañas y los datos combinados constan de más de 500 000 filas, los datos se dividirán adicionalmente por campaña en dos o más archivos, según sea necesario, con los nombres `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`, etc.

  Cada archivo de hoja de edición masiva del panel [!UICONTROL Downloads] también aparece en la vista [!UICONTROL Bulksheets]. Cuando se crea el archivo, recibe una notificación por correo electrónico con un vínculo desde el que puede descargar el archivo; según la cantidad de datos que se compile, la notificación puede tardar varios minutos o más. Sin embargo, si falla la generación del archivo, aparece un archivo de error en la vista Hojas de edición masiva y recibe una notificación por correo electrónico con un vínculo al archivo de error. Al eliminar un archivo de hoja de edición masiva del panel [!UICONTROL Download] o de la ficha [!UICONTROL Bulksheets], se eliminará de ambas ubicaciones.

1. (Opcional) Seleccione las filas individuales que desea incluir en el archivo.

   De lo contrario, se incluyen todos los datos de la vista.

1. A la derecha de la barra de herramientas, haz clic en ![Descarga de informe](/help/search-social-commerce/assets/download.png "Descarga de informe").

1. Haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear") **[!UICONTROL Create]**, agregue de forma opcional el nombre de archivo y, a continuación, haga clic en **[!UICONTROL Report]** o **[!UICONTROL Bulksheet]**.

1. (Opcional) Una vez completado el trabajo del informe, haga clic en ![Descarga de informe](/help/search-social-commerce/assets/download.png "Descarga de informe") para ver el panel [!UICONTROL Available Reports] y, a continuación, descargue o elimine el informe:

   * Para abrir o guardar el archivo según el procedimiento normal del explorador, haga clic en ![Descargar hoja de cálculo](/help/search-social-commerce/assets/download-spreadsheet.png "Descargar hoja de cálculo").

     Para obtener más información sobre el procedimiento del explorador, consulte la ayuda en línea del explorador.

   * Para eliminar el archivo, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar").

>[!MORELIKETHIS]
>
>[Elimine un informe de datos de rendimiento o un archivo de hoja de edición masiva del menú [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
