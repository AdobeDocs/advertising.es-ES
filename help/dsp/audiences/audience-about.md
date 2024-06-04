---
title: DSP Acerca de la Gestión de público en Advertising
description: Obtenga información sobre las funciones de gestión de público.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 94c41ec311ed79897e1e26a650605c0213450071
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 0%

---

# DSP Acerca de la Gestión de público en Advertising

DSP En, puede crear y administrar segmentos de audiencia y conjuntos de audiencias, que puede usar como objetivos para sus ubicaciones:

* DSP Recopile sus propios datos de audiencia de origen creando e implementando segmentos de. Posteriormente, puede redireccionar a los usuarios del segmento con anuncios o evitar que los usuarios del segmento reciban anuncios. Puede crear los siguientes tipos de segmentos:

   * [Segmentos personalizados](/help/dsp/audiences/custom-segment-create.md) para realizar un seguimiento de a) los usuarios expuestos a anuncios desde equipos de escritorio y dispositivos móviles y b) los usuarios que visitan páginas web específicas. La etiqueta de seguimiento puede rastrear usuarios basados en cookies o usuarios asociados con ID universales ID5.

   * [Segmentos de exclusión de la venta de CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) para rastrear los ID de usuario de las solicitudes de exclusión de la venta de consumidores en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA). Puede recuperar informes mensuales de los ID de usuario de las solicitudes de exclusión de venta.

     Para obtener más información sobre la compatibilidad del Adobe Advertising con las solicitudes de exclusión de la venta de la CCPA, consulte [Compatibilidad de Adobe Advertising con la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Función beta) [Obtención y uso de ID universales para segmentación sin cookies](/help/dsp/audiences/universal-ids.md):

   * Envíe manualmente los mensajes autenticados [!DNL LiveRamp] [!DNL RampID] DSP segmentos directamente a los que se va a.

   * DSP Permita importar segmentos de origen desde la plataforma de datos del cliente y traducirlos a tipos de ID universales admitidos.

   * Incluya segmentos de terceros que contengan ID universales en sus destinos de colocación sin ningún paso adicional.

* Crear una biblioteca de audiencias de [audiencias reutilizables](/help/dsp/audiences/reusable-audience-create.md). Las audiencias guardadas están compuestas por cualquiera de los segmentos de audiencia disponibles y por cualquiera de las demás audiencias guardadas. Los cambios que realice en una audiencia guardada se aplican automáticamente a todas las ubicaciones que dirijan o excluyan la audiencia, así como a todas las demás audiencias que incluyan la audiencia guardada.

  Las audiencias guardadas permiten a los planificadores de medios agrupar las audiencias según sea necesario, incluyendo y excluyendo varios segmentos mediante una lógica booleana compleja. El tamaño de cada segmento individual y el tamaño total de la audiencia se indican a medida que crea una audiencia. Los ejecutores de Campaign simplemente pueden seleccionar una o más audiencias guardadas como destinos de ubicación, en lugar de configurar manualmente los destinos de audiencia para cada ubicación.

También hay disponibles tipos de audiencia adicionales para la segmentación de ubicación.

## Importación de segmentos de datos de origen y de terceros

DSP DSP Dispone de muchas opciones para importar segmentos de datos de origen y de terceros en la mediante la interfaz de usuario de la interfaz de usuario de la aplicación o a través de servicios de importación personalizados.

* DSP Puede extraer su Adobe Audience Manager y otros recursos [!DNL Adobe] audiencias para segmentación. Para conocer los requisitos previos y las instrucciones, consulte &quot;[Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios](/help/integrations/audience-manager/import-audiences.md).

* DSP Puede traducir segmentos de datos de origen de plataformas de datos de clientes compatibles a segmentos con ID universales mediante el [Función Fuentes](/help/dsp/audiences/sources/source-about.md). También puede [enviar manualmente los mensajes autenticados [!DNL LiveRamp] [!DNL RampID] DSP segmentos directamente a la](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP Puede importar el resto de segmentos de datos de origen directamente desde su plataforma de administración de datos (DMP) y proporcionarlos a cualquier conjunto de anunciantes, según sea necesario.

* DSP Puede importar segmentos personalizados de terceros, incluidas combinaciones complejas de segmentos de terceros. Puede proporcionar los segmentos a cualquier conjunto de anunciantes, según sea necesario.

Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

## Audiencias disponibles como destinos de ubicación

Puede segmentar las ubicaciones para todos los tipos de audiencias siguientes.

* DSP Todos los conjuntos de audiencias creados por el usuario que se guardaron en el.

* DSP Todos los segmentos de audiencia creados por el usuario que se crearon en el sistema de segmentos de audiencia de:

   * Segmentos personalizados para usuarios que visitaron páginas web específicas y usuarios expuestos a impresiones de anuncios específicos.

     No se incurre en cargos por impresiones entregadas a ID universales.

   * Segmentos de audiencia de exclusión de CCPA para usuarios que enviaron solicitudes de exclusión de venta en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA).

* Todos los segmentos de datos de origen importados, incluidos los segmentos traducidos a ID universales.

  Se cobran cargos adicionales por las impresiones entregadas a los ID universales. Consulte &quot;[Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)&quot; para las tarifas.

* Todos los segmentos de datos de terceros personalizados importados.

* (Ubicaciones dirigidas únicamente a EE. UU.) [DSP Todos los segmentos de datos de terceros disponibles para los clientes de la de más de 30 proveedores](/help/dsp/audiences/third-party-data-providers.md), incluido [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast], y muchos más.

  Puede segmentar segmentos específicos, que se dirigen a usuarios en función de datos de audiencia (por ejemplo, usuarios con datos demográficos, intereses o intenciones específicos o perfiles de comportamiento). Puede examinar por proveedor de datos y categoría, buscar segmentos por nombre o ID de segmento o filtrar los resultados por proveedor de datos, tamaño total del segmento, recuento del explorador web o recuento de dispositivos.

  Los segmentos de terceros incurren en tarifas adicionales, que se indican junto al nombre de cada segmento.

* (Anunciantes con Adobe Experience Platform y [!DNL Real-Time CDP], Adobe Audience Manager o Adobe Analytics que solo utilizan etiquetas de conversión de JavaScript de Adobe Advertising) Todos los segmentos de audiencia de origen, segundo o tercero disponibles creados en [!DNL Real-Time CDP], creado en Audience Manager o publicado en Adobe Experience Cloud desde Audience Manager o [!DNL Analytics].

  DSP El precio para el uso de los segmentos está negociado previamente y no es visible en los segmentos de la lista de precios de la lista de precios de la lista de precios de la lista de precios de la lista de precios

  Segmentos de [!DNL Analytics] están disponibles aproximadamente una hora después de crearlas o publicarlas como audiencias de Experience Cloud. Segmentos procedentes directamente del Audience Manager o [!DNL Real-Time CDP] están disponibles en un plazo de 24 horas después de compartirlas.

  >[!NOTE]
  >
  >Consulte la documentación de [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html), y [el [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) para obtener información sobre la configuración y recopilación de datos para segmentos de esas soluciones.

## Datos de tamaño de audiencia

En Audiencias > Todas las audiencias y en la sección Segmentación de audiencia de la configuración de ubicación, puede filtrar cada lista de segmentos por intervalo de tamaño, incluido el intervalo total y los intervalos independientes para tipos de dispositivos específicos o tipos de ID universales.

![filtrar por tamaño de audiencia](/help/dsp/assets/audience-size-filter.png)

También puede ver datos detallados del tamaño de la audiencia:

* Se muestra el tamaño de audiencia deduplicada total y activa en todos los segmentos seleccionados y audiencias guardadas, y puede ver detalles por tipo de dispositivo (navegador, móvil o TV conectada).

  ![el tamaño de audiencia combinado](/help/dsp/assets/audience-size.png)

* Para segmentos individuales, el tamaño total de la audiencia y el CPM (cuando corresponda) se muestran junto al nombre del segmento.

  ![el tamaño del segmento individual](/help/dsp/assets/audience-size-segment.png)

* Puede ver más detalles sobre un segmento individual o una audiencia guardada, incluido el tamaño por explorador, móvil, TV conectada y socio de tipo ID universal. Para audiencias guardadas, el tamaño total es el total deduplicado.

  ![el segmento individual o los detalles de audiencia guardados](/help/dsp/assets/audience-size-segment-details.png)

## Las vistas Audiencias

### La vista Todas las audiencias

En el [!UICONTROL All Audiences] Ver, o Biblioteca de audiencias, puede guardar y administrar audiencias reutilizables, que incluyen grupos de segmentos de audiencia e incluso otras audiencias guardadas. Puede usar las audiencias como destinatarios para varias ubicaciones. El número de ubicaciones en las que se utiliza cada audiencia se indica junto al nombre de la ubicación.

Puede editar, clonar, eliminar, exportar o compartir cualquier audiencia.

### La vista Segmentos

En el [!UICONTROL Segments] Vista, todos los usuarios pueden crear segmentos personalizados adicionales.

El [!UICONTROL Segments] La vista también enumera los siguientes tipos de segmentos:

* Todos los segmentos personalizados creados por el usuario disponibles para el usuario.

  Puede ver las etiquetas de seguimiento de cualquiera de los segmentos personalizados que ha creado y compartir esos segmentos con otros usuarios. También puede editar o eliminar los segmentos personalizados que ha creado.

  No puede editar ni compartir segmentos personalizados que otros usuarios hayan compartido con usted.

* Todos los segmentos de origen importados tal cual están disponibles para el usuario.

  No puede editar ni compartir segmentos de origen que se compartieron con usted. Póngase en contacto con el equipo de cuenta de Adobe si necesita compartir segmentos de origen con usuarios adicionales.

* Todos los segmentos de terceros personalizados disponibles para el usuario.

  No puede editar ni compartir segmentos de terceros que se compartieron con usted. Póngase en contacto con el equipo de cuenta de Adobe si necesita compartir segmentos de terceros con usuarios adicionales.

### La vista Fuentes

En el [!UICONTROL Sources] En esta vista, puede configurar fuentes para segmentos de origen en plataformas de datos de clientes compatibles que desee convertir en segmentos que contengan tipos de ID universales especificados. La configuración de origen incluye una clave de origen generada automáticamente, que proporcionará a su plataforma de datos del cliente para establecer la conexión.

Para obtener más información sobre las plataformas de datos del cliente compatibles, los tipos de ID universales compatibles y los flujos de trabajo para configurar conexiones a cada plataforma de datos del cliente, consulte &quot;[Acerca de los orígenes](/help/dsp/audiences/sources/source-about.md).&quot;

Los segmentos traducidos están disponibles para incluirlos en audiencias reutilizables y en la configuración de ubicación para la segmentación sin cookies.

>[!MORELIKETHIS]
>
>* [Compatibilidad con la activación de ID universales](/help/dsp/audiences/universal-ids.md)
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Creación e implementación de un segmento personalizado](custom-segment-create.md)
>* [Creación e implementación de un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Importar manualmente segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
