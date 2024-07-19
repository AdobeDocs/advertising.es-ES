---
title: Seguridad de marca y calidad de medios
description: Obtenga más información sobre la seguridad de la marca y las funciones de calidad de los medios.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: a927c073fd27e0b2c84bd1929eb4d6d233a29cb5
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 0%

---

# Seguridad de marca y calidad de medios

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP proporciona un conjunto de funciones de protección de marca para garantizar que cada una de sus campañas llegue a usuarios reales en un entorno seguro para la marca.

Nuestro equipo de Vigilancia del Fraude trabaja en estrecha colaboración con socios líderes del sector, como [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] y [!DNL WhiteOps], para revisar cuidadosamente el inventario en nuestra plataforma. DSP A través de la administración proactiva de nuestro suministro, garantiza que todos los anunciantes en toda la plataforma estén protegidos del tráfico no humano (bots, rastreadores, tráfico de centros de datos y fraude) y que se ofrezca solo en contextos seguros para la marca.

Además de proporcionar una gestión de calidad central, creemos en el empoderamiento de los anunciantes para que diseñen los controles que se alineen con su marca. DSP ofrece integraciones con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] y [!DNL Peer39], lo que garantiza que cada anunciante pueda elegir el nivel deseado de protección contra fraudes, filtrado contextual y segmentación de palabras clave.

## Iniciativas de calidad

### Verificación de inventario con soporte para [!DNL Ads.txt]

[[!DNL Ads.txt], que significa  [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) es una iniciativa lanzada por [!DNL Interactive Advertising Bureau] ([!DNL IAB]) en junio de 2017 para facilitar la representación adecuada del inventario en el mercado abierto, combatiendo así las fuentes ilegítimas de tráfico y suplantación de dominio. Los editores y distribuidores participantes declaran públicamente las empresas autorizadas a vender su inventario digital y la naturaleza de esas relaciones, manteniendo una página de `ads.txt` en el nivel superior del dominio (como `example.com/ads.txt`).

DSP El servicio admite [!DNL ads.txt] al leer el archivo `ads.txt` de cada publicador y ofrecerle la opción de comprar únicamente a vendedores [!DNL ads.txt] verificados. Por ejemplo, si comparamos los vendedores que vemos que acceden a `nytimes.com` con el archivo `ads.txt` del New York Times, podemos identificar cuáles son legítimos y cuáles no, y bloquearemos a los infractores si la ubicación está configurada para comprar únicamente a vendedores verificados. <!-- can we actually mention NY Times? -->

Puede establecer controles predeterminados de [!DNL ads.txt] para cada anunciante<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, a continuación, [personalizar la configuración de cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md) para:

* comprar inventario solo a los vendedores directos autorizados de un dominio

* comprar inventario solo a los vendedores directos y revendedores autorizados de un dominio

* priorizar la compra de inventario a los vendedores directos y revendedores autorizados de un dominio

* comprar inventario a todos los vendedores

### Vigilancia del fraude de Platform

DSP ha creado sólidas herramientas y sistemas internos para administrar el fraude en toda nuestra plataforma, en asociación con proveedores líderes del sector como [!DNL Whiteops] y [!DNL Integral Ad Science].

Además, Adobe trabaja estrechamente con [!DNL IAB] y [!DNL TAG] para garantizar un bloqueo de fraude sólido y estándar en el sector a fin de proteger a nuestros anunciantes, aprovechando herramientas como [!DNL ads.txt] (consulte la sección anterior), la lista de bots y arañas de [!DNL IAB] y la lista de IP del centro de datos [!DNL TAG].

A través de nuestro enfoque multidimensional de la calidad, nuestro equipo supervisa las anomalías y los patrones de tráfico no válidos, lo que garantiza menos del 3% del tráfico no válido en el inventario protegido. Cualquier inventario que sea sospechoso, incluido el inventario de dominios específicos o de editores o vendedores específicos, se bloquea inmediatamente en toda la plataforma.

### Asignación de inventario, niveles y categorización

La asignación de inventario es el proceso detallado de revisión e incorporación necesario para todo el nuevo inventario antes de que se añada a nuestra plataforma. DSP Este proceso está diseñado para garantizar la seguridad y la calidad de todo el inventario en el momento de la creación de la.

* **Asignación:** Nuestro equipo de inventario revisa cada dominio cuidadosamente, evaluando aspectos como:

   * Seguridad de marca

   * Verificación del tipo de anuncio

   * Contenido genérico, dominios duplicados y servicio de publicidad falsa

* **Asignación de niveles:** Examinamos de manera integral la presencia de la marca en el ecosistema general para clasificar el inventario en diferentes niveles. Puede [dirigir sus ubicaciones](/help/dsp/campaign-management/placements/placement-settings.md) a estos niveles para alcanzar el nivel deseado:

   * **[!UICONTROL T1]**: sitios reconocidos internacionalmente con nombre de marca

   * **[!UICONTROL T2]**: sitios atractivos que son actuales, actualizados, sin contenido generado por el usuario y que normalmente carecen de reconocimiento global

   * **[!UICONTROL T3]**: contenido generado por el usuario y contenido especializado

* DSP **Categorización del sitio:** Para garantizar la fácil segmentación y bloqueo de contenido, etiquetamos cada propiedad con una categoría de sitio definida por el usuario basada en el contenido de la propiedad. Puede [segmentar o excluir estas categorías de sitio para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md) según los objetivos de ubicación.

### Soporte completo para el bloqueo de sitios

DSP proporciona una lista de sitios bloqueados globalmente y la opción de crear listas de sitios bloqueados personalizadas para anunciantes y cuentas de.

#### DSP Lista de sitios bloqueados globalmente {#global-blocked-sites}

DSP mantiene una lista de sitios bloqueados globalmente en los que se considera que no es seguro publicar anuncios. Esta lista contiene sitios con contenido censurable (como odio o terror) y sitios infectados por bots, pre-roll falso, dominios no coincidentes y otras actividades fraudulentas.

Como parte de nuestra iniciativa de seguridad de marca para erradicar las actividades que defraudan a los anunciantes, todos los sitios se examinan utilizando las medidas de la lista de sitios bloqueados del gráfico. Todos los sitios que no pasan las comprobaciones de seguridad de la marca se agregan a la lista de sitios bloqueados globalmente. DSP Debido a que administra esta lista de forma dinámica, los sitios pueden moverse dentro o fuera de la lista en cualquier momento, según el análisis de seguridad de marca más reciente.

Cuando se incluye un sitio en la lista de sitios bloqueados globalmente como destino de ubicación, el sitio se marca con un signo de exclamación rojo (!). Esto indica que los anuncios no se ejecutan en el sitio marcado.

>[!NOTE]
>
>Si lo desea, puede omitir la lista de sitios bloqueados globales para los anuncios de pantalla estándar adjuntos a una oferta privada de confianza habilitando la opción &quot;[!UICONTROL Allow unscreened sites]&quot; en la [configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Si es necesario, el equipo de cuenta de Adobe también puede, opcionalmente, deshabilitar el bloqueo de sitios para una operación pública (de nivel de subasta) en la configuración del editor de la operación.

#### Listas de sitios bloqueados a nivel de cuenta y de anunciante

Los usuarios también pueden mantener listas de sitios bloqueados a nivel de cuenta y de anunciante <!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, que se utilizan automáticamente para todas las ubicaciones. La lista de sitios bloqueados de nivel inferior se aplica además de la lista de sitios bloqueados globalmente.

## Integraciones de terceros

### Filtrado contextual

El filtrado contextual le permite segmentar o bloquear las oportunidades publicitarias en función del contexto de la página en la que aparecería el anuncio. El Adobe proporciona filtrado contextual mediante integraciones con proveedores líderes del sector: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] y [!DNL Peer39]. Los filtros actuales incluyen [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] y [!UICONTROL G-rated Sites].

Puede establecer controles de filtro contextual predeterminados para cada anunciante<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [personalizar la configuración para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales al utilizar esta función.

![Logotipo de Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo de DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo integral de Ad Science](/help/dsp/assets/ias-logo.png) ![Logotipo de Peer39](/help/dsp/assets/peer39-logo.png)

### Bloqueo por fraude antes de la puja

Aproveche nuestras integraciones de terceros con [!DNL DoubleVerify], [!DNL Integral Ad Science] y [!DNL Peer39] para bloquear el tráfico que no sea humano de sus campañas. Estas integraciones proporcionan capacidades de bloqueo de oferta previas líderes en el sector para minimizar el tráfico no válido general y sofisticado (GIVT y SIVT) en sus campañas.

Puede establecer controles predeterminados de bloqueo de fraude de ofertas previas para cada anunciante<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [personalizar la configuración para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales al utilizar esta función.

Para obtener más información sobre la funcionalidad, póngase en contacto directamente con el proveedor preferido o con el equipo de cuenta de Adobe.

![Logotipo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo Integral de Ad Science](/help/dsp/assets/ias-logo.png) ![Logotipo Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilidad de pujas previas {#pre-bid-viewability}

Los filtros de visibilidad de ofertas previas con tecnología de nuestros socios líderes del sector [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) y [!DNL Integral Ad Science] permiten a los anunciantes asegurarse de que sus campañas cumplan los objetivos de rendimiento de visibilidad deseados en el inventario de vídeos y pantallas.

>[!NOTE]
>
>[!DNL Oracle] dejará de funcionar en publicidad el 30 de septiembre de 2024, incluidos todos los servicios de [!DNL MOAT].

Puede establecer filtros de visibilidad predeterminados para cada anunciante<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [personalizar la configuración para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales al utilizar esta función.

![Logotipo de DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo de Advertising de Oracle](/help/dsp/assets/oracle-advertising-logo.png) ![Logotipo integral de Ad Science](/help/dsp/assets/ias-logo.png)

### Segmentación de atención y medición

La asociación de [!DNL Adobe's] con [!DNL Adelaide] proporciona a los anunciantes compatibilidad con la métrica de Adelaida &quot;[!DNL Attention Units]&quot;, que mide la calidad de los medios en función del seguimiento visual, la exposición y los datos de resultados.

La [segmentación de la atención previa a la oferta en el nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md) permite a los anunciantes segmentar niveles de atención específicos para mejorar la participación de los clientes.

Además, los anunciantes pueden habilitar el seguimiento [para la métrica [!UICONTROL Attention Score] de nivel de ubicación](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (el número promedio ponderado de [!DNL Attention Units] en todas las impresiones) para cualquier campaña a fin de comprender qué tácticas de ubicación producen los mejores resultados comerciales.

Se aplican tarifas adicionales por cada función por separado.

### Segmentación de temas

DSP La segmentación de temas le permite segmentar o bloquear listas de palabras clave aprovechando los socios contextuales líderes en el sector [!DNL Comscore] y [!DNL Oracle Data Cloud] (anteriormente [!DNL Grapeshot]). La segmentación de temas le ayuda a garantizar que los anuncios se publiquen siempre en un entorno que se ajuste a su marca, ya sea bloqueando contenido perjudicial o asegurando un gasto en un contexto que garantice un mayor resultado.

>[!NOTE]
>
>[!DNL Oracle] dejará de funcionar en publicidad el 30 de septiembre de 2024, incluidos todos los servicios de [!DNL Oracle Data Cloud] (anteriormente [!DNL Grapeshot]).

El direccionamiento de temas requiere que cree segmentos de temas personalizados directamente con la plataforma del socio. Una vez creados los segmentos, puede [segmentar o excluir un ID de segmento en la sección [!UICONTROL Audience Targeting] para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales para esta función.

Para crear una cuenta de [!DNL Comscore] y segmentos de temas personalizados, puede solicitar un inicio de sesión para [!DNL Activation Segment Manager] en [https://agents.comscore.com](https://agents.comscore.com). Consulte el [[!DNL Comscore] centro de ayuda](https://comscoreactivation.zendesk.com/hc/) para obtener instrucciones completas sobre la configuración de segmentos personalizados. Las tarifas para los segmentos personalizados están visibles en [!DNL Segment Manager] a medida que los crea.

![Logotipo de Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo de Grapeshot](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP Se ha asociado con [!DNL DoubleVerify] para ofrecer su solución de segmentación [!DNL Authentic Brand Safety], que le permite crear un conjunto centralizado de requisitos de seguridad de marca para dirigirse a todas las plataformas de compra con el fin de mantener la coherencia.

DSP Una vez que haya creado un segmento de seguridad de marca [!DNL DoubleVerify] con la segmentación necesaria, puede utilizarlo en para replicar las reglas de bloque posteriores a la oferta con la oferta previa en entornos web.

Puede especificar un ID de segmento [!DNL DoubleVerify] para cada anunciante<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [habilitar o deshabilitar [!UICONTROL Authentic Brand Safety] para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). DSP factura a su cuenta por el uso del ID de segmento.

Para obtener más información acerca de la funcionalidad, comuníquese directamente con [!DNL DoubleVerify] o comuníquese con el equipo de cuenta de Adobe.

![Logotipo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
