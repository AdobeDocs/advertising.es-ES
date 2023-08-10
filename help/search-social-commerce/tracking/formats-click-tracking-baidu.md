---
title: Formatos de rastreo de clics para [!DNL Baidu]
description: Obtenga información acerca de los formatos de seguimiento de clics para [!DNL Baidu] cuentas.
exl-id: a57ff0cf-0bcf-4d55-9a86-7551db8a08e7
feature: Search Tracking
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Formatos de rastreo de clics para anuncios patrocinados en [!DNL Baidu]

El siguiente formato de URL de destino base se aplica a los anuncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante dentro de Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si el paso de tokens está deshabilitado, sustituya `cq?` después `<advertiser_ID>` con `c?`.
>
>* `<campaignID>` es una variable para el ID de campaña numérico.
>
>* `<the landing page>` es una variable que representa la dirección URL del sitio a la que se dirige a los usuarios finales.

>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos para el código de seguimiento de ID de AMO](skwcid-tracking-parameter.md)
