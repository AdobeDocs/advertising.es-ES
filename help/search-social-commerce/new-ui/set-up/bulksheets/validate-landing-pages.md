---
title: (Nueva IU) Validar páginas de aterrizaje en archivos de hoja de edición masiva
description: Obtenga información sobre cómo validar las direcciones URL de destino en un archivo de hoja de edición masiva de una sola cuenta en la nueva IU de Search, Social y Commerce.
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
source-git-commit: f22a0f3f1884066faca71c6e8bb760253366b30e
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 0%

---

# (Nueva IU) Validar páginas de aterrizaje en archivos de hoja de edición masiva

*Cuentas con direcciones URL de destino solamente*

Puede validar las páginas de aterrizaje en todas las direcciones URL de destino en un archivo de hoja de edición masiva de una sola cuenta. Puede especificar frases y direcciones URL que indiquen una página no válida y, opcionalmente, notificar redirecciones de páginas de aterrizaje como errores. Las comprobaciones de Search, Social y Commerce para las condiciones especificadas y para las páginas de aterrizaje que faltan (lo que provoca errores HTTP 404 o &quot;No encontrado&quot;).

Cuando encuentra errores, Search, Social y Commerce crean un archivo de error de hoja de edición masiva que incluye todas las filas de la hoja de edición masiva original y mensajes de error para todas las filas con páginas de aterrizaje no válidas. Los errores se registran en la columna [!UICONTROL EF Errors]. La convención de nombres de archivo es `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Más tarde puede descargar el archivo, corregir los errores y cargar el archivo corregido y, a continuación, publicar el archivo corregido en la cuenta de red de publicidad.

>[!NOTE]
>
>* Esta función no valida los valores de la columna Dirección URL base/Dirección URL final.
>* Puede publicar archivos de hojas de edición masiva mientras se validan, o incluso si se encuentran errores.

>[!IMPORTANT]
>
>La compatibilidad con caracteres que no son ASCII en la validación de la página de aterrizaje se ha suspendido temporalmente. Si las direcciones URL de la página de aterrizaje contienen caracteres que no sean ASCII, póngase en contacto con el servicio de asistencia técnica para obtener ayuda.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Seleccione la casilla de verificación situada junto a cada archivo que desee validar.

   >[!NOTE]
   >
   >Solo puede validar hojas de edición masiva de EF de una sola cuenta que no estén actualmente en curso. Si selecciona una hoja de edición masiva de varias cuentas o una hoja de edición masiva que se esté procesando en ese momento, se excluirán esos archivos.

1. En la barra de acciones, haga clic en **[!UICONTROL Validate URLs]**.

1. En el cuadro de diálogo, escriba información en los campos y haga clic en **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]** Texto en el cuerpo de una página de aterrizaje que indica que la página no es válida. Para especificar varios valores, introdúzcalos en líneas independientes.

   **[!UICONTROL Enter invalid landing pages (one per line):]** Las direcciones URL de las páginas que no son válidas como páginas de aterrizaje. Para especificar varios valores, introdúzcalos en líneas independientes.

   **[!UICONTROL User Agent:]** Cómo se identifica el agente de validación de página de aterrizaje en el servidor web en el que reside la página de aterrizaje. El valor predeterminado es `default`, que atribuye las vistas del agente a un usuario [!DNL Mozilla Firefox] anónimo. Si el servidor web bloquea las solicitudes de los usuarios anónimos [!DNL Mozilla Firefox], escriba el nombre de otro agente. Por ejemplo, para [!DNL Googlebot], escriba `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Cuando una página de aterrizaje redirige a otra página (por ejemplo, si falta la página de aterrizaje y el sitio muestra una página de sustitución), la columna [!UICONTROL EF Errors] del archivo de error de la página de aterrizaje indica la dirección URL a la que se redirige la página de aterrizaje.

Cuando comienza la tarea, se agrega una nueva fila a la vista [!UICONTROL Bulksheets]. Cuando las notificaciones por correo electrónico para hojas de edición masiva están [habilitadas en [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md), se enviará una notificación por correo electrónico con un vínculo al archivo cuando se cree el archivo. Según la cantidad de datos recopilados, la notificación por correo electrónico puede tardar varios minutos o más. Puede descargar el archivo para editarlo y luego volver a cargarlo para publicarlo, o puede publicar el archivo tal cual.

>[!NOTE]
>
>* Los archivos grandes tardan más en validarse.
>* Los archivos de hojas de edición masiva para varias campañas pueden contener hasta 500 000 filas de datos. Si genera datos para varias campañas y los datos combinados constan de más de 500 000 filas, los datos se dividirán por campaña en dos o más archivos llamados `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, etc.

>[!MORELIKETHIS]
>
>* [(Nueva IU) Acerca de la administración de datos de campaña mediante hojas de edición por lotes](about.md)
>* [(Nueva IU) Cargar una hoja de edición masiva o archivo de error corregido](upload.md)
>* [(Nueva IU) Publicar hojas de edición masiva o archivos de error corregidos](post.md)
>* [(Nueva IU) Eliminar hojas de edición masiva y archivos de error cargados](delete.md)
>* [(Nueva interfaz de usuario) Detener un trabajo de hoja de edición masiva en curso](stop-job.md)
