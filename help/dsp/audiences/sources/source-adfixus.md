---
title: Importar segmentos de origen de  [!DNL AdFixus]
description: Obtenga información sobre cómo importar los  [!DNL AdFixus] segmentos de origen que constan de [!DNL AdFixus] ID universales a DSP.
feature: DSP Audiences
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 0%

---

# Importar segmentos de origen de [!DNL AdFixus]

*Aplicable solo a anunciantes de Australia*

Use la integración de Advertising DSP con [!DNL AdFixus] para importar los identificadores universales [!DNL AdFixus] con asignaciones de segmentos para la publicidad de destino. [!DNL AdFixus] Los ID solo están disponibles en Australia. DSP no cambia los identificadores de [!DNL AdFixus] a otros tipos de identificador ni convierte otros tipos de identificador a [!DNL AdFixus] identificadores. DSP no cobra ninguna tarifa por importar los ID.

Una vez importados los segmentos de [!DNL AdFixus] en DSP, puede segmentar ubicaciones a [!DNL AdFixus] ID y a segmentos de origen específicos desde [!DNL AdFixus]. También puede agregar [!DNL AdFixus] segmentos a audiencias reutilizables. Los detalles de cualquier segmento incluyen el recuento de [!DNL AdFixus] ID aplicables.

Puede ver las métricas de impresión, clics, frecuencia y otras métricas de los usuarios con [!DNL AdFixus] ID en los informes personalizados. Los anunciantes con [!DNL Analytics for Advertising] también pueden ver datos de visualizaciones de [!DNL AdFixus] ID de Adobe Analytics, así como datos de Adobe Analytics en DSP.

1. Use [!DNL AdFixus] para convertir los datos de origen de su organización en segmentos con [!DNL AdFixus] ID.

   Esto requiere una cuenta independiente con [!DNL AdFixus] y una clave de licencia activa. También deberá implementar código específico de [!DNL AdFixus] para las propiedades y los dominios del sitio web. Trabaje directamente con [!DNL AdFixus] para generar segmentos con identificadores.

1. (Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurar el seguimiento para la medición de [!DNL Analytics]:

   1. (Si aún no lo ha hecho) Complete todos los [requisitos previos para implementar [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y el [ID de AMO e ID de EF en sus URL de seguimiento](/help/integrations/analytics/ids.md).

   1. Implemente código específico de [!DNL AdFixus] en sus páginas web para que coincida con las conversiones de los identificadores de [!DNL AdFixus] en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones.

1. Importar los segmentos de origen [!DNL AdFixus]:

   1. [Crear un origen de audiencia](source-manage.md) de [!UICONTROL Type] **[!UICONTROL AdFixus ID]**. Debe aceptar los términos del contrato de servicio.

      La configuración de origen incluirá una clave de origen generada automáticamente.

   1. Comparta la clave de origen con su equipo [!DNL AdFixus] para que pueda transmitir los segmentos necesarios a DSP.

1. Compruebe en la sección [!UICONTROL First Party Segments] de la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o en la configuración de ubicación) que el segmento se está rellenando. Comparar el número de ID de [!DNL AdFixus] con el número de ID de usuario dentro de [!DNL AdFixus].

   Los segmentos están disponibles en DSP en cuanto se crean.

Los segmentos se actualizan y quedan disponibles para la segmentación cada tres horas, aunque el recuento que aparece en DSP se actualiza cada 24 horas. **Nota:** La inclusión en un segmento caduca después de un período de caducidad especificado, que usted configura en [!DNL AdFixus]. Actualice sus segmentos reinsertándolos desde [!DNL AdFixus] antes de la caducidad.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar orígenes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Conexión de Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=es)
>* Resumen del catálogo de destinos [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=es)
>* [Compatibilidad para activar identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
