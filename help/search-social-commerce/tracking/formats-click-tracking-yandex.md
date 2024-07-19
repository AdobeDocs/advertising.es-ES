---
title: Formatos de rastreo de clics para  [!DNL Yandex]
description: Obtenga información acerca de los formatos de seguimiento de clics para  [!DNL Yandex] cuentas.
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Formatos de rastreo de clics para anuncios patrocinados en [!DNL Yandex]

El siguiente formato de URL de destino base se aplica a los anuncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Ejemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` es una variable para el ID único del anunciante dentro del Adobe Advertising.
>
>* Este formato indica que la transferencia de tokens está habilitada para la campaña (el valor predeterminado). Si la transferencia de tokens está deshabilitada, sustituya `cq?` después de `<advertiser_ID>` por `c?`.
>
>* `<the landing page>` es una variable que representa la dirección URL del sitio a la que se dirige a los usuarios finales.
>
>* `source_type` es el tipo de coincidencia.
>
>* `source` indica si el anuncio se mostró en un sitio basado en contenido o en búsqueda.
>
>* `position` es el número de posición del anuncio en el bloque. Para el tráfico que no es de búsqueda, el valor es &quot;0&quot;.
>
>* `position_type` es el bloque en el cual se mostró el anuncio el [!DNL Yandex]. Valores posibles: &quot;premium&quot; (bloque superior), &quot;other&quot; (bloque derecho) o &quot;none&quot; (tráfico que no sea de búsqueda).

>[!MORELIKETHIS]
>
>* [Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID de AMO](/help/integrations/analytics/ids.md#amo-id-formats)
