---
title: '[!DNL Microsoft Advertising] configuración del grupo de anuncios'
description: Hacer referencia a la configuración de  [!DNL Microsoft Advertising] grupos de anuncios.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/f-mac9RGzF4qVr7P65-9AuhWKf22tdND5XSJ1YvLWyc
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b7a1ae8b58c7c4f699bc007473cef80ef2e3aa53
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configuración del grupo de anuncios

## \[Parte superior de la página]

**[!UICONTROL Ad Group Name]:** Un nombre de grupo de publicidad que es único dentro de la campaña.

**[!UICONTROL Status]:** El estado de visualización de la campaña: *Activo* o *En pausa*. El valor predeterminado para las nuevas campañas de publicidad es *Activo*.

## Ficha [!UICONTROL Basic Settings]

*Solo nuevas campañas*

**[!UICONTROL Network]:** La red publicitaria.

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign]:** La campaña.

## Ficha [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Language]:** (Campañas de búsqueda) El idioma de destino para los anuncios.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## Ficha [!UICONTROL Networks]

**[!UICONTROL Networks]:** (anuncios de búsqueda) Cómo y dónde colocar los anuncios dentro del grupo de anuncios:

* *[!UICONTROL Only Bing and Yahoo websites]* (predeterminado): para colocar ofertas de anuncios en la red de búsqueda.

* *[!UICONTROL Only Bing and Yahoo syndicated search partners]:* Para hacer pujas por anuncios en sitios de socios sindicados.

* *[!UICONTROL Content Network]:* obsoleto

## Ficha [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** obsoleto

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Grupos de anuncios de audiencia) Ya sea para:

* *[!UICONTROL Bid Only]:* Para mostrar anuncios incluso a personas que no están asociadas con audiencias de destino siempre y cuando satisfagan otros objetivos de nivel de grupo de anuncios. Sin embargo, puedes aumentar las probabilidades de que se muestren anuncios a audiencias específicas si estableces pujas más altas para esas audiencias.

* *[!UICONTROL Target and Bid]:* Para mostrar anuncios solamente a usuarios asociados con audiencias de destino que también cumplan cualquier otro objetivo para el grupo de anuncios.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Para [!DNL Microsoft Advertising] grupos de anuncios en la red de audiencias, los modificadores de oferta para los destinos de ubicación no están optimizados en portafolios estándar con la configuración &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

**[!UICONTROL Genre]:** (Grupos de anuncios en [!UICONTROL Audience CTV Video] campañas; disponibles en EE. UU., CA, BR, MX, Reino Unido, DE, ES, FR, IT, AU, MY y TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) Los géneros de destino, que determinan los programas y canales en los que aparecen los anuncios:

* *[!UICONTROL All genres]:* (El valor predeterminado) se dirige a todos los géneros.

* *[!UICONTROL Select From Below List]:* Segmenta los géneros seleccionados. Seleccione de la lista de todos los géneros disponibles.

La colocación de anuncios de TV conectada (CTV) depende de la calidad del vídeo y del importe de la oferta. Consulte los [requisitos técnicos para anuncios de CTV](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (opcional) géneros específicos para incluir o excluir como destinos: *[!UICONTROL Male]*, *[!UICONTROL Female]* y *[!UICONTROL Unknown]*. De forma predeterminada, todos los géneros son objetivos. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic una vez en el círculo adyacente para que aparezca una marca de verificación azul (![Include](/help/search-social-commerce/assets/include.png "Include")). Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada sexo objetivo.

* Para excluir un valor, haga clic dos veces en el círculo adyacente para que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")).

**[!UICONTROL Age]:** (Opcional) Categorías de edad específicas que se deben incluir o excluir como destinos: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* y *[!UICONTROL Unknown]*. De forma predeterminada, todas las páginas están segmentadas. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic una vez en el círculo adyacente para que aparezca una marca de verificación azul (![Include](/help/search-social-commerce/assets/include.png "Include")). Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada página de destino.

* Para excluir un valor, haga clic dos veces en el círculo adyacente para que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")).

**[!UICONTROL Company targets]:** (Opcional) Compañías específicas de los perfiles del usuario [!DNL LinkedIn] que se incluirán o excluirán como destinos. De forma predeterminada, se segmentan todas las compañías. Para reducir los objetivos, busque y seleccione empresas individuales y organizaciones de nivel medio. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic una vez en el círculo adyacente para que aparezca una marca de verificación azul (![Include](/help/search-social-commerce/assets/include.png "Include")). Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada empresa objetivo.

* Para excluir un valor, haga clic dos veces en el círculo adyacente para que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")).

**[!UICONTROL Industry]:** (Opcional) Industrias específicas de los perfiles del usuario [!DNL LinkedIn] que se incluirán o excluirán como destinos. De forma predeterminada, todas las industrias están segmentadas. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic una vez en el círculo adyacente para que aparezca una marca de verificación azul (![Include](/help/search-social-commerce/assets/include.png "Include")). Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada sector de destino.

* Para excluir un valor, haga clic dos veces en el círculo adyacente para que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")).

**[!UICONTROL Job Function Targets]:** (Opcional) Funciones de trabajo específicas de los perfiles del usuario [!DNL LinkedIn] que se van a incluir o excluir como destinos. De forma predeterminada, todas las funciones de trabajo están segmentadas. Las exclusiones siempre anulan las inclusiones.

* Para dirigirse a todos los valores, no seleccione ningún valor.

* Para incluir un valor, haga clic una vez en el círculo adyacente para que aparezca una marca de verificación azul (![Include](/help/search-social-commerce/assets/include.png "Include")). Si lo desea, puede aumentar o reducir las ofertas en un porcentaje especificado para cada función de trabajo de destino.

* Para excluir un valor, haga clic dos veces en el círculo adyacente para que aparezca una marca de verificación roja (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")).

## Ficha [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## Ficha [!UICONTROL Additional Ad Group Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

### [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (solo campañas en la red nativa/de visualización; opcional) Sitios en la red de visualización en los que no desea que se muestren los anuncios. Introduzca una URL válida, como www.example.com. Para especificar varias cadenas, sepárelas con comas o introdúzcalas en líneas independientes.

Para obtener información acerca de la disponibilidad, consulte la ayuda de [!DNL Microsoft Advertising] para &quot;[Impedir que aparezcan anuncios en sitios web específicos](https://help.ads.microsoft.com/#apex/bae/en/14061/0)&quot;.

### [!UICONTROL Ad Group Frequency Cap Settings]

(Opcional) El número de veces que se puede mostrar anuncios a un cliente desde el grupo de anuncios. Escriba un valor y seleccione la unidad de tiempo (*[!UICONTROL Hour]*, *[!UICONTROL Day]*, *[!UICONTROL Week]*) o *[!UICONTROL Month]*).

>[!MORELIKETHIS]
>
>* [Administrar grupos de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
