---
title: Creación e implementación de un segmento personalizado
description: Obtenga información sobre cómo crear e implementar un segmento personalizado para rastrear usuarios expuestos a anuncios o usuarios que visitan sus páginas web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
TQID: https://experienceleague.adobe.com/Xemx2oExt-bNTgJPVkDaWfillRBAZAfOPQx1eJYxupw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: c193c532-b70e-4556-bde7-857186cbe140
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 694
ht-degree: 0%

---

# Creación e implementación de un segmento personalizado

Puede recopilar sus propios datos de audiencia de origen creando e implementando un segmento de DSP personalizado. Puede utilizar el segmento para rastrear a) a los usuarios expuestos a anuncios desde dispositivos de escritorio y móviles y b) a los usuarios que visitan páginas web específicas. Más adelante, puede redireccionar a los usuarios del segmento con anuncios adicionales o evitar que los usuarios del segmento reciban anuncios adicionales.

>[!NOTE]
>
>Para rastrear los ID de usuarios de las solicitudes de exclusión de la venta de consumidores en su sitio web, de conformidad con la Ley de Privacidad del Consumidor de California (CCPA), cree un [segmento de exclusión de la venta de CCPA](ccpa-opt-out-segment-create.md).

## Requisitos previos para que los segmentos realicen un seguimiento de los ID5

*característica de Beta*

* Antes de generar un segmento para rastrear usuarios asociados con ID5 ID, firme un acuerdo con [!DNL ID5] y obtenga el ID de socio de su organización. Póngase en contacto con el equipo de su cuenta de Adobe para obtener instrucciones.

* Para realizar mediciones en Adobe Analytics, debe:

   1. Complete todos los [requisitos previos para implementar [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md), y asegúrese de que el [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se estén llenando en sus URL de seguimiento.

   1. Agregue el siguiente parámetro a sus páginas web antes o dentro del [código JavaScript necesario para [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md), en cualquier lugar antes de que se inicialice el último servicio de eventos.

      ```window.id5PartnerId=ID5_PartnerID;```

      Ejemplo:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

      Consulte &quot;[Formato de las etiquetas de seguimiento de conversión de JavaScript versión 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)&quot; y &quot;[Formato de las etiquetas de seguimiento de conversión de JavaScript versión 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)&quot; para ver el formato de etiqueta completo.

   1. Use cualquier herramienta de depuración del explorador para comprobar que cada llamada se inicia en el dominio `lasteventf-tm.everesttech.net` y contiene el parámetro `_les_id5` con un ID. de ID5 cifrado como valor.

## Creación e implementación de un segmento personalizado

1. Cree el segmento:

   1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

   1. Escriba un(a) **[!UICONTROL Segment Name]** único.

   1. Para **[!UICONTROL Segment Type]**, seleccione *[!UICONTROL Custom]*.

   1. Escriba **[!UICONTROL Lookback Window]**, que es el número de días que la cookie de un usuario permanece en el segmento.

      La ventana predeterminada es de 45 días. Introduzca un valor de uno (1) a 365.

   1. Haga clic en **[!UICONTROL Advanced]** para expandir la configuración avanzada y, a continuación, seleccione los tipos de identificadores de usuario que la etiqueta de segmento rastrea:

      * *[!UICONTROL Cookies]:* (Valor predeterminado) La etiqueta de segmento realiza el seguimiento de las cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* La etiqueta de segmento rastrea [!DNL ID5] ID. No se incurre en cargos por impresiones entregadas a ID universales.

        **[!UICONTROL Terms of Service]:** Los términos del contrato de servicio para usar identificadores universales. Usted u otro usuario de la cuenta de DSP deben aceptar los términos una vez, antes de poder usar un ID universal para un nuevo tipo de ID. Para los clientes con contratos de servicio administrado, su equipo de cuenta de Adobe recibirá su consentimiento y aceptará los términos en nombre de su organización. Para leer los términos, haga clic en **>**. Para aceptar los términos, desplácese hasta la parte inferior de los términos y haga clic en **[!UICONTROL Accept]**.

   1. Haga clic en **[!UICONTROL Save]**.

1. Copie e implemente etiquetas para realizar el seguimiento del segmento, según sea necesario:

   1. Volver a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Mantenga el cursor sobre la fila del segmento y haga clic en **[!UICONTROL Get Pixel]**.

      * Para realizar un seguimiento de los visitantes de escritorio y móviles de una página web:

         1. Copie la etiqueta de seguimiento de vista de página, con la etiqueta &quot;[!UICONTROL Desktop or mobile websites]&quot;.

         1. (Etiquetas para segmentos que rastrean [!DNL ID5] ID) En la etiqueta copiada, reemplace `ID5_PARTNER_ID` con el ID de socio que [!DNL ID5] asignó a su organización.

            Por ejemplo, si el ID del socio ID5 es `abcde` y la etiqueta de segmento generada es

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            a continuación, reemplace `ID5_PARTNER_ID` por `abcde` dentro de la etiqueta para obtener lo siguiente:

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Su organización recibió el ID de socio cuando firmó un acuerdo con [!DNL ID5]. Si no conoce su ID de socio, póngase en contacto con el equipo de cuenta de Adobe.

            Este paso no es necesario para que las etiquetas realicen un seguimiento de los ID de [!DNL ID5] de los usuarios expuestos a una unidad de publicidad en el escritorio o en dispositivos móviles.

         1. Proporcione la etiqueta al anunciante o al contacto del sitio web para su implementación.

            Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.

      * Para hacer un seguimiento de los usuarios expuestos a una unidad de publicidad en equipos de escritorio o dispositivos móviles:

         1. Copie la etiqueta de seguimiento de impresiones, con la etiqueta &quot;[!UICONTROL Desktop or mobile ads]&quot;.

         1. Agregue la etiqueta a la ficha [!UICONTROL Pixel] para cada anuncio relevante o a la sección [!UICONTROL Event Pixels] de la configuración [[!UICONTROL Tracking] para cada ubicación relevante](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Una vez implementada una etiqueta de seguimiento, puede utilizar el segmento en los objetivos de audiencia o las exclusiones para cualquier ubicación.

>[!TIP]
>
>Realice un seguimiento del tamaño del segmento a medida que se rastrea a los usuarios.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de audiencias](audience-about.md)
>* [Editar información de segmento](segment-edit.md)
>* [Eliminar un segmento](segment-delete.md)
>* [Ver píxeles de seguimiento de un segmento](segment-view-pixels.md)
>* [Compartir o dejar de compartir un segmento](segment-share.md)
>* [Crear e implementar un segmento [!UICONTROL CCPA Opt-Out-of-Sale]](ccpa-opt-out-segment-create.md)
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
