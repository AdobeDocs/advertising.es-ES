---
title: Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios
description: Obtenga información sobre cómo importar las audiencias  [!DNL Adobe] en Advertising DSP y buscar mediante Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios

Advertising DSP y [!DNL Advertising Search, Social, & Commerce] pueden extraer metadatos, datos de jerarquía y datos de audiencia única para todas las [!DNL Adobe] audiencias<!-- segments or audiences? Standardize terms per AAM's docs --> de un anunciante o una agencia, incluidas:

* Segmentos de Adobe Audience Manager

* Segmentos de Adobe Analytics publicados en Adobe Experience Cloud

* Segmentos creados con Adobe Experience Cloud [!DNL Audience Library]

* Segmentos creados en Adobe Experience Platform y enviados a Adobe Advertising mediante Audience Manager

Para acceder a las audiencias de [!DNL Adobe] en DSP o [!DNL Creative], debe importarlas a DSP. Para tener acceso a [!DNL Adobe] audiencias en [!DNL Search, Social, & Commerce], debe importar las audiencias en [!DNL Search, Social, & Commerce].

## Requisitos previos

* El anunciante debe implementar [the [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/es/docs/id-service/using/intro/overview) versión 2.0 o superior. El [!DNL Identity Service] proporciona un identificador universal y persistente que identifica a los visitantes en todas las soluciones de Experience Cloud.

  La implementación incluye agregar el código [!DNL Identity service] a cada página web de los sitios del anunciante.

* La organización debe estar [habilitada para los servicios de Experience Cloud](https://experienceleague.adobe.com/es/docs/core-services/interface/services/overview) y tener un Experience Cloud [!DNL Organization ID] (anteriormente denominado [!DNL IMS org ID]).

  [!UICONTROL Organization ID] permite que las organizaciones con varios productos de Adobe Experience Cloud compartan datos entre algunos de los productos.

* (Anunciantes con [!DNL Analytics]) El anunciante debe [implementar [!DNL Analytics] usando `appMeasurement.js`](https://experienceleague.adobe.com/es/docs/analytics/implementation/js/overview) versión 1.6.4 o superior.

* Los visitantes del sitio web del anunciante no incluyen un gran volumen de usuarios de [!DNL Apple Safari].

* (Recomendado cuando el anunciante usa Audience Manager y [!DNL Analytics]) Para reducir las llamadas a cada página web, elimine el código de Audience Manager [!DNL Data Integration Library] existente para la recopilación de datos y habilite el reenvío del lado del servidor para cada grupo de informes [!DNL Analytics]. Para obtener más información, consulte &quot;[Resumen del reenvío del lado del servidor](https://experienceleague.adobe.com/es/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Recomendado) Para tasas de coincidencia más altas, envíe solo datos del sitio web de origen a Adobe Advertising. Si el anunciante agrupa datos de terceros o datos sin conexión de un sistema de administración de la relación con los clientes, la fuga de datos puede reducir las tasas de coincidencia.

## Importar audiencias de Audience Manager a DSP

### Pasos para importar audiencias a DSP

Los equipos de operaciones de datos y cuenta de [!DNL Adobe] realizan los siguientes pasos.

1. El equipo de cuenta de Adobe debe establecer la configuración de nivel de anunciante &quot;[!UICONTROL Adobe Analytics Cloud]&quot;.

1. El equipo de cuenta de Adobe debe enviar una solicitud al equipo de operaciones de datos para importar los segmentos de Audience Manager de la organización mediante la integración de la API nativa de Advertising DSP.

### ¿Qué cambios resultan en Audience Manager?

La API hace lo siguiente automáticamente:

* Crea dos destinos de DSP en Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Asigna los dos destinos a todos los segmentos de Audience Manager, lo que permite que Audience Manager comparta los segmentos con la cuenta del anunciante de DSP asociada al mismo Experience Cloud [!DNL Organization ID] utilizado para Audience Manager.

  La organización puede, opcionalmente, eliminar segmentos innecesarios de los destinos dentro de Audience Manager.

* Agrega el siguiente píxel de sincronización de cookies de Exchange al contenedor de Audience Manager de la organización para mejorar el alcance de las campañas de los clientes:

   * Adobe AdCloud: 411 (Este píxel se convierte en estándar y automáticamente como parte de [!DNL Identity Service] versión 2.0. Las organizaciones con [!DNL Identity Service] versiones por debajo de 2.0 deben agregar este píxel a su contenedor de Audience Manager.

## Importar audiencias de Audience Manager a [!DNL Search, Social, & Commerce]

### Pasos para importar audiencias a [!DNL Search, Social, & Commerce]

El personal de [!DNL Adobe] realiza la mayoría o todos los pasos siguientes.

1. El equipo de cuenta de Adobe debe enviar una solicitud al equipo de operaciones de datos para configurar una integración entre [!DNL Search, Social, & Commerce] y Audience Manager. Incluya los nombres de los segmentos de Audience Manager que desea exportar a [!DNL Search, Social, & Commerce].

1. En Audience Manager, configure los destinos de [!DNL Search, Social, & Commerce]:

   1. Cree dos nuevos destinos: `[!UICONTROL Adobe Media Optimizer (HTTP)]` y `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] es un nombre anterior de [!DNL Search, Social, & Commerce].

   1. Especifique los segmentos para cada uno de los destinos.

      Con la opción [!UICONTROL Automatically map all current and future segments], todos los segmentos se asignan y sincronizan diariamente.

      La opción [!UICONTROL Manually map segments] le permite asignar manualmente los segmentos para sincronizarlos con el destino del lote (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). No es necesario asignar manualmente ningún segmento al destino HTTP.

1. En [!DNL Search, Social, & Commerce], el equipo de implementación [!DNL Search, Social, & Commerce] o un usuario con el rol de administrador de clientes de acceso directo deben iniciar la importación de [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Se requiere el Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID]) de la organización. El ID debe ser el mismo que se utilizó para la cuenta de Audience Manager de la organización.

### ¿Qué cambios resultan en Audience Manager?

Hay dos destinos [!DNL Search, Social, & Commerce] disponibles para la organización en Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Sincronización de datos

La importación inicial dura unas 24 horas. Después de la importación inicial, los datos se sincronizan en tiempo real, con un retraso de uno a dos segundos.

Los datos de abono a segmentos se envían únicamente después de que se produzca uno de los eventos siguientes:

* (Anunciantes con DSP):

   * El segmento se segmenta en un anuncio en pantalla de Adobe Advertising.

   * El segmento se agrega a [!DNL Adobe AdCloud Cross-Channel] destinos por lotes y en tiempo real dentro de la interfaz de usuario de Audience Manager.

* (Anunciantes con [!DNL Search, Social, & Commerce]):

   * El segmento se segmenta en un anuncio de búsqueda de Adobe Advertising.

   * El segmento se agrega al lote [!DNL Adobe Media Optimizer] y a los destinos HTTP dentro de la interfaz de usuario de Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Cómo DSP sincroniza los datos

DSP sincroniza los datos automáticamente usando [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante la sincronización, [!DNL ECID Service] llama a Adobe Advertising en [!DNL cm.everesttech.net]. Como Adobe Advertising es un dominio de confianza, las sincronizaciones de ID se realizan desde páginas principales en lugar de dentro de los iFrames de publicación de destino, como sucede con la mayoría de los socios de activación de terceros. Audience Manager identifica usuarios únicos por identificadores de dispositivo, usando el [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/es/docs/audience-manager/user-guide/reference/ids-in-aam), también llamado [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Cómo Search, Social y Commerce sincronizan los datos

Search, Social y Commerce sincronizan los datos automáticamente usando [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante la sincronización, [!DNL ECID Service] llama a Adobe Advertising en [!DNL cm.everesttech.net], que es un dominio de confianza que pertenece a Adobe Advertising. Audience Manager identifica usuarios únicos por identificadores de dispositivo, usando el [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/es/docs/audience-manager/user-guide/reference/ids-in-aam), también llamado [!DNL Device ID].

## Dónde encontrar los segmentos sincronizados

### En DSP

DSP organiza los nombres de los segmentos según la taxonomía de Audience Manager e incluye los recuentos de miembros de segmentos correspondientes en:

* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): en la ficha [!UICONTROL Adobe Segments] de la sección [!UICONTROL Audience Targeting].

* En [configuración de audiencia](/help/dsp/audiences/audience-settings.md): en la ficha [!UICONTROL Adobe Segments].

### En Advertising Creative

En [!DNL Creative], los segmentos están disponibles en la configuración de experiencia para los nodos de destino.

### En [!DNL Advertising Search, Social, & Commerce]

En [!DNL Search, Social, & Commerce], los segmentos están disponibles cuando crea una audiencia de [!DNL Google] con [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Para cada audiencia [!DNL Google] que cree, [!DNL Google] proporciona el tamaño de audiencia.

>[!MORELIKETHIS]
>
>* [Integraciones de Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
