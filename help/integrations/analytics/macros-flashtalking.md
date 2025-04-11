---
title: Anexar  [!DNL Analytics for Advertising] macros a [!DNL Flashtalking] etiquetas de publicidad
description: Aprenda por qué y cómo agregar  [!DNL Analytics for Advertising] macros a sus [!DNL Flashtalking] etiquetas de publicidad
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: e8c8316418acf4a8c62beabcae2c1b7388dbc297
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising] macros a [!DNL Flashtalking] etiquetas de publicidad

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

*Sólo* organizaciones sin una asociación directa con [!DNL Flashtalking]

*Aplicable solo a Advertising DSP*

Si usa etiquetas de anuncio de [!DNL Flashtalking] para sus anuncios de Advertising DSP, debe anexar parámetros de seguimiento a las direcciones URL de la página de aterrizaje. Para usar la asociación de Advertising DSP con [!DNL Flashtalking], añada parámetros de Analytics para Advertising a las direcciones URL de la página de aterrizaje. Los parámetros registran el identificador de AMO (`s_kwcid`) y `ef_id` parámetros de cadena de consulta en la dirección URL de la página de aterrizaje, lo que permite que Adobe Advertising envíe datos de clics para los anuncios a Adobe Analytics.

>[!NOTE]
>
>Si su organización tiene una asociación directa con [!DNL Flashtalking], no necesita este procedimiento. En su lugar, inicie sesión en su cuenta de [!DNL Flashtalking] y siga la documentación de soporte técnico de [!DNL Flashtalking] para recopilar datos de clics mediante macros de transferencia de datos en `https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`.

Utilice macros para [!DNL Flashtalking] anuncios de vídeo y visualización para los siguientes tipos de implementaciones de [!DNL Analytics for Advertising]:

* **Anunciantes con el código JavaScript [!DNL Adobe] [!DNL Analytics for Advertising] implementado en sus sitios web**: El código JavaScript ya registra los parámetros de cadena de consulta del identificador de AMO (`s_kwcid`) y `ef_id`. Sin embargo, el uso de macros amplía el seguimiento para incluir conversiones basadas en clics cuando no se admiten cookies de terceros. La práctica recomendada es añadir las macros de las secciones siguientes a las etiquetas de publicidad para capturar datos de clics adicionales que no se capturan mediante el código JavaScript.

  >[!NOTE]
  >
  >El código JavaScript es una solución para el rastreo de clics solo mientras las cookies sigan disponibles. Una vez interrumpidas las cookies, será necesario implementar las siguientes macros.

* **Anunciantes cuyos sitios web no usan el código JavaScript [!DNL Analytics for Advertising] y dependen del reenvío del lado del servidor [!DNL Analytics] solo para datos de clics** (sin datos de visualizaciones): Se requieren las siguientes macros para informar sobre la actividad de clics en el sitio provocada por los anuncios que compras a través de Adobe Advertising.

## Mostrar etiquetas de publicidad

En la configuración de etiquetas de publicidad de [!DNL Flashtalking], anexe la siguiente macro al final de la URL de pulsación en el campo `Clicktag`:

```
[ftqs:[AdobeAMO]]
```

Si es la primera o la única cadena de consulta después de la dirección URL base, sepárela con un `?`. Si la dirección URL base incluye varias cadenas de consulta, comience la primera cadena con `?` y cada cadena posterior con `&`.

Ejemplos:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Etiquetas de anuncios de vídeo

En la configuración de etiquetas de publicidad de [!DNL Flashtalking], anexe la siguiente macro al final de la URL de pulsación en el campo `Clicktag`:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Si es la primera o la única cadena de consulta después de la dirección URL base, sepárela con un `?`. Si la dirección URL base incluye varias cadenas de consulta, comience la primera cadena con `?` y cada cadena posterior con `&`.

Ejemplos:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [ID de Adobe Advertising usados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anexar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md)

