---
title: Informes de rendimiento de nivel de experiencia
description: Obtenga información sobre cómo ver informes de rendimiento de nivel de experiencia.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 118838e0236c0e40aea797edb1b2f8fb0efb2a79
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Informes de rendimiento de nivel de experiencia

*Beta cerrada*

Puede ver datos de rendimiento detallados de cualquier experiencia.

## Datos en informes de rendimiento de nivel de experiencia

La vista Informe incluye los siguientes datos:

* **Pestaña Información general**: Una descripción general del rendimiento en todas las métricas de conversión de toda la experiencia<!-- Currently, the only metric in the settings list at the top of this main tab is "Select All." -->, que incluye:

   * **Rendimiento general** sección:

      * **Rendimiento general**: el total de impresiones; clics; tasa de clics (CTR); y conversiones de visualizaciones y clics.

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

      * **Tasa predeterminada**: (Solo experiencias con segmentación en el árbol de decisiones) El número de impresiones resultantes de elementos creativos segmentados, elementos creativos genéricos sin segmentación o segmentados a &quot;Todos los demás&quot; y el elemento creativo predeterminado para la experiencia.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **Desglose de rendimiento** sección:

      * **Rendimiento regional:*: Métricas individuales por ubicación geográfica.

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Rendimiento del dispositivo:** Métricas individuales por tipo de dispositivo, sistema operativo y explorador. Si lo desea, haga clic en el valor de cualquier categoría de dispositivo para ver una lista de los <!-- NN --> principales creativos que se incluyen en ese criterio.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Rendimiento de Creative** pestaña*: Información general sobre el rendimiento por creatividad y paquete o etiqueta de publicidad, que incluye:

   * **Creativos** subpestaña: Número total de impresiones, clics y CTR para cada creativo en la experiencia.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

   * **Paquetes/etiquetas** subpestaña: El número total de impresiones, clics y CTR para paquetes individuales (experiencias con segmentación del árbol de decisiones) o etiquetas de publicidad (experiencias sin segmentación del árbol de decisiones) en la experiencia.

## Ver informes de rendimiento de una experiencia

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir experiencias específicas.

1. Seleccione la experiencia:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Reports]**.

   * En la vista de tabla, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL Reports]**.

   Se abre la ficha [!UICONTROL Overview].

1. (Opcional) En la barra de herramientas superior derecha, especifique el intervalo de fechas, la regla de atribución de conversión y las conversiones incluidas en los informes de rendimiento:

   * (Opcional) Para cambiar el intervalo de fechas de los datos de rendimiento, elija una opción en el menú de fecha:

      * Para especificar un período preestablecido, seleccione el informe: (*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today],* o *[!UICONTROL Yesterday]*.

      * Para especificar un intervalo de fechas personalizado, escriba la fecha de inicio y la de finalización o haga clic en ![icono de calendario](/help/search-social-commerce/assets/calendar.png) junto a un campo y seleccione una fecha.

   * (Opcional) Para cambiar la regla utilizada para atribuir datos de conversión en una serie de eventos que llevan a una conversión, haga clic en ![Configuración](/help/creative/assets/settings.png) y cambie **[!UICONTROL Attribution Rule]**.

     Para obtener más información acerca de las reglas de atribución, vea &quot;[Cómo se calculan las reglas de atribución](/help/search-social-commerce/reports/attribution-rules.md)&quot;.

   * (Opcional) Para cambiar las conversiones notificadas, haga clic en ![Configuración](/help/creative/assets/settings.png) y seleccione los nombres de conversión en el menú **[!UICONTROL Conversions]**. Actualmente, la única métrica disponible es &quot;Seleccionar todo&quot; para incluir todas las métricas de conversión.

     Las columnas de conversión disponibles incluyen las conversiones disponibles en Advertising Search, Social y Commerce, independientemente de si es cliente de Search, Social y Commerce. La lista puede incluir métricas de conversión y participación del sitio sincronizadas desde Adobe Analytics cuando el anunciante tiene [una [!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md). [!DNL Analytics] métricas calculadas y métricas calculadas avanzadas no están disponibles. Para obtener más información acerca de cómo incluir las conversiones recopiladas en los informes, consulte el tema de la Guía de Search, Social y Commerce &quot;[Acerca de la administración de las métricas de conversión de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)&quot;.

1. (En la ficha [!UICONTROL Overview]):

   * (Opcional) En la sección [!UICONTROL Overall Regional Performance], mantenga el cursor sobre un punto del gráfico para ver los datos de ese punto.

   * (Opcional) En la sección [!UICONTROL Regional Performance], realice una de las siguientes acciones:

      * Haga clic en un nombre de métrica (como [!UICONTROL Impressions]) para ver esa métrica.

      * Seleccione la región en el menú [!UICONTROL Region].

      * Mantenga el cursor sobre un país o estado para ver los datos de esa región.

   * (Opcional) En la sección [!UICONTROL Device Performance], realice una de las siguientes acciones:

      * Mantenga el cursor sobre el valor de cualquier categoría de dispositivo para ver los datos de ese criterio.

      * Haga clic en el valor de cualquier categoría de dispositivo para ver una lista de los <!-- NN--> principales creativos que se han proporcionado con ese criterio.

1. (Opcional) Para ver los datos por creatividad y por paquete o etiqueta de publicidad, haga clic en la pestaña **[!UICONTROL Creative Performance]**.

   * En la subpestaña [!UICONTROL Creatives], puede realizar cualquiera de las siguientes acciones:

      * (Opcional) Para cambiar entre la vista de gráfico y la vista de cuadrícula, haga clic en ![Gráfico](/help/creative/assets/chart-view-button.png "Gráfico") y ![Cuadrícula](/help/creative/assets/table-view-button.png "Cuadrícula"), respectivamente.

      * (Opcional) En la vista de gráfico, mantenga el cursor sobre un punto del gráfico para ver los datos de ese punto.

      * (Experiencias solo con segmentación en el árbol de decisiones; opcional) Para dividir el rendimiento de cada destino de anuncio aplicado, habilite **[!UICONTROL Split targeting]**.

1. Para ver los datos por paquete (experiencias con segmentación del árbol de decisiones) o etiqueta de publicidad (experiencias sin segmentación del árbol de decisiones), haga clic en la subpestaña **[!UICONTROL Bundles]**. Puede realizar cualquiera de las siguientes acciones:

   * (Opcional) Para cambiar entre la vista de gráfico y la vista de cuadrícula, haga clic en ![Gráfico](/help/creative/assets/chart-view-button.png "Gráfico") y ![Cuadrícula](/help/creative/assets/table-view-button.png "Cuadrícula"), respectivamente.

   * (Opcional) En la vista de gráfico, mantenga el cursor sobre un punto del gráfico para ver los datos de ese punto.

   * (Experiencias solo con segmentación en el árbol de decisiones; opcional) Para dividir el rendimiento de cada destino de anuncio aplicado, habilite **[!UICONTROL Split targeting]**.

## Descargar informes de rendimiento para una experiencia

* En la barra de herramientas situada en la parte superior de los informes de rendimiento, haga clic en ![Descargar](/help/creative/assets/download.png "Descargar").

  El archivo se descarga en un archivo de [!DNL Microsoft Excel] en formato de hoja de cálculo (XLSX), según el procedimiento normal del explorador.

>[!MORELIKETHIS]
>
>* [Informe de Creative personalizado](/help/creative/report-custom-creative.md)
>* [Descargar todas las experiencias en la vista](/help/creative/experiences/experience-download-view.md)
>* [Acerca de las experiencias en Advertising Creative](/help/creative/experiences/experience-about.md)
