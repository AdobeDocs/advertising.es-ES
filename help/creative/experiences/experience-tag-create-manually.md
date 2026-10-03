---
title: Crear manualmente una etiqueta de anuncio para un tamaño creativo aplicable
description: Aprenda a crear una etiqueta de anuncio para un tamaño creativo específico.
feature: Creative Experiences
exl-id: 77dedfa2-33de-4a92-a58b-1a2b91842f0a
TQID: 'https://experienceleague.adobe.com/xeWVCvDYgNAoZlNeEmHIAuajuMy5QZL73oFJO4gFfFE'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%
---
# (Experiencias sin segmentación) Cree manualmente una etiqueta de anuncio para un tamaño creativo aplicable

*Solo experiencias sin segmentación en el árbol de decisiones*

Puede crear una o más etiquetas de anuncio por idioma para cada tamaño creativo (creativos que no sean de vídeo) o duración de vídeo que se utilice para una experiencia. Puede [asignar posteriormente elementos creativos a la etiqueta de anuncio](experience-tag-assign-creatives.md).

>[!NOTE]
>
>Para las experiencias con segmentación en el árbol de decisiones, [!DNL Creative] crea automáticamente una etiqueta por idioma para cada tamaño creativo o duración de vídeo aplicable.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Tag Manager]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Tag Manager]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create Tag]**.

1. Escriba un(a) **[!UICONTROL Tag name]** único(a) y seleccione (anuncios de pantalla estándar) el(la) **[!UICONTROL Tag size]** o (anuncios de vídeo estándar) el(la) **[!UICONTROL Duration]**.

   Los tamaños o la duración de los elementos creativos predeterminados para la experiencia determinan los tamaños creativos o las duraciones de vídeo disponibles.

   Puede crear varias etiquetas para el mismo tamaño creativo o duración.<!-- What are the implications? -->

1. Haga clic en **[!UICONTROL Create]**.

   Puede ampliar la fila de etiquetas para ver los elementos creativos incluidos.

   Para las experiencias de anuncios de vídeo, los creativos de vídeo se transcodifican automáticamente con la codificación Adobe Advertising DSP como etiquetas VAST 2.0 para que pueda previsualizarlos. Opcionalmente, puede [aplicar la transcodificación para un DSP diferente](experience-tag-video-transcoding.md).

>[!MORELIKETHIS]
>
>* [Asignar elementos creativos a una etiqueta de anuncio para experiencias sin segmentación](experience-tag-assign-creatives.md)
>* [Personalizar las direcciones URL de seguimiento para una experiencia sin segmentación](experience-tracking-urls-no-targeting.md)
>* [Personalizar la optimización creativa y la programación de una experiencia sin segmentación](experience-optimization-scheduling-no-targeting.md)
>* [Personalizar opciones de transcodificación para una etiqueta de experiencia de anuncio de vídeo](experience-tag-video-transcoding.md)
>* [Exportar e implementar una etiqueta de experiencia de anuncio para una experiencia en vivo](experience-tag-export.md)
>* [Cambiar el nombre de una etiqueta de anuncio](experience-tag-rename.md)
