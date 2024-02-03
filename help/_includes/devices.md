---
source-git-commit: 24aa1afe9611ca6ae46795c9bca2964e1d9c4f97
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---
# Campo Dispositivos en la configuración de campaña y grupo de anuncios de GL y MS

**[!UICONTROL Devices]:** (Opcional; no disponible para [!DNL Google Ads] campañas de rendimiento máximo o [!DNL Microsoft Advertising] (anuncios de vídeo o CTV) Configure ajustes de oferta para diferentes tipos de dispositivos, como porcentajes de la oferta a nivel de palabra clave. Por ejemplo, si la oferta a nivel de palabra clave es 1 USD y el ajuste de oferta para smartphones es del 50 %, la oferta para smartphones es de 1,50 USD. De forma predeterminada, no se introduce ningún valor (ajuste de oferta=0) y todos los dispositivos se ofertan en el nivel de palabra clave.

Para [!DNL Google Ads]Sin embargo, los porcentajes válidos pueden incluir -100 para smartphones y tabletas (para no pujar por el tipo de dispositivo) y de -90 a 900 para todos los tipos de dispositivos.

Para [!DNL Microsoft Advertising], los porcentajes válidos pueden incluir:

* Smartphones y tablets: -100 (para no pujar por el tipo de dispositivo) y de -90 a 900
* Escritorio: de 0 a 900

>[!NOTE]
>* La configuración del nivel de grupo de anuncios anula la configuración del nivel de campaña. Sin embargo, si excluye un dispositivo en el nivel de campaña, no puede anular la exclusión en el nivel de grupo de anuncios.
>* Si asigna esta campaña a un portafolio optimizado estándar, Search, Social y Commerce determinan automáticamente la oferta de nivel de palabra clave base para ayudar al portafolio a cumplir su objetivo. A continuación, la red de publicidad ajusta la oferta según se especifica para distintos tipos de dispositivos.
>* (Para todas las campañas/grupos de anuncios excepto para [!DNL Microsoft Advertising] grupos de anuncios en la red de audiencias) Si asigna esta campaña a un portafolios optimizado estándar configurado para &quot;[!UICONTROL Auto-optimize Bid Adjustment Values],&quot; entonces la capacidad de optimización cambia los ajustes de oferta de dispositivo especificados en el nivel de grupo de anuncios, siempre que el valor ideal que calcula se encuentre dentro de los valores mínimo y máximo especificados en la configuración del portafolio y el grupo de anuncios no excluya las ofertas para el tipo de dispositivo.
