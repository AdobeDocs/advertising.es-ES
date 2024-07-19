---
title: Creación de varios anuncios de terceros
description: Obtenga información sobre cómo crear varios anuncios de terceros al mismo tiempo.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Creación de varios anuncios de terceros

Puede crear hasta 500 anuncios de terceros a la vez cargando etiquetas que apunten a recursos creativos alojados en servidores de publicidad de terceros. Puede incluir píxeles de seguimiento para los anuncios.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Puede cargar [!DNL DoubleClick] y [!DNL Flashtalking] hojas de etiquetas o un archivo rellenado manualmente con la plantilla proporcionada.

>[!TIP]
>
> La práctica recomendada es utilizar anuncios de terceros que se publiquen de forma segura mediante HTTPS. Las direcciones URL servidas mediante HTTPS comienzan por &quot;https&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña en la que desea incluir el anuncio.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**. En la sección Tipos de publicidad del menú, haga clic en **[!UICONTROL Bulk upload ads]**.

1. Seleccione el servidor de publicidad en el que se hospeda el anuncio: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* o *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] y [!DNL Flashtalking] anuncios) Seleccione el tipo de etiqueta que se usará para cada recurso de vídeo y cada recurso de visualización. Las opciones disponibles varían según el servidor de publicidad.

1. (Anuncios en todos los servidores de publicidad excepto [!DNL DoubleClick] y [!DNL Flashtalking]) Haga clic en **[!UICONTROL Download this template]** para descargar una plantilla en formato de hoja de cálculo [!DNL Microsoft Excel] (XLSX), que puede rellenar con datos de anuncio y guardar localmente. Las columnas requeridas incluyen [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag] y [!UICONTROL Ad Types].

1. Haga clic en **[!UICONTROL Upload]** y seleccione un archivo en los formatos .xlsx o .xls de su dispositivo o red.

   Para los anuncios de [!DNL DoubleClick] y [!DNL Flashtalking], cargue hojas de etiquetas sin editar del servidor de publicidad. Para otros servidores de publicidad, utilice la plantilla descargada en el paso 3.

1. Una vez completada la carga, haga clic en **[!UICONTROL Start Building Ads]**.

1. Revise los detalles y el estado de cada anuncio:

   1. (Anuncios de vídeo universales con etiquetas [!DNL Google] o [!DNL Flashtalking]) Haga clic en el campo **[!UICONTROL Ad Type]** y seleccione **[!UICONTROL Universal Video]**.

   1. (Anuncios de vídeo universales) Para cada anuncio nuevo, haz clic en ![editar](/help/dsp/assets/edit.png), selecciona el [formato de vídeo aplicable](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) y, a continuación, haz clic en **Guardar**.

   1. Revise el estado de cada anuncio, que se basa en las comprobaciones de validación de la etiqueta cargada.

   1. (Opcional) Realice cualquiera de las siguientes acciones para cada anuncio:

      * Para obtener una vista previa de un anuncio, haz clic en ![reproducir](/help/dsp/assets/play.png) en la fila del anuncio.

      * Para editar los detalles del anuncio, haz clic en ![editar](/help/dsp/assets/edit.png), edita los detalles y luego haz clic en **Guardar**.

      * Para quitar un anuncio, haga clic en **[!UICONTROL X]** en la fila del anuncio.

1. Haga clic en **[!UICONTROL Create *N *anuncio(s)]**.

1. Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Done]**.

   * (Si se rechaza un anuncio, opcional) Para editar el registro de anuncio y volver a enviarlo para su revisión:

      1. Haga clic en el nombre del anuncio.

      1. Edite la configuración del anuncio.

      1. Haga clic en **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Los anuncios de vídeo universales solo se pueden adjuntar a ubicaciones de vídeo universales.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de anuncios](ad-about.md)
>* [Especificaciones del anuncio](ad-specs.md)
>* [Crear un solo anuncio](ad-create.md)
>* [Vídeo: Cómo cargar de forma masiva etiquetas de anuncios de terceros](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Preguntas más frecuentes sobre el vídeo universal](/help/dsp/campaign-management/faq-universal-video.md)
