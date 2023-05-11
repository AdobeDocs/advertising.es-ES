---
title: Preguntas frecuentes sobre [!UICONTROL Household] Informe
description: Obtenga más información sobre [!UICONTROL Household] informe, incluida su diferencia con respecto a otros informes y solución de problemas.
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Preguntas frecuentes sobre [!UICONTROL Household] Informe

## ¿Cómo [!UICONTROL Household] informes de alcance y frecuencia diferentes de otros informes personalizados?

La variable [!UICONTROL Household] informe mide el alcance, la impresión y la frecuencia en diversas dimensiones a nivel de hogar en función de la dirección IP. Los demás informes personalizados se generan a nivel de dispositivo o cookie.

Por ejemplo, aunque se dé una impresión a tres dispositivos dentro de un hogar, la métrica Hogar único alcanzado es una.

### Dimension admitidos

La variable [!UICONTROL Household] es compatible con [dimensiones siguientes](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot;[!UICONTROL Package],&quot;[!UICONTROL Placement],&quot;[!UICONTROL Site/Apps]&quot; (que no proporciona acceso a métricas de superposición), &quot;[!UICONTROL Media Type],&quot;[!UICONTROL Feed Type],&quot;[!UICONTROL Device],&quot;[!UICONTROL Publisher],&quot;[!UICONTROL Audience],&quot;[!UICONTROL Creative Length],&quot; y la ubicación creada por el usuario &quot;[!UICONTROL Tags].&quot; |

### Métricas compatibles

La variable [métricas disponibles](/help/dsp/reports/report-columns.md) incluir:

* Métricas de superposición: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)]y [!UICONTROL Unique Household (Overlap)].

   Las métricas de superposición son los valores que se producen únicamente para la dimensión o combinación de dimensiones del informe y no para otras dimensiones. <!-- For example, it might show the ?? -->

* Métricas no superpuestas: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions]y [!UICONTROL Unique Household Reached]

No se admiten las métricas de conversión y los objetivos personalizados.

## ¿Cuál es la diferencia entre las métricas de superposición y no superposición?

En la siguiente figura se muestran tres métricas (Se llegó a un hogar único, Se llegó a un hogar incremental y Hogar incremental (Superposición)) para tres campañas (A, B y C).

![Ilustración de las métricas de superposición de hogares](/help/dsp/assets/household-overlap-metrics-illustration.png "Ilustración de las métricas de superposición de hogares")

* El Hogar único alcanzado (total) proporciona el Hogar único alcanzado por cada una de las campañas o el área total de cada uno de los círculos. En la figura, Hogar único alcanzado por A = Hogar incremental alcanzado por A + (A+B) + (A+C) +(A+B+C)

* El Hogar Incremental Alcanzado es el Hogar Único al que solo se ha llegado mediante una campaña. En la cifra, el hogar incremental al que llegan A nivel A, B y C es el hogar incremental al que llegan A nivel A, B y C, respectivamente.

* El Hogar incremental (superposición) es el Hogar único alcanzado por la campaña o combinación de campañas. En la figura, el Hogar Incremental Alcanzado por A, C es A+C.

## Flujo de trabajo

Siga los pasos normales para [crear un informe personalizado](report-create.md).

La variable [!UICONTROL Household] El informe solo puede incluir una dimensión. También puede incluir a) métricas de superposición por cualquier dimensión excepto Sitio/Aplicaciones o b) métricas no superpuestas, pero no ambas.

## ¿Cuáles son algunas limitaciones de la variable [!UICONTROL Household] informe? 

Los informes con métricas de superposición emiten intersecciones de hasta tres valores. Por ejemplo, si utiliza la métrica [!UICONTROL Unique Household (Overlap)] en el caso de 10 colocaciones, se pueden ver las familias únicas a las que llegan las colocaciones individuales, las familias comunes a las que se llega mediante una combinación de dos colocaciones cualesquiera y las familias comunes a las que se llega mediante combinaciones de tres colocaciones cualesquiera. No se puede ver que cuatro o más ubicaciones alcanzan hogares comunes.

Para dimensiones que no sean campañas, paquetes o ubicaciones, el informe admite hasta 10 valores en cada dimensión. Por ejemplo, para generar un [!UICONTROL Unique Household Reached] para [!UICONTROL Audience] , el número de audiencias únicas debe ser menor o igual que 10. Si incluye más de 10 audiencias únicas, se genera un informe en blanco.

## ¿Por qué los valores de frecuencia y alcance único son diferentes entre mis [!UICONTROL Custom] y [!UICONTROL Household] informe?

Estas métricas de [!UICONTROL Household] los informes se calculan con el recuento real de direcciones IP, mientras que las métricas de la variable [!UICONTROL Custom] informe de uso de números estimados calculados usando modelos. Sin embargo, la discrepancia debe ser inferior al 10 %.

## ¿Cómo configuro el informe para la variable [!UICONTROL Placement Tags] dimensión?

Para crear etiquetas para la colocación, [abra la configuración de ubicación](/help/dsp/campaign-management/placements/placement-edit.md) e introduzca valores en la variable [Campo Etiquetas de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).
 
Cuando una colocación incluye varias etiquetas, el informe considera que toda la cadena es una etiqueta. El informe incluye una fila por cada cadena única.

## [!UICONTROL Household] Informe vs. Datos de [!DNL Advanced Measurement Services]

Para informes avanzados sobre alcance y frecuencia basados en el hogar, la variable [[!DNL Strategic Advertising Consulting] equipo](/help/dsp/introduction/advanced-measurement-services.md) puede proporcionar informes altamente personalizables junto con recomendaciones estratégicas holísticas. Para obtener más información, consulte [!DNL Advanced Measurement Services], póngase en contacto con su equipo de cuentas de Adobe.

### Si ya estoy utilizando [!DNL Advanced Measurement Services], ¿por qué debería usar la variable [!UICONTROL Household] informe?

La variable [!UICONTROL Household] permite a los clientes extraer métricas de alcance y frecuencia a nivel de hogar de forma autónoma en tiempo real.

### ¿Puedo usar ambas [!UICONTROL Household] informe y [!DNL Advanced Measurement Services]? 

El caso de uso ideal es usar ambas variables [!UICONTROL Household] y [!DNL Advanced Measurement Services] servicios de informes y consultoría juntos. Tenga en cuenta las [!UICONTROL Household] informar como transaccional, con el fin de informar las optimizaciones diarias, y [!DNL Advanced Measurement Services] como más estratégico, con el fin de informar las lecciones holísticas y tomar medidas vinculadas a los objetivos generales del negocio.

>[!MORELIKETHIS]
>
>* [Acerca de los informes personalizados](/help/dsp/reports/report-about.md)
>* [Crear un informe personalizado](/help/dsp/reports/report-create.md)
>* [Editar un informe personalizado](/help/dsp/reports/report-edit.md)
>* [Configuración de informes personalizados](/help/dsp/reports/report-settings.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)

