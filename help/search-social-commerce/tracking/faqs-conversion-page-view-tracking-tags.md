---
title: Preguntas frecuentes sobre la conversión de Adobe Advertising y las etiquetas de seguimiento de vista de página
description: Consulte una comparación de las etiquetas de conversión de Adobe Advertising y de seguimiento de vista de página.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '309'
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
| Permite que se realice un seguimiento de todas las conversiones que se originan a partir de [!DNL Apple Safari] y [!DNL Mozilla Firefox] cuando se usan con la etiqueta de asignación de conversión JavaScript de Adobe Advertising | Sí | Sí | Sí | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Todas las implementaciones nuevas utilizan JavaScript versión 3.
>* La etiqueta JavaScript con ECID usa el [servicio Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html), así como el ef_id y el gsurferid heredados para medir las conversiones. Esta última etiqueta crea [cookies s_ecid de Experience Cloud de origen](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) y proporciona una integración más estrecha con otros productos de Experience Cloud.
>* Utilice las etiquetas de la versión 2 de JavaScript solo cuando ya hayan sido implementadas en las páginas web del anunciante.
>* La práctica recomendada es utilizar etiquetas de JavaScript en lugar de etiquetas de imagen a menos que el sitio tenga una política contra su uso.
>* Las etiquetas de JavaScript son necesarias para los anunciantes que deseen segmentar audiencias creadas en Adobe Experience Cloud, en Adobe Audience Manager o publicadas en Adobe Experience Cloud desde Audience Manager o Adobe Analytics.

>[!MORELIKETHIS]
>
>* [Acerca de las etiquetas de seguimiento de conversión de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generar una etiqueta de conversión de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato de etiquetas de seguimiento de conversión de imagen](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
