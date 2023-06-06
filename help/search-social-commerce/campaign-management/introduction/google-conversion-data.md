---
title: "[!DNL Google Ads] datos de conversión"
description: Obtenga información acerca de los tipos de [!DNL Google Ads]Datos de conversión no rastreados disponibles en en Search, Social y Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] datos de conversión en Search, Social y Commerce

Search, Social y Commerce se sincronizan automáticamente [!DNL Google Ads]Los datos de conversión rastreados de para todas sus campañas en la [!DNL Google Ads] redes de búsqueda y compras en Search, Social y Commerce para la creación de informes y optimización. Search, Social y Commerce sincronizan los datos de las conversiones para las que el &quot;[!DNL Include in 'Conversions']&quot; está activada, extrayendo los datos de los últimos 30 días y luego extrayendo cambios a los datos diariamente.

## Datos de conversión disponibles

Hasta tres propiedades de transacción para cada una [[!DNL Google Ads]Conversión con seguimiento automático](https://support.google.com/google-ads/answer/4677036) (que configuró en [!DNL Google Ads]) están disponibles automáticamente en Search, Social y Commerce, con los nombres de conversión configurados en [!DNL Google Ads]. Las propiedades de transacción para cada conversión incluyen:

* `GGL*` — (Al realizar el seguimiento) Suma de los valores de conversión de la palabra clave, comenzando por el prefijo &quot;GGL&quot; (como Compra GGL).

* `GGL_CT*` — el número (recuento) de conversiones, comenzando por el prefijo &quot;GGL_CT&quot; (por ejemplo, GGL_CT_Purchase).

* `GGL_XD_CT*` — (Cuando está disponible para el tipo de conversión, cuando se realiza el seguimiento de las mismas) El número (recuento) de conversiones entre dispositivos, según las medidas por Google XD XD, comenzando por el prefijo &quot;GGL__CT_&quot; (como GGL__CT_Purchase).

Los datos están disponibles a partir de la fecha en que la función se habilitó para la cuenta y se actualizarán a diario antes del 9 de mayo:00-10:00 en la zona horaria del anunciante.

[!DNL Google Ads] registra cada conversión por [unidad de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo y fecha del clic (no fecha de conversión). La atribución se basa en la configuración de atribución predeterminada de cada métrica de [!DNL Google Ads]; la atribución de publicidad de Adobe no se tiene en cuenta porque los datos de nivel de evento de clic no están disponibles. Cada día, Search, Social y Commerce extrae datos de conversión de los 30 días anteriores y, a continuación, calcula cualquier conversión incremental desde el día anterior, utilizando la fecha de clic de [!DNL Google Ads] y designando el día anterior como fecha de transacción. Como resultado, los datos históricos pueden cambiar día a día a medida que se rastrean nuevas conversiones para cada clic. Si compara los datos de Search, Social y Commerce con los de [!DNL Google Ads], use la opción ver o informar para ver &quot;[!UICONTROL Conversions by: Click date]&quot; (no por fecha de transacción).

Todas las métricas están disponibles automáticamente en las vistas de administración de campañas y en los informes básicos, y también están disponibles para su uso en objetivos de portafolio para la optimización.

>[!NOTE]
>
>* Si tiene varias cuentas con los mismos nombres de conversión, es posible que vea nombres de conversión duplicados en la publicidad de Adobe. Si esto sucede, [cambiar el nombre para mostrar](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) para una de las métricas duplicadas en [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Los informes no son precisos cuando dos métricas diferentes tienen el mismo nombre.
>* Los datos en el nivel de unidad de oferta coinciden con los datos en [!DNL Google Ads] en el mismo nivel. Sin embargo, [!DNL Google Ads]Los datos de conversión propios de para niveles superiores pueden incluir conversiones adicionales que no se atribuyen a las unidades de oferta secundarias. Los datos de Search, Social y Commerce siempre se acumulan desde el nivel de unidad de oferta, por lo que, por ejemplo, un informe de nivel de campaña podría no tener los mismos totales que un informe de nivel de campaña en Google Ads.
>* La variación de datos suele ser menor después de la sincronización matinal que más tarde en el día, cuando aún no se han sincronizado conversiones adicionales. Se recomienda validar los datos por la mañana.
>* Los datos de conversión no están disponibles para [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], y [!DNL YouTube] anuncios. Filtrar esos tipos de anuncios al comparar los datos en [!DNL Google Ads] con datos en Search, Social y Commerce.
>* Datos para [!DNL Google Ads] Las conversiones no están disponibles en el nivel de audiencia o de ubicación geográfica y, por lo tanto, no se utilizan para optimizar automáticamente los ajustes de oferta de RLSA y ubicación.


## Cómo comparar los datos de conversión en [!DNL Google Ads] con datos en Search, Social y Commerce

Utilice la siguiente configuración de informe para validar datos comparables.

### Configuración de informes que se utilizará en [!DNL Google Ads]

1. En la barra de herramientas principal, seleccione **[!DNL Reports]>[!DNL Report]**.

1. Seleccionar **[!DNL + Custom]>[!DNL Table]**.

1. En el panel izquierdo, especifique las filas y columnas del informe:

   1. Busque la variable **[!DNL Day]** y arrastra a la pestaña [!DNL Row] sección.

   1. Busque la variable **[!DNL All conv].** y arrastra a la pestaña [!DNL Column] sección.

   1. Busque la variable **[!DNL Conversion action]** y arrastra a la pestaña [!DNL Column] sección.

1. En la barra de herramientas de configuración del informe, seleccione **[!DNL Filter]>[!DNL Ad status]** y, a continuación, seleccione todos los cuadros.

1. En la barra de herramientas de configuración del informe, seleccione **[!DNL Download]>[!DNL Excel .csv]**.

### Configuración de informes que se utilizará en Search, Social y Commerce

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
>* [Acerca de la administración de campañas en Search, Social y Commerce](campaign-management-about.md)
>* [Información general sobre la implementación de cuentas y campañas de red de publicidad](campaign-implemention-overview.md)
>* [Monitorizar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)

