---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Campo de plantilla de seguimiento para entidades de Microsoft Advertising

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Opcional; no disponible para todas las entidades) La plantilla de seguimiento o la URL de seguimiento, que especifica todas las redirecciones de dominios fuera de aterrizaje y los parámetros de seguimiento e incrusta también la URL final/de la página de aterrizaje en un parámetro. Ejemplo: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir una redirección.

Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload],&quot; Search, Social y Commerce añadirá automáticamente como prefijo su propio código de seguimiento y redirección al guardar el registro.

* Para ver los parámetros admitidos para incrustar la dirección URL final, consulte los [[!DNL Microsoft Advertising] documentación sobre los parámetros para indicar la dirección URL final](https://help.ads.microsoft.com/#apex/3/en/56799).

* Opcionalmente, puede incluir parámetros de URL y cualquier parámetro personalizado definido para la campaña, separado por el símbolo &amp;, como {lpurl}?matchtype={matchtype}&amp;device={device}.

* Si lo desea, puede añadir redirecciones y seguimiento de terceros.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* La plantilla de seguimiento en el nivel más granular anula los valores en todos los niveles superiores. Por ejemplo, si tanto la configuración de la cuenta como la configuración de la palabra clave incluyen un valor, se aplica el valor de la palabra clave.
>* Puede actualizar las plantillas de seguimiento en cualquier nivel sin volver a enviar los anuncios para su aprobación.
