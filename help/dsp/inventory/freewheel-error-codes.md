---
title: Códigos de error para  [!DNL FreeWheel] envíos de publicidad
description: Hacer referencia a los códigos de error devueltos para los envíos de anuncios a  [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 3%

---

# Códigos de error para [!DNL FreeWheel] envíos de publicidad

Los mensajes de error para los envíos de anuncios erróneos pueden proceder de Advertising DSP o de [!DNL FreeWheel]. Los mensajes de error se muestran en la columna [!UICONTROL API Response] del cuadro de diálogo [[!UICONTROL Freewheel Status]](freewheel-check-status.md).

## Errores internos de Advertising DSP

| Mensaje de error | Descripción | Pasos siguientes |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] aún no ha respondido que el envío se realizó correctamente o no. | Vuelva a comprobar el estado en 10 minutos. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] no acepta anuncios del Reino Unido sin números de reloj asignados. | Asigne un número de reloj al anuncio y vuelva a enviarlo. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | El transcodificador no había terminado de transcodificar el anuncio cuando intentó enviarlo. | Espere diez minutos y vuelva a enviar el anuncio. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | El acuerdo enviado no se establece como un acuerdo programático garantizado. [!DNL FreeWheel] solo acepta ofertas garantizadas. | Configure el ID de la oferta como una oferta programática garantizada. El anuncio se envía automáticamente a [!DNL FreeWheel] cuando se guarda la ubicación predeterminada programática garantizada al final del flujo de trabajo del ID de la oferta. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id\> | El ID de oferta enviado no existe o no está activo en el extremo del Adobe. | Asegúrese de que la oferta esté activa y vuelva a enviar el anuncio. |
| [!DNL \[public_id=]\&lt;deal\>] no existe | El id. de acuerdo enviado no existe en el extremo [!DNL FreeWheel]. | Póngase en contacto con su representante de [!DNL FreeWheel] para confirmar el ID de la oferta. |
| [!DNL Ad with identifier] \&lt;*nombre del anuncio*\> [!DNL was not found.] | La clave de anuncio enviada no existe o no está activa en el extremo del Adobe. | Busque la clave de anuncio correcta y, a continuación, vuelva a enviar el anuncio. |
| [!DNL Pending Submission] | El envío aún está pendiente. | Actualice la página. |

{style="table-layout:auto"}

## [!DNL Freewheel] errores de API

| Código | Significado | Descripción | Pasos siguientes |
|--- |--- |--- |--- |
| 401 | No autorizado | Credenciales de acceso incorrectas, inexistentes o no válidas. | Póngase en contacto con el equipo de cuenta de Adobe. |
| 403 | Prohibido | El servidor entiende la solicitud, pero se niega a autorizarla. | Póngase en contacto con el equipo de cuenta de Adobe. |
| 404 | No encontrado | El recurso solicitado no está disponible. Si no se encuentra el ID del creativo en la operación del PUT, se devuelve un error 404. | Póngase en contacto con el equipo de cuenta de Adobe. |
| 405 | Método no permitido | Se realizó una solicitud de un recurso mediante un método de solicitud no admitido por ese recurso (por ejemplo, mediante el uso de GET en un método que requiere que el POST envíe los datos, o mediante el uso de PUT en un recurso de solo lectura). | Póngase en contacto con el equipo de cuenta de Adobe. |
| 408 | Tiempo de espera de solicitud | Se agotó el tiempo de espera mientras se procesaba esta solicitud. Los tiempos de espera suelen deberse a solicitudes simultáneas de acceso exclusivo a determinados recursos. | Vuelva a enviar la solicitud cuando reciba este estado. Si el problema persiste, póngase en contacto con el equipo de cuenta de Adobe. |
| 422 | Entidad no procesable | Medio no válido. Este error se produce cuando el cuerpo de la solicitud no es válido o el recurso creado/actualizado no es válido (por ejemplo, si no se encontró el ID de acuerdo). Consulte [Errores de API 422 de FreeWheel](#freewheel-422-errors) para obtener más información. | Póngase en contacto con el equipo de cuenta de Adobe. |
| 500 | Error interno del servidor | Error del sistema de API. | Póngase en contacto con el equipo de cuenta de Adobe. |

{style="table-layout:auto"}

## [!DNL Freewheel] errores de API 422 {#freewheel-422-errors}

| Código | Código HTTP | Descripción |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | Los datos solicitados no tienen un formato json válido. Consulte el mensaje de error para obtener más detalles. |
| DATA_VALIDATION_FAILURE | 422 | A los datos de la solicitud les faltan campos obligatorios o tienen un tipo de datos no válido. Consulte el mensaje de error para obtener más detalles. |
| DATA_DEAL_INVALID | 422 | La oferta se ha configurado incorrectamente o no existe. Consulte el mensaje de error para obtener más detalles. |
| DATA_DEAL_GET_FAILURE | 422 | No se ha encontrado la oferta o su configuración tiene un problema. Consulte el mensaje de error para obtener más detalles. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | La URL de creatividad no es válida. Consulte el mensaje de error para obtener más detalles. |
| DATA_CREATIVE_LINK_FAILURE | 422 | El creativo no estaba vinculado a los nodos de la unidad publicitaria del acuerdo. Consulte el mensaje de error para obtener más detalles. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | El elemento creativo no se ha actualizado. Consulte el mensaje de error para obtener más detalles. |
| DSP DATA__GET_FAILURE | 422 | DSP El elemento no existe dentro del sistema. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | El creativo no se ha desvinculado de las unidades de publicidad. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | No se ha eliminado el elemento creativo. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | No se ha detectado la dirección URL. |
| DATA_ENTITY_NOT_FOUND | 422 | El creativo no existe. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Información general sobre la configuración de ofertas garantizadas mediante programación en [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Enviar un anuncio para obtener una oferta programática garantizada a [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Comprobar el estado de los anuncios para [!DNL FreeWheel] Ofertas programáticas garantizadas](/help/dsp/inventory/freewheel-check-status.md)
