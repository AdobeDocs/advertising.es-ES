---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---
# Campo Carga automática en la configuración de cuenta y campaña

**[!UICONTROL Auto Upload]:** (Para campañas sincronizadas con [!UICONTROL EF Redirect] solo) Carga automáticamente lo siguiente en la red de publicidad la próxima vez que Search, Social y Commerce se sincronice con él: (a) Parámetros de seguimiento de Search, Social y Commerce para rastrear plantillas y los mismos parámetros anexados a las URL finales o (b) Nuevas URL de destino incrustadas con el código de seguimiento de Search, Social y Commerce. Para anunciantes con una [Integración de Adobe Advertising y Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) y una configuración de ID de AMO del lado del servidor (s_kwcid), la carga también incluye [Parámetros de ID de AMO](/help/integrations/analytics/ids.md#amo-id) para su [!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas. La configuración predeterminada en el nivel de cuenta se hereda de la configuración de seguimiento del anunciante. Puede anular la configuración de nivel de cuenta en el nivel de campaña.

**Nota:** Las direcciones URL de seguimiento se actualizan a diario solo para las entidades que no están sincronizadas (es decir, las nuevas entidades que se añadieron y las entidades existentes cuyas propiedades han cambiado). Por lo tanto, si cambia esta configuración de deshabilitada a habilitada para un anunciante, cuenta o campaña existente, las direcciones URL de seguimiento no se actualizan para las entidades existentes que ya están sincronizadas. Para agregar el seguimiento a las direcciones URL de entidades sincronizadas existentes, póngase en contacto con el equipo de cuenta de Adobe y solicite un proceso de sincronización manual único. El proceso de carga automática gestionará los cambios futuros.
