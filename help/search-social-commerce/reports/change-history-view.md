---
title: Ver el informe [!UICONTROL Change History]
description: Obtenga información sobre cómo ver los cambios recientes en la cuenta del anunciante.
exl-id: f8744da7-cc7a-49c1-aeac-1e601768f992
feature: Search Reports
TQID: https://experienceleague.adobe.com/nRlvKpVQf3wbMd83plf3CQp1pPYpHVJzMVJN54lryYM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 84eb5f060a696e057f706c0066c18c9afc1511e1
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 0%

---

# Ver el informe [!UICONTROL Change History]

El informe (nueva interfaz de usuario) [!UICONTROL History Logs] y (IU heredada) [!UICONTROL Change History] incluye un registro de los cambios realizados en la cuenta del anunciante en los últimos 31 días. El informe puede incluir cambios en los siguientes tipos de objetos: usuarios (anunciantes), portafolios, campañas, grupos de anuncios, anuncios, palabras clave, ubicaciones y destinos de productos. Puede ordenar y filtrar los datos por cualquier columna.

Puede descargar información adicional sobre los registros de historial del anunciante en un archivo en formato de libro de [!DNL Microsoft Excel] (archivo XLSX). El informe incluye los valores antiguos y nuevos, así como la hora en que se produjo el cambio.

>[!NOTE]
>
>Para ver los cambios en los portafolios, consulte también el [historial de cambios del portafolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-change-history.md).

## (Nueva IU) Ver el informe [!UICONTROL History Logs] {#history-logs-open}

1. En el menú principal, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL History Logs]**.

1. (Opcional) [Cambiar los datos incluidos en la vista](/help/search-social-commerce/common-tasks/data-views/data-views-about.md).

### Administrar descargas de informes para [!UICONTROL History Logs]

#### Generación de un informe con las filas de datos filtradas

1. [Abrir los registros de historial](#history-logs-open).

1. En la esquina superior derecha, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe").

1. En la configuración de [!UICONTROL Grid Reports], escriba un nombre de informe único y haga clic en **[!UICONTROL Generate]**.

   De forma predeterminada, el nombre del archivo es &quot;allChangeHistory_YYYYMMDD_NNNN&quot;, donde &quot;NNNN&quot; es el número de trabajo secuencial (como &quot;allChangeHistory_20260402_1326).

   El archivo se agrega a la lista [!UICONTROL Recently Generated].

1. (Opcional) Para descargar el archivo una vez que se haya completado, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

#### Descargar un informe completado

1. [Abrir los registros de historial](#history-logs-open).

1. En la esquina superior derecha, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe").

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

#### Eliminar un informe completado

1. [Abrir los registros de historial](#history-logs-open).

1. En la esquina superior derecha, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe").

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar") junto al nombre de archivo.

## (IU heredada) Ver el informe [!UICONTROL Change History]

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Insights & Reports]** > **[!UICONTROL Change History]**.

1. (Opcional) Cambie los datos incluidos en el informe de cualquiera de las siguientes maneras:

   * (Para mostrar u ocultar columnas) Haga clic en ![Flecha abajo](/help/search-social-commerce/assets/arrow-down-expand.png "Flecha abajo") a la derecha de cualquier encabezado de columna, resalte **[!UICONTROL Columns]** y, a continuación, active la casilla de verificación situada junto a cada columna para incluir y desactive la casilla de verificación situada junto a cada columna que desee excluir.

     La configuración de columna se aplica a la vista en todos los anunciantes.

   * (Para filtrar los datos por valor de columna) Realice una de las siguientes acciones:

      * [Aplicar un filtro mediante el vínculo **[!UICONTROL Add Filter]**](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

      * [Aplicar un filtro desde un menú de encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

   * (Para cambiar el intervalo de fechas del informe) Haga lo siguiente:

      1. Sobre la tabla de datos, haga clic en el intervalo de fechas actual.

      1. Especifique el rango:

         * (Para un rango preestablecido): seleccione en la lista de incrementos de tiempo comunes. El valor predeterminado es *[!UICONTROL 2 Days Ago]*.

         * (Para un intervalo específico): seleccione **[!UICONTROL Custom Date Range]** y, a continuación, especifique la fecha inicial y la fecha final.

           Introduzca las fechas en formato MM/DD/AAAA o MM-DD-AAAA, o haga clic en ![Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") junto a cada campo para abrir el calendario y seleccionar una fecha. Solo se pueden incluir datos de los 31 días anteriores.

      1. Haga clic en **[!UICONTROL Apply]**.

1. (Opcional) Descargue una copia del informe:

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Download]**.

      Una vez completado el informe, aparece en el menú [!UICONTROL Download].

   1. (Para abrir o guardar los datos del informe en un archivo) Haga clic en ![Descargar informe como XLS](/help/search-social-commerce/assets/download-spreadsheet2.png "Descargar informe como XLS") junto al nombre del archivo y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador.

      Para obtener más información, consulte la ayuda en línea del explorador.
