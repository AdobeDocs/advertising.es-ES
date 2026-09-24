---
title: '[!DNL ChatGPT Ads] configuración de campaña'
description: Hacer referencia a la configuración de [!DNL ChatGPT Ads] campañas.
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
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ca0ab7d593ba6e66f34ba2d9ae3bf56d71e06dff
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%
---
# [!DNL ChatGPT Ads] configuración de campaña

*Los anuncios de [!DNL ChatGPT] son una característica piloto de[!DNL OpenAI]*

## Ficha [!UICONTROL Basic Settings]

*Solo nuevas campañas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign Type]:** Dónde colocar anuncios: la única opción es *[!UICONTROL Standard]* para mostrar anuncios en [!DNL ChatGPT].

## Ficha [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Un nombre de campaña único en la cuenta.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *En pausa*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

**[!UICONTROL Objective]:** El objetivo de la campaña: *Alcanzar* o *Clics*.

**[!UICONTROL Location Targets]:** Ubicaciones geográficas de usuario admitidas para incluir como destinos. De forma predeterminada, todas las ubicaciones admitidas están segmentadas. Puede reducir los objetivos para incluir (pero no excluir) usuarios en cualquier combinación de ubicaciones.

* Para segmentar todas las ubicaciones, no seleccione ninguna ubicación.

* Para incluir una ubicación y sus ubicaciones secundarias, haga clic en el círculo adyacente.

* Para expandir una ubicación en sus subcomponentes (como regiones, territorios o ciudades), haga clic en el nombre de la ubicación.

* Para buscar una ubicación, introduzca o pegue al menos los tres primeros caracteres de la ubicación en el campo de entrada.

**[!UICONTROL Budget Type]:** Tipo de presupuesto de campaña: *Presupuesto diario* o *Duración*. No puede cambiar el tipo de presupuesto después de guardar la campaña.

**[!UICONTROL Budget]:** El presupuesto para el tipo de campaña especificado.

**[!UICONTROL Conversion events]:** (opcional) cualquier evento de conversión existente que se asocie a la campaña. **Nota:** Los datos de rendimiento para las conversiones rastreadas de [!DNL OpenAI] no están disponibles en Search, Social y Commerce. Supervise las conversiones rastreadas por [!DNL OpenAI] en [!DNL ChatGPT Ads Manager].

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

>[!MORELIKETHIS]
>
>* [Administrar campañas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
