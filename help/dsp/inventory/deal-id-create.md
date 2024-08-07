---
title: Creación manual de detalles de ID de acuerdo
description: Obtenga información sobre cómo introducir manualmente los detalles de un ID de acuerdo.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Creación manual de detalles de ID de acuerdo

1. En el menú principal, haga clic en **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Encima de la tabla de datos, haga clic en **[!UICONTROL Create]** y seleccione **[!UICONTROL Deal ID]**.

1. Escriba la [configuración de la oferta](deal-id-settings.md):

   1. En la sección [!UICONTROL Deal ID basics], especifique los detalles de la oferta y los anunciantes que pueden acceder a la oferta. Para ofertas garantizadas, también debe especificar las fechas de vuelo planificadas y el número estimado de impresiones, solo para fines de seguimiento.

      Puede rastrear el ritmo de las ofertas garantizadas incluyendo la columna de gasto &quot;Ritmo de impresión PG&quot; en la vista Inventario > Ofertas.

   1. (Solo usuarios administradores; opcional) En la sección [!UICONTROL Technical], edite la configuración predeterminada según sea necesario.

   1. Haga clic en **[!UICONTROL Save]**.

1. (Solo ofertas garantizadas) Seleccione los anuncios que desea utilizar para la oferta (o el píxel 1x1 para los anuncios administrados por el editor) y cree una ubicación programática garantizada (PG) predeterminada.

   Las ubicaciones de PG predeterminadas garantizan que la oferta siempre devuelva una oferta por cada solicitud de oferta. Si no crea una ubicación PG predeterminada, las ubicaciones que se dirijan a la oferta no realizarán pujas a menos que estén configuradas correctamente. Siempre debe crear una ubicación PG predeterminada. En la vista [!UICONTROL Placements], las ubicaciones de PG predeterminadas tienen un valor de columna [!UICONTROL Sub-type] de &quot;[!UICONTROL PG Default]&quot;.

   Si lo desea, puede utilizar la oferta como destino de inventario en ubicaciones adicionales, pero debe configurarlas correctamente para realizar pujas.

   1. En la configuración de [!UICONTROL Ad & Campaign Selection], seleccione los anuncios que se usarán en la oferta:

      1. Seleccione el anunciante, la campaña y el tipo de anuncio. Si lo desea, seleccione un estado de anuncio según el cual filtrar los anuncios.

      1. En la lista de anuncios disponibles, seleccione la casilla de verificación situada junto a cada anuncio que desee utilizar para la oferta.

         Para cada anuncio administrado por el editor, se aplica automáticamente un píxel de seguimiento 1x1 después de seleccionar un anunciante y una campaña.

      1. Haga clic en **[!UICONTROL Apply]**.

   1. En la pantalla de configuración de ubicación:

      1. Introduzca el nombre de la ubicación.

      1. (Opcional) Edite la [configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md), incluida la sobrescritura de la oferta predeterminada, que se rellena automáticamente con el valor CPM de la oferta; el cambio del intervalo de fecha; o la adición de más anuncios.

      El acuerdo se establece automáticamente como objetivo en la sección Destinos de inventario. Todas las demás opciones de segmentación no son aplicables.

      1. Haga clic en **[!UICONTROL Create placement]**.

Después de crear la oferta, puede utilizarla como objetivo de inventario para varias ubicaciones.

>[!NOTE]
>
> No es necesario que envíe la etiqueta de la oferta al editor para su verificación.

>[!TIP]
>
>* En la vista [!UICONTROL Inventory] > [!UICONTROL Deals], la columna [!UICONTROL Pacing & Budget] muestra el ritmo de la oferta hasta la fecha de vuelo especificada y el objetivo de impresión.
>
>* Si el ritmo de entrega es insuficiente o excesivo, póngase en contacto con el editor para ajustar el volumen que está enviando a través de la oferta.

>[!MORELIKETHIS]
>
>* [Configuración de ID de acuerdo manual](deal-id-settings.md)
>* [Configurar una oferta garantizada programática](programmatic-guaranteed-set-up.md)
>* [Enviar un anuncio para obtener un acuerdo programático garantizado con [!DNL FreeWheel]](freewheel-submit.md)
>* [Acerca de las ofertas garantizadas mediante programación](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
