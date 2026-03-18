---
title: Casos de uso
description: Descubra casos de uso para compartir sus datos de medios de Advertising DSP con Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Casos de uso para capturar datos de exposición de medios en Adobe Audience Manager

*Anunciantes solo con Advertising DSP*

*Solo anunciantes con una integración Adobe Advertising-Adobe Audience Manager*

A continuación se indican algunas formas en que puede beneficiarse de capturar los datos de exposición a medios de Advertising DSP <!-- ad impression data? --> en Audience Manager.

## Administración de actualización y frecuencia

La captura de datos de impresiones en Audience Manager permite mejorar la administración de frecuencias mediante la creación de segmentos de usuarios que han estado expuestos a un anuncio o una campaña en particular. Puede utilizar estos segmentos para la segmentación de anuncios si desea aumentar la frecuencia o para la supresión de anuncios si desea limitar la frecuencia.

Además, con Audience Manager [!DNL Segment Builder], puede aplicar [controles de actualización y frecuencia](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html?lang=es) a cualquier [característica basada en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=es) que contenga señales procesables. Esto le permite, por ejemplo, limitar el número de veces que se muestra a un usuario un creativo particular dentro de una campaña de medios. Lea &quot;[Eliminación instantánea entre dispositivos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html?lang=es)&quot; para saber cómo hacerlo.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Mensajes secuenciales

Al capturar los datos de impresión, puede crear un segmento de usuarios que han estado expuestos a una campaña o publicidad y utilizar este segmento para la mensajería secuencial o la supresión. Por ejemplo, puede redirigirse a los usuarios que vieron el elemento creativo `123` pero que no hicieron clic ni convirtieron mostrándoles el elemento creativo `456`.

Para ejecutar este ejemplo en Audience Manager, debe seguir estos pasos:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Cree un rasgo para capturar a los usuarios que vieron al creativo.

   Por ejemplo, para asignar un nombre al rasgo `Creative Trait 123`, use la siguiente regla de rasgos:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Cree una característica para capturar a los usuarios que hacen clic o convierten.

   Por ejemplo, para nombrar este rasgo `Click and Converter`, use la siguiente regla de rasgos:

   ```
   d_event == click OR d_event=conv
   ```

1. Cree un segmento llamado `Retarget Users` para rellenar con usuarios que vieron el elemento creativo `123` pero que no hicieron clic ni convirtieron. Utilice la siguiente regla de rasgos:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Asigne el segmento `Retarget Users` a un destino y dirija a los usuarios en el destino con el creativo `456`.

## [!DNL Adobe Audience Analytics] y datos de exposición de la campaña

Una vez que los datos de clics y impresiones de campaña están disponibles en Audience Manager, puede crear rasgos y segmentos de usuarios que estuvieron expuestos o interactuaron con una campaña o táctica en particular. Con una [[!DNL Audience Analytics] integración](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=es), sus segmentos de Audience Manager se pueden sincronizar con [!DNL Analytics] para un análisis más detallado. Los casos de uso potenciales incluyen los siguientes:

* **Análisis de interacción entre DSP y [!DNL Advertising Search, Social, & Commerce] anuncios:** La [[!DNL Analytics for Advertising] integración](/help/integrations/analytics/overview.md) estándar no proporciona información sobre la interacción entre DSP y [!DNL Search, Social, & Commerce] porque ambos canales utilizan ID de AMO que siguen las reglas de atribución de ID de AMO, para las cuales un clic en la búsqueda anula una visualización de visualización. Si crea un segmento de exposición de DSP en Audience Manager, puede usar [!DNL Audience Analytics] para analizar la interacción entre DSP y los anuncios de [!DNL Search, Social, & Commerce] en [!DNL Analytics].

* **Análisis de frecuencia:** Puede crear segmentos en Audience Manager basados en la cantidad de veces que un usuario estuvo expuesto a una publicidad o campaña en particular. A continuación, puede analizar los distintos segmentos de exposición en Analytics para ver cómo cambia el comportamiento del usuario según el número de exposiciones de DSP.

## [!DNL Audience Optimization Reports]

Puede aprovechar [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html?lang=es) para identificar posibles oportunidades de rendimiento para segmentos en sus campañas. Estos informes combinan datos de impresiones, clics y conversiones de campañas con métricas de segmentos para ofrecer optimizaciones centradas en segmentos y una combinación de canales eficaz.

### Tipos de informes relevantes de Audience Optimization

| Informe | Descripción |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html?lang=es) | Compara los segmentos asignados y no asignados según las impresiones y las tasas de conversión. |
| [[!UICONTROL Trend Analysis and Volume Analysis] informes]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Devuelve datos sobre impresiones, tasas de pulsaciones y conversiones para una amplia gama de dimensiones publicitarias. |
| [[!UICONTROL Optimal Frequency] informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html?lang=es) | Ayuda a descubrir el equilibrio óptimo entre la cantidad de impresiones servidas y las conversiones. Permite ajustar el número de impresiones que se van a mostrar antes de empezar a ver rendimientos decrecientes. |
| [[!UICONTROL Unique User Reach] informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html?lang=es) | Un gráfico de burbujas, en el que cada burbuja se dimensiona directamente en proporción al número de usuarios únicos para la dimensión seleccionada. |

### Consideraciones

* Si los usuarios de [!DNL Audience Optimization Reports] tienen controles de acceso basados en roles (RBAC), [!DNL Adobe Customer Care] debe configurar una asignación entre el ID del anunciante y el código de integración de la fuente de datos de Audience Manager de la organización. Los usuarios administradores pueden proporcionar derechos RBAC a distintos usuarios.

* Los informes de conversión de [!DNL Audience Optimization Reports] requieren cierta configuración por parte del usuario final. Los usuarios deben rellenar los archivos de metadatos.

* [!DNL Audience Optimization Reports] no admite cambios en los metadatos de la campaña (como el nombre de la campaña o el nombre de la ubicación).

* Los clics en anuncios de búsqueda se incluyen en [!DNL Audience Optimization Reports] solo cuando se correlacionan con impresiones. En otras palabras, los clics en la búsqueda se tratan como conversiones después de impresiones. Como resultado, es posible que muchos clics en la búsqueda no se incluyan en [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Información general sobre el envío de datos de exposición de medios de DSP a Adobe Audience Manager](overview.md)
>* [Recopilar datos de clics e impresiones de campañas de Advertising DSP](collect.md)
