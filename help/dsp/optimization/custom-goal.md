---
title: Prácticas recomendadas para objetivos personalizados
description: Conozca las prácticas recomendadas para definir objetivos personalizados para paquetes optimizados para la CPA más baja o el ROAS más alto.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# Prácticas recomendadas para objetivos personalizados

Las metas personalizadas definen los eventos de éxito que un anunciante necesita para alcanzar sus objetivos comerciales. Cada paquete que usa el objetivo de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; debe incluir un objetivo personalizado para ayudar a lograr el objetivo de optimización general. Puede crear metas personalizadas como *[objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md)*.

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Cada objetivo personalizado (objetivo) consiste en una o más métricas de conversión que se van a rastrear y optimizar, y los pesos relativos de esas métricas. Puede [asignar una meta personalizada a un paquete](/help/dsp/campaign-management/packages/package-settings.md) para la optimización algorítmica y de informes mediante [!DNL Adobe AI].

Para crear y administrar metas personalizadas, consulte &quot;[Administrar objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md)&quot;.

## Metas personalizadas con una sola métrica

Los siguientes ejemplos muestran cómo se pueden configurar objetivos dirigidos a una única métrica de conversión.

### Ejemplo de una campaña con el objetivo de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;

Si el objetivo de la campaña son los ingresos ([!UICONTROL Highest Return on Ad Spend (ROAS)]) y los ingresos de todos los tipos de dispositivos son igualmente importantes para usted, incluya la métrica &quot;[!UICONTROL Revenue]&quot; con una ponderación de uno (1). Seleccione el tipo de métrica *[!UICONTROL Goal]*.

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso de uno (1) equivale a un valor de uno (1) por cada $1 de ingresos que se rastrean para mostrar anuncios en cualquier dispositivo. Por ejemplo, una conversión de 250 $ con una ponderación de uno (1) se registra como 250 $ para las conversiones. Si a la métrica de conversión se le asigna una ponderación de 0,5, la conversión de 250 $ se registra como 125 $ en Adobe Advertising (conversión de 250 $ * 0,5 [!UICONTROL weight] = 125 $).

### Ejemplo de una campaña con el objetivo de optimización &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;

Si el objetivo de la campaña es el menor coste por adquisición (CPA) y solo requiere un evento de éxito (como &quot;Envío de solicitud&quot;), incluya esa métrica y especifique el tipo de métrica como *[!UICONTROL Goal]*. La práctica recomendada es establecer el peso como uno (1).

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso de uno (1) equivale a un valor de uno (1) para cada conversión de la que se realiza un seguimiento de los anuncios en pantalla de cualquier dispositivo. Por ejemplo, si se realiza el seguimiento de 10 conversiones de envío de aplicaciones, se informa de 10 conversiones de envío de aplicaciones. Sin embargo, si a la métrica de conversión se le asigna una ponderación de 0,5, las 10 conversiones se registran como cinco (5) en Adobe Advertising (10 conversiones * 0,5 [!UICONTROL weight] = 5).

## Metas personalizadas con varias métricas

Hay dos escenarios en los que utilizaría varias métricas en un objetivo personalizado:

* El objetivo de la campaña tiene varios eventos de éxito. Por ejemplo: tal vez esté anunciando más de una acción en el sitio (descarga de PDF, póngase en contacto con nosotros y regístrese por correo electrónico) y todas son acciones que contribuyen a su objetivo de CPA. Si el objetivo incluye las tres métricas independientes, cada una con pesos de uno (1), el algoritmo con tecnología [!DNL Adobe AI] tratará cada una de las métricas y tipos de dispositivos de usuario con la misma importancia. Si las distintas métricas tienen distintos costes o importancia, ajuste sus ponderaciones relativas en consecuencia.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La métrica de conversión única del objetivo personalizado no alcanza el mínimo de 10 conversiones al día necesarias para un rendimiento optimizado. Se pueden producir cantidades menores de conversiones debido a un gasto mínimo diario en paquetes o a un número limitado de conversiones naturales. Añadir métricas de soporte adicionales al objetivo personalizado puede ayudarle a alcanzar el umbral de 10 conversiones al día. Diez eventos de soporte pueden ayudar a un paquete a alcanzar el umbral de 10/día, incluso cuando cada uno de sus pesos es inferior a uno (1). Sin embargo, es posible que no tenga que agregar tantos eventos.

  Cuando añada métricas de soporte a un objetivo personalizado, pongúrelas según su importancia relativa al evento de éxito principal y tenga en cuenta la cantidad de puntos de datos. Esto permite que el algoritmo de [!DNL Adobe AI] equilibre varias métricas y las optimice hacia su objetivo.

  El siguiente objetivo de ejemplo incluye tres métricas, cada una con un peso diferente: Envío de solicitud = 1, Inicio de solicitud = 0,1 y Página de aterrizaje del anunciante = 0,01. Esto significa que cada conversión de envío de solicitud tiene para su empresa el mismo valor que un promedio de 10 conversiones de inicio de solicitud y 100 conversiones de página de aterrizaje del anunciante.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Si, en su lugar, ponderara las visitas de la página de aterrizaje de forma equitativa en los envíos de aplicaciones, la cantidad naturalmente mayor de visitas a la página de aterrizaje podría saturar el objetivo y sesgar la optimización hacia las visitas a la página de aterrizaje.

>[!MORELIKETHIS]
>
>* [Administrar objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md)
>* [Objetivos de optimización y cómo usarlos](optimization-goals.md)
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
>* [Cómo DSP optimiza sus campañas](optimization-how-dsp-optimizes-campaigns.md)
