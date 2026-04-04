---
title: Sincronizar  [!DNL Adobe] audiencias
description: Aprenda a sincronizar metadatos, datos de jerarquía y datos de audiencia única para sus  [!DNL Adobe] audiencias.
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
TQID: https://experienceleague.adobe.com/PKWhdnMHVAI3aI--1vdCeqnX6b8j34uvHycZLw1Yvjw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 0%

---

# Sincronizar audiencias de [!DNL Adobe]

*[!DNL Direct Access]solo administradores y gestores de clientes*

*Anunciantes con una integración Adobe Advertising-Adobe Audience Manager o Adobe Advertising-Adobe Analytics solamente*

Puede permitir que Search, Social y Commerce extraigan metadatos, datos de jerarquía y datos de audiencia única para todas las audiencias [!DNL Adobe] de un anunciante o agencia en las vistas [!UICONTROL Campaigns] > [!UICONTROL Audiences]. Esta información incluye datos para:

* Segmentos de Adobe Audience Manager

* Segmentos de Adobe Analytics publicados en Adobe Experience Cloud

* Segmentos creados con Adobe Experience Cloud [!DNL Audience Library]

Para ser elegible, el anunciante o la agencia deben implementar el [servicio de identidad de Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es) y proporcionar su ID de organización (anteriormente denominado [!DNL IMS Org ID]).

La sincronización inicial dura unas 24 horas. Después, los datos se sincronizan en tiempo real, con un retraso de uno a dos segundos.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**.

1. Escriba el identificador único de organización de la cuenta de Adobe Experience Cloud del anunciante y haga clic en **[!UICONTROL Submit]**.

   Si no conoce el identificador de organización del anunciante, búsquelo en el campo **[!UICONTROL IMS Org ID]** de la configuración del anunciante en [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Integración con soluciones y servicios de Adobe Experience Cloud](/help/search-social-commerce/introduction/integrations.md)
