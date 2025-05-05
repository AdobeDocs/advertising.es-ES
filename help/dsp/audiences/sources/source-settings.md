---
title: Configuración de Audience Source
description: Obtenga información acerca de la configuración de las fuentes de audiencia.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Configuración de Audience Source

*característica de Beta*

**[!UICONTROL Data Visibility Level]:** Si los segmentos están disponibles para un solo anunciante con acceso a la cuenta (*[!UICONTROL Advertiser]*) o para todos los anunciantes con acceso a la cuenta *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (solo visibilidad de nivel de anunciante) El anunciante para el que los segmentos están disponibles. Seleccione uno de la lista de anunciantes con acceso a la cuenta.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] orígenes solamente) El identificador de organización de Adobe Experience Cloud para la cuenta [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** Tipos de ID a los que convertirá su información de identificación personal (PII). Si selecciona varios tipos, el segmento generado se rellena con valores para cada tipo de ID seleccionado (como un [!DNL RampID] y un [!DNL Unified ID2.0] para cada dirección de correo electrónico). Los cargos por datos se aplican según corresponda.

Para [!DNL RampID] y [!DNL Unified ID2.0], el proveedor busca cada dirección de correo electrónico para ver si ya existe un identificador y traduce la dirección a un identificador coincidente cuando está disponible. Si no existe ningún ID para la dirección, se crea un nuevo ID.

>[!NOTE]
>
>Solo se puede segmentar un tipo de ID en una única ubicación. Para probar el rendimiento por tipo de identificador, [cree una ubicación independiente](/help/dsp/campaign-management/placements/placement-create.md) para cada tipo de identificador en el segmento.

* *[!DNL RampID]:* Para convertir PII en [!DNL RampID]. Puede usar [!DNL RampIDs] para volver a dirigirse a los usuarios que iniciaron sesión y para la medición de [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0] (Beta):* Para convertir PII en un ID de [Unified ID 2.0](https://unifiedid.com) para redireccionar a los usuarios que iniciaron sesión.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Los términos del contrato de servicio para convertir PII en identificadores universales. DSP Usted u otro usuario de la cuenta debe aceptar los términos una vez, para poder convertir los datos a un nuevo tipo de ID. Para los clientes con contratos de servicio gestionado, su equipo de cuenta de Adobe recibirá su consentimiento y aceptará los términos en nombre de su organización. Para leer los términos, haga clic en **>**. Para aceptar los términos, desplácese hasta la parte inferior de los términos y haga clic en **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (de solo lectura; generado automáticamente) La clave de origen que puede utilizar para crear una conexión de destino en la plataforma de datos del cliente para insertar audiencias en Advertising DSP. Puede copiar el valor en el portapapeles para pegarlo en la configuración de conexión de destino o en un archivo.

>[!MORELIKETHIS]
>
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Acerca de las fuentes de audiencia de origen](source-about.md)
>* [Importar segmentos autenticados manualmente desde [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
