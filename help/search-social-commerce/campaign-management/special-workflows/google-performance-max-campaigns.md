---
title: Implementar  [!DNL Google Ads] campañas de rendimiento máximo
description: Obtenga información acerca del flujo de trabajo para configurar  [!DNL Google Ads] campañas de rendimiento máximo.
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementar [!DNL Google Ads] campañas de rendimiento máximo

En [!DNL Google Ads] campañas con rendimiento máximo, no se configuran grupos de anuncios, anuncios ni palabras clave. En su lugar, en la configuración de la campaña debe especificar uno o más grupos de recursos, que incluyen titulares, descripciones e imágenes cargadas, logotipos y [!DNL YouTube videos]. [!DNL Google Ads] combina automáticamente los recursos para publicar anuncios basados en el canal (como [!DNL YouTube], [!DNL Gmail] o [!DNL Search]).

Puede ver sus campañas Máximo rendimiento existentes, con datos de rendimiento en formato de tabla y gráfico de tendencias, en la vista [!DNL Campaigns]; los datos no están disponibles en los niveles inferiores. Los datos de rendimiento de nivel de campaña también están disponibles en los informes y en Adobe Analytics (para anunciantes con una [integración de Analytics](/help/integrations/analytics/overview.md). Para ver los datos de rendimiento de las campañas Máximo rendimiento de [!DNL Analytics], la campaña debe usar el [código de seguimiento de ID de AMO actualizado](/help/integrations/analytics/ids.md#amo-id-formats) (que realiza el seguimiento del ID de campaña y el ID de grupo de anuncios).

>[!NOTE]
>
>* Debe cargar manualmente todos los archivos de imagen. No se admiten vínculos a [!DNL Google Merchant Center] fuentes de productos.
>* Solo están disponibles las configuraciones necesarias. Para obtener una configuración opcional, inicie sesión en el editor [!DNL Google Ads].
>* La compatibilidad con la lista de grupos no está disponible. Para administrar y ver los datos de los grupos de listas, inicie sesión en el editor [!DNL Google Ads].

## Pasos para configurar [!DNL Google Ads] campañas de rendimiento máximo

Puede configurar las campañas Máximo rendimiento de forma individual desde la vista [!UICONTROL Campaigns] > [!UICONTROL Campaigns].

1. [Crear una campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) con el tipo de campaña **[!UICONTROL Performance Max]**.

   Especifique [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting] y [!UICONTROL URL Options]. Si lo desea, escriba [!UICONTROL Negative Keywords], escriba [!UICONTROL Negative Websites] o anule las opciones de [!UICONTROL Campaign Tracking].

1. Cree grupos de recursos y cargue recursos para la campaña:

   1. En la parte inferior de la configuración de la campaña, haga clic en **[!UICONTROL Manage Asset Groups]**.

   1. Especifique la configuración del primer grupo de recursos y cargue las imágenes, los logotipos y los vídeos opcionales del grupo de recursos.

      Consulte [descripciones de la configuración del grupo de recursos](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) para conocer los requisitos y especificaciones.

   1. Añada grupos de recursos adicionales según sea necesario.

1. Haga clic en **[!UICONTROL Post]**.

1. (Opcional) Añada la campaña a un portafolio híbrido para la optimización.
