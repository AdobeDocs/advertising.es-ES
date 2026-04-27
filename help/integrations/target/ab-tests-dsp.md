---
title: Configuración de pruebas A/B para anuncios de Adobe Advertising DSP en Adobe Target
description: Aprenda a configurar una prueba A/B en  [!DNL Target]  para sus anuncios de DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
TQID: https://experienceleague.adobe.com/xETpACcZbZqfFjS58mS-k-kXhm0BT79W0aHz2bdKDGs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3did: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1645
ht-degree: 0%

---

# Configuración de pruebas A/B en Adobe Target para anuncios de Advertising DSP

*Anunciantes solo con Advertising DSP*

Adobe Advertising y Adobe Target facilitan aún más a los especialistas en marketing la entrega de una experiencia personalizada y conectada a través de medios de pago y mensajería en el sitio. Al compartir señales entre los productos, puede:

* Reduzca las tasas de visitas en el orden previsto del sitio vinculando la exposición de los clientes a los anuncios de las campañas de DSP con sus experiencias en el sitio.

* Establezca pruebas A/B reflejando las experiencias en el sitio con mensajes publicitarios mediante datos de exposición de Adobe Audience Manager y haga clic para alimentar las audiencias [!DNL Target].

* Mida el impacto de la mensajería unificada en un alza de objetivos en el sitio con visualizaciones simples en Adobe Analytics para [!DNL Target].

Consulte las secciones siguientes para conocer los requisitos previos y las instrucciones para configurar el seguimiento de clics y visualizaciones, implementar el uso compartido de señales entre DSP y [!DNL Target], configurar una actividad de prueba A/B y configurar [!DNL Analytics] Analysis Workspace para ver los datos de prueba.

Si tiene más preguntas, póngase en contacto con el equipo de cuenta de Adobe.

## Requisitos previos

Este caso de uso requiere los siguientes productos e integraciones:

* [!DNL Target]

* [[!DNL Analytics] para la integración de Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integración de [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)

* Audience Manager (requerido solo para pruebas de visualización)

## Paso 1: Configuración del marco de trabajo de pulsaciones {#click-through-framework}

![Módulo de pulsaciones](/help/integrations/assets/target-ct-framework.png)

Cuando agrega macros de DSP a una dirección URL de pulsación (la dirección URL que se muestra cuando un usuario hace clic en un anuncio y llega a la página de aterrizaje), DSP captura automáticamente la clave de colocación incluyendo `${TM_PLACEMENT_ID}` en la dirección URL de pulsación. Esta macro captura la clave de ubicación alfanumérica y no el ID de ubicación numérico.

![URL de pulsación anexada a la dirección URL de la página de aterrizaje](/help/integrations/assets/target-ct-url.jpg)

### (Solo DSP) Agregue macros de DSP a las direcciones URL de pulsación

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

En [!DNL Flashtalking] o Google Campaign Manager 360, actualice manualmente la dirección URL de pulsación para cada anuncio a fin de incluir las macros necesarias para capturar las variables de ID de AMO. Las variables de ID de AMO se utilizan para enviar datos sobre clics a Adobe Analytics y compartir claves de ubicación para pruebas A/B. Consulte las siguientes páginas para obtener instrucciones:

* [Anexar [!DNL Analytics for Advertising] macros a [!DNL Flashtalking] etiquetas de publicidad](/help/integrations/analytics/macros-flashtalking.md). **Nota:** Este procedimiento no es necesario si su organización tiene una asociación directa con [!DNL Flashtalking] y usa macros de paso de datos para realizar el seguimiento de los parámetros de seguimiento `s_kwcid` y `ef_id` según la documentación de soporte de [!DNL Flashtalking] en [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

* [Anexar  [!DNL Analytics for Advertising] macros a [!DNL Google Campaign Manager 360] etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md)

Póngase en contacto con el equipo de cuenta de Adobe para recuperar la clave de ubicación necesaria, finalizar la configuración y asegurarse de que cada URL de pulsación se rellena con la clave de ubicación.

## Paso 2: Configurar el marco de trabajo de visualización mediante Audience Manager {#view-through-framework}

![Módulo de visualización](/help/integrations/assets/targetr-vt-framework.png)

Al añadir un píxel de evento de impresión de Audience Manager en la configuración de colocación y etiquetas de publicidad, puede crear un segmento de prueba para oportunidades de prueba de visualizaciones adicionales.

1. Implement an Audience Manager impression event pixel in your ad tags and DSP placement settings.

   For instructions, see &quot;[Collect media exposure data from Advertising DSP campaigns](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Make sure you add [DSP macros](/help/dsp/campaign-management/macros.md) to capture all data you want the impression event pixel to pass back, including `${TM_PLACEMENT_ID_NUM}` for the numeric placement ID.

   >[!NOTE]
   >
   >Click-tracking URLs include the `${TM_PLACEMENT_ID}` macro for the alphanumeric placement key, instead of `${TM_PLACEMENT_ID_NUM}` for the numeric placement ID.

1. Configure an Audience Manager segment from the DSP impression data:

   1. Verify that segment data is available:

      1. [Search for the signal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) for the [key-value pair](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) that determines at what level the segment users are grouped.

         Use a [supported key](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) with a value that corresponds to a macro that you added to the Audience Manager impression event pixel.

         For example, to group users for a particular placement, use the `d_placement` key. For the value, use an actual numeric placement ID (such as 2501853) that&#39;s captured by the DSP macro `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         If the search results show user counts for the key-value pair, which indicates that the pixel was placed correctly and data is flowing, then continue to the next step.

   1. [Create a rule-based trait](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) for segment creation in Audience Manager.

      * Name the trait so that it’s easily identifiable within test activities. Store the trait in whichever folder you prefer.

      * Select `Ad Cloud` as the **[!UICONTROL Data Source]**.

      * For the trait expression, use `d_event` as the **[!UICONTROL Key]** and `imp` as the **[!UICONTROL Value]**.

   1. [Set up a test segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) for the new trait in Audience Manager, selecting `Ad Cloud` as the **[!UICONTROL Data Source]**.

      Audience Manager automatically splits the segment into a control group that receives the standard landing page experience and a test group that received a personalized onsite experience.

## Step 3: Set up an A/B test activity in [!DNL Target] for DSP

The following instructions highlight information pertaining to the DSP use case.

1. [Sign in to Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Create an A/B test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In the **[!UICONTROL Enter Activity URL]** field, enter the landing page URL for the test.

      >[!NOTE]
      >
      >You can use multiple URLs to test view-through site entry. For more information, see &quot;[Multipage Activity](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Puede identificar fácilmente las entradas principales por dirección URL de página creando un [informe de entrada al sitio](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) en Analytics.

   1. En el campo **[!UICONTROL Goal]**, introduzca la métrica de éxito de la prueba.

      >[!NOTE]
      >
      >Asegúrese de que [!DNL Analytics] esté habilitado como origen de datos en [!DNL Target] y de que esté seleccionado el grupo de informes correcto.

   1. Establezca **[!UICONTROL Priority]** en `High` o `999` para evitar conflictos cuando los usuarios del segmento de prueba reciban una experiencia en el sitio incorrecta.

   1. En **[!UICONTROL Reporting Settings]**, seleccione **[!UICONTROL Company Name]** y **[!UICONTROL Report Suite]** se conectaron a su cuenta de DSP.

      Para obtener sugerencias adicionales sobre los informes, consulte &quot;[Prácticas recomendadas de informes y solución de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)&quot;.

   1. En el campo **[!UICONTROL Date Range]**, escriba las fechas de inicio y finalización apropiadas para la prueba.

   1. Añada audiencias a la actividad:

      1. Elija el [segmento que creó anteriormente en Audience Manager para probar las audiencias de visualización](#view-through-framework).

      1. Seleccione **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** e introduzca la clave de ubicación de DSP en el campo **[!UICONTROL Value]** para utilizar los parámetros de cadena de consulta de Target para audiencias de pulsación.

   1. Para **[!UICONTROL Traffic Allocation Method]**, seleccione **[!UICONTROL Manual (Default)]** y divida la audiencia al 50/50.

   1. Guarde la actividad.

1. Use [Compositor de experiencias visuales de Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) para realizar cambios de diseño en la plantilla de página de aterrizaje de prueba A/B.

   * Experiencia A: no edite porque es la experiencia predeterminada/de control de página de aterrizaje sin personalización.

   * Experiencia B: utilice la interfaz de usuario [!DNL Target] para personalizar la plantilla de página de aterrizaje en función de los recursos incluidos en la prueba (como titulares, textos, ubicación de botones y material creativo).

   >[!NOTE]
   >
   >Por ejemplo, en casos de uso de pruebas creativas, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 4: Configurar su Analysis Workspace [!DNL Analytics for Target] en [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) es una integración de soluciones cruzadas que permite a los anunciantes crear actividades [!DNL Target] basadas en [!DNL Analytics] métricas de conversión y segmentos de audiencia y luego medir los resultados usando [!DNL Analytics] como fuente de informes. Todos los informes y la segmentación de esa actividad se basan en la recopilación de datos de [!DNL Analytics].

Para obtener más información acerca de [!DNL Analytics for Target], incluido un vínculo a las instrucciones de implementación, consulte &quot;[Adobe Analytics como fuente de informes para Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configurar el panel [!DNL Analytics for Target]

En Analysis Workspace, configure [!DNL Analytics for Target panel] para analizar las actividades y experiencias de [!DNL Target]. Tenga en cuenta los siguientes puntos importantes y la información sobre los informes.

#### Métricas

* Cree un panel dentro del espacio de trabajo específico para la campaña, el paquete o la ubicación de Adobe Advertising para el que se ejecutó la prueba. Utilice visualizaciones de resumen para mostrar las métricas de Adobe Advertising en el mismo informe que el rendimiento de la prueba [!DNL Target].

* Priorice el uso de métricas en el sitio (como visitas y conversiones) para medir el rendimiento.

* Tenga en cuenta que las métricas de medios agregadas de Adobe Advertising (como impresiones, clics y costes) no pueden coincidir con las métricas de [!DNL Target].

#### Dimensiones

Las siguientes dimensiones pertenecen a [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: nombre de la prueba A/B

* **[!UICONTROL Target Experiences]**: nombres de experiencias de página de aterrizaje usados en la actividad

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: el nombre de actividad y el nombre de experiencia de la misma fila

### Solucionar problemas de Analytics para datos de [!DNL Target]

En Analysis Workspace, si observa que los datos de actividad y experiencias son mínimos o no se rellenan, haga lo siguiente:

* Compruebe que se utiliza el mismo [!UICONTROL Supplemental Data ID] (SDID) para [!DNL Target] y [!DNL Analytics]. Puede comprobar los valores de SDID usando [Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) en la página de aterrizaje a la que la campaña dirige a los usuarios.

  [Valores de ID de datos suplementarios (SDID) en Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* En la misma página de aterrizaje, compruebe que a) [!UICONTROL Hostname] mostrado en Adobe Debugger bajo [!UICONTROL Solutions] > [!UICONTROL Target] coincide con b) [!UICONTROL Tracking Server] mostrado en [!DNL Target] para la actividad (bajo [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] requiere que se envíe un servidor de seguimiento [!DNL Analytics] en las llamadas de [!DNL Target] al servidor de recopilación de datos [!DNL Modstats] para Analytics.<!-- just "to Analytics?"-->

  [Valor de nombre de host en Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

  [Valor del servidor de seguimiento en Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Lectura adicional

* [Integrar Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Explica cómo configurar los informes de [!DNL Target] en Analysis Workspace.
* [Información general sobre pruebas A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Describe actividades de pruebas A/B que se pueden usar con anuncios de DSP.
* [Experiencias y ofertas](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explica las herramientas de [!DNL Target] para determinar el contenido en el sitio al que están expuestos los usuarios de prueba de DSP.
* [Señales, rasgos y segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html): define algunas de las herramientas de Audience Manager que pueden ayudar con las pruebas de visualización de DSP.
* [Información general sobre [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) - Presenta [!DNL Analytics for Advertising], que le permite rastrear las interacciones del sitio de clics y visualizaciones en sus instancias de Analytics.

>[!MORELIKETHIS]
>
>* [Configurar pruebas A/B en Adobe Target para anuncios de Advertising Search, Social y Commerce](ab-tests-search.md)
