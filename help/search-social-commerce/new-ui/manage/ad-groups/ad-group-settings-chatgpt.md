---
title: '[!DNL ChatGPT] configuración del grupo de anuncios'
description: Hacer referencia a la configuración de [!DNL ChatGPT] grupos de anuncios.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
source-git-commit: 52c1132246ea0cc48b6102e6d6f15be1ded32f09
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%
---
# [!DNL ChatGPT] configuración del grupo de anuncios

*Los anuncios de [!DNL ChatGPT] son una característica piloto de[!DNL OpenAI]*

## Ficha [!UICONTROL Basic Settings]

*Solo grupos de anuncios nuevos*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign]:** La campaña. No puede cambiar la campaña después de crear el grupo de publicidad.

## Ficha [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Group name]:** Un nombre de grupo de anuncios que es único dentro de la campaña e incluye al menos tres caracteres.

**[!UICONTROL Status]:** El estado de visualización del grupo de publicidad: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. El valor predeterminado para los nuevos grupos de anuncios es *[!UICONTROL Active]*.

**[!UICONTROL Bid strategy]:** (Campañas con el objetivo [!UICONTROL Clicks] o [!UICONTROL Conversions]) Cómo pujar por anuncios en el grupo de anuncios:

* *[!UICONTROL Autobid]:* (El valor predeterminado para los nuevos grupos de anuncios) [!DNL OpenAI] ajusta automáticamente las ofertas para obtener la mayor cantidad de clics o conversiones, según el objetivo de la campaña, de tu presupuesto. No has introducido el importe de la puja. Esta opción está disponible tanto para los presupuestos de campaña diarios como de duración.

* *[!UICONTROL Target CPC]:* (Campañas con el objetivo [!UICONTROL Clicks]) Se ofrece hacia una meta de costo por clic promedio. Escriba el objetivo en el campo [!UICONTROL Target CPC].

* *[!UICONTROL Target CPA]:* (Campañas con el objetivo [!UICONTROL Conversions]) Se ofrece hacia un objetivo de costo promedio por conversión. Escriba el objetivo en el campo [!UICONTROL Target CPA].

* *[!UICONTROL Manual: Max bid]:* (solo para grupos de anuncios de ofertas manuales existentes) Mantiene la oferta máxima existente como una cantidad de solo lectura. Puede mantener esta estrategia o cambiar a [!UICONTROL Autobid] o a la estrategia de destino para el objetivo de la campaña. Esta opción no está disponible para grupos de anuncios nuevos ni cuando se editan grupos de anuncios que ya utilizan la oferta automática o de destino.

Los grupos de anuncios de oferta manual existentes no se cambian automáticamente a otra estrategia. Editar sólo una cantidad de destino o una configuración no relacionada no cambia una estrategia de oferta de destino existente.

**[!UICONTROL Target CPC]:** (Grupos de anuncios con la estrategia de oferta [!UICONTROL Target CPC]; obligatorio) El costo promedio por clic que desea lograr, en la moneda de la cuenta. Introduzca un importe positivo. Este es un objetivo de coste medio, no una oferta máxima.

**[!UICONTROL Target CPA]:** (Grupos de anuncios con la estrategia de oferta [!UICONTROL Target CPA]; obligatorio) El costo promedio por conversión que desea lograr, en la moneda de la cuenta. Introduzca un importe positivo. Este es un objetivo de coste medio, no una oferta máxima.

**[!UICONTROL Maximum CPC bid]:** (Campañas con el objetivo [!UICONTROL Clicks]; solo grupos de anuncios de oferta manual existentes; solo lectura) Cantidad máxima existente que pagarás por cada clic.

**[!UICONTROL Conversion-optimized bid cap]:** (Campañas con el objetivo [!UICONTROL Conversions]; solo grupos de anuncios de oferta manual existentes; solo lectura) Cantidad máxima existente que está dispuesto a pujar por una conversión. [!DNL OpenAI] utiliza la tasa de conversión predicha para convertir este valor en una oferta de subasta por impresión.

**[!UICONTROL Maximum CPM bid]:** (Campañas con el objetivo [!UICONTROL Reach]) La cantidad máxima que pagará por mil impresiones, en la moneda de la cuenta. Escriba un valor entre 0,01 y 5000. Las campañas de alcance no tienen las opciones de [!UICONTROL Bid strategy].

**[!UICONTROL Context hints (optional)]:** Descripción de las conversaciones, temas o palabras clave para los que sus productos o servicios pueden ser relevantes. Separe las sugerencias con comas o saltos de línea. Las sugerencias se pueden usar para guiar la coincidencia, pero no son reglas de segmentación de coincidencia exacta. Ver [[!DNL ChatGPT Ads] ayuda sobre cómo escribir sugerencias de contexto efectivas](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints).

**[!UICONTROL Landing Page Suffix]:** (Opcional) Cualquier parámetro que se anexe al final de las direcciones URL de la página de aterrizaje para rastrear la información. Ejemplo: `param1=value1&param2=value2`.

>[!MORELIKETHIS]
>
>* [Administrar grupos de anuncios](ad-group-manage.md)
