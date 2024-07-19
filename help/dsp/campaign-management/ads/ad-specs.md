---
title: Especificaciones del anuncio
description: Consulte las especificaciones generales y específicas del editor.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Especificaciones para tipos de publicidad admitidos

## Anuncios de vídeo (anuncio previo a la emisión, CTV y vídeo universal)

### Screens compatible

Los anuncios se entregan de forma predeterminada en equipos de escritorio, dispositivos móviles y dispositivos de TV conectados. La segmentación de dispositivos está disponible para ajustar la entrega.

### Servidores de publicidad de terceros compatibles

Puede usar hojas de etiquetas de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] y [!DNL Sizmek]. Para obtener una lista completa de los proveedores admitidos, consulte &quot;[Partners Certificados de Servicio de publicidad](certified-ad-servers.md)&quot;.

### Requisitos para Video Assets de alta definición (obligatorio)

**Tipo de etiqueta de vídeo:** VPAID 2.0 JavaScript o VAST (CTV). Todas las unidades de anuncios VPAID deben cumplir con la [especificación VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) según la definición del Interactive Advertising Bureau (IAB).

**Códec de vídeo:** MP4/H.264

**Resolución:** 1280 x 720 para 720p, 1920 x 1080 para 1080p

**Velocidad de bits:** 1.500-2.500 kbps para 720p, 2.500-3.500 kbps para 1.080p

**Perfil/nivel H.264:** perfil alto, nivel 3.1 para 720p; perfil alto, nivel 4.0 para 1080p

**Velocidad de fotogramas de vídeo:** 29,970 fps (denominada comúnmente como 30 fps) para países NTSC, 25 fps para países PAL, 23,976 fps (denominada comúnmente como 24 fps) para contenido de aspecto cinematográfico

**Espacio de color del vídeo:** 4:2:0 submuestreo de croma YUV

**Entrelazado de vídeo:** Análisis progresivo; es decir, no entrelazado. Sin movimiento en el interior del campo (fusión de fotogramas) ni entrelazado.

**Líderes (pizarra):** No permitidos

**Códec de audio:** AAC-LC o HE-AACv1

**Velocidad de bits de audio:** 128-192 kbps para AAC-LC, 64-128 kbps para HE-AACv1

**Canal de audio:** mezcla estéreo de dos canales

**Velocidad de muestreo de audio:** 44,1 kHz o 48 kHz, según el material de origen

**Niveles de audio:** 24 LKFS (+/- 2.0 dB) en los EE.UU. según ATSC A/85; 23 LUFS (+/- 1.0) en la UE según EBU R128

#### Requisitos adicionales del editor para anuncios de TV conectados

* **Red A+E:** Consulte las [especificaciones del anuncio](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf) de la red A+E

* **Descubrimiento:** Consulte las [especificaciones del anuncio](/help/dsp/assets/discovery-networks-ad-specs.pdf) del descubrimiento.

* **Disney (incluye Hulu):** Ver las [especificaciones del anuncio](https://hulu.disneyadsales.com/ad-products/video-commercial/) de Disney.

* **Máximo de HBO:** Consulte las [especificaciones del anuncio](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx) de HBO Max.

* **NBCUniversal:**

   * [Vídeo digital](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Pavo Real](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Principal:** Consulte las [especificaciones del anuncio de Paramount](https://www.paramount.com/digital-ads).

## Publicidad en pantalla

### Screens compatible

Los anuncios se entregan de forma predeterminada en equipos de escritorio y dispositivos móviles. La segmentación de dispositivos está disponible para ajustar la entrega.

### Tipos de archivo compatibles

**Imagen:** GIF, JPG/JPEG, PNG

**HTML 5:** Tipos de archivo de imagen: GIF, JPG/JPEG, PNG, SVG

### Requisitos para Image Assets (obligatorio)

Se admite la visualización universal.

**Tamaños de anuncio recomendados:** 120 x 60, 160 x 600, 180 x 150, 300 x 50, 300 x 100, 300 x 1050, 300 x 250, 300 x 600, 320 x 50, 320 x 480, 480 60 x 60, 640 x 480, 88 x 31, 728 x 90, 970 x 250, 970 x 90

**Servidores de publicidad de terceros admitidos:** Puede usar hojas de etiquetas de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] y [!DNL Sizmek]. Para obtener una lista completa de los proveedores admitidos, consulte &quot;[Partners Certificados de Servicio de publicidad](certified-ad-servers.md)&quot;.

## Anuncios de audio

### Screens compatible

Escritorio, Móvil, Tablet, Altavoces inteligentes y TV conectada

### Servidores de publicidad de terceros compatibles

Puede usar hojas de etiquetas de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] y [!DNL Sizmek]. Para obtener una lista completa de los proveedores admitidos, consulte &quot;[Partners Certificados de Servicio de publicidad](certified-ad-servers.md)&quot;.

### Requisitos para Audio Assets (obligatorio)

**Tipo de archivo:** MP3, OGG, AAC

**Líderes (pizarra):** No permitidos

**Tamaño máximo de archivo:** 2 MB

**Velocidad de bits:** 128

**Longitud de archivo:** 0-60s

#### Requisitos adicionales del editor

* **[!DNL iHeartRadio]**
   * Duración: 5, 15, 30 o 60 segundos
   * Tipo de archivo: MP3
   * Tamaño máximo de archivo: 320 kbps
   * Volumen: 44,1 kHz

* **[!DNL Pandora]**
   * Duración: 15 o 30 segundos
   * Tipo de archivo: MP4 (en la aplicación), MP3 (escritorio)
   * Tamaño máximo de archivo: 2,2 MB

* **[!DNL SoundCloud]**
   * Duración: 6, 15 o 30 segundos
   * Tipo de archivo: MP3
   * Tamaño máximo de archivo: 5 MB

* **[!DNL Spotify]**
   * Duración: hasta 30 segundos
   * Tipo de archivo: OGG
   * Tamaño máximo de archivo: 500 MB
   * Volumen: RMS normalizado a -14; dBFS pico normalizado a -0,2 dBFS

* **[!DNL TargetSpot]**
   * Duración: 15, 30 o 60 segundos
   * Tipo de archivo: MP3

* **[!DNL TuneIn]**
   * Duración: 10, 15 o 30 segundos
   * Tipo de archivo: MP3, OG
   * Volumen: 44,1 kHz

### Requisitos para anuncios de banner de Companion (opcional)

**Tamaños compatibles:** 300 x 250, 500 x 500, 640 x 640, 1024 x 1024

#### Requisitos adicionales del editor

* **[!DNL iHeartRadio]:**
   * Tipo de archivo: JPEG, JPG, PNG, GIF, SWF, HTML
   * Tamaño máximo de archivo: 2,2 MB
   * Dimension: 300x250

* **[!DNL Pandora]:**
   * Tipo de archivo: JPEG, GIF
   * Tamaño máximo de archivo: Tamaño: 100 KB
   * Dimension: 300 x 250 (móvil o sobremesa) o 500 x 500 (sobremesa)

* **[!DNL SoundCloud]:**
   * Tipo de archivo: Estático, JPG, PNG
   * Tamaño máximo de archivo: menos de 400 KB
   * Dimension: 1024 x 1024

* **[!DNL Spotify]:**
   * Tipo de archivo: Estático, JPG, PNG
   * Tamaño máximo de archivo: 200 KB
   * Dimension: 300x250

* **[!DNL TuneIn]:**
   * Tipo de archivo: JPEG, HTML, JPG, PNG, GIF
   * Tamaño máximo de archivo: 2 MB
   * Dimension: 300x250

## Anuncios en pantalla nativos

Cada anuncio puede incluir una imagen fija o un GIF en movimiento (cinemagrafía).

### Screens compatible

Los anuncios se entregan de forma predeterminada en equipos de escritorio y dispositivos móviles. La segmentación de dispositivos está disponible para ajustar la entrega.

### Assets requerido para todos los formatos de entrada nativos

#### Recurso de imagen

**Resolución:** Mínimo de 600 x 600 px; mínimo recomendado de 1200 x 627 px

**Tipo de archivo:** JPEG (imagen de anuncio o imagen de portada de anuncio de vídeo), GIF (cinemógrafo)

**Tamaño de archivo:** Menos de 1 MB (la imagen no debe contener texto).

#### Logotipo del anunciante

**Resolución:** Mínimo de 80 x 80 px; mínimo recomendado de 300 x 300 px

**Tipo de archivo:** JPEG o PNG.

**Proporción de aspecto:** 1x1

>[!NOTE]
>
>Según la imagen sobre la que se superponga, elija entre recursos de logotipo claros u oscuros.

#### Texto/Copiar

**Titular:** Máximo de 200 caracteres; se recomiendan 25 caracteres

**Título:** máximo de 200 caracteres; se recomiendan 100 caracteres

**Patrocinado por:** Máximo de 200 caracteres; se recomiendan 30 caracteres

**Llamada a la acción (solo MoPub):** Máximo de 15 caracteres

>[!NOTE]
>
>El editor define el diseño final durante la ejecución. Si un anuncio supera el recuento de caracteres recomendado, es posible que algunos proveedores de inventario no entreguen el anuncio o que el editor o el SSP trunquen el texto.

#### URL de página de aterrizaje

La URL de pulsación con rastreadores de clics opcionales.

Requisitos para los rastreadores de clics:

* Píxeles de seguimiento de impresiones de terceros: solo formato de URL de imagen 1x1

* Visibilidad Rastreadores de JavaScript: compatible solo con IAS; imágenes 1x1 solo en formato JS.append

* Píxeles de seguimiento de clics de terceros: deben redirigir a la página de aterrizaje incrustada en la dirección URL (redirección HTTP 302)

* Los rastreadores de clics de la plataforma de administración de datos (DMP) con 200 o más respuestas no son compatibles.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Crear varios anuncios de terceros](ad-create-multiple.md)
>* [Editar un anuncio](ad-edit.md)
