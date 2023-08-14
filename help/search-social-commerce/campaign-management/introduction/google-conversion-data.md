---
title: '[!DNL Google Ads] datos de conversión'
description: Obtenga información acerca de los tipos de [!DNL Google Ads]Datos de conversión no rastreados disponibles en en Search, Social y Commerce.
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
feature: Search Campaign Management, Conversions
source-git-commit: dc5dc6c5770dd75c77c537c69e53a3b169a71efb
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 0%

---

# [!DNL Google Ads] datos de conversión en Search, Social y Commerce

Search, Social y Commerce se sincronizan automáticamente [!DNL Google Ads]Los datos de conversión rastreados de para todas sus campañas en la [!DNL Google Ads] redes de búsqueda y compras en Search, Social y Commerce para la creación de informes y optimización.

Todas las métricas están disponibles automáticamente en las vistas de administración de campañas y en los informes básicos, y también están disponibles para su uso en objetivos de portafolio para la optimización.

## Datos de conversión disponibles

Search, Social y Commerce sincronizan los datos de las conversiones para las que el &quot;[!DNL Include in 'Conversions']&quot; está activada, extrayendo los datos de los últimos 35 días y luego extrayendo los cambios en los datos diariamente para el 09:00-10:00 en la zona horaria del anunciante. Los datos históricos pueden cambiar día a día a medida que se realiza el seguimiento de las nuevas conversiones para cada clic.

Hasta tres métricas para cada uno [[!DNL Google Ads]Conversión con seguimiento automático](https://support.google.com/google-ads/answer/4677036) (que configuró en [!DNL Google Ads]) están disponibles automáticamente en Search, Social y Commerce, con los nombres de conversión configurados en [!DNL Google Ads]. Las métricas de cada conversión incluyen:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (Al realizar el seguimiento) El valor de conversión de la palabra clave, comenzando por el prefijo &quot;GGL&quot; (como Compra GGL).

* `GGL_CT*` — el número (recuento) de conversiones, comenzando por el prefijo &quot;GGL_CT&quot; (por ejemplo, GGL_CT_Purchase).

* `GGL_XD_CT*` — (Cuando está disponible para el tipo de conversión, cuando se realiza el seguimiento de las mismas) El número (recuento) de conversiones entre dispositivos, según las medidas por Google XD XD, comenzando por el prefijo &quot;GGL__CT_&quot; (como GGL__CT_Purchase).

[!DNL Google Ads] registra cada conversión por [unidad de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo y fecha del clic (no fecha de conversión). La atribución se basa en la configuración de atribución predeterminada de cada métrica de [!DNL Google Ads]; la atribución de Adobe Advertising no se tiene en cuenta porque los datos de nivel de evento de clic no están disponibles.

>[!NOTE]
>
>* Si tiene varias cuentas con los mismos nombres de conversión, es posible que vea nombres de conversión duplicados en el Adobe Advertising. Si esto sucede, [cambiar el nombre para mostrar](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) para una de las métricas duplicadas en [!UICONTROL Admin] > [!UICONTROL Conversions]. Los informes no son precisos cuando dos métricas diferentes tienen el mismo nombre.
>* Los datos en el nivel de unidad de oferta coinciden con los datos en [!DNL Google Ads] en el mismo nivel. Sin embargo, [!DNL Google Ads]Los datos de conversión propios de para niveles superiores pueden incluir conversiones adicionales que no se atribuyen a las unidades de oferta secundarias. Los datos de Search, Social y Commerce siempre se acumulan desde el nivel de unidad de oferta, por lo que, por ejemplo, un informe de nivel de campaña podría no tener los mismos totales que un informe de nivel de campaña en Google Ads.
>* La variación de datos suele ser menor después de la sincronización matinal que más tarde en el día, cuando aún no se han sincronizado conversiones adicionales. Se recomienda validar los datos por la mañana.
>* Los datos de conversión no están disponibles para [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], y [!DNL YouTube] anuncios. Filtrar esos tipos de anuncios al comparar los datos en [!DNL Google Ads] con datos en Search, Social y Commerce.
>* Datos para [!DNL Google Ads] Las conversiones no están disponibles en el nivel de audiencia o de ubicación geográfica y, por lo tanto, no se utilizan para optimizar automáticamente los ajustes de oferta de RLSA y ubicación.

## Cómo comparar los datos de conversión en [!DNL Google Ads] con datos en Search, Social y Commerce

Si compara los datos de Search, Social y Commerce con los de [!DNL Google Ads], utilice la opción ver o informar para ver las conversiones en función de la fecha de clic (no la fecha de transacción).

Utilice la siguiente configuración de informe para validar datos comparables.

### Configuración de informes que se utilizará en [!DNL Google Ads]

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

En Buscar, Social y Comercio, utilice la opción Ver o informar para ver las conversiones en función de la fecha de clic (no la fecha de transacción).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Create Report]**, mantenga el cursor sobre **[!UICONTROL Basic Reports]** y haga clic en **[!UICONTROL Search Engine Account Report]**.

1. En el [!UICONTROL Report Settings] , especifique la siguiente configuración de informe:

   1. En el **[!UICONTROL Conversions Based]** en la sección, seleccione **[!UICONTROL Click date]**.

   1. Especifique el mismo intervalo de fechas que utilizó para [!DNL Google Ads] informe.

   1. En el **[!UICONTROL Search/Content]** , seleccione **[!UICONTROL Search Only]**.

   1. En el **[!UICONTROL Search Engine Hierarchy]** , expanda la [!UICONTROL Google Adwords] y seleccione la cuenta.

   1. Abra el [!UICONTROL Columns] y agregue la pestaña [!DNL Google Ads] métricas (que comienzan con &quot;GGL&quot;) que desee comparar.

1. Haga clic **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Información general sobre la implementación de cuentas y campañas de red de publicidad](campaign-implemention-overview.md)
>* [Monitorizar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)
>* [Ver las métricas de conversión rastreadas de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Cree una etiqueta de conversión para [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
