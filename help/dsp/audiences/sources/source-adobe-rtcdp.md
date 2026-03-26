---
title: Usando la integración de DSP con  [!DNL Adobe] [!DNL Real-time CDP]
description: Aprenda a habilitar DSP para ingerir los segmentos de origen de  [!DNL Adobe] [!DNL Real-time CDP].
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 2dddf3560e1f98dab7158c28625bcd54b4efbdb2
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# Convertir ID de usuario de [!DNL Adobe Real-Time CDP] a ID universales

*característica de Beta*

Use la integración de DSP con [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=es), que forma parte de Adobe Experience Platform, para convertir sus identificadores de usuario (incluidas las direcciones de correo electrónico con hash, las cookies y los identificadores de publicidad móvil) en identificadores universales para publicidad de destino.

1. (Para convertir los identificadores de usuario en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurar el seguimiento para la medición de [!DNL Analytics]:

   1. (Si aún no lo ha hecho) Complete todos los [requisitos previos para implementar [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y el [ID de AMO e ID de EF en sus URL de seguimiento](/help/integrations/analytics/ids.md).

   1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

      * **Para [!DNL RampIDs]:** Debe implementar una etiqueta de JavaScript adicional en sus páginas web para que coincida con las conversiones de los identificadores en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones. Póngase en contacto con el equipo de su cuenta de Adobe, que le dará instrucciones para registrarse para una etiqueta [!DNL LiveRamp] [!DNL LaunchPad] desde [!DNL LiveRamp] soluciones de tráfico de autenticación. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, el equipo de cuenta de Adobe generará y proporcionará una etiqueta única para que su organización la implemente en sus páginas web.

1. [Cree una fuente de audiencia](source-manage.md) para importar audiencias a su cuenta de DSP o a una cuenta de anunciante. Puede elegir convertir sus identificadores de usuario a cualquiera de los [formatos de ID universales disponibles](source-about.md).

   La configuración de origen incluye una clave de origen generada automáticamente que se utilizará en el siguiente paso.

1. En Adobe Experience Platform, configure una conexión de destino de Advertising DSP con el [!UICONTROL Source Key] que se generó en la configuración de origen de DSP.

   Las direcciones de correo electrónico deben tener un cifrado hash con el algoritmo SHA-256.

   Para obtener instrucciones para activar la conexión de destino de DSP, activar audiencias y validar la exportación de datos, consulte &quot;[Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=es)&quot;.

   >[!NOTE]
   >
   >La conexión heredada, que solo admite direcciones de correo electrónico con hash, ahora se llama &quot;[Conexión heredada de DSP de Adobe Advertising Cloud](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection-legacy). Si ya utiliza la conexión heredada, no necesita realizar ningún cambio inmediatamente. Sin embargo, la conexión heredada se eliminará en algún momento.

1. Compruebe en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o en la configuración de ubicación) que el segmento se está rellenando y compare el número de ID universales con el número de ID de usuario originales.

   Los segmentos deberían estar disponibles en DSP en un plazo de 24 horas. Una vez que DSP recibe los datos del segmento, el recuento de público debe ser visible en un plazo de nueve (9) horas. Para obtener información sobre las tasas de traducción de ID aceptables y por qué los recuentos de segmentos pueden variar, consulte &quot;[Variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot;.

Los segmentos se actualizan cada 24 horas. Sin embargo, la inclusión en un segmento caduca después de 30 días de forma predeterminada o después de un periodo de caducidad especificado por el cliente. Actualice los segmentos volviendo a insertarlos desde Real-Time CDP antes de la caducidad. Para solicitar una caducidad de segmento personalizada, póngase en contacto con el equipo de cuenta de Adobe.

## Resolución de problemas

Para solucionar problemas de tasa de traducción y recuento de usuarios, consulte &quot;[Compatibilidad con la activación de los identificadores universales](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas con el procedimiento de conversión, póngase en contacto con el equipo de cuenta de Adobe o con `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar orígenes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=es)
>* Resumen del catálogo de destinos [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=es)
>* [Compatibilidad para activar identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
