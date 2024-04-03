---
title: '''[!DNL Microsoft® Advertising] configuración del grupo de publicidad"'
description: Haga referencia a la configuración de [!DNL Microsoft® Advertising] grupos de anuncios.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 29401370d18a5d1c7d5c28cb90a109ea5134ac00
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] configuración del grupo de anuncios

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Un nombre de grupo de publicidad único dentro de la campaña. La longitud máxima es de 128 caracteres.

**[!UICONTROL Status]:** El estado de visualización del grupo de anuncios: *Activo* o *Pausado*. El valor predeterminado para los nuevos grupos de anuncios es *Activo*.

**[!UICONTROL Ad Language]:** (Campañas de búsqueda) El idioma de destino de los anuncios.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Buscar anuncios) Cómo y dónde colocar los anuncios dentro del grupo de anuncios:

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! websites]* (el valor predeterminado): Para colocar ofertas de anuncios en la red de búsqueda.

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! syndicated search partners]:* Para realizar pujas por anuncios en sitios de socios sindicados.

* *[!UICONTROL Content network]:* Obsoleto

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Obsoleto

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Grupos de anuncios de audiencias) Si se desea:

* *[!UICONTROL Target and Bid]:* Para mostrar anuncios solo a usuarios asociados con audiencias de destino que también cumplan cualquier otro objetivo para el grupo de anuncios.

* *[!UICONTROL Bid Only]:* Para mostrar anuncios incluso a personas que no están asociadas con audiencias de destinatario, siempre y cuando satisfagan otros objetivos de nivel de grupo de anuncios. Sin embargo, puedes aumentar las probabilidades de que se muestren anuncios a audiencias específicas si estableces pujas más altas para esas audiencias.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Para [!DNL Microsoft® Advertising] grupos de anuncios en la red de audiencias, los modificadores de oferta para los destinos de ubicación no están optimizados en los portafolios estándar con la etiqueta &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Audiencia y grupos; opcional) Sexos específicos que se deben incluir o excluir como destinatarios: *[!UICONTROL Male]*, *[!UICONTROL Female]*, y *[!UICONTROL Unknown]*. De forma predeterminada, todos los géneros son objetivos. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic en el círculo que hay junto a él una vez para que aparezca una marca de verificación azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) aparece. Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada sexo objetivo.

* Para excluir un valor, haga clic dos veces en el círculo que aparece junto a él, de modo que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) aparece.

**[!UICONTROL Age]:** (Audiencia y grupos; opcional) Categorías de edad específicas que se deben incluir o excluir como objetivos: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*, y *[!UICONTROL Unknown]*. De forma predeterminada, todas las páginas están segmentadas. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic en el círculo que hay junto a él una vez para que aparezca una marca de verificación azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) aparece. Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada página de destino.

* Para excluir un valor, haga clic dos veces en el círculo que aparece junto a él, de modo que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) aparece.

**[!UICONTROL Industry]:** (Grupos de anuncios de audiencia; opcional) Industrias específicas que se deben incluir o excluir como objetivos. De forma predeterminada, todas las industrias están segmentadas. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic en el círculo que hay junto a él una vez para que aparezca una marca de verificación azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) aparece. Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada sector de destino.

* Para excluir un valor, haga clic dos veces en el círculo que aparece junto a él, de modo que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) aparece.

**[!UICONTROL Job Function Targets]:** (Audiencia y grupos; opcional) Funciones de trabajo específicas que se deben incluir o excluir como destinatarios. De forma predeterminada, todas las funciones de trabajo están segmentadas. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic en el círculo que hay junto a él una vez para que aparezca una marca de verificación azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) aparece. Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada función de trabajo de destino.

* Para excluir un valor, haga clic dos veces en el círculo que aparece junto a él, de modo que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) aparece.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Opcional) El número de veces que se mostrarán anuncios a un cliente desde el grupo de anuncios. Introduzca un valor y seleccione la unidad de tiempo (*[!UICONTROL Hour]*, *[!UICONTROL Day]*, o *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campañas solo en la red de visualización/nativa; opcional) Sitios en la red de visualización en los que no desea que se muestren los anuncios. Introduzca una URL válida, como www.example.com. Para especificar varias cadenas, sepárelas con comas o introdúzcalas en líneas independientes.

Para obtener más información sobre disponibilidad, consulte [!DNL Microsoft® Advertising] ayuda para &quot;[Impedir que aparezcan anuncios en sitios web específicos](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Administrar grupos de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
