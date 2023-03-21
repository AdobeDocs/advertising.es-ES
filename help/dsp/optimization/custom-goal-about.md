---
title: Acerca de los objetivos personalizados
description: Obtenga información sobre los objetivos personalizados para definir los eventos de éxito en paquetes optimizados para la CPA más baja o el ROAS más alto.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Acerca de los objetivos personalizados

Los objetivos personalizados definen los eventos de éxito que requiere un anunciante para alcanzar sus objetivos comerciales. Cada paquete que utiliza los objetivos de optimización &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; o &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; debe incluir un objetivo personalizado que ayude a lograr el objetivo de optimización general. Puede crear objetivos personalizados como *objetivos* en [!DNL Advertising Search, Social, & Commerce].

![objetivos personalizados](/help/dsp/assets/objective-goals.png)

Cada objetivo personalizado consta de una o más métricas, o *propiedades de transacción* y las ponderaciones relativas de esas propiedades de transacción. Las propiedades de transacción disponibles incluyen todas las métricas rastreadas utilizando el píxel de conversión de publicidad de Adobe y a través de Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] las dimensiones y los segmentos no están disponibles para la optimización de la publicidad de Adobe.
>* Para usar eventos de Analytics en DSP, trabaje con su equipo de cuentas de Adobe para configurar una integración de nivel de anunciante.
>* [!DNL Analytics] los eventos personalizados siguen esta convención de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Ejemplo: `custom_event_16_examplersid`


Por ejemplo, supongamos que tres métricas (propiedades de transacción) son relevantes para un paquete específico de una de las campañas: &quot;PDF Download&quot; valorado en 20 USD, &quot;Email Signup&quot; valorado en 30 USD, y &quot;Order Confirmation&quot; valorado en 40 USD. Si desea dar peso según el valor monetario único de la acción del cliente, las ponderaciones relativas de las propiedades serían 1, 2 y 1,5.

Consulte la [prácticas recomendadas para crear objetivos personalizados](custom-goal-best-practices.md) para obtener sugerencias sobre cómo configurar los objetivos personalizados.

Una vez que [crear un objetivo personalizado](custom-goal-create.md), puede [asignarlo a un paquete](/help/dsp/campaign-management/packages/package-settings.md) para la creación de informes y la optimización algorítmica con Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Crear un objetivo personalizado](custom-goal-create.md)
>* [Prácticas recomendadas para crear un objetivo personalizado](custom-goal-best-practices.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
> * [Cómo DSP las campañas](optimization-how-dsp-optimizes-campaigns.md)

