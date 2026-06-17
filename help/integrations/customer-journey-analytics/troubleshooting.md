---
title: Solución de problemas de datos de Adobe Advertising en Customer Journey Analytics
description: Obtenga información sobre cómo solucionar y resolver problemas con los datos de Adobe Advertising en Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: d78aa2f6596190b644d9f920f51c179e43e86317
workflow-type: tm+mt
source-wordcount: 611
ht-degree: 0%

---

# Solución de problemas de datos de Adobe Advertising en Customer Journey Analytics

A continuación se indican posibles problemas y sus causas.

## Informes de resumen

+++ No hay datos de informes de resumen disponibles en Customer Journey Analytics para Advertising DSP o Advertising Search, Social y Commerce.

Compruebe lo siguiente:

* La fuente de Adobe Advertising a Customer Journey Analytics está habilitada. Consulte con el equipo de cuenta de Adobe.

* El conjunto de datos de dimensión, clasificación o búsqueda de Adobe Advertising y el conjunto de datos de resumen se incluyen en la conexión de Customer Journey Analytics.

* Las dimensiones y métricas de resumen de Adobe Advertising se incluyen en la vista de datos de Customer Journey Analytics.

* Customer Journey Analytics Workspace hace referencia a la vista de datos correcta.

Si verifica toda la configuración anterior pero sigue sin ver los datos de resumen, abra un vale de soporte técnico para su organización en [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).
.

+++

+++ Los datos del informe de resumen están disponibles en Customer Journey Analytics para el anunciante 1, pero no en Advertiser 2.

Compruebe que la fuente de Adobe Advertising a Customer Journey Analytics esté habilitada para Anunciante 2. Consulte con el equipo de cuenta de Adobe.

Si la fuente está habilitada para un anunciante pero aún no ves datos de resumen, abre un ticket de asistencia para tu organización en [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).
.

+++

+++ (Usuarios de Search, Social y Commerce) Los datos de informes de resumen están disponibles en Customer Journey Analytics para una cuenta de [!DNL Google Ads], [!DNL Meta Ads] o [!DNL Microsoft Advertising], pero no para otra cuenta.

Compruebe que la fuente de Adobe Advertising a Customer Journey Analytics esté habilitada para la cuenta específica de red de publicidad. Consulte con el equipo de cuenta de Adobe.

Si la fuente está habilitada para una cuenta pero aún no ves datos de resumen, abre un ticket de asistencia para tu organización en [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Incluya [!UICONTROL Account ID] para la cuenta de red de publicidad.
.

+++

+++ Los datos de informes de resumen de Customer Journey Analytics Workspace son diferentes de los datos de Advertising DSP o Advertising Search, Social y Commerce, o faltan datos de resumen para algunas campañas y entidades de campañas.

Compruebe lo siguiente:

* Está usando los mismos intervalos de fechas tanto en [!DNL Workspace] como en el informe de Adobe Advertising.

* Los filtros y segmentos aplicados en [!DNL Workspace] y en el informe de Adobe Advertising no están causando diferencias en los datos.

Si está seguro de una discrepancia en los datos, abra un ticket de asistencia para su organización en [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Incluya [!UICONTROL Account ID] para la cuenta de red de publicidad.
. Incluya capturas de pantalla y hojas de cálculo para mostrar la evidencia de la discrepancia. El equipo de cuenta de Adobe puede corregir de forma retroactiva la fuente de datos para resolver la discrepancia si es necesario.

+++

## Informes de nivel de evento

+++ Escenario: los datos de conversión (como `Page Views`) no están disponibles para una dimensión de informes (como `Campaign`) en CJA Customer Journey Analytics Workspace.

Compruebe lo siguiente, empezando por los elementos con menos barreras:

* Las métricas de conversión aplicables son eventos web/en línea que Adobe Advertising puede atribuir a dimensiones.

* Está utilizando la vista de datos correcta.

* Adobe Advertising realiza un seguimiento de los clics y las visualizaciones en el sitio aplicable. <!-- Link to validation instructions in the user guide -->

* En la conexión de Customer Journey Analytics para el conjunto de datos de clasificaciones, los valores de la configuración de [!DNL Key] y [!DNL Matching Key] son correctos: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* El servicio [!DNL Adobe Advertising] se agrega a la secuencia de datos de Adobe Experience Platform, el esquema asignado para la secuencia de datos es `XDM ExperienceEvent Schema` y el grupo de campos `Adobe Advertising Cloud ExperienceEvent Full Extension` se agrega al esquema.

* Los ajustes de Adobe Advertising se configuran correctamente en la extensión del SDK web y se publican.

Si verifica toda la configuración anterior pero sigue sin ver los datos de conversión, abra un vale de soporte técnico para su organización en [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Incluya [!UICONTROL Account ID] para la cuenta de red de publicidad.
.

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [Información general](overview.md)
>* [ID de Adobe Advertising usados por [!DNL Customer Journey Analytics]](ids.md)
>* [Requisitos previos](prerequisites.md)
>* [Configurar la recopilación de datos, la transferencia de datos y la creación de informes](set-up.md)
>* [Métricas y dimensiones de Adobe Advertising en Customer Journey Analytics](advertising-data-in-cja.md)
>* (Usuarios de Adobe Analytics) [Recopilar datos históricos de ID de AMO e ID de EF para usarlos en Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
