---
title: Configuración de las pruebas A/B para la búsqueda de Adobe Advertising, medios sociales y anuncios de Commerce en Adobe Target
description: Obtenga información sobre cómo configurar una prueba A/B en [!DNL Target] para su [!DNL Google Ads] y [!DNL Microsoft Advertising] anuncios en Search, Social y Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configuración de pruebas A/B en Adobe Target para anuncios de Advertising Search, Social y Commerce

*Anunciantes solo con Advertising Search, Social y Commerce*

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo cuentas*

Adobe Advertising y Adobe Target facilitan la configuración de pruebas A/B de experiencia de página de aterrizaje para el tráfico de publicidad digital [!DNL Google Ads] y [!DNL Microsoft Advertising] hasta:

* Mejorar las tasas de conversión (CVR) y las medidas de eficiencia de adquisición (como CPA, CPL y CAC).

* Ofrezca una experiencia de página de aterrizaje más personalizada que sea relevante para el anuncio (por ejemplo, haciendo coincidir la señal creativa de imagen/vídeo, la copia, la palabra clave u otra señal publicitaria con la página de aterrizaje).

También puede combinar el nativo [[!DNL Analytics] para publicidad](/help/integrations/analytics/overview.md) y [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) dimensiones de integration reporting integradas en Adobe Analytics para medir y visualizar los datos de prueba con [!DNL Analytics] métricas y eventos de éxito.

Consulte las secciones siguientes para conocer los requisitos previos e instrucciones para configurar pruebas A/B en [!DNL Target] para obtener tráfico de clics de anuncios en Search, Social y Commerce, y sugerencias sobre cómo medir y visualizar las pruebas en [!DNL Analytics].

## Requisitos previos

### Productos requeridos

* Buscar, Social y Commerce
* [!DNL Target]

### Productos e integraciones recomendados

* [!DNL Analytics]

* [[!DNL Analytics] para publicidad](/help/integrations/analytics/overview.md) integración<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integración

## Paso 1: Crear una actividad de prueba A/B en [!DNL Target] para Search, Social y Commerce

Las siguientes instrucciones resaltan información relacionada con el caso de uso de Search, Social y Commerce.

1. [Iniciar sesión en Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Creación de una prueba A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. En el **[!UICONTROL Enter Activity URL]** , introduzca la dirección URL de la página de aterrizaje para la prueba.

   1. En el **[!UICONTROL Goal]** , introduzca la métrica de éxito de la prueba.

      >[!NOTE]
      >
      >Asegúrese de que [!DNL Analytics] está habilitado como fuente de datos dentro de [!DNL Target]y que esté seleccionado el grupo de informes correcto.

   1. Configure las variables **[!UICONTROL Priority]** hasta `High` o `999` para evitar conflictos cuando los usuarios del segmento de prueba reciben una experiencia en el sitio incorrecta.


   1. En **[!UICONTROL Reporting Settings]**, seleccione la **[!UICONTROL Company Name]** y **[!UICONTROL Report Suite]** conectado a su cuenta de Search, Social y Commerce.

      Para obtener más sugerencias sobre los informes, consulte[Informe sobre prácticas recomendadas y solución de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. En el **[!UICONTROL Date Range]** , introduzca las fechas de inicio y finalización adecuadas para la prueba.

   1. Seleccionar **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. En el **[!UICONTROL Value]** , introduzca la variable [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], o [!UICONTROL Network Ad ID] para la entidad de red de publicidad relevante en Search, Social y Commerce. Esto le permite utilizar la variable [!DNL Target] parámetros de cadena de consulta para audiencias de pulsaciones para la entidad.

      Puede encontrar el ID de la siguiente manera: [adición de la columna de ID relevante a la vista de entidades](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] en la columna [!UICONTROL Accounts] vista](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] en la columna [!UICONTROL Accounts] vista")

      Póngase en contacto con el equipo de cuenta de Adobe si necesita ayuda.

   1. Para el **[!UICONTROL Traffic Allocation Method]**, seleccione **[!UICONTROL Manual (Default)]** y dividió la audiencia al 50/50.

   1. Guarde la actividad.

1. Uso [Compositor de experiencias visuales de Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) para realizar cambios de diseño en la plantilla de página de aterrizaje de prueba A/B.

   * Experiencia A: no edite porque es la experiencia predeterminada/de control de página de aterrizaje sin personalización.

   * Experiencia B: usar el [!DNL Target] interfaz de usuario para personalizar la plantilla de página de aterrizaje en función de los recursos incluidos en la prueba (como titulares, textos, ubicación de botones y material creativo).

   >[!NOTE]
   >
   >Por ejemplo, en casos de uso de pruebas creativas, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 2: Configuración de [!DNL Analytics for Target] Analysis Workspace en [!DNL Analytics]

[!DNL Analytics for Target] (A4T) es una integración de soluciones cruzadas que permite a los anunciantes crear [!DNL Target] actividades basadas en [!DNL Analytics] métricas de conversión y segmentos de audiencia y, a continuación, mida los resultados utilizando [!DNL Analytics] como fuente de informes. Todos los informes y la segmentación de esa actividad se basan en [!DNL Analytics] recopilación de datos.

Para obtener más información acerca de [!DNL Analytics for Target], incluido un vínculo a las instrucciones de implementación, consulte &quot;[Adobe Analytics como fuente de informes para Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configure las variables [!DNL Analytics for Target] Panel

En Analysis Workspace, configure las [!DNL Analytics for Target panel] para analizar su [!DNL Target] actividades y experiencias. Tenga en cuenta los siguientes puntos importantes y la información sobre los informes.

#### Métricas

* Cree un panel dentro del espacio de trabajo específico para la cuenta de Adobe Advertising, la campaña o el grupo de anuncios<!-- only applicable entities? --> para el que se ejecutó la prueba. Utilice visualizaciones de resumen para mostrar las métricas de Adobe Advertising en el mismo informe que la variable [!DNL Target] rendimiento de las pruebas.

* Priorice el uso de métricas en el sitio (como visitas y conversiones) para medir el rendimiento.

* Comprenda que las métricas de medios agregadas de los Adobes Advertising (como impresiones, clics y costes) no se pueden comparar con [!DNL Target] métricas.

#### Dimension

Las siguientes dimensiones pertenecen a [!DNL Analytics for Target]:

* **Actividades de Target**: Nombre de la prueba A/B

* **Experiencias de Target**: Nombres de experiencias de página de aterrizaje utilizados dentro de la actividad

* **Actividad de Target** > **Experiencia**: Nombre de la actividad y nombre de la experiencia en la misma fila

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
* [Información general sobre las pruebas A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) : describe actividades de prueba A/B que puede utilizar con anuncios de Search, Social y Commerce.
* [Descripción general de Analytics para publicidad](/help/integrations/analytics/overview.md) : presenta Analytics para publicidad, que le permite rastrear las interacciones del sitio de clics y visualizaciones en las instancias de Analytics.

>[!MORELIKETHIS]
>
>* [Configuración de pruebas A/B en Adobe Target DSP para anuncios de Advertising](ab-tests-dsp.md)
