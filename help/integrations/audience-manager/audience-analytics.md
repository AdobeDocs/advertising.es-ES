---
title: '[!DNL Adobe] [!DNL Audience Analytics] para clientes de Adobe Advertising'
description: Aprenda a utilizar [!DNL Adobe] [!DNL Audience Analytics] para casos de uso de publicidad
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] para clientes de Adobe Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=es) es una integración entre Adobe Audience Manager y Adobe Analytics que permite a los clientes Audience Manager enviar segmentos a [!DNL Analytics] para obtener información detallada sobre la actividad del sitio.

Los clientes de Adobe Advertising pueden beneficiarse al usar [!DNL Audience Analytics]. La integración de le permite:

* Envíe datos de exposición de Adobes Advertising directamente a [!DNL Analytics] para determinar el impacto de la actividad del canal superior en la actividad del sitio descendente.

* Determine los canales de marketing y los puntos de entrada del sitio a partir de los anuncios de exposición del canal superior.

* Clasifique la integración con [!DNL Analytics for Advertising] para incorporar segmentos demográficos de terceros del [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html?lang=es) con datos de [!DNL Analytics for Advertising] para obtener más información sobre los perfiles de usuario.

  [!DNL Audience Marketplace] proporciona acceso a fuentes de datos de terceros con modelos de suscripción de &quot;Activación&quot;, que permiten a los compradores enviar datos a un destino. Si los datos se usan en un destino de [!DNL Analytics], no se aplican tarifas de activación.

* (Anunciantes con Advertising DSP) Agregue segmentos de exposición adicionales para obtener perspectivas integrales de administración de recorridos.

  Advertising DSP puede enviar datos de exposición a Audience Manager como señales procesables mediante la implementación de píxeles de seguimiento de impresiones de Adobe Experience Platform o de Audience Manager. Al reenviar los mismos datos a [!DNL Analytics], se habilita el análisis de datos avanzado. Consulte &quot;[Información general sobre la integración de datos de Adobe Advertising Media con Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obtener más información.

Para obtener más información acerca de [!DNL Audience Analytics], incluidos los requisitos previos y el flujo de trabajo, consulte &quot;[descripción general del Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=es)&quot;.

## Ejemplos de cómo usar datos de [!DNL Audience Analytics] con datos de Adobe Advertising

Los siguientes son ejemplos de cómo puede utilizar los datos combinados en [!DNL Analytics] [!DNL Analysis Workspace].

### Ver el impacto de la actividad de canal superior en la actividad descendente

Utilice segmentos de exposición del Audience Manager para ver el impacto de la actividad del sitio del canal superior en la actividad del sitio descendente. Incluya ID de macros de Adobe Advertising o de terceros en los píxeles de seguimiento para realizar un seguimiento del impacto a nivel detallado, desde el nivel de campaña hasta el nivel del sitio en el que estuvo expuesto el usuario.

Principales ventajas:

* Rastree la exposición por tipos de embudo/publicidad y use [!DNL Audience Analytics] para determinar las tasas de entrada y la superposición con la siguiente fase del recorrido del cliente.

* Determine el impacto de la actividad del canal superior en la actividad del sitio descendente.

* Conecte [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> y [!DNL Audience Analytics] datos <!-- (which includes the user's last exposure event) --> para determinar un recorrido holístico al sitio.

Los siguientes son ejemplos de informes que puede crear en [!DNL Analysis Workspace].

![Ver el impacto de la actividad del canal superior en la actividad del sitio descendente](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Usar [!DNL Audience Analytics] datos de segmentos de terceros para el análisis de perfiles de usuario

Utilice segmentos de Audience Manager de terceros para un análisis más completo de cómo los usuarios interactúan con el sitio. Puede utilizar la información para determinar nuevas audiencias de terceros para las que activar medios, en función de cómo se relacionan los perfiles de los segmentos de terceros con los indicadores de rendimiento clave para los sitios de campañas de medios.

>[!TIP]
> Utilice las dimensiones del Audience Manager `Audiences ID` y `Audiences Name` en [!DNL Analytics], como cualquier otra dimensión que [!DNL Analytics] recopile.

Los siguientes son ejemplos de informes que puede crear en [!DNL Analysis Workspace].

![Uso de segmentos de terceros para enriquecer el análisis del perfil de usuario](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integraciones de Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
