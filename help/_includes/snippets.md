---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# Fragmentos

## Campo Plantilla de seguimiento para entidades de Google Ads {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

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

## Campo de plantilla de seguimiento para [!DNL Microsoft Advertising] entidades {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (opcional): la plantilla de seguimiento o la dirección URL de seguimiento, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, y que también incrusta la dirección URL final de la página de aterrizaje/destino en un parámetro. Ejemplo: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir una redirección.

Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce prefieren automáticamente su propio código de redirección y seguimiento al guardar el registro.

* Para ver los parámetros admitidos para incrustar la dirección URL final, consulte la [[!DNL Microsoft Advertising] documentación sobre parámetros para indicar la dirección URL final](https://help.ads.microsoft.com/#apex/3/en/56799).

* Opcionalmente, puede incluir parámetros de URL y cualquier parámetro personalizado definido para la campaña, separado por el símbolo et (&amp;), como {lpurl}?matchtype={matchtype}&amp;device={device}.

* Si lo desea, puede añadir redirecciones y seguimiento de terceros.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* La plantilla de seguimiento en el nivel más granular anula los valores en todos los niveles superiores. Por ejemplo, si tanto la configuración de la cuenta como la configuración de la palabra clave incluyen un valor, se aplica el valor de la palabra clave.
>* Puede actualizar las plantillas de seguimiento en cualquier nivel sin volver a enviar los anuncios para su aprobación.

## Texto y plantilla: nota que explica cómo insertar un parámetro dinámico {#inventory-feed-template-insert-dynamic-parameter}

Para insertar un nombre de columna o un grupo de modificadores como parámetro dinámico, haga clic en el campo de entrada y, a continuación, haga clic en un nombre de columna en la lista de columnas o en un [nombre de modificador](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) en la lista Modificadores. Para insertar la variable [!DNL Param1] o [!DNL Param2], escriba el valor `{param1:default text}` o `{param2:default text}`, donde &quot;texto predeterminado&quot; es el texto que se utiliza si la columna de parámetro en el archivo de fuente está vacía para una fila de anuncio.

## Plantilla de anuncio de texto: nota que explica cómo insertar un personalizador de publicidad {#inventory-feed-template-insert-ad-customizer}

Para insertar un personalizador de anuncios, use los siguientes formatos, donde `Default text` es un valor opcional que se debe insertar cuando el archivo de fuente no incluye un valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, como `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, como `{CUSTOMIZER.Discount:10%}`
