---
title: Publicación de hojas de edición masiva o archivos de error corregidos
description: Aprenda a publicar archivos de hojas de edición masiva en las redes de anuncios.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Publicación de hojas de edición masiva o archivos de error corregidos

Puede publicar archivos de hojas de edición masiva existentes o archivos de error corregidos en las cuentas relevantes para [redes de publicidad admitidas](bulksheet-about.md#bulksheet-functionality-by-network). Si el archivo está en formato ZIP, no es necesario descomprimirlo primero.

Los archivos de hojas de edición masiva y los archivos de error se eliminan automáticamente 30 días después de cargarse o generarse.

>[!NOTE]
>También puede publicar un archivo de hoja de edición por lotes o un archivo de error al cargar el archivo.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Seleccione la casilla de verificación situada junto a cada archivo que desee publicar.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Post]**.

1. En el cuadro de diálogo, introduzca o seleccione información en la [[!UICONTROL Post Bulksheet] configuración](#bulksheet-post-settings)y haga clic en **[!UICONTROL Post]**.

   La misma configuración se aplica a todos los archivos que publique.

Cuando comienza la tarea, el estado y la fecha posterior programada de la fila se cambian en la [!UICONTROL Bulksheets] vista. Cuando se publica el archivo, se envía una notificación por correo electrónico con un vínculo al archivo. Según la cantidad de datos recopilados, la notificación por correo electrónico puede tardar varios minutos o más. Sin embargo, si alguno de los datos no se puede publicar, aparece un archivo de error en la [!UICONTROL Bulksheets] y se envía una notificación por correo electrónico con un vínculo al archivo de error.

>[!NOTE]
>
>* Las grandes cantidades de datos tardan más en publicarse. Puede seguir el progreso del archivo en la [!UICONTROL Progress] en la columna [!UICONTROL Bulksheets] vista.
>* Todos los datos publicados están sujetos al proceso editorial de la red.

* Antes de publicar el archivo de hoja de edición masiva, puede cancelar la publicación.

## Configuración de publicación para hojas de edición masiva y archivos de error corregidos {#bulksheet-post-settings}

| Parámetro | Descripción |
|----|----|
| [!UICONTROL Account (Search Engine)] | La cuenta de red de publicidad para la que se publican los datos. Si publica varios archivos simultáneamente o un archivo que se aplica a varias cuentas, el valor es <i>Varias cuentas seleccionadas</i>.<br><br>La primera letra del nombre de la red de anuncios aparece entre paréntesis después del nombre de la cuenta (como &quot;Acme Realty (G)&quot;) para un [!DNL Google Ads] account). |
| [!UICONTROL Scheduling] | Cuándo publicar el archivo en la red de anuncios especificada:<ul><li><i>[!UICONTROL Post to ad network now]</i> (predeterminado): Empieza a publicar los datos inmediatamente.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Comienza a publicar los datos en la fecha y hora especificadas; el valor predeterminado es mañana a las 02:00 (2 a. m.). Para cambiar la fecha, introduzca una fecha con el formato DD/MM/AAAA o D/M/AAAA o haga clic en ![Calendario](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md "Calendario") para abrir el calendario y [seleccionar una fecha](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para cambiar la hora, introdúzcala con el formato HH/MM o H/M o seleccione una hora (en intervalos de 15 minutos) de la lista.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Si se incluyen plantillas de seguimiento y sufijos de página de aterrizaje (para redes de anuncios aplicables) en cuentas con plantillas de seguimiento o URL de destino con códigos de seguimiento incrustados en cuentas con URL de destino, para todas las palabras clave, anuncios, ubicaciones, vínculos a sitios y [!DNL Google Ads] grupos de productos en la publicación: <i>[!UICONTROL Yes]</i> (el valor predeterminado) o <i>[!UICONTROL No]</i>. No importa si las unidades de oferta están en una cartera.<br><br>Si selecciona <i>[!UICONTROL Yes]</i>, las direcciones URL se generan según los parámetros del [!UICONTROL Tracking Methods] de la configuración de la cuenta o la configuración de la campaña relevantes. De forma predeterminada, si existen direcciones URL de seguimiento, estas no se regeneran a menos que se necesiten nuevas direcciones URL (por ejemplo, si ha cambiado el tipo de coincidencia de palabra clave, el texto del anuncio o los parámetros de seguimiento de las cuentas relevantes).<br><br>Si selecciona <i>[!UICONTROL No]</i>, aún puede generar direcciones URL de seguimiento más adelante publicando manualmente el archivo cargado.<br><br><b>Nota:</b> Si el anunciante utiliza el seguimiento de conversión de la publicidad Adobe y la dirección URL base ha cambiado, debe generar nuevas direcciones URL de seguimiento, a menos que la cuenta esté configurada para generar y cargar automáticamente las direcciones URL de seguimiento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite cambios de presupuesto en campañas en portafolios optimizados basados en datos publicados. De forma predeterminada, esta opción no está seleccionada. Si selecciona esta opción, cualquier cambio de presupuesto de campaña especificado es aplicable hasta que la capacidad de optimización determine que el presupuesto debe reasignarse (normalmente en el siguiente ciclo de oferta).<br><br><b>Nota:</b> Cualquier cambio de presupuesto que resulte de los datos publicados para campañas en portafolios no optimizados se produce cuando se publica el archivo. Los cambios aparecen en las vistas de administración de campañas al día siguiente. |
| [!UICONTROL Enable bidding on ads within portfolios] | Cuando los componentes de campaña incluidos están en un portafolio optimizado, esta función anula la estrategia de optimización y permite cambios de oferta basados en los datos de la hoja de edición masiva hasta una fecha de finalización especificada. Si selecciona esta opción, especifique una fecha de finalización entre 1 y 7 días fuera en la **[!UICONTROL Hold bulksheet bids until]** field. |

>[!MORELIKETHIS]
>
>* [Administración de datos de campaña mediante hojas de edición masiva](bulksheet-about.md)
>* [Descargar/crear un archivo de hoja de edición masiva](bulksheet-download.md)
>* [Carga de hojas de edición masiva o archivos de error corregidos](bulksheet-upload.md)
>* [Validación de páginas de aterrizaje en archivos de hoja de edición masiva](bulksheet-validate-landing-pages.md)
>* [Exportar un archivo de hoja de edición masiva generado o cargado](bulksheet-export.md)

