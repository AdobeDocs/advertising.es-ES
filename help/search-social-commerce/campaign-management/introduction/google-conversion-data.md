---
title: '[!DNL Google Ads] datos de conversión'
description: Obtenga información acerca de los tipos de datos de conversión rastreados de  [!DNL Google Ads] disponibles en Buscar, Social y Commerce.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# [!DNL Google Ads] datos de conversión en Search, Social y Commerce

Search, Social y Commerce sincronizan automáticamente los datos de conversión rastreados de [!DNL Google Ads] de todas sus campañas en las redes de búsqueda y compras de [!DNL Google Ads] en Search, Social y Commerce para los informes y la optimización.

Todas las métricas están disponibles automáticamente en las vistas de administración de campañas y en los informes básicos, y también están disponibles para su uso en objetivos de portafolio para la optimización.

## Datos de conversión disponibles

Search, Social y Commerce sincronizan los datos de las conversiones para las que la opción &quot;[!DNL Include in 'Conversions']&quot; está habilitada, extraen los datos de los últimos 35 días y extraen los cambios a los datos diariamente a las 09:00-10:00 en el huso horario del anunciante. Los datos históricos pueden cambiar día a día a medida que se realiza el seguimiento de las nuevas conversiones para cada clic.

Hay disponibles automáticamente hasta tres métricas para cada conversión ](https://support.google.com/google-ads/answer/4677036) rastreada por [[!DNL Google Ads] (que configuró en [!DNL Google Ads]) en Buscar, Social y Commerce, con los nombres de conversión configurados en [!DNL Google Ads]. Las métricas de cada conversión incluyen:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (Al realizar el seguimiento) El valor de conversión de la palabra clave, comenzando por el prefijo &quot;GGL&quot; (como GGL Purchase).

* `GGL_CT*`: número (recuento) de conversiones que comienzan por el prefijo &quot;GGL_CT&quot; (como GGL_CT_Purchase).

* `GGL_XD_CT*` — (Cuando está disponible para el tipo de conversión, cuando se realiza el seguimiento de las mismas) El número (recuento) de conversiones entre dispositivos, según las medidas por Google, comenzando con el prefijo &quot;GGL_XD_CT_&quot; (como GGL_XD_CT_Purchase).

[!DNL Google Ads] registra cada conversión por [unidad de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo y fecha de clic (no fecha de conversión). La atribución se basa en la configuración de atribución predeterminada para cada métrica de [!DNL Google Ads]; la atribución de Adobe Advertising no se tiene en cuenta porque no hay datos disponibles en el nivel de evento de clic.

>[!NOTE]
>
>* Si tiene varias cuentas con los mismos nombres de conversión, es posible que vea nombres de conversión duplicados en Adobe Advertising. Si esto sucede, [cambie el nombre para mostrar](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) de una de las métricas duplicadas en [!UICONTROL Admin] > [!UICONTROL Conversions]. Los informes no son precisos cuando dos métricas diferentes tienen el mismo nombre.
>* Los datos en el nivel de unidad de oferta coinciden con los datos en [!DNL Google Ads] en el mismo nivel. Sin embargo, los datos de conversión propios de [!DNL Google Ads] para niveles superiores pueden incluir conversiones adicionales que no se atribuyen a las unidades de oferta secundarias. Los datos de Search, Social y Commerce siempre se acumulan desde el nivel de unidad de oferta, por lo que, por ejemplo, un informe de nivel de campaña podría no tener los mismos totales que un informe de nivel de campaña en Google Ads.
>* La variación de datos suele ser menor después de la sincronización matinal que más tarde en el día, cuando aún no se han sincronizado conversiones adicionales. Se recomienda validar los datos por la mañana.
>* Los datos de conversión no están disponibles para los anuncios de [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App] y [!DNL YouTube]. Filtre esos tipos de anuncios al comparar los datos de [!DNL Google Ads] con los de Search, Social y Commerce.
>* Los datos de las conversiones de [!DNL Google Ads] no están disponibles en el nivel de audiencia o de ubicación geográfica y, por lo tanto, no se usan para optimizar automáticamente los ajustes de RLSA y oferta de ubicación.

## Cómo comparar los datos de conversión de [!DNL Google Ads] con los datos de Search, Social y Commerce

Si compara los datos de Search, Social y Commerce con los de [!DNL Google Ads], use la opción de ver o informar para ver las conversiones según la fecha de clic (no la fecha de transacción).

Utilice la siguiente configuración de informe para validar datos comparables.

### Configuración de informe que se usará en [!DNL Google Ads]

Genere el informe de las acciones de conversión seleccionadas por día e incluya los datos de todos los estados de publicidad.

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### Configuración de informes que se utilizará en Search, Social y Commerce

En Buscar, Social y Commerce, utilice la opción Ver o informar para ver las conversiones en función de la fecha de clic (no la fecha de transacción).

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Create Report]**, mantenga el cursor sobre **[!UICONTROL Basic Reports]** y, a continuación, haga clic en **[!UICONTROL Search Engine Account Report]**.

1. En la ventana [!UICONTROL Report Settings], especifique la siguiente configuración del informe:

   1. En **[!UICONTROL Conversions Based]** de la sección, seleccione **[!UICONTROL Click date]**.

   1. Especifique el mismo intervalo de fechas que utilizó para el informe [!DNL Google Ads].

   1. En la sección **[!UICONTROL Search/Content]**, seleccione **[!UICONTROL Search Only]**.

   1. En la sección **[!UICONTROL Search Engine Hierarchy]**, expanda la sección [!UICONTROL Google Adwords] y seleccione la cuenta.

   1. Abra la ficha [!UICONTROL Columns] y agregue las métricas [!DNL Google Ads] (comenzando por &quot;GGL&quot;) que desee comparar.

1. Haga clic en **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Información general sobre la implementación de cuentas y campañas de red de anuncios](campaign-implemention-overview.md)
>* [Supervisar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)
>* [Ver las métricas de conversión rastreadas de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Crear una etiqueta de conversión para [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
>* [Cargar datos de conversión sin conexión para conversiones mejoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
