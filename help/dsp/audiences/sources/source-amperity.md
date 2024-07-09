---
title: Conversión de ID de usuario [!DNL Amperity] a los ID universales
description: DSP Obtenga información sobre cómo habilitar la ingesta de datos en el sitio web de [!DNL Amperity] segmentos de origen.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: ed74f3fa3d0036e0dc8a529b05452567527f68a1
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Conversión de ID de usuario [!DNL Amperity] a los ID universales

*Función Beta*

DSP Uso de la integración de la con [!DNL Amperity] plataforma de datos del cliente para convertir las direcciones de correo electrónico con hash de origen de su organización en ID universales para la publicidad de destino.

1. (Para convertir direcciones de correo electrónico en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure el seguimiento para habilitar [!DNL Analytics] medida](#analytics-tracking).

1. [DSP Creación de una fuente de audiencia en la](#source-create).

1. [Preparación y uso compartido de datos de asignación de segmentos](#map-data).

1. [Solicitud de una inserción de datos desde [!DNL Amperity] DSP a la](#push-data).

1. [Comparar el número de ID universales con el número de direcciones de correo electrónico con hash](#compare-id-count).

## Paso 1: Configurar el seguimiento para [!DNL Analytics] medida {#analytics-tracking}

*Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para convertir direcciones de correo electrónico a [!DNL RampIDs] o [!DNL ID5] ID., debe hacer lo siguiente:

1. (Si aún no lo ha hecho) Completar todo [requisitos previos para la implementación [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y asegúrese de que la variable [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se están rellenando en las direcciones URL de seguimiento.

1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

   * **Para [!DNL RampIDs]:** Debe implementar una etiqueta de JavaScript adicional en las páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) para las visualizaciones. Póngase en contacto con el equipo de cuenta de Adobe, que le dará instrucciones para registrarse en [!DNL LiveRamp] [!DNL LaunchPad] etiqueta desde [!DNL LiveRamp] Soluciones de tráfico de autenticación. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, el equipo de cuenta de Adobe generará y proporcionará una etiqueta única para que su organización la implemente en sus páginas web.

## DSP Paso 2: Creación de una fuente de audiencia en el {#source-create}

1. [Crear una fuente de audiencia](source-manage.md) DSP para importar audiencias a su cuenta de o a una cuenta de anunciante de. Puede elegir convertir los identificadores de usuario a cualquiera de los siguientes [formatos de ID universales disponibles](source-about.md).

   La configuración de origen incluirá una clave de origen generada automáticamente, que utilizará para insertar los datos del segmento.

1. Después de crear la fuente de audiencia, comparta la clave de código fuente con el [!DNL Amperity] usuario.

## Paso 3: Preparar y compartir datos de asignación de segmentos {#map-data}

El anunciante debe preparar y compartir datos de asignación de segmentos.

1. En [!DNL Amperity], agregue hash a los ID de correo electrónico de la audiencia con el algoritmo SHA-256.

1. El anunciante debe proporcionar datos de asignación de segmentos al equipo de cuenta de Adobe DSP para crear los segmentos en la cuenta de. Utilice los siguientes nombres y valores de columna en un archivo de valores separados por comas:

   * **Clave de segmento externo:** El [!DNL Amperity] clave de segmento asociada al segmento.

   * **Nombre del segmento:** El nombre del segmento.

   * **Descripción del segmento:** El propósito o la regla del segmento, o ambos.

   * **Identificador principal:** Mantener en blanco

   * **CPM de vídeo:** 0

   * **Mostrar CPM:** 0

   * **Ventana de segmentos:** El tiempo de vida del segmento.

## Paso 4: Solicitar una inserción de datos de [!DNL Amperity] DSP a la {#push-data}

1. DSP Una vez que el segmento se asigna dentro de los segmentos, el anunciante debe trabajar con su [!DNL Amperity] DSP para distribuir los datos del segmento a los usuarios de la aplicación de la.

1. El anunciante debe confirmar con el equipo de cuenta de Adobe que se han recibido los datos del segmento.

DSP Los segmentos deben estar disponibles en un plazo de 24 horas para su uso en el mercado de la. Verifique en su biblioteca de audiencias (que está disponible cuando crea o edita una audiencia desde [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) que el segmento está disponible y se está rellenando.

Los segmentos se actualizarán según la configuración del anunciante en [!DNL Amperity]. Independientemente de la frecuencia con la que se actualice el segmento, la inclusión en un segmento caduca después de 30 días de forma predeterminada o después de un periodo de caducidad especificado por el cliente. Actualice los segmentos volviendo a insertarlos desde [!DNL Amperity] antes de la caducidad. Para solicitar una caducidad de segmento personalizada, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 5: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

DSP Una vez que reciba los datos del segmento, el recuento de audiencias debería ser visible en un plazo de nueve (9) horas. En la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia desde [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) compare el número de ID universales con el número de direcciones de correo electrónico con hash originales.

La tasa de traducción de direcciones de correo electrónico con hash a ID universales debe ser superior al 90 %; la tasa de traducción para [!DNL RampIDs] en particular, debe ser del 95 % si todas las direcciones de correo electrónico con hash son únicas. Por ejemplo, si envía 100 direcciones de correo electrónico con hash desde la plataforma de datos del cliente, deben traducirse al menos a 95 [!DNL RampIDs] o más de 90 tipos de ID universales. Una tasa de traducción más baja es un problema. Para obtener más información sobre cómo pueden variar los recuentos de segmentos, consulte[Causas de variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances).&quot;

Para obtener ayuda sobre la resolución de problemas, póngase en contacto con su equipo de cuenta de Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Compatibilidad con la activación de ID universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
