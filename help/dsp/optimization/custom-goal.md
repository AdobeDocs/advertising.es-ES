---
title: Objetivos personalizados
description: Obtenga información acerca de los objetivos personalizados para definir los eventos de éxito en paquetes optimizados para la CPA más baja o el ROAS más alto.
feature: DSP Optimization
source-git-commit: 7b9926d0bbba12728ed6a42e56115e8df708587b
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# Objetivos personalizados

Las metas personalizadas definen los eventos de éxito que un anunciante necesita para alcanzar sus objetivos comerciales. Cada paquete que utiliza el objetivo de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; debe incluir un objetivo personalizado que ayude a lograr el objetivo de optimización general. Puede crear objetivos personalizados como *objetivos* in [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Cada objetivo personalizado consta de una o más métricas de conversión y de los pesos relativos de esas métricas. Las métricas de conversión disponibles incluyen todas las métricas rastreadas con el píxel de conversión de Adobe Advertising y a través de Adobe Analytics.

Por ejemplo, supongamos que hay tres métricas de conversión relevantes para un paquete específico en una de las campañas: &quot;Descarga de PDF&quot; valorada en 20 USD, &quot;Suscripción por correo electrónico&quot; valorada en 30 USD y &quot;Confirmación de pedido&quot; valorada en 40 USD. Si desea dar peso según el valor monetario único de la acción del cliente, los pesos relativos de las métricas serían 1, 1,5 y 2.

Una vez que [crear una meta personalizada](#custom-goal-create), puede [asignarlo a un paquete](/help/dsp/campaign-management/packages/package-settings.md) para la optimización algorítmica y de informes con Adobe Sensei.

## Crear una meta personalizada {#custom-goal-create}

DSP Para crear un objetivo personalizado, la cuenta de la debe estar vinculada a un [!DNL Search, Social, & Commerce] cuenta con el mismo ID de organización de Adobe Experience Cloud, desde el [!DNL Search, Social, & Commerce] configuración de cliente. DSP Si la cuenta de la cuenta de la cuenta no está vinculada a un [!DNL Search, Social, & Commerce] y, a continuación, póngase en contacto con el equipo de cuenta de Adobe.

1. Iniciar sesión en [!DNL Advertising Search, Social, & Commerce] at (usuarios de Norteamérica) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) o (todos los demás usuarios) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Asegúrese de que se ha realizado el seguimiento de las métricas que desea incluir en el objetivo, que están disponibles en el producto e incluyen un nombre para mostrar:

   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Busque la métrica y asegúrese de que **[!UICONTROL Show in UI and Reports]** está habilitado para la métrica.

      >[!NOTE]
      >
      >* [!DNL Analytics] los eventos personalizados siguen esta convención de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Ejemplo: `custom_event_16_examplersid`

   1. Si la métrica no tiene un valor en **[!UICONTROL Display Name]** y, en la celda, introduzca el nombre para mostrar y haga clic en **[!UICONTROL Apply].**

1. Crear el objetivo personalizado como *objetivo*:

   1. En el menú principal, haga clic en **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. En la barra de herramientas, haga clic en ![Crear](/help/dsp/assets/create-search-ui.png "Crear").

   1. Introduzca la configuración del objetivo, incluidas las métricas asociadas y sus pesos numéricos relativos para dispositivos no móviles y dispositivos móviles, y luego guarde el objetivo.

      Al menos una métrica debe tener el tipo de métrica *[!UICONTROL Goal]*.

      >[!NOTE]
      >
      >* [!DNL Analytics] los eventos personalizados siguen esta convención de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Ejemplo: `custom_event_16_examplersid`
      >* [!DNL Analytics] las dimensiones y los segmentos no están disponibles para la optimización de Adobe Advertising.

      >[!TIP]
      >
      >Para obtener un rendimiento óptimo, las métricas combinadas en el objetivo personalizado (objetivo) deben sumar al menos diez conversiones al día. Si no es así, se recomienda añadir al objetivo métricas de conversión compatibles adicionales, como páginas de productos o inicios de aplicaciones. Consulte [Prácticas recomendadas para crear una meta personalizada](#custom-goal-best-practices) para obtener directrices.

DSP En la configuración del paquete de la para paquetes que utilizan el objetivo de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)],&quot; el nombre del objetivo ahora se incluye en la [!UICONTROL Custom Goals] lista. Al seleccionar el objetivo como objetivo personalizado para un paquete, la variable [!UICONTROL Conversion Metric] La lista incluye todas las métricas de objetivo del objetivo.

## Prácticas recomendadas para crear una meta personalizada {#custom-goal-best-practices}

### Objetivos personalizados con una sola métrica

Los siguientes ejemplos muestran cómo se pueden configurar objetivos dirigidos a una única métrica de conversión.

#### Ejemplo de una campaña con &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot; Objetivo de optimización

Si el objetivo de la campaña son los ingresos ([!UICONTROL Highest Return on Ad Spend (ROAS)]), y los ingresos de todos los tipos de dispositivos son igualmente importantes para usted, a continuación, incluya el &quot;[!UICONTROL Revenue]&quot; con una ponderación no móvil (para conversiones desde un dispositivo no móvil) de uno (1) y una ponderación móvil (para conversiones desde un dispositivo móvil) de uno (1). Seleccionar el tipo de métrica *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un peso móvil o peso no móvil de uno (1) equivale a un valor de uno (1) por cada $1 de ingresos que se rastrea.
>
> Por ejemplo, una conversión de 250 $ con una ponderación no móvil de uno (1) se registra como 250 $ para las conversiones. Si a la métrica de conversión se le asigna una ponderación no móvil de 0,5, la conversión de 250 $ desde un dispositivo no móvil se registra como 125 $ en Adobes Advertising (conversión de 250 $ * 0,5 [!UICONTROL Non-mobile Weight] = 125 $).

#### Ejemplo de una campaña con &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; Objetivo de optimización

Si el objetivo de la campaña es el menor coste por adquisición (CPA) y solo requiere un evento de éxito (como &quot;Envío de solicitud&quot;), incluya esa métrica y especifique el tipo de métrica como *[!UICONTROL Goal]*. La práctica recomendada es establecer tanto el peso no móvil como el peso móvil como uno (1).

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Una ponderación móvil o no móvil de uno (1) equivale a un valor de uno (1) para cada conversión de la que se realiza un seguimiento. Por ejemplo, si se realiza el seguimiento de 10 conversiones de envío de aplicaciones, se informa de 10 conversiones de envío de aplicaciones. Sin embargo, si a la métrica de conversión se le asigna una ponderación no móvil de 0,5, las 10 conversiones no móviles se registran como cinco (5) en Adobes Advertising (10 Conversiones * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Objetivos personalizados con varias métricas

Hay dos escenarios en los que utilizaría varias métricas en un objetivo personalizado:

* El objetivo de la campaña tiene varios eventos de éxito. Por ejemplo, es posible que esté anunciando más de una acción en el sitio (descarga de PDF, contacto con nosotros y registro por correo electrónico) y todas son acciones que contribuyen a su objetivo de CPA. Si el objetivo incluye las tres métricas independientes, cada una con pesos móviles y no móviles de uno (1), la variable [!DNL Adobe Sensei] Este algoritmo trata cada una de las métricas y tipos de dispositivos del usuario con la misma importancia. Si las distintas métricas y tipos de dispositivos tienen distintos costes o importancia, ajuste sus pesos relativos en consecuencia.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La métrica de conversión única del objetivo personalizado no alcanza el mínimo de 10 conversiones al día necesarias para un rendimiento optimizado. Esto puede ocurrir debido a un gasto diario mínimo en paquetes o a un número limitado de conversiones naturales. Añadir métricas de soporte adicionales al objetivo personalizado puede ayudarle a alcanzar el umbral de 10 conversiones al día. Diez eventos de soporte pueden ayudar a un paquete a alcanzar el umbral de 10/día, incluso cuando cada uno de sus pesos es inferior a uno (1). Sin embargo, es posible que no tenga que agregar tantos eventos.

  Cuando añada métricas de soporte a un objetivo personalizado, pongúrelas según su importancia relativa al evento de éxito principal y tenga en cuenta la cantidad de puntos de datos. Esto permite que el algoritmo de Adobe Sensei equilibre varias métricas y las optimice para alcanzar su objetivo.

  El siguiente objetivo de ejemplo incluye tres métricas, cada una con un peso diferente para los dispositivos no móviles: Envío de aplicación = 1, Inicio de aplicación = 0,1 y Página de aterrizaje del anunciante = 0,01. Esto significa que cada conversión de envío de aplicación desde dispositivos no móviles tiene el mismo valor para su empresa que un promedio de 10 conversiones de inicio de aplicación desde dispositivos no móviles y 100 conversiones de página de aterrizaje del anunciante desde dispositivos no móviles.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Si, en su lugar, ponderara las visitas de la página de aterrizaje de forma equitativa en los envíos de aplicaciones, la cantidad naturalmente mayor de visitas a la página de aterrizaje podría saturar el objetivo y distorsionar las visitas a la página de aterrizaje.<!--reword-->

>[!MORELIKETHIS]
>
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP Optimización de las campañas con la](optimization-how-dsp-optimizes-campaigns.md)
