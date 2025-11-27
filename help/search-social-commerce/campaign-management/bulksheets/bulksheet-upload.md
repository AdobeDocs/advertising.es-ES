---
title: Cargar una hoja de edición masiva o un archivo de error corregido
description: Obtenga información sobre cómo cargar manualmente un archivo de hoja de edición masiva o un archivo de error de validación de página de aterrizaje corregido.
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Cargar una hoja de edición masiva o un archivo de error corregido

Puede cargar archivos de hojas de edición masiva, archivos de error corregidos de validación de páginas de aterrizaje y otros archivos de error corregidos desde su dispositivo o red para [redes de anuncios compatibles](bulksheet-about.md#bulksheet-functionality-by-network). Todas las columnas personalizadas del archivo se eliminan al cargarlo.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Upload Bulksheet]**.

1. Especifique o seleccione información en la configuración [[!UICONTROL Upload Bulksheet]](#bulksheet-upload-settings).

1. Haga clic en **[!UICONTROL Apply]**.

Cuando comienza la tarea, el archivo aparece en la vista [!UICONTROL Bulksheets]. Cuando se completa el archivo, se envía una notificación por correo electrónico con un vínculo al archivo. Según la cantidad de datos recopilados, la notificación por correo electrónico puede tardar varios minutos o más. Sin embargo, si se produce un error en la generación del archivo, aparece un archivo de error en la vista [!UICONTROL Bulksheets] y se envía una notificación por correo electrónico con un vínculo al archivo de error.

>[!NOTE]
>
>Si publica los datos de la hoja de edición masiva en la red publicitaria, puede seguir el progreso del archivo en la columna [!UICONTROL Progress] de la vista [!UICONTROL Bulksheets]. Las grandes cantidades de datos tardan más en publicarse.

## Configuración de carga de hojas de edición masiva y archivos de error corregidos {#bulksheet-upload-settings}

| Parámetro | Descripción |
|----|----|
| [!UICONTROL File to Upload] | El archivo que se va a cargar. Especifique el archivo introduciendo la ruta de acceso completa y el nombre de archivo o haciendo clic en <b>[!UICONTROL Browse]</b> para localizarlo en su dispositivo o red.<br><br>Los archivos de hojas de edición masiva pueden tener hasta 2,5 GB (aproximadamente 2,5 millones de filas) y deben tener una de las siguientes extensiones de archivo: <i>[!UICONTROL .tsv]</i> (para valores separados por tabulaciones), <i>[!UICONTROL .txt]</i> (para texto ASCII compatible con Unicode), <i>[!UICONTROL .csv]</i> (para valores separados por comas) o <i>[!UICONTROL .zip]</i> (para formato ZIP comprimido, que se descomprime en un archivo TSV). El nombre de archivo no puede incluir los siguientes caracteres: `# % &amp; * \| \ : " < > . ? /`<br><br><b>Sugerencia:</b> Para los datos que incluyen caracteres internacionales, utilice archivos en formato TSV o TXT. |
| [!UICONTROL Single Account] | Si el archivo se aplica a una cuenta: <i>[!UICONTROL Yes]</i> (para una cuenta) o <i>[!UICONTROL No]</i> (para varias cuentas). |
| [!UICONTROL Account (Search Engine)] | (Cuando el archivo se aplica a una sola cuenta) La cuenta a la que cargar los datos. |
| [!UICONTROL Search Engine] | (Cuando el archivo se aplica a varias cuentas) La red de publicidad a la que cargar los datos. |
| [!UICONTROL Scheduling] | Cuándo o si publicar el archivo en la red de anuncios especificada:<ul><li><i>[!UICONTROL Post to ad network now]</i> (valor predeterminado): comienza a publicar los datos inmediatamente.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Comienza a publicar los datos en la fecha y hora especificadas; el valor predeterminado es mañana a las 02:00 (2 a. m.). Para cambiar la fecha, escriba una fecha con el formato DD/MM/AAAA o D/M/AAAA o haga clic en ![Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") para abrir el calendario y [seleccionar una fecha](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para cambiar la hora, introdúzcala con el formato HH/MM o H/M o seleccione una hora (en intervalos de 15 minutos) de la lista.</li><li><i>[!UICONTROL Preview only]:</i> Para cargar el archivo en Search, Social y Commerce sin publicar los datos en la red de publicidad; aún puede publicar el archivo más tarde. Cuando el archivo de hoja de edición masiva ocupa más de 10 MB pero menos de 2 GB, el archivo está en formato ZIP; no es necesario descomprimir el archivo para publicarlo.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Si se incluyen plantillas de seguimiento y sufijos de página de aterrizaje (para redes de anuncios aplicables) en cuentas con plantillas de seguimiento o direcciones URL de destino con códigos de seguimiento incrustados en cuentas con direcciones URL de destino, para todas las palabras clave, anuncios, ubicaciones, vínculos de sitios y [!DNL Google Ads] grupos de productos en la publicación: <i>[!UICONTROL Yes]</i> (el valor predeterminado) o <i>[!UICONTROL No]</i>. No importa si las unidades de oferta están en una cartera.<br><br>Si selecciona <i>[!UICONTROL Yes]</i>, las direcciones URL se generan según los parámetros de la sección [!UICONTROL Tracking Methods] de la configuración de cuenta o de campaña correspondiente. De forma predeterminada, si existen direcciones URL de seguimiento, estas no se regeneran a menos que se necesiten nuevas direcciones URL (por ejemplo, si ha cambiado el tipo de coincidencia de palabra clave, el texto del anuncio o los parámetros de seguimiento de las cuentas relevantes).<br><br>Si selecciona <i>[!UICONTROL No]</i>, puede generar direcciones URL de seguimiento más adelante publicando manualmente el archivo cargado.<br><br><b>Nota:</b> Si el anunciante usa el seguimiento de conversión de Adobe Advertising y la dirección URL base ha cambiado, debe generar nuevas direcciones URL de seguimiento a menos que la cuenta esté configurada para generar y cargar automáticamente direcciones URL de seguimiento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite cambios de presupuesto en campañas en portafolios optimizados basados en datos publicados. De forma predeterminada, esta opción no está seleccionada. Si selecciona esta opción, cualquier cambio de presupuesto de campaña especificado es aplicable hasta que la capacidad de optimización determine que el presupuesto debe reasignarse (normalmente en el siguiente ciclo de oferta).<br><br><b>Nota:</b> Cualquier cambio de presupuesto que resulte de los datos publicados para campañas en portafolios no optimizados se producirá cuando se publique el archivo. Los cambios aparecen en las vistas de administración de campañas al día siguiente. |
| [!UICONTROL Enable bidding on ads within portfolios] | Cuando los componentes de campaña incluidos están en un portafolio optimizado, esta función anula la estrategia de optimización y permite cambios de oferta basados en los datos de la hoja de edición masiva hasta una fecha de finalización especificada. Si selecciona esta opción, especifique una fecha de finalización entre 1 y 7 días en el campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [Acerca de la administración de datos de campaña mediante hojas de edición masiva](bulksheet-about.md)
>* [Descargar o crear un archivo de hoja de edición masiva](bulksheet-download.md)
>* [Publicar hojas de edición masiva o archivos de error corregidos](bulksheet-post.md)
>* [Validar páginas de aterrizaje en archivos de hojas de edición masiva](bulksheet-validate-landing-pages.md)
>* [Exportar un archivo de hoja de edición masiva generado o cargado](bulksheet-export.md)
