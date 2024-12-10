---
title: Acerca de la administración de anuncios en Advertising DSP
description: Obtenga información acerca de la administración de anuncios.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Acerca de la administración de anuncios en Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP La entrega de anuncios es compatible con la entrega de anuncios mediante etiquetas de servicio de anuncios de terceros (como Google, Flashtalk o Sizmek) para varios tipos de anuncios y la carga directa de recursos para anuncios en pantalla nativos. Puede cargar etiquetas de terceros de forma individual o en lotes. Las cargas masivas utilizan hojas de etiquetas de socios o una plantilla de etiquetas masiva.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Una vez configurados los anuncios, vincule cada anuncio a una o más ubicaciones, que incluyen los parámetros de segmentación (como ubicación geográfica, audiencia, dispositivo y segmentación de inventario) que controlan el rendimiento de la campaña. Debe adjuntar un anuncio a una ubicación para comenzar a ejecutarlo.

## Tipos de publicidad disponibles {#ad-types}

DSP Todos los tipos de anuncio siguientes están disponibles en la versión de. Para obtener las especificaciones completas para cada tipo de anuncio, consulte [Especificaciones del anuncio](ad-specs.md).

* **Anuncios de audio (solo de terceros)**: Los anuncios de audio se reproducen entre contenido de sitios de editores digitales y se pueden ejecutar de forma independiente como archivos de audio o junto con titulares complementarios. El audio se utiliza mejor para impulsar la imagen de marca y atraer audiencias sobre la marcha. Los indicadores clave de rendimiento para el audio incluyen [!UICONTROL Completion Rate] y [!UICONTROL Cost per Completion].

* **Anuncios de visualización (solo de terceros)**: Los anuncios de visualización son imágenes estáticas o animadas que se muestran en navegadores web o aplicaciones. Al hacer clic en la unidad de publicidad, se lleva al usuario a un sitio o micrositio con marca. La visualización se utiliza mejor para impulsar CPM eficientes, aumentar la asociación de mensajes, añadir puntos de contacto de productos o marcas adicionales y dirigir a los usuarios hacia abajo en el canal de compras. Los indicadores de rendimiento clave para la visualización incluyen [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions] y [!UICONTROL Cost per Conversion]. DSP admite una amplia variedad de tamaños de anuncios de banners de visualización.

* **Anuncios móviles (solo de terceros)**: Los anuncios móviles pueden estar en formato de vídeo previo a la emisión (VAST, MRAID) o en formato de visualización estándar. El vídeo móvil previo a la emisión puede reproducirse automáticamente o con un clic, y se utiliza mejor para llegar a los espectadores de todas las pantallas. La visualización estándar móvil es una imagen estática que se muestra en navegadores web móviles o en aplicaciones; se utiliza principalmente para complementar las compras de vídeo digital, impulsar la asociación de mensajes y añadir puntos de contacto de productos o marcas adicionales. Los anuncios móviles también pueden funcionar como adquisiciones a pantalla completa o como intersticiales móviles, que son anuncios móviles de alto impacto y pantalla completa que se utilizan mejor para desarrollar la imagen de marca de las audiencias móviles y dirigir las conversiones.

* **Anuncios en pantalla nativos (solo de origen)**: Los anuncios nativos se admiten en formato de visualización estándar. Los anuncios nativos incluyen un titular o título, una descripción, un logotipo y una imagen. Los elementos de anuncio se combinan y representan de modo que coincidan con el estilo de página del editor, de modo que el anuncio se integre con el contenido orgánico del editor y genere una mayor participación. El código nativo se utiliza mejor para concienciar a la marca y para aumentar las tasas de visualización de audiencia y participación con publicidad fácil de visualizar. Los indicadores clave de rendimiento incluyen [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions] y [!UICONTROL Cost Per Conversion].

* **Anuncios previos a la emisión (solo de terceros)**: Los anuncios previos a la emisión (VAST y VPAID) se muestran antes que el contenido de vídeo premium y proporcionan una experiencia de visualización atractiva e inmersiva. El vídeo previo a la emisión puede ser interactivo, contener funciones de medios enriquecidos e incluir superposiciones, rollovers y llamadas a la acción. Los indicadores de rendimiento clave para los anuncios de vídeo previos a la emisión incluyen [!UICONTROL Video Completion Rate] y [!UICONTROL Viewability Rate].

* **Anuncios de TV conectados (solo de terceros)**: Los anuncios de TV conectados se muestran antes y durante el contenido de vídeo de TV premium. Todo el inventario de TV conectado se ejecuta en dispositivos de TV, lo que significa que el vídeo se reproduce automáticamente en un entorno de pantalla completa e inclinado que los espectadores no pueden omitir. La TV conectada es el formato de vídeo digital más cercano a los anuncios de TV. Los indicadores de rendimiento clave para la TV conectada incluyen [!UICONTROL Completion Rate].

* **Anuncios de vídeo universales (solo de terceros)**: Los anuncios de vídeo universales le permiten segmentar el inventario de vídeos de entornos de escritorio, móviles y de TV conectada para el inventario VPAID y VAST con una sola ubicación de vídeo. Combinan todas las funciones de la TV conectada, el anuncio previo a la emisión y los anuncios previos a la emisión móviles, y se muestran antes y durante el contenido de vídeo. Los indicadores de rendimiento clave para el vídeo universal incluyen [!UICONTROL Completion Rate] y [!UICONTROL Viewability Rate].

  Los anuncios de vídeo universales solo se pueden adjuntar a ubicaciones de vídeo universales.

  Consulte &quot;[Preguntas más frecuentes acerca del vídeo universal](/help/dsp/campaign-management/faq-universal-video.md)&quot; para obtener más información acerca de los anuncios de vídeo universales.

## DSP Aprobaciones de anuncios

DSP Cuando cree un anuncio, lo revisa para categorías confidenciales, hace clic en Funcionalidad de URL y previsualiza el procesamiento.

Inicialmente, la columna [!UICONTROL Status] del anuncio muestra un punto rojo. El proceso de revisión suele durar entre 24 y 48 horas. Sin embargo, un anuncio roto puede tener un estado pendiente durante más de 48 horas, por lo que tiene tiempo para corregir errores antes de que se rechace el anuncio. Los anuncios rechazados incluyen un motivo para el rechazo.

DSP Cuando el usuario aprueba un anuncio, la columna Estado del anuncio muestra un punto verde.

![indicador de aprobación en [!UICONTROL Status] columna](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>DSP Su anuncio solo se puede publicar si tanto el proveedor de servicios como el proveedor de servicios compartidos (SSP) han aprobado el creativo. Cada SSP tiene sus propios requisitos y procesos de aprobación.

>[!MORELIKETHIS]
>
>* [Crear un solo anuncio](ad-create.md)
>* [Crear varios anuncios de terceros](ad-create-multiple.md)
>* [Especificaciones del anuncio](ad-specs.md)
