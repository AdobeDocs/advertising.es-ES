---
title: Convertir los identificadores de usuario de  [!DNL Amperity]  a identificadores universales
description: DSP Obtenga información sobre cómo habilitar la ingesta de segmentos de origen de  [!DNL Amperity]  por parte de los usuarios.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Convertir los identificadores de usuario de [!DNL Amperity] a identificadores universales

*característica de Beta*

DSP Utilice la integración de la con la plataforma de datos del cliente [!DNL Amperity] para convertir las direcciones de correo electrónico con hash de origen de su organización en ID universales para la publicidad de destino.

1. (Para convertir direcciones de correo electrónico en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure el seguimiento para habilitar [!DNL Analytics] la medición](#analytics-tracking).

1. DSP [Crear un origen de audiencia en la dirección de correo electrónico ](#source-create).

1. [Preparar y compartir datos de asignación de segmentos](#map-data).

1. DSP [Solicitar inserción de datos de [!DNL Amperity] a](#push-data).

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

1. Después de crear el origen de audiencia, comparta la clave de código fuente con el usuario [!DNL Amperity].

## Paso 3: Preparar y compartir datos de asignación de segmentos {#map-data}

El anunciante debe preparar y compartir datos de asignación de segmentos.

1. En [!DNL Amperity], hash de los ID de correo electrónico de la audiencia con el algoritmo SHA-256.

1. El anunciante debe proporcionar datos de asignación de segmentos al equipo de cuenta de Adobe DSP para crear los segmentos en la cuenta de. Utilice los siguientes nombres y valores de columna en un archivo de valores separados por comas:

   * **Clave de segmento externo:** Clave de segmento [!DNL Amperity] asociada al segmento.

   * **Nombre del segmento:** El nombre del segmento.

   * **Descripción del segmento:** El propósito o la regla del segmento, o ambos.

   * **Id. principal:** Mantener en blanco

   * **CPM de vídeo:** 0

   * **Mostrar CPM:** 0

   * **Ventana del segmento:** El tiempo de vida del segmento.

## DSP Paso 4: Solicitar una inserción de datos de [!DNL Amperity] a la {#push-data}

1. DSP DSP Una vez que el segmento se haya asignado dentro de los segmentos, el anunciante debe trabajar con su representante de [!DNL Amperity] para distribuir los datos del segmento a los usuarios de la red de distribución de datos de segmentos de la red de área de datos.

1. El anunciante debe confirmar con el equipo de cuenta de Adobe que se han recibido los datos del segmento.

DSP Los segmentos deben estar disponibles en un plazo de 24 horas para su uso en el mercado de la. Compruebe en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o en la configuración de ubicación) que el segmento está disponible y se está rellenando.

Los segmentos se actualizarán según la configuración del anunciante en [!DNL Amperity]. Independientemente de la frecuencia con la que se actualice el segmento, la inclusión en un segmento caduca después de 30 días de forma predeterminada o después de un periodo de caducidad especificado por el cliente. Actualice sus segmentos reinsertándolos desde [!DNL Amperity] antes de la caducidad. Para solicitar una caducidad de segmento personalizada, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 5: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

DSP Una vez que reciba los datos del segmento, el recuento de audiencias debería ser visible en un plazo de nueve (9) horas.

En su biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) compare el número de ID universales con el número de direcciones de correo electrónico con hash originales. Para obtener información sobre las tasas de traducción de ID aceptables y por qué los recuentos de segmentos pueden variar, consulte &quot;[Variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot;.

## Resolución de problemas

Para solucionar problemas de tasa de traducción y recuento de usuarios, consulte &quot;[Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas con el procedimiento de conversión, póngase en contacto con el equipo de la cuenta de Adobe o con `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
