---
title: Novedades de la versión
description: Obtenga información sobre las actualizaciones de las integraciones entre Adobe Advertising y otros productos y servicios en Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: ae93aff0056e58fd4427620d2eab76330a73039c
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Novedades de la versión

Las siguientes funciones son nuevas o han cambiado recientemente.

| Fecha | Función | Descripción | Para obtener más información |
| ---- | ------- | ----------- | -------------------- |
| 26 de marzo de 2025 | [!DNL Adobe Analytics for Advertising] | (Anunciantes con Search, Social, &amp; Commerce; [!DNL Microsoft Advertising] cuentas; y [!DNL Adobe Analytics for Advertising]) Para las cuentas con la opción de seguimiento [!UICONTROL Auto Upload], el formato del parámetro de ID de AMO en los sufijos de página de aterrizaje para todos los tipos de campaña se actualizó al formato más reciente. Anteriormente, las campañas Máximo rendimiento de para la mayoría de las cuentas se migraban al nuevo formato.<br><br>Para cuentas sin la opción de seguimiento [!UICONTROL Auto Upload] que aún no se migraron al nuevo formato, sin embargo, debe actualizar manualmente cada sufijo de página de aterrizaje para incluir el nuevo formato de ID de AMO.<br><br>Formato actual: `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | Consulte &quot;[Información general sobre [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)&quot; y los [formatos de ID de AMO](/help/integrations/analytics/ids.md#amo-id-formats).&quot; |
| 13 de noviembre de 2024 | [!DNL Analytics for Advertising] | (Anunciantes con [!DNL Analytics for Advertising] y Adobe Customer Journey Analytics) Si utiliza variables reservadas para capturar sus ID de AMO e ID de EF, puede prepararse para una futura integración entre Adobe Advertising y Adobe Customer Journey Analytics copiando las variables reservadas para el ID de AMO y el ID de EF en el estándar [!DNL eVars] lo antes posible. Esto permitirá la recopilación de datos históricos para los ID de AMO y EF ID en cuanto complete la tarea, y los datos históricos estarán disponibles para su uso futuro. El equipo de cuenta de Adobe le informará si utiliza variables reservadas y necesita completar esta tarea. | Consulte &quot;[Recopilar datos históricos para ID de AMO e ID de EF para su uso en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)&quot;. |
| Publicado el 29 de octubre de 2024 | [!DNL Adobe Analytics for Advertising] | (Anunciantes con [!DNL Adobe Analytics for Advertising] y [!DNL Microsoft Advertising] campañas de rendimiento máximo) Los datos de nivel de grupo de recursos para sus campañas de rendimiento máximo ahora están disponibles en Adobe Analytics al implementar un nuevo parámetro de ID de AMO ([!DNL s_kwcid]) en las direcciones URL de seguimiento para sus campañas de rendimiento máximo, que no incluyen anuncios y palabras clave. El seguimiento de la mayoría de las cuentas con campañas Máximo rendimiento ya se ha migrado al nuevo formato. Sin embargo, en el caso de las cuentas con campañas Máximo rendimiento de sin la opción de seguimiento [!UICONTROL Auto Upload] que aún no se hayan migrado al nuevo formato, deberá actualizar manualmente cada sufijo de página de aterrizaje para incluir el nuevo formato de ID de AMO.<br><br>Los datos de Adobe Analytics para tus campañas Máximo rendimiento también están disponibles en Buscar, Social y Commerce. | Ver el nuevo [formato de ID de AMO](/help/integrations/analytics/ids.md#amo-id-formats) y [cuándo y cómo añadir el parámetro a las URL de seguimiento](/help/integrations/analytics/ids.md#amo-id-implement). |
| 16 de diciembre de 2023 | Ayuda | En un nuevo documento se explica cómo configurar pruebas A/B en [!DNL Target] para el tráfico de pulsaciones de anuncios en Search, Social y Commerce, así como sugerencias para medir y visualizar las pruebas en [!DNL Analytics]. | Consulte &quot;[Configurar pruebas A/B en Adobe Target para anuncios de Search, Social y Commerce](/help/integrations/target/ab-tests-search.md)&quot;. |
| 8 de agosto de 2023 | [!DNL Analytics for Advertising] | Algunas [!DNL Analytics] métricas de eventos de éxito, incluidas las métricas de conversión estándar, personalizadas y reservadas y las métricas de tráfico, están disponibles automáticamente en DSP y en Search, Social y Commerce. Ahora, también puede configurar sus propias métricas de éxito basadas en sus [!DNL Analytics] [!DNL eVars] y [!DNL props] existentes canalizando los datos de nivel [!DNL eVar] y [!DNL prop] en un evento de éxito personalizado. | Consulte &quot;[Crear métricas de conversión a partir de Adobe Analytics [!DNL eVars] y [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;. |
| 13 de julio de 2023 | Informes | (Usuarios de DSP con [!DNL Analytics for Advertising]) Las conversiones de visualización de las ubicaciones de TV conectada (CTV) ahora se incluyen en los datos de conversión disponibles en Adobe Analytics. | Consulte la sección sobre &quot;Ejemplos de cómo usar la integración&quot; en &quot;[Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)&quot;. |
| 1 de noviembre de 2022 | Ayuda | En un nuevo documento se explica cómo implementar el uso compartido de señales de clics y visualizaciones entre Advertising DSP y Adobe Target, cómo configurar una actividad de prueba A/B en [!DNL Target] para los anuncios de DSP y cómo configurar Adobe Analytics Analysis Workspace para ver los datos de prueba. | Consulte &quot;[Configurar pruebas A/B en Adobe Target para Advertising DSP Ads](/help/integrations/target/ab-tests-dsp.md)&quot;. |
| 17 de agosto de 2022 | Ayuda | En un nuevo capítulo se explican todas las formas en que Adobe Advertising está integrado con Adobe Audience Manager. | Consulte el capítulo sobre &quot;Integración con Adobe Audience Manager&quot;, que incluye una descripción general de &quot;[Integraciones de Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)&quot;. |
| 27 de abril de 2021 | [!DNL Analytics for Advertising] | Aprenda por qué y cómo agregar macros de [!DNL Analytics for Advertising] a las etiquetas de publicidad de [!DNL Google Campaign Manager 360] para enviar datos de clics a Adobe Analytics. | Ver &quot;[Anexar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md).&quot; |
| 19 de abril de 2021 | [!DNL Analytics for Advertising] | Aprenda por qué y cómo anexar macros a las etiquetas de publicidad de [!DNL Flashtalking] para enviar datos de clics a Adobe Analytics. | Ver &quot;[Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad](/help/integrations/analytics/macros-flashtalking.md).&quot; |
| 27 de octubre de 2021 | [!DNL Analytics for Advertising] | Si su organización desea dejar de usar la biblioteca heredada de Adobe Analytics `visitorAPI.js` y cambiar a la biblioteca de [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es) (`alloy.js`) para la recopilación de datos, deberá realizar algunos cambios para habilitar la vinculación de ID. | Consulte &quot;[Uso de la biblioteca  [!DNL Last Event Service] JavaScript con Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md)&quot;. |
| 26 de mayo de 2021 | Ayuda | El capítulo &quot;[!DNL Analytics for Advertising]&quot; ahora incluye un subcapítulo sobre &quot;Trabajando en [!DNL Analytics Marketing Channels].&quot; | Consulte: &quot;[Aspectos básicos de los canales de marketing](/help/integrations/analytics/marketing-channels/mc-overview.md)&quot;, &quot;[Uso de Adobe Advertising ID para crear [!DNL Analytics Marketing Channels] reglas de procesamiento](/help/integrations/analytics/marketing-channels/mc-ids.md)&quot;, &quot;[Uso de [!DNL Analytics Marketing Channels] con datos de Adobe Advertising](/help/integrations/analytics/marketing-channels/mc-ac-data.md)&quot; y &quot;[Por qué los datos del canal pueden variar entre Adobe Advertising y [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)&quot;. |
| 26 de mayo de 2021 | Ayuda | Se agregó un vínculo a todos los tutoriales en vídeo acerca de [!DNL Analytics for Advertising]. | Consulte: &quot;[Tutoriales de vídeo sobre integraciones de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=es)&quot;. |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
