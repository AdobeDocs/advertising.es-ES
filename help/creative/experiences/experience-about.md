---
title: Acerca de las experiencias en Advertising Creative
description: Aprenda a configurar experiencias de publicidad personalizadas y optimizar los elementos de publicidad en función del rendimiento.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%

---

# Acerca de las experiencias en Advertising Creative 2.0

Cada experiencia de anuncio puede incluir un tipo de anuncio (pantalla estándar, vídeo estándar o visualización dinámica). [!DNL Advertising Creative 2.0] proporciona dos estructuras de experiencia de anuncio diferentes para los anuncios en una sola biblioteca creativa.

* **Experiencias con segmentación en el árbol de decisiones:** [!DNL Creative] le permite configurar experiencias de publicidad personalizadas en todo el recorrido del cliente mediante un modelo de árbol de decisiones. Puede personalizar todos los elementos de publicidad (imágenes, titulares, ofertas y páginas de aterrizaje) en función del público objetivo.

  Por ejemplo, puede especificar el mismo paquete creativo para las personas de Chicago y Nueva York que están en un segmento de audiencia de Adobe Analytics específico, pero envían a personas de Chicago a páginas de aterrizaje diferentes a las de los neoyorquinos. También puede especificar un paquete diferente para las personas del segmento que viven en cualquier lugar excepto Chicago y Nueva York, y un tercer paquete para otras personas que no están en el segmento.

  Las opciones de segmentación incluyen:

   * Los segmentos de audiencia de Adobe Audience Manager, Adobe Analytics y Advertising DSP; cualquier otro segmento de origen importado para la cuenta; los segmentos personalizados de Advertising DSP; los segmentos de terceros proporcionados por Advertising DSP y cualquier audiencia de Advertising DSP existente creada en la biblioteca de audiencias

   * Ubicaciones geográficas específicas, incluidos países, estados, DMA en Estados Unidos, ciudades y códigos postales

   * Visores para los que se pasan pares clave-valor específicos (destinos de paso de datos) desde DSP, el editor o el socio (como SKU=01234567890123 o Cart=empty)

   * [!DNL Creative] píxeles de retargeting y valores de atributo especificados

   * Tipos de dispositivos, sistemas operativos y exploradores específicos

  Una vez que haya creado una rama de audiencia de destinatario en el árbol de decisiones, puede emparejar la audiencia de destino con posibles creativos asignando paquetes creativos a la rama. Para cada experiencia, puede personalizar la optimización y la programación de los paquetes creativos y cambiar las páginas de aterrizaje predeterminadas y las direcciones URL de seguimiento <!-- later: and any flexible attributes --> para los creativos individuales de cada paquete.

* **Experiencias sin segmentación en el árbol de decisiones:** [!DNL Creative] optimiza los elementos publicitarios para la experiencia publicitaria sin reducir la audiencia. Para cada experiencia, se especifican fechas de inicio y finalización y algunos ajustes predeterminados, pero gran parte del flujo de trabajo no se realiza directamente en la experiencia. En lugar de agregar elementos creativos directamente a la experiencia, use [!UICONTROL Tag Manager] para crear una etiqueta de anuncio para cada tamaño de anuncio de la experiencia y, a continuación, agregue elementos creativos, configure la optimización y la programación creativas, y personalice las páginas de aterrizaje y las direcciones URL de seguimiento<!-- later: and any flexible attributes -->.

>[!NOTE]
>
> Dado que los dos tipos de experiencias tienen flujos de trabajo diferentes, no se puede cambiar una experiencia sin objetivo a una experiencia con objetivo ni una experiencia con objetivo a una experiencia sin objetivo.

## Entrega y optimización de anuncios

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative] proporciona anuncios de origen y déclencheur de anuncios de terceros para la experiencia en función de las opciones de objetivo de segmentación (cuando corresponda), programación, rotación de anuncios y optimización, así como del inventario de anuncios disponible.

* **Programación:** (opcional) Programe la ejecución de elementos creativos específicos durante períodos de tiempo secuenciales especificados.

* **Rotación de anuncios:** Rotar los elementos creativos manualmente según pesos relativos o algorítmicamente según el objetivo de optimización especificado.

* **Objetivo de optimización:** Optimice los elementos de publicidad para obtener la mejor tasa de pulsaciones o para un [objetivo personalizado de Advertising DSP existente](/help/dsp/optimization/custom-goal.md)

  [!DNL Creative] optimiza las experiencias de los anuncios al dar cuota de impresiones a los recursos con mejor rendimiento de la experiencia. Para las experiencias dirigidas a audiencias específicas, los anuncios se pueden optimizar en función del rendimiento de los elementos de anuncio individuales para los conjuntos de audiencias de destino. Para las experiencias sin objetivos de audiencia específicos, los elementos de publicidad se optimizan en función únicamente del rendimiento de los elementos de publicidad individuales.

Por ejemplo, puede programar Creative 1 para que se ejecute durante las dos primeras semanas a fin de optimizar la tasa de pulsaciones y Creative 2 para que se ejecute durante las dos semanas siguientes a fin de optimizar para un objetivo personalizado especificado.

## Implementación y administración de experiencias

Una vez que hayas creado una experiencia en vivo (con todos los elementos publicitarios requeridos), puedes [generar una etiqueta JavaScript o iframe para toda la experiencia](experience-tag-export.md). Puede cargar la etiqueta de experiencia como anuncio en una campaña en Adobe Advertising DSP o implementarla como anuncio en un DSP de terceros.

>[!NOTE]
>
>El comportamiento de direccionamiento jerárquico puede variar según DSP. Advertising DSP aplica la segmentación a nivel de anuncio sobre la segmentación a nivel de ubicación.

## Datos de rendimiento para sus experiencias

Están disponibles los siguientes datos de rendimiento:

* Al habilitar la opción [!UICONTROL Metrics] en la vista [!UICONTROL Creative] > [!UICONTROL Experiences], cada tarjeta o fila de experiencia indica el número de impresiones y clics que recibió la experiencia.

  ![Opción de métricas](/help/creative/assets/metrics-option.png "Opción de métricas")

* Puede [ver datos de rendimiento detallados de cualquier experiencia](experience-performance-details.md) desde la vista [!UICONTROL Experiences].

* Para supervisar el rendimiento en todas las experiencias, cree un [Informe de Creative personalizado](/help/creative/report-custom-creative.md).

## Estados de experiencia {#experience-statuses}

El estado de una experiencia se establece automáticamente, excepto *Eliminada,* que usted establece manualmente.

| Estado | Descripción |
| ------ | ----------- |
| [!UICONTROL Live] | La experiencia incluye todos los elementos necesarios para que pueda generar una etiqueta de experiencia para implementarla como anuncio en un DSP. Se puede programar el inicio de una experiencia en directo en el futuro. |
| [!UICONTROL Draft] | A todas las ramas de la experiencia no se les asignan elementos creativos, por lo que la experiencia está incompleta y no se puede generar una etiqueta de experiencia. |
| [!UICONTROL Processing] | Se ha editado una experiencia anterior, pero ahora está incompleta. No puede generar una etiqueta de experiencia para él. **Nota:** Si ya implementó una etiqueta de experiencia para la experiencia, se puede seguir usando la versión activa anterior. Si más adelante completa la experiencia (y la vuelve a activar), se puede ofrecer la nueva versión con la implementación de etiquetas existente. |
| [!UICONTROL Deleted] | La experiencia se eliminó de [!DNL Creative] y ya no es visible en las vistas [!UICONTROL Experiences]. |

>[!NOTE]
>
>Puede cambiar el estado de un anuncio dentro de una DSP sin que ello afecte al estado de la experiencia en [!DNL Creative].

## La vista [!UICONTROL Experiences]

La vista [!UICONTROL Experiences] muestra todas sus experiencias segmentadas y sin segmentar. Puede ver los nombres de las experiencias, el estado, las fechas de inicio y finalización, el número y las dimensiones de los creativos o paquetes creativos asignados, y si la experiencia incluye anuncios dinámicos. Al habilitar la opción [!UICONTROL Metrics] en la vista [!UICONTROL Experiences], cada fila o tarjeta de experiencia indica el número de impresiones y clics que recibió la experiencia. Cuando esté en el modo de tarjeta, puede desplazarse por los elementos creativos de una experiencia con varios elementos creativos mediante los botones &lt; y >.

Puede crear y administrar sus experiencias, crear y cambiar el nombre de las etiquetas de experiencia de publicidad y exportar las etiquetas en los formatos JavaScript e iframe para su implementación en los DSP. Los anunciantes con Advertising DSP pueden, opcionalmente, cargar las etiquetas de publicidad directamente en una campaña de Advertising DSP.

### Acciones disponibles

Las siguientes son acciones clave disponibles. Para obtener una lista completa, consulte la tabla de contenido del capítulo Creativos > Experiencias.

* [Descargar datos dentro de la vista](experience-download-view.md)

* [Crear](/help/creative/experiences/experience-create-targeting.md) y [editar](/help/creative/experiences/experience-edit-targeting.md) una experiencia con segmentación

* [Crear](/help/creative/experiences/experience-create-no-targeting.md), [editar](/help/creative/experiences/experience-edit-no-targeting.md) y [crear manualmente una etiqueta de anuncio](/help/creative/experiences/experience-tag-create-manually.md) para una experiencia sin segmentar

* [Clonar](experience-clone.md) una experiencia

* [Vista previa](experience-preview.md) de una experiencia

* [Compartir una URL de demostración](experience-share-demo-url.md) para una experiencia

* [Exportar etiquetas de publicidad para una experiencia](experience-tag-export.md), incluida la carga opcional de etiquetas de publicidad directamente en una campaña de Advertising DSP

* [Eliminar](experience-delete.md) una experiencia

>[!MORELIKETHIS]
>
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Crear una experiencia sin segmentación](experience-create-no-targeting.md)
