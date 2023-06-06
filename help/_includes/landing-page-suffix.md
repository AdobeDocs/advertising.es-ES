---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---
# Campo Sufijo de página de aterrizaje en la configuración de cuentas de GGL y MS, configuración de campañas y algunas configuraciones de anuncios

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] y [!DNL Microsoft Advertising] solo cuentas; opcional) Cualquier parámetro que se adjunte al final de las direcciones URL finales para rastrear la información; incluya todos los parámetros que su empresa debe rastrear. Ejemplo: `param1=value1&param2=value2`

Las cuentas que utilizan el seguimiento de conversión de publicidad Adobe deben incluir el identificador de clic ( ) de la red de publicidad`gclid` para [!DNL Google Ads] o `msclkid` para [!DNL Microsoft Advertising]) en el sufijo.

Las cuentas con una integración de Adobe Analytics deben utilizar el parámetro s_kwcid. Si la cuenta tiene una implementación s_kwcid del lado del servidor, el parámetro se agrega automáticamente cuando un usuario hace clic en un anuncio; de lo contrario, debe agregarlo aquí manualmente. Consulte la [formatos de sufijo necesarios para Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y [formatos de sufijo necesarios para Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Notas:**

* El campo no se actualiza en [!UICONTROL Auto Upload] configuración de seguimiento.

* Los sufijos de la página de aterrizaje en niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el editor de la red de anuncios.
