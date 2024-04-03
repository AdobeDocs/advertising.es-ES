---
title: Acerca de los objetivos personalizados
description: Obtenga información acerca de los objetivos personalizados para definir los eventos de éxito en paquetes optimizados para la CPA más baja o el ROAS más alto.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: 6aa81fe4fd5ea6cb188b7f18b1574c26ddfcbb92
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Acerca de los objetivos personalizados

Las metas personalizadas definen los eventos de éxito que un anunciante necesita para alcanzar sus objetivos comerciales. Cada paquete que utiliza el objetivo de optimización &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; debe incluir un objetivo personalizado que ayude a lograr el objetivo de optimización general. Puede crear objetivos personalizados como *objetivos* in [!DNL Advertising Search, Social, & Commerce].

![metas personalizadas](/help/dsp/assets/objective-goals.png)

Cada objetivo personalizado consta de una o más métricas de conversión y de los pesos relativos de esas métricas. Las métricas de conversión disponibles incluyen todas las métricas rastreadas con el píxel de conversión de Adobe Advertising y a través de Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] las dimensiones y los segmentos no están disponibles para la optimización de Adobe Advertising.
>* DSP Para utilizar eventos de Analytics en la creación de informes, trabaje con su equipo de cuenta de Adobe de para configurar una integración de nivel de anunciante.
>* [!DNL Analytics] los eventos personalizados siguen esta convención de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Ejemplo: `custom_event_16_examplersid`

Por ejemplo, supongamos que hay tres métricas de conversión relevantes para un paquete específico en una de las campañas: &quot;Descarga de PDF&quot; valorada en 20 USD, &quot;Suscripción por correo electrónico&quot; valorada en 30 USD y &quot;Confirmación de pedido&quot; valorada en 40 USD. Si desea dar peso según el valor monetario único de la acción del cliente, los pesos relativos de las propiedades serían 1, 2 y 1,5.

Consulte la [prácticas recomendadas para crear objetivos personalizados](custom-goal-best-practices.md) para obtener sugerencias sobre cómo configurar los objetivos personalizados.

Una vez que [crear una meta personalizada](custom-goal-create.md), puede [asignarlo a un paquete](/help/dsp/campaign-management/packages/package-settings.md) para la optimización algorítmica y de informes con Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Crear una meta personalizada](custom-goal-create.md)
>* [Prácticas recomendadas para crear una meta personalizada](custom-goal-best-practices.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP Optimización de las campañas con la](optimization-how-dsp-optimizes-campaigns.md)
