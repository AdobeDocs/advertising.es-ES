---
title: Personalización de las opciones de transcodificación de una etiqueta de vídeo y experiencia
description: Aprenda a personalizar las opciones de transcodificación de una etiqueta de anuncio de vídeo.
feature: Creative Experiences
exl-id: 6100213c-2e7d-4e98-a3ab-045ca10e5174
source-git-commit: 8f5740d1a90e505a16f69d566de13aefc1edf421
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# Personalización de las opciones de transcodificación de una etiqueta de vídeo y experiencia

*Beta cerrada*

Puede personalizar las opciones de transcodificación de una experiencia de anuncio de vídeo para garantizar una reproducción rápida y un control de calidad entre los editores.

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Tag Manager]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Tag Manager]**.

1. Mantenga el cursor sobre la fila de la etiqueta de publicidad aplicable, haga clic en **[!UICONTROL More]** y, a continuación, haga clic en **[!UICONTROL Video Settings]**.

1. En la lista de **[!UICONTROL Publisher-specific transcodes]**, seleccione el DSP cuya transcodificación desee aplicar.

1. Haga clic en **[!UICONTROL Save Settings]**.

## Especificación de transcodificación predeterminada ([!DNL Adobe] DSP)

| Tipo de archivo | Dimensiones | Velocidad de bits de vídeo | Velocidad de fotogramas de vídeo | Velocidad de bits de audio | Velocidad de muestreo de audio | Nivel de audio |
|---|---|---|---|---|---|---|
| mp4 | 640 x 360 | 1000 kbps | 23,98 fps | 128 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 400 x 300 | 1000 kbps | 23,98 fps | 128 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 1024 x 768 | 500 kbps | 23,98 fps | 128 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 640x480 | 1000 kbps | 23,98 fps | 128 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 960x540 | 2000 kbps | 23,98 fps | 128 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 960x720 | 2000 kbps | 23,98 fps | 128 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 1280x720 | 2000 kbps | 23,98 fps | 128 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 1920x1080 | 3500 kbps | 23,98 fps | 128 kbps | 44,100 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 640 x 360 | 800 kbps | 23,98 fps | 96 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 640 x 360 | 400 kbps | 23,98 fps | 128 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |
| mp4 | 1920x1080 | 16000 kbps | 23,98 fps | 256 kbps | 48,000 kHz | 24 LKFS (+/- 2 dB) |

>[!MORELIKETHIS]
>
>* [Acerca de sus bibliotecas creativas](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Crear una experiencia con segmentación](/help/creative/experiences/experience-create-targeting.md)
>* [Crear manualmente una etiqueta de anuncio para un tamaño creativo aplicable](experience-tag-create-manually.md)
>* [Exportar e implementar una etiqueta de experiencia de anuncio para una experiencia en vivo](experience-tag-export.md)
