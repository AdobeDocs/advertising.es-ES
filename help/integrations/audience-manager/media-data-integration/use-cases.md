---
title: Casos de uso
description: DSP Descubra casos de uso para compartir los datos de medios de Advertising con Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Casos de uso para capturar datos de exposición de medios en Adobe Audience Manager

*DSP Solo anunciantes con Advertising*

*Anunciantes con una integración de Adobe de Advertising-Adobe Audience Manager solamente*

DSP A continuación se indican algunas formas en que puede beneficiarse de capturar los datos de exposición a los medios de Advertising <!-- ad impression data? --> en Audience Manager.

## Administración de actualización y frecuencia

La captura de datos de impresiones en Audience Manager permite mejorar la gestión de frecuencias mediante la creación de segmentos de usuarios que han estado expuestos a una publicidad o campaña determinada. Puede utilizar estos segmentos para la segmentación de anuncios si desea aumentar la frecuencia o para la supresión de anuncios si desea limitar la frecuencia.

Además, con el Audience Manager [!DNL Segment Builder], puede aplicar [controles de actualización y frecuencia](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) a cualquier [rasgos basados en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) que contienen señales procesables. Esto le permite, por ejemplo, limitar el número de veces que se muestra a un usuario un creativo particular dentro de una campaña de medios. Leer &quot;[Eliminación instantánea entre dispositivos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; para aprender a hacer esto.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Mensajería secuencial

Al capturar los datos de impresión, puede crear un segmento de usuarios que han estado expuestos a una campaña o publicidad y utilizar este segmento para la mensajería secuencial o la supresión. Por ejemplo, puede redirigir a los usuarios que vieron el mensaje creativo `123` pero no hizo clic ni convirtió al mostrarles contenido creativo `456`.

Para ejecutar este ejemplo en Audience Manager, debe seguir estos pasos:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Cree un rasgo para capturar a los usuarios que vieron al creativo.

   Por ejemplo, para asignar un nombre al rasgo `Creative Trait 123`, utilice la siguiente regla de rasgos:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Cree una característica para capturar a los usuarios que hacen clic o convierten.

   Por ejemplo, para nombrar este rasgo `Click and Converter`, utilice la siguiente regla de rasgos:

   ```
   d_event == click OR d_event=conv
   ```

1. Cree un segmento llamado `Retarget Users` para rellenar con usuarios que vieron creative `123` pero no hizo clic ni convirtió. Utilice la siguiente regla de rasgos:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Asignación del segmento `Retarget Users` a un destino y dirija a los usuarios en el destino con creative `456`.

## [!DNL Adobe Audience Analytics] y datos de exposición de la campaña

Una vez que los datos de impresión y clics de la campaña estén disponibles en Audience Manager, puede crear rasgos y segmentos de usuarios que estuvieron expuestos o interactuaron con una campaña o táctica en particular. Con un [[!DNL Audience Analytics] integración](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), los segmentos del Audience Manager se pueden sincronizar con [!DNL Analytics] para un análisis más detallado. Los casos de uso potenciales incluyen los siguientes:

* **DSP Análisis de interacción entre la interacción entre la y [!DNL Advertising Search, Social, & Commerce] anuncios:** El estándar [[!DNL Analytics for Advertising] integración](/help/integrations/analytics/overview.md) DSP no proporciona perspectivas sobre la interacción entre la y [!DNL Search, Social, & Commerce] porque ambos canales utilizan ID de AMO que siguen las reglas de atribución de ID de AMO, para los que un clic en la búsqueda anula una visualización completa. DSP Si crea un segmento de exposición de la en Audience Manager, puede utilizar lo siguiente [!DNL Audience Analytics] DSP para analizar la interacción entre los grupos de trabajo de la y [!DNL Search, Social, & Commerce] anuncios en [!DNL Analytics].

* **Análisis de frecuencia:** Puede crear segmentos en Audience Manager basados en la cantidad de veces que un usuario estuvo expuesto a una publicidad o campaña en particular. DSP A continuación, puede analizar los distintos segmentos de exposición en Analytics para ver cómo cambia el comportamiento del usuario según el número de exposiciones de la.

## [!DNL Audience Optimization Reports]

Puede aprovechar [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) para identificar posibles oportunidades de rendimiento para segmentos en todas las campañas. Estos informes combinan datos de impresiones, clics y conversiones de campañas con métricas de segmentos para ofrecer optimizaciones centradas en segmentos y una combinación de canales eficaz.

### Tipos de informes de Audience Optimization relevantes

| Informe | Descripción |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Compara los segmentos asignados y no asignados según las impresiones y las tasas de conversión. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Informes]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Devuelve datos sobre impresiones, tasas de pulsaciones y conversiones para una amplia gama de dimensiones publicitarias. |
| [[!UICONTROL Optimal Frequency] Informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Ayuda a descubrir el equilibrio óptimo entre la cantidad de impresiones servidas y las conversiones. Permite ajustar el número de impresiones que se van a mostrar antes de empezar a ver rendimientos decrecientes. |
| [[!UICONTROL Unique User Reach] Informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Un gráfico de burbujas, en el que cada burbuja se dimensiona directamente en proporción al número de usuarios únicos para la dimensión seleccionada. |

### Consideraciones

* If [!DNL Audience Optimization Reports] Los usuarios de tienen controles de acceso basados en roles (RBAC). [!DNL Adobe Customer Care] debe configurar una asignación entre el ID del anunciante y el código de integración de la fuente de datos del Audience Manager de la organización. Los usuarios administradores pueden proporcionar derechos RBAC a distintos usuarios.

* Creación de informes de conversión en [!DNL Audience Optimization Reports] requiere cierta configuración por parte del usuario final. Los usuarios deben rellenar los archivos de metadatos.

* [!DNL Audience Optimization Reports] no admite cambios en los metadatos de la campaña (como el nombre de la campaña o el nombre de la ubicación).

* Los clics en anuncios de búsqueda se incluyen en [!DNL Audience Optimization Reports] solo cuando están correlacionados con impresiones. En otras palabras, los clics en la búsqueda se tratan como conversiones después de impresiones. Como resultado, es posible que muchos clics de búsqueda no se incluyan en [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [DSP Información general sobre el envío de datos de exposición de medios de comunicación de a Adobe Audience Manager](overview.md)
>* [DSP Recopilación de datos de clics e impresiones de campañas de Advertising](collect.md)

