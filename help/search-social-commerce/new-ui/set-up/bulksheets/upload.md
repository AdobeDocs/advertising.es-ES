---
title: (Nueva IU) Cargar una hoja de edición masiva o un archivo de error corregido
description: Obtenga información sobre cómo cargar manualmente un archivo de hoja de edición por lotes o el archivo de error de validación corregido de la página de aterrizaje en la nueva IU de Search, Social y Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 38fd7ff63b177f13bdfb19b980fb1d1e14edcf56
workflow-type: tm+mt
source-wordcount: 830
ht-degree: 0%

---

# (Nueva IU) Cargar una hoja de edición masiva o un archivo de error corregido

Puede cargar archivos de hojas de edición masiva, archivos de error corregidos de validación de páginas de aterrizaje y otros archivos de error corregidos desde su dispositivo o red para [redes de anuncios compatibles](about.md#bulksheet-functionality-by-network). Todas las columnas personalizadas del archivo se eliminan al cargarlo.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. En la barra de herramientas, haga clic en **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**.

1. Especifique o seleccione información en la configuración [[!UICONTROL Upload Bulksheet]](#bulksheet-upload-settings).

1. Haga clic en **[!UICONTROL Upload]**.

Cuando comienza la tarea, el archivo aparece en la vista [!UICONTROL Bulksheets]. Cuando las notificaciones por correo electrónico para hojas de edición masiva están [habilitadas en [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md), se envía una notificación por correo electrónico con un vínculo al archivo cuando se completa el trabajo. Según la cantidad de datos recopilados, la notificación por correo electrónico puede tardar varios minutos o más. Si falla la generación del archivo, aparece un archivo de error en la vista [!UICONTROL Bulksheets] y se envía una notificación por correo electrónico con un vínculo al archivo de error.

>[!NOTE]
>
>Si publica los datos de la hoja de edición masiva en la red publicitaria, puede seguir el progreso del archivo en la columna [!UICONTROL Progress] de la vista [!UICONTROL Bulksheets]. Las grandes cantidades de datos tardan más en publicarse.

## Configuración de carga de hojas de edición masiva y archivos de error corregidos {#bulksheet-upload-settings}

| Parámetro | Descripción |
|----|----|
| [!UICONTROL File to Upload] | El archivo que se va a cargar. Especifique el archivo haciendo clic en **[!UICONTROL Choose File]** para localizarlo en su dispositivo o red.<br><br>Los archivos de hojas de edición masiva pueden tener hasta 2,5 GB (aproximadamente 2,5 millones de filas) y deben tener una de las siguientes extensiones de archivo: *[!UICONTROL .tsv]* (para valores separados por tabulaciones), *[!UICONTROL .txt]* (para texto ASCII compatible con Unicode), *[!UICONTROL .csv]* (para valores separados por comas) o *[!UICONTROL .zip]* (para formato ZIP comprimido, que se descomprime en un archivo TSV). El nombre de archivo no puede incluir los siguientes caracteres: `# % & * \| \ : " < > . ? /`<br><br>**Sugerencia:** Para los datos que incluyen caracteres internacionales, utilice archivos en formato TSV o TXT. |
| [!UICONTROL Single Account] | Si el archivo se aplica a una cuenta: *[!UICONTROL Yes]* (para una cuenta) o *[!UICONTROL No]* (para varias cuentas). |
| [!UICONTROL Account (Search Engine)] | (Cuando el archivo se aplica a una sola cuenta) La cuenta a la que cargar los datos. |
| [!UICONTROL Search Engine] | (Cuando el archivo se aplica a varias cuentas) La red de anuncios a la que cargar los datos.<br><br>**Nota:** Los cambios de oferta para palabras clave en portafolios optimizados no se admiten con hojas de edición por lotes de varias cuentas. |
| [!UICONTROL Scheduling] | Cuándo o si publicar el archivo en la red de anuncios especificada:<ul><li>*[!UICONTROL Post to search engine now]* (valor predeterminado): comienza a publicar los datos inmediatamente.</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]:* Comienza a publicar los datos en la fecha y hora especificadas; el valor predeterminado es mañana a las 02:00 (2 a. m.). Para cambiar la fecha, introduzca una fecha con el formato DD/MM/AAAA o haga clic en el icono de calendario para abrir el calendario y seleccionar una fecha. Para cambiar la hora, seleccione una hora (en intervalos de 15 minutos) en la lista.</li><li>*[!UICONTROL Preview only]:* carga el archivo en Search, Social y Commerce sin publicar los datos en la red de anuncios; aún puede publicar el archivo más tarde. Cuando el archivo de hoja de edición masiva ocupa más de 10 MB pero menos de 2 GB, el archivo está en formato ZIP; no es necesario descomprimir el archivo para publicarlo.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Si se incluyen plantillas de seguimiento y sufijos de página de aterrizaje (para redes de anuncios aplicables) en cuentas con plantillas de seguimiento o direcciones URL de destino con códigos de seguimiento incrustados en cuentas con direcciones URL de destino, para todas las palabras clave, anuncios, ubicaciones, vínculos de sitios y [!DNL Google Ads] grupos de productos en la publicación: *[!UICONTROL Yes]* (el valor predeterminado) o *[!UICONTROL No]*. No importa si las unidades de oferta están en una cartera.<br><br>Si selecciona *[!UICONTROL Yes]*, las direcciones URL se generan según los parámetros de la sección [!UICONTROL Tracking Methods] de la configuración de cuenta o de campaña correspondiente. De manera predeterminada, si existen direcciones URL de seguimiento, no se regeneran a menos que se necesiten nuevas direcciones URL (como si el tipo de coincidencia de palabra clave, el texto del anuncio o los parámetros de seguimiento de las cuentas relevantes han cambiado).<br><br>Si selecciona *[!UICONTROL No]*, puede generar direcciones URL de seguimiento más adelante publicando manualmente el archivo cargado.<br><br>**Nota:** Si el anunciante utiliza el seguimiento de conversión de Adobe Advertising y la dirección URL base ha cambiado, debe generar nuevas direcciones URL de seguimiento a menos que la cuenta esté configurada para generar y cargar automáticamente direcciones URL de seguimiento. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Disponible cuando [!UICONTROL Generate Tracking URLs] es *[!UICONTROL Yes]*) Reemplaza cualquier seguimiento de Adobe Advertising existente en las direcciones URL del archivo cargado con un seguimiento recién generado. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite cambios de presupuesto en campañas en portafolios optimizados basados en datos publicados. De forma predeterminada, esta opción no está seleccionada. Si selecciona esta opción, cualquier cambio de presupuesto de campaña especificado se aplicará hasta que la capacidad de optimización determine que el presupuesto se debe reasignar (normalmente en el siguiente ciclo de oferta).<br><br>**Nota:** Cualquier cambio de presupuesto que resulte de los datos publicados para campañas en portafolios no optimizados se producirá cuando se publique el archivo. Los cambios aparecen en las vistas de administración de campañas al día siguiente. |
| [!UICONTROL Enable bidding on ads within portfolios] | Cuando los componentes de campaña incluidos están en un portafolio optimizado, esta función anula la estrategia de optimización y permite cambios de oferta basados en los datos de la hoja de edición masiva hasta una fecha de finalización especificada. Si selecciona esta opción, especifique una fecha de finalización entre 1 y 7 días en el campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [(Nueva IU) Acerca de la administración de datos de campaña mediante hojas de edición por lotes](about.md)
>* [(Nueva interfaz de usuario) Descargar o crear un archivo de hoja de edición por lotes](download.md)
>* [(Nueva IU) Publicar hojas de edición masiva o archivos de error corregidos](post.md)
>* [(Nueva IU) Validar páginas de aterrizaje en archivos de hojas de edición masiva](validate-landing-pages.md)
