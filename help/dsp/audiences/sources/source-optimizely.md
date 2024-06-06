---
title: Conversión de ID de usuario [!DNL Optimizely] a los ID universales
description: DSP Obtenga información sobre cómo habilitar la ingesta de datos en el sitio web de [!DNL Optimizely] segmentos de origen.
feature: DSP Audiences
source-git-commit: 729098f01fb9d076efb2b945be4011df9ab1c905
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Conversión de ID de usuario [!DNL Optimizely] a los ID universales

DSP Uso de la integración de la con [!DNL Optimizely] plataforma de datos del cliente para convertir las direcciones de correo electrónico con hash de origen de su organización en ID universales para la publicidad de destino.

1. (Para convertir direcciones de correo electrónico en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure el seguimiento para habilitar [!DNL Analytics] medida](#analytics-tracking).

1. [DSP Creación de una fuente de audiencia en la](#source-create).

1. [Preparar e insertar los datos del segmento en [!DNL Optimizely Data Platform]](#push-data).

1. [Comparar el número de ID universales con el número de direcciones de correo electrónico con hash](#compare-id-count).

DSP Los segmentos deben estar disponibles en el plazo de 24 horas y se actualizan cada 24 horas. **[¿Es cierto o hay expectativas diferentes para Optimizely?]**

## Paso 1: Configurar el seguimiento para [!DNL Analytics] medida {#analytics-tracking}

*Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para convertir direcciones de correo electrónico a [!DNL RampIDs] o [!DNL ID5] ID., debe hacer lo siguiente:

1. (Si aún no lo ha hecho) Completar todo [requisitos previos para la implementación [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y asegúrese de que la variable [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se están rellenando en las direcciones URL de seguimiento.

1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

   * **Para [!DNL RampIDs]:** Debe implementar una etiqueta JavaScript adicional en las páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) para las visualizaciones. Póngase en contacto con el equipo de cuenta de Adobe, que le dará instrucciones para registrarse en [!DNL LiveRamp] [!DNL LaunchPad] etiqueta desde [!DNL LiveRamp] Soluciones de tráfico de autenticación. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, el equipo de cuenta de Adobe generará y proporcionará una etiqueta única para que su organización la implemente en sus páginas web.

## DSP Paso 2: Creación de una fuente de audiencia en el {#source-create}

1. [Crear una fuente de audiencia](source-manage.md) DSP para importar audiencias a su cuenta de o a una cuenta de anunciante de. Puede elegir convertir los identificadores de usuario a cualquiera de los siguientes [formatos de ID universales disponibles](source-about.md).

   La configuración de origen incluirá una clave de origen generada automáticamente, que utilizará para insertar los datos del segmento.

1. Después de crear la fuente de audiencia, comparta la clave de código fuente con el [!DNL Optimizely] usuario.

## Paso 3: Preparar e insertar los datos del segmento {#push-data}

El anunciante debe preparar y enviar los datos en [!DNL Optimizely Data Platform].  **[¿Están utilizando la plataforma de datos optimizada?]**  <!-- Data Platform? -->

1. Use el hash de los ID de correo electrónico para la audiencia del anunciante mediante el algoritmo SHA-256.

1. DSP Inserte el segmento a la, incluidos los campos siguientes:

   **[¿Están utilizando los servicios web de la plataforma de datos, otro tipo de API o una interfaz de usuario? Añada un vínculo a las instrucciones. ¿Y dónde ingresarán estos campos?]**  <!-- Are they using the Data Platform web services or what? Add a link to instructions. And where will they input these fields?  -->

   * **Clave de origen:** Esta es la clave de origen creada en [Paso 2](#source-create).

   * **Código de cuenta:** DSP DSP Este es el código de cuenta alfanumérico de la cuenta de la, que puede encontrar en la dirección de correo electrónico de la dirección de correo electrónico, que se encuentra en la dirección de correo electrónico: [!UICONTROL Settings] > [!UICONTROL Account].

## Paso 4: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

Una vez completados todos los pasos, consulte en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia desde ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de colocación) que el segmento está disponible y se está rellenando en un plazo de 24 horas. Compare el número de ID universales con el número de direcciones de correo electrónico con hash originales.

La tasa de traducción de las direcciones de correo electrónico con hash a los ID universales debe ser superior al 90 %. Por ejemplo, si envía 100 direcciones de correo electrónico con hash desde la plataforma de datos del cliente, deben traducirse a más de 90 ID universales. Una tasa de traducción del 90 % o menos es un problema. Para obtener más información sobre cómo pueden variar los recuentos de segmentos, consulte[Causas de variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances).&quot;

Los segmentos se actualizan cada 24 horas. Sin embargo, la inclusión en un segmento caduca pasados 30 días para garantizar el cumplimiento de la privacidad, por lo que debe actualizar las audiencias reinsertándolas desde [!DNL Optimizely] cada 30 días o menos.

Para obtener ayuda sobre la resolución de problemas, póngase en contacto con su equipo de cuenta de Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Configuración de origen de audiencia](source-settings.md)
>* [Conversión de ID de usuario [!DNL Adobe Real-Time CDP] a los ID universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Conversión de ID de usuario [!DNL Tealium] a los ID universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
