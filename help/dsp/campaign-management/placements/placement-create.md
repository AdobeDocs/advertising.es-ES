---
title: Crear una ubicación
description: Obtenga información sobre cómo crear una ubicación.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Crear una ubicación

>[!TIP]
>
>Cree ubicaciones basadas en objetivos de campaña específicos o en las necesidades de creación de informes.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña en la que desea incluir la ubicación.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**. En la sección [!UICONTROL Placement Types] del menú, haga clic en el tipo de ubicación.

   El tipo de ubicación determina el tipo de anuncio que puede incluir la ubicación.

1. Escriba la [configuración de ubicación](placement-settings.md):

   1. Especifique la configuración de [!UICONTROL Placement Basics].

   1. En la sección [!UICONTROL Goals], especifique [!UICONTROL Gross Budget] y, opcionalmente, especifique objetivos de ubicación adicionales.

      Algunos campos tienen valores predeterminados que se pueden anular.

      Si el paquete al que se asigna la ubicación tiene un ritmo de nivel de paquete, los objetivos y la configuración del ritmo reflejarán la configuración del paquete.

   1. (Opcional) En la sección [!UICONTROL Geo-Targeting], reduzca las ubicaciones que se incluyen o excluyen.

      Si no identifica ubicaciones específicas, se segmentan todas las ubicaciones.

      >[!NOTE]
      >
      >Las ubicaciones de ciudad y DMA no están disponibles para las ubicaciones de Roku.

   1. En la sección [!UICONTROL Inventory Targeting], reduzca los orígenes de inventario que desea incluir o excluir.

      Para la mayoría de los tipos de ubicación, todos los tipos de inventario y todos los orígenes de cada tipo se incluyen de forma predeterminada. Para [!DNL Roku] ubicaciones, debe especificar el tipo de inventario y los orígenes.

   1. (Opcional) En la sección [!UICONTROL Site Targeting], reduzca los sitios a los que desee destinar y especifique los que desee excluir.

   1. (Opcional) En la sección [!UICONTROL Audience Targeting]:

      1. Reduzca la audiencia. Esto incluye la selección de segmentos de audiencia para segmentar dentro de la ubicación.

         DSP Para las ubicaciones de [!DNL Roku], puede aprovechar la coincidencia de audiencia única de [con  [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) incluyendo uno o más segmentos de audiencia que puedan coincidir con el conjunto de datos determinista [!DNL Roku] (incluido).

      1. (Para campañas con segmentación entre dispositivos por personas; opcional) Cuando la ubicación se dirija a una o más audiencias específicas, habilite la segmentación entre dispositivos por personas para la ubicación.

         [!DNL LiveRamp] proporciona la segmentación entre dispositivos basada en personas únicamente con datos de EE. UU. El servicio está disponible para todos los anunciantes a $0.35 CPM para las impresiones que se entregan mediante el gráfico de dispositivo [!DNL LiveRamp] (es decir, para los dispositivos que no se encuentran dentro de los segmentos de audiencia de destino).

   1. (Opcional) En la sección [!DNL Brand Safety and Media Targeting], aplique restricciones de seguridad de marca a sus ubicaciones.

   1. (Opcional) En la sección [!DNL Tracking], introduzca píxeles de evento de terceros o píxeles de conversión para los anuncios en la ubicación.

      >[!NOTE]
      >
      >([!DNL Roku] ubicaciones) Los proveedores de píxeles de terceros aprobados por [!DNL Roku] incluyen [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] y [!DNL Research Now].

1. Haga clic en **[!UICONTROL Create Placement]**.

1. (Opcional) Adjunte anuncios a la ubicación:

   1. Haga clic en **[!UICONTROL Attach an ad]**.

   1. Realice una de las acciones siguientes:

      * Para crear un anuncio nuevo:

         1. Haga clic en **[!UICONTROL Create a New Ad].**

         1. Especifique la configuración de anuncios para [anuncios de audio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [TV conectado](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [anuncios para mostrar](/help/dsp/campaign-management/ads/ad-settings-display.md), [anuncios móviles](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [anuncios nativos](/help/dsp/campaign-management/ads/ad-settings-native.md), [anuncios previos a la emisión](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) o [anuncios de vídeo universales](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >Las ubicaciones de vídeo universales solo pueden contener anuncios de vídeo universales.

         1. Haga clic en **[!UICONTROL Save & Submit for Review]**.

         1. (Opcional) Para cada anuncio adicional que desee crear para la ubicación, haga clic en **[!UICONTROL Attach Another Ad]** y, a continuación, repita los pasos del 1 al 3.

         1. Si no va a adjuntar anuncios existentes, haga clic en **[!UICONTROL I'm done for now]**.

      * Para adjuntar anuncios existentes en la campaña:

      1. Haga clic en **[!UICONTROL Select an Ad]**.

      1. Realice una de las acciones siguientes:

         * Para agregar un anuncio a la vez:

            1. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**

            1. (Opcional) Para cada anuncio adicional que desee adjuntar, haga clic en **[!UICONTROL Attach Another Ad]** y, a continuación, repita el proceso.

         * Para agregar hasta 20 anuncios a la vez:

            1. Seleccione la casilla de verificación situada encima de la lista de anuncios.

            1. Seleccione la casilla de verificación situada junto a cada anuncio que desee añadir.

            1. Haga clic en **[!UICONTROL Attach]**.

            1. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select]**.

      1. (Opcional) Para anular el período de vuelo y la rotación de publicidad predeterminados para anuncios específicos de la ubicación:

         1. Haga clic en **[!UICONTROL Custom Schedule Ads]**.

         1. Realice una de las siguientes acciones:

            * Para agregar un vuelo, haga clic en **[!UICONTROL Add Flight]** y después especifique la fecha de inicio y la fecha de finalización.

            * Para agregar un vuelo existente a un anuncio, haga clic en **[!UICONTROL +]** en la fila de anuncio de la columna vuelo.

            * Para eliminar un vuelo existente de un anuncio, haga clic en **[!UICONTROL x]** en la fila de anuncio de la columna vuelo.

            * (Cuando varios anuncios tengan el mismo vuelo) Para rotar los anuncios de forma desigual, haga clic en **[!UICONTROL Even Rotation]** en la información de vuelo y, a continuación, especifique el peso relativo por el que desea rotar cada anuncio, como porcentaje.

              El peso total debe ser igual a 100.

         1. En la esquina superior derecha, haga clic en **[!UICONTROL Continue]**.

         1. Revise los detalles del vuelo y haga clic en **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de ubicaciones](placement-about.md)
>* [Editar ubicaciones](placement-edit.md)
>* [Administrar multiplicadores de oferta para ubicaciones](placement-manage-bid-multipliers.md)
>* [Editar los horarios de anuncios para las ubicaciones](placement-edit-ad-schedule.md)
>* [Pausar o activar una ubicación](placement-pause-activate.md)
>* [Ver el registro de cambios de una ubicación](placement-change-log.md)
>* [Configuración de ubicación](placement-settings.md)
>* [Ver el informe de previsión de ubicación](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Preguntas más frecuentes sobre el vídeo universal](/help/dsp/campaign-management/faq-universal-video.md)
>* [Métodos abreviados de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Rendimiento de solución de problemas](/help/dsp/optimization/troubleshooting-performance.md)
>* [Vídeo: Cómo crear una ubicación de visualización estándar](https://video.tv.adobe.com/v/344998?captions=spa)
