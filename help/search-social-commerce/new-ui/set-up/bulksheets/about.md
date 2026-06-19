---
title: (Nueva IU) Acerca de la administración de datos de campaña mediante hojas de edición por lotes
description: Obtenga información acerca de la funcionalidad de hojas de edición masiva disponible por red de anuncios, el flujo de trabajo de hojas de edición masiva y la administración de errores en la nueva IU de Search, Social y Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 772
ht-degree: 0%

---

# (Nueva IU) Acerca de la administración de datos de campaña mediante hojas de edición por lotes

Una hoja de edición masiva es un archivo que contiene datos de campaña en un formato específico y que se puede utilizar para crear o modificar rápidamente datos de estructura de grupos de anuncios y campañas, y anuncios de texto. Puede generar (descargar) hojas de edición masiva con datos para una o varias cuentas, para campañas y grupos de anuncios específicos o incluso para anuncios de texto, ubicaciones y grupos de productos específicos. Puede utilizar hojas de edición masiva para administrar grandes conjuntos de datos o para realizar pequeños cambios. Cada red publicitaria requiere columnas de información diferentes.

Puede generar hojas de edición masiva con todos los datos que desee, o bien crearlas manualmente y cargarlas. Consulte &quot;[Datos requeridos e incluidos en hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-file-formats.md)&quot; para conocer los requisitos de formato de archivo y &quot;[Operaciones que puede realizar en hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md)&quot; para ver las operaciones admitidas por la red publicitaria.

Una vez creada una hoja de edición masiva, puede identificar cualquier página de aterrizaje rota que necesite corregirse o datos adicionales para agregar o editar. A continuación, puede editar el archivo y cargarlo en Search, Social y Commerce, y, opcionalmente, programarlo para que se publique en la red de publicidad correspondiente inmediatamente o más tarde. También puede publicar una hoja de edición masiva disponible inmediatamente o más tarde.

Todas las hojas de edición masiva, los archivos de error de validación de páginas de aterrizaje y otros archivos de error se eliminan automáticamente 30 días después de crearse, a menos que los elimine anteriormente.

## Funcionalidad por red de anuncios {#bulksheet-functionality-by-network}

* **Descargar, cargar y publicar:** cuentas de [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] y [!DNL Yandex]

* **Descargar y cargar solamente:** [!DNL Naver] cuentas

  Puede cargar [!DNL Naver] datos para usarlos en Search, Social y Commerce, pero no puede publicarlos en la red de anuncios. También puede descargar los datos existentes (sin sincronizar).

* **Descargar solo datos:** [!DNL Pinterest], [!DNL Yahoo DSP], [!DNL Yahoo Native] cuentas

  Puede descargar los datos existentes (no sincronizados).

## Información general sobre el uso de hojas de edición masiva

Los pasos estándar para utilizar hojas de edición masiva con cuentas sincronizadas son los siguientes:

1. [Descargue datos de una o más cuentas, campañas o grupos de anuncios en un archivo de hoja de edición por lotes](download.md). De forma opcional, puede rellenar manualmente una hoja de edición masiva específica de la red de anuncios y cargar el archivo.

1. [Valide las páginas de aterrizaje](validate-landing-pages.md) en las direcciones URL base (final) o en las direcciones URL de destino del archivo.

1. Cuando necesite añadir datos o realizar correcciones:

   1. Exporte el archivo a su escritorio y edítelo en [!DNL Microsoft Excel].

   1. [Cargue manualmente el archivo editado](upload.md) en Search, Social y Commerce.

1. (Para archivos cargados manualmente) [Publique el archivo](post.md) en la red de publicidad a medida que lo cargue o más tarde.

1. (Si es necesario) Descargue los nuevos archivos de error, corrija las filas y vuelva a publicar el archivo.

## Administración de errores al cargar y publicar datos de campaña

Search, Social y Commerce cargan y publican tantas filas de datos como puedan desde una hoja de edición masiva de campañas, incluidas las direcciones URL de seguimiento que generan cuando son necesarias.

Cuando se producen errores durante una operación de hoja de edición masiva, se genera uno de los dos tipos siguientes de archivos de error:

* **[!UICONTROL EF Errors]:** Cuando no se puede cargar o procesar un archivo o filas individuales del archivo, se crea un archivo de error denominado `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Si el problema está en filas individuales, se incluyen esas filas, con una explicación de cada error para que se pueda corregir.

* **[!UICONTROL SE Errors]:** Cuando se publica un archivo pero la red publicitaria no acepta todos o algunos de los datos, se crea un archivo de error denominado `<uploaded file name>_se_errors.<extension used for the bulksheet>`. Cuando se aceptan algunas filas, pero no todas, el archivo de error muestra las filas que no se publicaron y una explicación de cada error para que se pueda corregir. Los mensajes de error se muestran en las tres últimas columnas de cada fila.

>[!NOTE]
>
>Si publica anuncios de [!DNL Google Ads] que violen las políticas de publicidad de la red de anuncios, pero que puedan ser elegibles para exenciones, esos anuncios se vuelven a publicar automáticamente con solicitudes de exención. Si la solicitud de exención falla, la información sobre la infracción se incluye en el archivo de error.

Puede descargar cualquier tipo de archivo de error, realizar correcciones directamente en las filas y, a continuación, volver a cargar y publicar el archivo.

Los archivos de error se eliminan automáticamente pasados 30 días, a menos que los elimine anteriormente.

## Información sobre cada archivo

Todos los archivos de datos, archivos cargados y archivos de error descargados están disponibles en [!UICONTROL Setup] \> [!UICONTROL Bulksheets].

La información de cada archivo incluye el estado actual de la tarea y el porcentaje de la tarea que se ha completado, la fecha en que se creó, (cuando corresponda) la fecha en la que se publicó o se publicará en la red de anuncios especificada, la fecha programada de eliminación y el nombre de inicio de sesión del usuario que inició la tarea.

>[!MORELIKETHIS]
>
>* [(Nueva interfaz de usuario) Descargar o crear un archivo de hoja de edición por lotes](download.md)
>* [(Nueva IU) Cargar una hoja de edición masiva o archivo de error corregido](upload.md)
>* [(Nueva IU) Publicar hojas de edición masiva o archivos de error corregidos](post.md)
>* [(Nueva IU) Validar páginas de aterrizaje en archivos de hojas de edición masiva](validate-landing-pages.md)
>* [(Nueva IU) Eliminar hojas de edición masiva y archivos de error cargados](delete.md)
>* [(Nueva interfaz de usuario) Detener un trabajo de hoja de edición masiva en curso](stop-job.md)
