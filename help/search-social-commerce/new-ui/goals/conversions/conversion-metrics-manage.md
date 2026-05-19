---
title: Administrar las métricas de conversión de un anunciante
description: Aprenda a utilizar las métricas de conversión que Adobe Advertising rastrea para un anunciante.
feature: Conversions
source-git-commit: 3272a0d3e5766a22c2ff761b84f1774cafe153bd
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 0%

---

# (Nueva IU) Administrar y ver datos de rendimiento de las métricas de conversión de un anunciante

*característica de Beta*

Las métricas [conversion](/help/search-social-commerce/glossary.md#c-d) de un anunciante se utilizan en todo Adobe Advertising:

* En Search, Social y Commerce, los datos de las métricas de conversión se pueden mostrar en columnas en las vistas de administración de campañas, portafolios y objetivos, y en los informes. Los usuarios con privilegios de acceso suficientes también pueden utilizar métricas de conversión para crear objetivos, que se utilizan para optimizar los portafolios.

* (Anunciantes con Advertising DSP) En DSP, puede incluir métricas de conversión en las vistas de administración de campañas, los objetivos personalizados y los informes personalizados. También puede usar métricas de conversión para crear [objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md), que se usan para optimizar paquetes.

Las métricas disponibles incluyen:

* Métricas de conversión que Adobe Advertising rastrea para un anunciante.

* [Métricas de conversión y participación del sitio sincronizadas desde Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Eventos del sitio sincronizados desde Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Conversiones seguidas por [!DNL Google Ads] y conversiones seguidas por [!DNL Microsoft Advertising] etiquetas de seguimiento de eventos universales.

* (Cuando [ha configurado una combinación específica de cuenta, propiedad y vista de  [!DNL Google Analytics] como fuente de datos](/help/search-social-commerce/admin/data-sources/data-source-about.md) para las conversiones de búsqueda, medios sociales y Commerce), rastreada por [!DNL Google Analytics].

* Conversiones de fuentes personalizadas.

De la lista de métricas de conversión disponibles, cada usuario con acceso a los datos del anunciante puede personalizar las métricas que ve disponibles para las vistas de administración y los informes, incluidas u omitiendo las métricas específicas que elija. Puede utilizar un nombre de métrica exactamente como se escribe en los datos recuperados o cambiar el nombre que se muestra en los encabezados de columna para facilitar la lectura.

>[!IMPORTANT]
>
>De manera predeterminada, ninguna de las métricas de conversión de un anunciante (excepto las conversiones rastreadas por las etiquetas de seguimiento de eventos universales [!DNL Google Ads], [!DNL Google Analytics] y [!DNL Microsoft Advertising]) está disponible para su inclusión en las vistas, los objetivos y los informes de administración de portafolios y campañas. Para que una métrica de conversión esté disponible, debe habilitarla explícitamente.
>
>Las nuevas conversiones rastreadas por las etiquetas de seguimiento de eventos universales [!DNL Google Ads], [!DNL Google Analytics] y [!DNL Microsoft Advertising] siempre están disponibles automáticamente.

>[!TIP]
>
>Una vez que el anunciante (o la red publicitaria) deje de recopilar una métrica de conversión, [ocúltela de las vistas de administración y de los informes](#conversion-metrics-change-available) a menos que desee usarla para ver datos históricos.

## Ver las métricas de conversión rastreadas de un anunciante

* En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

Se muestran todas las métricas de conversión recopiladas para el anunciante y los diferentes nombres para mostrar asignados a él. Cada fila de métrica incluye el origen de la métrica.

## Cambiar el nombre para mostrar de una métrica de conversión

Por ejemplo, si recopila datos de registro mediante una métrica de conversión denominada *reg*, puede cambiar el nombre para mostrar para que se muestre como &quot;Registros&quot;.

No puede eliminar un nombre para mostrar existente.

>[!NOTE]
>
>Para [métricas de [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md), cualquier cambio manual en el nombre para mostrar se sobrescribirá si actualiza o vuelve a autenticar la integración. Del mismo modo, se omitirán los cambios de nombre dentro de [!DNL Google Analytics] a menos que [actualice](/help/search-social-commerce/admin/data-sources/data-source-edit.md) o [vuelva a autenticar](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md) la integración.

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Filtrar la lista [de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o de un [encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. En la columna **[!UICONTROL Conversion Display Name]** de la métrica, mantenga el cursor sobre el nombre de la métrica y haga clic en **...** > **[!UICONTROL Rename]**.

1. Escriba el nombre que se debe mostrar y haga clic en **[!UICONTROL Apply]**.

   Los nombres para mostrar deben ser únicos y no pueden incluir los siguientes caracteres especiales: `\"<'>&`

## Cambiar las métricas de conversión disponibles en vistas de administración, objetivos e informes {#conversion-metrics-change-available}

>[!NOTE]
>
>Si oculta una métrica de conversión que antes estaba disponible, se elimina de cualquier métrica derivada que contenga la métrica de conversión.

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

   Se muestran todas las métricas de conversión que se han recopilado para el anunciante y todos los nombres diferentes que se han especificado para mostrarlos.

1. (Opcional) Filtre la lista [de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o de un [encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Cambie las métricas de conversión disponibles para las vistas de administración y los informes:

   * Para mostrar u ocultar una única métrica, haga clic en el modificador de la columna **[!UICONTROL Visibility]** para cambiar la configuración.

   * Para mostrar u ocultar varias métricas, haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada métrica de conversión.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. En la barra de herramientas de acciones masivas, haga clic en ![Visibilidad](/help/search-social-commerce/assets/visible.png "Visibilidad") para mostrar las métricas o en ![Visibilidad desactivada](/help/search-social-commerce/assets/visibility-off.png "Visibilidad desactivada") para ocultarlas.

      1. (Para ocultar las métricas) En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]** para ocultar las métricas y eliminarlas de cualquier métrica derivada que las contenga.

## Administrar informes de datos de rendimiento para conversiones

Puede descargar la siguiente información sobre las conversiones rastreadas: el nombre de la métrica sincronizada, el nombre para mostrar de la métrica en las vistas de administración e informes de Search, Social y Commerce, si la métrica está visible en las vistas de administración y los informes, el ID de conversión y el origen de la métrica. Descargue los datos a un archivo en formato de libro [!DNL Microsoft Excel] (archivo XLSX).

### Generación de un informe con las filas de datos filtradas

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Especifique las conversiones cuyos datos desee descargar:

   * Para descargar datos de filas específicas, active las casillas de verificación situadas junto a las filas.

   * Para descargar los datos de todas las filas, no es necesario activar ninguna casilla de verificación. Todas las filas se incluyen de forma predeterminada.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la configuración de [!UICONTROL Grid Reports], escriba un nombre de informe único y haga clic en **[!UICONTROL Generate]**.

   De forma predeterminada, el nombre del archivo es &quot;conversionsReport_YYYYMMDD_NNNN&quot;, donde &quot;NNNN&quot; es el número de trabajo secuencial (como &quot;conversionsReport_20260402_1326).

   El archivo se agrega a la lista [!UICONTROL Recently Generated].

1. (Opcional) Para descargar el archivo una vez que se haya completado, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Descargar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Eliminar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") **[!UICONTROL Reports]**.

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar") junto al nombre de archivo.

<!--
>[!MORELIKETHIS]
>
>* 
-->
