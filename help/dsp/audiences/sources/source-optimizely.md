---
title: Convertir los identificadores de usuario de  [!DNL Optimizely]  a identificadores universales
description: DSP Obtenga información sobre cómo habilitar la ingesta de segmentos de origen de  [!DNL Optimizely]  por parte de los usuarios.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Convertir los identificadores de usuario de [!DNL Optimizely] a identificadores universales

*característica de Beta*

DSP Utilice la integración de la con la plataforma de datos del cliente [!DNL Optimizely] para convertir las direcciones de correo electrónico con hash de origen de su organización en ID universales para la publicidad de destino.

1. (Para convertir direcciones de correo electrónico en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure el seguimiento para habilitar [!DNL Analytics] la medición](#analytics-tracking).

1. DSP [Crear un origen de audiencia en la dirección de correo electrónico &#x200B;](#source-create).

1. [Prepare e inserte los datos del segmento](#push-data).

1. [Compare el número de identificadores universales con el número de direcciones de correo electrónico con hash](#compare-id-count).

## Paso 1: Configurar el seguimiento para la medición de [!DNL Analytics] {#analytics-tracking}

*Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para convertir direcciones de correo electrónico a [!DNL RampIDs] o [!DNL ID5] ID, debe hacer lo siguiente:

1. (Si aún no lo ha hecho) Complete todos los [requisitos previos para implementar [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y asegúrese de que el [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se estén rellenando en las direcciones URL de seguimiento.

1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

   * **Para [!DNL RampIDs]:** Debe implementar una etiqueta de JavaScript adicional en sus páginas web para que coincida con las conversiones de los identificadores en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones. Póngase en contacto con el equipo de cuenta de Adobe, que le dará instrucciones para registrarse para una etiqueta [!DNL LiveRamp] [!DNL LaunchPad] desde [!DNL LiveRamp] soluciones de tráfico de autenticación. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, el equipo de cuenta de Adobe generará y proporcionará una etiqueta única para que su organización la implemente en sus páginas web.

## DSP Paso 2: Creación de una fuente de audiencia en el {#source-create}

1. DSP [Cree una fuente de audiencia](source-manage.md) para importar audiencias a su cuenta de o a una cuenta de anunciante. Puede elegir convertir sus identificadores de usuario a cualquiera de los [formatos de ID universales disponibles](source-about.md).

   La configuración de origen incluirá una clave de origen generada automáticamente, que utilizará para insertar los datos del segmento.

1. Después de crear el origen de audiencia, comparta la clave de código fuente con el usuario [!DNL Optimizely].

## Paso 3: Preparar e insertar los datos del segmento {#push-data}

El anunciante debe preparar e insertar los datos usando [!DNL Optimizely Data Platform]. Para cualquier pregunta sobre el proceso, comuníquese con el representante de [!DNL Optimizely].

1. En [!DNL Optimizely Data Platform], hash de los ID de correo electrónico de la audiencia con el algoritmo SHA-256.

1. DSP Siga las [[!DNL Optimizely's] instrucciones de para insertar el segmento en la dirección de correo electrónico &lbrace;100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000 &#x200B;](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads) Incluya la siguiente información para habilitar la integración:

   * **Clave de Source:** Esta es la clave de origen creada en [Paso 2](#source-create).

   * DSP DSP **Código de cuenta:** Este es el código de cuenta alfanumérico de la cuenta de la, que puede encontrar en la dirección de correo electrónico en [!UICONTROL Settings] > [!UICONTROL Account].

Los segmentos se actualizarán según la configuración del anunciante. Independientemente de la frecuencia con la que se actualice el segmento, la inclusión en un segmento caduca después de 30 días de forma predeterminada o después de un periodo de caducidad especificado por el cliente. Actualice sus segmentos reinsertándolos desde [!DNL Optimizely] antes de la caducidad. Para solicitar una caducidad de segmento personalizada, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 4: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

DSP Los segmentos deben estar disponibles en un plazo de 24 horas para su uso en el mercado de la. DSP Una vez que reciba los datos del segmento, el recuento de audiencias debería ser visible en un plazo de nueve (9) horas.

Compruebe en su biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o en la configuración de ubicación) que el segmento está disponible y se está rellenando, y compare el número de ID universales con el número de direcciones de correo electrónico con hash originales. Para obtener información sobre las tasas de traducción de ID aceptables y por qué los recuentos de segmentos pueden variar, consulte &quot;[Variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot;.

## Resolución de problemas

Para solucionar problemas de tasa de traducción y recuento de usuarios, consulte &quot;[Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas con el procedimiento de conversión, póngase en contacto con el equipo de la cuenta de Adobe o con `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
