---
title: Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]
description: Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]

*DSP Anunciantes con Advertising y[!DNL Advertising Search, Social, & Commerce]*

Revise la siguiente información antes de integrar Adobe Advertising con Adobe Analytics.

## Requisitos para informar de datos de Adobe Advertising en [!DNL Analytics]

* Cualquiera de las siguientes opciones:
   * SDK web de Adobe Experience Platform: `alloy.js`
   * Servicio de identidad del Experience Cloud: `visitorAPI.js` versión 2.0 o superior
* Cualquier versión de Adobe Analytics (incluidas [!DNL Prime], [!DNL Premium], o [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versión 2.1 o superior
* DSP (Clientes de Advertising) Un [DSP Fragmento de JavaScript de Advertising](javascript.md) implementado en sus páginas web para realizar un seguimiento de las visitas de visualización.

>[!TIP]
>
>Para mejorar la fidelidad de los datos, utilice la versión más reciente de cada biblioteca.

## Requisitos para compartir segmentos de Analytics con Adobe Advertising

* Servicio de identidad del Experience Cloud: `visitorAPI.js` versión 2.1 o superior
* Adobe Analytics: `appMeasurement.js` versión 1.8 o superior

## Requisitos para los informes [!DNL Analytics] Datos en Adobe Advertising

Proporcione al equipo de implementación del Adobe Advertising lo siguiente:

* El [!DNL Analytics] ID del grupo de informes que se utilizará para los informes sobre la actividad de medios de pago y para alimentar la actividad del sitio para la optimización y los informes en Adobe Advertising
* ID de organización del Experience Cloud de la empresa (ID de organización).

Puede encontrar ambos ID en la página [Pestaña Resumen de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Pantalla Resumen del Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Datos en Adobe Advertising {#lookback-a4adc}

Porque [!DNL Analytics] Los datos de se envían al Adobe Advertising de para la creación de informes y la optimización. Los datos están sujetos a las reglas de atribución, incluidas las ventanas retrospectivas de impresiones y clics, que se configuran para el anunciante en Adobe Advertising.

![configuración de ventana retrospectiva de nivel de anunciante en Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* ventana retrospectiva de clics de atribución de Adobes Advertising: número de días después de que se produce el primer clic en los que el clic puede atribuirse a una conversión. De forma predeterminada, este valor es 60 días; el máximo es 90 días
* Ventana retrospectiva de impresión de atribución de Adobes Advertising: Número de días después de que se produzca una impresión de publicidad en los que la impresión puede atribuirse a una conversión. De forma predeterminada, este valor es 14 días; el máximo es 30 días

  >[!NOTE]
  >
  > La ventana retrospectiva de impresiones es específica del Adobe Advertising, no del [!DNL Analytics for Advertising], creación de informes.

El [!DNL Analytics for Advertising] JavaScript utiliza esta configuración para determinar hasta dónde se considera válida una entrada de visualización o una entrada de pulsaciones en el sitio. Para obtener más información sobre cómo se determinan las visualizaciones y los clics, consulte &quot;[ID de Adobe Advertising utilizados por Analytics](ids.md).&quot;

## Adobe Advertising de datos en [!DNL Analytics]

[!DNL Analytics] establece ID de Adobe Advertising (AMO ID) dentro de la visita de Analytics, según el ID del anunciante [!DNL eVar] configuración de persistencia, que se aplica tanto a pulsaciones como a visualizaciones. La configuración de persistencia se establece en el back-end del Adobe Advertising y el equipo de cuenta de Adobe puede cambiarla.

* [!DNL Analytics for Advertising] [!DNL eVar] caducidad: 60 días de forma predeterminada para los ID de AMO

>[!NOTE]
>
>Para segmentar datos para un periodo de tiempo diferente, puede [configuración de segmentos personalizados](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) con diferentes ventanas retrospectivas dentro de Analysis Workspace.

## Entornos de publicidad admitidos

* Buscar
* Mostrar
* Vídeo
* Vídeo en línea
* Nativo

Póngase en contacto con su equipo de cuenta de Adobe para conocer los entornos de publicidad admitidos más recientes en cada canal.

## Aspectos que debe saber antes de implementar

* El equipo de implementación de Adobe Advertising configura la integración.

* No se facturan costes adicionales por esta integración, ni las llamadas al servidor resultan en costes adicionales [!DNL Analytics] o tarifas de Adobe Advertising.

* [!DNL Analytics for Advertising] no depende del servidor de publicidad: puede producirse una visualización o un clic desde cualquier servidor de publicidad y se generan los ID adecuados al entrar en el sitio.

* La integración pasa solamente [!DNL Analytics] eventos estándar y personalizados con el Adobe Advertising para la optimización de ofertas de los esfuerzos posteriores de medios de pago y publicidad. No pasa... [!DNL Analytics] segmentos, métricas calculadas y [!DNL eVars] al Adobe Advertising para la optimización de ofertas.

* El Adobe Advertising crea ID persistentes dentro de [!DNL Analytics] se basa en el último anuncio en el que se hizo clic o se visualizó antes de que el usuario entre en el sitio, según la variable [ventanas retrospectivas de clics y visualizaciones](#lookback-a4adc) configurado en el Adobe Advertising. Si el visitante de un sitio tiene ambos tipos de interacciones de entrada al sitio dentro de su perfil y el clic se encuentra dentro del período retrospectivo, el ID de pulsación del visitante anula el ID de visualización para la creación de informes de sitio.

* [!DNL Analytics for Advertising] el seguimiento de conversión en Adobe Analytics utiliza una ventana retrospectiva de seguimiento configurable (de forma predeterminada, 60 días). Los informes de Adobe Advertising reflejan las conversiones del sitio y la participación a través del final de esta ventana retrospectiva de seguimiento.

* Se admiten todos los tipos de anuncios. Sin embargo, no todos los entornos de publicidad son compatibles.

  Por ejemplo, los anuncios de TV conectados (CTV) no se rastrean porque no se producen clics en CTV y no se pueden producir conversiones en el mismo dispositivo. Sin embargo, si el anuncio se visualiza dentro de un entorno de escritorio, se pueden rastrear algunos datos de entrada del sitio de visualización.

* [!DNL Analytics] en este momento, las conversiones solo se rastrean y atribuyen a un visitante del mismo dispositivo.

* [!DNL Analytics for Advertising] no admite conversiones de visualización en la aplicación.

* El seguimiento de visualizaciones no es compatible con los anunciantes que utilizan una implementación de reenvío del lado del servidor de [!DNL Analytics].

### ID suplementario

Una vez implementado el servicio de ID de Experience Cloud para un sitio, las visitas que contengan datos de [!DNL Analytics] o el Adobe Advertising contienen un ID suplementario.

Ejemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para una integración de datos precisa, todas las llamadas de Adobe Advertising utilizadas por un [!DNL Analytics for Advertising] actividad para entregar contenido o registrar la métrica de objetivo debe tener un correspondiente [!DNL Analytics] visita que comparte el mismo ID suplementario.

Cuando solucione problemas en [!DNL Analytics], asegúrese de que el ID suplementario esté presente para [!DNL Analytics] visitas. En el [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), puede ver este ID en la pestaña Adobe Advertising como `sdid` parámetro.

>[!NOTE]
>
> Esta implementación funciona de manera similar a la [!DNL Analytics for Target] integración.

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript para Analytics para publicidad](/help/integrations/analytics/javascript.md)
