---
title: Acerca de Insights
description: Obtenga información acerca de las perspectivas de rendimiento con visualizaciones.
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
source-git-commit: 0f022babeab6c044949760cedc103323eb0cc950
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Acerca de Insights

*característica de Beta*

Las perspectivas de rendimiento de alto nivel con visualizaciones le proporcionan la información que necesita para optimizar de forma eficaz sus campañas y descubrir nuevas oportunidades para escalar el rendimiento. Puede ver los datos de las campañas de un anunciante específico o explorar en profundidad un nivel inferior.

Utilice perspectivas de rendimiento para:

* Realizar un seguimiento de las tendencias a largo plazo para la planificación estratégica y la toma de decisiones informadas.

* Identificar oportunidades para lograr mejores resultados.

* Mejore la eficiencia reduciendo el tiempo entre la obtención de datos sin procesar y la obtención de perspectivas procesables.

Puede exportar todas las visualizaciones de una pestaña a un archivo de PDF o descargar los datos de un insight específico sin visualizaciones en formato de hoja de cálculo de Excel de Microsoft (XLSX).

También puede [cambiar el intervalo de fechas, configurar la vista y guardar una vista personalizada](/help/dsp/campaign-management/reports/campaign-data-views-manage.md){target="_blank"} como lo haría para las vistas de administración de campañas.

## Tipos de perspectivas

### [!UICONTROL Home] ficha

La pestaña [!UICONTROL Home] proporciona métricas clave de estándar, rendimiento y visibilidad en todas las campañas de un anunciante. De forma predeterminada, se muestran los datos de ubicaciones cruzadas de un anunciante específico y un objetivo personalizado. Si lo desea, puede configurar filtros para mostrar datos de un anunciante diferente, un objetivo personalizado diferente o una ubicación específica. <!-- I don't see campaigns or packages anymore:  You can optionally configure filters to show data for a different advertiser or data for only specific campaigns, packages, custom goals, and placements. --> Las perspectivas incluyen:

* **[!UICONTROL Trends]:** Un gráfico de tendencias para tres métricas especificadas por el cliente (de forma predeterminada, [!UICONTROL Net Spend], [!UICONTROL Impressions] y [!UICONTROL Net CPM]).

* **[!UICONTROL Delivery Breakdown]:** Un desglose de los datos de métricas específicas por tres dimensiones especificadas por el cliente, como por campaña, editor y tipo de medios. Para cada desglose dimensional, puede elegir una métrica diferente.

### [!UICONTROL Household Reach] ficha

La pestaña [!UICONTROL Household Reach] proporciona métricas de alcance doméstico en todas las campañas de un anunciante. De forma predeterminada, se muestran los datos de varias campañas. Si lo desea, puede configurar filtros para mostrar datos de un anunciante diferente, para una campaña específica, en paquetes o ubicaciones o para un paquete o ubicación específicos. Las perspectivas incluyen:

* **[!UICONTROL Trends]:** Un gráfico de tendencias por día o por semana para tres métricas especificadas por el cliente (de forma predeterminada, [!UICONTROL Net Spend], [!UICONTROL Unique Reach] y [!UICONTROL Net CPM]).

* **[!UICONTROL Incremental Household Reach]:** Gráfico de anillo que muestra el alcance incremental de la unidad familiar en [!UICONTROL Media Type], [!UICONTROL Device Type] o [!UICONTROL Inventory Type]. *Alcance doméstico incremental* se define como un hogar al que se llega exclusivamente a través de un solo medio, dispositivo o tipo de inventario.

* **[!UICONTROL Reach Breakdown]:** El alcance único incremental del hogar frente al alcance superpuesto del hogar por [!UICONTROL Media Type], [!UICONTROL Device Type] o [!UICONTROL Inventory Type].

  *Alcance doméstico incremental* se define como un hogar al que se llega exclusivamente a través de un solo medio, dispositivo o tipo de inventario. *Alcance doméstico superpuesto* se define como un hogar al que llegan varios medios, dispositivos o tipos de inventario.

* **[!UICONTROL Top Performers]:** Las campañas de mayor rendimiento, ubicaciones, paquetes, editores, sitios/aplicaciones, tipos de medios, tipos de inventario o tipos de dispositivos por [!UICONTROL Unique Reach], [!UICONTROL Net Spend] y [!UICONTROL Cost per Reach].

* **[!UICONTROL Performance Analysis]:** [!UICONTROL Cost per Reach] y [!UICONTROL Net Spend] por paquete, editor o sitio/aplicación. Utilice este insight para ver qué paquetes, editores o sitios/aplicaciones muestran el potencial de alcance incremental significativo.

  El tamaño de cada burbuja indica la puntuación de alcance incremental, con burbujas más grandes que indican un alcance incremental más alto en promedio. Para ver el nombre completo de la entidad y las métricas clave de cualquier burbuja, mantenga el cursor sobre la burbuja.

  Los niveles de impacto incluyen:

   * **Alto impacto:** Considere aumentar el presupuesto.
   * **Impacto moderado**
   * **Impacto limitado:** Necesita atención

### [!UICONTROL Household Conversion] ficha

La ficha [!UICONTROL Household Conversion] proporciona métricas de conversión domésticas en todas las campañas de un anunciante<!-- active only? -->. De forma predeterminada, se muestran los datos de campañas cruzadas de un anunciante específico y una métrica de conversión específica. Si lo desea, puede configurar filtros para mostrar datos de un anunciante o métrica de conversión diferente, de una campaña específica, de varios paquetes o ubicaciones, o de un paquete o ubicación específicos. Las perspectivas incluyen:

* **[!UICONTROL Trends]:** Un gráfico de tendencias por día o por semana para tres métricas especificadas por el cliente (de forma predeterminada, [!UICONTROL Net Spend], [!UICONTROL Conversions] y [!UICONTROL Net CPM]).

* **[!UICONTROL Conversion Participation Overview]:** Gráfico de barras que muestra los tipos de medios, tipos de inventario y tipos de dispositivos que generan la mayoría de las conversiones domésticas.

  Las impresiones entregadas dentro del período retroactivo (30 días) se consideran válidas para la participación en la conversión.

* **[!UICONTROL Top Performers]:** Una tabla de las campañas, paquetes, ubicaciones, editores, sitios/aplicaciones, tipos de medios y tipos de inventario que controlan el rendimiento de tres métricas especificadas por el cliente (de forma predeterminada, [!UICONTROL Net Spend], [!UICONTROL CPA] y [!UICONTROL Conversions]). El que tiene el mejor rendimiento aparece primero.

* **[!UICONTROL Performance Analysis]:** [!UICONTROL CPA] y [!UICONTROL Net Spend] por paquete, editor o sitio/aplicación. Utilice este insight para ver qué paquetes, editores o sitios/aplicaciones muestran el potencial de alcance incremental significativo.

  El tamaño de cada burbuja indica la puntuación de alcance incremental, con burbujas más grandes que indican un alcance incremental más alto en promedio. Para ver el nombre completo de la entidad y las métricas clave de cualquier burbuja, mantenga el cursor sobre la burbuja.

  Los niveles de impacto incluyen:

   * **Alto impacto:** Considere aumentar el presupuesto.
   * **Impacto moderado**
   * **Impacto limitado:** Necesita atención

## Abrir perspectivas de rendimiento

* (Para abrir perspectivas para todas las campañas) En el menú principal, haga clic en **[!UICONTROL Insights BETA]**.

* (Para abrir perspectivas para una campaña, paquete o ubicación específicos) Junto al nombre de la entidad en la vista [!UICONTROL Campaigns], [!UICONTROL Packages] o [!UICONTROL Placements], haga clic en **[!UICONTROL ...]** > **[!UICONTROL Insights]**.

* (Para abrir perspectivas para una ubicación específica) Junto al nombre de la entidad en la vista [!UICONTROL Campaigns], [!UICONTROL Packages] o [!UICONTROL Placements], haga clic en **[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Insights]** .

## Aplicar filtros a una pestaña

1. En la barra de herramientas situada en la parte superior de la ficha, haga clic en ![Botón Filtro](/help/dsp/assets/filter.png).

1. En la columna izquierda, seleccione una dimensión y, a continuación, seleccione uno o varios valores en la columna derecha, según corresponda.

   Solo puede seleccionar un anunciante a la vez.

1. Haga clic en **[!UICONTROL Apply]**.

1. (Opcional) Para reducir aún más los datos, seleccione el tipo de entidad en la barra de herramientas y, a continuación, seleccione un valor de entidad específico (una sola campaña, paquete o ubicación).

## Cambiar el informe de Dimension para un Insight

* En el menú desplegable situado en la parte superior izquierda de insight, seleccione la dimensión.

## Cambio de las métricas notificadas para una Insight

Para las métricas de conversión, existe compatibilidad con las conversiones rastreadas por Adobe Advertising y por Adobe Analytics.

1. En la parte superior derecha de insight, haga clic en ![Configuración de métricas](/help/dsp/assets/metric-settings.png "Configuración de métricas").

1. Seleccione las métricas y haga clic en **[!UICONTROL Apply]**.

## Exportar todas las visualizaciones de una ficha a un archivo de PDF

* Encima de la ficha, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Export]**.

  El archivo se guarda en la carpeta de descargas predeterminada del explorador.

## Descargar un Insight específico en un archivo XLSX

* En la parte superior derecha de insight, haz clic en ![Descargar](/help/creative/assets/download.png "Descargar").

  El archivo se guarda en la carpeta de descargas predeterminada del explorador.

>[!MORELIKETHIS]
>
>* [Acerca de los informes personalizados](/help/dsp/reports/report-about.md)
>* [Tipos de informes de rendimiento en las vistas de administración de campañas](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)
>* [Administrar Las Vistas De Datos De Campaign](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
