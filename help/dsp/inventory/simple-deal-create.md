---
title: Crear una oferta [!UICONTROL Simple Ad Serving]
description: Aprenda a crear un píxel de seguimiento para una oferta de [!UICONTROL Simple Ad Serving].
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Crear una oferta [!UICONTROL Simple Ad Serving]

1. En el menú principal, haga clic en **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Encima de la tabla de datos, haga clic en **[!UICONTROL Create]** y seleccione **[!UICONTROL Simple Ad Serving]**.

1. Escriba la [configuración de la oferta](simple-deal-settings.md):

   1. En la sección [!UICONTROL Select Ad Source], especifique información sobre el editor, el anunciante, la campaña y el tipo de anuncio y, a continuación, haga clic en **[!UICONTROL Next]**.

   1. DSP En la sección [!UICONTROL Select Ad(s)], especifique un anuncio para utilizarlo como proxy en el siguiente:

      1. Realice una de las acciones siguientes:

         * Para los anuncios existentes, seleccione los anuncios que desea utilizar.

         * Para anuncios nuevos, cree un [anuncio de terceros](/help/dsp/campaign-management/ads/ad-create-multiple.md) proxy.

      >[!NOTE]
      > DSP No se muestran los anuncios especificados por el usuario. El editor publica el anuncio.

      1. Haga clic en **[!UICONTROL Next]**.

   1. En Detalles de la fuente, edite los detalles de la fuente y, a continuación, haga clic en **[!UICONTROL Next]**.

      DSP La ubicación genera automáticamente una ubicación, denominada &quot;Ubicación SAS - &lt;*nombre de la oferta*>&quot;, para el anuncio. En la ubicación, la oferta se segmenta automáticamente en la sección [!UICONTROL Inventory Targets]. Todas las demás opciones de segmentación no son aplicables.

1. Envíe los píxeles de seguimiento de eventos al editor para su implementación de cualquiera de las siguientes maneras:

   * (Opcional) En la pantalla [!UICONTROL Activate Tag with Publisher], envíe la etiqueta de oferta al editor.

     DSP Cuando termine los pasos anteriores, generará un mensaje de correo electrónico que podrá enviar al editor en cuestión. El mensaje incluye los detalles de la oferta, un vínculo desde el que recuperar la etiqueta de oferta y un código de autorización para el vínculo.

      1. Revise los detalles de la oferta y, a continuación, realice una de las acciones siguientes:

         * Para pegar la información en un mensaje de correo electrónico en una aplicación de correo electrónico de su dispositivo, haga clic en **[!UICONTROL Email & Done]** y seleccione la aplicación de correo electrónico. El campo [!UICONTROL CC:] se ha rellenado previamente con una dirección de soporte técnico [!DNL Adobe]. A continuación, puede enviar el mensaje al contacto apropiado del editor.

         * Para copiar la información en el portapapeles, haga clic en **[!UICONTROL Copy Email].** A continuación, puede pegar manualmente el contenido en un mensaje de correo electrónico y enviarlo al contacto apropiado del editor. Debe incluir una copia (CC:) en `publisher-support-global@adobe.com`. Cuando termine de copiar el mensaje, haga clic en **[!UICONTROL Email & Done]**.

      1. (Si es necesario) Consulte con el editor para ver si la etiqueta incluye las macros adecuadas para que la etiqueta funcione con el servidor de publicidad del editor.

   * (Opcional) Envíe manualmente los píxeles de seguimiento de eventos al editor:

      1. En la fila de acuerdo dentro de la vista [!UICONTROL Deals], haga clic en ![Menú de opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Los píxeles del evento incluyen un píxel [!UICONTROL Clickthrough] y un píxel [!UICONTROL Impression]. Los anuncios de vídeo y audio también incluyen píxeles de evento por cuartil completado (de [!UICONTROL 25% Complete] a [!UICONTROL 100% Complete]).

      1. Copie los píxeles de seguimiento de eventos y envíeselos a su editor.

>[!MORELIKETHIS]
>
>* [Acerca de [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* Configuración de [[!UICONTROL Simple Ad Serving]](simple-deal-settings.md)
>* [Ver un informe detallado de una oferta](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
