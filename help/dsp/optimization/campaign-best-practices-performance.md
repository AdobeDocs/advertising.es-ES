---
title: Prácticas recomendadas para configurar campañas de rendimiento
description: Conozca las prácticas recomendadas para configurar sus campañas centradas en el rendimiento, que incluyen ubicaciones optimizadas para la CPA más baja o el ROAS más alto.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 802c75920bb11f262cbe0d76d2554971aaf35831
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# Prácticas recomendadas para configurar campañas de rendimiento

DSP Puede optimizar sus campañas centradas en el rendimiento. Consulte las siguientes prácticas recomendadas para campañas de rendimiento:

* Paso 1: Definición de la meta
* Paso 2: Definición de la estrategia
* Paso 3: Creación de paquetes
* Paso 4: Creación de una estructura de ubicación
* Paso 5: Uso de Creative Assets adecuado

## Paso 1: Definición de la meta

Es importante comprender el objetivo de la campaña, como lograr el ROAS más alto posible o el CPA más bajo posible. Las campañas de rendimiento tienen los [objetivos de optimización](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;. Especifique el objetivo de optimización correspondiente para cada paquete de la campaña.

![objetivo de optimización](/help/dsp/assets/optimization-goals.png)

También debe determinar los eventos de éxito que conducen a la meta general y crear metas personalizadas en consecuencia. Para cada paquete, especifique un objetivo personalizado que se utilizará con el objetivo de optimización general para la optimización algorítmica y de informes con [!DNL Adobe Sensei]. Para obtener más información sobre cómo crear metas personalizadas, incluidas las prácticas recomendadas, consulte [Metas personalizadas](custom-goal.md).

## Paso 2: Definición de la estrategia

### Estrategias de prospección

Los paquetes de canal superior incluyen ubicaciones con una segmentación muy amplia para llegar a nuevos consumidores netos.

#### Estrategias de colocación recomendadas para la prospección

* Busque nuevas audiencias que probablemente se conviertan con las siguientes tácticas:

   * Modelado de similitudes desde una plataforma de administración de datos (DMP), como Adobe Audience Manager.
   * Segmentación basada en el comportamiento con datos de terceros.
   * Segmentación contextual.
   * Segmentación de sitios/categorías.

* Usar la segmentación por ejecución de red (RON): es importante incluir una ejecución de ubicación de red sin segmentación de audiencia y con una segmentación de inventario amplia. Esto permite que el algoritmo [!DNL Adobe Sensei] encuentre usuarios valiosos que pueden tener cookies más recientes que aún no se han clasificado en una audiencia.

### Estrategias de redireccionamiento

Los paquetes de canal inferior incluyen ubicaciones que se dirigen a usuarios que ya han estado en la página web del anunciante o para los que el anunciante tiene datos CRM.

#### Estrategias de colocación recomendadas para la reorientación

* Si el anunciante es un cliente de Adobe Analytics o Adobe Audience Manager DSP, puede generar segmentos de origen (como visitantes de la página de inicio, páginas de productos o personas que abandonan el carro de compras) y utilizarlos como objetivos de ubicación en la.

* Evite asignar demasiado presupuesto a una ubicación segmentada por audiencia. Como regla general, presupuestar $30 por cada 1,000 usuarios al mes.

## Paso 3: Creación de paquetes

La práctica recomendada es crear paquetes separados para la prospección del canal superior y para el redireccionamiento del canal inferior. La optimización se produce en el nivel de paquete, de modo que los datos de rendimiento de todas las ubicaciones dentro de un paquete se agrupen. Por lo tanto, agrupe las ubicaciones en paquetes con un rendimiento esperado similar.

![ejemplo de paquetes separados para prospección y retargeting](/help/dsp/assets/p-r.png)

Además, utilice la siguiente configuración.

### Objetivos y presupuesto

* **Ritmo y límite:** Para seleccionar un objetivo de optimización de CPA o ROAS, el paquete debe utilizar un ritmo a nivel de paquete. Esto garantiza que todas las ubicaciones dentro del paquete estén optimizadas para distribuir el gasto en función del rendimiento y escalarlo para los objetivos seleccionados.

* **Fechas de vuelo:** (Prospección de paquetes) Cuando su campaña dure más de 25 días, use la característica [!UICONTROL Activate Custom Flighting]. Primero, establezca un vuelo personalizado para los primeros 10 días en aproximadamente el 75% del presupuesto diario necesario para reducir el gasto durante la *fase de aprendizaje*. Luego establezca un segundo vuelo personalizado para el resto del presupuesto.

  Por ejemplo, si tiene 100 000 $ para gastar en 30 días, establezca el presupuesto del vuelo 1 (días 1-10) en 25 000 $ (75 % x 100 000 $/30 días = 2 500 $ por día). Utilice el presupuesto restante de $75,000 para el Vuelo 2 (Días 11-30).

* DSP **Presupuesto:** siempre intenta asignar el 100% del presupuesto del paquete de manera uniforme entre todas las ubicaciones de un paquete. Si una ubicación tiene un gasto bajo o ninguno, se recomienda limitar el presupuesto a la ubicación para permitir que se asigne más del presupuesto a las ubicaciones con escala. Espere entre 24 y 48 horas para que se calibran los cambios de presupuesto.

* **Objetivos de optimización:** Use uno de los dos objetivos de optimización de rendimiento, *[!UICONTROL Highest Return on Ad Spend]* o *[!UICONTROL Lowest Cost per Acquisition]*, según el objetivo del paquete. Estos objetivos optimizan automáticamente el paquete hacia las ubicaciones de ROAS más alta o CPA más baja, respectivamente.

* **Metas personalizadas:**
   * Si un paquete nuevo tiene el mismo objetivo que un paquete existente, puede, opcionalmente, vincular el paquete existente para que el algoritmo pueda utilizar los datos de aprendizaje automático existentes.
   * Escriba el [!UICONTROL Target CPA] o [!UICONTROL Target ROAS] apropiado.

* **Ritmo de vuelo y ritmo intradía:** Para ambos tipos de ritmo, seleccione *[!UICONTROL Even]* para maximizar los objetivos de rendimiento mediante un ritmo uniforme durante todo el día y durante todo el vuelo.

  >[!CAUTION]
  >
  >Use *[!UICONTROL FrontLoad]* y *[!UICONTROL Aggressive Front Load]* para el ritmo de vuelo y *[!UICONTROL ASAP]* para el ritmo intradía solo cuando esté priorizando completamente la entrega y el gasto en comparación con la optimización del rendimiento, ya que esas estrategias pueden afectar negativamente a los KPI de rendimiento deseados.

## Paso 4: Creación de una estructura de ubicación

Menos es más. Si puede configurar menos de seis ubicaciones por paquete, el presupuesto disponible puede cambiar dinámicamente a las ubicaciones con mejor rendimiento con la mayor facilidad.

Además, asegúrese de agregar cada ubicación a un paquete con un tipo de objetivo de paquete de *[!UICONTROL Prospecting]* o *[!UICONTROL Retargeting]*, según corresponda.

A continuación se indican las opciones de colocación recomendadas para las campañas de rendimiento.

### Metas

Debe configurar la optimización de CPA o ROAS en el nivel de paquete (consulte Paso 3: Creación de paquetes), pero puede agregar ajustes de nivel de ubicación adicionales.

* **Oferta máxima:**
   * Para las ubicaciones de prospección, utilice una oferta máxima baja ($5).
   * Para volver a segmentar reemplazos, usa una puja máxima alta (12 dólares).

* **Filtros de oferta previa:** Minimice o, idealmente, evite establecer filtros de oferta previa agresivos, que impiden que la ubicación alcance la escala. Las prácticas recomendadas incluyen las siguientes:

   * Utilice un (1) filtro de oferta previa por ubicación. El uso de varios filtros de oferta previa requiere que se cumplan ambos, lo que reduce la escala.

   * Considere la posibilidad de establecer filtros de oferta previa menos estrictos en los casos en que se aplique una segmentación adicional (como segmentación por audiencia, ubicación geográfica y sitio).

Ver descripciones de cuándo usar cada filtro de oferta previa en [Filtros de oferta previa de nivel de ubicación y cómo usarlos](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventario

Para maximizar la escala, use el inventario [!UICONTROL Public] (Open Exchange) y [!UICONTROL On Demand].

### Segmentación de sitios

* **[!UICONTROL Traffic Type]**: solo [!UICONTROL Websites]
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Segmentación de audiencia

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Para las ubicaciones de prospección, agrupe categorías de audiencia similares y tamaños de audiencia similares en una ubicación. A continuación, en función del rendimiento, realice una de las siguientes acciones:
      * Elimine las audiencias con bajo rendimiento de las ubicaciones existentes.
      * Mueva las audiencias de mayor rendimiento a una ubicación independiente para controlar mejor los presupuestos.
   * Lo ideal es que, para volver a segmentar las ubicaciones, incluya un segmento de audiencia por ubicación a fin de controlar fácilmente las ofertas y el presupuesto.

>[!NOTE]
>
>Tus anuncios funcionan mejor si solo se puede llegar a un usuario en una ubicación. Una superposición significativa en los usuarios entre ubicaciones puede causar competencia, lo que da lugar a un ciclo de ofertas que aumentan continuamente, lo que aumenta el coste por usuario. Por lo tanto, si incluye varias audiencias, asegúrese de que no estén formadas por usuarios o miembros de audiencia superpuestos.
>
> Puede evitar audiencias superpuestas creando audiencias en niveles para poder suprimir los niveles más altos e inclusivos de las ubicaciones según sea necesario.

* **[!UICONTROL Frequency Capping]:**
   * Para las ubicaciones de prospección, utilice límites de frecuencia ajustados (una impresión por día).
   * Para redireccionar ubicaciones, establezca el límite de ubicación principal en 6-10 impresiones por día y el límite secundario en una impresión por hora.

* **[!UICONTROL Device Targeting]**:
   * Incluir [!UICONTROL Computer], [!UICONTROL Mobile] y [!UICONTROL Tablet].
   * No se debe segmentar [!UICONTROL Firefox] y [!UICONTROL Safari] debido a las limitaciones de segmentación y medición. Póngase en contacto con el equipo de cuenta de Adobe para obtener más detalles acerca de la compatibilidad con [!DNL Adobe] para [!DNL Safari ITP].
   * Si dirige el tráfico web móvil, deshabilite todos los exploradores móviles excepto [!UICONTROL Chrome] y [!UICONTROL Edge].

### Seguridad de marca y calidad de medios

El uso del filtrado contextual, el bloqueo de fraude de oferta previa o el filtrado [!UICONTROL Ads.txt] limita la escala de las ubicaciones, pero puede utilizarlos en caso necesario.

## Paso 5: Uso de Creative Assets adecuado

* La práctica recomendada es incluir tantos tamaños de anuncio únicos como sea posible para maximizar el alcance. La plantilla de visualización universal le permite cargar cualquier tamaño de anuncio de visualización estándar.
* Asegúrese de que todas las ubicaciones contengan *al menos* todos los tamaños de anuncios de pantallas principales (300x250, 728x90, 160x600, 300x600, 320x50 y 300x50).
* Actualice los elementos creativos con frecuencia para evitar la fatiga creativa.

>[!MORELIKETHIS]
>
>* [Configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
> * DSP [Cómo Optimiza El Uso De Las Campañas](optimization-how-dsp-optimizes-campaigns.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Filtros de pujas previas de nivel de ubicación y cómo usarlos](optimization-pre-bid-filters.md)
>* [Lista de comprobación de inicio de campaña](/help/dsp/campaign-management/campaign-launch-checklist.md)
