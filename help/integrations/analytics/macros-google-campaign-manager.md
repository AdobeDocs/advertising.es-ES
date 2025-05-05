---
title: Anexar  [!DNL Analytics for Advertising] macros a [!DNL Google Campaign Manager 360] etiquetas de publicidad
description: Aprenda por qué y cómo agregar  [!DNL Analytics for Advertising] macros a sus [!DNL Google Campaign Manager 360] etiquetas de publicidad
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising] macros a [!DNL Google Campaign Manager 360] etiquetas de publicidad

*Solo anunciantes con una integración de Adobe Analytics de Adobe Advertising*

*Aplicable solo a Advertising DSP*

Si usa las etiquetas de anuncio de [!DNL Google Campaign Manager 360] para sus anuncios de Advertising DSP, anexe [!DNL Analytics for Advertising] parámetros a las direcciones URL de la página de aterrizaje mediante la macro [`%p` ](https://support.google.com/campaignmanager/table/6096962). Los parámetros registran el identificador de AMO (`s_kwcid`) y `ef_id` parámetros de cadena de consulta en la dirección URL de la página de aterrizaje, lo que permite que el Adobe Advertising envíe datos de clics para los anuncios a Adobe Analytics.

Utilice macros para [!DNL Campaign Manager 360] anuncios de vídeo y visualización para los siguientes tipos de implementaciones de [!DNL Analytics for Advertising]:

* **Anunciantes con el código JavaScript [!DNL Adobe] [!DNL Analytics for Advertising] implementado en sus sitios web**: El código JavaScript ya registra los parámetros de cadena de consulta del identificador de AMO (`s_kwcid`) y `ef_id`. Sin embargo, el uso de macros amplía el seguimiento para incluir conversiones basadas en clics cuando no se admiten cookies de terceros. La práctica recomendada es añadir las macros de las secciones siguientes a las etiquetas de publicidad para capturar datos de clics adicionales que no se capturan mediante el código JavaScript.

>[!NOTE]
>
>El código JavaScript es una solución para el rastreo de clics solo mientras las cookies sigan disponibles. Una vez interrumpidas las cookies, será necesario implementar las siguientes macros.

* **Anunciantes cuyos sitios web no usan el código JavaScript de [!DNL Analytics for Advertising] y dependen del reenvío del lado del servidor de [!DNL Analytics] solo para datos de clics** (sin datos de visualizaciones): Se requieren las siguientes macros para informar de la actividad de clics en el sitio a partir de anuncios que se compran a través del Adobe Advertising.

## Anexar las macros a los anuncios de [!DNL Google Campaign Manager 360]

En [!DNL Google Campaign Manager 360], anexe el siguiente parámetro a la dirección URL de la página de aterrizaje para cada uno de los anuncios de vídeo y visualización: `%pamo=!;`

Puede especificar la dirección URL de la página de aterrizaje de varias formas. Las instrucciones para cada opción se incluyen en las siguientes subsecciones.

A continuación se muestra un ejemplo de la dirección URL de la página de aterrizaje con el sufijo formateado.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* Si la dirección URL de la página de aterrizaje incluye el símbolo hash (#), que no es común, coloque el parámetro `amo` antes del símbolo hash.
>* Si no se incluyen otros parámetros después del parámetro `amo`, agregue un parámetro (por ejemplo, &amp;a=b) después de él. Ejemplo: `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configurar el sufijo de URL de la página de aterrizaje de nivel del anunciante

1. Vea las [instrucciones para abrir las propiedades del anunciante](https://support.google.com/campaignmanager/answer/2829344).
1. En la configuración de [!UICONTROL Landing page URL suffix], incluya `%pamo!;` en el campo [!UICONTROL URL suffix].

### Configuración del sufijo de URL de la página de aterrizaje de nivel de campaña

1. Vea las [instrucciones para abrir las propiedades de la campaña](https://support.google.com/campaignmanager/answer/2838056#set).
1. En la configuración de [!UICONTROL Landing page URL suffix], incluya `%pamo!;` en el campo [!UICONTROL URL suffix].

### Configurar el sufijo de URL de la página de aterrizaje de nivel creativo

1. Abra las propiedades creativas.
1. En la configuración [!UICONTROL Click tags], incluya `%pamo!;` en la columna [!UICONTROL Landing page] para la etiqueta de clic.

## DSP Cómo se expanden las macros [!DNL Analytics for Advertising] en la vista de datos de

DSP En el caso de que cree un anuncio que incluya el parámetro [!DNL Analytics for Advertising] (`amo`), las macros `ef_id` y `s_kwcid` se anexan automáticamente a la dirección URL de clic. DSP La práctica recomendada es comprobar la etiqueta en el código de tiempo para asegurarse de que las macros `ef_id` y `s_kwcid` están presentes.

DSP A continuación se muestra un ejemplo de una etiqueta [!DNL Google Campaign Manager 360] [ins](https://support.google.com/campaignmanager/answer/6080468) tal como aparece en el cuadro de diálogo de la interfaz de usuario de &lbrace;2000100000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000

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

Cuando un usuario hace clic en el anuncio, [!DNL Google Campaign Manager 360] ve `%pamo` en el sufijo de la dirección URL e inserta dinámicamente el valor del parámetro `amo` en la dirección URL.

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [ID de Adobe Advertising usados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad](macros-flashtalking.md)
