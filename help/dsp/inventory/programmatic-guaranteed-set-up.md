---
title: Configurar una oferta garantizada programática
description: Aprenda a configurar un acuerdo programático garantizado (PG) que haya negociado con un editor.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: f887524a22dd5d665dcfc38b1a4ce2a1242638d7
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Configurar una oferta garantizada programática

*[Solo plataformas del lado de suministro compatibles](programmatic-guaranteed-about.md)*

DSP Después de negociar un acuerdo programático garantizado (PG) con un editor admitido, puede configurar el acuerdo dentro de las dos opciones, ya sea mediante el uso de la opción de configuración de la oferta de. [!DNL Deal ID inbox] o introduciendo manualmente los detalles de la operación.

>[!NOTE]
>
> Para las ofertas de PG, el editor gestiona todo el ritmo, el límite y la segmentación del presupuesto. DSP Todos los SSP que permiten PG a través de la confirmación de que el editor puede configurar un límite presupuestario.
>
> Configuración de acuerdos programáticos garantizados con editores en [!DNL FreeWheel] requiere permisos y pasos adicionales. Consulte &quot;[Información general sobre la configuración de ofertas garantizadas mediante programación en [!DNL FreeWheel]](freewheel-overview.md)&quot; para obtener más información.

## Configurar una oferta garantizada mediante programación utilizando [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

El siguiente método es el procedimiento preferido para [!DNL FreeWheel], [!DNL Google Authorized Buyers], y [!DNL Magnite DV+].

1. [Aceptar el trato](deal-id-inbox-accept.md).

1. Después de guardar la oferta, seleccione los anuncios (o el píxel de seguimiento 1x1 para los anuncios administrados por el editor) que se utilizarán para la oferta y cree una colocación predeterminada programática garantizada (PG), según se le solicite.

   La creación de una colocación de PG predeterminada para la oferta es obligatoria para entregar el 100% de su compra. DSP Este tipo de ubicación no tiene objetivo, por lo que puede devolver una oferta a cada solicitud de oferta del editor.

   * Si acepta una sola oferta, se le redirigirá automáticamente al flujo de trabajo de creación de ubicaciones predeterminado de PG.

     Todo [!DNL FreeWheel] los acuerdos se proponen como una sola operación.

   * Si acepta una propuesta con varios ID de acuerdo de PG, identifique cada ubicación predeterminada de PG que necesite crear. Una vez que haya creado todas las ubicaciones necesarias, el botón Continuar estará activado.

1. (Opcional) Oriente la oferta de PG en ubicaciones de PG o no PG adicionales haciendo clic en ![Menú Opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Una oferta puede dirigirse a varias ubicaciones que admitan cualquier combinación de tipos de medios (como TV, escritorio y audio conectados).

## Configurar manualmente una oferta garantizada mediante programación

Utilice este método para todos los demás SSP.

1. [Configurar manualmente los detalles del ID de la oferta](deal-id-create.md).

1. Después de guardar la oferta, seleccione los anuncios (o píxeles de seguimiento 1x1 para anuncios administrados por el editor) que se utilizarán para la oferta y cree una ubicación predeterminada PG, según se le solicite.

   La creación de una ubicación predeterminada de PG para la oferta es obligatoria para entregar el 100% de su compra. DSP Este tipo de ubicación no tiene objetivo, por lo que puede devolver una oferta a cada solicitud de oferta del editor.

1. (Opcional) Oriente la oferta de PG en ubicaciones de PG o no PG adicionales haciendo clic en ![Menú Opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Una oferta puede dirigirse a varias ubicaciones que admitan cualquier combinación de tipos de medios (como TV, escritorio y audio conectados).

>[!MORELIKETHIS]
>
>* [Acerca de Ofertas Programáticas Garantizadas](programmatic-guaranteed-about.md)
>* [Sugerencias para negociar un acuerdo garantizado programático](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Envíe un anuncio para un acuerdo garantizado programático con [!DNL FreeWheel]](freewheel-submit.md)
>* [Aceptar un acuerdo en la bandeja de entrada de Deal ID](deal-id-inbox-accept.md)
>* [Creación manual de detalles de ID de acuerdo](deal-id-create.md)
>* [Socios de SSP](ssp-partners.md)
>* [Resumen de las Funciones de Inventario](inventory-overview.md)
