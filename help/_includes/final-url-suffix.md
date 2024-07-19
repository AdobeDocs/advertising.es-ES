---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Definición final de sufijo de URL

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas solamente; opcional) Cualquier parámetro que se anexe al final de las direcciones URL finales para realizar el seguimiento de la información; incluya todos los parámetros que su empresa debe seguir. Ejemplo:`param1=value1&param2=value2`

En las cuentas que utilizan el seguimiento de conversión de Adobe Advertising, el sufijo debe incluir el identificador de clic (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para [!DNL Google Ads]) de la red publicitaria.

Las cuentas con una integración de Adobe Analytics deben usar el parámetro [AMO ID](/help/integrations/analytics/ids.md). Si la cuenta tiene una implementación de AMO ID del lado del servidor, el parámetro se añade automáticamente cuando un usuario hace clic en un anuncio; de lo contrario, debe añadirlo aquí de forma manual. Vea los [formatos de sufijo necesarios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y [formatos de sufijo necesarios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* La configuración de seguimiento [!UICONTROL Auto Upload] no actualiza este campo.
>* Los sufijos finales de URL en los niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el editor de la red de anuncios.
