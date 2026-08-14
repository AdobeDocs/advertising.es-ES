---
title: Solución de problemas de datos de Adobe Advertising en Customer Journey Analytics
description: Obtenga información sobre cómo solucionar y resolver problemas con los datos de Adobe Advertising en Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: b3b90fc7d453a9450f5858e47ae4c05243808a03
workflow-type: tm+mt
source-wordcount: 3033
ht-degree: 0%

---

# Solución de problemas de datos de Adobe Advertising en Customer Journey Analytics

A continuación se indican posibles problemas, sus posibles causas y soluciones.

## Lista de todos los síntomas potenciales

| Síntoma | Más información |
| ------- | ---------------- |
| No hay llamadas alloy() visibles en la pestaña de red del explorador | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[La extensión de WebSDK no se inicializa](#websdk-extension-doesn't-initialize)&quot; |
| Error de consola: no se ha definido la aleación | Consulte &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[La extensión de WebSDK no se inicializa](#websdk-extension-doesn't-initialize)&quot; |
| No interactuar ni recopilar solicitudes en edge.adobedc.net | Consulte &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[La extensión de WebSDK no se inicializa](#websdk-extension-doesn't-initialize)&quot; |
| Las solicitudes llegan al perímetro de, pero devuelven errores 400 o 500 | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Flujo de datos no configurado o mal configurado](#datastream-not-configured-or-misconfigured)&quot; |
| No aparecen datos en los informes de Adobe Analytics o Adobe Advertising | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Flujo de datos no configurado o mal configurado](#datastream-not-configured-or-misconfigured)&quot; |
| Error en la respuesta de red: &quot;no se encontró la secuencia de datos&quot; | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Flujo de datos no configurado o mal configurado](#datastream-not-configured-or-misconfigured)&quot; |
| El ID de visitante cambia entre páginas | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Problemas de identidad y ECID](#identity-and-ecid-issues)&quot; |
| Los segmentos de audiencia de Advertising no coinciden | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Problemas de identidad y ECID](#identity-and-ecid-issues)&quot; |
| El depurador muestra que no se cumplen las condiciones de las reglas | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Las reglas o eventos no se activan](#rules-or-events-aren't-firing)&quot; |
| La acción [!UICONTROL Send Event] nunca se ejecuta | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Las reglas o eventos no se activan](#rules-or-events-aren't-firing)&quot; |
| Los cambios realizados en [!DNL Tags] no se reflejan en el sitio activo | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Problemas de compilación y publicación de la biblioteca](#library-build-and-publishing-issues)&quot; |
| Se aplicó una actualización de extensión, pero el comportamiento antiguo persiste | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Problemas de compilación y publicación de la biblioteca](#library-build-and-publishing-issues)&quot; |
| La llamada de evento de envío `alloy()` se realizó correctamente (con una respuesta de 200), pero faltan datos de conversión de Adobe Advertising en los informes | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Problemas de validación de esquemas para campos de Advertising](#schema-validation-for-advertising-fields)&quot; |
| La carga XDM en Debugger no muestra ningún objeto `_experience.adcloud` | Consulte la sección &quot;[Problemas de instalación y configuración](#issues-installation-setup)&quot; > &quot;[Problemas de validación de esquemas para campos de Advertising](#schema-validation-for-advertising-fields)&quot; |
| No se han registrado conversiones de visualizaciones o clics para la página web | Consulte la sección &quot;[Problemas de configuración de la extensión de Advertising](#advertising-extension-setup-issues)&quot; |
| `_experience.adcloud` no aparece en la carga del Modelo de datos de experiencia (XDM) para clics | Consulte la sección &quot;[Problemas de configuración de la extensión de Advertising](#advertising-extension-setup-issues)&quot; |
| Las conversiones se confirman en una herramienta de depuración, pero no aparecen en los informes de Adobe Advertising | Consulte la sección &quot;[Problemas de configuración de la extensión de Advertising](#advertising-extension-setup-issues)&quot; |

## Problemas de instalación y configuración {#issues-installation-setup}

### La extensión WebSDK no inicializa {#websdk-extension-doesn&#39;t-initialize}

Síntomas:

* No hay llamadas alloy() visibles en la pestaña de red del explorador
* Error de consola: no se ha definido la aleación
* No interactuar ni recopilar solicitudes en edge.adobedc.net

| Causa | Fix |
| ----- | --- |
| Biblioteca no publicada o en estado de borrador | Vaya a [Flujo de publicación](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) y asegúrese de que la biblioteca que contiene la extensión WebSDK está en el estado aprobado/publicado. |
| Falta el código incrustado o el entorno es incorrecto | Compruebe que el código incrustado de [!DNL Tags] en la página web hace referencia al entorno correcto (Dev/Stage/Prod). Busque el entorno en la etiqueta `<head>` para la etiqueta de script `//assets.adobedtm.com/...`. |
| Conflicto de carga asíncrona frente a sincrónica | Asegúrese de que solo hay un código incrustado de [!DNL Tags] por página web. Los códigos incrustados duplicados causan condiciones de carrera. |
| Bloqueo de la política de seguridad de contenido (CSP) | Agregue `edge.adobedc.net` `and assets.adobedtm.com` a sus directivas CSP `connect-src` y `script-src`. |

### Flujo de datos no configurado o mal configurado {#datastream-not-configured-or-misconfigured}

Síntomas:

* Las solicitudes llegan al perímetro de, pero devuelven errores 400 o 500
* No aparecen datos en los informes de Adobe Analytics o Adobe Advertising<!-- It's not useful to organize this info by cause, not symptom -->
* Error en la respuesta de red: &quot;no se encontró la secuencia de datos&quot;

| Causa | Fix |
| ----- | --- |
| Falta el ID de secuencia de datos para la propiedad de etiqueta o es incorrecto. | <ol><li>En [!DNL Tags], abra los [ajustes de configuración de secuencia de datos](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) de su propiedad de etiquetas.</li><li>Confirme que el campo [!UICONTROL Datastream] señala a la secuencia de datos correcta para cada entorno (desarrollo, ensayo y producción), así como al esquema y al conjunto de datos correctos.<br><br>Cada entorno debe tener su propia secuencia de datos a menos que comparta explícitamente una secuencia de datos en los tres entornos.</li></ol> |
| Los servicios de flujo de datos no están habilitados para la propiedad de etiqueta. | [Abra la configuración del flujo de datos](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) y asegúrese de que los siguientes servicios estén habilitados:<ul><li>Adobe Advertising (para conversión/sincronización de audiencia)</li><li>Adobe Experience Platform (para la ingesta de perfiles)</li></ul> |
| Discordancia de zona protegida | Asegúrese de que la secuencia de datos pertenezca a la misma zona protegida de Adobe Experience Platform que el esquema y el conjunto de datos. Un error común es crear una secuencia de datos en la zona protegida de producción, pero señalar esquemas a la zona protegida de desarrollo. |

### Problemas de identidad y ECID {#identity-and-ecid-issues}

Síntomas:

* El ID de visitante cambia entre páginas
* Los segmentos de audiencia de Advertising no coinciden

| Causa | Fix |
| ----- | --- |
| Las cookies de terceros están bloqueadas | Migre a la recopilación de datos CNAME de origen configurando un dominio de origen en la configuración de Edge del conjunto de datos. |
| `idMigrationEnabled` se ha establecido en `false` mientras que una cookie `s_ecid` heredada está presente | Establezca `idMigrationEnabled: true` en la configuración base de WebSDK para migrar el ECID existente desde las cookies `s_ecid` o `AMCV_`. |

### Las reglas o los eventos no se activan {#rules-or-events-aren&#39;t-fire}

Síntomas:

* El depurador muestra que no se cumplen las condiciones de las reglas
* La acción [!UICONTROL Send Event] nunca se ejecuta

Compruebe lo siguiente:

* La regla se guarda e incluye en la compilación de biblioteca activa.
* El tipo de evento coincide con el comportamiento real de la página (como [!UICONTROL Library Loaded] frente a [!UICONTROL DOM Ready] frente a [!UICONTROL Window Loaded]).
* Las condiciones de la regla no son demasiado restrictivas. Realice la prueba eliminando temporalmente las condiciones para aislar el problema.
* El orden de las reglas es correcto. Si varias reglas comparten el mismo evento, compruebe el orden de las reglas.
* Ningún error de JavaScript anterior en la página detiene la ejecución. Compruebe si hay excepciones no detectadas en la consola del explorador.

### Problemas de compilación y publicación de bibliotecas {#library-build-and-publishing-issues}

Síntomas:

* Los cambios realizados en [!DNL Tags] no se reflejan en el sitio activo
* Se aplicó una actualización de extensión, pero el comportamiento antiguo persiste

| Causa | Fix |
| ----- | --- |
| Los cambios no se han añadido a una biblioteca | En [!UICONTROL Publishing Flow], confirme que los cambios se agregaron a una biblioteca en el entorno de desarrollo. Vaya a [!UICONTROL Libraries], abra la biblioteca de trabajo, seleccione **Agregar todos los recursos modificados** y, a continuación, seleccione **Guardar y crear**. |
| El explorador está almacenando en caché una biblioteca antigua | Realice una actualización rápida (Ctrl+Mayús+R o Cmd+Mayús+R) o abra la página en una ventana de incógnito o privada. Borre la memoria caché del explorador por completo si el problema persiste. |
| El código incrustado es para el entorno incorrecto | Confirme que el código incrustado de en la página es el código incrustado de producción si está probando el comportamiento de producción. |
| La compilación de la biblioteca falló silenciosamente | Vaya a [!UICONTROL Publishing Flow] y compruebe si la biblioteca muestra un estado [!UICONTROL Build Failed]. Abra la biblioteca y revise el registro de generación: las causas comunes son configuraciones de regla no válidas o conflictos de versión de extensión. |

### Problemas de validación de esquemas para campos de Advertising {#schema-validation-for-advertising-fields}

Síntomas:

* La llamada de evento de envío `alloy()` se realizó correctamente (con una respuesta de 200), pero faltan datos de conversión de Adobe Advertising en los informes
* La carga XDM en Debugger no muestra ningún objeto `_experience.adcloud`

#### Paso 1: Confirme que el grupo de campos [!UICONTROL Advertising] se agrega al esquema

1. Vaya a Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas].
1. Abra el esquema utilizado por el conjunto de datos.
1. En el panel [!UICONTROL Field Groups], confirme que aparece **Adobe Advertising Cloud ExperienceEvent Full Extension**.
1. Si falta, selecciona **Agregar**, busca **Adobe Advertising Cloud**, selecciona **Extensión completa de Adobe Advertising Cloud ExperienceEvent** y, a continuación, selecciona **Guardar**.

>[!NOTE]
>Volver a publicar su biblioteca [!DNL Tags] no es necesario solo para los cambios de esquema, pero debe volver a asignar el elemento de datos XDM en [!DNL Tags] si se agregaron nuevos campos.

#### Paso 2: Compruebe que los campos de Adobe Advertising requeridos estén presentes en el esquema en `_experience.adcloud.conversionDetails`

| Ruta de campo | Tipo | Descripción |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | Cadena | Asigna la conversión al clic del anuncio de origen. Rellenado desde el parámetro de consulta `s_kwcid` en la dirección URL de la página de aterrizaje. |
| `_experience.adcloud.conversionDetails.trackingIdentity` | Cadena | Almacena la identidad única y otros detalles del evento de conversión de pulsaciones o vistas rastreadas. Rellenado desde el parámetro de consulta `ef_id` en la dirección URL de la página de aterrizaje. |

Si falta alguno de los campos, confirme que el grupo de campos **Adobe Advertising Cloud ExperienceEvent Full Extension** se ha guardado en el esquema y, a continuación, actualice el editor de esquemas.

#### Paso 3: Confirme que la dirección URL de la página de aterrizaje incluye parámetros de consulta

En la pulsación de un anuncio, la dirección URL de la página de aterrizaje debe contener ambos parámetros de consulta, por ejemplo:

`https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`

| Falta un parámetro | Causa probable |
| ----- | --- |
| `s_kwcid` | El etiquetado automático no está habilitado en la configuración de la campaña de Adobe Advertising Search o DSP. |
| `ef_id` | La dirección URL de la página de aterrizaje no utiliza una redirección rastreada de Adobe Advertising o la adición de EF ID no está habilitada en la configuración de la campaña. |

#### Paso 4: Validar la carga útil XDM saliente

Abra AEP Debugger o la ficha [!UICONTROL Network] del explorador, filtre `edge.adobedc.net` e inspeccione el cuerpo de la solicitud de interacción. Una carga útil de pulsación válida tiene un aspecto similar al siguiente:

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

Si `trackingCode` o `trackingIdentity` están vacíos o faltan:

* El parámetro de consulta no estaba presente en la página cuando se activó la regla. Compruebe la dirección URL y el tiempo de evento de la regla.
* Falta el grupo de campos en el esquema. Vuelva a visitar los pasos de esquema anteriores.

## [!UICONTROL Advertising] problemas de configuración de extensión {#advertising-extension-setup-issues}

Síntomas:

* No se registran conversiones de visualizaciones o clics para la página web.

  Para comprobar si se han registrado las conversiones:

  1. Abra la página web con `ef_id=test&s_kwcid=test` anexado a la dirección URL.
  1. Abra la herramienta de inspección de código del explorador (denominada con frecuencia [!DNL Inspect]), abra la pestaña [!DNL Network] y busque una llamada de interacción para event_type=&quot;advertising.enrichment_ct&quot; desde Adobe Experience Platform.
  1. En la interfaz de recopilación de datos, [abra la definición de esquema](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) de los datos del sitio web que desea recopilar y confirme que `xdm->_experience->adcloud->conversionDetails->trackingCode` y `trackingIdentities` contienen `ef_id` y `s_kwcid`.

* `_experience.adcloud` no aparece en la carga del Modelo de datos de experiencia (XDM) para clics.

* Las conversiones se confirman en una herramienta de depuración, pero no aparecen en los informes de Adobe Advertising

| Causa | Fix |
| ----- | --- |
| El servicio `Adobe Advertising` no está habilitado para la secuencia de datos | <ol><li>En [!DNL Tags], abra los [ajustes de configuración de secuencia de datos](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) de su propiedad de etiquetas.</li><li>Habilite los siguientes servicios y guarde la configuración:<ul><li>Adobe Advertising (para conversión/sincronización de audiencia)</li><li>Adobe Experience Platform (para la ingesta de perfiles)</li></ul></ol> |
| El componente `Adobe Advertising` no está habilitado para la extensión [!UICONTROL WebSDK] | El componente `Adobe Advertising` de la extensión WebSDK está deshabilitado de forma predeterminada y debe habilitarse explícitamente antes de que funcione cualquier seguimiento de pulsaciones o visualizaciones de Adobe Advertising, independientemente de cómo se configuren el esquema o las reglas XDM.<ol><li>En [!DNL Tags], abra las [opciones de generación de la propiedad en los ajustes de configuración de Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components).</li><li>Habilite el componente **Advertising** y guarde la configuración.</li><li>Vuelva a compilar y publicar la biblioteca.</li></ol> |
| Solo se registran las conversiones de pulsaciones; las conversiones de visualizaciones nunca aparecen | Este es el comportamiento predeterminado esperado. Una vez habilitado el componente `Adobe Advertising`, el seguimiento de clics se activa automáticamente mediante los parámetros de consulta de URL `s_kwcid` y `ef_id`. El seguimiento de visualizaciones está deshabilitado de forma predeterminada y requiere una configuración adicional; consulte la fila siguiente. |
| El seguimiento de visualizaciones no está habilitado o configurado | <ol><li>Habilitar el servicio de Adobe Advertising para el conjunto de datos</li><ol><li>Vaya a [!UICONTROL Data Collection] > [!UICONTROL Datastreams] en Adobe Experience Platform y abra la secuencia de datos utilizada por su propiedad de [!DNL Tags].</li><li>Seleccione **Agregar servicio**, seleccione **Adobe Advertising** y **Adobe Experience Platform**, y después seleccione **Guardar**.</li></ol><li>Configuración de anunciantes en Adobe Advertising DSP</li><ol><li>En [!DNL Tags], vaya a [!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure].</li><li>En la sección [!UICONTROL Advertiser], seleccione un anunciante del menú desplegable y actívelo. Para configurar varios anunciantes, seleccione **Agregar anunciante**.</li></ol><li>Compruebe que se están activando los píxeles de conversión de visualización</li><ol><li>En AEP Debugger, confirme que la llamada de interacción incluye `stitchId` en el campo `xdm.query`.</li><li>Confirme en la ficha del explorador [!UICONTROL Network] que se ha activado un evento de tipo `advertising.enrichment` que incluye `stitchId` en `xdm.query`.</li></ol></ol> Las conversiones de visualización solo se activan cada 30 minutos, independientemente del número de visitas. Si no ve una llamada de interacción, borre la caché del explorador e inténtelo de nuevo. |
| (Si no hay eventos de visualización en Experience Platform después de que se active la llamada de interacción de visualización) Se escribió el anunciante manualmente en lugar de seleccionarlo en la lista desplegable | Vuelva a seleccionar el anunciante de la lista desplegable [!UICONTROL Advertiser] en lugar de introducirlo manualmente. |
| (Si no hay eventos de visualización en Experience Platform después de que se active la llamada de interacción de visualización) No se envía ningún ID de anunciante con la llamada de interacción de visualización | Confirme que hay un anunciante configurado y habilitado en la sección [!UICONTROL Advertiser] de la configuración de la extensión del SDK web y, a continuación, vuelva a generar y publicar la biblioteca. |

Antes de abrir un vale de soporte para [!UICONTROL Advertising] problemas de configuración de la extensión, compruebe lo siguiente:

* Los servicios **Adobe Advertising** y **Adobe Experience Platform** se han agregado al conjunto de datos.
* El componente **Adobe Advertising** está habilitado en la configuración de la extensión WebSDK.
* La biblioteca se reconstruyó y volvió a publicarse después de habilitar el componente.
* Para el seguimiento de clics, la dirección URL de la página de aterrizaje contiene `s_kwcid` y `ef_id` en los clics de anuncios.
* Para el seguimiento de visualizaciones, se configura un anunciante en Adobe Advertising DSP con el ID del anunciante correcto.
* La extensión WebSDK es la versión 2.36.0 o posterior.

## Informes de problemas

### Informes de resumen

| Síntoma | Verificación y resolución |
| ----- | --- |
| No hay datos de informes de resumen disponibles en Customer Journey Analytics para Advertising DSP o Advertising Search, Social y Commerce. | <ol><li>Confirme que Customer Journey Analytics Workspace hace referencia a la vista de datos correcta.</li><li>Confirme que la fuente de Adobe Advertising a Customer Journey Analytics esté habilitada. Consulte con el equipo de cuenta de Adobe.</li><li>Confirme que el conjunto de datos de dimensión, clasificación o búsqueda de Adobe Advertising y el conjunto de datos de resumen están incluidos en la conexión de Customer Journey Analytics.</li><li>Confirme que las dimensiones y las métricas de resumen de Adobe Advertising se incluyen en la vista de datos de Customer Journey Analytics.</li></ol>Si verifica toda la configuración anterior pero sigue sin ver los datos de resumen, abra un [ticket de asistencia](https://experienceleague.adobe.com/home?support-tab=home#support) para su organización. |
| Los datos del informe de resumen están disponibles en Customer Journey Analytics para el anunciante 1, pero no en Advertiser 2. | <ol><li>Confirme que la fuente de Adobe Advertising a Customer Journey Analytics esté habilitada para Anunciante 2. Consulte con el equipo de cuenta de Adobe.</li><li>Confirme que la configuración &quot;[!UICONTROL Backfill all existing data]&quot; esté habilitada para sus tres conjuntos de datos (métricas de dimensión, clasificación, búsqueda, resumen y evento) en su conexión de Customer Journey Analytics.</li></ol>Si verifica todas las condiciones anteriores pero sigue sin ver los datos de resumen, abra un [ticket de asistencia](https://experienceleague.adobe.com/home?support-tab=home#support) para su organización. |
| (Usuarios de Search, Social y Commerce) Los datos de informes de resumen están disponibles en Customer Journey Analytics para una cuenta de [!DNL Google Ads], [!DNL Meta Ads] o [!DNL Microsoft Advertising], pero no para otra cuenta. | Compruebe que la fuente de Adobe Advertising a Customer Journey Analytics esté habilitada para la cuenta específica de red de publicidad. Consulte con el equipo de cuenta de Adobe.<br><br>Si la fuente está habilitada para una cuenta pero aún no ve datos de resumen, abra un [ticket de asistencia](https://experienceleague.adobe.com/home?support-tab=home#support) para su organización. Incluir [!UICONTROL Account ID] para la cuenta de red de publicidad. |
| Los datos de informes de resumen de Customer Journey Analytics Workspace son diferentes de los datos de Advertising DSP o Advertising Search, Social y Commerce, o faltan datos de resumen para algunas campañas y entidades de campaña. | <ol><li>Confirme que está usando los mismos intervalos de fechas tanto en [!DNL Workspace] como en el informe de Adobe Advertising.</li><li>Confirme que los filtros y segmentos aplicados en [!DNL Workspace] y en el informe de Adobe Advertising no están causando diferencias en los datos.</li><li>Confirme que [!UICONTROL Time Zone] de la vista de datos de Customer Journey Analytics coincide con [!UICONTROL Default Timezone] de su [cuenta de Advertising DSP](/help/dsp/admin/user-own-profile-edit.md).</li><li>Confirme que la configuración &quot;[!UICONTROL Backfill all existing data]&quot; esté habilitada para sus tres conjuntos de datos (métricas de dimensión, clasificación, búsqueda, resumen y evento) en su conexión de Customer Journey Analytics.</li></ol>Si está seguro de una discrepancia en los datos, abra un [vale de soporte](https://experienceleague.adobe.com/home?support-tab=home#support) para su organización. Incluir [!UICONTROL Account ID] para la cuenta de red de publicidad. Para mostrar evidencia de la discrepancia, incluya capturas de pantalla y hojas de cálculo. El equipo de cuenta de Adobe puede corregir de forma retroactiva la fuente de datos para resolver la discrepancia si es necesario. |

### Informes de nivel de evento

| Síntoma | Verificación y resolución |
| ----- | --- |
| Los datos de conversión (como `Page Views`) no están disponibles para una dimensión de informes (como `Campaign`) en Customer Journey Analytics Workspace. | Compruebe lo siguiente, empezando por los elementos con menos barreras de verificación:<ul><li>Confirme que está utilizando la vista de datos correcta.</li><li>Confirme que las métricas de conversión aplicables son eventos web/en línea que Adobe Advertising puede atribuir a dimensiones.</li><li>Confirme que Adobe Advertising está realizando un seguimiento de las pulsaciones y las visualizaciones en el sitio correspondiente.</li><li>En la conexión de Customer Journey Analytics para el conjunto de datos de clasificaciones, confirme que los valores de la configuración de [!DNL Key] y [!DNL Matching Key] son correctos: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event.experience.adcloud.conversionDetails.trackingCode).</li><li>Confirme que el servicio [!DNL Adobe Advertising] se agrega a la secuencia de datos de Adobe Experience Platform, que el esquema asignado para la secuencia de datos es `XDM ExperienceEvent Schema` y que el grupo de campos `Adobe Advertising Cloud ExperienceEvent Full Extension` se agrega al esquema `XDM ExperienceEvent`.</li><li>Confirme que la configuración de Adobe Advertising es correcta en la extensión y publicación del SDK web.</li></ul>Si verifica toda la configuración anterior pero sigue sin ver los datos de conversión, abra un [ticket de asistencia](https://experienceleague.adobe.com/home?support-tab=home#support) para su organización. Incluir [!UICONTROL Account ID] para la cuenta de red de publicidad. |

<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

## Herramientas de validación y depuración

### Adobe Experience Platform Debugger

Instale la extensión [!DNL Adobe Experience Platform Debugger] para [!DNL Chrome]. Proporciona lo siguiente:

* Una vista en tiempo real de todas las llamadas al SDK web `alloy()`
* Validación de entorno e ID de flujo de datos
* Inspección de carga útil XDM
* Detalles de solicitud y respuesta de Edge Network

Comprobaciones de claves en Debugger:

| Ficha | Qué comprobar |
| ----- | --- |
| [!UICONTROL Summary] | Confirma que se ha detectado el SDK web y muestra la versión instalada. |
| [!UICONTROL AEP Web SDK] | Muestra cada evento activado, la carga útil XDM completa y la respuesta de Edge. |
| [!UICONTROL Adobe Advertising] | Confirma la captura del ID de AMO y la llamada de interacción XDM con el tipo de evento `advertising.enrichment`. |

### Pestaña Red del explorador

Filtre por `edge.adobedc.net` para inspeccionar las solicitudes perimetrales sin procesar:

* URL de solicitud: `https://[org-id].data.adobedc.net/ee/v2/interact`
* Método: `POST`
* Estado: `200` (en buen estado), `400` (carga útil incorrecta) o `500` (error del servidor o de la secuencia de datos)

Compruebe la carga útil de la solicitud para:

* El `dataStreamId` correcto
* La presencia de un objeto `xdm` con los campos esperados
* Un `identityMap` con el ECID completado

### Validación de consola

Compruebe la versión instalada del SDK web:

```js
window.alloy.version
```

Almacenar en déclencheur manualmente un evento de prueba:

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## Lista de comprobación de referencia rápida

Compruebe lo siguiente antes de abrir un ticket de asistencia:

* La extensión WebSDK está en la versión más reciente.
* La biblioteca se publica y el código incrustado es correcto para el entorno.
* El ID de la secuencia de datos está configurado correctamente para el desarrollo, el ensayo y la producción.
* Todos los servicios de flujo de datos necesarios están habilitados.
* El componente [!UICONTROL Advertising] está habilitado en la configuración de la extensión WebSDK y se ha configurado un ID de anunciante de DSP.
* El esquema XDM incluye el grupo de campos [!UICONTROL Advertising].
* La regla [!UICONTROL Send Event] incluye un mapa de identidad y se activa en el evento correcto.
* Ninguna CSP o configuración de privacidad del explorador bloquea las solicitudes perimetrales.
* AEP Debugger confirma que los eventos están llegando al límite de.
* Ningún error de JavaScript en la consola del explorador detiene la ejecución.
* El grupo de campos **Extensión completa de ExperienceEvent de Adobe Advertising Cloud** se agrega al esquema.
* `_experience.adcloud.conversionDetails.trackingCode` está presente en el esquema.
* `_experience.adcloud.conversionDetails.trackingIdentity` está presente en el esquema.
* La dirección URL de la página de aterrizaje contiene `s_kwcid` y `ef_id` al hacer clic.
* AEP Debugger confirma que `conversionDetails` se ha rellenado en la carga útil saliente.

## Cuándo escalar

Póngase en contacto con el equipo de cuenta de Adobe o con el equipo de ingeniería si:

* Las solicitudes de Edge devuelven errores persistentes `500` después de la validación de la secuencia de datos.
* Las conversiones de [!UICONTROL Advertising] se han confirmado en Debugger, pero no aparecen en los informes después de 24 a 48 horas.
* Una actualización de la versión de WebSDK introduce una regresión que no estaba presente en la versión anterior. Incluya los números de versión específicos en el ticket de asistencia.

>[!MORELIKETHIS]
>
>* [Información general](overview.md)
>* [ID de Adobe Advertising usados por [!DNL Customer Journey Analytics]](ids.md)
>* [Requisitos previos](prerequisites.md)
>* [Configurar la recopilación de datos, la transferencia de datos y la creación de informes](set-up.md)
>* [Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics](advertising-data-in-cja.md)
>* (Usuarios de Adobe Analytics) [Recopilar datos históricos de ID de AMO e ID de EF para usarlos en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
