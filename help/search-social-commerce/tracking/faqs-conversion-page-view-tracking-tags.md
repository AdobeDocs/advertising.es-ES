---
title: Preguntas frecuentes sobre las etiquetas de conversión de publicidad de Adobe y seguimiento de vista de página
description: Consulte una comparación de las Adobes de conversión de publicidad y las etiquetas de seguimiento de vista de página.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Preguntas frecuentes sobre las etiquetas de conversión de publicidad de Adobe y seguimiento de vista de página

Lo siguiente se aplica a las etiquetas de seguimiento de conversión de Adobe Advertising y a las etiquetas de seguimiento de vista de página.

|  | Etiquetas JS con ECID | Etiquetas de JS versión 3 | Etiquetas de JS versión 2 | Etiquetas de imagen |
| ---- | ---- | ---- | ---- | ---- |
| Se puede utilizar en la misma página web que otra versión de JS | — | — | — | n/a |
| Permite el uso de varias etiquetas con los mismos ID de usuario del anunciante en la misma página web | Sí | Sí | Sí | — |
| Permite el uso de varias etiquetas con distintos ID de usuario de anunciante en la misma página web | Sí | Sí | No | No |
| Utilizado por la extensión de publicidad de Adobe para Adobe Experience Platform y compatible con otras etiquetas generadas mediante Experience Platform | Sí | Sí | — | — |
| Permite todas las conversiones que se originan en [!DNL Apple Safari] y [!DNL Mozilla Firefox] que se debe rastrear cuando se utiliza con la etiqueta de asignación de conversión JavaScript de Adobe Advertising | Sí | Sí | Sí | — |

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
>* [Generación de una etiqueta de conversión de publicidad de Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato de las etiquetas de seguimiento de conversión de imagen](/help/search-social-commerce/tracking/format-conversion-tag-image.md)


<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
