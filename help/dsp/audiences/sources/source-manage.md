---
title: Administrar fuentes de audiencia para activar audiencias de ID universal
description: Obtenga información sobre cómo crear y administrar una fuente para importar audiencias desde la plataforma de datos del cliente y convertirlas en segmentos que contengan ID universales.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Administrar fuentes de audiencia para activar audiencias de ID universal

*Función beta*

DSP Cree una fuente de datos en los segmentos para cada audiencia de origen en la plataforma de datos del cliente que desee convertir en segmentos que contengan tipos de ID universales especificados. DSP Puede importar los segmentos a la cuenta de usuario de la organización o a una cuenta de anunciante de la cuenta de la organización de que se trate. Los cargos por datos se aplican en función de los tipos de ID universal seleccionados.

Se requieren pasos adicionales para introducir las audiencias de cada plataforma de datos del cliente. Consulte la nota al final del procedimiento.

Más adelante puede cambiar los tipos de ID universales a los que se traduce la audiencia de origen y ver un registro de los cambios.

También puede eliminar un origen.

## Crear una fuente de audiencia

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clic **[!UICONTROL Add Source]**.

1. En el [!UICONTROL Select a Type] menú, seleccione la plataforma de datos del cliente:

   * *[!UICONTROL RT-CDP]*: [El [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: La [[!DNL ActionIQ] plataforma de datos del cliente](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (solo usuarios configurados) El [[!DNL Tealium] plataforma de datos del cliente](source-about.md).

1. Especifique el [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Introduzca el resto [configuración de origen](source-settings.md).

   Conserve una copia del [!UICONTROL Source Key] que se genera. Necesitará el valor más tarde.

1. Clic **[!UICONTROL Save]**.

>[!NOTE]
>
>Después de crear una fuente para la plataforma de datos del cliente, deberá completar los pasos adicionales. Consulte la [flujo de trabajo para importar audiencias desde [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> y el [flujo de trabajo para importar audiencias desde [!DNL Tealium]](source-tealium.md).

## Cambiar los tipos de ID para una fuente de audiencia

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Edit]**.

1. Cambie el [ID seleccionados para el origen](source-settings.md).

1. Clic **[!UICONTROL Save]**.

## Eliminar una fuente de audiencia

Al eliminar una fuente, se eliminan los segmentos traducidos a través de la fuente.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Ver el registro de cambios de una fuente de audiencia

Puede ver detalles sobre los cambios realizados en un registro de origen de audiencia y, opcionalmente, adjuntar notas al registro.

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Change log]**.

1. (Opcional) Para adjuntar una nota al registro de cambios:

   1. Mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL Add Notes]**.

   1. Introduzca la nota y haga clic en **[!UICONTROL Save]**.

      La longitud máxima es de 256 caracteres.

1. (Opcional) Para abrir el registro en una pantalla de detalles más grande, mantenga el cursor sobre la fila de origen y haga clic en **[!UICONTROL View Details]**.

## Configuración de origen de audiencia

**[!UICONTROL Data Visibility Level]:** Si los segmentos están disponibles para un solo anunciante con acceso a la cuenta (*[!UICONTROL Advertiser]*) o a todos los anunciantes con acceso a la cuenta *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Solo visibilidad a nivel de anunciante) El anunciante para el que los segmentos están disponibles. Seleccione uno de la lista de anunciantes con acceso a la cuenta.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] solo fuentes) El ID de organización de Adobe Experience Cloud para [!DNL Adobe Experience Platform] cuenta.

**[!UICONTROL Convert PII to the following IDs]:** Los tipos de ID a los que convertirá su información de identificación personal (PII). Si selecciona varios tipos, el segmento generado se rellena con valores para cada tipo de ID seleccionado (como un [!DNL RampID] y una [!DNL Unified ID2.0] para cada dirección de correo electrónico). Los cargos por datos se aplican según corresponda.

Para [!DNL RampID] y [!DNL Unified ID2.0], el proveedor busca cada dirección de correo electrónico para ver si ya existe un ID y traduce la dirección a un ID coincidente cuando está disponible. Si no existe ningún ID para la dirección, se crea un nuevo ID.

>[!NOTE]
>
>Solo se puede segmentar un tipo de ID en una única ubicación. Para probar el rendimiento por tipo de ID, [crear una ubicación independiente](/help/dsp/campaign-management/placements/placement-create.md) para cada tipo de ID del segmento.

* *[!DNL RampID]:* Para convertir PII en un [!DNL RampID]. Puede utilizar [!DNL RampIDs] para redireccionar usuarios que inician sesión y para [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) medición.

* *[!DNL Unified ID2.0](Beta):* Para convertir PII en un [ID unificado 2.0](https://unifiedid.com) ID para volver a direccionar a los usuarios que iniciaron sesión.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** El acuerdo de términos de servicio para convertir PII en ID universales. DSP Usted u otro usuario de la cuenta debe aceptar los términos una vez, para poder convertir los datos a un nuevo tipo de ID. Para los clientes con contratos de servicio gestionado, su equipo de cuenta de Adobe recibirá su consentimiento y aceptará los términos en nombre de su organización. Para leer los términos, haga clic en **>**. Para aceptar los términos, desplácese hasta la parte inferior de los términos y haga clic en **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** DSP (Solo lectura; se genera automáticamente) La clave de origen que puede utilizar para crear una conexión de destino en la plataforma de datos del cliente para insertar audiencias en Advertising. Puede copiar el valor en el portapapeles para pegarlo en la configuración de conexión de destino o en un archivo.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](source-about.md)
>* [Importar manualmente segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
