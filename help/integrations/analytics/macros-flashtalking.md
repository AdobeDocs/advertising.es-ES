---
title: Añadir [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad
description: Descubra por qué y cómo añadir [!DNL Analytics for Advertising] macros a su [!DNL Flashtalking] etiquetas de publicidad
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Añadir [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad

*Anunciantes con solo integración de Adobe Advertising-Adobe Analytics*

*DSP Aplicable solo a Advertising*

Si usa las etiquetas de anuncio de [!DNL Flashtalking] DSP para los anuncios de Advertising, añada parámetros de Analytics para Advertising a las direcciones URL de la página de aterrizaje. Los parámetros registran el ID de AMO (`s_kwcid`) y `ef_id` parámetros de cadena de consulta en la dirección URL de la página de aterrizaje, lo que permite al Adobe Advertising enviar datos de clics para los anuncios a Adobe Analytics.

Uso de macros para [!DNL Flashtalking] anuncios de vídeo y visualización para los siguientes tipos de [!DNL Analytics for Advertising] implementaciones:

* **Anunciantes con el [!DNL Adobe] [!DNL Analytics for Advertising] Código JavaScript implementado en sus sitios web**: el código JavaScript ya registra el ID de AMO (`s_kwcid`) y `ef_id` parámetros de cadena de consulta. Sin embargo, el uso de macros amplía el seguimiento para incluir conversiones basadas en clics cuando no se admiten cookies de terceros. La práctica recomendada es añadir las macros de las secciones siguientes a las etiquetas de publicidad para capturar datos de clics adicionales que no se capturan mediante el código JavaScript.

>[!NOTE]
>
>El código JavaScript es una solución para el rastreo de clics solo mientras las cookies sigan disponibles. Una vez interrumpidas las cookies, será necesario implementar las siguientes macros.

* **Anunciantes cuyos sitios web no utilizan [!DNL Analytics for Advertising] Código JavaScript y, en su lugar, confíe en [!DNL Analytics] reenvío del lado del servidor solo para datos de pulsaciones** (sin datos de visualizaciones): Se requieren las siguientes macros para informar de la actividad de clics en el sitio impulsada por anuncios que compra mediante Adobe Advertising.

## Mostrar etiquetas de publicidad

Dentro de [!DNL Flashtalking] Para agregar la configuración de etiqueta, anexe la siguiente macro al final de la URL de pulsación en la `Clicktag` campo:

```html
?[ftqs:[AdobeAMO]]
```

Ejemplo:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## Etiquetas de anuncios de vídeo

Dentro de [!DNL Flashtalking] Para agregar la configuración de etiqueta, anexe la siguiente macro al final de la URL de pulsación en la `Clicktag` campo:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Ejemplo:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [ID de Adobe Advertising utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Añadir [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md)
