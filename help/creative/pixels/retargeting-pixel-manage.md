---
title: Administrar píxeles de retargeting
description: Aprenda a crear e implementar píxeles de retargeting para utilizarlos como objetivos para experiencias de publicidad.
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: ed3bf0200d3d3b31ef80c790c4e702914459c521
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Administrar píxeles de retargeting

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

Puede crear un píxel de resegmentación para identificar a los visitantes en las páginas de aterrizaje de un anunciante o en las páginas de conversión mediante cookies de usuario o ID universales. El píxel realiza el seguimiento del evento más reciente que el visitante realiza en una página y captura atributos específicos que la página está rastreando para esos visitantes. Una vez creado el píxel, genere una etiqueta de píxel para insertarla en las páginas web relevantes y así comenzar a rastrear visitantes.<!-- Note to self: surfer id=cookie or universal ID -->

A continuación, puede utilizar el píxel como destino para cualquier elemento creativo dentro de una experiencia publicitaria y mostrar anuncios únicamente a los usuarios con atributos especificados que hayan visitado previamente las páginas web asociadas con el píxel. Por ejemplo, puede dirigirse a visitantes que vean zapatos rojos de tamaño 10 si las páginas web rastrean esos valores de atributos.<!-- better example? Make sure they match attribute examples below -->: los destinos de nivel de experiencia se aplican junto con las opciones de segmentación de DSP; el comportamiento de la segmentación jerárquica puede variar en DSP.

Los perfiles de redireccionamiento se almacenan durante 180 días.

Ejemplo de píxel:

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative] solo admite identificadores universales para Advertising DSP.
>* También puedes usar audiencias de origen de Adobe Audience Manager y Adobe Analytics como [objetivos creativos para tus experiencias](/help/creative/experiences/experience-settings-targeting.md).
>* Cuando utiliza una experiencia como anuncio en una ubicación de Advertising DSP, puede segmentar la ubicación a todas las audiencias disponibles en DSP. También puede [crear etiquetas de segmento de audiencia personalizadas](/help/dsp/audiences/custom-segment-create.md) para rastrear a todos los visitantes a páginas de aterrizaje específicas y luego usar esos segmentos como destinos creativos para una ubicación. Advertising DSP aplica una segmentación a nivel de anuncio sobre la segmentación a nivel de ubicación (no en su lugar).
>* Los visitantes del sitio web que hayan excluido el seguimiento para la segmentación de anuncios no reciben anuncios con contenido creativo personalizado basado en segmentos de audiencia o perfiles de retargeting.

## Crear un píxel de retargeting

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Encima de la tabla de datos, haga clic en **[!UICONTROL Creative]** y seleccione > **[!UICONTROL Retargeting Pixel]**.

1. Especifique la [configuración de píxeles de redireccionamiento](#retargeting-pixel-settings).

1. Haga clic en **[!UICONTROL Save]**.

1. [Genere la etiqueta de píxel](#retargeting-pixel-generate) para proporcionar al anunciante o al contacto del sitio web.

   La etiqueta de píxeles de redireccionamiento debe ser la última acción de la página.<!-- verify here and below -->

   Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.

## Edición de un píxel de retargeting

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Mantenga el cursor sobre el nombre del píxel y haga clic en **[!UICONTROL Edit]**.

1. Edite la [configuración de píxeles de retargeting](#retargeting-pixel-settings).

1. Haga clic en **[!UICONTROL Save]**.

1. [Genere la etiqueta de píxel](#retargeting-pixel-generate) para proporcionar al anunciante o al contacto del sitio web que pueda reemplazar la etiqueta original.

   La etiqueta de píxel de redireccionamiento debe ser la última acción de la página de aterrizaje.

   Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.

## Generación de una etiqueta para un píxel de resegmentación {#retargeting-pixel-generate}

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Mantenga el cursor sobre el nombre del píxel y haga clic en **[!UICONTROL Generate Tag]**.

1. Haga clic en **[!UICONTROL Copy to Clipboard]** para copiar la etiqueta en el portapapeles del equipo, desde el cual puede pegar el texto en un archivo para guardarlo.

1. En la etiqueta de píxeles, especifique un valor para cada atributo en las secciones `<img src>` y `<script src>` reemplazando cada &quot;`Insert <attribute>`&quot; por un valor. Especifique un ID de socio ID5 si la etiqueta captura un ID universal.

   Si agrega atributos adicionales manualmente, incluya la codificación de la URL.

   Por ejemplo, si ha incluido los atributos &quot;categoría&quot;, &quot;color&quot; y &quot;tamaño&quot; y los ID universales de captura ID5, la etiqueta de píxeles incluye los siguientes parámetros: `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` y `&id5pid=--Insert ID5_PARTNER_ID--`. Para dirigirse a los usuarios que seleccionen sandalias rojas en el tamaño 10, cambie los parámetros en la etiqueta de imagen y en la etiqueta de script a `&ut1=sandals&ut2=red&ut3=10`, y también introduzca su ID5 de socio en la etiqueta de script, como `&id5pid=0123456789`.

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. Proporcione la etiqueta de píxel completada al anunciante o al contacto del sitio web, junto con una lista de las páginas de aterrizaje relevantes en las que insertarla.

   La etiqueta de píxel de redireccionamiento debe ser la última acción de la página de aterrizaje.

   Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.

## Eliminar un píxel de resegmentación

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Mantenga el cursor sobre el nombre del píxel y haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Configuración de píxeles de redireccionamiento {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** El nombre del píxel. **Nota:** La etiqueta de píxeles incluye el identificador de píxel (`pxId=<ID>`), no el nombre de píxel.

**[!UICONTROL Advertiser]:** (solo lectura para píxeles existentes) El anunciante para el que se realiza el seguimiento del píxel.

**[!UICONTROL Attribute 1]:** Atributo que se va a incluir en la etiqueta de píxeles, como &quot;SKU&quot;, &quot;categoría&quot;, &quot;tamaño&quot; u otros atributos de la página o del producto mostrado en la página. Especifique un valor para el atributo en la etiqueta de píxeles antes de insertarlo en las páginas web relevantes.

Cuando dirige experiencias de anuncio a usuarios expuestos al píxel, la configuración de segmentación especifica los valores de atributo que deben estar presentes para mostrar los elementos creativos.

**[!UICONTROL Attribute 2]**, **[!UICONTROL Attribute 3]**, **[!UICONTROL Attribute 4]**, **[!UICONTROL Attribute 5]:** (Opcional) Atributos adicionales para incluir en la etiqueta de píxeles. Especifique un valor para cada atributo adicional en la etiqueta de píxeles antes de insertarlo en las páginas web relevantes.

Cuando dirige experiencias de anuncio a usuarios expuestos al píxel, la configuración de segmentación especifica los valores de atributo que deben estar presentes para mostrar los elementos creativos.

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** (solo nuevos píxeles; opcional) Tipos de ID universales para la etiqueta de píxeles que se va a rastrear:

* *[!UICONTROL ID5]:* La etiqueta de píxeles rastrea [!DNL ID5] ID. No se incurre en cargos por impresiones entregadas a ID universales.

* *[!UICONTROL Ramp ID]:* La etiqueta de píxeles rastrea [!DNL Ramp IDs]. No se incurre en cargos por impresiones entregadas a ID universales.

Para utilizar esta función, usted u otro usuario de la cuenta de DSP deben aceptar el contrato de términos de servicio para usar un ID universal una vez, antes de poder usar un ID universal para un nuevo tipo de ID. Para los clientes con contratos de servicio administrado, su equipo de cuenta de Adobe recibirá su consentimiento y aceptará los términos en nombre de su organización. Para leer los términos, haga clic en **[!UICONTROL Terms of Service]**. Para aceptar los términos, desplácese hasta la parte inferior de los términos y haga clic en **[!UICONTROL Accept]**.

>[!MORELIKETHIS]
>
>* [Configuración de experiencia de anuncio segmentada](/help/creative/experiences/experience-settings-targeting.md)
>* [Acerca de las experiencias publicitarias](/help/creative/experiences/experience-about.md)
