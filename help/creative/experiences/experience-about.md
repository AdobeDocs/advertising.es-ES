---
title: Acerca de las experiencias en Advertising Creative
description: Aprenda a configurar experiencias de publicidad personalizadas y optimizar los elementos de publicidad en función del rendimiento.
feature: Creative Experiences
source-git-commit: fbf663b38282f48facab57efaf5533892642a252
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Acerca de las experiencias en Advertising Creative 2.0

*Beta cerrada*

<!-- Revisit Description metadata -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] proporciona dos estructuras de experiencia de anuncio diferentes para los anuncios de la biblioteca creativa<!-- can use a single library only -->:

* **Experiencias con segmentación en el árbol de decisiones:** [!DNL Creative] le permite configurar experiencias de publicidad personalizadas en todo el recorrido del cliente mediante un modelo de árbol de decisiones. Puede personalizar todos los elementos de publicidad (imágenes, titulares, ofertas y páginas de aterrizaje) en función del público objetivo.

  Por ejemplo, puede especificar el mismo paquete creativo para las personas de Chicago y Nueva York que están en un segmento de audiencia de Adobe Analytics específico, pero enviar a personas de Chicago que están en el mismo segmento a páginas de aterrizaje diferentes a las de los neoyorquinos. También puede especificar un paquete diferente para las personas del segmento que viven en cualquier lugar excepto Chicago y Nueva York, y un tercer paquete para otras personas que no están en el segmento.

  Las opciones de segmentación incluyen visores de sus segmentos de audiencia de origen de Adobe Audience Manager, Adobe Analytics y Advertising Cloud DSP DSP; visores de ubicaciones geográficas específicas, incluidos países, estados, DMA en Estados Unidos, ciudades y códigos postales; visores para los que el usuario, el editor o el socio pasan pares clave-valor específicos (destinos de paso de datos); visores con [!DNL Creative] píxeles de redireccionamiento y valores de atributo especificados; y visores con tipos de dispositivos, sistemas operativos y navegadores específicos.

  Puede asignar paquetes creativos a cada experiencia. Opcionalmente, puede personalizar la optimización y la programación de los paquetes creativos y cambiar las páginas de aterrizaje predeterminadas y las direcciones URL de seguimiento <!-- and any flexible attributes --> para los creativos individuales de cada paquete.

* **Experiencias sin segmentación en el árbol de decisiones:** [!DNL Creative] optimiza los elementos publicitarios para la experiencia publicitaria sin reducir la audiencia.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> Especificará las fechas de inicio y finalización y algunos ajustes predeterminados para cada experiencia, pero gran parte del flujo de trabajo no se encuentra directamente en la experiencia. En lugar de agregar elementos creativos directamente a la experiencia, se crea una etiqueta de anuncio para cada tamaño de anuncio y, a continuación, se agregan elementos creativos a la experiencia, se configura la optimización y la programación creativas y se personalizan las páginas de aterrizaje y las direcciones URL de seguimiento desde [!UICONTROL Tag Manager].

## Optimización de publicidad

<!-- MORE -->
[!DNL Creative] optimiza los elementos de anuncio para cualquier experiencia en función del rendimiento. Para las experiencias dirigidas a audiencias específicas, los anuncios se pueden optimizar en función del rendimiento de los elementos de anuncio individuales para los conjuntos de audiencias de destino. Para las experiencias sin objetivos de audiencia específicos, los elementos de publicidad se optimizan en función únicamente del rendimiento de los elementos de publicidad individuales.

## Implementación y administración de experiencias

Una vez que haya creado una experiencia en vivo (con todos los elementos de publicidad requeridos), puede [generar una etiqueta JavaScript o iframe para toda la experiencia](experience-tag-export.md), que opcionalmente puede cargar como un anuncio a una campaña en Adobe Advertising DSP DSP o implementarla como un anuncio en una campaña de terceros [!DNL Creative] proporciona anuncios para la experiencia en función de las opciones de segmentación y rotación de anuncios, así como del inventario de anuncios disponible.

## Datos de rendimiento para sus experiencias

Al habilitar la opción [!UICONTROL Metrics] en la vista [!UICONTROL Experiences], cada fila o tarjeta de experiencia indica el número de impresiones y clics que recibió la experiencia.

![Opción de métricas](/help/creative/assets/metrics-option.png "Opción de métricas")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

Puede ver datos de rendimiento detallados de cualquier experiencia en la vista [!UICONTROL Creative] > [!UICONTROL Experiences]. Para supervisar el rendimiento en todas las experiencias, cree un [!UICONTROL Custom Creative Report].

<!--
You can [view detailed performance data for any experience](experience-view-report.md) from the Creative > Experiences view. To monitor performance across your experiences, [create custom reports](/help/dsp/reports/report-create.md).
-->

## Estados de experiencia {#experience-statuses}

<!-- verify that these are all still the same -->

El estado de una experiencia se establece automáticamente, excepto *eliminada,* que usted establece manualmente.

DSP *Activo:* La experiencia incluye todos los elementos necesarios para que pueda generar una etiqueta de experiencia para implementarla como un anuncio en un grupo de usuarios de la red de distribución de contenido. <!-- A live experience may be scheduled to start in the future -->

*Borrador:* A todas las ramas de la experiencia no se les han asignado elementos creativos, por lo que la experiencia está incompleta y no se puede generar una etiqueta de experiencia.

*Procesamiento:* Se ha editado una experiencia que ya estaba activa, pero ahora está incompleta. No puede generar una etiqueta de experiencia para él. **Nota:** Si ya implementó una etiqueta de experiencia para la experiencia, se ofrecerá la versión que estaba activa anteriormente. Si más adelante completa la experiencia (y la vuelve a activar), la nueva versión se proporcionará con la implementación de etiquetas existente.

*Eliminada:* La experiencia se eliminó de [!DNL Creative] y ya no es visible en las vistas [!UICONTROL Experiences].

>[!NOTE]
>
>DSP Puede cambiar el estado de un anuncio dentro de una sin que ello afecte al estado de la experiencia en [!DNL Creative].

## La vista [!UICONTROL Experiences]

La vista [!UICONTROL Experiences] muestra todas sus experiencias segmentadas y sin segmentar. Puede ver los nombres de las experiencias, el estado, las fechas de inicio y finalización, el número y las dimensiones de los creativos o paquetes creativos asignados, y si la experiencia incluye anuncios dinámicos. Al habilitar la opción [!UICONTROL Metrics] en la vista [!UICONTROL Experiences], cada fila o tarjeta de experiencia indica el número de impresiones y clics que recibió la experiencia.

Puede crear y administrar sus experiencias, incluida la optimización y la asignación de creativos y paquetes creativos a sus experiencias. También puede crear y cambiar el nombre de las etiquetas de experiencia de anuncio y exportarlas en los formatos JavaScript DSP e iframe para su implementación en el entorno de trabajo de la aplicación de la aplicación de la. Los anunciantes con Advertising DSP pueden, opcionalmente, cargar etiquetas directamente en una campaña de Advertising DSP como anuncios.

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Crear una experiencia sin segmentación](experience-create-no-targeting.md)
