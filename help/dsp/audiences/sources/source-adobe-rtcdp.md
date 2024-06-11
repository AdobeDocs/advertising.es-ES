---
title: DSP Uso de la integración de con [!DNL Adobe] [!DNL Real-time CDP]
description: DSP Obtenga información sobre cómo habilitar la ingesta de datos en el sitio web de [!DNL Adobe] [!DNL Real-time CDP] segmentos de origen.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 33766fc210da032102bdc07a0db4ce348b12fe92
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Conversión de ID de usuario [!DNL Adobe Real-Time CDP] a los ID universales

*Función beta*

DSP Uso de la integración de la con [el [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=es), que forma parte de Adobe Experience Platform, para convertir las direcciones de correo electrónico con hash en ID universales para la publicidad de destino.

1. (Para convertir direcciones de correo electrónico en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurar el seguimiento de [!DNL Analytics] medición:

   1. (Si aún no lo ha hecho) Completar todo [requisitos previos para la implementación [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y el [ID de AMO e ID de EF en las URL de seguimiento](/help/integrations/analytics/ids.md).

   1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

      * **Para [!DNL RampIDs]:** Debe implementar una etiqueta JavaScript adicional en las páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) para las visualizaciones. Póngase en contacto con el equipo de cuenta de Adobe, que le dará instrucciones para registrarse en [!DNL LiveRamp] [!DNL LaunchPad] etiqueta desde [!DNL LiveRamp] Soluciones de tráfico de autenticación. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, el equipo de cuenta de Adobe generará y proporcionará una etiqueta única para que su organización la implemente en sus páginas web.

1. [Crear una fuente de audiencia](source-manage.md) DSP para importar audiencias a su cuenta de o a una cuenta de anunciante de. Puede elegir convertir los identificadores de usuario a cualquiera de los siguientes [formatos de ID universales disponibles](source-about.md).

   La configuración de origen incluye una clave de origen generada automáticamente que se utilizará en el siguiente paso.

1. En Adobe Experience Platform DSP, configure una conexión de destino de Advertising mediante el [!UICONTROL Source Key] DSP que se generó en la configuración de origen de la.

   DSP Para obtener instrucciones sobre cómo activar la conexión de destino de la, seleccionar segmentos y acceder a permisos de control, consulte &quot;[Conexión de Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   Las direcciones de correo electrónico de origen deben tener un cifrado hash con el algoritmo SHA-256.

1. Una vez completados todos los pasos, consulte en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia desde ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) que el segmento se está rellenando en un plazo de 24 horas. Compare el número de ID universales con el número de direcciones de correo electrónico con hash originales.

   La tasa de traducción de las direcciones de correo electrónico con hash a los ID universales debe ser superior al 90 %. Por ejemplo, si envía 100 direcciones de correo electrónico con hash desde la plataforma de datos del cliente, deben traducirse a más de 90 ID universales. Una tasa de traducción del 90 % o menos es un problema. Para obtener más información sobre cómo pueden variar los recuentos de segmentos, consulte[Causas de variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances).&quot;

   Para obtener ayuda sobre la resolución de problemas, póngase en contacto con su equipo de cuenta de Adobe o `adcloud-support@adobe.com`.

Los segmentos se actualizan cada 24 horas. Sin embargo, la inclusión en un segmento caduca pasados 30 días para garantizar el cumplimiento de la privacidad, por lo que debe actualizar las audiencias reinsertándolas desde Real-Time CDP cada 30 días o menos.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Resumen del catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Compatibilidad con la activación de ID universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
