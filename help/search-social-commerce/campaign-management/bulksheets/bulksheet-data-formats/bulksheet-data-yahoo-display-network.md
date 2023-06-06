---
title: Datos de hoja de edición masiva para [!DNL Yahoo! Display Network] cuentas
description: Hacer referencia a los campos de encabezado y a los campos de datos en las hojas de edición masiva descargadas para [!DNL Yahoo! Display Network] cuentas.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Apéndice: Datos de hojas de edición masiva para [!DNL Yahoo! Display Network] cuentas

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

Puede descargar datos para [!DNL Yahoo! Display Network] cuentas de en bloque, pero no pueden cargar ni publicar hojas de edición en bloque en la red de publicidad.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Campos de datos disponibles

| Campo | Campaign | Grupo de publicidad | Anuncio | Descripción |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | (Incluida en las hojas de edición masiva generadas con fines informativos) La plataforma de publicidad. |
| [!UICONTROL Acct  Name] | Si se incluye | Si se incluye | Si se incluye | El nombre único que identifica una cuenta de red de publicidad. |
| [!UICONTROL Campaign Name] | Si se incluye | Si se incluye | Si se incluye | El nombre único que identifica una campaña para una cuenta. |
| [!UICONTROL Ad Group Name] | n/a | Si se incluye | Si se incluye | El nombre único que identifica un grupo de anuncios. |
| [!UICONTROL Ad Name] | n/a | n/a | Si se incluye | El nombre único que identifica el anuncio dentro de un grupo de anuncios. La longitud máxima es de 50 caracteres. |
| [!UICONTROL Ad Title] | n/a | n/a | Si se incluye | El titular de un anuncio. |
| [!UICONTROL Description Line 1] | n/a | n/a | Si se incluye | La primera línea del cuerpo de un anuncio. |
| [!UICONTROL Description Line 2] | n/a | n/a | Si se incluye | La segunda línea del cuerpo de un anuncio. |
| [!UICONTROL Base URL/Final URL] | n/a | n/a | Si se incluye | La dirección URL de la página de aterrizaje a la que se dirigen los usuarios finales cuando hacen clic en su anuncio, incluidos los parámetros de adición configurados para la campaña o cuenta. Las direcciones URL base/final en el nivel de palabra clave anulan las direcciones URL en el nivel de anuncio y superiores. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | (Incluido en hojas de edición masiva generadas con fines informativos; no publicado en la red de anuncios). Para cuentas con direcciones URL de destino, este valor es la dirección URL que vincula un anuncio a una dirección URL o página de aterrizaje base en el sitio web del anunciante (a veces a través de otro sitio que rastrea el clic y luego redirige al usuario a la página de aterrizaje). Incluye cualquier parámetro de datos anexados configurado para la campaña o cuenta de Search, Social y Commerce. Si ha generado direcciones URL de seguimiento, este valor se basa en los parámetros de seguimiento de la configuración de la cuenta y la configuración de la campaña. Si ha anexado parámetros específicos de red de anuncios, se pueden reemplazar por los parámetros equivalentes para Buscar, Social y Comercio. |
| \[Clasificación de etiquetas específica del anunciante\] | Si se incluye | Si se incluye | Si se incluye | (Nombrado para una clasificación de etiquetas específica del anunciante, como &quot;Color&quot; para una clasificación de etiquetas denominada Color) Un valor para la clasificación especificada que está asociada a la entidad. |
| [!UICONTROL Constraints] | Si se incluye | Si se incluye | n/a | Una restricción asignada a la entidad. |
| [!UICONTROL Campaign Status] | Si se incluye | n/a | n/a | El estado de visualización de la campaña: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, o <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | n/a | Si se incluye | n/a | El estado de visualización del grupo de anuncios: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, o <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | n/a | n/a | Si se incluye | El estado de visualización de la palabra clave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, o <i>[!UICONTROL Deleted]</i> (solo palabras clave existentes). |
| [!UICONTROL Campaign ID] | Si se incluye | Si se incluye | Si se incluye | ID único que identifica una campaña existente. |
| [!UICONTROL Ad Group ID] | n/a | Si se incluye | Si se incluye | ID único que identifica un grupo de anuncios existente. |
| [!UICONTROL Keyword ID] | n/a | n/a | Si se incluye | Identificador exclusivo que identifica una palabra clave existente. |
| [!UICONTROL AMO ID] | n/a | n/a | n/a | (En hojas de edición masiva generadas) Identificador único generado por el Adobe para una entidad sincronizada. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | (Incluido en hojas de edición masiva generadas con fines informativos) Marcador de posición para mostrar mensajes de error de Search, Social y Commerce con respecto a los datos de la fila; los mensajes de error se incluyen en los archivos de errores de EF. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Descargar/crear un archivo de hoja de edición masiva](../bulksheet-download.md)

