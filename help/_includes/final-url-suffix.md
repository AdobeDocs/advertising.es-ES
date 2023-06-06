---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---
# Definición final de sufijo de URL

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] y [!DNL Microsoft Advertising] solo cuentas; opcional) Cualquier parámetro que se adjunte al final de las direcciones URL finales para rastrear la información; incluya todos los parámetros que su empresa debe rastrear. Ejemplo:`param1=value1&param2=value2`

En las cuentas que utilizan el seguimiento de conversión de publicidad de Adobe, el sufijo debe incluir el identificador de clic ( ) de la red de publicidad`msclkid` para [!DNL Microsoft Advertising]; `gclid` para [!DNL Google Ads]).

Las cuentas con una integración de Adobe Analytics deben utilizar el parámetro s_kwcid. Si la cuenta tiene una implementación s_kwcid del lado del servidor, el parámetro se agrega automáticamente cuando un usuario hace clic en un anuncio; de lo contrario, debe agregarlo aquí manualmente. Consulte la [formatos de sufijo necesarios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y [formatos de sufijo necesarios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* El campo no se actualiza en [!UICONTROL Auto Upload] configuración de seguimiento.
>* Los sufijos finales de URL en los niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el editor de la red de anuncios.

