---
title: DSP Macros de Advertising
description: Haga referencia a las macros disponibles para el seguimiento general y para rastrear clics en anuncios en pantalla de terceros.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# DSP Macros de Advertising

Una macro es un comando corto o un método abreviado para una instrucción y suele seguir el formato `${MACRO_NAME}`. Las macros incluidas en el código creativo o en las URL de pulsaciones se expanden a una cadena de código más larga que el servidor de publicidad puede comprender. DSP El servidor de publicidad ejecuta macros cuando se sirve el anuncio o se hace clic en él.

DSP Las macros de servidor de publicidad son útiles para pasar información importante a servidores de publicidad de terceros o a servidores de publicidad de terceros. Las macros se utilizan principalmente durante el tráfico de código creativo o metadatos de terceros y personalizados (como los píxeles de terceros).

DSP Puede insertar manualmente una macro en cualquier lugar, como en una etiqueta VAST, en cualquier dirección URL, o en un píxel de evento de terceros o de un grupo de datos de la lista de permitidos. DSP Sin embargo, cada cliente y socio de la tiene un formato de etiqueta de anuncio diferente, y las macros deben insertarse en diferentes puntos de la etiqueta en consecuencia. DSP Cada vez que trabaje con un cliente o socio nuevo, pídale documentación sobre dónde insertar las macros en sus etiquetas publicitarias que comercializa el tráfico de la.

## Macros de seguimiento generales

Utilice macros de seguimiento generales en todos los tipos de publicidad y etiquetas para devolver datos específicos, según sea necesario.

| Macro | Descripción de reemplazo | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | ID de la cuenta. | entero |
| `${TM_AD_ID}` | La clave del anuncio (adKey). | cadena |
| `${TM_AD_ID_NUM}` | ID del anuncio. | entero |
| `${TM_ADVERTISER_ID}` | El ID del anunciante. | entero |
| `${TM_CAMPAIGN_ID}` | La clave de campaña. | cadena |
| `${TM_CAMPAIGN_ID_NUM}` | El ID de campaña. | entero |
| ` ${TM_CLICK_URL}` | La dirección URL de redireccionamiento, que permite a los servidores de publicidad rastrear y contar clics de publicidad. Cuando se publica el anuncio, si el usuario hace clic en él, la macro se activa y el clic se registra y se cuenta para la creación de informes. | cadena |
| ` ${TM_CLICK_URL_URLENC}` | La URL de redireccionamiento codificada, que permite a los servidores de publicidad rastrear y contar los clics de publicidad. Cuando se publica el anuncio, si el usuario hace clic en él, la macro se activa y el clic se registra y se cuenta para la creación de informes. No utilice esta macro a menos que esté creando anuncios de terceros y el proveedor requiera la codificación de la dirección URL. | cadena |
| `${TM_FEED_ID}` | La clave para la ubicación de los medios (feedKey). | cadena |
| `${TM_FEED_ID_NUM}` | El ID de la ubicación de los medios. | entero |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | La clave del sitio para la ubicación. Necesario para [!DNL AppsFlyer] rastreadores de clics para anuncios de instalación de aplicaciones móviles.<!-- should map to placement_site_key column of placement_site table --> | cadena |
| `${TM_PLACEMENT_ID}` | La clave de ubicación (cpKey). | cadena |
| `${TM_PLACEMENT_ID_NUM}` | ID de ubicación. | entero |
| `${TM_RANDOM}` | Cachebuster: un número aleatorio entre 1 y 1000000. | largo |
| `${TM_SESSION_ID}` | El ID de la sesión, que corresponde a una sola recuperación de la etiqueta de publicidad. | cadena |
| `${TM_SITE_DOMAIN_URLENC}` | Subdominio de página analizado desde la dirección URL en la solicitud de oferta; con codificación URL. No es compatible con los anuncios en banner con clic para reproducir. | cadena |
| ` ${TM_SITE_NAME}` | El nombre del sitio para la ubicación. | cadena |
| `${TM_SITE_URL_URLENC}` | La URL pasada en la solicitud de oferta; codificada con la URL. No es compatible con los anuncios en banner con clic para reproducir. | cadena |
| `${TM_SITE_ID_NUM}` | ID del sitio para la ubicación. | entero |
| `${TM_TIMESTAMP}` | La marca de tiempo Unix que indica el número de segundos transcurridos desde la medianoche (00:00 UTC) del 1 de enero de 1970. | largo |
| ` ${TM_VIDEO_DURATION}` | Duración del vídeo de anuncio en segundos. | entero |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Macros específicas para móviles

| Macro | Descripción de reemplazo | Tipo |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) El ID de plataforma, que corresponde al sistema operativo del dispositivo:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` cuando la plataforma no es ninguna de las anteriores</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) El nombre del modelo del dispositivo, con codificación URL. | cadena |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) Entorno en el que se publicó el anuncio:<ul><li>`a` = aplicación móvil</li><li>`b` = sitio web móvil</li></ul> | cadena (`a` o `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) El ID de plataforma, que corresponde al sistema operativo del dispositivo:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` cuando la plataforma no es ninguna de las anteriores</li></ul> | cadena |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) El tipo de dispositivo en el que se visualizó el anuncio:<ul><li>`TAB` = tableta</li><li>`PHN` = mobile</li><li>`computer` = equipo</li></ul> | cadena |
| `${UOO}` | ([!DNL Nielsen]) Indica si el usuario ha optado por no participar en el seguimiento de anuncios:<ul><li>`1` (indicador DNT = 1) = el usuario ha excluido el seguimiento de anuncios</li><li>`0` (indicador DNT = 0) = el usuario ha elegido el seguimiento de anuncios</li></ul> | entero (`0` o `1`) |
| `${TM_BUNDLE}` | El [!DNL iOS] o [!DNL Android] ID de paquete de App Store. Ejemplos: com.zynga.wwf2.free o id804379658 | cadena |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indica si el postor determina que la solicitud de oferta proviene del origen de la Unión Europea y requiere el cumplimiento del RGPD:<ul><li>`1` = RGPD debe aplicarse</li><li>`0` = No se debe aplicar el RGPD</li></ul>`gdpr_consent=${GDPR_CONSENT}` es el valor de consentimiento pasado desde el socio de suministro en la solicitud de oferta entrante:<ul><li>En la mayoría de los casos, se trata de una cadena de consentimiento codificada en base64url o daisybit (ejemplo: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = sin consentimiento</li><li>`1` = consentimiento</li></ul> | daisybit o entero |

{style="table-layout:auto"}

## Haga clic en Macros para anuncios en pantalla de terceros

DSP Para rastrear con precisión los clics de anuncios mediante etiquetas de visualización de terceros, se requiere una macro de clic en pantalla. Solo se requiere una versión de la macro; la macro correspondiente depende del tipo de etiqueta.

| Macro | Descripción de reemplazo | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | Dirección URL de redireccionamiento que permite a los servidores de publicidad realizar un seguimiento y contar los clics de publicidad en la plataforma. | cadena |
| `${TM_CLICK_URL_URLENC}` | La URL de redireccionamiento que habilita los servidores de publicidad que requieren codificación de URL para rastrear y contar clics de publicidad en la plataforma. | cadena |

{style="table-layout:auto"}

DSP La aplicación inserta automáticamente macros de clic de visualización en una etiqueta de visualización de terceros cuando:

* Exportación de etiquetas de publicidad desde un socio de servidor de publicidad <!-- [Needs PM confirmation.] -->
* Carga masiva [!DNL Flashtalking] o [!DNL Google DoubleClick for Advertisers] DSP Etiquetas de publicidad directamente en el

DSP Si falta una macro de clic al generar un anuncio de visualización, muestra un mensaje de advertencia, que le pedirá que inserte manualmente la macro de clic de visualización adecuada en el área correcta de la etiqueta.

## Solucionar problemas de errores de macros

Cuando agregue macros al código, asegúrese de utilizar la sintaxis exacta de la macro. DSP Al validar las macros, comprueba que la macro coincida exactamente con una de las macros válidas.

Los errores se generan si faltan caracteres desde el principio o el final del nombre de la macro. Por ejemplo, verá un mensaje de error si:

* Se olvidan uno o más caracteres al principio del nombre de la macro, como `${`. Si no se incluye la sintaxis completa, la entrada no se reconoce como una macro válida.
* La macro no termina con un conjunto de caracteres válido, como `}`.

>[!MORELIKETHIS]
>
>* [Configuración de anuncios de audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Configuración de anuncios de TV conectados](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Configuración de anuncio de visualización](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Configuración de publicidad móvil](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Configuración de publicidad nativa](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Configuración de anuncio previo a la emisión](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Configuración de anuncio de vídeo universal](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

