---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Anexar parámetros en la configuración de cuenta y campaña

**[!UICONTROL Append Parameters]:** (Opcional) Cualquier parámetro de seguimiento adicional que se anexe a las direcciones URL base.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Los parámetros de datos anexados del nivel de anunciante se incluyen de forma predeterminada en el nivel de cuenta y de campaña, pero se pueden anular.

Puede usar cualquier cadena de texto estático, incluidos los parámetros de seguimiento de terceros, o cualquiera de los [parámetros de seguimiento admitidos](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), que insertan un valor de datos apropiado en la dirección URL base.

Separe los distintos parámetros con comas o el símbolo &amp;. No se admiten corchetes anidados.

**Notas:**

* La opción [!UICONTROL Auto Upload] no controla los cambios en los parámetros de datos anexados. Si cambia los parámetros de adición para direcciones URL base existentes, las nuevas direcciones URL no se generan automáticamente. Agregue los nuevos parámetros descargando un archivo de hoja de edición masiva para la cuenta o campaña, actualizando los campos [!UICONTROL Base URL/Final URL] y luego cargando y publicando la hoja de edición masiva.

* (Redes de anuncios con seguimiento paralelo) Evite utilizar macros que no sustituyan los clics de fuentes que habilitan el seguimiento paralelo. Si el anunciante debe utilizar macros, el equipo de cuenta de Adobe debe trabajar con Asistencia al cliente o con el equipo de implementación para agregarlas.

* (Anunciantes con una integración de Adobe Advertising-Adobe Analytics) Para incluir un parámetro de ID de AMO para enviar datos de Search, Social y Commerce a [!DNL Analytics], vea los [formatos específicos de red de anuncios](/help/integrations/analytics/ids.md#amo-id-formats). No es necesario agregar manualmente el parámetro para las cuentas de [!DNL Google Ads] y [!DNL Microsoft Advertising] con una implementación de ID de AMO del lado del servidor.
