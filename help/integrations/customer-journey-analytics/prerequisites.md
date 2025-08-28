---
title: Requisitos previos para integrar Adobe Advertising con Customer Journey Analytics
description: Requisitos previos para integrar Adobe Advertising con Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: ba23ab97c916f829cf9d640669423dd8e72949c0
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Requisitos previos para integrar Adobe Advertising con Customer Journey Analytics

*Anunciantes con Advertising DSP y[!DNL Advertising Search, Social, & Commerce]*

Revise la siguiente información antes de integrar Adobe Advertising con Adobe Customer Journey Analytics.

## Requisitos para informar sobre datos de Adobe Advertising en Customer Journey Analytics

* Anunciantes con [!DNL Analytics for Advertising] y Customer Journey Analytics:

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [Todos los demás requisitos previos de [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md).

* Anunciantes con Customer Journey Analytics pero no con [!DNL Analytics for Advertising]:

   * Biblioteca de Adobe Experience Platform Web SDK: `alloy.js`

     [!DNL Org ID] utilizado para Web SDK y para la cuenta del anunciante de Adobe Advertising debe ser el mismo. Puede encontrar este ID en la [pestaña Summary de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=es).

     ![Pantalla de resumen de Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

     Necesitará asistencia del administrador del sitio de Experience Platform para crear un conjunto de datos de Experience Platform y un esquema XDM.

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     Necesitará asistencia de su analista web interno para configurar una conexión con su conjunto de datos y crear informes.

>[!TIP]
>
>Para mejorar la fidelidad de los datos, utilice la versión más reciente de cada biblioteca.

>[!MORELIKETHIS]
>
>* [Información general](overview.md)
>* (Usuarios de Adobe Analytics) [Recopilar datos históricos para los ID de AMO e ID de EF para su uso en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
