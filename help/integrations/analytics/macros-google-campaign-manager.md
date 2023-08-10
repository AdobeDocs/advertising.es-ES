---
title: Añadir [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad
description: Descubra por qué y cómo añadir [!DNL Analytics for Advertising] macros a su [!DNL Google Campaign Manager 360] etiquetas de publicidad
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 703cda43e96dfa9d80bbce2d64192fc461d5dbae
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Añadir [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad

*Anunciantes con solo integración de Adobe Advertising-Adobe Analytics*

*DSP Aplicable solo a Advertising*

Si usa las etiquetas de anuncio de [!DNL Google Campaign Manager 360] DSP para sus anuncios de Advertising, añada [!DNL Analytics for Advertising] parámetros a las direcciones URL de la página de aterrizaje usando [`%p` macro](https://support.google.com/campaignmanager/table/6096962). Los parámetros registran el ID de AMO (`s_kwcid`) y `ef_id` parámetros de cadena de consulta en la dirección URL de la página de aterrizaje, lo que permite al Adobe Advertising enviar datos de clics para los anuncios a Adobe Analytics.

Uso de macros para [!DNL Campaign Manager 360] anuncios de vídeo y visualización para los siguientes tipos de [!DNL Analytics for Advertising] implementaciones:

* **Anunciantes con el [!DNL Adobe] [!DNL Analytics for Advertising] Código JavaScript implementado en sus sitios web**: el código JavaScript ya registra el ID de AMO (`s_kwcid`) y `ef_id` parámetros de cadena de consulta. Sin embargo, el uso de macros amplía el seguimiento para incluir conversiones basadas en clics cuando no se admiten cookies de terceros. La práctica recomendada es añadir las macros de las secciones siguientes a las etiquetas de publicidad para capturar datos de clics adicionales que no se capturan mediante el código JavaScript.

>[!NOTE]
>
>El código JavaScript es una solución para el rastreo de clics solo mientras las cookies sigan disponibles. Una vez interrumpidas las cookies, será necesario implementar las siguientes macros.

* **Anunciantes cuyos sitios web no utilizan [!DNL Analytics for Advertising] Código JavaScript y, en su lugar, confíe en [!DNL Analytics] reenvío del lado del servidor solo para datos de pulsaciones** (sin datos de visualizaciones): Se requieren las siguientes macros para informar de la actividad de clics en el sitio impulsada por anuncios que compra mediante Adobe Advertising.

## Anexar las macros a su [!DNL Google Campaign Manager 360] Anuncios

En [!DNL Google Campaign Manager 360], añada el siguiente parámetro a la dirección URL de la página de aterrizaje para cada uno de los anuncios de vídeo y visualización: `%pamo=!;`

Puede especificar la dirección URL de la página de aterrizaje de varias formas. Las instrucciones para cada opción se incluyen en las siguientes subsecciones.

A continuación se muestra un ejemplo de la dirección URL de la página de aterrizaje con el sufijo formateado.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* Si la dirección URL de la página de aterrizaje incluye el símbolo hash (#), que no es común, coloque el `amo` antes del símbolo hash.
>* Si no se incluyen otros parámetros después de `amo` y después agregue un parámetro (por ejemplo, &amp;a=b). Ejemplo:`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configurar el sufijo de URL de la página de aterrizaje de nivel del anunciante

1. Consulte la [instrucciones para abrir las propiedades del anunciante](https://support.google.com/campaignmanager/answer/2829344).
1. En el [!UICONTROL Landing page URL suffix] configuración, incluir `%pamo!;` en el [!UICONTROL URL suffix] field.

### Configuración del sufijo de URL de la página de aterrizaje de nivel de campaña

1. Consulte la [instrucciones para abrir las propiedades de la campaña](https://support.google.com/campaignmanager/answer/2838056#set).
1. En el [!UICONTROL Landing page URL suffix] configuración, incluir `%pamo!;` en el [!UICONTROL URL suffix] field.

### Configurar el sufijo de URL de la página de aterrizaje de nivel creativo

1. Abra las propiedades creativas.
1. En el [!UICONTROL Click tags] configuración, incluir `%pamo!;` en el [!UICONTROL Landing page] para la etiqueta click.

## Cómo [!DNL Analytics for Advertising] DSP Las macros se expanden en la

DSP En, cuando crea un anuncio que incluye la variable [!DNL Analytics for Advertising] parámetro (`amo`), el `ef_id` y `s_kwcid` Las macros de se anexan automáticamente a la URL de clic. DSP La práctica recomendada es comprobar la etiqueta en para asegurarse de que la etiqueta de la etiqueta de la cuenta de usuario de la cuenta de usuario de la cuenta de correo electrónico de se ha guardado de forma correcta. `ef_id` y `s_kwcid` hay macros de.

El siguiente es un ejemplo de [!DNL Google Campaign Manager 360] [etiqueta ins](https://support.google.com/campaignmanager/answer/6080468) DSP tal como aparece en la lista de la.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

Cuando un usuario hace clic en el anuncio, [!DNL Google Campaign Manager 360] ve `%pamo` en el sufijo URL e inserta dinámicamente el valor del `amo` en la dirección URL.

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [ID de Adobe Advertising utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Añadir [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad](macros-flashtalking.md)
