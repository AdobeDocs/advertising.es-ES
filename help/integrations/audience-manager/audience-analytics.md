---
title: '''[!DNL Adobe] [!DNL Audience Analytics] para los clientes de publicidad de Adobe'
description: Aprenda a utilizar [!DNL Adobe] [!DNL Audience Analytics] para casos de uso de publicidad
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] para clientes de publicidad de Adobe

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) es una integración entre Adobe Audience Manager y Adobe Analytics que permite a los clientes de Audience Manager enviar segmentos a [!DNL Analytics] para obtener información detallada sobre la actividad del sitio.

Los clientes de Adobe Advertising pueden beneficiarse de [!DNL Audience Analytics]. La integración de le permite:

* Envío de datos de Adobe de publicidad directamente a [!DNL Analytics] para determinar el impacto de la actividad del canal superior en la actividad del sitio descendente.

* Determine los canales de marketing y los puntos de entrada del sitio a partir de los anuncios de exposición del canal superior.

* Capa de la integración con [!DNL Analytics for Advertising] para incorporar segmentos demográficos de terceros de [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) con [!DNL Analytics for Advertising] para obtener más información sobre los perfiles de usuario.

   [!DNL Audience Marketplace] proporciona acceso a fuentes de datos de terceros con modelos de suscripción &quot;Activation&quot;, que permiten a los compradores enviar datos a un destino. Si los datos se utilizan en un [!DNL Analytics] destino, no se aplican tarifas de activación.

* DSP (Anunciantes con Advertising) Añada segmentos de exposición adicionales para obtener perspectivas integrales de administración de recorridos.

   DSP Advertising puede enviar datos de exposición a Audience Manager como señales procesables mediante la implementación de píxeles de seguimiento de impresiones de Adobe Experience Platform o de Audience Manager. Reenvío de los mismos datos a [!DNL Analytics] activa el análisis de datos avanzado. Consulte &quot;[Descripción general de la integración de datos de Advertising Media de Adobe con Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obtener más información.

Para obtener más información acerca de [!DNL Audience Analytics], incluidos los requisitos previos y el flujo de trabajo, consulte &quot;[Introducción al Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Ejemplos de uso de [!DNL Audience Analytics] Datos con datos de publicidad de Adobe

A continuación se muestran ejemplos de cómo puede utilizar los datos combinados en [!DNL Analytics] [!DNL Analysis Workspace].

### Ver el impacto de la actividad de canal superior en la actividad descendente

Utilice segmentos de exposición del Audience Manager para ver el impacto de la actividad del sitio del canal superior en la actividad del sitio descendente. Incluya publicidad en Adobe o ID de macros de terceros en los píxeles de seguimiento para realizar un seguimiento del impacto a nivel detallado, desde el nivel de campaña hasta el nivel del sitio en el que estuvo expuesto el usuario.

Principales ventajas:

* Seguimiento de la exposición por tipo de canal/anuncio y uso [!DNL Audience Analytics] para determinar las tasas de entrada y la superposición con la siguiente fase del recorrido del cliente.

* Determine el impacto de la actividad del canal superior en la actividad del sitio descendente.

* Connect [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> y [!DNL Audience Analytics] datos <!-- (which includes the user's last exposure event) --> para determinar un recorrido holístico del sitio.

A continuación se muestran ejemplos de informes que puede crear en [!DNL Analysis Workspace].

![Ver el impacto de la actividad del canal superior en la actividad del sitio descendente](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Uso [!DNL Audience Analytics] Datos de segmentos de terceros para el análisis de perfiles de usuario

Utilice segmentos de Audience Manager de terceros para un análisis más completo de cómo los usuarios interactúan con el sitio. Puede utilizar la información para determinar nuevas audiencias de terceros para las que activar medios, en función de cómo se relacionan los perfiles de los segmentos de terceros con los indicadores de rendimiento clave para los sitios de campañas de medios.

>[!TIP]
> Usar el Audience Manager `Audiences ID` y `Audiences Name` dimensiones en [!DNL Analytics], como cualquier otra dimensión que [!DNL Analytics] recopila.

A continuación se muestran ejemplos de informes que puede crear en [!DNL Analysis Workspace].

![Uso de segmentos de terceros para enriquecer el análisis del perfil del usuario](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integraciones de Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

