---
title: Activar segmentos autenticados de socios de ID universales
description: Obtenga información acerca de la activación de audiencias autenticadas mediante una solución de ID universal.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: e9ff454428d0256402a2ef2fa74f8bd45bd7592f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Activar segmentos autenticados de socios de ID universales

DSP Para activar audiencias autenticadas a través de una solución de ID universal en Advertising, los segmentos deben traducirse a [!DNL RampIDs], que son reconocibles en un entorno de oferta. Para ello, puede hacer lo siguiente:

* DSP Aprovechamiento de la integración de la con [!DNL Adobe Real-Time Customer Data Platform (CDP)] y el [!DNL Adobe-LiveRamp Retrieval API].

* DSP Envío manual de segmentos autenticados a los que se va a realizar una autenticación desde el [!DNL LiveRamp] [!DNL Connect] panel.

## Tareas

1. Para cualquier opción, póngase en contacto con `adcloud-support@adobe.com` DSP DSP para habilitar la siguiente configuración en la, que le permitirá dirigirse a segmentos autenticados en campañas de una sola vez [se han completado todos los pasos del flujo de trabajo de activación](source-adobe-rtcdp.md):

   1. [!DNL LiveRamp] [!DNL RampID] configuración de campaña antes del uso compartido de segmentos de [!DNL Real-Time CDP].

   1. El nivel de cuenta &quot;[!UICONTROL LiveRamp segments]Opción &quot;.

1. (Los usuarios comparten manualmente segmentos autenticados de [!DNL LiveRamp]) Complete los siguientes pasos en la [!DNL LiveRamp] [!DNL Connect] panel:

   1. Activar el mosaico de destino **[!DNL AAC API 1P Onboarding]**.

   1. Establecer [!DNL Identifier Settings] hasta **[!DNL Ramp ID]** solo.

      ![Configuración de identificador](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Opcional) Si desea seguir recibiendo identificadores basados en cookies, cree un segundo [!DNL AAC API 1P Onboarding] mosaico de destino con &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; y &quot;[!DNL AAID]&quot; seleccionado.

## Prácticas recomendadas para pruebas y validación de datos

* **Target [!DNL RampID]Segmentos basados en y cookies en campañas independientes.**

   * La configuración de la campaña solo permite priorizar un identificador.

   * Actualmente, [!DNL RampIDs] no se pueden recuperar durante los eventos en el sitio. Esto significa que algunos objetivos personalizados, como CPA más baja y ROAS, no están disponibles con el uso de segmentos autenticados. Utilice segmentos basados en cookies únicamente si tiene un KPI de rendimiento restrictivo.

* **Cree una ubicación en ambas [!DNL RampID] y campañas basadas en cookies.**

   * Oriente los segmentos que se comparten desde [!DNL LiveRamp] mediante el proceso de activación de segmentos estándar.

   * Póngase en contacto con el equipo de soporte de Adobe Advertising para validar la correcta distribución de los datos.

DSP Para obtener más información sobre la integración de la con [!DNL LiveRamp], contacto `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia](source-about.md)
>* [Crear una fuente de audiencia para activar audiencias de origen](source-create.md)
>* [Configuración de origen de audiencia](source-settings.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
