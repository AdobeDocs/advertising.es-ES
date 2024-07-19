---
title: Acerca de [!UICONTROL Deal ID Inbox]
description: Obtenga información acerca de la característica [!UICONTROL Deal ID inbox], que le permite aceptar ofertas privadas que ya ha negociado con los editores el  [!DNL FreeWheel], [!DNL Google Authorized Buyers]  (anteriormente conocido como  [!DNL AdX]), and [!DNL Magnite DV+] (anteriormente  [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Acerca de [!UICONTROL Deal ID Inbox]

Advertising DSP DSP [!UICONTROL Deal ID inbox] le permite configurar rápidamente ofertas que se han importado desde editores a través de plataformas de suministro (SSP), de modo que no tenga que configurar cada oferta manualmente. Puede aceptar los acuerdos de inventario privado garantizados y no garantizados que ya ha negociado con los editores de [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conocido como [!DNL AdX]) y [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]) de [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP DSP es la primera vez que se integra con la API de [!DNL FreeWheel] en el proceso de integración de la interfaz de usuario.

En [!UICONTROL Deal ID inbox], puede ver los detalles de la oferta tal como los ve su editor, acelerar la configuración de la oferta y evitar errores de entrada manual.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP El cliente actualiza automáticamente todos los detalles de la oferta todos los días a las 4:30 a.m. EST. También actualiza todas las [!DNL FreeWheel] ofertas y actualiza las ofertas existentes de [!DNL Google] y [!DNL Magnite DV+] por hora. También puede actualizar manualmente los detalles de la oferta para rellenar nuevas ofertas en cualquier momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Para obtener ofertas programáticas garantizadas a través de [!DNL Google Authorized Buyers], debe entregar al menos el 90% del presupuesto o su cuenta perderá el acceso a [!DNL Google] ofertas en [!UICONTROL Deal ID inbox].

## Implementando [!UICONTROL Deal ID Inbox]

DSP Para recibir sus ofertas en [!UICONTROL Deal ID inbox], las cuentas de SSP deben asignar la cuenta de su organización a la cuenta de SSP de su organización, que es la cuenta de su cuenta de SSP. DSP Puede compartir los nombres de cuenta de la organización con los SSP relevantes. Póngase en contacto con el equipo de cuenta de Adobe para obtener instrucciones.

DSP Durante las negociaciones, dile al editor que envíe la oferta a tu comprador en lugar de a la cuenta de la empresa matriz de la que se ha realizado el contrato. El identificador de la operación puede ser un nombre o un ID, según el SSP.

## Acciones que puede llevar a cabo con sus ofertas

* **Revise las ofertas** para verificar que el SSP ha enviado el editor, las fechas de vuelo, el CPM y otros detalles de la oferta correctos. DSP Si el editor ha cometido un error, póngase en contacto con ellos fuera de la empresa para que puedan corregir y reenviar el acuerdo.

* **Acepta ofertas** después de revisarlas y ya no aparecerán en [!UICONTROL Deal ID inbox]. Las ofertas aceptadas se enumeran en [!UICONTROL Inventory] > [!UICONTROL Deals] y están listas para segmentarse en las ubicaciones de los anunciantes.

* **Ignorar ofertas** que no sean necesarias o no se hayan solicitado. Las ofertas omitidas se mueven a la ficha [!UICONTROL Ignored Deals] dentro de [!UICONTROL Deal ID inbox], que sirve como archivo. DSP No avisa a los SSP y a los editores cuando ignora un acuerdo.

* **Modificar detalles de ofertas ya aceptadas** de [!UICONTROL Inventory] > [!UICONTROL Deals] (no en [!UICONTROL Deal ID inbox]). Del mismo modo, cuando los editores envían cambios a las ofertas, los anunciantes son responsables de implementar esos cambios en [!UICONTROL Inventory] > [!UICONTROL Deals] porque [!UICONTROL Deal ID inbox] no sincroniza los cambios de los SSP después de configurar las ofertas.

## ¿Qué tipos de acuerdos no se pueden aceptar?

Cuando el anuncio de una oferta no incluye un icono ![Accept](/help/dsp/assets/accept.png) ni un botón [!UICONTROL Accept], no puedes aceptarlo desde [!UICONTROL Deal ID inbox]. En su lugar, puede [crear los detalles del ID de la oferta manualmente](/help/dsp/inventory/deal-id-create.md).

No puede aceptar los siguientes tipos de ofertas:

* [!DNL Google] ofertas que no están en USD.

* [!DNL Magnite DV+] ofertas que no están en USD

* [!DNL FreeWheel] ofertas que no están en la divisa de la cuenta.

* Ofertas que tengan una fecha de finalización anterior a hoy.

* Ofertas de [!DNL Magnite DV+] antiguas que se etiquetaron como &quot;varios tipos de medios&quot;.

Los detalles del acuerdo incluyen la razón por la que el acuerdo no está disponible para aceptar.

>[!MORELIKETHIS]
>
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Descripción general de las características de inventario](inventory-overview.md)
