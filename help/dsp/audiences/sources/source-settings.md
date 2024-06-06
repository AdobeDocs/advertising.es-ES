---
title: Configuración de origen de audiencia
description: Obtenga información acerca de la configuración de las fuentes de audiencia.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Configuración de origen de audiencia

*Función beta*

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
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Acerca de las fuentes de audiencia de origen](source-about.md)
>* [Importar manualmente segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
