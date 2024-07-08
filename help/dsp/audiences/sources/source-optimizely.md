---
title: Convert User IDs from [!DNL Optimizely] to Universal IDs
description: Learn how to enable DSP to ingest your [!DNL Optimizely] first-party segments.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# Convert User IDs from [!DNL Optimizely] to Universal IDs

*Función beta*

Utilice la integración DSP con la plataforma de datos del [!DNL Optimizely] cliente para convertir las direcciones de correo electrónico hash de origen de su organización en ID universales para publicidad segmentada.

1. (A convertir correo electrónico direcciones a [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure seguimiento para habilitar [!DNL Analytics] la medición](#analytics-tracking).

1. [Crear una fuente audiencia en DSP](#source-create).

1. [Prepare y envíe los datos](#push-data) segmento.

1. [Compare el número de ID universales con el número de direcciones](#compare-id-count) de correo electrónico con hash.

## Paso 1: Configuración de seguimiento para [!DNL Analytics] la medición {#analytics-tracking}

*Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

To convert email addresses to [!DNL RampIDs] o [!DNL ID5] IDs, you must do the following:

1. (If you haven&#39;t already done so) Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.

1. Register with the universal ID partner and deploy universal ID-specific code on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs:

   * **For [!DNL RampIDs]:** You must deploy an additional JavaScript tag on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs. Póngase en contacto con su equipo de cuentas de Adobe Systems, que le dará instrucciones para registrarse en un [!DNL LiveRamp] [!DNL LaunchPad] etiqueta de [!DNL LiveRamp] Authentication Traffic Solutions. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, su equipo de cuentas de Adobe Systems generará y proporcionará un etiqueta único para que su organización lo implementar en sus páginas web.

## Paso 2: Crear una fuente audiencia en DSP {#source-create}

1. [Crear una fuente](source-manage.md) audiencia para importar audiencias a su DSP cuenta o a una anunciante cuenta. Puede elegir convertir sus identificadores usuario a cualquiera de los [formatos](source-about.md) de ID universales disponibles.

   La configuración de origen incluirá una clave de origen generada automáticamente, que usará para insertar los datos de segmento.

1. Después de crear el audiencia origen, comparta la clave de código fuente con el [!DNL Optimizely] usuario.

## Step 3: Prepare and push the segment data {#push-data}

The advertiser must prepare and push the data with the help of their [!DNL Optimizely] representative.

1. Within [!DNL Optimizely Data Platform], hash the email IDs for the advertiser&#39;s audience using the SHA-256 algorithm.

1. Follow&#39;s [[!DNL Optimizely's] instructions to push the segment to DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Include the following information to enable the integration:

   * **Clave Origen:** Esta es la clave de origen creada en [el paso 2](#source-create).

   * **Code de cuenta:** Este es el Code alfanumérico DSP cuenta, que puede encontrar en DSP en [!UICONTROL Settings] > [!UICONTROL Account].

Los segmentos estarán disponibles en DSP en un plazo de 24 horas y se actualizarán según lo configurado para el anunciante. Independientemente de la frecuencia con la que se actualice el segmento, la inclusión en un segmento caduca después de 30 días de forma predeterminada o después de un período de vencimiento especificado por el cliente. Actualizar los segmentos volviéndolos a insertar desde antes de [!DNL Optimizely] la caducidad. Para solicitud la caducidad de una segmento personalizada, póngase en contacto con el equipo de Adobe Systems cuentas.

## Paso 4: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

After you complete all steps, verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is available and is populating within 24 hours. Comparar el número de ID universales con el número de direcciones correo electrónico hash originales.

The translation rate of hashed email addresses to universal IDs should be greater than 90%. For example, if you send 100 hashed email addresses from your customer data platform, they should be translated to more than 90 universal IDs. A translation rate of 90% or less is an issue. For more information about how the segment counts can vary, see &quot;[Causas de variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances).&quot;

For troubleshooting support, contact your Adobe Account Team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar orígenes de audiencia para activar el Audiences de ID universal](source-manage.md)
>* [Compatibilidad con la activación de ID universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de la gestión de público](/help/dsp/audiences/audience-about.md)
