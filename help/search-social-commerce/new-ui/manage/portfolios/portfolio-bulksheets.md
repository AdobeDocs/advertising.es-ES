---
title: Edición masiva de la configuración de portafolios mediante archivos de hojas de edición masiva
description: Obtenga información sobre cómo editar la configuración de varios portafolios mediante un archivo de hoja de edición por lotes.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: 04b6fbaf4a8b360bc3a60bdad4871694d50f1bf9
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Edición masiva de la configuración de portafolios mediante archivos de hojas de edición masiva

*característica de Beta*

Una hoja de edición masiva de portafolios es un archivo que contiene la configuración de portafolios en un formato específico y que se puede utilizar para revisar y modificar rápidamente la configuración. Puede generar (descargar) hojas de edición masiva con la configuración de uno o más portafolios. El archivo se descarga como un libro de [!DNL Excel] con dos hojas de cálculo (formato XLSX). El libro incluye:

* Una hoja de cálculo [!UICONTROL Instructions] de sólo lectura con información sobre cómo editar los campos.

* Una ficha [!UICONTROL Portfolio Settings Edit], con una fila por portafolio incluido. Si lo desea, puede editar los campos según sea necesario, guardar el archivo localmente y posteriormente [cargar el archivo editado](#portfolio-bulksheet-upload) en Search, Social y Commerce. Los campos editables se resaltan en color.

## Descargar un archivo de hoja de edición masiva con la configuración del portafolio

1. (Opcional) Seleccione la casilla de verificación situada junto a cada portafolio para incluirlo en la hoja de edición masiva.

   Si no selecciona portafolios específicos, puede descargar la configuración de todos los portafolios.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en:

   * (Para todos los portafolios) **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export All Portfolios]**.

   * (Para portafolios seleccionados) **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**.

1. Escriba el nombre del archivo de hoja de edición masiva que desea crear y haga clic en **[!UICONTROL Export Now]**.

   El archivo se guarda en la carpeta de descargas predeterminada del explorador.

## Cargar un archivo de hoja de edición masiva con la configuración actualizada del portafolio {#portfolio-bulksheet-upload}

El archivo debe tener el formato XLSX.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**. &lt;!— Debería ser &quot;Importar configuración de Portfolio&quot; — &quot;Detalles&quot; puede ser demasiado vago y sugerir que puede incluir otra cosa. —>

1. En el cuadro de diálogo [!UICONTROL Import Portfolio Details File]:<!-- reword if we change the name of the operation -->

   1. Arrastre y suelte un archivo en el cuadro o haga clic en **[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? -->para seleccionar un archivo de su dispositivo o red.

   1. Haga clic en **[!UICONTROL Import]**.

Puede comprobar el estado de la carga desde el botón [!UICONTROL Global Sync Status] (![Estado de sincronización global](/help/search-social-commerce/assets/global-sync-status.png "Estado de sincronización global")) situado junto al selector de intervalo de fechas.<!-- icon similar to Refresh -->. Si alguno de los cambios no se realizó correctamente, puede descargar un archivo de error que muestre los errores.

Las notificaciones también se agregan al Centro de notificaciones y puede abrir el panel Notificaciones desde el icono ![Notificaciones](/help/search-social-commerce/assets/notifications-new.png "Notificaciones") situado junto al botón [!UICONTROL Global Sync Status] (![Estado de sincronización global](/help/search-social-commerce/assets/global-sync-status.png "Estado de sincronización global")).

## Requisitos de datos para archivos de hojas de edición masiva cargados

Todos los archivos de hojas de edición masiva deben incluir la columna [!UICONTROL Portfolio ID], y cada fila de datos debe incluir un valor para que [!UICONTROL Portfolio ID] pueda ser procesado. Para obtener más información acerca de los requisitos de datos, consulte la ficha [!UICONTROL Instructions] en el archivo de hoja de edición masiva descargado.

Para obtener explicaciones sobre las columnas de configuración del portafolio en la ficha [!UICONTROL Portfolio Settings Edit], consulte la Guía de optimización, que está disponible en Buscar, Social y Commerce.

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [(nueva interfaz de usuario) Editar un portafolio](portfolio-edit.md)
>* [Crear un portafolio](portfolio-create.md)
>* [(Nueva interfaz de usuario) Acerca de los portafolios](portfolio-about.md)
