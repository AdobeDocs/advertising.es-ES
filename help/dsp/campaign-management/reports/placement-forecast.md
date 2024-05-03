---
title: Ver el informe Previsión de ubicación
description: Ver el número de impresiones, el gasto y la oferta máxima óptima prevista para una estrategia de segmentación determinada para una ubicación.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: 2ecf1eacb2a47c20e0c05f9ff62386869b644ba6
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Ver el informe Previsión de ubicación

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

La herramienta de previsión de ubicación muestra el número previsto de impresiones, el gasto y la oferta máxima óptima para una estrategia de segmentación determinada. La previsión se calcula en función del inventario general disponible con la ubicación y los usuarios únicos disponibles.

>[!NOTE]
>
>* Los códigos postales no se tienen en cuenta en los cálculos de previsión de ubicación.
>* No se genera ninguna previsión para las ubicaciones con una segmentación programática garantizada (PG) únicamente porque la disponibilidad y el gasto son deterministas.

## Información en la previsión

La previsión incluye la siguiente información:

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** El coste estimado por cada mil impresiones (eCPM) que la configuración de direccionamiento puede esperar alcanzar.

   * **[!UICONTROL Budget]:** Presupuesto estimado para la configuración de segmentación.

   * **[!UICONTROL Impression]:** El número estimado de impresiones para la configuración de segmentación.

* **[!UICONTROL Budget Yield Curve]:** El número estimado de impresiones que la ubicación puede entregar en diferentes niveles de presupuesto si todas las demás configuraciones de segmentación son iguales.

* **[!UICONTROL Max Bid Yield Curve]:** El gasto estimado para la colocación en diferentes niveles de puja máxima, cuando todas las demás configuraciones de segmentación son iguales.

* **[!UICONTROL Message]:** Proporciona información sobre el resultado previsto, incluidos los escenarios en los que no se pudo generar la previsión. También resalta cualquier configuración de segmentación revisada pero no considerada en ese escenario debido a la falta de datos.

### Cálculo del presupuesto

* En el caso de las ubicaciones que no están asignadas a un paquete, el presupuesto de ubicación se utiliza para los cálculos. Dentro de un vuelo, se calcula el mismo presupuesto general.

* Para las ubicaciones dentro de un paquete, el presupuesto asignado a la ubicación se utiliza para los cálculos. Durante el vuelo, el presupuesto asignado a la ubicación se calcula y se incluye en el mensaje.

* Para las ubicaciones agregadas a un paquete en vuelo, el presupuesto se divide equitativamente en función del número de ubicaciones. Cuando la ubicación se activa, se calcula el presupuesto asignado por el paquete.

## Requisitos

* Gasto mínimo: $25 diarios o equivalente en moneda local por ubicación.

* Gasto máximo: $15,000 diarios o el equivalente en moneda local por ubicación.

* Oferta máxima mínima, Oferta máxima máxima: Hay una oferta máxima mínima (para la curva de rendimiento del presupuesto) y una oferta máxima (para la curva de rendimiento de oferta máxima) por tipo de ubicación. Estos valores son verdaderos a nivel global y no tienen en cuenta las variaciones regionales. A veces, estos valores pueden ser demasiado altos o bajos para la región de destino.

* Datos históricos: la previsión de ubicación está disponible cuando hay suficientes datos históricos disponibles. Los siguientes son ejemplos de cuándo pueden estar disponibles datos históricos insuficientes:

   * La ubicación se dirige a una nueva región para la campaña.

   * La ubicación se dirige a un nuevo acuerdo de inventario para la campaña.

   * La ubicación utiliza un nuevo tipo de anuncio para la campaña.

     Una ubicación suele ser una colección de varias plantillas de publicidad, tal como se definen en las plataformas del lado del suministro. Por lo tanto, aunque la ubicación haya existido durante mucho tiempo, la plantilla de anuncio subyacente puede ser nueva y la herramienta de previsión no podrá realizar previsiones.

## Abrir el informe Previsión de ubicación

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña y luego haga clic en **[!UICONTROL Placements]**.

1. Junto al nombre de la ubicación, haga clic en  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Busque el **[!UICONTROL Forecast]** en la parte superior derecha. Si es necesario, haga clic en ![Pronóstico](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* A veces, la previsión puede no estar disponible debido a la caché del explorador. Si esto sucede, borre la caché e inténtelo de nuevo.

>[!MORELIKETHIS]
>
>* [Tipos de informes de rendimiento en las vistas de Campaign Management](campaign-reports-about.md)
>* [Ver los informes de diagnóstico de ubicación](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
