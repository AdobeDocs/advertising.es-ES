---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---
# Campo Sufijo de página de aterrizaje en la configuración de cuentas de GGL y MS, configuración de campañas y algunas configuraciones de anuncios

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas solamente; opcional) Cualquier parámetro que se anexe al final de las direcciones URL finales para realizar el seguimiento de la información; incluya todos los parámetros que su empresa debe seguir. Ejemplo: `param1=value1&param2=value2`

Las cuentas que usan el seguimiento de conversión de Adobe Advertising deben incluir el identificador de clic (`gclid` para [!DNL Google Ads] o `msclkid` para [!DNL Microsoft Advertising]) de la red de publicidad en el sufijo.

Las cuentas con una integración de Adobe Analytics deben utilizar el parámetro s_kwcid. Si la cuenta tiene una implementación s_kwcid del lado del servidor, el parámetro se agrega automáticamente cuando un usuario hace clic en un anuncio; de lo contrario, debe agregarlo aquí manualmente. Vea los [formatos de sufijos necesarios para Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y [formatos de sufijos necesarios para Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Notas:**

* La configuración de seguimiento [!UICONTROL Auto Upload] no actualiza este campo.

* Los sufijos de la página de aterrizaje en niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el editor de la red de anuncios.
