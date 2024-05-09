---
title: Filtros previos a la oferta de nivel de ubicación y cómo utilizarlos
description: Consulte los filtros de oferta previa de nivel de ubicación disponibles y vea cómo utilizarlos.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Filtros previos a la oferta de nivel de ubicación y cómo utilizarlos

| Filtro de puja previa | Descripción | Cuándo usar este filtro |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Establece un umbral de predicción mínimo para la probabilidad de que una subasta pueda dar lugar a una pulsación. Por ejemplo, si establece el umbral en 0,1%, solo pujará en subastas cuando la probabilidad prevista de un clic sea mayor o igual que el 0,1%.<br><br><b>Nota:</b> Los filtros se aplican antes de los objetivos de optimización. Como resultado, los filtros muy estrictos pueden impedir el gasto. | Utilícelo cuando tenga un objetivo de KPI mínimo para la tasa de clics (CTR) y no desee gastar su presupuesto cuando el CTR esté por debajo del umbral. Este filtro puede ser bastante restrictivo, por lo que es importante establecer objetivos realistas. Dependiendo de otras restricciones en la ubicación, un objetivo de 0,03-,07% es generalmente un buen punto de partida. Puede optimizar esto en el nivel de sitio según sea necesario para ayudar a mejorar las métricas.<br><br>Si su objetivo es lograr un CTR mínimo y el mejor CPM posible, la configuración recomendada es combinar un [!UICONTROL Click Through Rate] filtre con el objetivo de optimización &quot;[!UICONTROL Lowest CPM].&quot; Si su objetivo es un CPM máximo sin beneficio real por lograr más de lo debido, y un CTR mínimo, entonces emparejando un [!UICONTROL Click Through Rate] filtre con el objetivo de optimización &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; puede ser más apropiado. |
| [!UICONTROL 100% Completion Rate] | Establece una tasa mínima de finalización requerida que debe cumplirse antes de pujar por una impresión. | Utilice este filtro cuando el objetivo principal de la campaña sea las tasas de finalización. Tenga en cuenta otros parámetros de segmentación, pero el porcentaje de inicio recomendado es del 65 %. |
| [!UICONTROL Player Size - Adobe] | DSP Establece un tamaño mínimo del reproductor requerido, utilizando los datos de la aplicación de datos de la aplicación de datos de la aplicación Pujarás por una impresión cuando el [!UICONTROL Player Size] se ha alcanzado el umbral. | DSP Úselo para asegurarse de que está entregando el inventario de reproductores de episodio completo con los datos de la aplicación de datos de la aplicación de datos de la aplicación de datos de la aplicación de reproducción de la aplicación. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Establece un tamaño mínimo de reproductor requerido, con datos de [!DNL Moat] o [!DNL Integral Ad Science] ([!DNL IAS]). Pujarás por una impresión cuando el [!UICONTROL Player Size] se ha alcanzado el umbral. | Úselo para asegurarse de que está entregando el inventario de reproductores de episodios completos usando toda la plataforma [!DNL Moat] o [!DNL IAS] datos.<br><br><b>Nota:</b> Utilice este filtro solo cuando la campaña esté configurada para utilizar [!DNL Moat] o [!DNL IAS] datos. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | DSP Establece un porcentaje mínimo de visibilidad requerido, usando números y medidas de visibilidad de la vista de la. Pujarás por una impresión cuando se alcance el umbral especificado.<br><br><b>Notas:</b><ul><li>Si la campaña es [!UICONTROL Viewability Sensitivity] La configuración es &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)],&quot; y luego el [!DNL Media Rating Council] (MRC) El estándar de medición de la visibilidad se utiliza para la campaña. Si la variable [!UICONTROL Viewability Sensitivity] La configuración es &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)],&quot; y luego el [!DNL GroupM] el estándar de medición de visibilidad se usa para la campaña.</li><li>Las definiciones de medición de Adobes difieren de las definiciones de terceros, por lo que puede haber pequeñas discrepancias con los datos de terceros.</li></ul> | La práctica recomendada es hacer coincidir el objetivo de optimización y cualquier configuración de filtro de oferta previa con el de la campaña [!UICONTROL Viewability Sensitivity] configuración. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [DSP Optimización de las campañas con la](optimization-how-dsp-optimizes-campaigns.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
