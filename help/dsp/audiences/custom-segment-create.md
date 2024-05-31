---
title: Creación e implementación de un segmento personalizado
description: Obtenga información sobre cómo crear e implementar un segmento personalizado para rastrear usuarios expuestos a anuncios o usuarios que visitan sus páginas web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 99091cd673fd064908fec4a89e28d2ddb448e9a8
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Creación e implementación de un segmento personalizado

DSP Puede recopilar sus propios datos de audiencia de origen creando e implementando un segmento de audiencia personalizado de. Puede utilizar el segmento para rastrear a) a los usuarios expuestos a anuncios desde dispositivos de escritorio y móviles y b) a los usuarios que visitan páginas web específicas. Más adelante, puede redireccionar a los usuarios del segmento con anuncios adicionales o evitar que los usuarios del segmento reciban anuncios adicionales.

>[!NOTE]
>
>Para rastrear los ID de usuario de las solicitudes de exclusión de la venta de consumidores en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA), cree una [Segmento de exclusión de la venta de CCPA](ccpa-opt-out-segment-create.md).

## Requisitos previos para que los segmentos realicen un seguimiento de los ID5

*Función beta*

* Antes de generar un segmento para rastrear usuarios asociados con ID5 ID, debe firmar un acuerdo con [!DNL ID5] y obtenga el ID de socio de su organización. Póngase en contacto con el equipo de cuenta de Adobe para obtener instrucciones.

* Para realizar mediciones en Adobe Analytics, debe:

   1. Completar todo [requisitos previos para la implementación [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md), y asegúrese de que la variable [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se están rellenando en las direcciones URL de seguimiento.

   1. Agregue el siguiente parámetro a sus páginas web antes o dentro de la variable [Código JavaScript necesario para [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) — en cualquier lugar antes de que se inicialice el último servicio de eventos.

      ```window.id5PartnerId=Your_ID5_PartnerID;```

      Ejemplo:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

## Creación e implementación de un segmento personalizado

1. Cree el segmento:

   1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

   1. Introduzca un único **[!UICONTROL Segment Name]**.

   1. Para el **[!UICONTROL Segment Type]**, seleccione *[!UICONTROL Custom]*.

   1. Introduzca el **[!UICONTROL Lookback Window]**, que es el número de días que la cookie de un usuario permanece en el segmento.

      La ventana predeterminada es de 45 días. Introduzca un valor de uno (1) a 365.

   1. Clic **[!UICONTROL Advanced]** para expandir la configuración avanzada y, a continuación, seleccione los tipos de identificadores de usuario que rastrea la etiqueta de segmento:

      * *[!UICONTROL Cookies]:* (El valor predeterminado) La etiqueta de segmento rastrea las cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* La etiqueta de segmento rastrea [!DNL ID5] ID. No se incurre en cargos por impresiones entregadas a ID universales.

        **[!UICONTROL Terms of Service]:** El contrato de términos de servicio para usar un identificador universal. DSP Usted u otro usuario de la cuenta debe aceptar los términos una vez, a fin de poder usar identificadores universales para un nuevo tipo de ID. Para los clientes con contratos de servicio gestionado, su equipo de cuenta de Adobe recibirá su consentimiento y aceptará los términos en nombre de su organización. Para leer los términos, haga clic en **>**. Para aceptar los términos, desplácese hasta la parte inferior de los términos y haga clic en **[!UICONTROL Accept]**.

   1. Clic **[!UICONTROL Save]**.

1. Copie e implemente etiquetas para realizar el seguimiento del segmento, según sea necesario:

   1. Volver a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Mantenga el cursor sobre la fila del segmento y haga clic en **[!UICONTROL Get Pixel]**.

      * Para realizar un seguimiento de los visitantes de escritorio y móviles de una página web:

         1. Copie la etiqueta de seguimiento de vista de página, que está etiquetada como &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. (Etiquetas para segmentos que realizan un seguimiento) [!DNL ID5] (ID) En la etiqueta copiada, sustituya `ID5_PARTNER_ID` con el ID de socio que [!DNL ID5] asignado a su organización.

            Por ejemplo, si el ID del socio ID5 es `abcde` y la etiqueta de segmento generada es

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            luego reemplazar `ID5_PARTNER_ID` con `abcde` dentro de la etiqueta para obtener lo siguiente:

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Su organización recibió el ID de socio cuando firmó un acuerdo con [!DNL ID5]. Si no conoce su ID de socio, póngase en contacto con el equipo de cuenta de Adobe.

            Este paso no es necesario para que las etiquetas se rastreen [!DNL ID5] ID para usuarios expuestos a una unidad de publicidad en dispositivos de escritorio o móviles.

         1. Proporcione la etiqueta al anunciante o al contacto del sitio web para su implementación.

            Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.

      * Para hacer un seguimiento de los usuarios expuestos a una unidad de publicidad en equipos de escritorio o dispositivos móviles:

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
