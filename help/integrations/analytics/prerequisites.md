---
title: Requisitos previos e información clave para implementar  [!DNL Analytics for Advertising]
description: Requisitos previos e información clave para implementar  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Requisitos previos e información clave para implementar [!DNL Analytics for Advertising]

*Anunciantes con Advertising DSP y[!DNL Advertising Search, Social, & Commerce]*

Revise la siguiente información antes de integrar Adobe Advertising con Adobe Analytics.

## Requisitos para informar datos de Adobe Advertising en [!DNL Analytics]

* Cualquiera de las siguientes opciones:
   * SDK web de Adobe Experience Platform: `alloy.js`
   * Servicio de identidad de Experience Cloud: `visitorAPI.js` versión 2.0 o superior
* Cualquier versión de Adobe Analytics (incluidas [!DNL Prime], [!DNL Premium] o [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versión 2.1 o superior
* (Clientes de Advertising DSP) Se ha implementado un [fragmento de Advertising DSP JavaScript](javascript.md) en sus páginas web para rastrear las visitas de visualización.

>[!TIP]
>
>Para mejorar la fidelidad de los datos, utilice la versión más reciente de cada biblioteca.

## Requisitos para compartir segmentos de Analytics con Adobe Advertising

* Servicio de identidad del Experience Cloud: `visitorAPI.js` versión 2.1 o superior
* Adobe Analytics: `appMeasurement.js` versión 1.8 o superior

## Requisitos para informar [!DNL Analytics] datos en Adobe Advertising

Proporcione al equipo de implementación del Adobe Advertising lo siguiente:

* El ID del grupo de informes [!DNL Analytics] que se usará para generar informes sobre la actividad de medios de pago y para alimentar la actividad del sitio para la optimización y la creación de informes en el Adobe Advertising
* ID de organización del Experience Cloud de la empresa (ID de organización).

Puede encontrar ambos ID en la [pestaña Summary de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=es).

![Pantalla de resumen de Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] datos en el Adobe Advertising {#lookback-a4adc}

Como los datos de [!DNL Analytics] se envían al Adobe Advertising para la creación de informes y la optimización, están sujetos a las reglas de atribución, incluidas las ventanas retrospectivas de impresiones y clics, que se configuran para el anunciante en Adobe Advertising.

![configuración de ventana retrospectiva de nivel de anunciante en el Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* ventana retrospectiva de clics de atribución de Adobes Advertising: número de días después de que se produce el primer clic en los que el clic puede atribuirse a una conversión. De forma predeterminada, este valor es 60 días; el máximo es 90 días
* Ventana retrospectiva de impresión de atribución de Adobes Advertising: Número de días después de que se produzca una impresión de publicidad en los que la impresión puede atribuirse a una conversión. De forma predeterminada, este valor es 14 días; el máximo es 30 días

  >[!NOTE]
  >
  > La ventana retrospectiva de impresiones es específica para los informes de Adobe Advertising, no de [!DNL Analytics for Advertising].

El JavaScript [!DNL Analytics for Advertising] usa esta configuración para determinar hasta dónde se considera válida una entrada de pulsaciones o vistas del sitio. Para obtener más información sobre cómo se determinan las visualizaciones y los clics, consulte &quot;[ID de Adobe Advertising usados por Analytics](ids.md)&quot;.

## Datos de Adobe Advertising en [!DNL Analytics]

[!DNL Analytics] establece los ID de Adobe Advertising (AMO ID) dentro de la visita de Analytics, sujeto a la configuración de persistencia [!DNL eVar] del anunciante, que se aplica tanto a las pulsaciones como a las visualizaciones. La configuración de persistencia se establece en el back-end del Adobe Advertising y el equipo de cuenta de Adobe puede cambiarla.

* [!DNL Analytics for Advertising] [!DNL eVar] caducidad: 60 días de forma predeterminada para los ID de AMO

>[!NOTE]
>
>Para segmentar datos para un periodo de tiempo diferente, puede [configurar segmentos personalizados](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=es) con diferentes ventanas retrospectivas dentro de Analysis Workspace.

## Entornos de publicidad admitidos

* Buscar
* Mostrar
* Vídeo
* Vídeo en línea
* Televisor conectado
* Nativo

Póngase en contacto con su equipo de cuenta de Adobe para conocer los entornos de publicidad admitidos más recientes en cada canal.

## Aspectos que debe saber antes de implementar

* El equipo de implementación de Adobe Advertising configura la integración.

* No se facturan costos adicionales por esta integración, ni las llamadas al servidor resultan en [!DNL Analytics] adicionales o cargos de Adobe Advertising.

* [!DNL Analytics for Advertising] no depende de un servidor de publicidad: es posible que se produzca una visualización o un clic desde cualquier servidor de publicidad y que se generen los ID adecuados al ingresar al sitio.

* La integración pasa solamente [!DNL Analytics] eventos estándar y personalizados al Adobe Advertising para la optimización de ofertas de los esfuerzos de medios pagados y publicidad subsiguientes. No pasa [!DNL Analytics] segmentos, métricas calculadas ni [!DNL eVars] al Adobe Advertising para la optimización de ofertas.

* El Adobe Advertising crea ID persistentes dentro de [!DNL Analytics] basados en el último anuncio en el que se hizo clic o que se vio antes de que el usuario ingresara al sitio, en función de [las ventanas retrospectivas de clics y visualizaciones](#lookback-a4adc) configuradas en el Adobe Advertising. Si el visitante de un sitio tiene ambos tipos de interacciones de entrada al sitio dentro de su perfil y el clic se encuentra dentro del período retrospectivo, el ID de pulsación del visitante anula el ID de visualización para la creación de informes de sitio.

* El seguimiento de conversión de [!DNL Analytics for Advertising] en Adobe Analytics usa una ventana retrospectiva de seguimiento configurable (de forma predeterminada, 60 días). Los informes de Adobe Advertising reflejan las conversiones del sitio y la participación a través del final de esta ventana retrospectiva de seguimiento.

* Se admiten todos los tipos de anuncios. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* En este momento se realiza un seguimiento de las conversiones de [!DNL Analytics], que solo se atribuyen a un visitante del mismo dispositivo.

* [!DNL Analytics for Advertising] no admite conversiones de visualización en la aplicación.

* El seguimiento de visualizaciones no es compatible con anunciantes que usen una implementación de reenvío del lado del servidor de [!DNL Analytics].

### ID suplementario

Una vez implementado el servicio de identidad de Experience Cloud para un sitio, las visitas que contienen datos de [!DNL Analytics] o Adobe Advertising contienen un ID suplementario.

Ejemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para conseguir una integración de datos precisa, todas las llamadas de Adobe Advertising que use una actividad [!DNL Analytics for Advertising] para entregar contenido o registrar la métrica de objetivo deben tener una visita [!DNL Analytics] correspondiente que comparta el mismo ID suplementario.

Cuando solucione problemas en [!DNL Analytics], asegúrese de que el ID suplementario esté presente para [!DNL Analytics] visitas. En [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=es), puede ver este identificador en la ficha Adobe Advertising como el parámetro `sdid`.

>[!NOTE]
>
> Esta implementación funciona de manera similar a la integración de [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript para Analytics para Advertising](/help/integrations/analytics/javascript.md)
