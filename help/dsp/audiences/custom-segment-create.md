---
title: Creación e implementación de un segmento personalizado
description: Obtenga información sobre cómo crear e implementar un segmento personalizado para rastrear usuarios expuestos a anuncios o usuarios que visitan sus páginas web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Creación e implementación de un segmento personalizado

DSP Puede recopilar sus propios datos de audiencia de origen creando e implementando un segmento de audiencia personalizado de. Puede utilizar el segmento para rastrear a) usuarios expuestos a anuncios desde dispositivos de escritorio, móviles y CTV, y b) usuarios que visitan páginas web específicas. Más adelante, puede redireccionar a los usuarios del segmento con anuncios adicionales o evitar que los usuarios del segmento reciban anuncios adicionales.

>[!NOTE]
>
>Para rastrear los ID de usuario de las solicitudes de exclusión de la venta de consumidores en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA), cree una [Segmento de exclusión de la venta de CCPA](ccpa-opt-out-segment-create.md).

1. Cree el segmento:

   1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

   1. Introduzca un único **[!UICONTROL Segment Name]**.

   1. Para el **[!UICONTROL Segment Type]**, seleccione *[!UICONTROL Custom]*.

   1. Introduzca el **[!UICONTROL Segment Window]**, que es el número de días que la cookie de un usuario permanece en el segmento.

      La ventana predeterminada es de 45 días. Introduzca un valor de uno (1) a 365.

   1. Haga clic **[!UICONTROL Save]**.

1. Copie e implemente etiquetas para realizar el seguimiento del segmento, según sea necesario:

   1. Volver a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Mantenga el cursor sobre la fila del segmento y haga clic en **[!UICONTROL Get Pixel]**.

      * Para realizar un seguimiento de los visitantes de escritorio y móviles de una página web:

         1. Copie la etiqueta de seguimiento de vista de página, que está etiquetada como &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Proporcione la etiqueta al anunciante o al contacto del sitio web para su implementación.

            Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.
      * Para hacer un seguimiento de los usuarios expuestos a una unidad de publicidad en dispositivos de escritorio, móviles o CTV:

         1. Copie la etiqueta de seguimiento de impresiones, que tiene la etiqueta &quot;[!UICONTROL Desktop or mobile ads].&quot;


1. Agregue la etiqueta a la variable [!UICONTROL Pixel] para cada anuncio relevante o para el [!UICONTROL Event Pixels] de la sección [[!UICONTROL Tracking] configuración para cada ubicación relevante](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Una vez implementada una etiqueta de seguimiento, puede utilizar el segmento en los objetivos de audiencia o las exclusiones para cualquier ubicación.

>[!TIP]
>
>Realice un seguimiento del tamaño del segmento a medida que se rastrea a los usuarios.

>[!MORELIKETHIS]
>
>* [Acerca de Audience Management](audience-about.md)
>* [Editar información del segmento](segment-edit.md)
>* [Eliminar un segmento](segment-delete.md)
>* [Visualización de los píxeles de seguimiento de un segmento](segment-view-pixels.md)
>* [Compartir o dejar de compartir un segmento](segment-share.md)
>* [Creación e implementación de un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)

