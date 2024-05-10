---
title: Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios
description: Obtenga información sobre cómo importar su [!DNL Adobe] DSP Audiencias de en Advertising y Search con Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---

# Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios

DSP Advertising y [!DNL Advertising Search, Social, & Commerce] puede extraer metadatos, datos de jerarquía y datos de audiencia únicos de todos los anuncios o agencias [!DNL Adobe] audiencias<!-- segments or audiences? Standardize terms per AAM's docs -->. Esto incluye datos para:

* Segmentos de Adobe Audience Manager

* Segmentos de Adobe Analytics publicados en Adobe Experience Cloud

* Segmentos que se crean con Adobe Experience Cloud [!DNL Audience Library]

* Segmentos creados en Adobe Experience Platform y enviados al Adobe Advertising mediante un Audience Manager

Para acceder a [!DNL Adobe] DSP Audiencias en el entorno de o [!DNL Creative]DSP , debe importar las audiencias en la interfaz de usuario de. Para acceder a [!DNL Adobe] audiencias en [!DNL Search, Social, & Commerce], debe importar las audiencias en [!DNL Search, Social, & Commerce].

## Requisitos previos

* El anunciante debe implementar [el [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) versión 2.0 o superior. El [!DNL Identity Service] proporciona un ID universal y persistente que identifica a los visitantes en todas las soluciones de Experience Cloud.

  La implementación incluye añadir el [!DNL Identity service] codifique a cada página web en los sitios del anunciante.

* La organización debe ser [habilitado para servicios de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) y tenga un Experience Cloud [!DNL Organization ID] (anteriormente denominado [!DNL IMS org ID]).

  El [!UICONTROL Organization ID] permite a las organizaciones con varios productos de Adobe Experience Cloud compartir datos entre algunos de los productos.

* (Anunciantes con [!DNL Analytics]) El anunciante debe [implementar [!DNL Analytics] usando `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) versión 1.6.4 o superior.

* Los visitantes del sitio web del anunciante no incluyen un gran volumen de [!DNL Apple Safari] usuarios.

* (Se recomienda cuando el anunciante utiliza Audience Manager y [!DNL Analytics]) Para reducir las llamadas a cada página web, elimine el Audience Manager existente [!DNL Data Integration Library] código para la recopilación de datos y habilitar el reenvío del lado del servidor para cada [!DNL Analytics] grupo de informes en su lugar. Para obtener más información, consulte &quot;[Resumen del reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Recomendado) Para tasas de coincidencia más altas, envíe solo datos del sitio web de origen al Adobe Advertising. Si el anunciante agrupa datos de terceros o datos sin conexión de un sistema de administración de la relación con los clientes, la fuga de datos puede reducir las tasas de coincidencia.

## Importación de audiencias de Audience Manager DSP a la

### DSP Pasos para importar audiencias a los grupos de trabajo

El [!DNL Adobe] Los equipos de operaciones de datos y cuentas de realizan los siguientes pasos.

1. El equipo de cuenta de Adobe debe configurar la opción de nivel de anunciante &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. El equipo de cuenta de Adobe debe enviar una solicitud<!-- Submit a request as a JIRA task? --> al equipo de operaciones de datos<!-- implementation team? --> para importar los segmentos de Audience Manager DSP de la organización mediante la integración de la API nativa de Advertising.

### ¿Qué cambios resultan en Audience Manager?

La API hace lo siguiente automáticamente:

* DSP Crea dos destinos de en el Audience Manager:

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Asigna los dos destinos a todos los segmentos del Audience Manager, lo que permite que el Audience Manager DSP comparta los segmentos con la cuenta del anunciante de la aplicación asociada con el mismo Experience Cloud. [!DNL Organization ID] se usa para el Audience Manager. <!-- Verify -->

  La organización puede, opcionalmente, eliminar segmentos innecesarios de los destinos dentro de Audience Manager.

* Agrega el siguiente píxel de sincronización de cookies de Exchange al contenedor de Audience Manager de la organización para mejorar el alcance de las campañas de los clientes:

   * Adobe AdCloud: 411 (se trata de una versión estándar y se incluye automáticamente como parte de [!DNL Identity Service] versión 2.0. Organizaciones con [!DNL Identity Service] las versiones anteriores a 2.0 deben añadir este píxel a su contenedor de Audience Manager.

## Importar audiencias de Audience Manager a [!DNL Search, Social, & Commerce]

### Pasos para importar audiencias en [!DNL Search, Social, & Commerce]

[!DNL Adobe] el personal realiza la mayoría o la totalidad de los pasos siguientes.

1. El equipo de cuenta de Adobe debe enviar una solicitud al equipo de operaciones de datos para configurar una integración entre [!DNL Search, Social, & Commerce] y Audience Manager. Incluya los nombres de los segmentos de Audience Manager a los que desea exportar [!DNL Search, Social, & Commerce].

1. En el Audience Manager, configure los destinos de [!DNL Search, Social, & Commerce]:

   1. Cree dos nuevos destinos: `[!UICONTROL Adobe Media Optimizer (HTTP)]` y `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] es un nombre anterior de [!DNL Search, Social, & Commerce].

   1. Especifique los segmentos para cada uno de los destinos.

      Con el [!UICONTROL Automatically map all current and future segments] , todos los segmentos se asignan y sincronizan diariamente.

      El [!UICONTROL Manually map segments] La opción le permite asignar manualmente los segmentos para sincronizarlos con el destino del lote (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). No es necesario asignar manualmente ningún segmento al destino HTTP.

1. En [!DNL Search, Social, & Commerce], ya sea la [!DNL Search, Social, & Commerce] el equipo de implementación o un usuario con la función de administrador de cliente de acceso directo deben iniciar la importación desde [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Debe introducir el Experience Cloud de la organización [!DNL Organization ID] ([!DNL IMS org ID]). El ID debe ser el mismo que se utilizó para la cuenta de Audience Manager de la organización.

### ¿Qué cambios resultan en Audience Manager?

Dos [!DNL Search, Social, & Commerce] Los destinos de están disponibles para la organización en Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Sincronización de datos

La importación inicial dura unas 24 horas. Después de la importación inicial, los datos se sincronizan en tiempo real, con un retraso de uno a dos segundos.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].

![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search, Social, & Commerce]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Dónde encontrar los segmentos sincronizados

### DSP En la

DSP En la práctica, los nombres de segmentos están organizados por la taxonomía de Audience Manager y disponibles con los recuentos de miembros de segmentos correspondientes en:

* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): en el [!UICONTROL Adobe Segments] de la pestaña [!UICONTROL Audience Targeting] sección.

* Entrada [configuración de audiencia](/help/dsp/audiences/audience-settings.md): en el [!UICONTROL Adobe Segments] pestaña.

### En Advertising Creative

Entrada [!DNL Creative]Sin embargo, los segmentos están disponibles en la configuración de experiencia para los nodos de destino.

### Entrada [!DNL Advertising Search, Social, & Commerce]

Entrada [!DNL Search, Social, & Commerce]No obstante, los segmentos están disponibles al crear una [!DNL Google] audiencia con el [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Para cada [!DNL Google] audiencia que cree, [!DNL Google] proporciona el tamaño de la audiencia.

>[!MORELIKETHIS]
>
>* [Integraciones de Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
