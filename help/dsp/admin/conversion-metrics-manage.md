---
title: Administre las métricas de conversión de un anunciante en DSP.
description: Aprenda a utilizar las métricas de conversión que Adobe Advertising rastrea para un anunciante de DSP.
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Administrar las métricas de conversión de un anunciante

Las métricas de conversión de un anunciante se utilizan en toda la publicidad de Adobe:

* En Advertising DSP, puede incluir métricas de conversión en las vistas de administración de campañas, los objetivos personalizados y los informes personalizados. También puede usar las métricas de conversión de un anunciante para crear [objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md), que se usan para optimizar paquetes.

* (Anunciantes con Advertising Search, Social y Commerce) En Search, Social y Commerce, los datos de las métricas de conversión se pueden mostrar en columnas en las vistas de administración de campañas, portafolios y objetivos, y en los informes. Los usuarios con privilegios de acceso suficientes también pueden utilizar métricas de conversión para crear objetivos, que se utilizan para optimizar los portafolios.

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

Los tipos de métricas rastreadas para usuarios de DSP incluyen:

* Métricas de conversión que Adobe Advertising rastrea para un anunciante.

* [Métricas de conversión y participación del sitio sincronizadas desde Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Eventos del sitio sincronizados desde Customer Journey Analytics de Adobe](/help/integrations/customer-journey-analytics/overview.md).

* Conversiones de fuentes personalizadas.

De la lista de métricas de conversión disponibles, cada usuario con acceso a los datos del anunciante puede personalizar las métricas que ve disponibles para las vistas de administración y los informes, incluidas u omitiendo las métricas específicas que elija. Puede utilizar un nombre de métrica exactamente como se escribe en los datos recuperados o cambiar el nombre que se muestra en los encabezados de columna para facilitar la lectura.

>[!IMPORTANT]
>
>De forma predeterminada, ninguna de las métricas de conversión de un anunciante está disponible para su inclusión en las vistas de administración de campañas, los objetivos personalizados y los informes personalizados. Para que una métrica de conversión esté disponible, debe habilitarla explícitamente.

>[!TIP]
>
>Una vez que el anunciante (o la red publicitaria) deje de recopilar una métrica de conversión, [ocúltela de las vistas de administración y de los informes](#conversion-metrics-change-available) a menos que desee usarla para ver datos históricos.

## Ver las métricas de conversión rastreadas de un anunciante

* En el menú principal, haga clic en **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

Se muestran todas las métricas de conversión recopiladas para el anunciante y los diferentes nombres para mostrar asignados a él. Cada fila de métrica incluye el origen de la métrica.

## Cambiar el nombre para mostrar de una métrica de conversión

Por ejemplo, si recopila datos de registro mediante una métrica de conversión denominada *reg*, puede cambiar el nombre para mostrar para que se muestre como &quot;Registros&quot;.

No puede eliminar un nombre para mostrar existente.

1. En el menú principal, haga clic en **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

1. Mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Edit Display Name]**.

1. Escriba el nombre que se debe mostrar y haga clic en **[!UICONTROL Save]**.

   Los nombres para mostrar deben ser únicos y no pueden incluir los siguientes caracteres especiales: `\"<'>&`

## Cambiar las métricas de conversión disponibles en las vistas de administración de campañas, los objetivos personalizados y los informes personalizados {#change-the-conversion-metrics-available-in-ui}

1. En el menú principal, haga clic en **[!UICONTROL Settings]>[!UICONTROL Conversions]**.

   Se muestran todas las métricas de conversión que se han recopilado para el anunciante y todos los nombres diferentes que se han especificado para mostrarlos.

1. (Opcional) Filtre la lista:

   1. Sobre la lista, haz clic en ![Filtro](/help/dsp/assets/filter.png "Filtro").

   1. Especifique los filtros y haga clic en **[!DNL Apply]**.

      Puede filtrar las métricas por el ID del cliente de AMO, por si las métricas son visibles u ocultas en la interfaz de usuario y por fuente de datos.

1. Cambie las métricas de conversión disponibles para las vistas de administración y los informes:

   * Para mostrar una métrica, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Show in UI and Reports]**.

   * Para ocultar una métrica, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Hide in UI and Reports]**.

>[!MORELIKETHIS]
>
>* [Administrar las vistas de datos de tu campaña](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Administrar objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md)
