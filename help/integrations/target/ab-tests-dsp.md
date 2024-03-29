---
title: Configuración de pruebas A/B para anuncios de Adobe Advertising DSP en Adobe Target
description: Obtenga información sobre cómo configurar una prueba A/B en [!DNL Target] DSP para sus anuncios de la.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 7ffa5d3e9f1aae0f9d66d87c74807e491e818daa
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---

# Configuración de pruebas A/B en Adobe Target DSP para anuncios de Advertising

*DSP Solo anunciantes con Advertising*

Adobe Advertising y Adobe Target facilitan aún más a los especialistas en marketing la entrega de una experiencia personalizada y conectada a través de medios de pago y mensajería en el sitio. Al compartir señales entre los productos, puede:

* DSP Reduzca las tasas de visitas en el orden previsto del sitio vinculando la exposición de los clientes a los anuncios de las campañas de la campaña de la campaña de la campaña de la campaña de la campaña de publicidad a sus experiencias en el sitio.

* Establezca pruebas A/B reflejando las experiencias en el sitio con mensajes publicitarios mediante datos de exposición de Adobe Audience Manager y clics para alimentarlas [!DNL Target] audiencias.

* Mida el impacto de la mensajería unificada en un alza de objetivos en el sitio con visualizaciones simples en Adobe Analytics para [!DNL Target].

DSP Consulte las secciones siguientes para conocer los requisitos previos y las instrucciones para configurar el seguimiento de clics y visualizaciones, implementar el uso compartido de señales entre los usuarios de y [!DNL Target] y configure una actividad de prueba A/B, y [!DNL Analytics] Analysis Workspace para ver los datos de prueba.

Si tiene más preguntas, póngase en contacto con adcloud_support@adobe.com.

## Requisitos previos

Este caso de uso requiere los siguientes productos e integraciones:

* [!DNL Target]

* [[!DNL Analytics] para publicidad](/help/integrations/analytics/overview.md) integración<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integración

* Audience Manager (necesario solo para las pruebas de visualización)

## Paso 1: Configuración del marco de trabajo de pulsaciones {#click-through-framework}

![Marco de pulsaciones](/help/integrations/assets/target-ct-framework.png)

DSP DSP Cuando agrega macros de a una dirección URL de pulsación (la dirección URL que se muestra cuando un usuario hace clic en un anuncio y llega a la página de aterrizaje), captura automáticamente la clave de colocación incluyendo `${TM_PLACEMENT_ID}` en la URL de pulsación. Esta macro captura la clave de ubicación alfanumérica y no el ID de ubicación numérico.

![URL de pulsación adjunta a la dirección URL de la página de aterrizaje](/help/integrations/assets/target-ct-url.jpg)

### DSP DSP (Solo en el caso de los) Agregar macros de código a las direcciones URL de pulsación

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

En Flashes o Google Campaign Manager 360, actualice manualmente la URL de pulsación para cada anuncio para incluir las macros necesarias para capturar las variables de ID de AMO. Las variables de ID de AMO se utilizan para enviar datos sobre clics a Adobe Analytics y compartir claves de ubicación para pruebas A/B. Consulte las siguientes páginas para obtener instrucciones:

* [Añadir [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad](/help/integrations/analytics/macros-flashtalking.md)

* [Añadir [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md)

Póngase en contacto con el equipo de cuenta de Adobe y con el grupo de soluciones de publicidad (aac-advertising-solutions-group@adobe.com) para recuperar la clave de ubicación necesaria y finalizar la configuración, así como para asegurarse de que cada URL de pulsación se rellena con la clave de ubicación.

## Paso 2: Configurar el marco de trabajo de visualización mediante un Audience Manager {#view-through-framework}

![Marco de visualización](/help/integrations/assets/targetr-vt-framework.png)

Al añadir un píxel de evento de impresión Audience Manager en la configuración de colocación y etiquetas de publicidad, puede crear un segmento de prueba para oportunidades de prueba de visualizaciones adicionales.

1. Implemente un píxel de evento de impresión Audience Manager DSP en la configuración de colocación de etiquetas de publicidad y de elementos de.

   Para obtener instrucciones, consulte &quot;[DSP Recopilación de datos de exposición de medios de campañas de Advertising](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Asegúrese de añadir [DSP macros de](/help/dsp/campaign-management/macros.md) para capturar todos los datos que desea que devuelva el píxel del evento de impresión, incluido `${TM_PLACEMENT_ID_NUM}` para el ID de ubicación numérico.

   >[!NOTE]
   >
   >Las direcciones URL de seguimiento de clics incluyen `${TM_PLACEMENT_ID}` macro para la tecla de posición alfanumérica, en lugar de `${TM_PLACEMENT_ID_NUM}` para el ID de ubicación numérico.

1. Configure un segmento de Audience Manager DSP a partir de los datos de impresión de la:

   1. Compruebe que los datos del segmento están disponibles:

      1. [Buscar la señal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) para el [par clave-valor](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) que determina a qué nivel se agrupan los usuarios del segmento.

         Utilice un [clave admitida](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) con un valor que corresponde a una macro agregada al píxel del evento de impresión del Audience Manager.

         Por ejemplo, para agrupar usuarios para una ubicación determinada, utilice el `d_placement` clave. DSP Para el valor, utilice un ID de colocación numérica real (como 2501853) capturado por la macro de `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Si los resultados de la búsqueda muestran los recuentos de usuarios para el par clave-valor, lo que indica que el píxel se colocó correctamente y los datos están fluyendo, continúe con el siguiente paso.

   1. [Crear un rasgo basado en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) para la creación de segmentos en Audience Manager.

      * Asigne un nombre al rasgo para que se pueda identificar fácilmente dentro de las actividades de prueba. Almacene el rasgo en la carpeta que prefiera.

      * Seleccionar `Ad Cloud` como el **[!UICONTROL Data Source]**.

      * Para la expresión de rasgos, utilice `d_event` como el **[!UICONTROL Key]** y `imp` como el **[!UICONTROL Value]**.

   1. [Configuración de un segmento de prueba](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) para el nuevo rasgo en Audience Manager, seleccione `Ad Cloud` como el **[!UICONTROL Data Source]**.

      Audience Manager divide automáticamente el segmento en un grupo de control que recibe la experiencia de página de aterrizaje estándar y un grupo de prueba que recibió una experiencia en el sitio personalizada.

## Paso 3: Configurar una actividad de prueba A/B en [!DNL Target] DSP para la

DSP Las siguientes instrucciones resaltan la información relacionada con el caso de uso de la.

1. [Iniciar sesión en Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Creación de una prueba A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. En el **[!UICONTROL Enter Activity URL]** , introduzca la dirección URL de la página de aterrizaje para la prueba.

      >[!NOTE]
      >
      >Puede utilizar varias direcciones URL para probar la entrada del sitio de visualización. Para obtener más información, consulte &quot;[Actividad de varias páginas](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Puede identificar fácilmente las entradas principales por dirección URL de página creando un [Informe de entrada al sitio](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) en Analytics.

   1. En el **[!UICONTROL Goal]** , introduzca la métrica de éxito de la prueba.

      >[!NOTE]
      >
      >Asegúrese de que [!DNL Analytics] está habilitado como fuente de datos dentro de [!DNL Target]y que esté seleccionado el grupo de informes correcto.

   1. Configure las variables **[!UICONTROL Priority]** hasta `High` o `999` para evitar conflictos cuando los usuarios del segmento de prueba reciben una experiencia en el sitio incorrecta.

   1. En **[!UICONTROL Reporting Settings]**, seleccione la **[!UICONTROL Company Name]** y **[!UICONTROL Report Suite]** DSP conectado a su cuenta de la cuenta de la.

      Para obtener más sugerencias sobre los informes, consulte[Informe sobre prácticas recomendadas y solución de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. En el **[!UICONTROL Date Range]** , introduzca las fechas de inicio y finalización adecuadas para la prueba.

   1. Añada audiencias a la actividad:

      1. Elija la [segmento que creó anteriormente en Audience Manager para probar las audiencias de visualización](#view-through-framework).

      1. Seleccionar **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** DSP , e introduzca la clave de ubicación de la en **[!UICONTROL Value]** para utilizar los parámetros de cadena de consulta de Target para audiencias de pulsación.

   1. Para el **[!UICONTROL Traffic Allocation Method]**, seleccione **[!UICONTROL Manual (Default)]** y dividió la audiencia al 50/50.

   1. Guarde la actividad.

1. Uso [Compositor de experiencias visuales de Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) para realizar cambios de diseño en la plantilla de página de aterrizaje de prueba A/B.

   * Experiencia A: no edite porque es la experiencia predeterminada/de control de página de aterrizaje sin personalización.

   * Experiencia B: usar el [!DNL Target] interfaz de usuario para personalizar la plantilla de página de aterrizaje en función de los recursos incluidos en la prueba (como titulares, textos, ubicación de botones y material creativo).

   >[!NOTE]
   >
   >Por ejemplo, en casos de uso de pruebas creativas, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 4: Configuración de [!DNL Analytics for Target] Analysis Workspace en [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) es una integración de soluciones cruzadas que permite a los anunciantes crear [!DNL Target] actividades basadas en [!DNL Analytics] métricas de conversión y segmentos de audiencia y, a continuación, mida los resultados utilizando [!DNL Analytics] como fuente de informes. Todos los informes y la segmentación de esa actividad se basan en [!DNL Analytics] recopilación de datos.

Para obtener más información acerca de [!DNL Analytics for Target], incluido un vínculo a las instrucciones de implementación, consulte &quot;[Adobe Analytics como fuente de informes para Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configure las variables [!DNL Analytics for Target] Panel

En Analysis Workspace, configure las [!DNL Analytics for Target panel] para analizar su [!DNL Target] actividades y experiencias. Tenga en cuenta los siguientes puntos importantes y la información sobre los informes.

#### Métricas

* Cree un panel dentro del espacio de trabajo específico para la campaña de Adobe Advertising, el paquete o la ubicación para los que se ejecutó la prueba. Utilice visualizaciones de resumen para mostrar las métricas de Adobe Advertising en el mismo informe que la variable [!DNL Target] rendimiento de las pruebas.

* Priorice el uso de métricas en el sitio (como visitas y conversiones) para medir el rendimiento.

* Comprenda que las métricas de medios agregadas de los Adobes Advertising (como impresiones, clics y costes) no se pueden comparar con [!DNL Target] métricas.

#### Dimension

Las siguientes dimensiones pertenecen a [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: Nombre de la prueba A/B

* **[!UICONTROL Target Experiences]**: Nombres de experiencias de página de aterrizaje utilizados dentro de la actividad

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: Nombre de la actividad y nombre de la experiencia en la misma fila

### Solución de problemas de Analytics para [!DNL Target] Datos

En Analysis Workspace, si observa que los datos de actividad y experiencias son mínimos o no se rellenan, haga lo siguiente:

* Compruebe que es lo mismo [!UICONTROL Supplemental Data ID] (SDID) se utiliza tanto para [!DNL Target] y [!DNL Analytics]. Puede verificar los valores de SDID mediante el [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) en la página de aterrizaje a la que la campaña dirija a los usuarios.

[Valores de ID de datos suplementarios (SDID) en Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* En la misma página de aterrizaje, compruebe que: a) la variable [!UICONTROL Hostname] mostrado en el Adobe Debugger debajo de [!UICONTROL Solutions] > [!UICONTROL Target] coincide con b) el [!UICONTROL Tracking Server] mostrado en [!DNL Target] para la actividad (en [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] requiere un [!DNL Analytics] servidor de seguimiento para enviar en llamadas desde [!DNL Target] a la [!DNL Modstats] servidor de recopilación de datos para Analytics.<!-- just "to Analytics?"-->

[Valor de nombre de host en Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor del servidor de seguimiento en Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Lectura adicional

* [Integración de Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Explica cómo configurar [!DNL Target] creación de informes en Analysis Workspace.
* [Información general sobre las pruebas A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) DSP : Describe las actividades de prueba A/B, que puede utilizar con anuncios de la lista de distribución de.
* [Experiencias y ofertas](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explica [!DNL Target] DSP herramientas para determinar el contenido en el sitio al que están expuestos los usuarios de prueba de la.
* [Señales, rasgos y segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) : define algunas de las herramientas del Audience Manager DSP que pueden ayudar con las pruebas de visualización de la vista de la.
* [Descripción general de Analytics para publicidad](/help/integrations/analytics/overview.md) : presenta Analytics para publicidad, que le permite rastrear las interacciones del sitio de clics y visualizaciones en las instancias de Analytics.

>[!MORELIKETHIS]
>
>* [Configuración de pruebas A/B en Adobe Target para anuncios de Advertising Search, Social y Commerce](ab-tests-search.md)
