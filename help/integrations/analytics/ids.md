---
title: ID de Adobe Advertising usados por  [!DNL Analytics]
description: ID de Adobe Advertising usados por  [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# ID de Adobe Advertising usados por [!DNL Analytics]

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

*Aplicable a Advertising DSP y[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising usa dos ID para el seguimiento del rendimiento en el sitio: el *ID de EF* y el *ID de AMO*.

Cuando se produce una impresión de un anuncio, Adobe Advertising crea los valores de ID de AMO e ID de EF y los almacena. Cuando un visitante que ha visto un anuncio entra al sitio sin hacer clic en un anuncio, [!DNL Analytics] llama a estos valores desde Adobe Advertising a través del código de JavaScript [!DNL Analytics for Advertising]. Para el tráfico de visualización, [!DNL Analytics] genera un identificador suplementario (`SDID`), que se usa para unir el ID de EF y el ID de AMO en [!DNL Analytics]. Para el tráfico de clics, estos identificadores se incluyen en la dirección URL de la página de aterrizaje usando los parámetros de cadena de consulta `ef_id` y `s_kwcid` (para el ID de AMO).

Adobe Advertising distingue entre una entrada de pulsaciones o visualizaciones al sitio web según los siguientes criterios:

* Se registra una entrada de visualización cuando un usuario visita el sitio después de ver un anuncio, pero sin hacer clic en él. [!DNL Analytics] registra una visualización si se cumplen dos condiciones:

   * El visitante no tiene pulsaciones para un anuncio de [!DNL DSP] o [!DNL Search, Social, & Commerce] durante la [ventana retrospectiva de clics](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * El visitante ha visto al menos un anuncio de [!DNL DSP] durante la [ventana retrospectiva de impresiones](/help/integrations/analytics/prerequisites.md#lookback-a4adc). La última impresión se pasa como la visualización.

* Se captura una entrada de pulsación cuando un visitante del sitio hace clic en un anuncio antes de entrar en el sitio. [!DNL Analytics] registra una pulsación cuando se da cualquiera de las siguientes condiciones:

   * La dirección URL incluye un EF ID y un AMO ID, tal como Adobe Advertising lo agregó a la dirección URL de la página de aterrizaje.

   * La dirección URL no contiene códigos de seguimiento, pero el código JavaScript de Adobe Advertising detecta un clic en los últimos dos minutos.

![Integración de [!DNL Analytics] basada en la vista de Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: integración [!DNL Analytics] basada en la vista de Adobe Advertising*

![Integración de [!DNL Analytics] basada en URL de clic de Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Adobe Advertising hace clic en la integración [!DNL Analytics] basada en URL*

## ID de Adobe Advertising EF

{{$include /help/_includes/ef-id.md}}

### Formatos de ID de EF {#ef-id-formats}

{{$include /help/_includes/ef-id-formats.md}}

### El Dimension EF ID en [!DNL Analytics]

En [!DNL Analytics] informes, puede encontrar datos de EF ID buscando la dimensión [!UICONTROL EF ID] y usando la métrica [!UICONTROL EF ID Instance].

Los EF ID están sujetos al límite de 500 000 identificadores únicos en Analysis Workspace. Una vez que se alcanza el valor de 500.000, todos los nuevos códigos de seguimiento se incluyen en el título de un elemento de línea &quot;[!UICONTROL Low Traffic]&quot;. Debido a la posibilidad de que falte fidelidad en los informes, los EF ID no se clasifican y no debe utilizarlos para segmentos o informes en [!DNL Analytics].

## ID de Adobe Advertising AMO {#amo-id}

{{$include /help/_includes/amo-id.md}}

## Formatos de ID de AMO {#amo-id-formats}

{{$include /help/_includes/amo-id.md}}

### Formas de implementar el ID de AMO {#amo-id-implement}

El parámetro se añade a las direcciones URL de seguimiento de una de las siguientes maneras:

* (Recomendado) Cuando se implementa la función de inserción del lado del servidor.

   * Clientes de DSP: El servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final ve un anuncio en pantalla con el píxel de Adobe Advertising.

   * Clientes de Search, Social y Commerce:

      * Para las cuentas de [!DNL Google Ads] y [!DNL Microsoft Advertising] con la configuración [!UICONTROL Auto Upload] habilitada para la cuenta o campaña, el servidor de píxeles anexa automáticamente el parámetro s_kwcid a los sufijos de la página de aterrizaje cuando un usuario final hace clic en un anuncio con el píxel de Adobe Advertising.

      * Para otras redes de anuncios o cuentas de [!DNL Google Ads] y [!DNL Microsoft Advertising] con la configuración de [!UICONTROL Auto Upload] deshabilitada, agregue manualmente el parámetro a los [parámetros de datos anexados de nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que lo anexan a las direcciones URL base.

* Cuando la función de inserción del lado del servidor no está implementada:

   * Clientes de DSP: el [código JavaScript](javascript.md) registra automáticamente las pulsaciones y las visualizaciones. Cuando un explorador no admite cookies de terceros, puede seguir realizando el seguimiento de las conversiones basadas en clics para los siguientes tipos de anuncios:

      * Para las etiquetas de anuncio de [!DNL Flashtalking], inserte manualmente macros adicionales por &quot;[Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de anuncio](/help/integrations/analytics/macros-flashtalking.md)&quot;. **Nota:** Este procedimiento no es necesario si su organización tiene una asociación directa con [!DNL Flashtalking] y usa macros de paso de datos para realizar el seguimiento de los parámetros de seguimiento `s_kwcid` y `ef_id` según la documentación de soporte de [!DNL Flashtalking] en [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

      * Para las etiquetas de anuncio de [!DNL Google Campaign Manager 360], inserte manualmente macros adicionales por &quot;[Anexar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de anuncio](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;.

   * Clientes de Search, Social y Commerce:

      * Para los anuncios ([!DNL Google Ads] y [!DNL Microsoft Advertising]), agregue manualmente el parámetro de ID de AMO a los sufijos de la página de aterrizaje. Lo ideal es hacerlo a [nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, a menos que sea necesario un seguimiento diferente para los componentes de cuenta individuales.

      * Para anuncios en todas las demás redes de anuncios, agrega manualmente el parámetro de ID de AMO a tus [parámetros de datos anexados a nivel de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que lo anexan a tus URL base.

Para implementar la función de inserción del lado del servidor o para determinar la mejor opción para su empresa, hable con el equipo de cuenta de Adobe.

### DIMENSION de ID de AMO en [!DNL Analytics]

En los informes de Analytics, puede encontrar datos de ID de AMO buscando la dimensión [!UICONTROL AMO ID] y utilizando la métrica [!UICONTROL AMO ID Instances]. La dimensión [!UICONTROL AMO ID] aloja todos los valores de ID de AMO capturados, mientras que la métrica [!UICONTROL AMO ID Instances] indica la frecuencia con la que el sitio capturó un valor de ID de AMO. Por ejemplo, si se hizo clic cuatro veces en el mismo anuncio de búsqueda pero Analytics rastreó siete entradas de sitio, [!UICONTROL AMO ID Instances] sería siete (7) y [!UICONTROL Clicks] sería cuatro (4).

Para cualquier informe o auditoría dentro de [!DNL Analytics], la práctica recomendada es utilizar el ID de AMO junto con su instancia correspondiente. Para obtener más información, consulte &quot;[Validación de datos con clic para [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; en &quot;Variaciones de datos previstas entre [!DNL Analytics] y Adobe Advertising&quot;.

## Acerca de las clasificaciones de Analytics

En [!DNL Analytics], una [clasificación](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=es) es un fragmento de metadatos para un código de seguimiento determinado, como Cuenta, Campaña o Anuncio. Adobe Advertising clasifica los datos de Adobe Advertising sin procesar mediante clasificaciones para que pueda mostrarlos de diferentes maneras (por ejemplo, por tipo de anuncio o campaña) al generar informes. Las clasificaciones forman la base de los informes de Adobe Advertising en [!DNL Analytics] y se pueden usar con las métricas de AMO, como [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] y [!UICONTROL AMO Clicks], así como con eventos personalizados y estándar en el sitio, como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] y [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Variaciones de datos previstas entre [!DNL Analytics]  y Adobe Advertising](data-variances.md)
