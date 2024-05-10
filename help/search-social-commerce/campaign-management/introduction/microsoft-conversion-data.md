---
title: '[!DNL Microsoft Advertising] datos de conversión'
description: Obtenga información acerca de los tipos de [!DNL Microsoft Advertising]Los datos de conversión rastreados de están disponibles en Search, Social y Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] datos de conversión en Search, Social y Commerce

Search, Social y Commerce sincronizan automáticamente todas las conversiones rastreadas por su [[!DNL Microsoft Advertising] etiquetas de seguimiento universal de eventos (UET)](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) para conversiones de sitios web, incluidas las conversiones de visualizaciones, para creación de informes y optimización.

Todas las métricas están disponibles automáticamente en las vistas de administración de campañas y en los informes básicos, y también están disponibles para su uso en objetivos de portafolio para la optimización de [!DNL Microsoft Advertising] campañas.

## Datos de conversión disponibles

Search, Social y Commerce sincronizan los datos de las conversiones para las que el &quot;[!DNL Include in 'Conversions']&quot; está activada, extrayendo los datos de los últimos 35 días y luego extrayendo los cambios en los datos diariamente para el 09:00-10:00 en la zona horaria del anunciante. Los datos históricos pueden cambiar día a día a medida que se realiza el seguimiento de las nuevas conversiones para cada clic.

Dos métricas para cada uno [[!DNL Microsoft Advertising]Conversión con seguimiento automático](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (que configuró en [!DNL Microsoft Advertising]) están disponibles automáticamente en Buscar, Social y Commerce, con los nombres de conversión configurados en [!DNL Microsoft Advertising]. Las métricas de cada conversión incluyen:

* `<conversion-name>` — El valor de conversión de la palabra clave (por ejemplo, Compra).

  >[!TIP]
  >
  >Utilice este tipo de métrica de conversión en el objetivo para portafolios que incluyen [!DNL Microsoft Advertising] campañas con el valor de conversión máximo y estrategias de oferta de ROAS de Target.

* `CT_<conversion-name>` — El número (recuento) de conversiones, comenzando por el prefijo &quot;CT_&quot; (como CT_Purchase).

  >[!TIP]
  >
  >Utilice este tipo de métrica de conversión en el objetivo para portafolios que incluyen [!DNL Microsoft Advertising] campañas con las conversiones máximas y las estrategias de oferta de CPA de Target.

Los datos están disponibles en función de la hora del clic y de la conversión/transacción desde la fecha en que la función está habilitada para la cuenta.

[!DNL Microsoft Advertising] registra cada conversión por [unidad de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo y fecha del clic (no fecha de conversión). La atribución se basa en la configuración de atribución predeterminada de cada métrica de [!DNL Microsoft Advertising]; la atribución de Adobe Advertising no se tiene en cuenta porque los datos de nivel de evento de clic no están disponibles.

>[!NOTE]
>
>* Si tiene varias cuentas con los mismos nombres de conversión, es posible que vea nombres de conversión duplicados en el Adobe Advertising. Si esto sucede, [cambiar el nombre para mostrar](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) para una de las métricas duplicadas en [!UICONTROL Admin] > [!UICONTROL Conversions]. Los informes no son precisos cuando dos métricas diferentes tienen el mismo nombre.
>* Los datos en el nivel de unidad de oferta coinciden con los datos en la red de publicidad en el mismo nivel. Sin embargo, los datos de conversión propios de la red de anuncios para niveles superiores pueden incluir conversiones adicionales que no se atribuyen a las unidades de oferta secundarias. Los datos de Search, Social y Commerce siempre se acumulan desde el nivel de unidad de oferta, por lo que, por ejemplo, un informe de nivel de campaña podría no tener los mismos totales que un informe de nivel de campaña en la red de publicidad.
>* La variación de datos suele ser menor después de la sincronización matinal que más tarde en el día, cuando aún no se han sincronizado conversiones adicionales. Se recomienda validar los datos por la mañana.
>* Los datos no están disponibles en el nivel de audiencia o de ubicación geográfica y, por lo tanto, no se utilizan para optimizar automáticamente los ajustes de oferta de RLSA y ubicación.

## Cómo comparar los datos de conversión en [!DNL Microsoft Advertising] con datos en Search, Social y Commerce

Utilice la siguiente configuración de informe para validar datos comparables.

### Configuración de informes que se utilizará en [!DNL Microsoft Advertising]

Genere el informe de las acciones de conversión seleccionadas por día e incluya los datos de todos los estados de publicidad.

### Configuración de informes que se utilizará en Search, Social y Commerce

En Buscar, Social y Comercio, utilice la opción Ver o informar para ver las conversiones en función de la fecha de clic (no la fecha de transacción).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Create Report]**, mantenga el cursor sobre **[!UICONTROL Basic Reports]** y haga clic en **[!UICONTROL Search Engine Account Report]**.

1. En el [!UICONTROL Report Settings] , especifique la siguiente configuración de informe:

   1. En el **[!UICONTROL Conversions Based]** en la sección, seleccione **[!UICONTROL Click date]**.

   1. Especifique el mismo intervalo de fechas que utilizó para [!DNL Microsoft Advertising] informe.

   1. En el **[!UICONTROL Search/Content]** , seleccione **[!UICONTROL Search Only]**.

   1. En el **[!UICONTROL Search Engine Hierarchy]** , expanda la [!UICONTROL Microsoft Advertising] y seleccione la cuenta.

   1. Abra el [!UICONTROL Columns] y agregue la pestaña [!DNL Microsoft Advertising] métricas que desee comparar.

1. Clic **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Información general sobre la implementación de cuentas y campañas de red de publicidad](campaign-implemention-overview.md)
>* [Monitorizar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)
>* [Ver las métricas de conversión rastreadas de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
