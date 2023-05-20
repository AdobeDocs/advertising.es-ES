---
title: Creación e implementación de un segmento de exclusión de la venta de CCPA
description: Obtenga información sobre cómo crear e implementar un segmento para rastrear los ID de usuario de solicitudes de exclusión de venta de consumidores.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Creación e implementación de un segmento de exclusión de la venta de CCPA

Puede crear un segmento para rastrear los ID de usuario de las solicitudes de exclusión de venta de consumidores en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA). Los usuarios permanecen indefinidamente en los segmentos de exclusión de la venta de la CCPA.

Una vez implementada la etiqueta de píxel de segmento, la publicidad de Adobe empezará a recopilar un grupo de ID en nombre del anunciante.

>[!NOTE]
>
>* Para obtener información sobre cómo comunicar las solicitudes de exclusión de la venta de la CCPA a la publicidad de Adobe mediante la API de Adobe Experience Platform Privacy Service, consulte [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Para rastrear a los usuarios que visitan páginas web con fines no relacionados con el seguimiento de eventos de exclusión de la venta de la CCPA, así como a los usuarios expuestos a anuncios de dispositivos de escritorio, móviles y de CTV, cree una [segmento personalizado](/help/dsp/audiences/custom-segment-create.md).


1. Cree el segmento:

   1. En el menú principal, haga clic en **Audiencias > Segmentos**.

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

   1. Introduzca un único **[!UICONTROL Segment Name]**.

      Nombre de segmento recomendado: &quot;&lt;*Su nombre del anunciante*> - Exclusión de la venta de la CCPA&quot; (como &quot;Acme - Exclusión de la venta de la CCPA&quot;)

   1. Para el [!UICONTROL Segment Type], seleccione **[!UICONTROL CCPA Opt-out of sale]**.

   1. Haga clic **[!UICONTROL Save]**.

1. Copie e implemente una etiqueta de píxel para realizar el seguimiento del segmento:

   1. Volver a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. En la fila del segmento, mantenga el cursor sobre el nuevo segmento y haga clic en **[!UICONTROL Get pixel]**.

   1. Copie el píxel de la imagen (comenzando por `<img src="https://rtd-tm.everesttech.net"`) para recopilar los ID de usuario de los visitantes de ordenadores de escritorio y móviles de una página web.

   1. Proporcione la etiqueta al anunciante o al contacto del sitio web para su implementación mediante el mecanismo que utiliza la compañía para rastrear las solicitudes de exclusión de venta de CCPA (como el uso de una plataforma de administración de consentimiento).

      Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.

      Una vez implementado el píxel, la publicidad de Adobe empezará a recopilar un grupo de ID en nombre del anunciante.

      Aunque la lógica y la elección de la implementación dependen del anunciante, este es un ejemplo de cómo un anunciante podría activar el píxel:

      1. Un consumidor llega a la página principal del anunciante.
      1. El consumidor encuentra y hace clic en el botón &quot;Exclusión de la venta de la CCPA&quot; del anunciante.
      1. Al consumidor se le presenta una lista de proveedores de servicios con los que trabaja el anunciante.
      1. El consumidor marca la casilla para excluirse de la venta de datos a Adobe Advertising.

         Esta acción déclencheur el píxel para que se active y recopile el ID de cookie del consumidor dentro del &quot; especificado[!UICONTROL CCPA Opt-out of sale]&quot; segmento.

>[!MORELIKETHIS]
>
>* [Adobe Compatibilidad con publicidad para la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Acerca de [!UICONTROL CCPA Opt-out-of-Sale] Segmentos e informes](ccpa-opt-out-about.md)
>* [Recuperación de informes de exclusión de venta de consumidores](ccpa-opt-out-segment-report-retrieve.md)
>* [Creación e implementación de un segmento personalizado](custom-segment-create.md)
>* [Acerca de Audience Management](audience-about.md)

