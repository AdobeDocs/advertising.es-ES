---
title: Acerca de [!UICONTROL Deal ID Inbox]
description: Obtenga información acerca de [!UICONTROL Deal ID inbox] función, que le permite aceptar acuerdos privados en los que ya ha negociado con editores [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conocido como [!DNL AdX]), and [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Acerca de [!UICONTROL Deal ID Inbox]

DSP El Advertising [!UICONTROL Deal ID inbox] DSP permite configurar rápidamente ofertas que se han importado de los editores a través de plataformas de suministro (SSP), de modo que no es necesario configurar cada oferta manualmente. Puede aceptar las ofertas de inventario privado garantizadas y no garantizadas que ya ha negociado con los editores [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conocido como [!DNL AdX]), y [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]) desde el [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>DSP DSP Advertising es la primera vez que se integra con el [!DNL FreeWheel] API.

En el [!UICONTROL Deal ID inbox], puede ver los detalles de la oferta tal como los ve su editor, acelerar la configuración de la oferta y evitar errores de entrada manual.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP El cliente actualiza automáticamente todos los detalles de la oferta todos los días a las 4:30 a.m. EST. También actualiza todos los [!DNL FreeWheel] ofertas y actualizaciones de ofertas existentes de [!DNL Google] y [!DNL Magnite DV+] cada hora. También puede actualizar manualmente los detalles de la oferta para rellenar nuevas ofertas en cualquier momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Para ofertas programáticas garantizadas mediante [!DNL Google Authorized Buyers], debes cumplir al menos el 90% de tu presupuesto o tu cuenta perderá el acceso a [!DNL Google] ofertas en [!UICONTROL Deal ID inbox].

## Implementación de [!UICONTROL Deal ID Inbox]

Para recibir sus ofertas en la [!UICONTROL Deal ID inbox]DSP , las cuentas de SSP deben asignar la cuenta de SSP de la organización a la cuenta de la cuenta de la cuenta de la organización de SSP. DSP Puede compartir los nombres de cuenta de la organización con los SSP relevantes. Póngase en contacto con el equipo de cuenta de Adobe para obtener instrucciones.

DSP Durante las negociaciones, dile al editor que envíe la oferta a tu comprador en lugar de a la cuenta de la empresa matriz de la que se ha realizado el contrato. El identificador de la operación puede ser un nombre o un ID, según el SSP.

## Acciones que puede llevar a cabo con sus ofertas

* **Revisar ofertas** para verificar que el SSP ha enviado al editor, las fechas de vuelo, el CPM y otros detalles de la operación correctos. DSP Si el editor ha cometido un error, póngase en contacto con ellos fuera de la empresa para que puedan corregir y reenviar el acuerdo.

* **Aceptar ofertas** después de la revisión, y ya no aparecerán en el [!UICONTROL Deal ID inbox]. Las ofertas aceptadas se enumeran en [!UICONTROL Inventory] > [!UICONTROL Deals] y están listos para segmentar en las ubicaciones de los anunciantes.

* **Ignorar ofertas** que no son necesarios o no se solicitan. Las ofertas ignoradas se mueven al [!UICONTROL Ignored Deals] dentro de la [!UICONTROL Deal ID inbox], que sirve como archivo. DSP No avisa a los SSP y a los editores cuando ignora un acuerdo.

* **Modificar detalles de ofertas ya aceptadas** de [!UICONTROL Inventory] > [!UICONTROL Deals] (no en el [!UICONTROL Deal ID inbox]). Del mismo modo, cuando los editores envían cambios a las ofertas, los anunciantes son responsables de implementar esos cambios en [!UICONTROL Inventory] > [!UICONTROL Deals] porque la variable [!UICONTROL Deal ID inbox] no sincroniza los cambios de los SSP después de configurar las ofertas.

## ¿Qué tipos de acuerdos no se pueden aceptar?

Cuando un anuncio de acuerdo no incluye una ![Aceptar](/help/dsp/assets/accept.png) o un [!UICONTROL Accept] botón, no puede aceptarlo desde el [!UICONTROL Deal ID inbox]. En su lugar, puede [crear los detalles del ID de la oferta manualmente](/help/dsp/inventory/deal-id-create.md).

No puede aceptar los siguientes tipos de ofertas:

* [!DNL Google] ofertas que no están en USD.

* [!DNL Magnite DV+] ofertas que no están en USD

* [!DNL FreeWheel] ofertas que no estén en la divisa de la cuenta.

* Ofertas que tengan una fecha de finalización anterior a hoy.

* Antiguo [!DNL Magnite DV+] ofertas que se etiquetaron como &quot;varios tipos de medios&quot;.

Los detalles del acuerdo incluyen la razón por la que el acuerdo no está disponible para aceptar.

>[!MORELIKETHIS]
>
>* [Aceptar un acuerdo en la bandeja de entrada de Deal ID](deal-id-inbox-accept.md)
>* [Resumen de las Funciones de Inventario](inventory-overview.md)
