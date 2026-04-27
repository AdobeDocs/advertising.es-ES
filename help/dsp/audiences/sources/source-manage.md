---
title: Administrar fuentes de audiencia para activar audiencias de ID universal
description: Obtenga información sobre cómo crear y administrar una fuente para importar audiencias desde la plataforma de datos del cliente y convertirlas en segmentos que contengan ID universales.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
TQID: https://experienceleague.adobe.com/us8NC8BEngb240MAW8hEo-DHGoW7MRDWvu0HedMsnFs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 0%

---

# Administrar fuentes de audiencia para activar audiencias de ID universal

*característica de Beta*

Cree una fuente en DSP para cada audiencia propia en la plataforma de datos del cliente que desee convertir en segmentos que contengan tipos de ID universales especificados. Puede importar los segmentos a la cuenta de DSP de su organización o a una cuenta de anunciante. Los cargos por datos se aplican en función de los tipos de ID universal seleccionados. Una vez creada una fuente de datos, se requieren pasos adicionales para introducir las audiencias de cada plataforma de datos del cliente. Vea la nota al final del procedimiento para crear un origen.

Más adelante puede cambiar los tipos de ID universales a los que se traduce la audiencia de origen y ver un registro de los cambios.

También puede eliminar un origen.

## Crear una fuente de audiencia

<!--
 Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Haga clic en **[!UICONTROL Add Source]**.

1. En el menú [!UICONTROL Select a Type], seleccione su [plataforma de datos del cliente](source-about.md):

   * *[!UICONTROL RT-CDP]*: El [!DNL Adobe Real-Time CDP].

   * *[!UICONTROL ActionIQ]*: la plataforma de datos del cliente [!DNL ActionIQ].

   * *[!UICONTROL Amperity]*: la plataforma de datos del cliente [!DNL Amperity].

   * *[!UICONTROL Optimizely]*: la plataforma de datos del cliente [!DNL Optimizely].

   * *[!UICONTROL Tealium CDP]*: (Solo usuarios configurados) La plataforma de datos del cliente [!DNL Tealium].

1. Especifique [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Escriba la [configuración de origen](#source-settings) restante.

   Mantener una copia de [!UICONTROL Source Key] que se ha generado. Necesitará el valor más tarde.

1. Haga clic en **[!UICONTROL Save]**.

>[!NOTE]
>
>Después de crear una fuente para la plataforma de datos del cliente, debe completar los pasos adicionales para importar la audiencia. Vea el [flujo de trabajo para [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md),<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> el [flujo de trabajo para [!DNL Amperity]](source-amperity.md), el [flujo de trabajo para [!DNL Optimizely]](source-optimizely.md) y el [flujo de trabajo para [!DNL Tealium]](source-tealium.md).

## Cambio de los tipos de ID de una fuente de audiencia

<!-- 
Clarify this:

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses that you shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we don't delete any historical IDs of that type from the segments shared through the source.

-->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Edit]**.

1. Cambiar los [ID seleccionados para el origen](#source-settings).

1. Haga clic en **[!UICONTROL Save]**.

## Eliminar una fuente de audiencia

Al eliminar un origen, se eliminan los segmentos traducidos a través del origen.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Ver el registro de cambios de una fuente de audiencia

Puede ver detalles sobre los cambios realizados en un registro de origen de audiencia y, opcionalmente, adjuntar notas al registro.

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Change log]**.

1. (Opcional) Para adjuntar una nota al registro de cambios:

   1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Add Notes]**.

   1. Escriba la nota y haga clic en **[!UICONTROL Save]**.

      La longitud máxima es de 256 caracteres.

1. (Opcional) Para abrir el registro en una pantalla de detalles más grande, mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL View Details]**.

## Configuración de origen de audiencia {#source-settings}

**[!UICONTROL Data Visibility Level]:** Si los segmentos están disponibles para un solo anunciante con acceso a la cuenta (*[!UICONTROL Advertiser]*) o para todos los anunciantes con acceso a la cuenta *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (solo visibilidad de nivel de anunciante) El anunciante para el que los segmentos están disponibles. Select one from the list of advertisers with access to the account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] sources only) The Adobe CX Enterprise organization ID for the [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** The ID types to which you&#39;ll convert your personally identifiable information (PII). If you select multiple types, the generated segment is populated with values for each selected ID type (such as a [!DNL RampID] and a [!DNL Unified ID2.0] for each email address). Data charges are applied accordingly.

For [!DNL RampID] and [!DNL Unified ID2.0], the vendor looks up each email address to see if an ID already exists and translates the address to a matching ID when available. If an ID doesn&#39;t exist for the address, then it creates a new ID.

>[!NOTE]
>
>You can target only one type of ID in a single placement. To test performance by ID type, [create a separate placement](/help/dsp/campaign-management/placements/placement-create.md) for each ID type in the segment.

* *[!DNL RampID]:* To convert PII to a [!DNL RampID]. You can use [!DNL RampIDs] for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

* *[!DNL Unified ID2.0] (Beta):* To convert PII to a [Unified ID 2.0](https://unifiedid.com) ID for retargeting logging-in users.

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** The terms of service agreement for converting PII to universal IDs. You or another user in the DSP account must accept the terms once before you can convert data to a new ID type. For customers with managed service contracts, your Adobe Account Team gets your consent and accepts the terms on your organization&#39;s behalf. To read the terms, click **>**. To accept the terms, scroll to the bottom of the terms and click **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Read-only; generated automatically) The source key that you can use to create a destination connection in the customer data platform to push audiences to Advertising DSP. You can copy the value to your clipboard to paste into the destination connection settings or into a file.

>[!MORELIKETHIS]
>
>* [About first-party audience sources](source-about.md)
>* [Support for activating universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Convert user IDs from [!DNL Adobe Real-Time CDP] to universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convert user IDs from [!DNL Amperity] to universal IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Convert user IDs from [!DNL Optimizely] to universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convert user IDs from [!DNL Tealium] to universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
