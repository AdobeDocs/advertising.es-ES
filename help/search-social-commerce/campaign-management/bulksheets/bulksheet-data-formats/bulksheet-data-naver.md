---
title: Se requieren datos de hojas de edición masiva para  [!DNL Naver] cuentas
description: Haga referencia a los campos de encabezado y los campos de datos requeridos en hojas de edición masiva para  [!DNL Naver] cuentas.
exl-id: 1bfcdbb6-8026-4230-ab6b-b7c79b0d185a
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Apéndice: Datos de hoja de edición masiva requeridos para las cuentas de [!DNL Naver]

Rellene las cuentas de [!DNL Naver] en Search, Social y Commerce generando un archivo de hoja de edición masiva en [!DNL Naver] y luego cargándolo en Search, Social y Commerce.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Campos de datos disponibles

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Campo | Campaign | Grupo de publicidad | Palabra clave | Descripción |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | (Incluida en las hojas de edición masiva generadas con fines informativos) La plataforma de publicidad. Obligatorio a menos que cada fila incluya un ID de AMO para la entidad. |
| [!UICONTROL Acct Name] | Obligatorio/Opcional | Obligatorio/Opcional | Obligatorio/Opcional | El nombre único que identifica una cuenta de red de publicidad. Obligatorio a menos que cada fila incluya un ID de AMO para la entidad. |
| [!UICONTROL Campaign Name] | Requerido | Requerido | Requerido | El nombre único que identifica una campaña para una cuenta. |
| [!UICONTROL Ad Group Name] | n/a | Requerido | Requerido | El nombre único que identifica un grupo de anuncios. |
| [!UICONTROL Keyword] | n/a | n/a | Requerido | Cadena de palabra clave. |
| [!UICONTROL Base URL] | n/a | n/a | Opcional | La dirección URL de la página de aterrizaje a la que se dirigen los usuarios finales cuando hacen clic en su anuncio, incluidos los parámetros de adición configurados para la campaña o cuenta.<br><br>Las direcciones URL base/final en el nivel de palabra clave anulan las direcciones URL en el nivel de anuncio y superiores. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | (Incluido en hojas de edición masiva generadas con fines informativos; no publicado en la red de anuncios). Para cuentas con direcciones URL de destino, este valor es la dirección URL que vincula un anuncio a una dirección URL o página de aterrizaje base en el sitio web del anunciante (a veces a través de otro sitio que rastrea el clic y luego redirige al usuario a la página de aterrizaje). Incluye cualquier parámetro de adición configurado para la campaña o cuenta de Search, Social y Commerce. Si ha generado direcciones URL de seguimiento, este valor se basa en los parámetros de seguimiento de la configuración de la cuenta y la configuración de la campaña. Si ha anexado parámetros específicos de red de anuncios, pueden reemplazarse por los parámetros equivalentes para Search, Social y Commerce.<br><br>Para cuentas con direcciones URL finales, esta columna muestra el mismo valor que [!UICONTROL Base URL/Final URL column]. |
| \[Clasificación de etiquetas específica del anunciante\] | Opcional | Opcional | Opcional | (Nombrado para una clasificación de etiquetas específica del anunciante, como &quot;Color&quot; para una clasificación de etiquetas denominada Color) Un valor para la clasificación especificada que está asociada a la entidad. Solo se puede incluir un valor por clasificación por entidad (como &quot;rojo&quot; para la clasificación de etiquetas &quot;Color&quot; para la Campaña A). La longitud máxima es de 100 caracteres y el valor puede incluir caracteres ASCII y no ASCII.<br><br>Las clasificaciones de etiquetas y sus valores de etiqueta se aplican a todos los componentes secundarios; los nuevos componentes que se agregan posteriormente se asocian automáticamente a la etiqueta. Las clasificaciones de etiquetas para los grupos de productos se aplican al nivel de unidad (más granular).<br><br>El nombre de clasificación y el valor de clasificación no distinguen entre mayúsculas y minúsculas. |
| [!UICONTROL Constraints] | Opcional | Opcional | Opcional | Una restricción asignada a la entidad. Sólo se puede asignar una restricción por entidad.Las entidades secundarias heredan las restricciones <br><br>, por lo que no es necesario introducir valores para entidades secundarias a menos que desee anular los valores heredados. |
| [!UICONTROL Campaign Status] | Opcional: crear o editar<br>Requerido: eliminar | n/a | n/a | El estado de visualización de la campaña: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo campañas existentes). El valor predeterminado para las nuevas campañas es <i>[!UICONTROL Active]</i>. Para eliminar una campaña activa o pausada, ingrese el valor &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | n/a | Opcional: crear o editar<br>Requerido: eliminar | n/a | El estado de visualización del grupo de anuncios: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo grupos de anuncios existentes). El valor predeterminado para los nuevos grupos de anuncios es <i>[!UICONTROL Active]</i>. Para eliminar un grupo de anuncios activo o en pausa, escriba el valor &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | n/a | n/a | Opcional: crear o editar<br>Requerido: eliminar | Estado de visualización de la palabra clave: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo palabras clave existentes). El valor predeterminado para las nuevas palabras clave es <i>[!UICONTROL Active]</i>. Para eliminar una palabra clave activa o pausada, escriba el valor &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Campaign ID] | n/a: Crear<br>Requerido/Opcional: Editar o eliminar | Opcional | Opcional | ID único que identifica una campaña existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia el nombre de la campaña, a menos que la fila incluya un identificador de AMO para la campaña. |
| [!UICONTROL Ad Group ID] | n/a | n/a: Crear<br>Requerido/Opcional: Editar o eliminar | Opcional | ID único que identifica un grupo de anuncios existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando cambia el nombre del grupo de anuncios, a menos que la fila incluya un identificador de AMO para el grupo de anuncios. |
| [!UICONTROL Keyword ID] | n/a | n/a | n/a: Crear<br>Requerido/Opcional: Editar<br>Requerido: Eliminar | Identificador exclusivo que identifica una palabra clave existente. En los archivos CSV y TSV, debe ir precedido de una comilla simple (&#39;).[^1] Necesario solo cuando se cambia el nombre de la palabra clave, a menos que la fila incluya a) suficientes columnas de propiedad para identificar la palabra clave o b) un identificador de AMO. |
| [!UICONTROL AMO ID] | n/a: Crear<br>Opcional: editar o eliminar | n/a: Crear<br>Opcional: editar o eliminar | n/a: Crear<br>Opcional: editar o eliminar | (En hojas de edición masiva generadas) Identificador único generado por [!DNL Adobe] para una entidad sincronizada. Para los anuncios adaptables de búsqueda, el ID de AMO es necesario para editar o eliminar anuncios a menos que incluya [!UICONTROL Ad ID]. Para editar los datos de todos los demás tipos de entidades con un ID de AMO, el ID de AMO es necesario para editar o eliminar los datos a menos que se incluya el ID de entidad y el ID de entidad principal.<br><br>Search, Social y Commerce usan el valor para determinar la identidad correcta que se debe editar, pero no publican el ID en la red de anuncios. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar mensajes de error de Search, Social y Commerce con respecto a los datos de la fila; los mensajes de error se incluyen en [!UICONTROL EF Errors] archivos. Este valor no se publica en la red de anuncios. |
| [!UICONTROL SE Error Message] | n/a | n/a | n/a | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar mensajes de error de la red de publicidad con respecto a los datos de la fila; los mensajes de error se incluyen en [!UICONTROL SE Errors] archivos. Este valor no se publica en la red de anuncios. |

[^1]: Excel convierte los números grandes en notación científica (como 2.12E+09 para 2115585666) cuando abre el archivo. Para ver los dígitos en la notación estándar, seleccione cualquier celda de la columna y haga clic dentro de la barra de fórmulas.

>[!MORELIKETHIS]
>
>* [Apéndice: errores de hojas de edición masiva](../bulksheet-errors.md)
>* [Operaciones que puede realizar en hojas de edición masiva](bulksheet-operations.md)
>* [Formatos de archivo de hojas de edición masiva admitidos](bulksheet-file-formats.md)
>* [Descargar o crear un archivo de hoja de edición masiva](../bulksheet-download.md)
>* [Formatos de rastreo de clics para [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Cargar un archivo de hoja de edición masiva o archivo de error corregido](../bulksheet-upload.md)
>* [Implementar [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
