---
title: Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]
description: Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]

*Anunciantes con DSP publicitaria y[!DNL Advertising Search, Social, & Commerce]*

Revise la siguiente información antes de integrar Adobe Systems Advertising con Adobe Analytics.

## Requisitos para la creación de informes Adobe Systems datos publicitarios en [!DNL Analytics]

* Cualquiera de las siguientes opciones:
   * SDK web de Adobe Experience Platform: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` versión 2.0 o superior
* Cualquier versión de Adobe Analytics (incluyendo [!DNL Prime], [!DNL Premium], o [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versión 2.1 o superior
* (Publicidad DSP clientes) Fragmento [](javascript.md) de DSP JavaScript publicitario implementado en las páginas web para realizar un seguimiento de vista visitas.

>[!TIP]
>
>Para mejorar la fidelidad de los datos, utilice la versión más reciente de cada biblioteca.

## Requisitos para compartir segmentos de Analytics con publicidad Adobe Systems

* Experience Cloud Identity Service: `visitorAPI.js` versión 2.1 o superior
* Adobe Analytics: `appMeasurement.js` versión 1.8 o superior

## Requisitos para la presentación de [!DNL Analytics] datos en Adobe Systems publicidad

Proporcione al implementación equipo de publicidad Adobe Systems lo siguiente:

* El [!DNL Analytics] ID del grupo de informes utilizar para la sistema de informes en medios de pago actividad y para alimentar el sitio actividad para la optimización y el sistema de informes en Adobe Systems Advertising
* El compañía Experience Cloud identificador de organización (identificador de organización).

Puede encontrar ambos ID en la [pestaña de resumen de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud pantalla Resumen del depurador](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Datos en Adobe Systems publicidad {#lookback-a4adc}

Dado que [!DNL Analytics] los datos se envían a Adobe Systems Advertising para sistema de informes y optimización, los datos están sujetos a las reglas de atribución, incluidas las ventanas retrospectiva de impresión y clic, que están configuradas para el anunciante en Adobe Systems Advertising.

![Configuración de la ventana retrospectiva de nivel anunciante en Adobe Systems Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Systems Ventana retrospectiva de clics de Advertising atribución: Número de días después de que se produce el primer clic en los que el clic puede atribuirse a un Conversión. De forma predeterminada, este valor es de 60 días; El máximo es de 90 días
* Adobe Systems Ventana retrospectiva de atribución impresión publicidad: Número de días después de ocurrir un impresión de anuncios en los que el impresión puede atribuirse a un Conversión. De forma predeterminada, este valor es 14 días; El máximo es de 30 días

  >[!NOTE]
  >
  > La ventana retrospectiva impresión es específica de Adobe Systems Publicidad, no [!DNL Analytics for Advertising]de , sistema de informes.

El [!DNL Analytics for Advertising] JavaScript utiliza esta configuración para determinar el grado de antigüedad que debe considerarse válida una entrada de vista o una entrada de clics al sitio. Para obtener más información sobre cómo se determinan las vista pulsaciones y las pulsaciones, consulte &quot;[Adobe Systems ID de publicidad utilizados por Analytics](ids.md)&quot;.

## Adobe Systems datos publicitarios en [!DNL Analytics]

[!DNL Analytics] establece Adobe Systems ID de publicidad (AMO ID) dentro del Analytics Visita, sujeto a la configuración de persistencia del [!DNL eVar] anunciante, que se aplica tanto a las pulsaciones como a las vista. La opción de persistencia se configura en el back-end de publicidad de Adobe Systems y el equipo de cuentas de Adobe Systems puede cambiarla.

* [!DNL Analytics for Advertising][!DNL eVar] caducidad: 60 días de forma predeterminada para los ID de AMO

>[!NOTE]
>
>Para segmento datos de un periodo de tiempo diferente, puede [configurar segmentos personalizados con diferentes ventanas retrospectivas dentro de](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace.

## Entornos publicitarios admitidos

* Buscar
* Monitor
* Vídeo
* Vídeo en línea
* Conectado TV
* Nativo

Póngase en contacto con su equipo de Adobe Systems cuentas para obtener información sobre los entornos anuncios compatibles más recientes en cada canal.

## Aspectos importantes antes de una implementación

* El implementación equipo Adobe Systems Advertising configura la integración.

* No se facturan costes adicionales por esta integración, ni las llamadas al servidor dan lugar a tarifas de publicidad adicionales [!DNL Analytics] o Adobe Systems.

* [!DNL Analytics for Advertising] es independiente del servidor de anuncios: puede producirse una pulsación o vista desde cualquier servidor de anuncios, y las ID adecuadas se generan al ingresar al sitio.

* La integración solo [!DNL Analytics] pasa eventos estándar y personalizados a Adobe Systems Advertising para oferta optimización de los medios de pago y los esfuerzos publicitarios posteriores. No pasa [!DNL Analytics] segmentos, métricas calculadas y [!DNL eVars] Adobe Systems publicidad para oferta optimización.

* Adobe Systems Publicidad crea ID persistentes en [!DNL Analytics] función del último anuncio en el que se hizo clic o se vio antes de que el usuario ingrese al sitio, en función de las [ventanas](#lookback-a4adc) retrospectivas de clic y vista configuradas en Adobe Systems Publicidad. Si una visitante del sitio tiene ambos tipos de interacciones de entrada de sitio dentro de su perfil, y el clic está dentro del período de retroactividad, entonces el ID de pulsación del visitante anula el ID de vista para el sistema de informes del sitio.

* [!DNL Analytics for Advertising] Conversión seguimiento en Adobe Analytics usa una ventana retroactiva de seguimiento configurable (60 días de forma predeterminada). Adobe Systems informes de publicidad reflejan las conversiones y el participación del sitio hasta el final de esta ventana retrospectiva de seguimiento.

* Se admiten todos los tipos de anuncios. Sin embargo, no todos los entornos anuncios son compatibles.

* [!DNL Analytics] Actualmente, las conversiones se rastrean y atribuyen únicamente a un visitante del mismo dispositivos.

* [!DNL Analytics for Advertising] no admite conversiones en vista a través de la aplicación.

* Ver no admite seguimiento de transferencia para anunciantes que utilicen una implementación de reenvío de del lado del servidor de [!DNL Analytics].

### ID suplementario

Una vez que el servicio de identidad de Experience Cloud se ha implementado para un sitio, las visitas que contienen datos de [!DNL Analytics] o Adobe Systems publicidad contienen un ID suplementario.

Ejemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para una integración de datos precisa, todas las llamadas publicitarias Adobe Systems utilizadas por una [!DNL Analytics for Advertising] actividad para entregar contenido o registrar el Métrica objetivo deben tener un Visita correspondiente [!DNL Analytics] que comparta el mismo ID suplementario.

Cuando esté solucionando problemas en [!DNL Analytics], asegúrese de que el ID suplementario esté presente para [!DNL Analytics] las visitas. En Adobe Experience Cloud [Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), puede ver este ID en el pestaña de publicidad Adobe Systems como `sdid` parámetro.

>[!NOTE]
>
> Este implementación funciona de manera similar a la [!DNL Analytics for Target] integración.

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript Code para Analytics de publicidad](/help/integrations/analytics/javascript.md)
