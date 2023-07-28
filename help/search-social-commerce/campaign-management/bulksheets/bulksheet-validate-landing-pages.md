---
title: Validación de páginas de aterrizaje en archivos de hoja de edición masiva
description: Obtenga información sobre cómo validar las direcciones URL de destino en un archivo de hoja de edición masiva de una sola cuenta.
exl-id: cf703687-1151-46f6-9540-12a83d41dfc8
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Validación de páginas de aterrizaje en archivos de hoja de edición masiva

*Cuentas solo con direcciones URL de destino*

Puede validar las páginas de aterrizaje en todas las direcciones URL de destino en un archivo de hoja de edición masiva de una sola cuenta. Puede especificar frases y direcciones URL que indiquen una página no válida y, opcionalmente, notificar redirecciones de páginas de aterrizaje como errores. Las comprobaciones de búsqueda, medios sociales y comerciales buscan las condiciones especificadas y las páginas de aterrizaje que faltan (lo que provoca errores HTTP 404 o &quot;No encontrado&quot;).

Cuando encuentra errores, Search, Social y Commerce crea un archivo de error de hoja de edición masiva que incluye todas las filas de la hoja de edición masiva original y mensajes de error para todas las filas con una página de aterrizaje no válida. Los errores se registran en la variable [!UICONTROL EF Errors] columna. La convención de nombres de archivo es `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Más tarde puede descargar el archivo, corregir los errores y cargar el archivo corregido y, a continuación, publicar el archivo corregido en la cuenta de red de publicidad.

>[!NOTE]
>
>* Esta función no valida los valores de la columna Dirección URL base/Dirección URL final.
>* Puede publicar archivos de hojas de edición masiva mientras se validan, o incluso si se encuentran errores.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Seleccione la casilla de verificación situada junto a cada archivo que desee validar.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Validate URLs]**.

1. En el cuadro de diálogo, escriba información en los campos y haga clic en **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Texto en el cuerpo de una página de aterrizaje que indica que la página no es válida. Para especificar varios valores, introdúzcalos en líneas independientes.

   **[!UICONTROL Enter invalid landing pages(one per line):]** Direcciones URL de páginas que no son válidas como páginas de aterrizaje. Para especificar varios valores, introdúzcalos en líneas independientes.

   **[!UICONTROL User Agent:]** Cómo se identifica el agente de validación de página de aterrizaje en el servidor web en el que reside la página de aterrizaje. El valor predeterminado es, que atribuye las vistas del agente a un anónimo [!DNL Mozilla Firefox] usuario. Si el servidor web bloquea las solicitudes del anónimo [!DNL Mozilla Firefox] usuarios y, a continuación, introduzca el nombre de un agente diferente. Por ejemplo, para [!DNL Googlebot], introduzca `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Cuando una página de aterrizaje se redirige a otra página (por ejemplo, si falta la página de aterrizaje y el sitio muestra una página de sustitución), la variable [!UICONTROL ER Errors] en el archivo de error de la página de aterrizaje indica la dirección URL a la que se redirige la página de aterrizaje.

Cuando comienza la tarea, se agrega una nueva fila al [!UICONTROL Bulksheets view]. Cuando se crea el archivo, se envía una notificación por correo electrónico con un vínculo al archivo. Según la cantidad de datos recopilados, la notificación por correo electrónico puede tardar varios minutos o más. Puede descargar el archivo para editarlo y luego volver a cargarlo para publicarlo, o puede publicar el archivo tal cual. Sin embargo, si la generación de archivos falla, aparece un archivo de error en la [!UICONTROL Bulksheet Management] y se envía una notificación por correo electrónico con un vínculo al archivo de error.

>[!NOTE]
>
>* Los archivos grandes tardan más en validarse.
>* Los archivos de hojas de edición masiva para varias campañas pueden contener hasta 500 000 filas de datos. Si genera datos para varias campañas y los datos combinados constan de más de 500 000 filas, los datos se dividen por campaña en dos o más archivos llamados `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, etc.

>[!MORELIKETHIS]
>
>* [Administración de datos de campaña mediante hojas de edición masiva](bulksheet-about.md)
>* [Eliminar hojas de edición masiva y archivos de error cargados](bulksheet-delete.md)
>* [Publicación de hojas de edición masiva o archivos de error corregidos](bulksheet-post.md)
>* [Detener un trabajo de hoja de edición masiva en curso](bulksheet-stop-job.md)
>* [Cargar una hoja de edición masiva o un archivo de error corregido](bulksheet-upload.md)
>* [Exportar un archivo de hoja de edición masiva generado o cargado](bulksheet-export.md)
