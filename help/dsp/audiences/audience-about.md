---
title: DSP Acerca de la Gestión de público en Advertising
description: Obtenga información sobre las funciones de gestión de público.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: e2387f7e373e69c72e97ee83eff8f6a7ce9ceed5
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 0%

---

# DSP Acerca de la Gestión de público en Advertising

DSP En, puede crear y administrar segmentos de audiencia y conjuntos de audiencias, que puede usar como objetivos para sus ubicaciones:

* Puede recopilar sus propios datos de audiencia de origen creando e implementando segmentos. Posteriormente, puede redireccionar a los usuarios del segmento con anuncios o evitar que los usuarios del segmento reciban anuncios. Puede crear los siguientes tipos de segmentos:

   * [Segmentos personalizados](/help/dsp/audiences/custom-segment-create.md) para realizar un seguimiento de a) los usuarios expuestos a anuncios desde equipos de escritorio y dispositivos móviles y b) los usuarios que visitan páginas web específicas.

   * [Segmentos de exclusión de la venta de CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) para rastrear los ID de usuario de las solicitudes de exclusión de la venta de consumidores en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA). Puede recuperar informes mensuales de los ID de usuario de las solicitudes de exclusión de venta.

     Para obtener más información sobre la compatibilidad del Adobe Advertising con las solicitudes de exclusión de la venta de la CCPA, consulte [Compatibilidad de Adobe Advertising con la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* Puede crear una biblioteca de audiencias de [audiencias reutilizables](/help/dsp/audiences/reusable-audience-create.md). Las audiencias guardadas están compuestas por cualquiera de los segmentos de audiencia disponibles y por cualquiera de las demás audiencias guardadas. Los cambios que realice en una audiencia guardada se aplican automáticamente a todas las ubicaciones que dirijan o excluyan la audiencia, así como a todas las demás audiencias que incluyan la audiencia guardada.

  Las audiencias guardadas permiten a los planificadores de medios agrupar las audiencias según sea necesario, incluyendo y excluyendo varios segmentos mediante una lógica booleana compleja. El tamaño de cada segmento individual y el tamaño total de la audiencia se indican a medida que crea una audiencia. Los ejecutores de Campaign simplemente pueden seleccionar una o más audiencias guardadas como destinos de ubicación, en lugar de configurar manualmente los destinos de audiencia para cada ubicación.

También hay disponibles tipos de audiencia adicionales para la segmentación de ubicación.

## Importación de segmentos de datos de origen y de terceros

DSP Puede traducir sus segmentos de origen a ID universales para una segmentación sin cookies y puede ponerlos a disposición de cualquier anunciante o cuenta. DSP ha establecido conectores para la [el [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=es) y otras CDP. Para obtener más información, consulte la [Sección Fuentes](/help/dsp/audiences/sources/source-about.md).

DSP También puede importar el resto de segmentos de datos de origen directamente desde su plataforma de administración de datos (DMP) y proporcionarlos a cualquier conjunto de anunciantes, según sea necesario.

DSP Además, puede importar segmentos personalizados de terceros, incluidas combinaciones complejas de segmentos de terceros. Puede proporcionar los segmentos a cualquier conjunto de anunciantes, según sea necesario.

Póngase en contacto con el equipo de cuenta de Adobe para obtener más información.

## Audiencias disponibles como destinos de ubicación

Puede segmentar las ubicaciones para todos los tipos de audiencias siguientes.

* DSP Todos los conjuntos de audiencias creados por el usuario que se guardaron en el.

* DSP Todos los segmentos de audiencia creados por el usuario que se crearon en el sistema de segmentos de audiencia de:

   * Segmentos personalizados para usuarios que visitaron páginas web específicas y usuarios expuestos a impresiones de anuncios específicos.

   * Segmentos de audiencia de exclusión de CCPA para usuarios que enviaron solicitudes de exclusión de venta en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA).

* Todos los segmentos de datos de origen importados.

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

En la configuración de audiencia y de ubicación guardadas, puede ver datos detallados sobre el tamaño de la audiencia:

* Se muestra el tamaño de audiencia deduplicada total y activa en todos los segmentos seleccionados y audiencias guardadas, y puede ver detalles por tipo de dispositivo (navegador, móvil o TV conectada).

  ![el tamaño de audiencia combinado](/help/dsp/assets/audience-size.png)

* Para segmentos individuales y audiencias guardadas, el tamaño total de la audiencia y el CPM (cuando corresponda) se muestran junto al nombre del segmento. Puede ver más detalles sobre el segmento, incluido el tamaño por tipo de dispositivo (navegador, móvil o TV conectada). Para audiencias guardadas, el tamaño total es el total deduplicado.

  ![el tamaño del segmento individual](/help/dsp/assets/audience-size-segment.png)

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

* Todos los segmentos de origen importados disponibles para el usuario.

  No puede editar ni compartir segmentos de origen que se compartieron con usted. Póngase en contacto con el equipo de cuenta de Adobe si necesita compartir segmentos de origen con usuarios adicionales.

* Todos los segmentos de terceros personalizados disponibles para el usuario.

  No puede editar ni compartir segmentos de terceros que se compartieron con usted. Póngase en contacto con el equipo de cuenta de Adobe si necesita compartir segmentos de terceros con usuarios adicionales.

>[!MORELIKETHIS]
>
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Sintaxis de la lógica de segmento de audiencia](audience-segment-logic-syntax.md)
>* [Creación e implementación de un segmento personalizado](custom-segment-create.md)
>* [Creación e implementación de un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
