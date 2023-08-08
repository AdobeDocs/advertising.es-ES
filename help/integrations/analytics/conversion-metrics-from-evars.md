---
title: Crear métricas de conversión a partir de eVars y props de Adobe Analytics
description: Configure métricas de eventos de éxito personalizadas mediante datos de nivel de eVar y de propiedad.
feature: Integration with Adobe Analytics, Conversions
source-git-commit: d4f439ad23fc386bc85d95cc1291ec668ecf1cd2
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Crear métricas de conversión a partir de eVars y props de Adobe Analytics

*Anunciantes con solo integración de Adobe Advertising-Adobe Analytics*

DSP Puede utilizar métricas de eventos de éxito para optimizar paquetes de soluciones y campañas de búsqueda, medios sociales y comerciales basadas en datos del sitio de Adobe Analytics que se ajusten mejor a los objetivos de su marca. Puede configurar métricas de eventos de éxito personalizadas basadas en las [!DNL Analytics] [eVars](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) y [props](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) canalizando datos de nivel de eVar y prop en un evento. Otros [!DNL Analytics] DSP Las métricas de, incluidas las métricas de conversión estándar, personalizadas y reservadas, y las métricas de tráfico, están disponibles automáticamente en Búsqueda y búsqueda de, Social y Comercio.

![Ejemplo de uso](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Ejemplo de uso")

La mayoría de las tareas siguientes deben ser realizadas por un [!DNL Analytics] administrador u otro usuario. DSP DSP Si necesita ayuda, póngase en contacto (con los usuarios de la) con el equipo de asistencia técnica de en `adcloud_support@adobe.com` o (usuarios de Search, Social y Commerce) su equipo de cuenta de Adobe.

1. Entrada [!DNL Analytics], [crear un evento de éxito de marcador de posición](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Utilice los siguientes parámetros adicionales:

   **Tipo:** `Counter`

   **Polaridad:**  o bien `Up is Good` o `Up is Bad`

   **Visibilidad:** `Visible Everywhere`

   **Registro de un evento único:** `Always Record Event`

   **Participación:** `Enabled`

   No es necesario implementar el nuevo evento en el sitio web de la marca, ya que utiliza datos existentes ya capturados.

1. Creación de una regla de procesamiento en [!DNL Analytics]:

   >[!NOTE]
   >
   >Solo [!DNL Analytics] los administradores de cuentas pueden crear reglas de procesamiento a menos que hayan concedido permiso a usuarios que no sean administradores.

   1. [Creación de una regla de procesamiento](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), con la siguiente configuración:

      * Para la condición que debe cumplirse, especifique las eVars o props necesarias.

        Puede configurar niveles adicionales de granularidad según sea necesario para garantizar que se crean los eventos más precisos.

        >[!TIP]
        >
        >La práctica recomendada es utilizar solo un eVar o prop.

      * Para la acción, seleccione **Definir evento** y seleccione el evento placeholder.

   1. Entrada [!DNL Analytics] [!DNL Analysis Workspace], [creación de un proyecto](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) y extraiga el nuevo evento en una tabla de forma libre para asegurarse de que los datos se rellenan para la métrica eVar o prop.

1. Póngase en contacto con el equipo de cuenta de Adobe para sincronizar la nueva métrica con el Adobe Advertising.

Una vez que la métrica esté disponible, puede utilizarla para crear un objetivo, que luego puede asignar a un portafolio de Search, Social y Commerce, o usar como [meta personalizada](/help/dsp/optimization/custom-goal-about.md) DSP para obtener un paquete de.

Para obtener más información sobre la creación de objetivos, consulte el capítulo de la Guía de optimización sobre &quot;Objetivos&quot;, que está disponible en Search, Social y Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Datos en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->