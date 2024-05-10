---
title: Soluciones entre dispositivos
description: Obtenga más información acerca de las funciones entre dispositivos.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Soluciones entre dispositivos

DSP La integración de Advertising con [!DNL LiveRamp] permite ampliar la audiencia a todos los dispositivos conocidos de una persona, no solo a los dispositivos de los que ha hecho un seguimiento su marca. La integración también proporciona límite de frecuencia y medición de atribución en todos los dispositivos.

Cuando utiliza un gráfico de dispositivos basado en personas compatible, puede:

* Haga coincidir audiencias en varios canales y dispositivos para enviar anuncios a personas y hogares, en lugar de a dispositivos.
* Equilibrio y exposición al comprender y limitar la frecuencia entre individuos.
* Estrategias de prueba que exponen o convierten audiencias en varios canales o dispositivos.

## Ventajas de la [!DNL LiveRamp] Gráfico del dispositivo

* Proporciona un grupo de datos determinístico, incluidos los datos de clientes sin conexión

* Proporciona una cobertura uniforme entre los ID de cookie y los ID de dispositivos móviles

* Incluye datos principalmente de Estados Unidos

* Está libre para la restricción de frecuencia y la medición de atribución

* Precio de 0,35 $ CPM para impresiones extendidas (impresiones que se entregan únicamente mediante el uso de [!DNL LiveRamp] gráfico de dispositivos, en lugar de en dispositivos ubicados dentro de los segmentos de audiencia de destino)

  La tarifa se refleja en su tarjeta de tarifa de la cuenta.

## Administración de frecuencia basada en personas

La gestión de frecuencias basada en personas permite especificar límites de frecuencia en el nivel de la persona, en lugar de en el nivel del dispositivo, para un verdadero control de la exposición a los medios.

### Activar la administración de frecuencias basada en personas

* **Campañas:** Al crear una nueva campaña, puede especificar una [!UICONTROL Cross-Device Level] configuración. Habilitar &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; y seleccione un gráfico de dispositivos. El gráfico de dispositivo especificado se utiliza tanto para la segmentación entre dispositivos en el nivel de ubicación como para la administración de frecuencias basada en personas en el nivel de campaña, paquete y ubicación. Los límites de frecuencia se aplican a todos los dispositivos conocidos de una persona.

Para obtener más información, consulte [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Una vez guardada una campaña, no se puede cambiar su [!UICONTROL Cross Device Level] configuración.

* **Paquetes:**  Si lo desea, puede definir límites de frecuencia adicionales en el nivel de paquete. DSP respeta el límite de frecuencia más estricto de la jerarquía de campañas.

* **Ubicaciones:** Si lo desea, puede definir límites de frecuencia adicionales en el nivel de posición. DSP respeta el límite de frecuencia más estricto de la jerarquía de campañas.

## Segmentación basada en personas

La segmentación basada en personas permite encontrar clientes en equipos de escritorio y dispositivos móviles.

### Activar segmentación basada en personas

* **Campañas:** Al crear una nueva campaña, puede especificar una [!UICONTROL Cross-Device Level] configuración. Habilitar &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; y seleccione un gráfico de dispositivos. El gráfico de dispositivos especificado se utiliza tanto para la segmentación entre dispositivos en el nivel de ubicación como para la administración de frecuencias basada en personas.

Para obtener más información, consulte [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Ubicaciones:** Al seleccionar objetivos de audiencia para una ubicación en una campaña con un gráfico de dispositivos especificado, se muestra un [!UICONTROL Cross-Device Targeting] Esta opción le permite ampliar el direccionamiento a todos los dispositivos conocidos de una persona (según el gráfico de dispositivos especificado en la configuración de la campaña), incluso a los dispositivos que no están en los segmentos especificados.

### Configuración de informes para segmentación basada en personas

Puede incluir las siguientes métricas en los informes personalizados:

* **Impresiones extendidas:** (En el [!UICONTROL Build Your Report] sección debajo de [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) El volumen de impresiones incrementales que arroja el uso de un gráfico de dispositivos (que no se encuentra dentro de los segmentos de audiencia originales). Esta métrica también se utiliza para calcular las tarifas aplicables asociadas con el uso de un gráfico de dispositivos de terceros.

  Para determinar el coste de las impresiones extendidas durante un período de tiempo, ejecute un informe personalizado que incluya la variable [!UICONTROL Extended Impressions] y luego multiplicar el número total de impresiones extendidas por 0,00035 $ (0,35 $/1000 impresiones).

  El coste agregado también se incluye en la [!UICONTROL Billable Other Net Spend] columna (debajo de [!UICONTROL Metrics] > [!UICONTROL Spend]), aunque esa métrica también incluye otras tarifas de campaña que puede haber agregado.

* **Gráfico del dispositivo:** (En el [!UICONTROL Build Your Report] sección debajo de [!UICONTROL Dimensions] > [!UICONTROL Campaign]) El gráfico del dispositivo seleccionado para una campaña, paquete o ubicación en particular.

## Medición de atribución basada en personas

*Anunciantes solo con seguimiento de conversión de Adobe Advertising*

Con la atribución basada en personas, puede atribuir conversiones que se produjeron en un dispositivo diferente al dispositivo en el que se produjo la exposición a los medios. DSP La medición de atribución basada en personas está disponible en todas las áreas de trabajo, y es: [!DNL Adobe Advertising Creative], y [!DNL Adobe Advertising Search, Social, & Commerce] para anunciantes que hayan implementado píxeles de conversión de Adobe Advertising en sus sitios.

### Habilitar la medición de atribución basada en personas

Si desea activar la medición de atribución entre dispositivos, póngase en contacto con el equipo de cuenta de Adobe.

### Configuración de informes de conversión para atribución de conversión entre dispositivos

#### Configuración del informe de conversión

Cuando un gráfico de dispositivo está habilitado para la medición de atribución, la variable [!UICONTROL Conversion] El informe incluye un [!UICONTROL Cross-Device Breakout] , que le permite incluir hasta tres columnas independientes para cada métrica de conversión, lo que incluye:

* &lt;*Conversión*>[!UICONTROL (tp)]: Incluye las conversiones totales (personas totales), que incluyen tanto las conversiones del mismo dispositivo como las conversiones entre dispositivos (si corresponde). En el informe, &quot;[!UICONTROL (tp)]&quot; se anexa al nombre de la métrica de conversión, el tipo de regla y los tipos de conversión en la ruta de conversión (por ejemplo, &quot;Responses(le)(tl)(tp)&quot;).

* &lt;*Conversión*>[!UICONTROL (sd)]: (Opcional) incluye solo las conversiones para las que se ha rastreado un solo dispositivo en la ruta de conversión. En el informe, &quot;[!UICONTROL (sd)]&quot; se anexa al nombre de la métrica de conversión, el tipo de regla y los tipos de conversión en la ruta de conversión (por ejemplo, &quot;Responses(le)(tl)(sd)&quot;).

* &lt;*Conversión*>[!UICONTROL (xd)]: (opcional) incluye solo las conversiones para las que se ha rastreado más de un dispositivo en la ruta de conversión. En el informe, &quot;[!UICONTROL (xd)]&quot; se anexa al nombre de la métrica de conversión, el tipo de regla y los tipos de conversión en la ruta de conversión (por ejemplo, &quot;Responses(le)(tl)(xd)&quot;).

#### Interpretación del informe de conversión

Ordene el porcentaje del total de conversiones entre dispositivos ([!UICONTROL (xd)]/[!UICONTROL (tl)]) de alto a bajo para comprender qué es lo que impulsa conversiones entre dispositivos por encima de la media. Puede utilizarlo para informar su estrategia creativa o de segmentación de modo que la inversión en mensajería y canal coincida con el comportamiento del usuario.

* Paquetes: vea qué paquetes generan la mayor cantidad de conversiones totales y cuáles tienen un alto porcentaje de conversiones entre dispositivos. Esto puede ayudarle a comprender dónde concentrar los gastos.

* Ubicaciones: compare el rendimiento de la ubicación y la atribución (por ejemplo, un anuncio en la web móvil puede generar conversiones en el escritorio). Sin un gráfico de dispositivo para la atribución, es posible que se pierda el impacto de una ubicación web móvil en las conversiones de escritorio, o que quede enterrada si la mayoría de los usuarios realizan la conversión en una web de escritorio y no en una web móvil.

* Anuncios: descubra qué anuncios generan conversiones más altas y cuantifique su valor y su impacto tanto en los navegadores web como en los entornos de aplicaciones móviles.

* Sitios: optimice los sitios en lugar de excluirlos manualmente por completo. Si un sitio web genera conversiones entre dispositivos, puede ver en qué dispositivos se produce este comportamiento.

* Ofertas: mejore la optimización manual comprobando qué ofertas de inventario ofrecen conversiones entre dispositivos y, a continuación, decida si debe ampliar su segmentación para incluir más dispositivos y canales en esas ofertas.

>[!MORELIKETHIS]
>
>* [Configuración de informes](/help/dsp/reports/report-settings.md)
>* [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
