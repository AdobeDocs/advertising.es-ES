---
title: Enviar un anuncio para un acuerdo de PG a  [!DNL FreeWheel]
description: Aprenda a solicitar la aprobación de un anuncio para un acuerdo programático garantizado con un publicador en  [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Enviar un anuncio para una oferta garantizada programática a [!DNL Freewheel]

*Sólo cuentas con el permiso Programmatic Guaranteed [!DNL FreeWheel]*

Una vez que [aceptes un acuerdo programático garantizado con un editor en FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), incluida la selección de un anuncio y la creación de la ubicación programática predeterminada garantizada que se usará para el acuerdo, debes enviar el anuncio a [!DNL Freewheel] para su aprobación.

>[!PREREQUISITES]
>
>Trabaje con su equipo de cuenta de Adobe para asegurarse de que su cuenta de [!DNL DSP] tenga permiso para usar el flujo de trabajo programático garantizado de [!DNL FreeWheel].

1. Copie la clave de anuncio para el anuncio utilizado con la oferta [!DNL Freewheel]:

   1. Haga clic en el nombre de la campaña.

   1. En el submenú, haga clic en **[!UICONTROL Ads]**.

   1. Haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]** junto al nombre del anuncio.

   1. Una vez abierta la configuración del anuncio, copie la clave de anuncio alfanumérica en la dirección URL que se muestra en la barra de direcciones del explorador.

      Por ejemplo, en la siguiente URL, la clave de anuncio es `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Enviar el anuncio a [!DNL Freewheel]:

   1. Realice una de las acciones siguientes:

      * Junto al nombre del anuncio, haga clic en **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * En el menú principal, haga clic en **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. En la fila de la oferta, haga clic en ![Menú de opciones](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Compruebe el identificador de la oferta, escriba el **[!UICONTROL Ad Key]** que copió en el paso 1 y, a continuación, haga clic en **[!UICONTROL Submit]**.

   El anuncio debe enviarse y aprobarse antes de ejecutarse.

1. [Compruebe el estado de envío del anuncio](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Información general sobre la configuración de ofertas garantizadas mediante programación en [!DNL Freewheel]](freewheel-overview.md)
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Comprobar el estado de los anuncios para [!DNL FreeWheel] Ofertas programáticas garantizadas](freewheel-check-status.md)
>* [Códigos de error para [!DNL Freewheel] Envíos de publicidad](freewheel-error-codes.md)
