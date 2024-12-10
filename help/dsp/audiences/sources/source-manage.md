---
title: Administrar fuentes de audiencia para activar audiencias de ID universal
description: Obtenga información sobre cómo crear y administrar una fuente para importar audiencias desde la plataforma de datos del cliente y convertirlas en segmentos que contengan ID universales.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# Administrar fuentes de audiencia para activar audiencias de ID universal

*característica de Beta*

DSP Cree una fuente de datos en los segmentos para cada audiencia de origen en la plataforma de datos del cliente que desee convertir en segmentos que contengan tipos de ID universales especificados. DSP Puede importar los segmentos a la cuenta de usuario de la organización o a una cuenta de anunciante de la cuenta de la organización de que se trate. Los cargos por datos se aplican en función de los tipos de ID universal seleccionados. Una vez creada una fuente de datos, se requieren pasos adicionales para introducir las audiencias de cada plataforma de datos del cliente. Vea la nota al final del procedimiento para crear un origen.

Más adelante puede cambiar los tipos de ID universales a los que se traduce la audiencia de origen y ver un registro de los cambios.

También puede eliminar un origen.

## Creación de un Source de audiencia

<!-- Not sure about this

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

## Cambio de los tipos de ID para un Audience Source

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Edit]**.

1. Cambiar los [ID seleccionados para el origen](#source-settings).

1. Haga clic en **[!UICONTROL Save]**.

## Eliminar un Audience Source

Al eliminar un origen, se eliminan los segmentos traducidos a través del origen.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Visualización del registro de cambios de un Audience Source

Puede ver detalles sobre los cambios realizados en un registro de origen de audiencia y, opcionalmente, adjuntar notas al registro.

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Change log]**.

1. (Opcional) Para adjuntar una nota al registro de cambios:

   1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Add Notes]**.

   1. Escriba la nota y haga clic en **[!UICONTROL Save]**.

      La longitud máxima es de 256 caracteres.

1. (Opcional) Para abrir el registro en una pantalla de detalles más grande, mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL View Details]**.

## Configuración de Audience Source {#source-settings}

**[!UICONTROL Data Visibility Level]:** Si los segmentos están disponibles para un solo anunciante con acceso a la cuenta (*[!UICONTROL Advertiser]*) o para todos los anunciantes con acceso a la cuenta *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (solo visibilidad de nivel de anunciante) El anunciante para el que los segmentos están disponibles. Seleccione uno de la lista de anunciantes con acceso a la cuenta.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] orígenes solamente) El identificador de organización de Adobe Experience Cloud para la cuenta [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** Tipos de ID a los que convertirá su información de identificación personal (PII). Si selecciona varios tipos, el segmento generado se rellena con valores para cada tipo de ID seleccionado (como un [!DNL RampID] y un [!DNL Unified ID2.0] para cada dirección de correo electrónico). Los cargos por datos se aplican según corresponda.

Para [!DNL RampID] y [!DNL Unified ID2.0], el proveedor busca cada dirección de correo electrónico para ver si ya existe un identificador y traduce la dirección a un identificador coincidente cuando está disponible. Si no existe ningún ID para la dirección, se crea un nuevo ID.

>[!NOTE]
>
>Solo se puede segmentar un tipo de ID en una única ubicación. Para probar el rendimiento por tipo de identificador, [cree una ubicación independiente](/help/dsp/campaign-management/placements/placement-create.md) para cada tipo de identificador en el segmento.

* *[!DNL RampID]:* Para convertir PII en [!DNL RampID]. Puede usar [!DNL RampIDs] para volver a dirigirse a los usuarios que iniciaron sesión y para la medición de [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0](Beta):* Para convertir PII en un ID de [Unified ID 2.0](https://unifiedid.com) para redireccionar a los usuarios que iniciaron sesión.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Los términos del contrato de servicio para convertir PII en identificadores universales. DSP Usted u otro usuario de la cuenta debe aceptar los términos una vez, para poder convertir los datos a un nuevo tipo de ID. Para los clientes con contratos de servicio gestionado, su equipo de cuenta de Adobe recibirá su consentimiento y aceptará los términos en nombre de su organización. Para leer los términos, haga clic en **>**. Para aceptar los términos, desplácese hasta la parte inferior de los términos y haga clic en **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (de solo lectura; generado automáticamente) La clave de origen que puede utilizar para crear una conexión de destino en la plataforma de datos del cliente para insertar audiencias en Advertising DSP. Puede copiar el valor en el portapapeles para pegarlo en la configuración de conexión de destino o en un archivo.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](source-about.md)
>* [Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Convertir los identificadores de usuario de [!DNL Adobe Real-Time CDP] a identificadores universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir los identificadores de usuario de [!DNL Amperity] a identificadores universales](/help/dsp/audiences/sources/source-amperity.md)
>* [Convertir los identificadores de usuario de [!DNL Optimizely] a identificadores universales](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convertir los identificadores de usuario de [!DNL Tealium] a identificadores universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
