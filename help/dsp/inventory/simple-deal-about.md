---
title: Acerca de [!UICONTROL Simple Ad Serving]
description: Obtenga información acerca de [!UICONTROL Simple Ad Serving] ofertas que usan píxeles de seguimiento de eventos.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
TQID: https://experienceleague.adobe.com/w4KFePatd7CZ1xC8dd1CItl88-6myAZw8TuatHzHnRI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# Acerca de [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] proporciona informes y envíos de anuncios garantizados y sin decisión para un editor especificado y un tipo de anuncio único, con una única ubicación dedicada. Use [!DNL Simple Ad Serving] cuando su editor no pueda ejecutar su acuerdo a través de los ID de acuerdo. El editor gestiona todos los objetivos, el ritmo y el límite del presupuesto y la restricción de frecuencia. Ejecute estas ofertas a través de píxeles de seguimiento de eventos.

Con [!UICONTROL Simple Ad Serving], cada anuncio lo proporciona directamente el editor (servidor del sitio) y DSP proporciona un píxel de seguimiento de eventos para enviarlo al editor, que debe implementar el píxel y el tráfico para los anuncios de DSP. Según el tipo de inventario, los píxeles de evento miden los eventos de impresión, pulsaciones y reproducción de vídeo.

Están disponibles los siguientes tipos de anuncios:

* anuncio previo a la emisión estándar de escritorio
* anuncio previo a la emisión para tablet y mobile standard
* anuncio previo a la emisión estándar de TV conectado
* exhibición
* audio

Puede crear una oferta [!UICONTROL Simple Ad Serving] en la vista [!UICONTROL Inventory] > [!UICONTROL Deals]. DSP genera automáticamente una ubicación con el subtipo &quot;[!DNL Simple ad serving]&quot; para el anuncio. La ubicación se dirige al acuerdo, pero no permite un direccionamiento, presupuesto o límite de frecuencia adicionales. Solo puede editar algunos de los ajustes de la oferta, como el nombre de la oferta, el CPM, las impresiones y las fechas de vuelo.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

Las ubicaciones de [!UICONTROL Simple Ad Serving] no cumplen con los fondos utilizables de la cuenta ni con los presupuestos de campaña y paquete. Sin embargo, el gasto se rastrea y se contabiliza en esos presupuestos. Incluso cuando CPM tiene un valor de 0 $, siempre se realiza un seguimiento de los datos de evento.

>[!MORELIKETHIS]
>
>* [Crear una oferta [!UICONTROL Simple Ad Serving]](simple-deal-create.md)
>* [Editar la configuración de la oferta [!UICONTROL Simple Ad Serving]](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] configuración](simple-deal-settings.md)
>* [Ver un informe detallado de una oferta](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
