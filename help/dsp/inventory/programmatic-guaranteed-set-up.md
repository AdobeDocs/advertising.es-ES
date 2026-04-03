---
title: Configurar un acuerdo programático garantizado
description: Aprenda a configurar un acuerdo programático garantizado (PG) que haya negociado con un editor.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
TQID: https://experienceleague.adobe.com/z7kz7dnCjgCGmlgDlFvbZXTn8d9-OMEunv-Sm-k6TzY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# Configurar un acuerdo programático garantizado

*[Solo se admiten plataformas del lado del suministro](programmatic-guaranteed-about.md)*

Después de negociar un acuerdo programático garantizado (PG) con un editor admitido, puede configurar el acuerdo en DSP mediante el uso de [!DNL Deal ID Inbox] o introduciendo manualmente los detalles del acuerdo.

>[!NOTE]
>
> Para las ofertas de PG, el editor gestiona todo el ritmo, el límite y la segmentación del presupuesto. Todos los SSP que permiten PG a través de DSP confirman que el editor puede configurar un límite presupuestario.
>
> La configuración de acuerdos programáticos garantizados con editores en [!DNL FreeWheel] requiere permisos y pasos adicionales. Consulte &quot;[Información general sobre la configuración de ofertas programáticas garantizadas en [!DNL FreeWheel]](freewheel-overview.md)&quot; para obtener más información.

## Configurar una oferta programática garantizada con [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

El siguiente método es el procedimiento preferido para [!DNL FreeWheel], [!DNL Google Authorized Buyers] y [!DNL Magnite DV+].

1. [Acepta el trato](deal-id-inbox-accept.md).

1. Después de guardar la oferta, seleccione los anuncios (o el píxel de seguimiento 1x1 para los anuncios administrados por el editor) que se utilizarán para la oferta y cree una colocación predeterminada programática garantizada (PG), según se le solicite.

   La creación de una colocación de PG predeterminada para la oferta es obligatoria para entregar el 100% de su compra. Este tipo de ubicación no tiene objetivo, por lo que DSP puede devolver una oferta a cada solicitud de oferta del editor.

   * Si acepta una sola oferta, se le redirigirá automáticamente al flujo de trabajo de creación de ubicaciones predeterminado de PG.

     Todas las [!DNL FreeWheel] ofertas se proponen como una sola oferta.

   * Si acepta una propuesta con varios ID de acuerdo de PG, identifique cada ubicación predeterminada de PG que necesite crear. Una vez que haya creado todas las ubicaciones necesarias, el botón Continuar estará activado.

1. (Opcional) Dirija la oferta PG a ubicaciones PG o no PG adicionales haciendo clic en ![Menú de opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Una oferta puede dirigirse a varias ubicaciones que admitan cualquier combinación de tipos de medios (como TV, escritorio y audio conectados).

## Configurar manualmente una oferta programática garantizada

Utilice este método para todos los demás SSP.

1. [Configurar manualmente los detalles del ID de la oferta](deal-id-create.md).

1. Después de guardar la oferta, seleccione los anuncios (o píxeles de seguimiento 1x1 para anuncios administrados por el editor) que desea utilizar para la oferta y cree una ubicación predeterminada PG, según se le solicite.

   La creación de una ubicación predeterminada de PG para la oferta es obligatoria para entregar el 100% de su compra. Este tipo de ubicación no tiene objetivo, por lo que DSP puede devolver una oferta a cada solicitud de oferta del editor.

1. (Opcional) Dirija la oferta PG a ubicaciones PG o no PG adicionales haciendo clic en ![Menú de opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Una oferta puede dirigirse a varias ubicaciones que admitan cualquier combinación de tipos de medios (como TV, escritorio y audio conectados).

>[!MORELIKETHIS]
>
>* [Acerca de ofertas programáticas garantizadas](programmatic-guaranteed-about.md)
>* [Sugerencias para negociar un acuerdo programático garantizado](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Envíe un anuncio para obtener un acuerdo programático garantizado con [!DNL FreeWheel]](freewheel-submit.md)
>* [Aceptar un trato en [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Crear manualmente los detalles del ID de la oferta](deal-id-create.md)
>* [socios de SSP](ssp-partners.md)
>* [Descripción general de las características del inventario en Advertising DSP](inventory-overview.md)
