---
title: (Nueva IU) Publicar hojas de edición masiva o archivos de error corregidos
description: Aprenda a publicar archivos de hojas de edición masiva en las redes de anuncios en la nueva IU de Search, Social y Commerce.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# (Nueva IU) Publicar hojas de edición masiva o archivos de error corregidos

Puede publicar archivos de hojas de edición masiva existentes o archivos de error corregidos en las cuentas relevantes para [redes de anuncios compatibles](about.md#bulksheet-functionality-by-network). Si el archivo está en formato ZIP, no es necesario descomprimirlo primero.

Los archivos de hojas de edición masiva y los archivos de error se eliminan automáticamente 30 días después de cargarse o generarse.

>[!NOTE]
>
>También puede publicar un archivo de hoja de edición por lotes o un archivo de error al cargar el archivo.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Seleccione la casilla de verificación situada junto a cada archivo que desee publicar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Post]**.

1. Escriba o seleccione información en la configuración [[!UICONTROL Post Bulksheet]](#bulksheet-post-settings) y, a continuación, haga clic en **[!UICONTROL Post]**.

   La misma configuración se aplica a todos los archivos que publique.

Cuando comienza la tarea, el estado y la fecha posterior programada de la fila se actualizan en la vista [!UICONTROL Bulksheets]. Cuando las notificaciones por correo electrónico para hojas de edición masiva están [habilitadas en [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md), se enviará una notificación por correo electrónico con un vínculo al archivo cuando se publique el archivo. Según la cantidad de datos recopilados, la notificación por correo electrónico puede tardar varios minutos o más. Si no se puede publicar alguno de los datos, aparecerá un archivo de error en la vista [!UICONTROL Bulksheets] y se enviará una notificación por correo electrónico con un vínculo al archivo de error.

>[!NOTE]
>
>* Las grandes cantidades de datos tardan más en publicarse. Puede seguir el progreso del archivo en la columna [!UICONTROL Progress] de la vista [!UICONTROL Bulksheets].
>* Todos los datos publicados están sujetos al proceso editorial de la red.
>* Antes de publicar el archivo de hoja de edición masiva, puede cancelar la publicación.

## Configuración de publicación para hojas de edición masiva y archivos de error corregidos {#bulksheet-post-settings}

| Parámetro | Descripción |
|----|----|
| [!UICONTROL Account (Search Engine)] | La cuenta de red de publicidad para la que se publican los datos. Si publica varios archivos simultáneamente o un archivo que se aplica a varias cuentas, el valor es *Varias cuentas seleccionadas*.<br><br>La primera letra del nombre de red de anuncios está entre paréntesis después del nombre de cuenta (como &quot;Acme Realty (G)&quot; para una cuenta de [!DNL Google Ads]). |
| [!UICONTROL Scheduling] | Cuándo publicar el archivo en la red de anuncios especificada:<ul><li>*[!UICONTROL Post to ad network now]* (valor predeterminado): comienza a publicar los datos inmediatamente.</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:* Comienza a publicar los datos en la fecha y hora especificadas; el valor predeterminado es mañana a las 02:00 (2 a. m.). Para cambiar la fecha, introduzca una fecha con el formato DD/MM/AAAA o haga clic en el icono de calendario para abrir el calendario y seleccionar una fecha. Para cambiar la hora, seleccione una hora (en intervalos de 15 minutos) en la lista.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Si se incluyen plantillas de seguimiento y sufijos de página de aterrizaje (para redes de anuncios aplicables) en cuentas con plantillas de seguimiento o direcciones URL de destino con códigos de seguimiento incrustados en cuentas con direcciones URL de destino, para todas las palabras clave, anuncios, ubicaciones, vínculos de sitios y [!DNL Google Ads] grupos de productos en la publicación: *[!UICONTROL Yes]* (el valor predeterminado) o *[!UICONTROL No]*. No importa si las unidades de oferta están en una cartera.<br><br>Si selecciona *[!UICONTROL Yes]*, las direcciones URL se generan según los parámetros de la sección [!UICONTROL Tracking Methods] de la configuración de cuenta o de campaña correspondiente. De manera predeterminada, si existen direcciones URL de seguimiento, no se regeneran a menos que se necesiten nuevas direcciones URL (como si el tipo de coincidencia de palabra clave, el texto del anuncio o los parámetros de seguimiento de las cuentas relevantes han cambiado).<br><br>Si selecciona *[!UICONTROL No]*, puede generar direcciones URL de seguimiento más adelante publicando manualmente el archivo cargado.<br><br>**Nota:** Si el anunciante utiliza el seguimiento de conversión de Adobe Advertising y la dirección URL base ha cambiado, debe generar nuevas direcciones URL de seguimiento a menos que la cuenta esté configurada para generar y cargar automáticamente direcciones URL de seguimiento. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Disponible cuando [!UICONTROL Generate Tracking URLs] es *[!UICONTROL Yes]*) Reemplaza cualquier seguimiento de Adobe Advertising existente en las direcciones URL del archivo cargado con un seguimiento recién generado. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite cambios de presupuesto en campañas en portafolios optimizados basados en datos publicados. De forma predeterminada, esta opción no está seleccionada. Si selecciona esta opción, cualquier cambio de presupuesto de campaña especificado se aplicará hasta que la capacidad de optimización determine que el presupuesto se debe reasignar (normalmente en el siguiente ciclo de oferta).<br><br>**Nota:** Cualquier cambio de presupuesto que resulte de los datos publicados para campañas en portafolios no optimizados se producirá cuando se publique el archivo. Los cambios aparecen en las vistas de administración de campañas al día siguiente. |
| [!UICONTROL Enable bidding on ads within portfolios] | Cuando los componentes de campaña incluidos están en un portafolio optimizado, esta función anula la estrategia de optimización y permite cambios de oferta basados en los datos de la hoja de edición masiva hasta una fecha de finalización especificada. Si selecciona esta opción, especifique una fecha de finalización entre 1 y 7 días en el campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [(Nueva IU) Acerca de la administración de datos de campaña mediante hojas de edición por lotes](about.md)
>* [(Nueva interfaz de usuario) Descargar o crear un archivo de hoja de edición por lotes](download.md)
>* [(Nueva IU) Cargar una hoja de edición masiva o archivo de error corregido](upload.md)
>* [(Nueva IU) Validar páginas de aterrizaje en archivos de hojas de edición masiva](validate-landing-pages.md)
>* [(Nueva IU) Eliminar hojas de edición masiva y archivos de error cargados](delete.md)
