---
title: Configuración del ID de acuerdo manual
description: Consulte las descripciones de la configuración de los ID de acuerdo introducidos manualmente.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Configuración del ID de acuerdo manual

| Sección | Parámetro | Descripción | Requerido | Editable |
|---------|-----------|-------------|----------|----------|
| [Detalles del acuerdo] | [!UICONTROL Deal name] | Nombre para identificar a su [!UICONTROL Deal ID] en Advertising DSP. DSP Escriba un nombre o seleccione **[!UICONTROL Auto-name]** para que los usuarios puedan generar un nombre basado en los detalles de la oferta.<br><br>Ejemplo de nombre generado automáticamente: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Sí | Sí |
| | [!UICONTROL External deal ID] | El ID utilizado por el editor y el SSP para identificar esta oferta. | Sí | No |
| | [!UICONTROL Publisher] | El nombre del editor que está vendiendo este inventario. | Sí | No |
| | [!UICONTROL SSP] | La plataforma de suministro (SSP) a través de la cual se ejecuta este acuerdo. | Sí | No |
| | [!UICONTROL Media type] | El tipo de medios comprados a través de este acuerdo: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* o *[!UICONTROL Publisher Managed]*. Las opciones varían según el SSP.<br><br> Si la oferta permite varios tipos de medios, seleccione el tipo de medios para la ubicación predeterminada cuando cree la oferta. Más adelante, puede cambiar el valor o simplemente [adjuntar una nueva ubicación con el tipo de medio adicional](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Sí | No |
| | [!UICONTROL Deal type] | El compromiso del acuerdo y la estructura de precios:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: el editor y usted no se han comprometido a realizar un número fijo de envíos de impresiones. El acuerdo especifica el precio mínimo del inventario, aunque el CPM puede fluctuar y aumentar dependiendo de las condiciones del mercado.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: el editor y usted no se han comprometido a realizar un número fijo de envíos de impresiones. El precio es a una tasa fija negociada.</li><li>*[!UICONTROL Guaranteed (fixed)]*: usted y el editor han acordado un número predefinido de impresiones, objetivos, fechas de vuelo y precio fijo.<br><br><b>Nota:</b> Las ofertas garantizadas requieren fechas de vuelo y un número especificado de impresiones en la sección [!UICONTROL Tracking]. También debe crear una ubicación programática garantizada (PG) predeterminada para la oferta y, opcionalmente, puede utilizar la oferta para otras ubicaciones en su lugar.</li></ul> | Sí | No |
| | [!UICONTROL CPM] | El coste negociado por 1000 impresiones (CPM). | Sí | Sí |
| | [Moneda] | La moneda para el acuerdo.<br><br>Todos los SSP aceptan ofertas en USD. DSP Cuando la plataforma compartida única acepta la moneda de su cuenta de la cuenta de la, también está disponible esa moneda. | Sí | No |
| | [!UICONTROL Billing method] | Todos los ID de acuerdo están financiados y facturados por [!DNL Adobe]. DSP El servicio paga a todos los proveedores de medios disponibles según el uso, gestiona las discrepancias con los proveedores y envía una factura consolidada a la cuenta. Esta opción incurre en cargos adicionales como se describe en la tarjeta de tarifas de la cuenta. | Sí | No |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | La dirección de correo electrónico de la cuenta de usuario que puede acceder a la oferta. | No | Sí |
| | [!UICONTROL Advertisers that can access this deal] | Los anunciantes específicos de la cuenta que pueden acceder a esta oferta.<br><br><b>Nota:</b> Puede compartir el acuerdo con anunciantes en cuentas adicionales desde la vista [!UICONTROL Deals]. En la fila de la oferta, haga clic en **[!UICONTROL #]**, haga clic en **[!UICONTROL share]** y, a continuación, comparta la oferta con una dirección de correo electrónico. | Sí | Sí |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Las fechas de inicio y finalización del tráfico que utiliza esta oferta. Estas fechas son solo para fines de seguimiento y no afectan a la publicación de anuncios.<br><br><b>Sugerencia:</b> En la vista [!UICONTROL Inventory] > [!UICONTROL Deals], la columna [!UICONTROL Pacing & Budget] muestra el ritmo de la oferta hasta la fecha de vuelo especificada y el objetivo de impresión. Si el ritmo de entrega es insuficiente o excesivo, póngase en contacto con el editor para ajustar el volumen que está enviando a través de la oferta. | Ofertas garantizadas: Sí<br>Ofertas no garantizadas: No | Sí |
| | [!UICONTROL Impressions] | (Opcional para ofertas no garantizadas) El número estimado de impresiones que espera ejecutar con esta oferta. Este valor es solo para fines de seguimiento; el editor controla la entrega. | Ofertas garantizadas: Sí<br>Ofertas no garantizadas: No | Sí |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Crear manualmente los detalles del ID de acuerdo](deal-id-create.md)
>* [Socios del SSP](ssp-partners.md)
>* [Acerca del inventario privado](private-inventory-about.md)
