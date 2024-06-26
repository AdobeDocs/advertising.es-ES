---
title: Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios
description: Obtenga información sobre cómo importar su [!DNL Adobe] Audiencias de en Advertising DSP y Buscar con Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios

Advertising DSP y [!DNL Advertising Search, Social, & Commerce] puede extraer metadatos, datos de jerarquía y datos de audiencia únicos de todos los anuncios o agencias [!DNL Adobe] audiencias<!-- segments or audiences? Standardize terms per AAM's docs -->, incluidos:

* Segmentos de Adobe Audience Manager

* Segmentos de Adobe Analytics publicados en Adobe Experience Cloud

* Segmentos que se crean con Adobe Experience Cloud [!DNL Audience Library]

* Segmentos creados en Adobe Experience Platform y enviados al Adobe Advertising mediante un Audience Manager

Para acceder a [!DNL Adobe] DSP Audiencias en el entorno de o [!DNL Creative]DSP , debe importar las audiencias en la interfaz de usuario de. Para acceder a [!DNL Adobe] audiencias en [!DNL Search, Social, & Commerce], debe importar las audiencias en [!DNL Search, Social, & Commerce].

## Requisitos previos

* El anunciante debe implementar [el [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) versión 2.0 o superior. El [!DNL Identity Service] proporciona un ID universal y persistente que identifica a los visitantes en todas las soluciones de Experience Cloud.

  La implementación incluye añadir el [!DNL Identity service] codifique a cada página web en los sitios del anunciante.

* La organización debe ser [habilitado para servicios de Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) y tenga un Experience Cloud [!DNL Organization ID] (anteriormente denominado [!DNL IMS org ID]).

  El [!UICONTROL Organization ID] permite a las organizaciones con varios productos de Adobe Experience Cloud compartir datos entre algunos de los productos.

* (Anunciantes con [!DNL Analytics]) El anunciante debe [implementar [!DNL Analytics] usando `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) versión 1.6.4 o superior.

* Los visitantes del sitio web del anunciante no incluyen un gran volumen de [!DNL Apple Safari] usuarios.

* (Se recomienda cuando el anunciante utiliza Audience Manager y [!DNL Analytics]) Para reducir las llamadas a cada página web, elimine el Audience Manager existente [!DNL Data Integration Library] código para la recopilación de datos y habilitar el reenvío del lado del servidor para cada [!DNL Analytics] grupo de informes en su lugar. Para obtener más información, consulte &quot;[Resumen del reenvío del lado del servidor](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Recomendado) Para tasas de coincidencia más altas, envíe solo datos del sitio web de origen al Adobe Advertising. Si el anunciante agrupa datos de terceros o datos sin conexión de un sistema de administración de la relación con los clientes, la fuga de datos puede reducir las tasas de coincidencia.

## Importación de audiencias de Audience Manager DSP a la

### DSP Pasos para importar audiencias a los grupos de trabajo

El [!DNL Adobe] Los equipos de operaciones de datos y cuentas de realizan los siguientes pasos.

1. El equipo de cuenta de Adobe debe configurar la opción de nivel de anunciante &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. El equipo de cuenta de Adobe debe enviar una solicitud al equipo de operaciones de datos para importar los segmentos de Audience Manager de la organización mediante la integración de la API nativa de Advertising DSP.

### ¿Qué cambios resultan en Audience Manager?

La API hace lo siguiente automáticamente:

* DSP Crea dos destinos de en el Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Asigna los dos destinos a todos los segmentos del Audience Manager, lo que permite que el Audience Manager DSP comparta los segmentos con la cuenta del anunciante de la aplicación asociada con el mismo Experience Cloud. [!DNL Organization ID] se usa para el Audience Manager.

  La organización puede, opcionalmente, eliminar segmentos innecesarios de los destinos dentro de Audience Manager.

* Agrega el siguiente píxel de sincronización de cookies de Exchange al contenedor de Audience Manager de la organización para mejorar el alcance de las campañas de los clientes:

   * Adobe AdCloud: 411 (Este píxel se convierte en estándar y automáticamente como parte de [!DNL Identity Service] versión 2.0. Organizaciones con [!DNL Identity Service] las versiones anteriores a 2.0 deben añadir este píxel a su contenedor de Audience Manager.

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

   El Experience Cloud de la organización [!DNL Organization ID] ([!DNL IMS org ID]) es obligatorio. El ID debe ser el mismo que se utilizó para la cuenta de Audience Manager de la organización.

### ¿Qué cambios resultan en Audience Manager?

Dos [!DNL Search, Social, & Commerce] Los destinos de están disponibles para la organización en Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Sincronización de datos

La importación inicial dura unas 24 horas. Después de la importación inicial, los datos se sincronizan en tiempo real, con un retraso de uno a dos segundos.

Los datos de abono a segmentos se envían únicamente después de que se produzca uno de los eventos siguientes:

* DSP (Anunciantes con el servicio de publicidad de):

   * El segmento se segmenta en un anuncio de visualización de Adobe Advertising.

   * El segmento se añade a [!DNL Adobe AdCloud Cross-Channel] destinos por lotes y en tiempo real dentro de la interfaz de usuario de Audience Manager.

* (Anunciantes con [!DNL Search, Social, & Commerce]):

   * El segmento se segmenta en un anuncio de búsqueda de Adobe Advertising.

   * El segmento se añade a [!DNL Adobe Media Optimizer] destinos por lotes y HTTP en la interfaz de usuario de Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSP Cómo se sincronizan los datos de la

DSP los datos automáticamente mediante el [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante la sincronización, la variable [!DNL ECID Service] Adobe Advertising de llamadas en [!DNL cm.everesttech.net]. Como Adobe Advertising es un dominio de confianza, las sincronizaciones de ID se realizan desde páginas principales en lugar de dentro de los iframes de publicación de destino, como sucede con la mayoría de los socios de activación de terceros. El Audience Manager identifica a los usuarios únicos por ID de dispositivo, utilizando [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), también denominado [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Cómo Search, Social y Commerce sincronizan los datos

Search, Social y Commerce sincronizan los datos automáticamente mediante [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante la sincronización, la variable [!DNL ECID Service] Adobe Advertising de llamadas en [!DNL cm.everesttech.net], que es un dominio de confianza que pertenece al Adobe Advertising. El Audience Manager identifica a los usuarios únicos por ID de dispositivo, utilizando [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), también denominado [!DNL Device ID].

## Dónde encontrar los segmentos sincronizados

### DSP En la

DSP Organiza los nombres de segmentos por la taxonomía de Audience Manager e incluye los recuentos de miembros de segmentos correspondientes en:

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
