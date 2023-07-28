---
title: '''[!DNL Google Ads] configuración del grupo de publicidad"'
description: Haga referencia a la configuración de [!DNL Google Ads] grupos de anuncios.
exl-id: 00aaa936-796f-4e22-9bee-4bb5121cd887
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] configuración del grupo de anuncios

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Un nombre de grupo de publicidad único dentro de la campaña. La longitud máxima es de 255 caracteres de doble byte.

**[!UICONTROL Status]:** El estado de visualización del grupo de anuncios: *Activo* o *Pausado*. El valor predeterminado para los nuevos grupos de anuncios es *Activo*.

**[!UICONTROL Ad Group Type]:** (Solo campañas de publicidad de búsqueda dinámica expandida) El tipo de grupo de anuncios:

* *[!UICONTROL Search Standard]* (valor predeterminado): Para anuncios estándar.

* *[!UICONTROL Search Dynamic]:* Para anuncios dinámicos de búsqueda.

**[!UICONTROL Ad Rotation Mode]:** Con qué frecuencia [!DNL Google Ads] envía los anuncios activos en relación con los demás dentro del grupo de anuncios:

* *[!UICONTROL Optimize]:* Google Ads prefiere los anuncios que espera que tengan un mejor rendimiento que otros anuncios del grupo de anuncios. Estos anuncios entran en la subasta de anuncios con más frecuencia y, con el tiempo, se favorece un solo anuncio. Esto puede no ser coherente con sus objetivos empresariales y de optimización.

* *[!UICONTROL Rotate forever]:*   Cada uno de los anuncios entra en la subasta de anuncios un número más par de veces, lo que permite a Search, Social y Commerce puntuar los anuncios no solo en la tasa de pulsaciones, sino también en las conversiones.

* *[!UICONTROL Use campaign setting]*(el valor predeterminado para los nuevos grupos de anuncios): Utiliza la configuración existente de rotación de anuncios en el nivel de campaña. **Nota:** La configuración de nivel de campaña no es visible en Buscar, Social y Comercio.

Si la campaña utiliza una estrategia de oferta de oferta inteligente (como [!UICONTROL Target CPA], [!UICONTROL Target ROAS], o [!UICONTROL Enhanced CPC]), entonces [!DNL Google Ads] establece automáticamente la opción en &quot;[!UICONTROL Optimize].&quot;

**[!UICONTROL Custom Bid Level]:** (Campañas dirigidas únicamente a la red de visualización) Cómo pujar: por *[!UICONTROL Ad Group]* (el valor predeterminado), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Intereses y remarketing en Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (sitio web), *[!UICONTROL Unknown]*, o *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Cuando pujes por palabra clave, crea plantillas de seguimiento en el nivel de palabra clave. Del mismo modo, cuando puje por ubicación, cree plantillas de seguimiento en el nivel de ubicación. Para todas las demás dimensiones, cree plantillas de seguimiento en el nivel de anuncio.
>* Al realizar ofertas por edad, sexo, interés y lista o vertical para campañas en portafolios, la capacidad de optimización no optimiza las ofertas para la dimensión. Además, toda la atribución se aplica al grupo de anuncios.
>* Los anuncios de la red de búsqueda siempre utilizan ofertas de palabras clave.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campañas con [!UICONTROL Target CPA] pujas; opcional) El coste por adquisición (CPA) objetivo para el grupo de anuncios. Este valor anula el objetivo de nivel de campaña.

**[!UICONTROL Target ROAS]:** (Campañas con [!UICONTROL Target ROAS] Pujas; opcional) El objetivo de retorno de la inversión en publicidad (ROAS) para el grupo de anuncios, como porcentaje. Este valor anula el objetivo de nivel de campaña.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campañas solo en la red de búsqueda, y las existentes, de solo lectura) [!DNL Gmail] campañas en la red de visualización) Si se desea:

* *[!UICONTROL Target and Bid]:* Para mostrar anuncios solo a usuarios asociados con audiencias de destino que también cumplan cualquier otro objetivo para el grupo de anuncios.

* *[!UICONTROL Bid Only]:* Para mostrar anuncios incluso a personas que no están asociadas con audiencias de destinatario, siempre y cuando satisfagan otros objetivos de nivel de grupo de anuncios. Sin embargo, puedes aumentar las probabilidades de que se muestren anuncios a audiencias específicas si estableces pujas más altas para esas audiencias.

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
