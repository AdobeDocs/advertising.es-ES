---
title: Solución de problemas de rendimiento
description: Consulte los problemas de rendimiento comunes y cómo solucionarlos.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Solución de problemas de rendimiento

| Problema | Causa posible | Acciones que se deben realizar |
| --- | --- | --- |
| Sin gasto en ubicación | La ubicación no incluye anuncios o los anuncios no están activos. | Compruebe que todos los anuncios esperados estén adjuntos a la ubicación y que estén aprobados y activos.<br><br>Además, comprueba si la ubicación incluye un horario de anuncios personalizado, lo que puede limitar el período de vuelo de cada anuncio. Para ver la programación de anuncios de una ubicación desde la vista Ubicaciones, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** junto al nombre de la ubicación. |
| | Las fechas afectadas no están dentro de las fechas de vuelo configuradas. | Compruebe que las fechas de vuelo son válidas en los niveles de campaña, paquete y ubicación. |
| | El objetivo del presupuesto se ha cumplido o no es lo suficientemente alto. | Compruebe la configuración del presupuesto en los niveles de campaña, paquete y ubicación. |
| | La cuenta no tiene fondos suficientes. | Para ver si su cuenta cuenta cuenta cuenta con fondos suficientes, vaya a **[!UICONTROL Settings]** > **[!UICONTROL Account]** y observe la cantidad de [!UICONTROL Usable Funds]. Si necesita añadir más fondos, póngase en contacto con el equipo de cuenta de Adobe. |
| | No hay ningún inventario disponible. | Compruebe si los orígenes de inventario especificados ([!UICONTROL Public], [!UICONTROL Private] o [!UICONTROL On Demand]) son:<ul><li>Configure correctamente.</li><li>Activo y enviando mediante subastas.</li><li>Compatible con el tipo de anuncio y ubicación aplicable.</li></ul><br>Si todos los orígenes de inventario son válidos y están activos, asigne a orígenes de inventario adicionales o todos cuando sea posible. |
| | No hay usuarios disponibles. | Compruebe que los objetivos de audiencia especificados incluyan suficientes usuarios activos. Si no es así, expanda los destinatarios agregando más audiencias. |
| Gasto bajo en ubicación | La sección [!UICONTROL Non Bids] del informe de diagnóstico de ubicación muestra los posibles motivos por los que la ubicación no se ofreció. | [Revise el informe [!UICONTROL Non Bids]](/help/dsp/campaign-management/reports/placement-diagnostics.md) para comprender por qué no se realizó la oferta.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | La ubicación usa [filtros de ofertas previas](/help/dsp/campaign-management/placements/placement-settings.md) que limitan las ofertas. | Reduzca los umbrales de los filtros de oferta previa en un 5 % para evaluar el equilibrio entre gasto y rendimiento. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Tenga en cuenta que el uso de varios destinos de ubicación, como filtros de ofertas previas, geos, inventario y audiencias, puede limitar las ofertas y los gastos de manera acumulativa. |
| | La ubicación tiene una tasa de ganancia baja. | Aumente [!UICONTROL Max Bid] para mejorar la tasa de ganancia.<br><br><b>NOTA:</b> Los precios de inventario pueden variar según el destino de la ubicación.<br><br>Una tasa de ganancia del 10% se considera saludable. |
| | Hay un número bajo de inventario disponible. | Segmente fuentes de inventario adicionales o todas si es posible.<br><br>Tenga en cuenta que el uso de varios destinos de ubicación, como filtros de ofertas previas, geos, inventario y audiencias, puede limitar las ofertas y los gastos de manera acumulativa. |
| | Hay un número bajo de usuarios disponibles. | Compruebe que los objetivos de audiencia especificados incluyan suficientes usuarios activos. Si no es así, expanda los destinatarios agregando más audiencias.<br><br>Tenga en cuenta que el uso de varios destinos de ubicación, como filtros de ofertas previas, geos, inventario y audiencias, puede limitar las ofertas y los gastos de manera acumulativa. |
| | El paquete incluye un gran número de ubicaciones activas. | Reduzca el número de ubicaciones activas dentro del paquete o aumente el presupuesto general del paquete.DSP <br><br>Si el paquete tiene muchas ubicaciones, pero no el presupuesto suficiente, es posible que no pueda asignar suficiente presupuesto a cada ubicación. Cada ubicación debe tener una oportunidad de gastar al menos 2 USD/día. Por ejemplo, si el paquete tiene un presupuesto de 10 USD/día, lo mejor es incluir cinco ubicaciones o menos. palo de golf |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md)
