---
title: Cargar una hoja de edición masiva o un archivo de error corregido
description: Obtenga información sobre cómo cargar manualmente un archivo de hoja de edición masiva o un archivo de error de validación de página de aterrizaje corregido.
exl-id: 34843245-6c55-489c-8e04-f8bae4046ae4
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Cargar una hoja de edición masiva o un archivo de error corregido

Puede cargar archivos de hojas de edición masiva, archivos de error de validación de páginas de aterrizaje corregidos y otros archivos de error corregidos desde su dispositivo o red para [redes de publicidad admitidas](bulksheet-about.md#bulksheet-functionality-by-network). Todas las columnas personalizadas del archivo se eliminan al cargarlo.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Upload Bulksheet]**.

1. Introduzca o seleccione información en la [[!UICONTROL Upload Bulksheet] configuración](#bulksheet-upload-settings).

1. Haga clic **[!UICONTROL Apply]**.

Cuando comience la tarea, el archivo aparecerá en la lista de [!UICONTROL Bulksheets] vista. Cuando se completa el archivo, se envía una notificación por correo electrónico con un vínculo al archivo. Según la cantidad de datos recopilados, la notificación por correo electrónico puede tardar varios minutos o más. Sin embargo, si la generación de archivos falla, aparece un archivo de error en la [!UICONTROL Bulksheets] y se envía una notificación por correo electrónico con un vínculo al archivo de error.

>[!NOTE]
>
>Si publica los datos de la hoja de edición masiva en la red publicitaria, puede seguir el progreso del archivo en la [!UICONTROL Progress] en la columna [!UICONTROL Bulksheets] vista. Las grandes cantidades de datos tardan más en publicarse.

## Configuración de carga de hojas de edición masiva y archivos de error corregidos {#bulksheet-upload-settings}

| Parámetro | Descripción |
|----|----|
| [!UICONTROL File to Upload] | El archivo que se va a cargar. Especifique el archivo introduciendo la ruta de acceso completa y el nombre del archivo o haciendo clic en <b>[!UICONTROL Browse]</b> para localizar el archivo en su dispositivo o red.<br><br>Los archivos de hojas de edición masiva pueden tener hasta 2,5 GB (aproximadamente 2,5 millones de filas) y deben tener una de las siguientes extensiones de archivo: <i>[!UICONTROL .tsv]</i> (para valores separados por tabulaciones), <i>[!UICONTROL .txt]</i> (para texto ASCII compatible con Unicode), <i>[!UICONTROL .csv]</i> (para valores separados por comas), o <i>[!UICONTROL .zip]</i> (para el formato ZIP comprimido, que se descomprime en un archivo TSV). El nombre de archivo no puede incluir los siguientes caracteres: `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Sugerencia:</b> Para datos que incluyen caracteres internacionales, utilice archivos en formato TSV o TXT. |
| [!UICONTROL Single Account] | Si el archivo se aplica a una cuenta: <i>[!UICONTROL Yes]</i> (para una cuenta) o <i>[!UICONTROL No]</i>(para varias cuentas). |
| [!UICONTROL Account (Search Engine)] | (Cuando el archivo se aplica a una sola cuenta) La cuenta a la que cargar los datos. |
| [!UICONTROL Search Engine] | (Cuando el archivo se aplica a varias cuentas) La red de publicidad a la que cargar los datos. |
| [!UICONTROL Scheduling] | Cuándo o si publicar el archivo en la red de anuncios especificada:<ul><li><i>[!UICONTROL Post to ad network now]</i> (predeterminado): Empieza a publicar los datos inmediatamente.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Comienza a publicar los datos en la fecha y hora especificadas; el valor predeterminado es mañana a las 02:00 (2 a. m.). Para cambiar la fecha, introduzca una fecha con el formato DD/MM/AAAA o D/M/AAAA o haga clic en ![Calendario](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md "Calendario") para abrir el calendario y [seleccionar una fecha](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para cambiar la hora, introdúzcala con el formato HH/MM o H/M o seleccione una hora (en intervalos de 15 minutos) de la lista.</li><li><i>[!UICONTROL Preview only]:</i> Para cargar el archivo en Search, Social y Commerce sin publicar los datos en la red de publicidad; aún puede publicar el archivo más tarde. Cuando el archivo de hoja de edición masiva ocupa más de 10 MB pero menos de 2 GB, el archivo está en formato ZIP; no es necesario descomprimir el archivo para publicarlo.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Si se incluyen plantillas de seguimiento y sufijos de página de aterrizaje (para redes de anuncios aplicables) en cuentas con plantillas de seguimiento o URL de destino con códigos de seguimiento incrustados en cuentas con URL de destino, para todas las palabras clave, anuncios, ubicaciones, vínculos a sitios y [!DNL Google Ads] grupos de productos en la publicación: <i>[!UICONTROL Yes]</i> (el valor predeterminado) o <i>[!UICONTROL No]</i>. No importa si las unidades de oferta están en una cartera.<br><br>Si selecciona <i>[!UICONTROL Yes]</i>, las direcciones URL se generan según los parámetros del [!UICONTROL Tracking Methods] de la configuración de la cuenta o la configuración de la campaña relevantes. De forma predeterminada, si existen direcciones URL de seguimiento, estas no se regeneran a menos que se necesiten nuevas direcciones URL (por ejemplo, si ha cambiado el tipo de coincidencia de palabra clave, el texto del anuncio o los parámetros de seguimiento de las cuentas relevantes).<br><br>Si selecciona <i>[!UICONTROL No]</i>, aún puede generar direcciones URL de seguimiento más adelante publicando manualmente el archivo cargado.<br><br><b>Nota:</b> Si el anunciante utiliza el seguimiento de conversión de Adobes Advertising y la dirección URL base ha cambiado, debe generar nuevas direcciones URL de seguimiento a menos que la cuenta esté configurada para generar y cargar automáticamente direcciones URL de seguimiento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite cambios de presupuesto en campañas en portafolios optimizados basados en datos publicados. De forma predeterminada, esta opción no está seleccionada. Si selecciona esta opción, cualquier cambio de presupuesto de campaña especificado es aplicable hasta que la capacidad de optimización determine que el presupuesto debe reasignarse (normalmente en el siguiente ciclo de oferta).<br><br><b>Nota:</b> Cualquier cambio de presupuesto que resulte de los datos publicados para campañas en portafolios no optimizados se produce cuando se publica el archivo. Los cambios aparecen en las vistas de administración de campañas al día siguiente. |
| [!UICONTROL Enable bidding on ads within portfolios] | Cuando los componentes de campaña incluidos están en un portafolio optimizado, esta función anula la estrategia de optimización y permite cambios de oferta basados en los datos de la hoja de edición masiva hasta una fecha de finalización especificada. Si selecciona esta opción, especifique una fecha de finalización entre 1 y 7 días fuera en la **[!UICONTROL Hold bulksheet bids until]** field. |

>[!MORELIKETHIS]
>
>* [Administración de datos de campaña mediante hojas de edición masiva](bulksheet-about.md)
>* [Descargar/crear un archivo de hoja de edición masiva](bulksheet-download.md)
>* [Publicación de hojas de edición masiva o archivos de error corregidos](bulksheet-post.md)
>* [Validación de páginas de aterrizaje en archivos de hoja de edición masiva](bulksheet-validate-landing-pages.md)
>* [Exportar un archivo de hoja de edición masiva generado o cargado](bulksheet-export.md)
