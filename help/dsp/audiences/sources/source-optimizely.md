---
title: Conversión de ID de usuario [!DNL Optimizely] a los ID universales
description: DSP Obtenga información sobre cómo habilitar la ingesta de datos en el sitio web de [!DNL Optimizely] segmentos de origen.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 31713da81bbb1eb840de0f8e0d40013b42cd3140
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Conversión de ID de usuario [!DNL Optimizely] a los ID universales

*Función Beta*

Utilice la integración DSP con la plataforma de datos del [!DNL Optimizely] cliente para convertir las direcciones de correo electrónico hash de origen de su organización en ID universales para publicidad segmentada.

1. (A convertir correo electrónico direcciones a [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure seguimiento para habilitar [!DNL Analytics] la medición](#analytics-tracking).

1. [Crear una fuente audiencia en DSP](#source-create).

1. [Prepare y envíe los datos](#push-data) segmento.

1. [Compare el número de ID universales con el número de direcciones](#compare-id-count) de correo electrónico con hash.

## Paso 1: Configuración de seguimiento para [!DNL Analytics] la medición {#analytics-tracking}

*Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para convertir direcciones de correo electrónico a [!DNL RampIDs] o [!DNL ID5] ID., debe hacer lo siguiente:

1. (Si aún no lo ha hecho) Completar todo [requisitos previos para la implementación [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y asegúrese de que la variable [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se están rellenando en las direcciones URL de seguimiento.

1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

   * **Para [!DNL RampIDs]:** Debe implementar una etiqueta de JavaScript adicional en las páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) para las visualizaciones. Póngase en contacto con su equipo de cuentas de Adobe Systems, que le dará instrucciones para registrarse en un [!DNL LiveRamp] [!DNL LaunchPad] etiqueta de [!DNL LiveRamp] Authentication Traffic Solutions. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, su equipo de cuentas de Adobe Systems generará y proporcionará un etiqueta único para que su organización lo implementar en sus páginas web.

## Paso 2: Crear una fuente audiencia en DSP {#source-create}

1. [Crear una fuente](source-manage.md) audiencia para importar audiencias a su DSP cuenta o a una anunciante cuenta. Puede elegir convertir sus identificadores usuario a cualquiera de los [formatos](source-about.md) de ID universales disponibles.

   La configuración de origen incluirá una clave de origen generada automáticamente, que usará para insertar los datos de segmento.

1. Después de crear la fuente de audiencia, comparta la clave de código fuente con el [!DNL Optimizely] usuario.

## Paso 3: Preparar e insertar los datos del segmento {#push-data}

El anunciante debe preparar y enviar los datos utilizando [!DNL Optimizely Data Platform]. Para cualquier pregunta sobre el proceso, póngase en contacto con su [!DNL Optimizely] representante.

1. En [!DNL Optimizely Data Platform], agregue hash a los ID de correo electrónico de la audiencia con el algoritmo SHA-256.

1. Seguir de [[!DNL Optimizely's] DSP instrucciones para insertar el segmento en el entorno de trabajo de la](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Incluya la siguiente información para habilitar la integración:

   * **Clave Origen:** Esta es la clave de origen creada en [el paso 2](#source-create).

   * **Code de cuenta:** Este es el Code alfanumérico DSP cuenta, que puede encontrar en DSP en [!UICONTROL Settings] > [!UICONTROL Account].

Los segmentos estarán disponibles en DSP en un plazo de 24 horas y se actualizarán según lo configurado para el anunciante. Independientemente de la frecuencia con la que se actualice el segmento, la inclusión en un segmento caduca después de 30 días de forma predeterminada o después de un período de vencimiento especificado por el cliente. Actualizar los segmentos volviéndolos a insertar desde antes de [!DNL Optimizely] la caducidad. Para solicitud la caducidad de una segmento personalizada, póngase en contacto con el equipo de Adobe Systems cuentas.

## Paso 4: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

Después de completar todos los pasos, compruebe en el biblioteca de audiencias (que está disponible al crear o editar un audiencia desde > [!UICONTROL All Audiences] o dentro de ubicación configuración) que el segmento está disponible y se está rellenando en un plazo de [!UICONTROL Audiences] 24 horas. Compare el número de ID universales con el número de direcciones de correo electrónico con hash originales.

La tasa de traducción de las direcciones de correo electrónico con hash a los ID universales debe ser superior al 90 %. Por ejemplo, si envía 100 direcciones de correo electrónico con hash desde la plataforma de datos del cliente, deben traducirse a más de 90 ID universales. Una tasa de traducción del 90 % o menos es un problema. Para obtener más información sobre cómo pueden variar los recuentos de segmentos, consulte[Causas de variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances).&quot;

Para obtener ayuda sobre la resolución de problemas, póngase en contacto con su equipo de cuenta de Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia propia](/help/dsp/audiences/sources/source-about.md)
>* [Administrar orígenes de audiencia para activar el Audiences de ID universal](source-manage.md)
>* [Compatibilidad con la activación de ID universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de la gestión de público](/help/dsp/audiences/audience-about.md)
