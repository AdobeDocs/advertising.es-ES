---
title: '[!DNL Google Ads] configuración de anuncios de solo llamada'
description: Hacer referencia a la configuración de  [!DNL Google Ads] anuncios de solo llamada.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads] configuración de anuncios de solo llamada

Puede crear anuncios de texto solo de llamada para campañas que utilicen la red de búsqueda.

Search, Social y Commerce rastrean los anuncios de solo llamada usando el sufijo de página de aterrizaje de nivel de cuenta y la plantilla de seguimiento, pero también puede anular el seguimiento de nivel de cuenta en el nivel de anuncio dentro del Administrador de [!DNL Google Ads].

Consulte la ayuda de [!DNL Google Ads] para [límites de anuncios por cuenta](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** El nombre de la empresa. La longitud máxima es de 25 caracteres o 12 caracteres de doble byte.

**[!UICONTROL Country]:** (opcional) país en el que se encuentra la empresa.

**[!UICONTROL Phone Number]:** Número de teléfono de la empresa. Ejemplos: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** Primera y segunda línea del cuerpo del anuncio. La longitud máxima de cada línea es de 35 caracteres o 17 caracteres de doble byte.

La sintaxis de sustitución de palabras clave no cuenta para la longitud máxima. Por ejemplo, &quot;`{Description1: Free Account Analysis!}`&quot; se trata como 22 caracteres (solo la parte &quot;Análisis de cuenta gratuito\!&quot;).

>[!NOTE]
>
>Los campos de descripción no pueden incluir números de teléfono.

**[!UICONTROL Display URL]:** Dirección URL mostrada en el anuncio. La dirección URL para mostrar debe coincidir con un dominio asociado con su empresa, pero el anuncio no envía personas a una página de aterrizaje.

La longitud máxima es de 35 caracteres de un byte o 17 caracteres de doble byte. La sintaxis de sustitución de palabras clave no cuenta para la longitud máxima. Por ejemplo, &quot;`{DisplayURL: example.com}`&quot; se trata como 11 caracteres (solo la parte &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (opcional) una página web en la que el número de teléfono de su anuncio aparece como texto para que [!DNL Google Ads] pueda comprobar que el número de teléfono es válido. Debe tener el mismo dominio que la dirección URL para mostrar del anuncio.

**[!UICONTROL Is Tracked]:** Habilita el seguimiento de llamadas y las conversiones de solo llamada.

**[!UICONTROL Count calls as phone call conversions]:** (cuando se selecciona &quot;[!UICONTROL Is Tracked]&quot;; opcional) Atribuye todas las llamadas resultantes del anuncio a un tipo específico de conversión de llamada telefónica, cuando se especifica una. De lo contrario, [!DNL Google Ads] crea una acción de conversión predeterminada llamada &quot;[!UICONTROL Calls from ads]&quot; una vez que registra al menos una conversión de los números de reenvío y, a continuación, le atribuye las llamadas.

**[!UICONTROL Count Action]:** (cuando se selecciona &quot;[!UICONTROL Count calls as phone call conversions]&quot;; opcional) La acción de conversión existente a la que se atribuyen las llamadas.

Puede crear y administrar acciones de conversión en [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Acerca de los anuncios](ad-about.md)
>* [Administrar anuncios](ad-manage.md)
>* [[!DNL Google Ads] configuración de anuncios dinámicos de búsqueda expandida](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] configuración del anuncio de búsqueda adaptable](ad-settings-google-rsa.md)
