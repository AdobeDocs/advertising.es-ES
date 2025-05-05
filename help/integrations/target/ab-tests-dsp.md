---
title: Configuración de pruebas A/B para anuncios de Adobe Advertising DSP en Adobe Target
description: Aprenda a configurar una prueba A/B en  [!DNL Target]  para sus anuncios de DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: a69bef9d249514f5c494cff8d706b9df792eaf23
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# Configuración de pruebas A/B en Adobe Target para publicidad DSP publicidad

*Solo anunciantes con DSP publicitarios*

Adobe Systems La publicidad y el Adobe Target hacen que sea igualado más fácil para los especialistas en marketing ofrecer un experiencia personalizado y conectado en medios de pago y mensajería en el sitio. Al compartir señales entre los productos, puede:

* Reduzca las tasas de visitas en el orden previsto del sitio vinculando la exposición de los clientes a los anuncios de las campañas de DSP con sus experiencias en el sitio.

* Establezca pruebas A/B reflejando las experiencias en el sitio con mensajes publicitarios mediante datos de exposición de Adobe Audience Manager y haga clic para alimentar las audiencias [!DNL Target].

* Mida el impacto de los mensajería unificados en un alza objetiva in situ con visualizaciones sencillas en Adobe Analytics para [!DNL Target].

Consulte las siguientes secciones para conocer los requisitos previos y obtener instrucciones sobre cómo configurar las seguimiento de pulsaciones y vista, implementar el uso compartido de señales entre DSP y [!DNL Target] y configurar un actividad de prueba A/B, y configurar [!DNL Analytics] Analysis Workspace para vista los datos prueba.

Si tiene más preguntas, póngase en contacto con adcloud_support@adobe.com.

## Requisitos previos

Este caso de uso requiere los siguientes productos e integraciones:

* [!DNL Target]

* [[!DNL Analytics] para la integración de publicidad](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integración de [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=es)

* Audience Manager (requerido solo para pruebas de visualización)

## Paso 1: Configuración del marco de trabajo de pulsaciones {#click-through-framework}

![Módulo de pulsaciones](/help/integrations/assets/target-ct-framework.png)

Cuando agrega macros de DSP a una dirección URL de pulsación (la dirección URL que se muestra cuando un usuario hace clic en un anuncio y llega a la página de aterrizaje), DSP captura automáticamente la clave de colocación incluyendo `${TM_PLACEMENT_ID}` en la dirección URL de pulsación. Esta macro captura la clave de ubicación alfanumérica y no el ID de ubicación numérico.

![URL de pulsación anexada a la dirección URL de la página de aterrizaje](/help/integrations/assets/target-ct-url.jpg)

### (Solo DSP) Agregar macros de DSP a las direcciones URL de pulsaciones

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

En [!DNL Flashtalking] o Google Campaign Manager 360, actualice manualmente la dirección URL de pulsación para cada anuncio a fin de incluir las macros necesarias para capturar las variables de ID de AMO. Las variables de ID de AMO se utilizan para enviar datos sobre clics a Adobe Analytics y compartir claves de ubicación para pruebas A/B. Consulte las siguientes páginas para obtener instrucciones:

* [Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad](/help/integrations/analytics/macros-flashtalking.md). **Nota:** Este procedimiento no es necesario si su organización tiene una asociación directa con [!DNL Flashtalking] y usa macros de paso de datos para realizar el seguimiento de los parámetros de seguimiento `s_kwcid` y `ef_id` según la documentación de soporte de [!DNL Flashtalking] en [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

* [Anexar  [!DNL Analytics for Advertising] macros a [!DNL Google Campaign Manager 360] etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md)

Póngase en contacto con el equipo de su cuenta de Adobe y con el grupo de soluciones de Advertising (aac-advertising-solutions-group@adobe.com) para recuperar la clave de ubicación necesaria y finalizar la configuración, así como para asegurarse de que cada URL de pulsación se rellena con la clave de ubicación.

## Paso 2: Configurar el marco de trabajo de visualización mediante Audience Manager {#view-through-framework}

![Módulo de visualización](/help/integrations/assets/targetr-vt-framework.png)

Al añadir un píxel de evento de impresión de Audience Manager en la configuración de colocación y etiquetas de publicidad, puede crear un segmento de prueba para oportunidades de prueba de visualizaciones adicionales.

1. Implemente un píxel de evento de impresión de Audience Manager en la configuración de colocación de etiquetas de publicidad y DSP.

   Para obtener instrucciones, consulte &quot;[Recopilar datos de exposición de medios de campañas de Advertising DSP](/help/integrations/audience-manager/media-data-integration/collect.md)&quot;.

   Asegúrese de agregar [macros de DSP](/help/dsp/campaign-management/macros.md) para capturar todos los datos que desea que devuelva el píxel del evento de impresión, incluido `${TM_PLACEMENT_ID_NUM}` para el identificador numérico de ubicación.

   >[!NOTE]
   >
   >Las direcciones URL de seguimiento de clics incluyen la macro `${TM_PLACEMENT_ID}` para la clave de ubicación alfanumérica, en lugar de `${TM_PLACEMENT_ID_NUM}` para el ID de ubicación numérico.

1. Configure un segmento de Audience Manager a partir de los datos de impresiones de DSP:

   1. Compruebe que los datos del segmento están disponibles:

      1. [Busque la señal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html?lang=es) del [par clave-valor](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html?lang=es) que determina en qué nivel se agrupan los usuarios del segmento.

         Use una [clave admitida](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=es) con un valor que corresponda a la macro que agregó al píxel del evento de impresión de Audience Manager.

         Por ejemplo, para agrupar usuarios para una ubicación en particular, use la clave `d_placement`. Para el valor, use un Id. de ubicación numérica real (como 2501853) capturado por la macro de DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Si los resultados de la búsqueda muestran los recuentos de usuarios para el par clave-valor, lo que indica que el píxel se colocó correctamente y los datos están fluyendo, continúe con el siguiente paso.

   1. [Crear un rasgo basado en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=es) para la creación de segmentos en Audience Manager.

      * Asigne un nombre al rasgo para que se pueda identificar fácilmente dentro de las actividades de prueba. Almacene el rasgo en la carpeta que prefiera.

      * Seleccione `Ad Cloud` como **[!UICONTROL Data Source]**.

      * Para la expresión de rasgos, use `d_event` como **[!UICONTROL Key]** y `imp` como **[!UICONTROL Value]**.

   1. [Configure un segmento de prueba](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html?lang=es) para el nuevo rasgo en Audience Manager, seleccionando `Ad Cloud` como **[!UICONTROL Data Source]**.

      Audience Manager divide automáticamente el segmento en un grupo de control que recibe la experiencia de página de aterrizaje estándar y un grupo de prueba que recibió una experiencia en el sitio personalizada.

## Paso 3: Configurar una actividad de prueba A/B en [!DNL Target] para DSP

Las siguientes instrucciones resaltan información perteneciente al caso de uso de DSP.

1. [Inicie sesión en Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=es).

1. [Crear una prueba A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=es):

   1. En el campo **[!UICONTROL Enter Activity URL]**, introduzca la dirección URL de la página de aterrizaje para la prueba.

      >[!NOTE]
      >
      >Puede utilizar varias direcciones URL para probar la entrada del sitio de visualización. Para obtener más información, consulte &quot;[Actividad multipágina](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html?lang=es)&quot;. Puede identificar fácilmente las entradas principales por dirección URL de página creando un [informe de entrada al sitio](https://experienceleague.adobe.com/es/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) en Analytics.

   1. En el campo **[!UICONTROL Goal]**, introduzca la métrica de éxito de la prueba.

      >[!NOTE]
      >
      >Asegúrese de que [!DNL Analytics] esté habilitado como origen de datos en [!DNL Target] y de que esté seleccionado el grupo de informes correcto.

   1. Establezca **[!UICONTROL Priority]** en `High` o `999` para evitar conflictos cuando los usuarios del segmento de prueba reciban una experiencia en el sitio incorrecta.

   1. En **[!UICONTROL Reporting Settings]**, seleccione **[!UICONTROL Company Name]** y **[!UICONTROL Report Suite]** se conectaron a su cuenta de DSP.

      Para obtener sugerencias adicionales sobre los informes, consulte &quot;[Prácticas recomendadas de informes y solución de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=es)&quot;.

   1. En el campo **[!UICONTROL Date Range]**, escriba las fechas de inicio y finalización apropiadas para la prueba.

   1. Añada audiencias a la actividad:

      1. Elija el [segmento que creó anteriormente en Audience Manager para probar las audiencias de visualización](#view-through-framework).

      1. Seleccione **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** e introduzca la clave de ubicación de DSP en el campo **[!UICONTROL Value]** para utilizar los parámetros de cadena de consulta de Target para audiencias de pulsación.

   1. Para el **[!UICONTROL Traffic Allocation Method]**, seleccione **[!UICONTROL Manual (Default)]** y divida el audiencia 50/50.

   1. Guardar el actividad.

1. Utilice [Target Compositor](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=es) de experiencias visuales para realizar cambios de diseño en la prueba A/B página de aterrizaje plantilla.

   * Experiencia A: no edite porque es la experiencia predeterminada/de control de página de aterrizaje sin personalización.

   * Experiencia B: utilice la interfaz de usuario [!DNL Target] para personalizar la plantilla de página de aterrizaje en función de los recursos incluidos en la prueba (como titulares, textos, ubicación de botones y material creativo).

   >[!NOTE]
   >
   >Por ejemplo, en casos de uso de pruebas creativas, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 4: Configura tu [!DNL Analytics for Target] Analysis Workspace en [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) es una integración entre soluciones que permite a los anunciantes crear [!DNL Target] actividades basadas en [!DNL Analytics] métricas de Conversión y segmentos de audiencia y luego medir los resultados utilizando [!DNL Analytics] como fuente sistema de informes. Todos los sistema de informes y segmentación para esa actividad se basan en [!DNL Analytics] recopilación de datos.

Para obtener más información acerca de [!DNL Analytics for Target], incluido un vincular para implementación instrucciones, consulte &quot;[Adobe Analytics como origen sistema de informes para Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=es)&quot;.

### Configuración del [!DNL Analytics for Target] panel

En Analysis Workspace, configure el [!DNL Analytics for Target panel] para analizar sus [!DNL Target] actividades y experiencias. Tenga en cuenta los siguientes puntos importantes y la información sobre los informes.

#### Métricas

* Cree un panel dentro del espacio de trabajo específico para la campaña, el paquete o la ubicación de Adobe Advertising para el que se ejecutó la prueba. Utilice visualizaciones de resumen para mostrar las métricas de Adobe Advertising en el mismo informe que el rendimiento de la prueba [!DNL Target].

* Priorice el uso de métricas en el sitio (como visitas y conversiones) para medir el rendimiento.

* Tenga en cuenta que las métricas de medios agregadas de Adobe Advertising (como impresiones, clics y costes) no pueden coincidir con las métricas de [!DNL Target].

#### Dimensiones

Las siguientes dimensiones corresponden a [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: nombre de la prueba A/B

* **[!UICONTROL Target Experiences]**: nombres de experiencias de página de aterrizaje usados en la actividad

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: el nombre de actividad y el nombre de experiencia de la misma fila

### Solucionar problemas de Analytics para datos de [!DNL Target]

Dentro de Analysis Workspace, si nota que los datos de actividad y experiencias son mínimos o no se rellenan, haga lo siguiente:

* Compruebe que se utiliza el mismo [!UICONTROL Supplemental Data ID] (SDID) para ambos [!DNL Target] y [!DNL Analytics]para . Puede verificar los valores de SDID utilizando el [depurador](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=es) de Adobe Experience Cloud en la página de aterrizaje a la que el campaña conduce a los usuarios.

[Valores de ID de datos suplementarios (SDID) en Adobe Systems Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* En el mismo página de aterrizaje, compruebe que a) el [!UICONTROL Hostname] que se muestra en Adobe Systems Debugger en [!UICONTROL Solutions] > [!UICONTROL Target] coincide b) el [!UICONTROL Tracking Server] que se muestra en [!DNL Target] para el actividad (en [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target]Requiere el envío de un [!DNL Analytics] servidor seguimiento en llamadas desde al [!DNL Modstats] servidor recopilación de datos [!DNL Target] para Analytics.<!-- just "to Analytics?"-->

[Valor de nombre de host en Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor del servidor de seguimiento en Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Lectura adicional

* [Integrar Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=es) - Explica cómo configurar los informes de [!DNL Target] en Analysis Workspace.
* [Información general sobre pruebas A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=es) - Describe actividades de pruebas A/B que se pueden usar con anuncios de DSP.
* [Experiencias y ofertas](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html?lang=es) - Explica las herramientas de [!DNL Target] para determinar el contenido en el sitio al que están expuestos los usuarios de prueba de DSP.
* [Señales, rasgos y segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html?lang=es): define algunas de las herramientas de Audience Manager que pueden ayudar con las pruebas de visualización de DSP.
* [Información general sobre Analytics para Advertising](/help/integrations/analytics/overview.md): presenta Analytics para Advertising, que le permite rastrear las interacciones de sitios de clics y visualizaciones en las instancias de Analytics.

>[!MORELIKETHIS]
>
>* [Configurar pruebas A/B en Adobe Target para anuncios de Advertising Search, Social y Commerce](ab-tests-search.md)
