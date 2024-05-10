---
title: Administración de datos de campaña mediante hojas de edición masiva
description: Obtenga información acerca de la funcionalidad de hojas de edición masiva disponible por red de anuncios, el flujo de trabajo de hojas de edición masiva y la gestión de errores.
exl-id: 34a16ee3-9eba-4b8b-a5ca-65318f4ee6c5
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Administración de datos de campaña mediante hojas de edición masiva

Una hoja de edición masiva es un archivo que contiene datos de campaña en un formato específico y que se puede utilizar para crear o modificar rápidamente datos de estructura de grupos de anuncios y campañas, y anuncios de texto. Puede generar (descargar) hojas de edición masiva con datos para una o varias cuentas, para campañas y grupos de anuncios específicos o incluso para anuncios de texto, ubicaciones y grupos de productos específicos. Puede utilizar hojas de edición masiva para administrar grandes conjuntos de datos o para realizar pequeños cambios. Cada red publicitaria requiere columnas de información diferentes.

Puede generar hojas de edición masiva con todos los datos que desee, o bien crearlas manualmente y cargarlas (consulte el capítulo sobre &quot;Datos requeridos/incluidos en las hojas de edición masiva&quot;).

Una vez creada una hoja de edición masiva, puede identificar cualquier página de aterrizaje rota que necesite corregirse o datos adicionales para agregar o editar. A continuación, puede editar el archivo y cargarlo en Search, Social y Commerce, y, opcionalmente, programarlo para que se publique en la red de publicidad correspondiente inmediatamente o más tarde. También puede publicar una hoja de edición masiva disponible inmediatamente o más tarde.

Si lo desea, puede cargar archivos de hojas de edición masiva en una cuenta de FTP específica para recuperarlos y publicarlos automáticamente. El directorio se analiza cada hora y los nuevos archivos se publican en la red de búsqueda en el orden en que se reciben.

Todas las hojas de edición masiva, los archivos de error de validación de páginas de aterrizaje y otros archivos de error se eliminan automáticamente 30 días después de crearse, a menos que los elimine anteriormente.

## Funcionalidad por red de anuncios

* **Descargar, cargar y publicar:**  [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], y [!DNL Yandex] cuentas

* **Descargar y cargar solo:** [!DNL Naver] cuentas

  Puede cargar [!DNL Naver] datos para usar en Search, Social y Commerce, pero no pueden publicarlos en la red de anuncios. También puede descargar los datos existentes (sin sincronizar).

* **Descargar solo datos:**  [!DNL Pinterest], [!DNL Yahoo Native], y [!DNL Yahoo! Display Network] cuentas

  Puede descargar los datos existentes (no sincronizados).

## Información general sobre el uso de hojas de edición masiva

Los pasos estándar para utilizar hojas de edición masiva para cuentas sincronizadas son los siguientes:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Descargue datos de una o más cuentas, campañas o grupos de anuncios en un archivo de hoja de edición por lotes](bulksheet-download.md). De forma opcional, puede rellenar manualmente una hoja de edición masiva específica de la red de anuncios y cargar el archivo.

1. [Validación de las páginas de aterrizaje](bulksheet-validate-landing-pages.md) en las direcciones URL base (final) o de destino en el archivo.

1. Cuando necesite añadir datos o realizar correcciones:

   1. [Exportación del archivo](bulksheet-export.md) a su escritorio y edítelo en [!DNL Microsoft Excel].

   1. [Cargar manualmente el archivo editado](bulksheet-upload.md) a Buscar, Social y Commerce, o [cargar el archivo en una cuenta de FTP específica](bulksheet-ftp-account.md) para el registro automático.

1. (Para archivos cargados manualmente) [Publicar el archivo](bulksheet-post.md) a la red de publicidad a medida que la carga o más tarde.

1. (Si es necesario) Descargue los nuevos archivos de error, corrija las filas y vuelva a publicar el archivo.

## Administración de errores al cargar y publicar datos de campaña

Search, Social y Commerce cargan y publican tantas filas de datos como puedan desde una hoja de edición masiva de campañas, incluidas las direcciones URL de seguimiento que generan cuando son necesarias.

Cuando se producen errores durante la operación de la hoja de edición masiva, se genera uno de los dos tipos siguientes de archivos de error:

* **[!UICONTROL EF Errors]:**  Cuando no se puede cargar o procesar un archivo o filas individuales del archivo, se llama a un archivo de error `<uploaded file name>_ef_errors.<extension used for the bulksheet>` se ha creado. Si el problema está en filas individuales, se incluyen esas filas, con una explicación de cada error para que se pueda corregir.

* **[!UICONTROL SE Errors]:**  Cuando se publica un archivo pero la red publicitaria no acepta todos o algunos de los datos, aparece un archivo de error llamado `<uploaded file name>_se_errors.<extension used for the bulksheet>` se ha creado. Cuando se aceptan algunas filas, pero no todas, el archivo de error muestra las filas que no se publicaron y una explicación de cada error para que se pueda corregir. Los mensajes de error se muestran en las tres últimas columnas de cada fila.

>[!NOTE]
>
>Si publica alguna [!DNL Google Ads] anuncios que violan las políticas publicitarias de la red de anuncios, pero que pueden ser elegibles para exenciones, entonces esos anuncios se vuelven a publicar automáticamente con solicitudes de exención. Si la solicitud de exención falla, la información sobre la infracción se incluye en el archivo de error.

Puede descargar cualquier tipo de archivo de error, realizar correcciones directamente en las filas y, a continuación, volver a cargar y publicar el archivo.

Los archivos de error se eliminan automáticamente pasados 30 días, a menos que los elimine anteriormente.

## Información sobre cada archivo

Todos los archivos de datos descargados, los archivos cargados y los archivos de error están disponibles en [!UICONTROL Search] > [!UICONTROL Bulksheets].

La información de cada archivo incluye el estado actual de la tarea y el porcentaje de la tarea que se ha completado, la fecha en que se creó, (cuando corresponda) la fecha en la que se publicó o se publicará en la red de anuncios especificada, la fecha programada de eliminación y el nombre de inicio de sesión del usuario que inició la tarea.

>[!MORELIKETHIS]
>
>* [Descargar/crear un archivo de hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Cargar una hoja de edición masiva o un archivo de error corregido](bulksheet-upload.md)
>* [Publicación de hojas de edición masiva o archivos de error corregidos](bulksheet-post.md)
>* [Exportar un archivo de hoja de edición masiva generado o cargado](bulksheet-export.md)
