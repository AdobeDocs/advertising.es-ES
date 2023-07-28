---
title: Preguntas frecuentes sobre la conversión de Adobe Advertising y las etiquetas de seguimiento de vista de página
description: Consulte una comparación de las etiquetas de conversión de Adobe Advertising y de seguimiento de vista de página.
exl-id: 5eb414a7-2f96-47de-b157-a17851653206
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Preguntas frecuentes sobre la conversión de Adobe Advertising y las etiquetas de seguimiento de vista de página

Lo siguiente se aplica a las etiquetas de seguimiento de conversión de Adobe Advertising y a las etiquetas de seguimiento de vista de página.

| | Etiquetas JS con ECID | Etiquetas de JS versión 3 | Etiquetas de JS versión 2 | Etiquetas de imagen |
| ---- | ---- | ---- | ---- | ---- |
| Se puede utilizar en la misma página web que otra versión de JS | — | — | — | n/a |
| Permite el uso de varias etiquetas con los mismos ID de usuario del anunciante en la misma página web | Sí | Sí | Sí | — |
| Permite el uso de varias etiquetas con distintos ID de usuario de anunciante en la misma página web | Sí | Sí | No | No |
| Lo utiliza la extensión de Adobe Advertising para Adobe Experience Platform y es compatible con otras etiquetas generadas mediante Experience Platform | Sí | Sí | — | — |
| Permite todas las conversiones que se originan en [!DNL Apple Safari] y [!DNL Mozilla Firefox] que se debe rastrear cuando se utiliza con la etiqueta de asignación de conversión de JavaScript de Adobe Advertising | Sí | Sí | Sí | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Todas las implementaciones nuevas utilizan JavaScript versión 3.
>* La etiqueta JavaScript con ECID utiliza el [Servicio de Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) así como el ef_id y el gsurferid heredados para medir las conversiones. Esta última etiqueta crea [cookies s_ecid del Experience Cloud de origen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) y proporciona una integración más estrecha con otros productos de Experience Cloud.
>* Utilice etiquetas JavaScript versión 2 solo cuando ya hayan sido implementadas en las páginas web del anunciante.
>* La práctica recomendada es utilizar etiquetas JavaScript en lugar de etiquetas de imagen a menos que el sitio tenga una política contra su uso.
>* Las etiquetas JavaScript son necesarias para los anunciantes que deseen segmentar audiencias creadas en Adobe Experience Cloud, en Adobe Audience Manager o publicadas en Adobe Experience Cloud desde Audience Manager o Adobe Analytics.

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generación de una etiqueta de conversión de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato de las etiquetas de seguimiento de conversión de imagen](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
