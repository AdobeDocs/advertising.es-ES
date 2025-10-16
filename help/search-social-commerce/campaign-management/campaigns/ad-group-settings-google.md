---
title: '[!DNL Google Ads] configuración del grupo de anuncios'
description: Hacer referencia a la configuración de  [!DNL Google Ads] grupos de anuncios.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: 345c2af5363ca10412f3809700e281af5b06897f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# [!DNL Google Ads] configuración del grupo de anuncios

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Un nombre de grupo de anuncios que es único dentro de la campaña. La longitud máxima es de 255 caracteres de doble byte.

**[!UICONTROL Status]:** El estado de visualización del grupo de anuncios: *Activo* o *En pausa*. El valor predeterminado para los nuevos grupos de anuncios es *Activo*.

**[!UICONTROL Ad Group Type]:** (Solo campañas de anuncios dinámicos de búsqueda expandida) El tipo de grupo de anuncios:

* *[!UICONTROL Search Standard]* (valor predeterminado): para anuncios estándar.

* *[!UICONTROL Search Dynamic]:* para anuncios dinámicos de búsqueda.

**[!UICONTROL Ad Rotation Mode]:** Con qué frecuencia [!DNL Google Ads] entrega sus anuncios activos entre sí dentro del grupo de anuncios:

* *[!UICONTROL Optimize]:* Google Ads prefiere los anuncios que espera que tengan un mejor rendimiento que otros anuncios del grupo de anuncios. Estos anuncios entran en la subasta de anuncios con más frecuencia y, con el tiempo, se favorece un solo anuncio. Esto puede no ser coherente con sus objetivos empresariales y de optimización.

* *[!UICONTROL Rotate forever]:*   Cada uno de los anuncios entra en la subasta de anuncios un número más par de veces, lo que permite a Search, Social y Commerce puntuar sus anuncios no solo en la tasa de pulsaciones, sino también en las conversiones.

* *[!UICONTROL Use campaign setting]* (el valor predeterminado para los nuevos grupos de anuncios): utiliza la configuración de rotación de anuncios de nivel de campaña existente. **Nota:** La configuración de nivel de campaña no es visible en Search, Social y Commerce.

Si la campaña usa una estrategia de oferta de oferta inteligente (como [!UICONTROL Target CPA], [!UICONTROL Target ROAS], [!DNL Google Ads] establece automáticamente la opción en &quot;[!UICONTROL Optimize]&quot;.

**[!UICONTROL Custom Bid Level]:** (Campañas dirigidas solo a la red de visualización) Cómo pujar: por *[!UICONTROL Ad Group]* (predeterminado), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Intereses y remarketing en Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (sitio web), *[!UICONTROL Unknown]* o *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Cuando pujes por palabra clave, crea plantillas de seguimiento en el nivel de palabra clave. Del mismo modo, cuando puje por ubicación, cree plantillas de seguimiento en el nivel de ubicación. Para todas las demás dimensiones, cree plantillas de seguimiento en el nivel de anuncio.
>* Al realizar ofertas por edad, sexo, interés y lista o vertical para campañas en portafolios, la capacidad de optimización no optimiza las ofertas para la dimensión. Además, toda la atribución se aplica al grupo de anuncios.
>* Los anuncios de la red de búsqueda siempre utilizan ofertas de palabras clave.

**[!UICONTROL AI Max Search Term Matching]:** (Campañas dirigidas a la red de búsqueda para las que la característica [AI Max](https://support.google.com/google-ads/answer/15910366) y la característica de coincidencia de términos de búsqueda de nivel de campaña están habilitadas; solo lectura) Indica si la coincidencia de términos de búsqueda de nivel de grupo de anuncios está habilitada: *[!UICONTROL Disabled]* o *[!UICONTROL Enabled]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campañas con ofertas de [!UICONTROL Target CPA]; opcional) El costo por adquisición (CPA) objetivo para el grupo de anuncios. Este valor anula el objetivo de nivel de campaña.

**[!UICONTROL Target ROAS]:** (Campañas con ofertas de [!UICONTROL Target ROAS]; opcional) El objetivo de retorno de la inversión en publicidad (ROAS) para el grupo de anuncios, como porcentaje. Este valor anula el objetivo de nivel de campaña.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campañas solo en la red de búsqueda y las campañas existentes de solo lectura de [!DNL Gmail] en la red de visualización) Si se desea:

* *[!UICONTROL Target and Bid]:* Para mostrar anuncios solamente a usuarios asociados con audiencias de destino que también cumplan cualquier otro objetivo para el grupo de anuncios.

* *[!UICONTROL Bid Only]:* Para mostrar anuncios incluso a personas que no están asociadas con audiencias de destino siempre y cuando satisfagan otros objetivos de nivel de grupo de anuncios. Sin embargo, puedes aumentar las probabilidades de que se muestren anuncios a audiencias específicas si estableces pujas más altas para esas audiencias.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Administrar grupos de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
