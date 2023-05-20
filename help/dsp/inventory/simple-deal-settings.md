---
title: '[!UICONTROL Simple Ad Serving] Configuración del acuerdo'
description: Obtenga información acerca de la configuración disponible para [!UICONTROL Simple Ad Serving] ofertas.
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Configuración de acuerdo

## Nuevo [!UICONTROL Simple Ad Serving] Acuerdos

### [!UICONTROL Select Ad Source]

| Parámetro | Descripción |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Tipo de medio de esta oferta: *[!UICONTROL Video],* *[!UICONTROL Display],* o *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | El nombre del editor que está vendiendo este inventario. Busque un editor escribiendo al menos los dos primeros caracteres en el nombre. Para agregar un editor que no aparezca en la lista, póngase en contacto con el equipo de cuenta de Adobe. |
| **[!UICONTROL Advertiser]** | Un solo anunciante en la cuenta que puede acceder a esta oferta. Seleccione también la campaña y (opcionalmente) el paquete en el que está disponible la oferta. |
| **[!UICONTROL Media Quality Assessment?]** | DSP (Algunos usuarios) Habilita el anuncio para que se ejecute en otro para la verificación de terceros. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | La única opción es *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Solo nuevas ofertas) Si desea:<ul><li>*[!UICONTROL Create New]:* Para crear un anuncio para este acuerdo.</li><li>*[!UICONTROL Select Ads]:* Para usar un anuncio existente para este acuerdo.</li></ul> |
| **[!UICONTROL Ad Type]** | El tipo de anuncio de esta oferta. Si va a crear anuncios para la oferta, incluya el tamaño del anuncio o la duración, según se solicite. Las opciones disponibles varían según el tipo de medio. |

{style="table-layout:auto"}

### [!UICONTROL Select Ad(s)]

(Cuando usa anuncios existentes) Los anuncios que se incluirán en la oferta. Seleccione la casilla de verificación situada junto a cada anuncio que desee incluir.

### [!UICONTROL Select & Upload [Media Type]]

(Solo anuncios nuevos) Pantallas para crear un nuevo [anuncio de terceros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| Parámetro | Descripción |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | El coste por 1000 impresiones (CPM), tal como se refleja en la tarjeta de tarifas de su contrato. Póngase en contacto con el equipo de cuenta de Adobe para obtener este valor. <br><br>Especifique también la moneda de la operación. DSP Todos los usuarios pueden seleccionar el dólar estadounidense o, si el SSP admite monedas adicionales, la moneda de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la red. |
| **[!UICONTROL Third Party Billed Fees]** | (Opcional) Una tarifa estática de terceros que se rastreará como un coste no facturable y la moneda de la operación.<br><br>DSP Todos los usuarios pueden seleccionar el dólar estadounidense o, si el SSP admite monedas adicionales, la moneda de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de la red. **NOTA:** Las tarifas facturables se reflejan en la [!UICONTROL Net CPM] métrica. |
| **[!UICONTROL Third Party Fee Description]** | (Opcional) Una descripción de las tarifas de terceros. |
| **[!UICONTROL Flight Dates]** | Las fechas de inicio y finalización del tráfico que utiliza esta oferta. Las fechas de vuelo deben incluirse dentro de las fechas de vuelo de la campaña. Las etiquetas de anuncio devuelven una respuesta solo durante el vuelo especificado.<br><br> La práctica recomendada es crear una campaña de servicio de publicidad simple independiente con una duración de año y crear píxeles de seguimiento dentro de ella. |
| **[!UICONTROL Impressions]** | (Opcional) El número estimado de impresiones que espera ejecutar con esta oferta. Este valor se utiliza únicamente con fines de seguimiento y para marcar cuándo se cumplen los objetivos de entrega; el editor controla la entrega de publicidad real. DSP La práctica recomendada es introducir un número elevado de impresiones para mantener la etiqueta activa en, de modo que se pueda renovar o ampliar si es necesario. |
| **[!UICONTROL Deal Name]** | El nombre del trato. Introduzca un nombre o seleccione *[!UICONTROL Auto Generate Deal Name]* DSP para permitir que los clientes generen un nombre basado en los detalles de la oferta.<br><br>Ejemplo de nombre generado automáticamente: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Solo lectura) Los anuncios que forman parte de la oferta. Para editar un anuncio, haga clic en su nombre. Para eliminar un anuncio de la oferta, haga clic en **[!UICONTROL X]** junto al nombre del anuncio. |

{style="table-layout:auto"}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [Acerca de [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Crear un [!UICONTROL Simple Ad Serving] Acuerdo](simple-deal-create.md)
>* [Editar [!UICONTROL Simple Ad Serving] Configuración de acuerdo](simple-deal-edit.md)
>* [Ver un informe detallado de una oferta](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
