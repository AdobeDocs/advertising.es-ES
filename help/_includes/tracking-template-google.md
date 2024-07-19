---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Campo Plantilla de seguimiento para entidades de Google Ads

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (opcional): la plantilla de seguimiento o la dirección URL de seguimiento, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, y también incrusta la dirección URL final de la página de aterrizaje/destino en un parámetro [!DNL ValueTrack]. Ejemplo: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir una redirección.

Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce prefieren automáticamente su propio código de redirección y seguimiento al guardar el registro.

* Para ver los parámetros admitidos para incrustar la dirección URL final, consulte la [[!DNL Google Ads] documentación de los [!DNL ValueTrack] formatos admitidos](https://support.google.com/google-ads/answer/6305348). (Vaya a los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección &quot;Parámetros disponibles [!DNL ValueTrack]&quot;).

* Opcionalmente, puede incluir parámetros de URL y cualquier parámetro personalizado definido para la campaña, separado por el símbolo et (&amp;), como {lpurl}?matchtype={matchtype}&amp;device={device}.

* Si lo desea, puede añadir redirecciones y seguimiento de terceros.

>[!NOTE]
>
>* Evite utilizar macros que no sustituyan los clics de fuentes que habilitan el seguimiento en paralelo. Si el anunciante debe utilizar macros, el equipo de cuenta de Adobe debe trabajar con Asistencia al cliente o con el equipo de implementación para agregarlas.
>* La plantilla de seguimiento en el nivel más granular anula los valores en todos los niveles superiores. Por ejemplo, si tanto la configuración de la cuenta como la configuración de la palabra clave incluyen un valor, se aplica el valor de la palabra clave.
>* Si actualiza una plantilla de seguimiento en el nivel de anuncio, vínculo de sitio o palabra clave, los anuncios relevantes se vuelven a enviar para su revisión. Puede actualizar las plantillas de seguimiento en los niveles de cuenta, campaña o grupo de publicidad sin volver a enviar los anuncios para su aprobación.
