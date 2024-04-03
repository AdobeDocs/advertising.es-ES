---
title: Prácticas recomendadas para crear una meta personalizada
description: Conozca las prácticas recomendadas para crear objetivos personalizados y definir los eventos de éxito.
feature: DSP Optimization, DSP Best Practices
exl-id: 8b1247cd-083d-4c8c-8588-9e8c03c4cc67
source-git-commit: 6aa81fe4fd5ea6cb188b7f18b1574c26ddfcbb92
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Prácticas recomendadas para crear una meta personalizada

## Objetivos personalizados con una sola propiedad

Los siguientes ejemplos muestran cómo se pueden configurar objetivos dirigidos a una única métrica de conversión.

### Ejemplo de una campaña con &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot; Objetivo de optimización

Si el objetivo de la campaña son los ingresos ([!UICONTROL Highest Return on Ad Spend (ROAS)]), entonces su objetivo personalizado (objetivo) incluirá la &quot;[!UICONTROL Revenue]&quot; métrica con un peso de uno (1).

![Ejemplo de un objetivo personalizado ROAS con una única métrica de conversión](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de uno equivale a un valor de uno por cada $1 de ingresos que se rastrean.
>
> Por ejemplo, una conversión de 250 $ con una ponderación de uno se registra como 250 $. Si a la métrica de conversión se le asigna una ponderación de 0,5, la conversión de 250 $ se registra como 125 $ en Adobes Advertising (conversión de 250 $ * 0,5 [!UICONTROL Property Weight] = 125 $).

### Ejemplo de una campaña con &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; Objetivo de optimización

Si el objetivo de la campaña es el menor coste por adquisición (CPA) y solo requiere un evento de éxito, incluirá esa métrica (en el siguiente ejemplo, &quot;Envío de solicitud&quot;). La práctica recomendada es establecer el peso como uno (1).

![Ejemplo de un objetivo personalizado de CPA con una única métrica de conversión](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de uno equivale a un valor de uno para cada conversión que se rastree.
>
> Por ejemplo, si se realiza el seguimiento de 10 conversiones de envío de aplicaciones, se informa de 10 conversiones de envío de aplicaciones.  Si a la métrica de conversión se le asigna una ponderación de 0,5, las 10 conversiones se registran como cinco (5) en Adobes Advertising (10 Conversiones * 0,5 [!UICONTROL Property Weight] = 5).

## Objetivos personalizados con varias propiedades

Existen dos escenarios en los que se pueden utilizar varias propiedades en un objetivo personalizado:

* El objetivo de la campaña tiene varios eventos de éxito. Por ejemplo, puede que esté anunciando más de una acción en el sitio y todas se atribuyan a su objetivo de CPA. El siguiente objetivo de ejemplo incluye tres propiedades independientes (Descarga del PDF, Contáctenos y Suscripción por correo electrónico), cada una con un peso de uno (1), que indica a la variable [!DNL Adobe Sensei] que cada una de las propiedades tiene la misma importancia. Si incluye propiedades con costes o importancia variables, puede ajustar sus pesos relativos en consecuencia.

  ![ejemplo de un objetivo personalizado con varias propiedades](/help/dsp/assets/custom-goal-multiple-properties.png)

* La métrica de conversión única del objetivo personalizado no alcanza el mínimo de 10 conversiones al día necesarias para un rendimiento optimizado. Esto puede ocurrir debido a un gasto diario mínimo en paquetes o a un número limitado de conversiones naturales. Añadir propiedades de compatibilidad adicionales al objetivo personalizado puede ayudarle a alcanzar el umbral de 10 conversiones al día. Diez eventos de soporte pueden ayudar a un paquete a alcanzar el umbral de 10/día, incluso cuando cada uno de sus pesos es inferior a uno (1). Sin embargo, es posible que no tenga que agregar tantos eventos.

  Cuando añada propiedades de compatibilidad a un objetivo personalizado, pondere estas según su importancia relativa al evento de éxito principal y tenga en cuenta la cantidad de puntos de datos. Esto permite que el algoritmo de Adobe Sensei equilibre varias propiedades y optimice el logro de su objetivo.

  El siguiente objetivo de ejemplo incluye tres propiedades, cada una con un peso diferente: Envío de solicitud = 1, Inicio de solicitud = 0,1 y Página de aterrizaje del anunciante = 0,01. Esto significa que cada conversión de envío de solicitud tiene para su empresa el mismo valor que un promedio de 10 conversiones de inicio de solicitud y 100 conversiones de página de aterrizaje del anunciante.

  ![ejemplo de un objetivo personalizado con varias propiedades](/help/dsp/assets/custom-goal-multiple-properties2.png)

  Si, en su lugar, ponderara las visitas de la página de aterrizaje de forma equitativa en los envíos de aplicaciones, la cantidad naturalmente mayor de visitas a la página de aterrizaje podría saturar el objetivo y distorsionar las visitas a la página de aterrizaje.<!--reword-->

>[!MORELIKETHIS]
>
>* [Acerca de los objetivos personalizados](custom-goal-about.md)
>* [Crear una meta personalizada](custom-goal-create.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP Optimización de las campañas con la](optimization-how-dsp-optimizes-campaigns.md)
