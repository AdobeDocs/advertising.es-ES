---
title: Formatos de rastreo de clics para [!DNL Yahoo! Display Network]
description: Obtenga información acerca de los formatos de seguimiento de clics para [!DNL Yahoo! Display Network] cuentas.
exl-id: 62ea592c-9138-4a8e-9616-c8f2475fea26
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Formatos de rastreo de clics para anuncios patrocinados en [!DNL Yahoo! Display Network]

El siguiente formato de URL de destino base se aplica a los anuncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante dentro de Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si el paso de tokens está deshabilitado, sustituya `cq?` después `<advertiser_ID>` con `c?`.
>
>* `<the landing page>` es una variable que representa la dirección URL del sitio a la que se dirige a los usuarios finales.

>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos para el código de seguimiento de ID de AMO](amo-id-tracking-parameter.md)
