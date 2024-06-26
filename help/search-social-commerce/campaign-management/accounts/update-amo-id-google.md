---
title: Actualizar el código de seguimiento de ID de AMO (s_kwcid) para un [!DNL Google Ads] account
description: Obtenga información sobre cómo cambiar al código de seguimiento de ID de AMO más reciente para un [!DNL Google Ads] cuenta.
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Actualizar el código de seguimiento de ID de AMO (s_kwcid) para un [!DNL Google Ads] account

*Anunciantes solo con una integración de Adobe Advertising y Adobe Analytics*

*[!DNL Google Ads]solo cuentas*

El formato heredado (antes de octubre de 2019) para [Código de seguimiento de ID de AMO](/help/integrations/analytics/ids.md#amo-id-formats) para los existentes [!DNL Google Ads] Las cuentas de no admiten algunas funciones de Analytics, como la creación de informes en los niveles de campaña y grupo de publicidad para [!DNL Google Ads] campañas de rendimiento máximo, campañas de borradores y experimentos, y otros casos de uso en los que existe la misma combinación de tipo anuncio+palabra clave+coincidencia en varias campañas.

El formato actual incluye parámetros para el ID de campaña y el ID de grupo de publicidad:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Puede cambiar al formato actual para cualquiera o todas las cuentas existentes, individualmente. Si no tiene campañas Máximo rendimiento de o campañas de borradores y experimentos, la migración al nuevo formato es opcional.

Todo nuevo [!DNL Google Ads] Las cuentas de utilizan automáticamente el formato de ID de AMO actual.

>[!NOTE]
>
>Después de migrar una cuenta, todos los datos de clics, costes e impresiones se presentarán correctamente tras el cambio, pero cualquier pulsación que se haya producido antes de la migración seguirá atribuyéndose a los datos de conversión basados en el antiguo formato de ID de AMO.

1. En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenga el cursor sobre el nombre de la cuenta y haga clic en ![icono desplegable de flecha](/help/search-social-commerce/assets/arrow-dropdown-menu.png), y luego seleccione **[!UICONTROL Edit]**.

1. Clic **[!UICONTROL Set Account Tracking]**.

1. Inicie la migración:

   1. Junto a **[!UICONTROL S_KWCID FORMAT]** , haga clic en **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Clic **[!UICONTROL Migrate to new s_kwcid format]**.

   1. En el mensaje de confirmación, active la casilla y, a continuación, haga clic en **[!UICONTROL Continue]**.

   1. En la configuración de la cuenta, haga clic en **[!UICONTROL Post]**.

   Los metadatos de las campañas se actualizan en [!DNL Analytics] dentro de unos días. El seguimiento continúa sin interrupciones, por lo que no se pierden datos, pero es posible que los informes no reflejen los nuevos códigos de seguimiento hasta [!DNL Analytics] recibe todos los metadatos.

   >[!NOTE]
   >
   >Todas las pulsaciones que se produjeron antes de la migración siguen informando de los datos de conversión basados en el formato antiguo.

1. Una vez iniciada la migración, actualice la configuración del sufijo de la página de aterrizaje (denominado &quot;sufijo URL final&quot; en algunas redes publicitarias) según sea necesario:

   * Si la variable [!UICONTROL Auto Upload]La función &quot; está habilitada en la configuración de seguimiento, Buscar, Social y Commerce actualizan automáticamente el código de seguimiento en el sufijo de página de aterrizaje de esta cuenta y sus campañas. Usted no tiene que hacer nada.

   * Si la variable [!UICONTROL Auto Upload]&quot; no está activada y no se utiliza la función &quot; [Función de ID de AMO del lado del servidor](/help/integrations/analytics/ids.md#amo-id-formats), debe actualizar manualmente el parámetro de ID de AMO en la configuración del sufijo de la página de aterrizaje. Puede cambiar manualmente los sufijos de nivel de cuenta y de campaña en la configuración de cuenta y campaña o cargando los cambios en una hoja de edición por lotes. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el [!DNL Google Ads] editor.

   * Si incluye el ID de AMO en la configuración de URL base para cualquier componente de campaña, muévalo a la configuración de Sufijo de página de aterrizaje correspondiente.

1. (Recomendado) Compruebe los datos de esta cuenta en [!DNL Analytics] antes de migrar cuentas adicionales.

>[!MORELIKETHIS]
>
>* [Administrar las cuentas de red de publicidad](ad-network-account-manage.md)
>* [ID de Adobe Advertising utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Información general de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
