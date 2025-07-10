---
title: Exportación e implementación de una etiqueta de experiencia de anuncio para una experiencia en directo
description: Obtenga información sobre cómo exportar una etiqueta de experiencia de anuncio y, opcionalmente, cargarla en una campaña de Advertising DSP.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: 45b2dad83aa626ea30e7553df7caaf5e7f53b3e1
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Exportación e implementación de una etiqueta de experiencia de anuncio para una experiencia en directo

*Beta cerrada*

Una vez que haya disponible una etiqueta de anuncio para un tamaño creativo específico para una experiencia [live](experience-about.md#experience-statuses), puede generar y copiar la etiqueta en los formatos JavaScript e iframe para su implementación en Advertising DSP u otros DSP. Las etiquetas de DSP incluyen todas las macros necesarias para DSP.

Los anunciantes con Advertising DSP pueden, opcionalmente, cargar etiquetas directamente en una campaña de Advertising DSP como anuncios con el tipo de anuncio &quot;visualización estándar&quot;.

>[!NOTE]
>
>* Cuando crea una experiencia con la segmentación del árbol de decisiones, [!DNL Creative] crea automáticamente una etiqueta de anuncio para cada tamaño creativo aplicable.
>* Cuando crea una experiencia sin segmentar el árbol de decisiones, debe [crear manualmente una etiqueta de anuncio](experience-tag-create-manually.md) para cada tamaño creativo aplicable.
>* Las etiquetas de experiencia son dinámicas. No es necesario actualizar las etiquetas si edita una experiencia.
>* Asegúrese de que las campañas en las que va a implementar una experiencia publicitaria incluyan una segmentación compatible con la experiencia. El comportamiento de direccionamiento jerárquico puede variar según DSP. En Advertising DSP, la segmentación a nivel de anuncio se aplica sobre la segmentación a nivel de ubicación (no en su lugar).

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Realice una de las siguientes acciones:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Tag Manager]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Tag Manager]**.

1. Mantenga el cursor sobre la fila de la etiqueta de publicidad aplicable y haga clic en ![Exportar etiquetas de publicidad](/help/creative/assets/export.png "Exportar etiquetas de publicidad") **[!UICONTROL Export ad tags]** o **[!UICONTROL ... More] > **[!UICONTROL Export ad tags]**.

>[!NOTE]
>
>Para experiencias de anuncios de vídeo estándar, espere hasta que la columna [!UICONTROL Tag Status] muestre &quot;[!UICONTROL Ready]&quot;, lo que indica que se han transcodificado todos los vídeos de la experiencia. DSP transcodifica automáticamente todos los creativos de vídeo, pero [puede aplicar la transcodificación](experience-tag-video-transcoding.md) específica del editor a cualquier etiqueta de experiencia de anuncio de vídeo.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Opcional) En la ficha [!UICONTROL Macros], especifique hasta cinco macros personalizadas para incluir en la etiqueta. Para que cada macro incluya:

   1. Seleccione una casilla de verificación.<!-- Explain more -->

   1. Escriba la macro personalizada.<!-- Explain more -->

1. Haga clic en **[!UICONTROL Next]** en la esquina superior derecha o haga clic en **[!UICONTROL Generate ad tags]** en el menú de la izquierda.

1. Seleccione el tipo de etiqueta: ** *JavaScript<!-- sic -->* ** o ** *IFRAME* ** <!-- sic -->.

1. En la lista [!UICONTROL Destinations], seleccione dónde creará anuncios para la experiencia.

   * *Genérico:* Para anuncios que crearás en otros DSP. **Nota:** Es posible que tenga que incluir manualmente [macros adicionales](/help/creative/creative-macros.md) según sea necesario.

   * *Adobe AdCloud:* Para anuncios que crearás en Advertising DSP.

   * *Google CM360:* Para anuncios que crearás en [!DNL Google Campaign Manager 360]. **Nota:** Es posible que tenga que incluir manualmente [macros adicionales](/help/creative/creative-macros.md) según sea necesario.

1. Haga clic en **[!UICONTROL Generate tags]**.

1. Copie o descargue las etiquetas:

   * Para copiar una etiqueta para un solo tamaño de anuncio, expanda la fila de etiqueta, mantenga el cursor sobre la fila y, a continuación, haga clic en ![Copiar](/help/creative/assets/copy.png "Copiar") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * Para descargar todas las etiquetas generadas como un archivo en la ubicación de descarga predeterminada del explorador, haga clic en ![Descargar etiquetas](/help/creative/assets/download.png "Descargar etiquetas").

   Puede abrir el archivo en un editor de texto para copiar cada etiqueta. Para las etiquetas JavaScript, la etiqueta se incluye entre `<script></script>` y `<noscript></noscript>`tags. Para las etiquetas de iframe, la etiqueta se incluye entre `<iframe></iframe>` etiquetas.

1. Implemente las etiquetas para el DSP correspondiente:

   * Para los DSP que no sean de Advertising DSP, proporcione las etiquetas a quienquiera que cree los anuncios dentro de DSP.

   * Para Advertising DSP:

      1. Haga clic en **[!UICONTROL Next]** en la esquina superior derecha o haga clic en **[!UICONTROL DSP link]** en el menú de la izquierda.

      1. Seleccione la campaña en la que desea cargar la etiqueta de publicidad.

      1. Haga clic en **[!UICONTROL Assign Tags]**.

         DSP se abre a la vista [!UICONTROL Ads] de la campaña seleccionada.

      1. En la vista [!UICONTROL Create ads], revise las etiquetas de anuncio, seleccione las etiquetas para las que desee crear un anuncio y, a continuación, haga clic en **[!UICONTROL Create]**.

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [Crear manualmente una etiqueta de anuncio para un tamaño creativo aplicable](experience-tag-create-manually.md)
>* [Asignar elementos creativos a una etiqueta de anuncio para experiencias sin segmentación](experience-tag-assign-creatives.md)
>* [Cambiar el nombre de una etiqueta de anuncio](experience-tag-rename.md)
>* [Personalizar opciones de transcodificación para una etiqueta de experiencia de anuncio de vídeo](experience-tag-video-transcoding.md)
