---
title: Implementación [!DNL Google Ads] campañas de rendimiento máximo
description: Obtenga información sobre el flujo de trabajo para configurar [!DNL Google Ads] campañas de rendimiento máximo.
exl-id: afad96b2-d4a6-41ee-ad84-38aa1306d73e
feature: Search Campaign Management
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementación [!DNL Google Ads] campañas de rendimiento máximo

Entrada [!DNL Google Ads] campañas de rendimiento máximo, no se configuran grupos de anuncios, anuncios ni palabras clave. En su lugar, dentro de la configuración de la campaña puede especificar uno o más grupos de recursos, que incluyen titulares, descripciones e imágenes, logotipos y archivos cargados. [!DNL YouTube videos]. [!DNL Google Ads] combina automáticamente los recursos para publicar anuncios en función del canal (por ejemplo, [!DNL YouTube], [!DNL Gmail], o [!DNL Search]).

Puede ver las campañas Máximo rendimiento existentes, con datos de rendimiento en formato de tabla y gráfico de tendencias, en la [!DNL Campaigns] vista; los datos no están disponibles en los niveles inferiores. Los datos de rendimiento de nivel de campaña también están disponibles en los informes y en Adobe Analytics (para anunciantes con un [Integración de Analytics](/help/integrations/analytics/overview.md). Para ver los datos de rendimiento de las campañas Máximo rendimiento en [!DNL Analytics], la campaña debe utilizar el [código de seguimiento de ID de AMO actualizado](/help/integrations/analytics/ids.md#amo-id-formats) (que realiza un seguimiento del ID de campaña y del ID de grupo de publicidad).

>[!NOTE]
>
>* Debe cargar manualmente todos los archivos de imagen. Vínculos a [!DNL Google Merchant Center] las fuentes de productos de no son compatibles.
>* Solo están disponibles las configuraciones necesarias. Para obtener una configuración opcional, inicie sesión en [!DNL Google Ads] editor.
>* La compatibilidad con la lista de grupos no está disponible. Para administrar y ver los datos de los grupos de listas, inicie sesión en [!DNL Google Ads] editor.

## Pasos para la configuración [!DNL Google Ads] campañas de rendimiento máximo

Puede configurar las campañas Máximo rendimiento de forma individual desde el [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vista.

1. [Creación de una campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) con tipo de campaña **[!UICONTROL Performance Max]**.

   Especifique el [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting], y [!UICONTROL URL Options]. Opcionalmente, introduzca [!UICONTROL Negative Keywords], introduzca [!UICONTROL Negative Websites], y/o anule la [!UICONTROL Campaign Tracking] opciones.

1. Cree grupos de recursos y cargue recursos para la campaña:

   1. En la parte inferior de la configuración de la campaña, haga clic en **[!UICONTROL Manage Asset Groups]**.

   1. Especifique la configuración del primer grupo de recursos y cargue las imágenes, los logotipos y los vídeos opcionales del grupo de recursos.

      Consulte [descripciones de la configuración del grupo de recursos](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) para comprender los requisitos y especificaciones.

   1. Añada grupos de recursos adicionales según sea necesario.

1. Haga clic **[!UICONTROL Post]**.

1. (Opcional) Añada la campaña a un portafolio híbrido para la optimización.
