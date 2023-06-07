---
title: Formatos de rastreo de clics para [!DNL Yahoo! Japan Ads]
description: Obtenga información acerca de los formatos de seguimiento de clics para [!DNL Yahoo! Japan Ads] cuentas.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Formatos de rastreo de clics para anuncios patrocinados en [!DNL Yahoo! Japan Ads]

Los siguientes formatos de plantilla de seguimiento de base se aplican a los anuncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

o, cuando la opción de etiquetado automático está establecida para la cuenta en [!DNL Yahoo! Japan Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante dentro de la publicidad de Adobe.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si el paso de tokens está deshabilitado, sustituya `cq?` después `<advertiser_ID>` con `c?`.
>
>* `<the landing page>` es una variable que representa la dirección URL del sitio a la que se dirige a los usuarios finales.


>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversiones de Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos para el código de seguimiento s\_kwcid](skwcid-tracking-parameter.md)
