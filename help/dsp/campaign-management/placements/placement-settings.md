---
title: Configuración de ubicación
description: Consulte las descripciones de la configuración de ubicación disponible.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: eaa25ce24bf00fb5ff7ea1e4a3364d4439f49b00
workflow-type: tm+mt
source-wordcount: '4039'
ht-degree: 0%

---

# Configuración de ubicación

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** El nombre de la ubicación.

>[!TIP]
>Utilice una convención de nombres que tenga sentido para su situación. Una convención de nombres sugerida es &quot;*\&lt;Campaign Name\>: \&lt;Ad Unit\>: \&lt;Duration\>: \&lt;Targeting\>*&quot;.

**[!UICONTROL Status]:** Estado de la ubicación: *[!UICONTROL Active]* (predeterminado) o *[!UICONTROL Paused]*.

>[!TIP]
>La práctica recomendada es pausar la ubicación hasta que esté listo para iniciarla.

**[!UICONTROL Details]:** (solo lectura) El tipo de anuncio aplicable, la cuenta que está creando o creando la ubicación y la campaña principal. Para ver más detalles, haga clic en **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Abre una lista de plantillas de ubicación existentes. Para rellenar automáticamente la configuración de direccionamiento desde una plantilla:

1. Realice una de las acciones siguientes:

   * Para reutilizar todos los destinos de una plantilla, active la casilla de verificación situada junto al nombre de la plantilla.

   * Para reutilizar tipos de destino individuales de una plantilla, expanda el nombre de la plantilla y active la casilla de verificación situada junto a los tipos de destino que desea reutilizar.

1. Haga clic en **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Solo formatos de anuncios de vídeo) La duración del anuncio y/o las especificaciones del anuncio, que se utilizan para calcular la proyección de Forecast a la derecha. Los campos varían según el tipo de anuncio.

**[!UICONTROL Environment]:** (solo formato de anuncio de vídeo universal) Los entornos de dispositivo (escritorio, móvil, TV conectada) que se incluirán como destinos en la ubicación. Especifique al menos uno.

En los informes personalizados, la dimensión de nivel de ubicación &quot;Entorno del dispositivo&quot; indica el entorno de destino.

**[!UICONTROL Placement tags]:** (Opcional) Palabras clave o apodos que le ayudarán a localizar esta ubicación.

## Metas

**[!UICONTROL Package]:** (opcional) paquete al que se asigna la ubicación. Haga clic en ![Editar](/help/dsp/assets/edit.png) para seleccionar un paquete existente o crear un paquete. Al asignar la ubicación a un paquete, la sección [!UICONTROL Goals] se actualiza con las fechas de vuelo, el objetivo de entrega y el presupuesto del paquete.

**[!UICONTROL Flight Dates]:** Fecha de inicio y finalización de la ubicación. Los anuncios aprobados pueden ejecutarse durante el vuelo cuando la ubicación esté activa y asignada a un paquete o campaña activos.

Las fechas del paquete (cuando corresponda) o de la campaña se rellenan automáticamente de forma predeterminada.

>[!NOTE]
>
>* Las fechas de vuelo deben incluirse en las fechas de vuelo de la campaña y en las fechas de vuelo del paquete.

### Ubicaciones asignadas a paquetes con ritmo de nivel de paquete

**[!UICONTROL Placement Funding]:** Cómo presupuestar la ubicación:

* *[!UICONTROL Optimize based on performance]:* controla el presupuesto en el nivel de paquete.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Permite establecer un presupuesto de ubicación mínimo o máximo. Especifique al menos un tipo de presupuesto:

   * *[!UICONTROL Maximum Budget]*: escriba un valor y la duración (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: el presupuesto mínimo como porcentaje del presupuesto del paquete. Cuando se especifica un límite de intervalo, el valor de presupuesto mínimo siempre se calcula como un porcentaje del límite de intervalo. De lo contrario, se calcula como un porcentaje del presupuesto del paquete.

**[!UICONTROL Max Bid]:** El máximo para pagar 1000 impresiones.

**[!UICONTROL Placement Pre-bid Filters]:** Hasta cinco umbrales de KPI (como una métrica mínima de visibilidad o una tasa de pulsaciones) que deben cumplirse para que se produzca la puja. Puede usar filtros de oferta previa como tácticas de optimización, pero tenga en cuenta que cada regla puede limitar las oportunidades en las que esta ubicación puede pujar. Para añadir o editar filtros:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las acciones siguientes:
   * Para añadir un filtro:
      1. Haga clic en **[!UICONTROL Add Filter]**.
      1. Junto a **[!UICONTROL Only bid if]**, seleccione una métrica y luego ingrese un valor.
   * Para quitar un filtro, haga clic en **[!UICONTROL X]** en la fila de filtro.
1. Haga clic en **[!UICONTROL Save]**.

Consulte las descripciones de cada filtro de oferta previa en &quot;[Filtros de oferta previa de nivel de ubicación y Cómo utilizarlos](/help/dsp/optimization/optimization-pre-bid-filters.md)&quot;.

### Todas las demás ubicaciones

**[!UICONTROL Budget Goal]:** Límite presupuestario bruto e intervalo presupuestario (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Ubicaciones en campañas solo con administración de márgenes) El límite presupuestario bruto y el intervalo presupuestario (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** El objetivo de optimización para el paquete. Consulte las descripciones de cada objetivo de optimización en &quot;[Objetivos de optimización y cómo utilizarlos](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** El objetivo de destino, que se usa para realizar el seguimiento del rendimiento.

>[!NOTE]
>
>Este campo es solo un punto de referencia y no se utiliza para la toma de decisiones.

**[!UICONTROL Pace on]:** La base para el ritmo:

* **[!UICONTROL Budget goal]:** (Predeterminado) Esta opción proporciona tantas impresiones como sea posible dentro del presupuesto asignado.

* **[!UICONTROL Impressions]:** Esta opción envía impresiones hasta que se alcance una cantidad especificada dentro de un intervalo especificado. Cuando seleccione esta opción, especifique el número de impresiones y el intervalo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** El máximo para pagar 1000 impresiones.

**[!UICONTROL Flight pacing]:** (Ubicaciones solo con ritmo de nivel de ubicación) Cómo espaciar la entrega de anuncios:

* *[!UICONTROL Even]:* (El valor predeterminado) Rastrea la entrega de manera uniforme durante cada vuelo, con un objetivo del 50 % de la entrega en la primera mitad del vuelo.

* *[!UICONTROL Slightly Ahead]:* (El valor predeterminado) Acelera la entrega para que se complete en un 55-65 % a mitad de la duración del vuelo.

* *[!UICONTROL Frontload]:* Acelera la entrega para que se complete en un 65-75% a mitad del vuelo.

* *[!UICONTROL Aggressive Frontload]:* Acelera la entrega para que se complete en un 75-85% a mitad del vuelo.

**[!UICONTROL Intraday pacing]:** (Ubicaciones solo con ritmo de nivel de ubicación) Cómo realizar el ritmo y la entrega a lo largo de cada día dentro del vuelo:

* *[!UICONTROL Even]:* (El valor predeterminado) Escala el envío según la disponibilidad del inventario. Por lo general, se publican más anuncios por hora durante el día, cuando el volumen de subasta es mayor, y menos anuncios por las mañanas y las noches.

* *[!UICONTROL ASAP]:* (El valor predeterminado) Acelera el envío al doble de la velocidad de *Even*.

  >[!CAUTION]
  >
  >Esta opción puede afectar negativamente al rendimiento. Utilícelo únicamente cuando priorice completamente la entrega y gaste en lugar de optimizar el rendimiento.

**[!UICONTROL Placement Pre-bid Filters]:** (Opcional) Hasta cinco filtros que deben cumplirse para que se produzca la puja. Puede usar filtros de oferta previa como tácticas de optimización, pero tenga en cuenta que cada regla puede limitar las oportunidades en las que esta ubicación puede pujar. Para añadir o editar filtros:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las acciones siguientes:
   * Para añadir un filtro:
      1. Haga clic en **[!UICONTROL Add Filter]**.
      1. Junto a **[!UICONTROL Only bid if]**, seleccione una métrica y luego ingrese un valor.
   * Para quitar un filtro, haga clic en **[!UICONTROL X]** en la fila de filtro.
1. Haga clic en **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (opcional) ubicaciones específicas en las que incluir o excluir anuncios en la ubicación. Si no especifica ninguna ubicación, se segmentarán todas las ubicaciones.

>[!NOTE]
>
>Las ubicaciones de ciudad y DMA no están disponibles para las ubicaciones de Roku.

Para especificar ubicaciones:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para incluir o excluir un país, estado, ciudad, DMA, distrito legislativo federal o distrito legislativo estatal:
      1. Seleccione el tipo de ubicación en la columna izquierda.
      1. (Según sea necesario) Haga clic en una ubicación para expandirla.
      1. Junto a la ubicación, haga clic en *[!UICONTROL Include]* para incluirlo como destino o en *[!UICONTROL Exclude]* para excluirlo como destino.
   * Para buscar un código postal e incluir o excluir todos los resultados seleccionados:
      1. Haga clic en **[!UICONTROL Search Postal Code]**.
      1. Seleccione el país.
      1. Escriba el nombre de la ciudad y haga clic en ![Editar](/help/dsp/assets/search.png).
      1. Haga clic en el resultado de búsqueda correcto.
      1. Haga clic en *[!UICONTROL Include All]* para incluir todas las ubicaciones como destinos o en *[!UICONTROL Exclude All]* para excluir todas las ubicaciones como destinos.
   * Para introducir o pegar códigos postales e incluirlos o excluirlos todos:
      1. Haga clic en **[!UICONTROL Paste Postal Code]**.
      1. Seleccione el país.
      1. Introduzca o pegue hasta 1000 códigos postales.
Incluya un código postal por línea o introduzca varios valores separados por comas o tabulaciones.
      1. Haga clic en *[!UICONTROL Include All]* para incluir todas las ubicaciones como destinos o en *[!UICONTROL Exclude All]* para excluir todas las ubicaciones como destinos.
   * Para quitar una ubicación de la lista [!UICONTROL Included] o [!UICONTROL Excluded], haga clic en **[!UICONTROL X]** junto a la ubicación en la columna derecha.
1. Haga clic en **[!UICONTROL Done]**.

>[!NOTE]
>
>* No todos los países tienen ubicaciones de estado, ciudad o código postal.
>* DMA (área de mercado designada), distritos legislativos federales y distritos legislativos estatales solo están disponibles para ubicaciones de EE. UU.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** orígenes de inventario para incluir o excluir como destinos. Para la mayoría de los tipos de ubicación, todos los tipos de inventario y todos los orígenes de cada tipo se incluyen de forma predeterminada. Para [!DNL Roku] ubicaciones, debe especificar el tipo de inventario y los orígenes. Puede elegir entre los siguientes tipos de inventario:

* [!UICONTROL Public]: (Todos los tipos de ubicación excepto Roku) Todo el inventario de Exchange abierto al que DSP tiene acceso. Puede incluir y excluir el inventario público.

  Puede ver la lista por origen o por fuente. Cuando vea la lista por fuente, puede buscar por nombre de fuente, clave de fuente o una etiqueta de característica seleccionada.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: sus ofertas privadas existentes (o ofertas privadas existentes de [!DNL Roku] para [!DNL Roku] ubicaciones) con los editores que ha configurado en DSP. Puede incluir, pero no excluir, el inventario público.

  Puede buscar en la lista por palabra clave, clave, ID de oferta o etiqueta personalizada.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Opcional) anula el algoritmo de precio de oferta para pujar al menos los precios fijos y mínimos de las ofertas.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: todos los [inventarios premium [!UICONTROL On Demand] sin garantía](/help/dsp/inventory/on-demand-inventory-about.md) (o [!UICONTROL On Demand] [!DNL Roku] ofertas para [!DNL Roku] ubicaciones) a los que te has suscrito en [!DNL DSP]. Puede incluir y excluir [!UICONTROL On Demand] inventario.

  Puede ver la lista por origen o por fuente. Cuando vea la lista por fuente, puede buscar por nombre de fuente, clave de fuente o una región de editor, etiqueta de categoría o etiqueta característica seleccionada.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Opcional) anula el algoritmo de precio de oferta para pujar al menos los precios fijos y mínimos de las ofertas.

Para especificar la segmentación de inventario:

* Para excluir un tipo de inventario, desactive la casilla de verificación situada junto al nombre.
* Para dirigirse a un tipo de inventario:
   1. Active la casilla de verificación situada junto al nombre del tipo de inventario.
   1. (Opcional) Cambie los orígenes para incluir lo siguiente:
      1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
      1. (Inventario de [!UICONTROL Public] y [!UICONTROL On Demand]) Haga clic en **[!UICONTROL View by Source]** o **[!UICONTROL View by Feed]** para cambiar la forma en que se enumeran los orígenes.
      1. (Cuando corresponda) Filtre el inventario según sea necesario.
      1. Especifique las fuentes que desea incluir y excluir:
         * Para incluir un origen de [!UICONTROL Public] o [!UICONTROL On Demand], haga clic en **[!UICONTROL Include]** junto al nombre del origen.
         * Para incluir [!UICONTROL Private] orígenes:
            * Para incluir todo el inventario en una oferta, haga clic en **[!UICONTROL Include all]** junto al nombre de la oferta.
            * Para incluir un origen de inventario individual, expanda el nombre de la oferta y, a continuación, haga clic en la casilla de verificación situada junto al nombre del origen.
         * Para excluir un(a) [!UICONTROL Public] o [!UICONTROL On source], haga clic en **[!UICONTROL Exclude]** junto al nombre de origen.
   1. (Opcional) Para descargar un archivo CSV con la información de destino en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Save & Export]**.
   1. Haga clic en **[!UICONTROL Save]**.

>[!TIP]
>
>Si se ha suscrito al inventario [!UICONTROL On Demand] pero no puede encontrar los editores ni las ofertas para target, compruebe el estado de las ofertas. Para obtener más información sobre los estados, consulte [Acerca de [!DNL On Demand] Inventario Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Solo ubicaciones de vídeos) Excluye el tráfico de salida.

Los anuncios salientes suelen aparecer sobre el contenido como una ventana emergente o rellenos de contenido (en la experiencia nativa), en lugar de como anuncios de vídeo normales en un reproductor de vídeo.

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** Tipos de tráfico de destino. Las opciones incluyen **[!UICONTROL Websites]** y **[!UICONTROL Apps]**.

**[!UICONTROL Tier]:** (disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) La calidad del tráfico de destino. Los niveles 1-3 son todos seguros para la marca y han sido aprobados por el equipo de asignación de DSP.

* *[!UICONTROL Tier 1]:* sitios y aplicaciones Premium reconocibles a nivel nacional.

* *[!UICONTROL Tier 2]:* Objetivos de nivel 1, así como sitios y aplicaciones de calidad menos conocidos que el nivel 1.

* *[!UICONTROL Tier 3]:* se dirige a los niveles 1-2, además de a sitios y aplicaciones legítimos y seguros para la marca que atienden a una audiencia específica. Utilice el nivel 3 para las compras de alcance o segmentación de datos.

* *[!UICONTROL All Sites or Apps]:* se dirige a los niveles 1-3 y al nuevo inventario que no se ha examinado ni clasificado, y que puede utilizar para llegar a ellos.

>[!NOTE]
>
>El inventario es específico de las unidades de anuncio de la ubicación.

>[!TIP]
>
>Para las campañas de rendimiento, la práctica recomendada es seleccionar *[!UICONTROL All Sites]*.

**[!UICONTROL Site or App Categories]:** (opcional; disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) Categorías de sitio dentro de los niveles de sitio seleccionados para incluir o excluir (pero no ambos) como destinos. Elija entre las listas de sitios verticales que DSP ha asignado en función del asunto:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique las categorías del sitio que se incluirán o excluirán:
   * Para incluir categorías de sitio:
      1. Haga clic en **[!UICONTROL Include categories]**.
      1. Seleccione la casilla de verificación situada junto a cada categoría de destino.
   * Para excluir las categorías del sitio:
      1. Haga clic en **[!UICONTROL Exclude categories]**.
      1. Seleccione la casilla de verificación situada junto a cada categoría que desee excluir.
1. (Opcional) Para descargar un archivo CSV con la información de destino en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Haga clic en **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (opcional; disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) Sitios que excluir. Puede buscar y seleccionar sitios, o bien escribir o pegar nombres de dominio:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los sitios:
   * Para buscar un sitio:
      1. Haga clic en **[!UICONTROL Search]**.
      1. Introduzca una palabra clave, seleccione un nivel de sitio y/o seleccione una categoría de sitio.
      1. En los resultados de búsqueda, seleccione los sitios que desea excluir:
         * Para excluir un sitio individual, active la casilla de verificación adyacente.
         * (Cuando haya más de 50 resultados disponibles) Para excluir los primeros 50 resultados, haga clic en **[!UICONTROL Exclude these 50]**. Para excluir todos los resultados de búsqueda, haga clic en **[!UICONTROL Exclude these \<*NN *\>]**.
   * Para introducir nombres de dominio:
      1. Haga clic en **[!UICONTROL Paste]**.
      1. Escriba uno o varios nombres de dominio en líneas independientes.
      1. Haga clic en **[!UICONTROL Exclude All]**.
1. Haga clic en **[!UICONTROL Done]** cuando haya terminado.

>[!NOTE]
>
>* También se aplican listas de sitios bloqueados a nivel de cuenta y de anunciante, además de la [lista de sitios bloqueados globalmente](/help/dsp/introduction/features/brand-safety-media-quality.md) de DSP, que incluye los sitios considerados no seguros para los anuncios.
>* Las listas de sitios bloqueados siempre anulan las listas de sitios de destino. Si una ubicación excluye e incluye el mismo destino para un anuncio, se excluye el destino.

**[!UICONTROL Language]:** (opcional) un solo idioma de destino.

**[!UICONTROL Site or App List Preview]:** (solo lectura) Todos los sitios de destino y bloqueados para la ubicación.

Si lo desea, puede exportar la lista de sitios de destino y bloqueados como archivo de valores separados por comas (CSV). Para exportar la lista, haga clic en **[!UICONTROL Export full site list]** y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador.

**[!UICONTROL Allow unscreened sites]:** (solo ubicaciones de visualización estándar) Habilita la entrega de anuncios en sitios no auditados. Cuando la ubicación se dirige al inventario privado, esta opción puede enviar anuncios en sitios bloqueados.

**[!UICONTROL Paste list of targeted sites]:** Le permite dirigirse únicamente a sitios específicos. Cuando activa esta opción, se desactivan las demás opciones de segmentación del sitio.

**[!UICONTROL Sites]:** (disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL On]*) sitios de destino. Puede buscar y seleccionar sitios, o bien escribir o pegar nombres de dominio:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los sitios:
   * Para buscar un sitio:
      1. Haga clic en **[!UICONTROL Search]**.
      1. Introduzca una palabra clave, seleccione un nivel de sitio y/o seleccione una categoría de sitio.
      1. En los resultados de búsqueda, seleccione los sitios que desea incluir:
         * Para excluir un sitio individual, active la casilla de verificación adyacente.
         * (Cuando haya más de 50 resultados disponibles) Para incluir los primeros 50 resultados, haga clic en **[!UICONTROL Include these 50]**. Para incluir todos los resultados de búsqueda, haga clic en **[!UICONTROL Include these \<*NN *\>]**.
   * Para introducir nombres de dominio:
      1. haga clic en **[!UICONTROL Paste]**.
      1. Escriba uno o varios nombres de dominio en líneas independientes.
      1. Haga clic en **[!UICONTROL Include All]**.
1. Haga clic en **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Cualquier destino de audiencia para la ubicación, incluidos [segmentos de terceros, segmentos de origen, segmentos de Adobe, segmentos personalizados y audiencias guardadas](/help/dsp/audiences/audience-settings.md). También se muestra el tamaño de audiencia deduplicada total y activa en todos los segmentos seleccionados y en las audiencias guardadas. Puede seleccionar una audiencia existente, crear una audiencia que pueda reutilizar posteriormente o seleccionar segmentos de audiencia específicos:

* Para seleccionar una audiencia existente, haga clic en ![Seleccionar](/help/dsp/assets/chevron-down.png) al lado de [!UICONTROL Included Audiences] y luego seleccione la audiencia.
* Para crear una audiencia, haga clic en ![Seleccionar](/help/dsp/assets/chevron-down.png) al lado de [!UICONTROL Included Audiences] y luego seleccione **[!UICONTROL + Create Audience]**. Para obtener instrucciones, consulte [Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md), a partir del paso 3.
* Para seleccionar segmentos de audiencia específicos, haga clic en **[!UICONTROL Select segments for this placement only]**. Seleccione la lógica del segmento; para obtener instrucciones, consulte el paso 6 en &quot;[Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md)&quot;. Cuando hayas terminado, haz clic en **Guardar**.

**[!UICONTROL Excluded Audiences]:** Cualquier audiencia que se excluya para la ubicación, incluidas las audiencias con [segmentos de terceros, segmentos de origen, segmentos de Adobe, segmentos personalizados y audiencias guardadas](/help/dsp/audiences/audience-settings.md). También se muestra el tamaño de audiencia deduplicada total y activa en todas las audiencias excluidas. Puede seleccionar una audiencia existente o crear una nueva que pueda reutilizar más adelante:

* Para seleccionar una audiencia existente, haga clic en ![Seleccionar](/help/dsp/assets/chevron-down.png) al lado de [!UICONTROL Excluded Audiences] y luego seleccione la audiencia.

* Para crear una audiencia, haz clic en ![Seleccionar](/help/dsp/assets/chevron-down.png) al lado de [!UICONTROL Excluded Audiences] y, a continuación, selecciona **+ Crear audiencia**. Para obtener instrucciones, consulte [Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md), a partir del paso 3.

**[!UICONTROL Targeting]:** Tipos de ID de usuario que se van a asignar. No puede cambiar esta configuración después de que la ubicación esté activa (es decir, después de que haya comenzado el vuelo).

Al seleccionar ID heredados e ID universales, se da preferencia de oferta a los ID universales.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (predeterminado) segmenta a los usuarios en función de sus cookies, ID de publicidad móvil o ID de TV (CTV) conectados. Los ID se seleccionan en función del inventario del explorador, la aplicación o CTV.

* *[!UICONTROL Universal ID Beta]*: identifica ID centrados en la privacidad del usuario; seleccione un tipo de ID. Las opciones disponibles están determinadas por los destinos geográficos seleccionados en la sección [!UICONTROL Geo-Targeting]. Se utiliza con [[!DNL RampID] segmentos importados directamente a DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [segmentos para los cuales DSP convierte su PII en ID universales](/help/dsp/audiences/sources/source-about.md) o [segmentos personalizados que rastrean ID universales](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*: los identificadores de objetivos [!DNL ID5] se crearon probabilísticamente a partir de direcciones de correo electrónico y otras señales.<!-- What countries/geos are these available for? Everywhere?--> ID5 ID están disponibles sin cargo. **Nota:** Los segmentos de terceros de [!DNL Eyeota] pueden incluir ID5.

   * *[!UICONTROL RampID]*: Destinos [!DNL LiveRamp] [!DNL RampIDs] de usuarios que iniciaron sesión en el sitio mediante sus direcciones de correo electrónico.<!-- Verify --> [!DNL RampIDs] están disponibles para los usuarios de Norteamérica, Australia y Nueva Zelanda.

   * *[!UICONTROL Unified ID2.0]*: segmenta los ID de [!DNL Unified ID2.0] (UID2) de los usuarios que iniciaron sesión en el sitio mediante sus direcciones de correo electrónico.<!-- Verify -->[!DNL UID2 IDs] no están disponibles para los usuarios del Área Económica Europea y algunos países adicionales. Ver la [lista de países prohibidos](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: contrato de términos de servicio para usar identificadores universales. Usted u otro usuario de la cuenta de DSP deben aceptar los términos una vez antes de poder convertir los datos a un nuevo tipo de ID. Para los clientes con contratos de servicio administrado, su equipo de cuenta de Adobe recibirá su consentimiento y aceptará los términos en nombre de su organización. Para leer los términos, haga clic en **>**. Para aceptar los términos, desplácese hasta la parte inferior de los términos y haga clic en **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (disponible cuando la campaña [está configurada para la segmentación entre dispositivos basada en personas](/help/dsp/campaign-management/campaigns/campaign-settings.md), solo se segmentan los ID heredados (no los ID universales) y se selecciona al menos un segmento o una audiencia. Permite ampliar el direccionamiento a todos los dispositivos conocidos de una persona (según el gráfico del dispositivo especificado en la configuración de la campaña), incluso a los dispositivos que no están en los segmentos especificados. Se pueden aplicar tarifas según el gráfico especificado para la campaña. Los datos de gráficos de dispositivos solo están disponibles en Norteamérica.

**[!UICONTROL Placement Cap]:** (opcional) la cantidad de veces que un dispositivo único, un identificador universal o una persona (según el [!UICONTROL Cross Device Level] especificado para la campaña y la configuración [!UICONTROL Targeting] de la ubicación) se pueden mostrar como anuncios desde la ubicación. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
> Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respeta el límite de frecuencia más estricto en la jerarquía de campañas.

**[!UICONTROL Secondary Cap]:** (opcional; disponible cuando se incluye un elemento numérico [!UICONTROL Placement Cap]) Una limitación adicional dentro de los límites del límite de ubicación principal. Seleccione el número de impresiones y el período de tiempo (por ejemplo, 3 por 12 horas).

**[!UICONTROL Day Parting]:** (Opcional) Días específicos de la semana y la hora del día en que se pueden ejecutar los anuncios. Para especificar intervalos de partición de día:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Seleccione la zona horaria aplicable.
1. Especifique los intervalos:
   * Para seleccionar un intervalo preestablecido, haga clic en uno de los botones de intervalo. Las opciones incluyen *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* o *[!UICONTROL Prime]* (primetime).
   * Para seleccionar manualmente un intervalo, haga clic dentro de una celda y, opcionalmente, arrastre para seleccionarlo.
1. Haga clic en **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (opcional; disponible para anunciantes configurados con [!DNL Proximic by Comscore] segmentos) Nombres de segmento o ID específicos de [!DNL Proximic by Comscore] que se incluirán como destinos. Se pueden aplicar tarifas adicionales para esta función. Para activar esta función y configurar segmentos de temas, póngase en contacto con el equipo de cuenta de Adobe.

Para especificar la segmentación de temas:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los segmentos que desea segmentar:
   1. En la columna izquierda, seleccione el socio: (*[!UICONTROL Comscore]*).
   1. En el campo de entrada, introduzca los nombres o ID de los segmentos.
1. (Opcional) Para descargar un archivo CSV con la información del tema en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Haga clic en **[!UICONTROL Save]**.

>[!TIP]
>
>* La segmentación de temas limita el inventario en el que se puede pujar, por lo que debe utilizar la segmentación de temas solo para un pequeño porcentaje de la compra general.
>
>* Configure cualquier objetivo negativo dentro del segmento en [!DNL Proximic by Comscore].

**[!UICONTROL Device Targeting]:** (Opcional) Información específica del dispositivo, incluidos los tipos de dispositivos, fabricantes, sistemas operativos, exploradores y tipos de conectividad, que se incluirán y excluirán como destinos. Los tipos varían según el tipo de ubicación. Para especificar la segmentación del dispositivo:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los detalles del dispositivo que desea incluir y excluir:
   1. En la columna izquierda, seleccione la categoría.
   1. Especifique el objetivo:
      * Para incluir un valor, haga clic en **[!UICONTROL Include]** junto al nombre del valor.
      * Para excluir un valor, haga clic en **[!UICONTROL Exclude]** junto al nombre del valor.
1. (Opcional) Para descargar un archivo CSV con la información de segmentación del dispositivo en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Haga clic en **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Opcional) Proveedores de servicios de Internet (ISP) específicos para incluir o excluir (pero no ambos) como destinos. Para especificar la segmentación del ISP:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los ISP que desea incluir o excluir:
   * Para incluir ISP:
      1. Haga clic en **[!UICONTROL Include ISPs]**.
      1. (Opcional) Filtre la lista por palabra clave.
      1. Seleccione la casilla de verificación situada junto a cada ISP que desee segmentar.
   * Para excluir los ISP:
      1. Haga clic en **[!UICONTROL Exclude ISPs]**.
      1. (Opcional) Filtre la lista por palabra clave.
      1. Seleccione la casilla de verificación situada junto a cada ISP que desee excluir.
1. (Opcional) Para descargar un archivo CSV con la información de segmentación del ISP en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Haga clic en **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (opcional; solo para clientes de [!DNL DoubleVerify]; disponible solo para la visualización de escritorio previa a la emisión, la visualización estándar y de clic para reproducción y las ubicaciones de vídeo y visualización nativas; no compatible con [ubicaciones predeterminadas garantizadas mediante programación para ofertas](/help/dsp/inventory/programmatic-guaranteed-about.md)) Un ID de segmento de [!DNL DoubleVerify Authentic Brand Safety] asociado a la cuenta de la organización [!DNL DoubleVerify] que se utilizará para la ubicación. Especificar un ID bloquea las impresiones después de la oferta utilizando las reglas de seguridad de marca personalizadas configuradas para el ID de segmento especificado. DSP factura a su cuenta por el uso del ID de segmento.

El ID debe comenzar por &quot;51&quot; y constar de ocho dígitos. De forma predeterminada, si se especifica un ID de segmento en la configuración de cuenta del anunciante, se introduce el ID de nivel de anunciante, pero puede cambiarlo para utilizar un segmento diferente o eliminar el ID para deshabilitar la función.

**[!UICONTROL Contextual filtering]:** (aplicable a anuncios de vídeo, nativos y de visualización web móvil y de escritorio) Se deben aplicar los tipos de filtros contextuales [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] y [!DNL Peer39]. Los valores predeterminados de nivel de anunciante están seleccionados para nuevas ubicaciones, pero puede cambiar la configuración:

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de contexto de inventario que se bloquearán de forma predeterminada. Se pueden aplicar tarifas adicionales.

* [!UICONTROL Peer 39]:

   * **Sitios de destino que son:** (opcional) Uno o más tipos de atributos de inventario que se van a destinar de manera predeterminada. Se pueden aplicar tarifas adicionales.

* [!UICONTROL ComScore]:

   * **Bloquear sitios que:** (Opcional) Uno o más tipos de atributos de inventario que se van a bloquear de manera predeterminada. Se pueden aplicar tarifas adicionales.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Opcional) Grado de contenido para adultos para el que se bloquearán los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (el valor predeterminado), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Se pueden aplicar tarifas adicionales.

   * **[!UICONTROL Alcohol Content]:** (Opcional) Grado de contenido alcohólico para el que se bloquearán los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (predeterminado), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Pre-bid fraud blocking]:** Tipos de sitios que se bloquearán según el tráfico fraudulento y las actividades sospechosas medidas a través de [!DNL DoubleVerify], [!DNL Integral Ad Science] y [!DNL Peer39]. Los valores predeterminados de nivel de anunciante están seleccionados para nuevas ubicaciones, pero puede cambiar la configuración:

* [!UICONTROL DoubleVerify]: (Aplicable a anuncios de escritorio, de visualización web móvil, nativos y de vídeo) <!-- Applicable for desktop and mobile web display, native, video, and standard connected TV ads -->

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** De forma predeterminada, bloquea todo el tráfico 100% no válido, incluido el tráfico en dispositivos secuestrados, para las nuevas ubicaciones. Se pueden aplicar tarifas adicionales.

   * **[!UICONTROL Also block sites with]:** (Opcional) Un nivel adicional de fraude y tráfico no válido que hace que DSP bloquee los anuncios de forma predeterminada: *[!UICONTROL None]* (el valor predeterminado, que no bloquea el tráfico adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* o *[!UICONTROL >25% Average Fraud/IVT levels]*. Se pueden aplicar tarifas adicionales.

* [!UICONTROL Peer 39]: (aplicable a anuncios de escritorio, móviles, nativos y de vídeo)

   * **[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de fraude que hacen que DSP bloquee los anuncios de forma predeterminada: *[!UICONTROL Fraud]* (que bloquea todos los sitios con fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* o *[!UICONTROL Fraud: Zero Ads]*. Se pueden aplicar tarifas adicionales.

* [!UICONTROL Integral Ad Science]: (aplicable a anuncios de escritorio, móviles, nativos y de vídeo)

   * **[!UICONTROL Block sites that are]:** (Opcional) Tipo de actividad sospechosa en un sitio web o aplicación que hace que DSP bloquee los anuncios de forma predeterminada: *[!UICONTROL None]* (el valor predeterminado, que no bloquea los anuncios basándose en actividades sospechosas), *[!UICONTROL Suspicious Activity - High Risk]* o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Pre-bid viewability]:** (aplicable a anuncios de vídeo, nativos y de pantalla web móvil y de escritorio) que filtra la visibilidad de oferta previa por [!DNL DoubleVerify] y [!DNL Integral Ad Science] para solicitar la ubicación. Los valores predeterminados de nivel de anunciante están seleccionados para nuevas ubicaciones, pero puede cambiar la configuración. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Ads.txt filtering]:** (aplicable a anuncios de escritorio, web móvil, nativos, de vídeo y audio) Qué nivel de filtrado de oferta previa de [Ads.txt](https://iabtechlab.com/ads-txt-about/) debe usarse aplicando la lista Vendedores digitales autorizados de cada editor. El nivel de anunciante predeterminado está seleccionado para nuevas ubicaciones, pero puede cambiar la configuración:

* *[!UICONTROL Opt out of ads.txt (default)]*: para comprar inventario a todos los vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: para priorizar la compra de inventario a los vendedores directos y revendedores autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar inventario solamente de vendedores y revendedores directos autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar inventario solamente de los vendedores directos autorizados de un dominio.

**[!UICONTROL Attention Targeting]:** (aplicable a pantallas web de escritorio y móviles, vídeo y anuncios de TV conectados estándar) Segmenta [!DNL Adelaide] segmentos de oferta previa con un nivel de atención específico (alto, medio o bajo) según el sitio, el formato y el tamaño del anuncio especificados. Los segmentos se actualizan semanalmente. **Nota:** Al usar [!DNL Adelaide] segmentos para la segmentación, se incurre en una tarifa de CPM por cada impresión que se entrega con una segmentación de atención de [!DNL Adelaide]; esta tarifa es independiente de las tarifas de [medición de atención](/help/dsp/campaign-management/campaigns/campaign-settings.md). Para las ubicaciones interactivas previas a la emisión, solo se te cobrarán las impresiones VAST.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] ubicaciones) Los proveedores de seguimiento de terceros aprobados por [!DNL Roku] incluyen [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] y [!DNL Research Now].

**[!UICONTROL Event Pixels]:** píxeles de seguimiento de eventos de terceros (opcionales) que se adjuntarán de forma predeterminada a todos los anuncios nuevos de la ubicación. Para especificar píxeles de evento:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para seleccionar un píxel existente, marque la casilla de verificación en la fila de píxeles.
   * Para crear un píxel:
      1. Haga clic en **[!UICONTROL Create]**.
      1. Introduzca la siguiente información:
         * **[!UICONTROL Pixel name]:** El nombre del píxel; la longitud máxima es de 500 caracteres. Utilice un nombre que le ayude a identificar fácilmente el píxel.
         * **[!UICONTROL Pixel event fires on]:** Evento que déclencheur el píxel que se va a activar. Los eventos disponibles varían según el tipo de anuncio.
         * **[!UICONTROL Pixel type]:** Indica si el píxel es *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** Dirección URL de la imagen en píxeles.
      1. Haga clic en **[!UICONTROL Create and attach]**.
   1. Haga clic en **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (opcional) píxeles de seguimiento de conversión que se adjuntarán de forma predeterminada a todos los anuncios nuevos de la ubicación. Para especificar píxeles de conversión:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para seleccionar un píxel existente, marque la casilla de verificación en la fila de píxeles.
   * Para crear un píxel:
      1. Haga clic en **[!UICONTROL Create]**.
      1. Introduzca la siguiente información:
         * **[!UICONTROL Conversion pixel name]:** El nombre del píxel; la longitud máxima es de 500 caracteres. Utilice un nombre que le ayude a identificar fácilmente el píxel.
         * **[!UICONTROL Conversion category]:** El tipo de conversión.
         * **[!UICONTROL Impression conversion window]:** Número de días después de que se produzca una impresión de anuncio en los que la impresión puede atribuirse a una conversión. El valor predeterminado es de 30 días.
         * **[!UICONTROL Click conversion window]:** Número de días después de que se produzca un clic en un anuncio en los que el clic puede atribuirse a una conversión. El valor predeterminado es de 30 días.
         * **[!UICONTROL Notes]:** (opcional) descripción u otra información sobre el píxel.
      1. Haga clic en **[!UICONTROL Create and attach]**.
      1. Implemente el píxel de conversión en las páginas web relevantes:
         1. En el menú principal, vaya a **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. En la fila de píxeles, haga clic en **[!UICONTROL edit]**.
         1. Copie los valores de los campos [!UICONTROL HTML Tag] y [!UICONTROL Flash Tag], según sea necesario, para proporcionárselos al anunciante o al contacto del sitio web.

            Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.
   1. Haga clic en **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Opcional) Una tarifa estática de cargo de terceros que se rastreará como un costo no facturable por 1000 impresiones. El valor predeterminado de nivel de paquete se aplica automáticamente a las nuevas ubicaciones, cuando corresponda, a menos que introduzca un valor diferente.

>[!NOTE]
>
>Las tarifas facturables se reflejan en la métrica [!UICONTROL Net CPM].

>[!MORELIKETHIS]
>
>* [Acerca de la administración de ubicaciones](placement-about.md)
>* [Crear una ubicación](placement-create.md)
>* [Editar ubicaciones](placement-edit.md)
>* [Administrar multiplicadores de oferta para ubicaciones](placement-manage-bid-multipliers.md)
>* [Ver el registro de cambios de una ubicación](placement-change-log.md)
>* [Métodos abreviados de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Preguntas frecuentes sobre la administración de campañas](/help/dsp/campaign-management/faq-campaign-management.md)
