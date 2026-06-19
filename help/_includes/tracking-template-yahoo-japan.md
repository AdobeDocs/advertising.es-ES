---
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# Campo de plantilla de seguimiento para [!DNL LY Ads] entidades

<!-- Search CRUD and bulk edit of LY Ads entity settings -->

**[!UICONTROL Tracking Template]:** (opcional): la plantilla de seguimiento o la dirección URL de seguimiento, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, y que también incrusta la dirección URL final de la página de aterrizaje/destino en un parámetro. Utilice el parámetro `!{lpurl}` para indicar la dirección URL de la página de aterrizaje. Ejemplo: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir una redirección.

Si lo desea, puede añadir redirecciones y seguimiento de terceros.

Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce prefieren automáticamente su propio código de redirección y seguimiento al guardar el registro.

>[!NOTE]
>
>* La plantilla de seguimiento en el nivel más granular anula los valores en todos los niveles superiores. Por ejemplo, si tanto la configuración de la cuenta como la configuración de la palabra clave incluyen un valor, se aplica el valor de la palabra clave.
>* Puede actualizar las plantillas de seguimiento en cualquier nivel sin volver a enviar los anuncios para su aprobación.
