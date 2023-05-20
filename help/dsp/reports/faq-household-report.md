---
title: Preguntas frecuentes sobre [!UICONTROL Household] Informe
description: Obtenga más información acerca de [!UICONTROL Household] , incluido en qué se diferencia de otros informes y solución de problemas.
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Preguntas frecuentes sobre [!UICONTROL Household] Informe

## ¿Cómo [!UICONTROL Household] ¿son diferentes los informes de alcance y frecuencia de otros informes personalizados?

El [!UICONTROL Household] informar sobre el alcance, la impresión y la frecuencia en varias dimensiones a nivel de hogar en función de la dirección IP. Los demás informes personalizados se generan en el nivel de dispositivo o cookie.

Por ejemplo, incluso si se sirve una impresión a tres dispositivos dentro de un hogar, la métrica Alcanzado en el hogar único es una.

### Dimension admitidos

El [!UICONTROL Household] El informe admite [siguientes dimensiones](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (que no proporciona acceso a métricas superpuestas), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length],&quot; y la ubicación creada por el usuario &quot;[!UICONTROL Tags].&quot; |

### Métricas compatibles

El [métricas disponibles](/help/dsp/reports/report-columns.md) incluir:

* Métricas de superposición: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], y [!UICONTROL Unique Household (Overlap)].

   Las métricas de superposición son valores que se producen únicamente para la dimensión o combinación de dimensiones del informe y no para otras dimensiones. <!-- For example, it might show the ?? -->

* Métricas no superpuestas: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], y [!UICONTROL Unique Household Reached]

Las métricas de conversión y los objetivos personalizados no son compatibles.

## ¿Cuál es la diferencia entre las métricas de superposición y las que no son de superposición?

La siguiente figura muestra tres métricas (Hogar único alcanzado, Hogar incremental alcanzado y Hogar incremental (superpuesto)) para tres campañas (A, B y C).

![Ilustración de métricas de superposición de hogares](/help/dsp/assets/household-overlap-metrics-illustration.png "Ilustración de métricas de superposición de hogares")

* Unique Household Reached (Total) proporciona el Unique Household alcanzado por cada una de las campañas o el área total de cada uno de los círculos. En la figura, Hogar único alcanzado por A = Hogar incremental alcanzado por A + (A+B) + (A+C) + (A+B+C)

* El hogar incremental alcanzado es el hogar único al que solo se ha llegado mediante una campaña. En la figura, el hogar incremental alcanzado por A, B, C es el hogar incremental alcanzado por A, B, C respectivamente.

* Hogar incremental (superposición) es el hogar único al que se llega mediante la campaña o la combinación de campañas. En la figura, el hogar incremental alcanzado por A, C es A + C.

## Flujo de trabajo

Siga los pasos normales para [creación de un informe personalizado](report-create.md).

El [!UICONTROL Household] El informe solo puede incluir una dimensión. También puede incluir a) métricas de superposición de cualquier dimensión, excepto Sitio/Aplicaciones o b) métricas no superpuestas, pero no ambas.

## ¿Cuáles son algunas limitaciones de la [!UICONTROL Household] ¿reportar? 

Los informes con métricas de superposición generan intersecciones de hasta tres valores. Por ejemplo, si utiliza la métrica [!UICONTROL Unique Household (Overlap)] en el caso de 10 ubicaciones, se pueden ver los hogares únicos a los que han llegado las ubicaciones individuales, los hogares comunes a los que ha llegado una combinación de dos ubicaciones cualesquiera y los hogares comunes a los que se ha llegado mediante combinaciones de tres ubicaciones cualesquiera. No se pueden ver hogares comunes a los que se haya llegado en cuatro o más ubicaciones.

Para dimensiones que no sean campaña, paquete o ubicación, el informe admite hasta 10 valores en cada dimensión. Por ejemplo, para generar un [!UICONTROL Unique Household Reached] informe para [!UICONTROL Audience] de dimensión, el número de audiencias únicas debe ser inferior o igual a 10. Si incluye más de 10 audiencias únicas, se genera un informe en blanco.

## ¿Por qué los valores de frecuencia y alcance únicos son diferentes entre mis [!UICONTROL Custom] informes y el [!UICONTROL Household] ¿reportar?

Estas métricas en [!UICONTROL Household] Los informes de se calculan usando el recuento real de direcciones IP, mientras que las métricas de la variable [!UICONTROL Custom] los informes utilizan números estimados calculados mediante modelos. Sin embargo, la discrepancia debe ser inferior al 10 %.

## ¿Cómo configuro el informe para? [!UICONTROL Placement Tags] dimensión?

Para crear etiquetas para la ubicación, haga lo siguiente: [abrir la configuración de ubicación](/help/dsp/campaign-management/placements/placement-edit.md) e introduzca valores en [Campo Etiquetas de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).
 
Cuando una ubicación incluye varias etiquetas, el informe considera toda la cadena como una etiqueta. El informe incluye una fila por cada cadena única.

## [!UICONTROL Household] Informe frente a datos de [!DNL Advanced Measurement Services]

Para la elaboración avanzada de informes sobre el alcance y la frecuencia basados en el hogar, la variable [[!DNL Strategic Advertising Consulting] equipo](/help/dsp/introduction/advanced-measurement-services.md) puede proporcionar informes altamente personalizables junto con recomendaciones estratégicas integrales. Para obtener más información acerca de [!DNL Advanced Measurement Services], póngase en contacto con el equipo de cuenta de Adobe.

### Si ya estoy utilizando [!DNL Advanced Measurement Services], ¿por qué debería usar el [!UICONTROL Household] ¿reportar?

El [!UICONTROL Household] Este informe permite a los clientes extraer de forma autónoma en tiempo real las métricas de alcance y frecuencia a nivel del hogar.

### ¿Puedo usar los dos [!UICONTROL Household] informe y [!DNL Advanced Measurement Services]? 

El caso de uso ideal es utilizar tanto la variable [!UICONTROL Household] y el [!DNL Advanced Measurement Services] los servicios de consultoría y elaboración de informes. Considere la [!UICONTROL Household] informar como transaccional, pensado para informar las optimizaciones diarias, y [!DNL Advanced Measurement Services] como algo más estratégico, pensado para informar aprendizajes y aprendizajes integrales vinculados a objetivos empresariales globales.

>[!MORELIKETHIS]
>
>* [Acerca de los informes personalizados](/help/dsp/reports/report-about.md)
>* [Creación de un informe personalizado](/help/dsp/reports/report-create.md)
>* [Edición de un informe personalizado](/help/dsp/reports/report-edit.md)
>* [Configuración de informe personalizada](/help/dsp/reports/report-settings.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)

