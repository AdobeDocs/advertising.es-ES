---
title: Formatos de rastreo de clics para  [!DNL Yahoo DSP]
description: Obtenga información acerca de los formatos de seguimiento de clics para  [!DNL Yahoo DSP] cuentas.
exl-id: ee6642b3-fb84-4604-91cc-da1213835be8
feature: Search Tracking
TQID: https://experienceleague.adobe.com/sQo6hr3UHQwN9GgazCKv2ba-m4ZXf2ZrhdemCpbVYvU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# Formatos de rastreo de clics para anuncios patrocinados en [!DNL Yahoo DSP]

El siguiente formato de URL de destino base se aplica a los anuncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

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
>* [Formatos de ID de AMO](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
