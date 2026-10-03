---
title: Enviar un anuncio de una oferta de PG a [!DNL FreeWheel]
description: Aprenda a solicitar la aprobación de un anuncio para un acuerdo programático garantizado con un editor de [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
TQID: 'https://experienceleague.adobe.com/f6Cu6mG77YOjwshI4xVbkLSkykAhqXonfSMg5ynDK5g'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 20c71a28-1f3b-56af-ad52-f3281489a219
    internal-label: DSP Private Inventory
  - id: 85825b7c-c02c-536d-b821-66dc33454fb8
    internal-label: DSP Deal IDs
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
    internal-label: Private Inventory
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
    internal-label: Deal IDs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%
---
# Enviar un anuncio para obtener una oferta programática garantizada a [!DNL FreeWheel]

*Sólo cuentas con el permiso Programmatic Guaranteed [!DNL FreeWheel]*

Una vez que [aceptes un acuerdo programático garantizado con un editor en FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), incluida la selección de un anuncio y la creación de la ubicación programática predeterminada garantizada que se usará para el acuerdo, debes enviar el anuncio a [!DNL FreeWheel] para su aprobación.

>[!PREREQUISITES]
>
>Trabaje con su equipo de cuenta de Adobe para asegurarse de que su cuenta de [!DNL DSP] tenga permiso para utilizar el flujo de trabajo programático garantizado de [!DNL FreeWheel].

1. Copie la clave de anuncio para el anuncio utilizado con la oferta [!DNL FreeWheel]:

   1. Haga clic en el nombre de la campaña.

   1. En el submenú, haga clic en **[!UICONTROL Ads]**.

   1. Haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]** junto al nombre del anuncio.

   1. Una vez abierta la configuración del anuncio, copie la clave de anuncio alfanumérica en la dirección URL que se muestra en la barra de direcciones del explorador.

      Por ejemplo, en la siguiente URL, la clave de anuncio es `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Enviar el anuncio a [!DNL FreeWheel]:

   1. Realice una de las acciones siguientes:

      * Junto al nombre del anuncio, haga clic en **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * En el menú principal, haga clic en **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. En la fila de la oferta, haga clic en ![Menú de opciones](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Compruebe el identificador de la oferta, escriba el **[!UICONTROL Ad Key]** que copió en el paso 1 y, a continuación, haga clic en **[!UICONTROL Submit]**.

   El anuncio debe enviarse y aprobarse antes de ejecutarse.

1. [Compruebe el estado de envío del anuncio](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Información general sobre la configuración de ofertas programáticas garantizadas en [!DNL FreeWheel]](freewheel-overview.md)
>* [Aceptar un trato en [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Comprueba el estado de los anuncios para una [!DNL FreeWheel] oferta de PG](freewheel-check-status.md)
>* [Códigos de error para [!DNL FreeWheel] envíos de anuncios](freewheel-error-codes.md)
