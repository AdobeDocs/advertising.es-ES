---
title: Configuración de las pruebas A/B para anuncios de Adobe Advertising Search, Social y Commerce en Adobe Target
description: Aprenda a configurar una prueba A/B en  [!DNL Target] para sus anuncios [!DNL Google Ads] y [!DNL Microsoft Advertising] en Search, Social y Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configuración de pruebas A/B en Adobe Target para anuncios de Advertising Search, Social y Commerce

*Solo anunciantes con Advertising Search, Social y Commerce*

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo cuentas*

Adobe Advertising y Adobe Target facilitan la configuración de pruebas A/B de experiencia de página de aterrizaje para el tráfico de publicidad digital [!DNL Google Ads] y [!DNL Microsoft Advertising] a fin de:

* Mejorar las tasas de conversión (CVR) y las medidas de eficiencia de adquisición (como CPA, CPL y CAC).

* Ofrezca una experiencia de página de aterrizaje más personalizada que sea relevante para el anuncio (por ejemplo, haciendo coincidir la señal creativa de imagen/vídeo, la copia, la palabra clave u otra señal publicitaria con la página de aterrizaje).

También puede combinar las dimensiones de informes de integración nativas [[!DNL Analytics] para Advertising](/help/integrations/analytics/overview.md) y [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=es) que están integradas en Adobe Analytics para medir y visualizar los datos de prueba con [!DNL Analytics] métricas y eventos de éxito.

Consulte las siguientes secciones para conocer los requisitos previos, instrucciones para configurar pruebas A/B en [!DNL Target] para el tráfico de pulsaciones de anuncios en Search, Social y Commerce, y sugerencias sobre cómo medir y visualizar las pruebas en [!DNL Analytics].

## Requisitos previos

### Productos requeridos

* Buscar, Social y Commerce
* [!DNL Target]

### Productos e integraciones recomendados

* [!DNL Analytics]

* [[!DNL Analytics] para la integración de Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integración de [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=es)

## Paso 1: Crear una actividad de prueba A/B en [!DNL Target] para Search, Social y Commerce

Las siguientes instrucciones resaltan información relacionada con el caso de uso de Search, Social y Commerce.

1. [Inicie sesión en Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=es).

1. [Crear una prueba A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=es):

   1. En el campo **[!UICONTROL Enter Activity URL]**, introduzca la dirección URL de la página de aterrizaje para la prueba.

   1. En el campo **[!UICONTROL Goal]**, introduzca la métrica de éxito de la prueba.

      >[!NOTE]
      >
      >Asegúrese de que [!DNL Analytics] esté habilitado como origen de datos en [!DNL Target] y de que esté seleccionado el grupo de informes correcto.

   1. Establezca **[!UICONTROL Priority]** en `High` o `999` para evitar conflictos cuando los usuarios del segmento de prueba reciban una experiencia en el sitio incorrecta.


   1. En **[!UICONTROL Reporting Settings]**, seleccione **[!UICONTROL Company Name]** y **[!UICONTROL Report Suite]** se conectaron a su cuenta de Search, Social y Commerce.

      Para obtener sugerencias adicionales sobre los informes, consulte &quot;[Prácticas recomendadas de informes y solución de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=es)&quot;.

   1. En el campo **[!UICONTROL Date Range]**, escriba las fechas de inicio y finalización apropiadas para la prueba.

   1. Seleccione **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. En el campo **[!UICONTROL Value]**, escriba [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID] o [!UICONTROL Network Ad ID] para la entidad de red de publicidad relevante en Buscar, Social y Commerce. Esto le permite usar los parámetros de cadena de consulta [!DNL Target] para audiencias de pulsaciones de la entidad.

      Puede encontrar el ID [agregando la columna de ID relevante a la vista de entidades](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] columna en la vista [!UICONTROL Accounts] &#x200B;](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] columna en la vista [!UICONTROL Accounts]")

      Póngase en contacto con el equipo de su cuenta de Adobe si necesita ayuda.

   1. Para **[!UICONTROL Traffic Allocation Method]**, seleccione **[!UICONTROL Manual (Default)]** y divida la audiencia al 50/50.

   1. Guarde la actividad.

1. Use [Compositor de experiencias visuales de Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=es) para realizar cambios de diseño en la plantilla de página de aterrizaje de prueba A/B.

   * Experiencia A: no edite porque es la experiencia predeterminada/de control de página de aterrizaje sin personalización.

   * Experiencia B: utilice la interfaz de usuario [!DNL Target] para personalizar la plantilla de página de aterrizaje en función de los recursos incluidos en la prueba (como titulares, textos, ubicación de botones y material creativo).

   >[!NOTE]
   >
   >Por ejemplo, en casos de uso de pruebas creativas, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 2: Configurar su Analysis Workspace [!DNL Analytics for Target] en [!DNL Analytics]

[!DNL Analytics for Target] (A4T) es una integración de soluciones cruzadas que permite a los anunciantes crear actividades [!DNL Target] basadas en [!DNL Analytics] métricas de conversión y segmentos de audiencia y luego medir los resultados usando [!DNL Analytics] como fuente de informes. Todos los informes y la segmentación de esa actividad se basan en la recopilación de datos de [!DNL Analytics].

Para obtener más información acerca de [!DNL Analytics for Target], incluido un vínculo a las instrucciones de implementación, consulte &quot;[Adobe Analytics como fuente de informes para Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=es)&quot;.

### Configurar el panel [!DNL Analytics for Target]

En Analysis Workspace, configure [!DNL Analytics for Target panel] para analizar las actividades y experiencias de [!DNL Target]. Tenga en cuenta los siguientes puntos importantes y la información sobre los informes.

#### Métricas

* Cree un panel dentro del área de trabajo específico para la cuenta de Adobe Advertising, la campaña o el grupo de anuncios <!-- only applicable entities? --> para el que se ejecutó la prueba. Utilice visualizaciones de resumen para mostrar las métricas de Adobe Advertising en el mismo informe que el rendimiento de la prueba [!DNL Target].

* Priorice el uso de métricas en el sitio (como visitas y conversiones) para medir el rendimiento.

* Tenga en cuenta que las métricas de medios agregadas de Adobe Advertising (como impresiones, clics y costes) no pueden coincidir con las métricas de [!DNL Target].

#### Dimensiones

Las siguientes dimensiones pertenecen a [!DNL Analytics for Target]:

* **Actividades de Target**: Nombre de la prueba A/B

* **Experiencias de Target**: Nombres de experiencias de página de aterrizaje usados en la actividad

* **Actividad de Target** > **Experiencia**: Nombre de la actividad y nombre de la experiencia en la misma fila

### Solucionar problemas de Analytics para datos de [!DNL Target]

En Analysis Workspace, si observa que los datos de actividad y experiencias son mínimos o no se rellenan, haga lo siguiente:

* Compruebe que se utiliza el mismo [!UICONTROL Supplemental Data ID] (SDID) para [!DNL Target] y [!DNL Analytics]. Puede comprobar los valores de SDID con [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=es) en la página de aterrizaje a la que la campaña dirija a los usuarios.

[Valores de ID de datos suplementarios (SDID) en Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* En la misma página de aterrizaje, compruebe que a) [!UICONTROL Hostname] mostrado en Adobe Debugger bajo [!UICONTROL Solutions] > [!UICONTROL Target] coincide con b) [!UICONTROL Tracking Server] mostrado en [!DNL Target] para la actividad (bajo [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] requiere que se envíe un servidor de seguimiento [!DNL Analytics] en las llamadas de [!DNL Target] al servidor de recopilación de datos [!DNL Modstats] para Analytics.<!-- just "to Analytics?"-->

[Valor de nombre de host en Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor del servidor de seguimiento en Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Lectura adicional

* [Integrar Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=es) - Explica cómo configurar los informes de [!DNL Target] en Analysis Workspace.
* [Información general sobre la prueba A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=es): describe actividades de prueba A/B que puede usar con anuncios de Search, Social y Commerce.
* [Información general sobre Analytics para Advertising](/help/integrations/analytics/overview.md): presenta Analytics para Advertising, que le permite rastrear las interacciones de sitios de clics y visualizaciones en las instancias de Analytics.

>[!MORELIKETHIS]
>
>* [Configurar pruebas A/B en Adobe Target para Advertising DSP Ads](ab-tests-dsp.md)
