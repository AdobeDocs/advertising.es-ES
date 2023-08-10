---
title: Implementación [!DNL Google Ads] anuncios dinámicos de búsqueda
description: Obtenga información sobre el flujo de trabajo para configurar [!DNL Google Ads] anuncios dinámicos de búsqueda.
exl-id: 4c806824-b582-46dc-8d88-85c73bfb0944
feature: Search Campaign Management
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Implementación [!DNL Google Ads] anuncios dinámicos de búsqueda

*[!DNL Google Ads]campañas solo de búsqueda con seguimiento a nivel creativo o de palabras clave y nivel creativo únicamente*

Los anuncios dinámicos de búsqueda utilizan contenido del sitio web, en lugar de palabras clave, para decidir cuándo mostrar los anuncios. Puede definir las páginas de los sitios web cuyo contenido se utiliza para segmentar los anuncios dinámicos de búsqueda configurando objetivos de búsqueda dinámicos independientes para el grupo de anuncios o eligiendo una configuración de nivel de campaña para segmentar los anuncios mediante el contenido del sitio web.

Puede configurar anuncios dinámicos de búsqueda ya sea de forma individual o mediante hojas de edición por lotes. Las siguientes instrucciones incluyen vínculos para crear entidades individuales.

## Pasos para la configuración [!DNL Google Ads] anuncios dinámicos de búsqueda

1. [Creación de una campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para anuncios dinámicos de búsqueda:

   1. Establezca inicialmente el presupuesto de la campaña en el 10 % de su gasto diario en campañas de búsqueda.

      Más tarde, puede aumentar el presupuesto después de que los anuncios demuestren su valor.

   1. (Si lo desea [!DNL Google Ads] para mostrar los anuncios dinámicos de búsqueda (según el contenido del sitio web) Especifique el dominio raíz y el idioma del dominio en la variable [!UICONTROL DSA Options] de la configuración de la campaña.

      >[!NOTE]
      >
      >Su dominio debe estar indexado por la variable [!DNL Google Ads] índice de búsqueda orgánica que se va a segmentar. Además, si el dominio contiene páginas en varios idiomas y desea segmentarlas todas, cree una campaña independiente para cada idioma.

      Si no utiliza el dominio del sitio web para segmentar los anuncios, cree objetivos de búsqueda dinámica (consulte el paso 4) para cada grupo de anuncios. Puede crear los objetivos [individualmente](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) o usando [hojas a granel](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Asegúrese de que la campaña se dirige al canal de búsqueda y solo al [!DNL Google Ads] red de búsqueda (no la red de visualización). Esta configuración está disponible en [!UICONTROL Networks and Devices] pestaña.

   1. (Opcional) Excluir palabras clave en [!UICONTROL Negatives] pestaña.

   1. (Opcional) Configure una plantilla de seguimiento de nivel de campaña, que anula la plantilla de seguimiento de nivel de cuenta, pero que se puede sobrescribir en los niveles inferiores.

      (Anunciantes con Adobe Analytics sin seguimiento del lado del servidor) Si desea incluir el seguimiento de la fuente inversa de Search, Social y Commerce en Analytics, agregue el código de seguimiento de ID de AMO a los parámetros de datos anexados del nivel de la cuenta, que agregan el código a la dirección URL final. Consulte &quot;[El parámetro de seguimiento de ID de AMO](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md).&quot;

1. [Crear un grupo de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dentro de la campaña, incluidos los pasos siguientes:

   1. Configure las variables [!UICONTROL Ad Group Type] hasta **[!UICONTROL Search Dynamic].**

   1. Establece la oferta predeterminada para todos los anuncios.

      Si se configuran, se puede anular la oferta predeterminada para destinos de búsqueda dinámica concretos.

   1. (Opcional) Configure una plantilla de seguimiento de nivel de grupo de anuncios, que anula todas las plantillas de seguimiento en niveles superiores, pero que se puede sobrescribir en el nivel de anuncio.

      Si ha añadido el seguimiento de Adobe Analytics en el nivel de campaña y desea incluirlo para el grupo de publicidad, agréguelo aquí. Consulte el paso 1e.

1. [Crear cada anuncio de búsqueda dinámica](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) dentro del grupo de anuncios.

   [!DNL Google Ads] genera dinámicamente el titular, la dirección URL de visualización y la dirección URL de la página de aterrizaje para cada anuncio. Si lo desea, puede agregar redirecciones y seguimiento a la plantilla de seguimiento de nivel de anuncio, que anula las plantillas de seguimiento en niveles superiores.
Si desea anular cualquier seguimiento de Adobe Analytics en niveles superiores con seguimiento de nivel de anuncio, agréguelo aquí. Véanse los pasos 1e y 2c.

1. (Necesario cuando no se incluyen el dominio raíz y el idioma para el dominio en la sección Opciones de DSA de la configuración de campaña; opcional en caso contrario) Crear [destinos de búsqueda dinámica](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) para el grupo de publicidad. Si lo desea, puede anular la oferta en el nivel de grupo de anuncios con ofertas en el nivel de destino.

   Los objetivos definen si la red de anuncios utiliza todas las páginas del sitio web o un subconjunto de ellas para segmentar los anuncios dinámicos de búsqueda. Para realizar el mejor seguimiento del rendimiento, configure la campaña con un grupo de anuncios por cada destino de búsqueda dinámica e incluya un grupo de anuncios que se ajuste a todos los criterios.

1. Si es necesario, [edición de la configuración de campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar el presupuesto de la campaña y restringir el tráfico excluyendo palabras clave adicionales de la campaña.
