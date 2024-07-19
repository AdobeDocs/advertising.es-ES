---
title: Preguntas frecuentes sobre informes de hogares
description: Obtenga más información acerca del alcance, la frecuencia y los datos de conversión del hogar, incluido cómo los informes del hogar son diferentes de otros informes y la resolución de problemas.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# Preguntas frecuentes sobre informes de hogares

## El informe [!UICONTROL Household Reach & Frequency]

### ¿En qué se diferencian los informes de [!UICONTROL Household Reach & Frequency] de otros informes personalizados?

El informe [!UICONTROL Household Reach & Frequency] mide el alcance, la impresión y la frecuencia en varias dimensiones a nivel doméstico según la dirección IP. Los demás informes personalizados se generan en el nivel de dispositivo o cookie.

Por ejemplo, incluso si se sirve una impresión a tres dispositivos dentro de un hogar, la métrica Alcanzado en el hogar único es una.

#### Dimension admitidos

El informe [!UICONTROL Household Reach & Frequency] admite las [siguientes dimensiones](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (que no proporciona acceso a las métricas de superposición), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length]&quot; y la ubicación creada por el usuario &quot;[!UICONTROL Tags].&quot; |

#### Métricas compatibles

Las [métricas disponibles](/help/dsp/reports/report-columns.md) incluyen:

* Métricas de superposición: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)] y [!UICONTROL Unique Household (Overlap)].

  Las métricas de superposición son valores que se producen únicamente para la dimensión o combinación de dimensiones del informe y no para otras dimensiones. <!-- For example, it might show the ?? -->

* Métricas que no se superponen: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions] y [!UICONTROL Unique Household Reached]

Las métricas de conversión y los objetivos personalizados no son compatibles.

### ¿Cuál es la diferencia entre las métricas de superposición y las que no son de superposición?

La siguiente figura muestra tres métricas (Hogar único alcanzado, Hogar incremental alcanzado y Hogar incremental (superpuesto)) para tres campañas (A, B y C).

![Ilustración de métricas de superposición de hogares](/help/dsp/assets/household-overlap-metrics-illustration.png "Ilustración de métricas de superposición de hogares")

* Unique Household Reached (Total) proporciona el Unique Household alcanzado por cada una de las campañas o el área total de cada uno de los círculos. En la figura, Hogar único alcanzado por A = Hogar incremental alcanzado por A + (A+B) + (A+C) + (A+B+C)

* El hogar incremental alcanzado es el hogar único al que solo se ha llegado mediante una campaña. En la figura, el hogar incremental alcanzado por A, B, C es el hogar incremental alcanzado por A, B, C respectivamente.

* Hogar incremental (superposición) es el hogar único al que se llega mediante la campaña o la combinación de campañas. En la figura, el hogar incremental alcanzado por A, C es A + C.

### Flujo de trabajo

Siga los pasos normales para [crear un informe personalizado](report-create.md).

El informe [!UICONTROL Household Reach & Frequency] solo puede incluir una dimensión. También puede incluir a) métricas de superposición de cualquier dimensión, excepto Sitio/Aplicaciones o b) métricas no superpuestas, pero no ambas.

### ¿Cuáles son algunas limitaciones del informe [!UICONTROL Household Reach & Frequency]?

Los informes con métricas de superposición generan intersecciones de hasta tres valores. Por ejemplo, si utiliza la métrica [!UICONTROL Unique Household (Overlap)] para 10 ubicaciones, podrá ver los hogares únicos a los que han llegado las ubicaciones individuales, los hogares comunes a los que ha llegado una combinación de dos ubicaciones cualesquiera y los hogares comunes a los que han llegado combinaciones de tres ubicaciones cualesquiera. No se pueden ver hogares comunes a los que se haya llegado en cuatro o más ubicaciones.

Para dimensiones que no sean campaña, paquete o ubicación, el informe admite hasta 10 valores en cada dimensión. Por ejemplo, para generar un informe [!UICONTROL Unique Household Reached] para la dimensión [!UICONTROL Audience], el número de audiencias únicas debe ser inferior o igual a 10. Si incluye más de 10 audiencias únicas, se genera un informe en blanco.

### ¿Por qué la frecuencia y los valores de alcance únicos son diferentes entre mis informes [!UICONTROL Custom] y el informe [!UICONTROL Household Reach & Frequency]?

Estas métricas en los informes [!UICONTROL Household] se calculan usando el recuento real de direcciones IP, mientras que las métricas del informe [!UICONTROL Custom] utilizan números estimados calculados mediante modelos. Sin embargo, la discrepancia debe ser inferior al 10 %.

### ¿Cómo configuro el informe para la dimensión [!UICONTROL Placement Tags]?

Para crear etiquetas para la ubicación, [abra la configuración de ubicación](/help/dsp/campaign-management/placements/placement-edit.md) e introduzca valores en el campo [Etiquetas de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

Cuando una ubicación incluye varias etiquetas, el informe considera toda la cadena como una etiqueta. El informe incluye una fila por cada cadena única.

## El informe [!UICONTROL Household Conversions]

### ¿Cuáles son los tipos de métodos de atribución admitidos en el informe [!UICONTROL Household Conversions]?

Se admiten dos tipos de métodos de atribución:

* [!UICONTROL Unique]: Cuenta el número de veces que un valor de dimensión (como un dispositivo o una ubicación) estaba en la ruta de conversión.

* [!UICONTROL Multi-Touch Attribution (MTA)]: distribuye el crédito de cada conversión en función de la frecuencia con la que se produjo el valor de dimensión (como un dispositivo o una ubicación) en la ruta de acceso a la conversión. Por ejemplo, si había un total de 10 impresiones antes de la conversión, con 8 en CTV y 2 en Mobile, entonces el 80% del crédito (0,8) se da a las pantallas CTV y 0,2 a Mobile.

### ¿En qué se diferencian los informes de conversión doméstica de los informes de visualización de CTV en Adobe Analytics?

Los datos de visualizaciones de CTV en [!DNL Analytics] se alimentan del seguimiento [!DNL Analytics], y los datos de conversión del hogar utilizan datos recopilados mediante el seguimiento de conversión de Adobe Advertising. DSP Además, la lógica de atribución de en [!DNL Analytics] utiliza solo el último evento, pero los informes de conversión de hogares admiten dos métodos de atribución diferentes: Único y MTA.

### ¿Puedo ver los datos de visualizaciones de CTV tanto en [!DNL Analytics for Advertising] como en los informes personalizados?

Anunciantes sin [!DNL Analytics for Advertising] solo pueden usar el Informe de conversión de hogares para los informes de conversión de hogares.

Si su organización tiene [!DNL Analytics for Advertising], utilice ambos tipos de informes a la vez. Aunque los informes de visualización de CTV son adecuados para el análisis de canales generales, el comportamiento del sitio, etc., los informes personalizados proporcionan una vista granular (con datos desglosados por tipo de medios, editores, etc.) para indicar los factores que impulsan las tasas de conversión.

## Informes [!UICONTROL Household Reach & Frequency] y [!UICONTROL Household Conversions] frente a datos de [!DNL Advanced Measurement Services]

Para generar informes avanzados sobre el alcance y la frecuencia o las conversiones basados en el hogar, el [[!DNL Strategic Advertising Consulting] equipo](/help/dsp/introduction/advanced-measurement-services.md) puede proporcionar informes altamente personalizables junto con recomendaciones estratégicas holísticas. Para obtener más información sobre [!DNL Advanced Measurement Services], comuníquese con el equipo de cuenta de Adobe.

### Si ya estoy usando [!DNL Advanced Measurement Services], ¿por qué debería usar los informes [!UICONTROL Household Reach & Frequency] y [!UICONTROL Household Conversions]?

Los informes [!UICONTROL Household Reach & Frequency] y [!UICONTROL Household Conversions] permiten a los clientes extraer de forma autónoma en tiempo real las métricas de alcance, frecuencia y conversión a nivel doméstico, respectivamente.

### ¿Puedo usar los informes [!UICONTROL Household Reach & Frequency] y [!UICONTROL Household Conversions], y [!DNL Advanced Measurement Services]?

El caso de uso ideal es usar juntos el informe [!UICONTROL Household] y los servicios de consultoría e informes [!DNL Advanced Measurement Services]. Considere el informe [!UICONTROL Household] como transaccional, con el fin de informar las optimizaciones diarias, y [!DNL Advanced Measurement Services] como más estratégico, con el fin de informar las lecciones integrales y las ofertas para llevar vinculadas a los objetivos empresariales generales.

>[!MORELIKETHIS]
>
>* [Acerca de los informes personalizados](/help/dsp/reports/report-about.md)
>* [Crear un informe personalizado](/help/dsp/reports/report-create.md)
>* [Editar un informe personalizado](/help/dsp/reports/report-edit.md)
>* [Configuración de informe personalizada](/help/dsp/reports/report-settings.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)
