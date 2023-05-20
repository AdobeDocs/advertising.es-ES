---
title: Creación de varios anuncios de terceros
description: Obtenga información sobre cómo crear varios anuncios de terceros al mismo tiempo.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 5139e6022cd5f5f11046d8f38bd0f1db91464928
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Creación de varios anuncios de terceros

Puede crear hasta 500 anuncios de terceros a la vez cargando etiquetas que apunten a recursos creativos alojados en servidores de publicidad de terceros. Puede incluir píxeles de seguimiento para los anuncios.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Puede realizar la carga [!DNL DoubleClick] y [!DNL Flashtalking] hojas de etiquetas o un archivo rellenado manualmente con la plantilla proporcionada.

>[!TIP]
>
> La práctica recomendada es utilizar anuncios de terceros que se publiquen de forma segura mediante HTTPS. Las direcciones URL servidas mediante HTTPS comienzan por &quot;https&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña en la que se incluirá el anuncio.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**. En la sección Tipos de anuncio del menú, haga clic en **[!UICONTROL Bulk upload ads]**.

1. Seleccione el servidor de publicidad en el que está alojado el anuncio: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]*, o *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] y [!DNL Flashtalking] anuncios) Seleccione el tipo de etiqueta que desea utilizar para cada recurso de vídeo y cada recurso de visualización. Las opciones disponibles varían según el servidor de publicidad.

1. (Anuncios en todos los servidores de publicidad excepto [!DNL DoubleClick] y [!DNL Flashtalking]) Haga clic **[!UICONTROL Download this template]** para descargar una plantilla en [!DNL Microsoft Excel] formato de hoja de cálculo (XLSX), que se puede rellenar con datos de publicidad y guardar localmente. Las columnas requeridas incluyen [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag], y [!UICONTROL Ad Types].

1. Clic **[!UICONTROL Upload]** y seleccione un archivo en los formatos .xlsx o .xls desde su dispositivo o red.

   Para [!DNL DoubleClick] y [!DNL Flashtalking] anuncios, cargue hojas de etiquetas sin editar del servidor de publicidad. Para otros servidores de publicidad, utilice la plantilla descargada en el paso 3.

1. Una vez completada la carga, haga clic en **[!UICONTROL Start Building Ads]**.

1. Revise los detalles y el estado de cada anuncio:

   1. (Anuncios de vídeo universales que utilizan [!DNL Google] o [!DNL Flashtalking] etiquetas) Haga clic en **[!UICONTROL Ad Type]** y seleccione **[!UICONTROL Universal Video]**.

   1. (Anuncios de vídeo universales) Para cada nuevo anuncio, haga clic en ![editar](/help/dsp/assets/edit.png), seleccione la [formato de vídeo aplicable](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)y haga clic en **Guardar**.

   1. Revise el estado de cada anuncio, que se basa en las comprobaciones de validación de la etiqueta cargada.

   1. (Opcional) Realice cualquiera de las siguientes acciones para cada anuncio:

      * Para previsualizar un anuncio, haga clic en ![play](/help/dsp/assets/play.png) en la fila del anuncio.

      * Para editar los detalles del anuncio, haga clic en ![editar](/help/dsp/assets/edit.png), edite los detalles y haga clic en **Guardar**.

      * Para quitar un anuncio, haga clic en **[!UICONTROL X]** en la fila del anuncio.

1. Clic **[!UICONTROL Create *N *Anuncio(s)]**.

1. Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL Done]**.

   * (Si se rechaza un anuncio, opcional) Para editar el registro de anuncio y volver a enviarlo para su revisión:

      1. Haga clic en el nombre del anuncio.

      1. Edite la configuración del anuncio.

      1. Haga clic **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Los anuncios de vídeo universales solo se pueden adjuntar a ubicaciones de vídeo universales.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Vídeo: Carga masiva de etiquetas de publicidad de terceros](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Preguntas frecuentes sobre Universal Video](/help/dsp/campaign-management/faq-universal-video.md)

