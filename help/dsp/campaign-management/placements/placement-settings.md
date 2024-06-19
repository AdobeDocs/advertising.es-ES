---
title: Configuración de ubicación
description: Consulte las descripciones de la configuración de ubicación disponible.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 80b584c124e247e97e8a21153abf30072c361c42
workflow-type: tm+mt
source-wordcount: '3857'
ht-degree: 0%

---

# Configuración de ubicación

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** El nombre de la ubicación.

>[!TIP]
>Utilice una convención de nombres que tenga sentido para su situación. Una convención de nombres sugerida es &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** El estado de la ubicación: *[!UICONTROL Active]* (el valor predeterminado) o *[!UICONTROL Paused]*.

>[!TIP]
>La práctica recomendada es pausar la ubicación hasta que esté listo para iniciarla.

**[!UICONTROL Details]:** (Solo lectura) El tipo de anuncio aplicable, la cuenta que crea o crea la ubicación y la campaña principal. Para ver más detalles, haga clic en **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Abre una lista de plantillas de ubicación existentes. Para rellenar automáticamente la configuración de direccionamiento desde una plantilla:

1. Realice una de las acciones siguientes:

   * Para reutilizar todos los destinos de una plantilla, active la casilla de verificación situada junto al nombre de la plantilla.

   * Para reutilizar tipos de destino individuales de una plantilla, expanda el nombre de la plantilla y active la casilla de verificación situada junto a los tipos de destino que desea reutilizar.

1. Clic **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Solo formatos de anuncio de vídeo) La duración del anuncio o las especificaciones del anuncio, que se utilizan para calcular la proyección de Forecast a la derecha. Los campos varían según el tipo de anuncio.

**[!UICONTROL Environment]:** (Solo formato de anuncio de vídeo universal) Los entornos de dispositivo (escritorio, móvil, TV conectada) que se incluirán como destinos en la ubicación. Especifique al menos uno.

En los informes personalizados, la dimensión de nivel de ubicación &quot;Entorno del dispositivo&quot; indica el entorno de destino.

**[!UICONTROL Placement tags]:** (Opcional) Palabras clave o apodos para ayudarle a localizar esta ubicación.

## Metas

**[!UICONTROL Package]:** (Opcional) Un paquete al que se asigna la ubicación. Clic ![Editar](/help/dsp/assets/edit.png) para seleccionar un paquete existente o crear un paquete. Al asignar la ubicación a un paquete, la variable [!UICONTROL Goals] se actualiza con las fechas de vuelo, el objetivo de envío y el presupuesto del paquete.

**[!UICONTROL Flight Dates]:** La fecha de inicio y la fecha de finalización de la ubicación. Los anuncios aprobados pueden ejecutarse durante el vuelo cuando la ubicación esté activa y asignada a un paquete o campaña activos.

Las fechas del paquete (cuando corresponda) o de la campaña se rellenan automáticamente de forma predeterminada.

>[!NOTE]
>
>* Las fechas de vuelo deben incluirse en las fechas de vuelo de la campaña y en las fechas de vuelo del paquete.

### Ubicaciones asignadas a paquetes con ritmo de nivel de paquete

**[!UICONTROL Placement Funding]:** Cómo presupuestar la ubicación:

* *[!UICONTROL Optimize based on performance]:* Controla el presupuesto en el nivel de paquete.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Permite establecer un presupuesto de colocación mínimo o máximo. Especifique al menos un tipo de presupuesto:

   * *[!UICONTROL Maximum Budget]*: introduzca un valor y la duración (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: el presupuesto mínimo como porcentaje del presupuesto del paquete. Cuando se especifica un límite de intervalo, el valor de presupuesto mínimo siempre se calcula como un porcentaje del límite de intervalo. De lo contrario, se calcula como un porcentaje del presupuesto del paquete.

**[!UICONTROL Max Bid]:** El máximo para pagar 1000 impresiones.

**[!UICONTROL Placement Pre-bid Filters]:** Hasta cinco umbrales de KPI (como una métrica mínima de visibilidad o una tasa de pulsaciones) que deben cumplirse para que se produzca la oferta. Puede usar filtros de oferta previa como tácticas de optimización, pero tenga en cuenta que cada regla puede limitar las oportunidades en las que esta ubicación puede pujar. Para añadir o editar filtros:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las acciones siguientes:
   * Para añadir un filtro:
      1. Clic **[!UICONTROL Add Filter]**.
      1. Junto a **[!UICONTROL Only bid if]**, seleccione una métrica y, a continuación, introduzca un valor.
   * Para quitar un filtro, haga clic en **[!UICONTROL X]** en la fila de filtro.
1. Clic **[!UICONTROL Save]**.

Consulte las descripciones de cada filtro de oferta previa en &quot;[Filtros previos a la oferta de nivel de ubicación y cómo utilizarlos](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Todas las demás ubicaciones

**[!UICONTROL Budget Goal]:** El límite presupuestario bruto y el intervalo presupuestario (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Ubicaciones en campañas solo con administración de márgenes) El límite presupuestario bruto y el intervalo presupuestario (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  El objetivo de optimización del paquete. Consulte las descripciones de cada objetivo de optimización en &quot;[Objetivos de optimización y cómo utilizarlos](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** El objetivo, que se utiliza para rastrear el rendimiento.

>[!NOTE]
>
>Este campo es solo un punto de referencia y no se utiliza para la toma de decisiones.

**[!UICONTROL Pace on]:** La base del ritmo:

* **[!UICONTROL Budget goal]:** (Predeterminado) Esta opción ofrece tantas impresiones como sea posible dentro del presupuesto asignado.

* **[!UICONTROL Impressions]:** Esta opción envía impresiones hasta que se alcanza una cantidad especificada dentro de un intervalo especificado. Cuando seleccione esta opción, especifique el número de impresiones y el intervalo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** El máximo para pagar 1000 impresiones.

**[!UICONTROL Flight pacing]:** (Ubicaciones solo con ritmo de nivel de ubicación) Cómo espaciar la entrega de anuncios:

* *[!UICONTROL Even]:* (Predeterminado) Coloca la entrega de forma uniforme durante cada vuelo, con un objetivo del 50 % de la entrega en la primera mitad del vuelo.

* *[!UICONTROL Slightly Ahead]:* (Predeterminado) Acelera la entrega de modo que se complete en un 55-65 % a mitad de la duración del vuelo.

* *[!UICONTROL Frontload]:* Acelera la entrega para que se complete en un 65-75% a mitad del vuelo.

* *[!UICONTROL Aggressive Frontload]:* Acelera la entrega para que se complete en un 75-85% a mitad del vuelo.

**[!UICONTROL Intraday pacing]:** (Ubicaciones solo con ritmo de nivel de ubicación) Cómo realizar el ritmo y la entrega a lo largo de cada día dentro del vuelo:

* *[!UICONTROL Even]:* (El valor predeterminado) Escala el envío según la disponibilidad del inventario. Por lo general, se publican más anuncios por hora durante el día, cuando el volumen de subasta es mayor, y menos anuncios por las mañanas y las noches.

* *[!UICONTROL ASAP]:* (El valor predeterminado) Acelera la entrega al doble de velocidad que *Uniforme*.

  >[!CAUTION]
  >
  >Esta opción puede afectar negativamente al rendimiento. Utilícelo únicamente cuando priorice completamente la entrega y gaste en lugar de optimizar el rendimiento.

**[!UICONTROL Placement Pre-bid Filters]:** (Opcional) Hasta cinco filtros que deben cumplirse para que se produzca la puja. Puede usar filtros de oferta previa como tácticas de optimización, pero tenga en cuenta que cada regla puede limitar las oportunidades en las que esta ubicación puede pujar. Para añadir o editar filtros:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las acciones siguientes:
   * Para añadir un filtro:
      1. Clic **[!UICONTROL Add Filter]**.
      1. Junto a **[!UICONTROL Only bid if]**, seleccione una métrica y, a continuación, introduzca un valor.
   * Para quitar un filtro, haga clic en **[!UICONTROL X]** en la fila de filtro.
1. Clic **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Opcional) Ubicaciones específicas en las que incluir o excluir anuncios en la ubicación. Si no especifica ninguna ubicación, se segmentarán todas las ubicaciones.

>[!NOTE]
>
>Las ubicaciones de ciudad y DMA no están disponibles para las ubicaciones de Roku.

Para especificar ubicaciones:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para incluir o excluir un país, estado, ciudad, DMA, distrito legislativo federal o distrito legislativo estatal:
      1. Seleccione el tipo de ubicación en la columna izquierda.
      1. (Según sea necesario) Haga clic en una ubicación para expandirla.
      1. Junto a la ubicación, haga clic en *[!UICONTROL Include]* para incluirlo como destino o *[!UICONTROL Exclude]* para excluirlo como objetivo.
   * Para buscar un código postal e incluir o excluir todos los resultados seleccionados:
      1. Clic **[!UICONTROL Search Postal Code]**.
      1. Seleccione el país.
      1. Introduzca el nombre de la ciudad y haga clic en ![Editar](/help/dsp/assets/search.png).
      1. Haga clic en el resultado de búsqueda correcto.
      1. Clic *[!UICONTROL Include All]* para incluir todas las ubicaciones como destinos o *[!UICONTROL Exclude All]* para excluir todas las ubicaciones como destinos.
   * Para introducir o pegar códigos postales e incluirlos o excluirlos todos:
      1. Clic **[!UICONTROL Paste Postal Code]**.
      1. Seleccione el país.
      1. Introduzca o pegue hasta 1000 códigos postales.
Incluya un código postal por línea o introduzca varios valores separados por comas o tabulaciones.
      1. Clic *[!UICONTROL Include All]* para incluir todas las ubicaciones como destinos o *[!UICONTROL Exclude All]* para excluir todas las ubicaciones como destinos.
   * Para quitar una ubicación de [!UICONTROL Included] o [!UICONTROL Excluded] , haga clic en **[!UICONTROL X]** situado junto a la ubicación en la columna derecha.
1. Clic **[!UICONTROL Done]**.

>[!NOTE]
>
>* No todos los países tienen ubicaciones de estado, ciudad o código postal.
>* DMA (área de mercado designada), distritos legislativos federales y distritos legislativos estatales solo están disponibles para ubicaciones de EE. UU.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Orígenes de inventario que se deben incluir o excluir como destinos. Para la mayoría de los tipos de ubicación, todos los tipos de inventario y todos los orígenes de cada tipo se incluyen de forma predeterminada. Para [!DNL Roku] ubicaciones, debe especificar el tipo de inventario y los orígenes. Puede elegir entre los siguientes tipos de inventario:

* [!UICONTROL Public]DSP : (Todos los tipos de ubicación excepto Roku) Todos los inventarios de intercambio abiertos a los que tiene acceso la. Puede incluir y excluir el inventario público.

  Puede ver la lista por origen o por fuente. Cuando vea la lista por fuente, puede buscar por nombre de fuente, clave de fuente o una etiqueta de característica seleccionada.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: sus ofertas privadas existentes (o las ofertas privadas existentes) [!DNL Roku] ofertas para [!DNL Roku] DSP ubicaciones) con los editores que ha configurado en el sitio de trabajo de la versión de la aplicación de. Puede incluir, pero no excluir, el inventario público.

  Puede buscar en la lista por palabra clave, clave, ID de oferta o etiqueta personalizada.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Opcional) Anula el algoritmo de precio de oferta para pujar al menos los precios fijos y mínimos de las ofertas.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: todos [premium, no garantizado [!UICONTROL On Demand] inventario](/help/dsp/inventory/on-demand-inventory-about.md) (o [!UICONTROL On Demand] [!DNL Roku] ofertas para [!DNL Roku] ubicaciones) a las que se ha suscrito en [!DNL DSP]. Puede incluir y excluir [!UICONTROL On Demand] inventario.

  Puede ver la lista por origen o por fuente. Cuando vea la lista por fuente, puede buscar por nombre de fuente, clave de fuente o una región de editor, etiqueta de categoría o etiqueta característica seleccionada.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Opcional) Anula el algoritmo de precio de oferta para pujar al menos los precios fijos y mínimos de las ofertas.

Para especificar la segmentación de inventario:

* Para excluir un tipo de inventario, desactive la casilla de verificación situada junto al nombre.
* Para dirigirse a un tipo de inventario:
   1. Active la casilla de verificación situada junto al nombre del tipo de inventario.
   1. (Opcional) Cambie los orígenes para incluir lo siguiente:
      1. Clic ![Editar](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] y [!UICONTROL On Demand] inventory) Haga clic **[!UICONTROL View by Source]** o **[!UICONTROL View by Feed]** para cambiar la forma en que se enumeran las fuentes.
      1. (Cuando corresponda) Filtre el inventario según sea necesario.
      1. Especifique las fuentes que desea incluir y excluir:
         * Para incluir un [!UICONTROL Public] o [!UICONTROL On Demand] origen, haga clic en **[!UICONTROL Include]** junto al nombre de origen.
         * Para incluir [!UICONTROL Private] fuentes:
            * Para incluir todo el inventario en una oferta, haga clic en **[!UICONTROL Include all]** junto al nombre de la oferta.
            * Para incluir un origen de inventario individual, expanda el nombre de la oferta y, a continuación, haga clic en la casilla de verificación situada junto al nombre del origen.
         * Para excluir un [!UICONTROL Public] o [!UICONTROL On source], haga clic en **[!UICONTROL Exclude]** junto al nombre de origen.
   1. (Opcional) Para descargar un archivo CSV con la información de objetivo en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Save & Export]**.
   1. Clic **[!UICONTROL Save]**.

>[!TIP]
>
>Si se ha suscrito a [!UICONTROL On Demand] realizar un inventario, pero no puede localizar los editores ni las ofertas que se van a segmentar y, a continuación, comprobar el estado de las ofertas. Para obtener más información sobre los estados, consulte [Acerca de [!DNL On Demand] Inventario Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Solo ubicaciones de vídeo) Excluye el tráfico de salida.

Los anuncios salientes suelen aparecer sobre el contenido como una ventana emergente o rellenos de contenido (en la experiencia nativa), en lugar de como anuncios de vídeo normales en un reproductor de vídeo.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** Los tipos de tráfico de destino. Las opciones incluyen **[!UICONTROL Websites]** y **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) La calidad de los sitios de destino. DSP Los niveles 1-3 son todos seguros para la marca y han sido aprobados por el equipo de mapeo de la marca de la.

* *[!UICONTROL Tier 1]:* Sitios y aplicaciones Premium reconocibles a nivel nacional.

* *[!UICONTROL Tier 2]:* Se dirige al nivel 1, así como a sitios y aplicaciones de calidad menos conocidos que el nivel 1.

* *[!UICONTROL Tier 3]:* Se dirige a los niveles 1-2, además de sitios y aplicaciones legítimos y seguros para la marca que se adaptan a una audiencia específica. Utilice el nivel 3 para las compras de alcance o segmentación de datos.

* *[!UICONTROL All Sites]:* Se dirige a los niveles 1-3 y al nuevo inventario que no se ha examinado ni clasificado, y que puede utilizar para llegar a ellos.

>[!NOTE]
>
>El inventario es específico de las unidades de anuncio de la ubicación.

>[!TIP]
>
>Para las campañas de rendimiento, la práctica recomendada es seleccionar *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Opcional; disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) Categorías de sitio dentro de los niveles de sitio seleccionados para incluirlas o excluirlas (pero no ambas) como destinos. DSP Elija entre las listas verticales de sitios que ha asignado el usuario en función del asunto:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Especifique las categorías del sitio que se incluirán o excluirán:
   * Para incluir categorías de sitio:
      1. Clic **[!UICONTROL Include categories]**.
      1. Seleccione la casilla de verificación situada junto a cada categoría de destino.
   * Para excluir las categorías del sitio:
      1. Clic **[!UICONTROL Exclude categories]**.
      1. Seleccione la casilla de verificación situada junto a cada categoría que desee excluir.
1. (Opcional) Para descargar un archivo CSV con la información de objetivo en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Opcional; disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) Sitios que excluir. Puede buscar y seleccionar sitios, o bien escribir o pegar nombres de dominio:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Especifique los sitios:
   * Para buscar un sitio:
      1. Clic **[!UICONTROL Search]**.
      1. Introduzca una palabra clave, seleccione un nivel de sitio y/o seleccione una categoría de sitio.
      1. En los resultados de búsqueda, seleccione los sitios que desea excluir:
         * Para excluir un sitio individual, active la casilla de verificación adyacente.
         * (Cuando haya más de 50 resultados disponibles) Para excluir los primeros 50 resultados, haga clic en **[!UICONTROL Exclude these 50]**. Para excluir todos los resultados de la búsqueda, haga clic en **[!UICONTROL Exclude these \<*NN *\>]**.
   * Para introducir nombres de dominio:
      1. Clic **[!UICONTROL Paste]**.
      1. Escriba uno o varios nombres de dominio en líneas independientes.
      1. Clic **[!UICONTROL Exclude All]**.
1. Clic **[!UICONTROL Done]** cuando hayas terminado.

>[!NOTE]
>
>* DSP También se aplican listas de sitios bloqueados a nivel de cuenta y de anunciante, además de la lista de sitios bloqueados a nivel de [lista de sitios bloqueados globalmente](/help/dsp/introduction/features/brand-safety-media-quality.md), que incluye sitios considerados inseguros para los anuncios.
>* Las listas de sitios bloqueados siempre anulan las listas de sitios de destino. Si una ubicación excluye e incluye el mismo destino para un anuncio, se excluye el destino.

**[!UICONTROL Language]:** (Opcional) Un solo idioma de destino.

**[!UICONTROL Site List Preview]:** (Solo lectura) Todos los sitios segmentados y bloqueados para la ubicación.

Si lo desea, puede exportar la lista de sitios de destino y bloqueados como archivo de valores separados por comas (CSV). Para exportar la lista, haga clic en **[!UICONTROL Export full site list]** y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador.

**[!UICONTROL Allow unscreened sites]:** (Solo ubicaciones de visualización estándar) Habilita la entrega de anuncios en sitios no auditados. Cuando la ubicación se dirige al inventario privado, esta opción puede enviar anuncios en sitios bloqueados.

**[!UICONTROL Paste list of targeted sites]:** Permite dirigirse únicamente a sitios específicos. Cuando activa esta opción, se desactivan las demás opciones de segmentación del sitio.

**[!UICONTROL Sites]:** (Disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL On]*) Sitios para segmentar. Puede buscar y seleccionar sitios, o bien escribir o pegar nombres de dominio:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Especifique los sitios:
   * Para buscar un sitio:
      1. Clic **[!UICONTROL Search]**.
      1. Introduzca una palabra clave, seleccione un nivel de sitio y/o seleccione una categoría de sitio.
      1. En los resultados de búsqueda, seleccione los sitios que desea incluir:
         * Para excluir un sitio individual, active la casilla de verificación adyacente.
         * (Cuando haya más de 50 resultados disponibles) Para incluir los 50 primeros resultados, haga clic en **[!UICONTROL Include these 50]**. Para incluir todos los resultados de búsqueda, haga clic en **[!UICONTROL Include these \<*NN *\>]**.
   * Para introducir nombres de dominio:
      1. click **[!UICONTROL Paste]**.
      1. Escriba uno o varios nombres de dominio en líneas independientes.
      1. Clic **[!UICONTROL Include All]**.
1. Clic **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Cualquier destinatario de audiencia para la ubicación, incluidos [segmentos de terceros, segmentos de origen, segmentos de Adobe, segmentos personalizados y audiencias guardadas](/help/dsp/audiences/audience-settings.md). También se muestra el tamaño de audiencia deduplicada total y activa en todos los segmentos seleccionados y en las audiencias guardadas. Puede seleccionar una audiencia existente, crear una audiencia que pueda reutilizar posteriormente o seleccionar segmentos de audiencia específicos:

* Para seleccionar una audiencia existente, haga clic en ![Seleccionar](/help/dsp/assets/chevron-down.png) junto a [!UICONTROL Included Audiences]y, a continuación, seleccione la audiencia.
* Para crear una audiencia, haga clic en ![Seleccionar](/help/dsp/assets/chevron-down.png) junto a [!UICONTROL Included Audiences], y luego seleccione **[!UICONTROL + Create Audience]**. Para obtener instrucciones, consulte [Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md), empezando por el paso 3.
* Para seleccionar segmentos de audiencia específicos, haga clic en **[!UICONTROL Select segments for this placement only]**. Seleccione la lógica del segmento; para obtener instrucciones, consulte el paso 6 en &quot;[Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md).&quot; Cuando haya terminado, haga clic en **Guardar**.

**[!UICONTROL Excluded Audiences]:** Cualquier audiencia que se excluya para la ubicación, incluidas las audiencias con [segmentos de terceros, segmentos de origen, segmentos de Adobe, segmentos personalizados y audiencias guardadas](/help/dsp/audiences/audience-settings.md). También se muestra el tamaño de audiencia deduplicada total y activa en todas las audiencias excluidas. Puede seleccionar una audiencia existente o crear una nueva que pueda reutilizar más adelante:

* Para seleccionar una audiencia existente, haga clic en ![Seleccionar](/help/dsp/assets/chevron-down.png) junto a [!UICONTROL Excluded Audiences]y, a continuación, seleccione la audiencia.

* Para crear una audiencia, haga clic en ![Seleccionar](/help/dsp/assets/chevron-down.png) junto a [!UICONTROL Excluded Audiences], y luego seleccione **+ Crear audiencia**. Para obtener instrucciones, consulte [Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md), empezando por el paso 3.

**[!UICONTROL Targeting]:** Los tipos de ID de usuario a los que dirigirse. No puede cambiar esta configuración después de que la ubicación esté activa (es decir, después de que haya comenzado el vuelo).

Al seleccionar ID heredados e ID universales, se da preferencia de oferta a los ID universales.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (predeterminado) segmenta a los usuarios en función de sus cookies, ID de publicidad móvil o ID de canales de TV conectados. Los ID se seleccionan en función del inventario del explorador, la aplicación o CTV.

* *[!UICONTROL Universal ID Beta]*: identifica ID centrados en la privacidad del usuario; seleccione un tipo de ID. Las opciones disponibles están determinadas por los destinos geográficos seleccionados en la variable [!UICONTROL Geo-Targeting] sección. Uso con [[!DNL RampID] DSP segmentos importados directamente a la dirección de correo electrónico](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [DSP segmentos para los que el convierte su PII en ID universales](/help/dsp/audiences/sources/source-about.md), o [segmentos personalizados que rastrean ID universales](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*: Objetivos [!DNL ID5] ID creados probabilísticamente a partir de direcciones de correo electrónico y otras señales.<!-- What countries/geos are these available for? Everywhere?--> Los ID de ID5 están disponibles sin coste adicional. **Nota:** Segmentos de terceros de [!DNL Eyeota] puede incluir ID5.

   * *[!UICONTROL RampID]*: Objetivos [!DNL LiveRamp] [!DNL RampIDs] de usuarios que iniciaron sesión en el sitio mediante sus direcciones de correo electrónico.<!-- Verify --> [!DNL RampIDs] están disponibles para usuarios de Norteamérica, Australia y Nueva Zelanda.

   * *[!UICONTROL Unified ID2.0]*: Objetivos [!DNL Unified ID2.0] (UID2) ID de usuarios que iniciaron sesión en el sitio mediante sus direcciones de correo electrónico.<!-- Verify -->[!DNL UID2 IDs] no están disponibles para los usuarios del Espacio Económico Europeo y de otros países. Consulte la [lista de países prohibidos](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: contrato de términos de servicio para el uso de ID universales. DSP Usted u otro usuario de la cuenta debe aceptar los términos una vez, para poder convertir los datos a un nuevo tipo de ID. Para los clientes con contratos de servicio gestionado, su equipo de cuenta de Adobe recibirá su consentimiento y aceptará los términos en nombre de su organización. Para leer los términos, haga clic en **>**. Para aceptar los términos, desplácese hasta la parte inferior de los términos y haga clic en **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (Disponible cuando la variable [campaign está configurada para la segmentación entre dispositivos basada en personas](/help/dsp/campaign-management/campaigns/campaign-settings.md), solo se segmentan los ID heredados (no los ID universales) y se selecciona al menos un segmento o audiencia. Permite ampliar el direccionamiento a todos los dispositivos conocidos de una persona (según el gráfico del dispositivo especificado en la configuración de la campaña), incluso a los dispositivos que no están en los segmentos especificados. Se pueden aplicar tarifas según el gráfico especificado para la campaña. Los datos de gráficos de dispositivos solo están disponibles en Norteamérica.

**[!UICONTROL Placement Cap]:** (Opcional) El número de veces que un dispositivo único, ID universal o persona (según el especificado) [!UICONTROL Cross Device Level] para la campaña y la ubicación [!UICONTROL Targeting] configuración) se pueden servir anuncios desde la ubicación. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
> Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respeta el límite de frecuencia más estricto de la jerarquía de campañas.

**[!UICONTROL Secondary Cap]:** (Opcional; disponible cuando se incluye un valor numérico) [!UICONTROL Placement Cap]) Una limitación adicional dentro de los límites del límite de ubicación principal. Seleccione el número de impresiones y el período de tiempo (por ejemplo, 3 por 12 horas).

**[!UICONTROL Day Parting]:** (Opcional) Días específicos de la semana y la hora del día en que se pueden publicar los anuncios. Para especificar intervalos de partición de día:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Seleccione la zona horaria aplicable.
1. Especifique los intervalos:
   * Para seleccionar un intervalo preestablecido, haga clic en uno de los botones de intervalo. Las opciones incluyen *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*, o *[!UICONTROL Prime]* (primetime).
   * Para seleccionar manualmente un intervalo, haga clic dentro de una celda y, opcionalmente, arrastre para seleccionarlo.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Opcional; disponible para anunciantes configurados con [!DNL Proximic by Comscore] y [!DNL Oracle Data Cloud] segmentos) Nombres de segmentos específicos o ID de [!DNL Proximic by Comscore] y [!DNL Oracle Data Cloud] (anteriormente [!DNL Grapeshot]) para incluirlos como destinos. Se pueden aplicar tarifas adicionales para esta función. Para activar esta función y configurar segmentos de temas, póngase en contacto con el equipo de cuenta de Adobe.

Para especificar la segmentación de temas:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Especifique los segmentos que desea segmentar:
   1. En la columna izquierda, seleccione el socio (*[!UICONTROL Comscore]* o *[!UICONTROL Grapeshot]*).
   1. En el campo de entrada, introduzca los nombres o ID de los segmentos.
1. (Opcional) Para descargar un archivo CSV con la información del tema en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

>[!TIP]
>
>* La segmentación de temas limita el inventario en el que se puede pujar, por lo que debe utilizar la segmentación de temas solo para un pequeño porcentaje de la compra general.
>
>* Configure cualquier objetivo negativo dentro del segmento en [!DNL Proximic by Comscore] o [!DNL Oracle Data Cloud].

**[!UICONTROL Device Targeting]:** (Opcional) Información específica del dispositivo, incluidos los tipos de dispositivo, los fabricantes, los sistemas operativos, los navegadores y los tipos de conectividad, que se deben incluir y excluir como objetivos. Para especificar la segmentación del dispositivo:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Especifique los detalles del dispositivo que desea incluir y excluir:
   1. En la columna izquierda, seleccione la categoría.
   1. Especifique el objetivo:
      * Para incluir un valor, haga clic en **[!UICONTROL Include]** junto al nombre del valor.
      * Para excluir un valor, haga clic en **[!UICONTROL Exclude]** junto al nombre del valor.
1. (Opcional) Para descargar un archivo CSV con la información de segmentación del dispositivo en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Opcional) Los proveedores de servicios de Internet (ISP) específicos deben incluir o excluir (pero no ambos) como destinatarios. Para especificar la segmentación del ISP:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Especifique los ISP que desea incluir o excluir:
   * Para incluir ISP:
      1. Clic **[!UICONTROL Include ISPs]**.
      1. (Opcional) Filtre la lista por palabra clave.
      1. Seleccione la casilla de verificación situada junto a cada ISP que desee segmentar.
   * Para excluir los ISP:
      1. Clic **[!UICONTROL Exclude ISPs]**.
      1. (Opcional) Filtre la lista por palabra clave.
      1. Seleccione la casilla de verificación situada junto a cada ISP que desee excluir.
1. (Opcional) Para descargar un archivo CSV con la información de segmentación del ISP en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Tipos de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], y [!DNL Peer39] filtros contextuales para aplicar. Los valores predeterminados de nivel de anunciante están seleccionados para nuevas ubicaciones, pero puede cambiar la configuración:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de contexto de inventario que se bloquearán de forma predeterminada. Se pueden aplicar tarifas adicionales.

* [!UICONTROL Peer 39]:

   * **Sitios de destino que:** (Opcional) Uno o más tipos de atributos de inventario que se van a asignar de forma predeterminada. Se pueden aplicar tarifas adicionales.

* [!UICONTROL ComScore]:

   * **Bloquear sitios que:** (Opcional) Uno o más tipos de atributos de inventario para bloquear de forma predeterminada. Se pueden aplicar tarifas adicionales.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Opcional) Grado de contenido para adultos para el que se bloquean los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (el valor predeterminado), *[!UICONTROL Standard]*, o *[!UICONTROL Strict]*. Se pueden aplicar tarifas adicionales.

   * **[!UICONTROL Alcohol Content]:** (Opcional) Grado de contenido alcohólico para el que se bloquean los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (el valor predeterminado), *[!UICONTROL Standard]*, o *[!UICONTROL Strict]*. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Pre-bid fraud blocking]:** Tipos de sitios que bloquear según el tráfico fraudulento y las actividades sospechosas medidas a través de [!DNL DoubleVerify], [!DNL Integral Ad Science], y [!DNL Peer39]. Los valores predeterminados de nivel de anunciante están seleccionados para nuevas ubicaciones, pero puede cambiar la configuración:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** De forma predeterminada, bloquea todo el tráfico 100 % inválido, incluido el tráfico en dispositivos secuestrados, para las nuevas ubicaciones. Se pueden aplicar tarifas adicionales.

   * **[!UICONTROL Also block sites with]:** DSP (Opcional) Un nivel adicional de fraude y tráfico no válido que hace que los anuncios se bloqueen de forma predeterminada por parte de los usuarios de la siguiente manera:  *[!UICONTROL None]* (el valor predeterminado, que no bloquea el tráfico adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, o *[!UICONTROL >25% Average Fraud/IVT levels]*. Se pueden aplicar tarifas adicionales.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** DSP (Opcional) Uno o más tipos de fraude que causan que los anuncios se bloqueen de forma predeterminada con la ayuda de la siguiente manera: *[!UICONTROL Fraud]* (que bloquea todos los sitios con fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, y/o *[!UICONTROL Fraud: Zero Ads]*. Se pueden aplicar tarifas adicionales.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** DSP (Opcional) Un tipo de actividad sospechosa de un sitio web o una aplicación que hace que los anuncios se bloqueen de forma predeterminada de la siguiente manera: *[!UICONTROL None]* (el valor predeterminado, que no bloquea los anuncios en función de la actividad sospechosa), *[!UICONTROL Suspicious Activity - High Risk]*, o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Ads.txt filtering]:**

Qué nivel de [Ads.txt](https://iabtechlab.com/ads-txt-about/) Filtro de ofertas previas que se usará aplicando la lista de vendedores digitales autorizados de cada editor. El nivel de anunciante predeterminado está seleccionado para nuevas ubicaciones, pero puede cambiar la configuración:

* *[!UICONTROL Opt out of ads.txt (default)]*: para comprar inventario a todos los vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: para priorizar la compra de inventario a los vendedores directos y revendedores autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar inventario solo de los vendedores y revendedores directos autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar inventario solo de los vendedores directos autorizados de un dominio.

**[!UICONTROL Attention Targeting]:** (Visualización, vídeo, móvil y ubicaciones de TV conectadas estándar) Targets [!DNL Adelaide] puja previa de segmentos con un nivel de atención específico (alto, medio o bajo) según el sitio, el formato y el tamaño del anuncio especificados. Los segmentos se actualizan semanalmente. **Nota:** Uso de [!DNL Adelaide] Los segmentos para segmentar incurren en una tarifa CPM por cada impresión entregada con [!DNL Adelaide] segmentación de la atención; esta tarifa es independiente de las tarifas para [medición de la atención](/help/dsp/campaign-management/campaigns/campaign-settings.md). Para las ubicaciones interactivas previas a la emisión, solo se te cobrarán las impresiones VAST.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Anunciantes configurados con el [!UICONTROL DoubleVerify Authentic Brand Safety] option) Habilita [!DNL DoubleVerify Authentic Brand Safety], que bloquea las impresiones después de la oferta utilizando las reglas de seguridad de marca personalizadas configuradas para el ID de segmento especificado. DSP a su cuenta el uso del ID de segmento especificado en la configuración del anunciante.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] ubicaciones) Proveedores de seguimiento de terceros aprobados por [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], y [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Opcional) Píxeles de seguimiento de eventos de terceros que se adjuntarán de forma predeterminada a todos los anuncios nuevos de la ubicación. Para especificar píxeles de evento:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para seleccionar un píxel existente, marque la casilla de verificación en la fila de píxeles.
   * Para crear un píxel:
      1. Clic **[!UICONTROL Create]**.
      1. Introduzca la siguiente información:
         * **[!UICONTROL Pixel name]:** Nombre del píxel; la longitud máxima es de 500 caracteres. Utilice un nombre que le ayude a identificar fácilmente el píxel.
         * **[!UICONTROL Pixel event fires on]:** Evento que déclencheur el píxel que se va a activar. Los eventos disponibles varían según el tipo de anuncio.
         * **[!UICONTROL Pixel type]:** Si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** La URL de la imagen de píxel.
      1. Clic **[!UICONTROL Create and attach]**.
   1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Opcional) Los píxeles de seguimiento de conversión se adjuntarán de forma predeterminada a todos los anuncios nuevos de la ubicación. Para especificar píxeles de conversión:

1. Clic ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para seleccionar un píxel existente, marque la casilla de verificación en la fila de píxeles.
   * Para crear un píxel:
      1. Clic **[!UICONTROL Create]**.
      1. Introduzca la siguiente información:
         * **[!UICONTROL Conversion pixel name]:** Nombre del píxel; la longitud máxima es de 500 caracteres. Utilice un nombre que le ayude a identificar fácilmente el píxel.
         * **[!UICONTROL Conversion category]:** El tipo de conversión.
         * **[!UICONTROL Impression conversion window]:** El número de días después de que se produzca una impresión de anuncio en los que la impresión puede atribuirse a una conversión. El valor predeterminado es de 30 días.
         * **[!UICONTROL Click conversion window]:** El número de días después de que se produzca un clic en un anuncio en los que el clic puede atribuirse a una conversión. El valor predeterminado es de 30 días.
         * **[!UICONTROL Notes]:** (Opcional) Una descripción u otra información sobre el píxel.
      1. Clic **[!UICONTROL Create and attach]**.
      1. Implemente el píxel de conversión en las páginas web relevantes:
         1. En el menú principal, vaya a **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. En la fila de píxeles, haga clic en **[!UICONTROL edit]**.
         1. Copie los valores en la variable [!UICONTROL HTML Tag] y [!UICONTROL Flash Tag] campos, según sea necesario, para proporcionar al anunciante o al contacto del sitio web.

            Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.
   1. Clic **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Opcional) Una tarifa estática de terceros que se rastreará como un coste no facturable por 1000 impresiones. El valor predeterminado de nivel de paquete se aplica automáticamente a las nuevas ubicaciones, cuando corresponda, a menos que introduzca un valor diferente.

>[!NOTE]
>
>Las tarifas facturables se reflejan en la [!UICONTROL Net CPM] métrica.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de ubicación](placement-about.md)
>* [Crear una ubicación](placement-create.md)
>* [Editar ubicaciones](placement-edit.md)
>* [Administrar multiplicadores de oferta para ubicaciones](placement-manage-bid-multipliers.md)
>* [Ver el registro de cambios de una ubicación](placement-change-log.md)
>* [Métodos abreviados de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Preguntas frecuentes sobre Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
