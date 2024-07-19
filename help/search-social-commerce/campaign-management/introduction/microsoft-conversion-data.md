---
title: '[!DNL Microsoft Advertising] datos de conversión'
description: Obtenga información acerca de los tipos de datos de conversión rastreados de  [!DNL Microsoft Advertising] disponibles en Search, Social y Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] datos de conversión en Search, Social y Commerce

Search, Social y Commerce sincronizan automáticamente todas las conversiones rastreadas por las etiquetas [[!DNL Microsoft Advertising] UET (seguimiento universal de eventos)](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) para las conversiones de sitios web, incluidas las conversiones de visualización, para la generación de informes y la optimización.

Todas las métricas están disponibles automáticamente en las vistas de administración de campañas y en los informes básicos, y también están disponibles para usarlas en los objetivos del portafolio para la optimización de [!DNL Microsoft Advertising] campañas.

## Datos de conversión disponibles

Search, Social y Commerce sincronizan los datos de las conversiones para las que la opción &quot;[!DNL Include in 'Conversions']&quot; está habilitada, extraen los datos de los últimos 35 días y extraen los cambios a los datos diariamente a las 09:00-10:00 en el huso horario del anunciante. Los datos históricos pueden cambiar día a día a medida que se realiza el seguimiento de las nuevas conversiones para cada clic.

Hay dos métricas disponibles automáticamente para cada conversión ](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) rastreada por [[!DNL Microsoft Advertising] (que configuró en [!DNL Microsoft Advertising]) en Buscar, Social y Commerce, usando los nombres de conversión configurados en [!DNL Microsoft Advertising]. Las métricas de cada conversión incluyen:

* `<conversion-name>`: el valor de conversión de la palabra clave (como Compra).

  >[!TIP]
  >
  >Utilice este tipo de métrica de conversión en el objetivo para portafolios que incluyan [!DNL Microsoft Advertising] campañas con el valor de conversión máximo y las estrategias de oferta de ROAS de destino.

* `CT_<conversion-name>`: número (recuento) de conversiones que comienzan por el prefijo &quot;CT_&quot; (como CT_Purchase).

  >[!TIP]
  >
  >Utilice este tipo de métrica de conversión en el objetivo para portafolios que incluyan [!DNL Microsoft Advertising] campañas con las estrategias de oferta de conversiones máximas y CPA de Target.

Los datos están disponibles en función de la hora del clic y de la conversión/transacción desde la fecha en que la función está habilitada para la cuenta.

[!DNL Microsoft Advertising] registra cada conversión por [unidad de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo y fecha de clic (no fecha de conversión). La atribución se basa en la configuración de atribución predeterminada para cada métrica de [!DNL Microsoft Advertising]; la atribución de Adobe Advertising no se tiene en cuenta porque no hay disponibles datos de nivel de evento de clic.

>[!NOTE]
>
>* Si tiene varias cuentas con los mismos nombres de conversión, es posible que vea nombres de conversión duplicados en el Adobe Advertising. Si esto sucede, [cambie el nombre para mostrar](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) de una de las métricas duplicadas en [!UICONTROL Admin] > [!UICONTROL Conversions]. Los informes no son precisos cuando dos métricas diferentes tienen el mismo nombre.
>* Los datos en el nivel de unidad de oferta coinciden con los datos en la red de publicidad en el mismo nivel. Sin embargo, los datos de conversión propios de la red de anuncios para niveles superiores pueden incluir conversiones adicionales que no se atribuyen a las unidades de oferta secundarias. Los datos de Search, Social y Commerce siempre se acumulan desde el nivel de unidad de oferta, por lo que, por ejemplo, un informe de nivel de campaña podría no tener los mismos totales que un informe de nivel de campaña en la red de publicidad.
>* La variación de datos suele ser menor después de la sincronización matinal que más tarde en el día, cuando aún no se han sincronizado conversiones adicionales. Se recomienda validar los datos por la mañana.
>* Los datos no están disponibles en el nivel de audiencia o de ubicación geográfica y, por lo tanto, no se utilizan para optimizar automáticamente los ajustes de oferta de RLSA y ubicación.

## Cómo comparar los datos de conversión de [!DNL Microsoft Advertising] con los datos de Search, Social y Commerce

Utilice la siguiente configuración de informe para validar datos comparables.

### Configuración de informe que se usará en [!DNL Microsoft Advertising]

Genere el informe de las acciones de conversión seleccionadas por día e incluya los datos de todos los estados de publicidad.

### Configuración de informes que se utilizará en Search, Social y Commerce

En Buscar, Social y Commerce, utilice la opción Ver o informar para ver las conversiones en función de la fecha de clic (no la fecha de transacción).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Create Report]**, mantenga el cursor sobre **[!UICONTROL Basic Reports]** y, a continuación, haga clic en **[!UICONTROL Search Engine Account Report]**.

1. En la ventana [!UICONTROL Report Settings], especifique la siguiente configuración del informe:

   1. En **[!UICONTROL Conversions Based]** de la sección, seleccione **[!UICONTROL Click date]**.

   1. Especifique el mismo intervalo de fechas que utilizó para el informe [!DNL Microsoft Advertising].

   1. En la sección **[!UICONTROL Search/Content]**, seleccione **[!UICONTROL Search Only]**.

   1. En la sección **[!UICONTROL Search Engine Hierarchy]**, expanda la sección [!UICONTROL Microsoft Advertising] y seleccione la cuenta.

   1. Abra la ficha [!UICONTROL Columns] y agregue las métricas [!DNL Microsoft Advertising] que desee comparar.

1. Haga clic en **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Información general sobre la implementación de cuentas y campañas de red de anuncios](campaign-implemention-overview.md)
>* [Supervisar y administrar el rendimiento de las campañas de red de anuncios](monitor-performance-campaigns.md)
>* [Ver las métricas de conversión rastreadas de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
