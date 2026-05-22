---
title: Convertir ID de usuario de  [!DNL Amperity]  a ID universales
description: Aprenda a habilitar DSP para que ingrese sus  [!DNL Amperity] segmentos de origen.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
TQID: https://experienceleague.adobe.com/LOl3N6NB0alkOXiTNe7Xzj9mcVVfYxog3x-iIuVa82M
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 706
ht-degree: 0%

---

# Convertir ID de usuario de [!DNL Amperity] a ID universales

Utilice la integración de DSP con la plataforma de datos del cliente [!DNL Amperity] para convertir las direcciones de correo electrónico con hash de origen de su organización en ID universales para la publicidad de destino.

1. (Para convertir direcciones de correo electrónico en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure el seguimiento para habilitar [!DNL Analytics] la medición](#analytics-tracking).

1. [Crear un origen de audiencia en DSP](#source-create).

1. [Preparar y compartir datos de asignación de segmentos](#map-data).

1. [Solicitar inserción de datos de [!DNL Amperity] a DSP](#push-data).

1. [Compare el número de identificadores universales con el número de direcciones de correo electrónico con hash](#compare-id-count).

## Paso 1: Configurar el seguimiento para la medición de [!DNL Analytics] {#analytics-tracking}

*Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para convertir direcciones de correo electrónico a [!DNL RampIDs] o [!DNL ID5] ID, debe hacer lo siguiente:

1. (Si aún no lo ha hecho) Complete todos los [requisitos previos para implementar [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y asegúrese de que el [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se estén rellenando en las direcciones URL de seguimiento.

1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

   * **Para [!DNL RampIDs]:** Debe implementar una etiqueta de JavaScript adicional en sus páginas web para que coincida con las conversiones de los identificadores en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones. Póngase en contacto con el equipo de su cuenta de Adobe, que le dará instrucciones para registrarse para una etiqueta [!DNL LiveRamp] [!DNL LaunchPad] desde [!DNL LiveRamp] soluciones de tráfico de autenticación. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, el equipo de cuenta de Adobe generará y proporcionará una etiqueta única para que su organización la implemente en sus páginas web.

## Paso 2: Crear una fuente de audiencia en DSP {#source-create}

1. [Cree una fuente de audiencia](source-manage.md) para importar audiencias a su cuenta de DSP o a una cuenta de anunciante. Puede elegir convertir sus identificadores de usuario a cualquiera de los [formatos de ID universales disponibles](source-about.md).

   La configuración de origen incluirá una clave de origen generada automáticamente, que utilizará para insertar los datos del segmento.

1. Después de crear el origen de audiencia, comparta la clave de código fuente con el usuario [!DNL Amperity].

## Paso 3: Preparar y compartir datos de asignación de segmentos {#map-data}

El anunciante debe preparar y compartir datos de asignación de segmentos.

1. En [!DNL Amperity], hash de los ID de correo electrónico de la audiencia con el algoritmo SHA-256.

1. El anunciante debe proporcionar datos de asignación de segmentos al equipo de cuenta de Adobe para crear los segmentos en DSP. Utilice los siguientes nombres y valores de columna en un archivo de valores separados por comas:

   * **Clave de segmento externo:** Clave de segmento [!DNL Amperity] asociada al segmento.

   * **Nombre del segmento:** El nombre del segmento.

   * **Descripción del segmento:** El propósito o la regla del segmento, o ambos.

   * **Id. principal:** Mantener en blanco

   * **CPM de vídeo:** 0

   * **Mostrar CPM:** 0

   * **Ventana del segmento:** El tiempo de vida del segmento.

## Paso 4: Solicitar una inserción de datos de [!DNL Amperity] a DSP {#push-data}

1. Una vez asignado el segmento en DSP, el anunciante debe trabajar con su representante de [!DNL Amperity] para distribuir los datos del segmento a DSP.

1. El anunciante debe confirmar con el equipo de cuenta de Adobe que se han recibido los datos del segmento.

Los segmentos deberían estar disponibles en DSP en un plazo de 24 horas. Compruebe en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o en la configuración de ubicación) que el segmento está disponible y se está rellenando.

Los segmentos se actualizarán según la configuración del anunciante en [!DNL Amperity]. Independientemente de la frecuencia con la que se actualice el segmento, la inclusión en un segmento caduca después de 30 días de forma predeterminada o después de un periodo de caducidad especificado por el cliente. Actualice sus segmentos reinsertándolos desde [!DNL Amperity] antes de la caducidad. Para solicitar una caducidad de segmento personalizada, póngase en contacto con el equipo de cuenta de Adobe.

## Paso 5: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

Una vez que DSP recibe los datos del segmento, el recuento de público debe ser visible en un plazo de nueve (9) horas.

En su biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) compare el número de ID universales con el número de direcciones de correo electrónico con hash originales. Para obtener información sobre las tasas de traducción de ID aceptables y por qué los recuentos de segmentos pueden variar, consulte &quot;[Variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot;.

## Resolución de problemas

Para solucionar problemas de tasa de traducción y recuento de usuarios, consulte &quot;[Compatibilidad con la activación de los identificadores universales](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas con el procedimiento de conversión, póngase en contacto con el equipo de cuenta de Adobe o con `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar orígenes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Compatibilidad para activar identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
