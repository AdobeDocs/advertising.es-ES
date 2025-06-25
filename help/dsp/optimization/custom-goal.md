---
title: Objetivos personalizados
description: Obtenga información acerca de los objetivos personalizados para definir los eventos de éxito en paquetes optimizados para la CPA más baja o el ROAS más alto.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# Objetivos personalizados

Las metas personalizadas definen los eventos de éxito que un anunciante necesita para alcanzar sus objetivos comerciales. Cada paquete que usa el objetivo de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; debe incluir un objetivo personalizado para ayudar a lograr el objetivo de optimización general. Puede crear metas personalizadas como *objetivos* en [!DNL Advertising Search, Social, & Commerce]. El nombre de cada objetivo para DSP debe ir precedido del prefijo &quot;ADSP_&quot;.

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Cada objetivo personalizado (objetivo) consta de una o más métricas de conversión y de los pesos relativos de esas métricas. Las métricas de conversión disponibles incluyen todas las métricas rastreadas con el píxel de conversión de Adobe Advertising y a través de Adobe Analytics. Solo se tienen en cuenta los pesos que no son móviles para los objetivos personalizados de DSP, pero se utilizan para todos los tipos de anuncios.

Por ejemplo, supongamos que hay tres métricas de conversión relevantes para un paquete específico en una de las campañas: &quot;Descarga de PDF&quot; valorada en 20 USD, &quot;Suscripción por correo electrónico&quot; valorada en 30 USD y &quot;Confirmación de pedido&quot; valorada en 40 USD. Si desea dar peso según el valor monetario único de la acción del cliente, los pesos relativos de las métricas serían 1, 1,5 y 2.

Una vez que [cree una meta personalizada](#custom-goal-create), puede [asignarla a un paquete](/help/dsp/campaign-management/packages/package-settings.md) para la optimización algorítmica y de informes mediante Adobe Sensei.

Las recomendaciones de peso se generan automáticamente para métricas atribuidas a DSP en objetivos y pueden aplicarse con un solo clic. Todos los cambios de peso en los objetivos con el prefijo &quot;ADSP_&quot; se aplican de forma algorítmica en DSP en un plazo de dos días. Para obtener más información sobre las recomendaciones de peso, consulte el capítulo Guía de optimización sobre &quot;Nuevos objetivos de (Beta)&quot;, que está disponible en Search, Social y Commerce.

## Crear una meta personalizada {#custom-goal-create}

Para crear un objetivo personalizado, la cuenta de DSP debe estar vinculada a una cuenta de [!DNL Search, Social, & Commerce] con el mismo identificador de organización de Adobe Experience Cloud, desde la configuración de cliente de [!DNL Search, Social, & Commerce]. Si su cuenta de DSP no está vinculada a una cuenta de [!DNL Search, Social, & Commerce], póngase en contacto con el equipo de cuenta de Adobe.

1. Inicie sesión en [!DNL Advertising Search, Social, & Commerce] a las(os) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) o (todos los demás usuarios) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Asegúrese de que se ha realizado el seguimiento de las métricas que desea incluir en el objetivo, que están disponibles en el producto e incluyen un nombre para mostrar:

   1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Busque la métrica y asegúrese de que **[!UICONTROL Show in UI and Reports]** esté habilitado para la métrica.

      >[!NOTE]
      >
      >* [!DNL Analytics] eventos personalizados siguen esta convención de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Ejemplo: `custom_event_16_examplersid`

   1. Si la métrica no tiene un valor en la columna **[!UICONTROL Display Name]**, haga clic en la celda, escriba el nombre para mostrar y haga clic en **[!UICONTROL Apply].**

1. Crear la meta personalizada como *objetivo*:

   1. En el menú principal, haga clic en **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. En la barra de herramientas, haz clic en ![Crear](/help/dsp/assets/create-search-ui.png "Crear").

   1. Introduzca la configuración del objetivo, incluidas las métricas asociadas y sus pesos numéricos relativos para dispositivos no móviles, y luego guarde el objetivo. Tenga en cuenta lo siguiente:

      * Para los objetivos utilizados para los paquetes de Advertising DSP, el nombre del objetivo debe ir precedido del prefijo &quot;ADSP_&quot; como &quot;ADSP_Registrations&quot;. El prefijo no distingue entre mayúsculas y minúsculas.

      * Incluya solo las métricas que se atribuyen a DSP. Se ignorará cualquier métrica atribuida a Search, Social y Commerce, o a cualquier otra red de publicidad.

      * Al menos una métrica debe tener el tipo de métrica *[!UICONTROL Goal]*.

      * DSP utiliza las ponderaciones no móviles para todos los anuncios. Se ignorarán todos los pesos móviles especificados.

      >[!NOTE]
      >
      >* [!DNL Analytics] eventos personalizados siguen esta convención de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Ejemplo: `custom_event_16_examplersid`
      >* [!DNL Analytics] dimensiones y segmentos no están disponibles para la optimización de Adobe Advertising.

      >[!TIP]
      >
      >Para obtener un rendimiento óptimo, las métricas combinadas en el objetivo personalizado (objetivo) deben sumar al menos diez conversiones al día. Si no es así, se recomienda añadir al objetivo métricas de conversión compatibles adicionales, como páginas de productos o inicios de aplicaciones. Vea [Prácticas recomendadas para crear un objetivo personalizado](#custom-goal-best-practices) para obtener instrucciones.

En la configuración del paquete de DSP para los paquetes que utilizan el objetivo de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;, el nombre del objetivo ahora se incluye en la lista [!UICONTROL Custom Goals]. Al seleccionar el objetivo como objetivo personalizado para un paquete, la lista [!UICONTROL Conversion Metric] incluye todas las métricas de objetivo del objetivo.

## Prácticas recomendadas para crear una meta personalizada {#custom-goal-best-practices}

### Objetivos personalizados con una sola métrica

Los siguientes ejemplos muestran cómo se pueden configurar objetivos dirigidos a una única métrica de conversión.

#### Ejemplo de una campaña con el objetivo de optimización [!UICONTROL Highest Return on Ad Spend (ROAS)]

Si el objetivo de la campaña son los ingresos ([!UICONTROL Highest Return on Ad Spend (ROAS)]) y los ingresos de todos los tipos de dispositivos son igualmente importantes para usted, incluya la métrica &quot;[!UICONTROL Revenue]&quot; con una ponderación no móvil de uno (1); se omitirá la ponderación móvil. Seleccione el tipo de métrica *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso no móvil de uno (1) equivale a un valor de uno (1) por cada $1 de ingresos que se rastrean para mostrar anuncios en cualquier dispositivo. Por ejemplo, una conversión de 250 $ con una ponderación no móvil de uno (1) se registra como 250 $ para las conversiones. Si a la métrica de conversión se le asigna una ponderación no móvil de 0,5, la conversión de 250 $ se registra como 125 $ en Adobe Advertising (conversión de 250 $ * 0,5 [!UICONTROL Non-mobile Weight] = 125 $).

#### Ejemplo de una campaña con el objetivo de optimización [!UICONTROL Lowest Cost per Acquisition (CPA)]

Si el objetivo de la campaña es el menor coste por adquisición (CPA) y solo requiere un evento de éxito (como &quot;Envío de solicitud&quot;), incluya esa métrica y especifique el tipo de métrica como *[!UICONTROL Goal]*. La práctica recomendada es establecer el peso no móvil como uno (1); se ignora el peso móvil.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Una ponderación no móvil de uno (1) equivale a un valor de uno (1) para cada conversión de la que se realiza un seguimiento de los anuncios en pantalla de cualquier dispositivo. Por ejemplo, si se realiza el seguimiento de 10 conversiones de envío de aplicaciones, se informa de 10 conversiones de envío de aplicaciones. Sin embargo, si a la métrica de conversión se le asigna una ponderación no móvil de 0,5, las 10 conversiones se registran como cinco (5) en Adobe Advertising (10 conversiones * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Objetivos personalizados con varias métricas

Hay dos escenarios en los que utilizaría varias métricas en un objetivo personalizado:

* El objetivo de la campaña tiene varios eventos de éxito. Por ejemplo, puede que esté anunciando más de una acción en el sitio (descarga de PDF, póngase en contacto con nosotros y regístrese por correo electrónico), y todas son acciones que contribuyen a su objetivo de CPA. Si el objetivo incluye las tres métricas independientes, cada una con pesos no móviles de uno (1), el algoritmo [!DNL Adobe Sensei] tratará cada una de las métricas y tipos de dispositivos de usuario con la misma importancia. Si las distintas métricas tienen distintos costes o importancia, debe ajustar sus pesos relativos en consecuencia.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La métrica de conversión única del objetivo personalizado no alcanza el mínimo de 10 conversiones al día necesarias para un rendimiento optimizado. Esto puede ocurrir debido a un gasto diario mínimo en paquetes o a un número limitado de conversiones naturales. Añadir métricas de soporte adicionales al objetivo personalizado puede ayudarle a alcanzar el umbral de 10 conversiones al día. Diez eventos de soporte pueden ayudar a un paquete a alcanzar el umbral de 10/día, incluso cuando cada uno de sus pesos es inferior a uno (1). Sin embargo, es posible que no tenga que agregar tantos eventos.

  Cuando añada métricas de soporte a un objetivo personalizado, pongúrelas según su importancia relativa al evento de éxito principal y tenga en cuenta la cantidad de puntos de datos. Esto permite que el algoritmo de Adobe Sensei equilibre varias métricas y las optimice para alcanzar su objetivo.

  El siguiente objetivo de ejemplo incluye tres métricas, cada una con un peso diferente para los dispositivos no móviles: Envío de aplicación = 1, Inicio de aplicación = 0,1 y Página de aterrizaje del anunciante = 0,01. Esto significa que cada conversión de envío de solicitud tiene para su empresa el mismo valor que un promedio de 10 conversiones de inicio de solicitud y 100 conversiones de página de aterrizaje del anunciante.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Si, en su lugar, ponderara las visitas de la página de aterrizaje de forma equitativa en los envíos de aplicaciones, la cantidad naturalmente mayor de visitas a la página de aterrizaje podría saturar su objetivo y sesgar las visitas a la página de aterrizaje.<!--reword-->

>[!MORELIKETHIS]
>
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
> * [Cómo DSP Optimiza Sus Campañas](optimization-how-dsp-optimizes-campaigns.md)
