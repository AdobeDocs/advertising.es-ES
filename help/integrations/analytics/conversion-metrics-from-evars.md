---
title: Crear métricas de conversión a partir de Adobe Analytics [!DNL eVars]  y props
description: Configure métricas de eventos de éxito personalizadas con datos de nivel  [!DNL eVar] y  [!DNL prop].
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: 91e8435ff00feca804dfa2f4c323f88ee31813ab
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Crear métricas de conversión desde Adobe Analytics [!DNL eVars] y [!DNL props]

*Solo anunciantes con una integración de Adobe Analytics de Adobe Advertising*

DSP Puede utilizar métricas de eventos de éxito para optimizar paquetes de campañas de búsqueda, sociales y de Commerce basados en datos del sitio de Adobe Analytics que se ajusten mejor a los objetivos de su marca. Puede configurar métricas de eventos de éxito personalizadas basadas en sus [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=es) y [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html?lang=es) existentes canalizando datos de nivel [!DNL eVar] y [!DNL prop] en un evento. DSP Otras métricas de [!DNL Analytics], incluidas las métricas de conversión estándar, personalizadas y reservadas y las métricas de tráfico, están disponibles automáticamente en las redes sociales, Commerce y de búsqueda de.

![Ejemplo de uso](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Ejemplo de uso")

La mayoría de las tareas siguientes deben ser realizadas por un administrador de [!DNL Analytics] u otro usuario. DSP DSP Si necesita ayuda, póngase en contacto (con usuarios de la) con el equipo de soporte técnico de la aplicación en `adcloud_support@adobe.com` o (con los usuarios de Search, Social y Commerce) con el equipo de la cuenta de Adobe.

1. En [!DNL Analytics], [cree un evento de éxito de marcador de posición](https://experienceleague.adobe.com/es/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event).

   Utilice los siguientes parámetros adicionales:

   **Tipo:** `Counter`

   **Polaridad:** ya sea `Up is Good` o `Up is Bad`

   **Visibilidad:** `Visible Everywhere`

   **Registro de eventos únicos:** `Always Record Event`

   **Participación:** `Enabled`

   No es necesario implementar el nuevo evento en el sitio web de la marca, ya que utiliza datos existentes ya capturados.

1. Crear y validar una regla de procesamiento en [!DNL Analytics]:

   >[!NOTE]
   >
   >Solo los administradores de cuenta de [!DNL Analytics] pueden crear reglas de procesamiento a menos que hayan concedido permiso a usuarios que no sean administradores.

   1. [Cree una regla de procesamiento](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=es) con la siguiente configuración:

      * Para la condición que debe cumplirse, especifique el [!DNL eVars] o [!DNL props] requerido.

        Puede configurar niveles adicionales de granularidad según sea necesario para garantizar que se crean los eventos más precisos.

        >[!TIP]
        >
        >Se recomienda usar solamente un(a) [!DNL eVar] o [!DNL prop].

      * Para la acción, seleccione **Set Event** y seleccione el evento de marcador de posición.

   1. En [!DNL Analytics] [!DNL Analysis Workspace], [cree un proyecto](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=es) e inserte el nuevo evento en una tabla de forma libre para asegurarse de que se están rellenando los datos de la métrica [!DNL eVar] o [!DNL prop].

1. Póngase en contacto con el equipo de cuenta de Adobe para sincronizar la nueva métrica con el Adobe Advertising.

Una vez que la métrica esté disponible, puede usarla para crear un objetivo, que luego puede asignar a un portafolio de Search, Social y Commerce DSP, o usar como [objetivo personalizado](/help/dsp/optimization/custom-goal.md) para un paquete de.

Para obtener más información sobre la creación de objetivos, consulte el capítulo de la Guía de optimización sobre &quot;Objetivos&quot;, que está disponible en Search, Social y Commerce

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Datos en el Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Ver las métricas de conversión rastreadas de un anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
