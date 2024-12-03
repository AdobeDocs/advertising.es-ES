---
title: 'Actualizar el código de seguimiento de la ID de AMO (s_kwcid) para una cuenta  [!DNL Google Ads] '
description: Aprenda a cambiar al código de seguimiento de ID de AMO más reciente para una cuenta de  [!DNL Google Ads] .
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: edb46265c6977a1e2c1b352f41fedcfc3a9e3bbf
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Actualizar el código de seguimiento del ID de AMO (s_kwcid) para una cuenta de [!DNL Google Ads]

*Anunciantes con una integración de Adobe Advertising-Adobe Analytics solamente*

*[!DNL Google Ads]solo cuentas*

El formato heredado (anterior a octubre de 2019) para el [código de seguimiento de ID de AMO](/help/integrations/analytics/ids.md#amo-id-formats) para las cuentas existentes de [!DNL Google Ads] no admite algunas características en Analytics, como la creación de informes en los niveles de campaña y grupo de anuncios para las campañas con el rendimiento máximo de [!DNL Google Ads], las campañas de borradores y experimentos, y otros casos de uso en los que existe la misma combinación de tipo anuncio+palabra clave+coincidencia en varias campañas.

El formato actual incluye parámetros para el ID de campaña y el ID de grupo de publicidad:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Para una cuenta existente que utiliza el formato heredado, puede cambiar al formato actual. Si no tiene campañas Máximo rendimiento de o campañas de borradores y experimentos, la migración al nuevo formato es opcional.

Todas las cuentas nuevas de [!DNL Google Ads] utilizan automáticamente el formato de ID de AMO actual.

>[!NOTE]
>
>Esta opción solo está disponible para cuentas que no utilizan el formato actual.
>
>Después de migrar una cuenta, todos los datos de clics, costes e impresiones se presentarán correctamente tras el cambio, pero cualquier pulsación que se haya producido antes de la migración seguirá atribuyéndose a los datos de conversión basados en el antiguo formato de ID de AMO.

1. En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenga el cursor sobre el nombre de la cuenta, haga clic en ![icono desplegable de flecha](/help/search-social-commerce/assets/arrow-dropdown-menu.png) y, a continuación, seleccione **[!UICONTROL Edit]**.

1. Haga clic en **[!UICONTROL Set Account Tracking]**.

1. Inicie la migración:

   1. Junto a **[!UICONTROL S_KWCID FORMAT]** en la configuración de [!UICONTROL Account Tracking], haga clic en **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Haga clic en **[!UICONTROL Migrate to new s_kwcid format]**.

   1. En el mensaje de confirmación, active la casilla y, a continuación, haga clic en **[!UICONTROL Continue]**.

   1. En la configuración de la cuenta, haga clic en **[!UICONTROL Post]**.

   Los metadatos de las campañas se actualizaron en [!DNL Analytics] en unos días. El seguimiento continúa sin interrupciones, por lo que no se pierden datos, pero es posible que los informes no reflejen los nuevos códigos de seguimiento hasta que [!DNL Analytics] reciba todos los metadatos.

   >[!NOTE]
   >
   >Todas las pulsaciones que se produjeron antes de la migración siguen informando de los datos de conversión basados en el formato antiguo.

1. Una vez iniciada la migración, actualice la configuración del sufijo de la página de aterrizaje (denominado &quot;sufijo URL final&quot; en algunas redes publicitarias) según sea necesario:

   * Cuando la característica [!UICONTROL Auto Upload]&quot; está habilitada en la configuración de seguimiento, Search, Social y Commerce actualizan automáticamente el código de seguimiento en el sufijo de página de aterrizaje de esta cuenta y sus campañas. Usted no tiene que hacer nada.

   * Cuando la característica [!UICONTROL Auto Upload]&quot; no está habilitada y no usa la [característica de ID de AMO del lado del servidor](/help/integrations/analytics/ids.md#amo-id-formats), debe actualizar manualmente el parámetro de ID de AMO en la configuración del sufijo de página de aterrizaje. Puede cambiar manualmente los sufijos de nivel de campaña y de cuenta en [configuración de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) y [configuración de campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md), o bien [cargando cambios en una hoja de edición por lotes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md). Para configurar un sufijo en el nivel de grupo de anuncios o inferior, use el editor [!DNL Google Ads].

   * Si incluye el ID de AMO en la configuración de URL base para cualquier componente de campaña, muévalo a la configuración de Sufijo de página de aterrizaje correspondiente.

1. (Recomendado) Compruebe los datos de esta cuenta en [!DNL Analytics] antes de migrar cuentas adicionales.

>[!MORELIKETHIS]
>
>* [Administrar cuentas de red de anuncios](ad-network-account-manage.md)
>* [ID de Adobe Advertising usados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Información general de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
