---
title: Formatos de rastreo de clics para  [!DNL LY Ads]
description: Obtenga información acerca de los formatos de seguimiento de clics para  [!DNL LY Ads] cuentas.
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ZFNzA0bfxKhlNW6fvPWMwBc4naT7rOhvym-wSpxvYXg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 0%

---

# Formatos de rastreo de clics para anuncios patrocinados en [!DNL LY Ads]

Los siguientes formatos de plantilla de seguimiento de base se aplican a los anuncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

o bien, cuando la opción de etiquetado automático está establecida para la cuenta en [!DNL LY Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante en Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si la transferencia de tokens está deshabilitada, sustituya `cq?` después de `<advertiser_ID>` por `c?`.
>
>* `<the landing page>` es una variable que representa la dirección URL del sitio a la que se dirige a los usuarios finales.

>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID de AMO](https://experienceleague.adobe.com/es/docs/analytics/components/dimensions/amo-id#dimension-items)
