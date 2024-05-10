---
title: Seguridad de marca y calidad de medios
description: Obtenga más información sobre la seguridad de la marca y las funciones de calidad de los medios.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Seguridad de marca y calidad de medios

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

DSP Advertising proporciona un conjunto de funciones de protección de marca para garantizar que cada una de sus campañas llegue a usuarios reales en un entorno seguro para la marca.

Nuestro equipo de Vigilancia del Fraude trabaja estrechamente con socios líderes del sector, como el [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)], y [!DNL WhiteOps], para revisar cuidadosamente el inventario en nuestra plataforma. DSP A través de la administración proactiva de nuestro suministro, garantiza que todos los anunciantes en toda la plataforma estén protegidos del tráfico no humano (bots, rastreadores, tráfico de centros de datos y fraude) y que se ofrezca solo en contextos seguros para la marca.

Además de proporcionar una gestión de calidad central, creemos en el empoderamiento de los anunciantes para que diseñen los controles que se alineen con su marca. DSP ofrece integraciones de con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud], y [!DNL Peer39], lo que garantiza que cada anunciante pueda elegir el nivel deseado de protección contra el fraude, filtrado contextual y segmentación de palabras clave.

## Iniciativas de calidad

### Verificación de inventario con [!DNL Ads.txt] Asistencia

[[!DNL Ads.txt], que significa [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) es una iniciativa lanzada por el [!DNL Interactive Advertising Bureau] ([!DNL IAB]) en junio de 2017 para facilitar la adecuada representación de los inventarios en el mercado abierto, combatiendo así las fuentes ilegítimas de tráfico y suplantación de dominio. Los editores y distribuidores participantes declaran públicamente las empresas autorizadas a vender su inventario digital y la naturaleza de esas relaciones, manteniendo un `ads.txt` página en el nivel superior del dominio (como `example.com/ads.txt`).

DSP soportes de la [!DNL ads.txt] leyendo el de cada editor `ads.txt` y le da la opción de comprar solo desde verificado [!DNL ads.txt] vendedores. Por ejemplo, al hacer coincidir los vendedores, vemos que se accede a `nytimes.com` al New York Times&#39; `ads.txt` podemos identificar cuáles son legítimos y cuáles no, y bloquearemos a los infractores si la ubicación está configurada para comprar solo a vendedores verificados. <!-- can we actually mention NY Times? -->

Puede establecer valores predeterminados [!DNL ads.txt] controles para cada anunciante<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->y, a continuación, opcionalmente [personalizar la configuración para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md) hasta:

* comprar inventario solo a los vendedores directos autorizados de un dominio

* comprar inventario solo a los vendedores directos y revendedores autorizados de un dominio

* priorizar la compra de inventario a los vendedores directos y revendedores autorizados de un dominio

* comprar inventario a todos los vendedores

### Vigilancia del fraude de Platform

DSP ha creado sólidas herramientas y sistemas internos para gestionar el fraude en toda nuestra plataforma, en asociación con proveedores líderes del sector, como [!DNL Whiteops] y [!DNL Integral Ad Science].

Además, Adobe trabaja estrechamente con [!DNL IAB] y [!DNL TAG] para garantizar un bloqueo de fraude robusto y estándar en la industria para proteger a nuestros anunciantes, aprovechando herramientas como [!DNL ads.txt] (consulte la sección anterior), la variable [!DNL IAB] La lista Bots y Arañas y la [!DNL TAG] Lista de IP del centro de datos.

A través de nuestro enfoque multidimensional de la calidad, nuestro equipo supervisa las anomalías y los patrones de tráfico no válidos, lo que garantiza menos del 3% del tráfico no válido en el inventario protegido. Cualquier inventario que sea sospechoso, incluido el inventario de dominios específicos o de editores o vendedores específicos, se bloquea inmediatamente en toda la plataforma.

### Asignación de inventario, niveles y categorización

La asignación de inventario es el proceso detallado de revisión e incorporación necesario para todo el nuevo inventario antes de que se añada a nuestra plataforma. DSP Este proceso está diseñado para garantizar la seguridad y la calidad de todo el inventario en el momento de la creación de la.

* **Asignación:** Nuestro equipo de Inventario revisa cada dominio cuidadosamente, evaluando aspectos como:

   * Seguridad de marca

   * Verificación del tipo de anuncio

   * Contenido genérico, dominios duplicados y servicio de publicidad falsa

* **Intervalos:** Examinamos holísticamente la presencia de la marca en el ecosistema general para clasificar el inventario en diferentes niveles. Puede [segmentar las ubicaciones](/help/dsp/campaign-management/placements/placement-settings.md) Vaya a estos niveles para obtener el nivel de alcance deseado:

   * **[!UICONTROL T1]** — Sitios de marca reconocida internacionalmente

   * **[!UICONTROL T2]** — Sitios de gran aspecto que son actuales, actualizados, sin contenido generado por el usuario y que generalmente carecen de reconocimiento global

   * **[!UICONTROL T3]** — Contenido generado por el usuario y contenido especializado

* **Categorización del sitio:** DSP Para garantizar una segmentación y un bloqueo de contenido sencillos, etiquetamos cada propiedad con una categoría de sitio definida por el usuario en función del contenido de la propiedad. Puede [dirija o excluya estas categorías de sitio para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md) en función de los objetivos de colocación.

### Soporte completo para el bloqueo de sitios

DSP proporciona una lista de sitios bloqueados globalmente y la opción de crear listas de sitios bloqueados personalizadas para anunciantes y cuentas de.

#### DSP Lista de sitios bloqueados globalmente {#global-blocked-sites}

DSP mantiene una lista de sitios bloqueados globalmente en los que se considera que no es seguro publicar anuncios. Esta lista contiene sitios con contenido censurable (como odio o terror) y sitios infectados por bots, pre-roll falso, dominios no coincidentes y otras actividades fraudulentas.

Como parte de nuestra iniciativa de seguridad de marca para erradicar las actividades que defraudan a los anunciantes, todos los sitios se examinan utilizando las medidas de la lista de sitios bloqueados del gráfico. Todos los sitios que no pasan las comprobaciones de seguridad de la marca se agregan a la lista de sitios bloqueados globalmente. DSP Debido a que administra esta lista de forma dinámica, los sitios pueden moverse dentro o fuera de la lista en cualquier momento, según el análisis de seguridad de marca más reciente.

Cuando se incluye un sitio en la lista de sitios bloqueados globalmente como destino de ubicación, el sitio se marca con un signo de exclamación rojo (!). Esto indica que los anuncios no se ejecutan en el sitio marcado.

>[!NOTE]
>
>Si lo desea, puede omitir la lista de sitios bloqueados globales para anuncios estándar adjuntos a una oferta privada de confianza activando la opción &quot;[!UICONTROL Allow unscreened sites]&quot; en la [configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Si es necesario, el equipo de cuenta de Adobe también puede, opcionalmente, deshabilitar el bloqueo de sitios para una operación pública (de nivel de subasta) en la configuración del editor de la operación.

#### Listas de sitios bloqueados a nivel de cuenta y de anunciante

Los usuarios también pueden mantener listas de sitios bloqueados a nivel de cuenta y de anunciante<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, que se utilizan automáticamente para todas las ubicaciones. La lista de sitios bloqueados de nivel inferior se aplica además de la lista de sitios bloqueados globalmente.

## Integraciones de terceros

### Filtrado contextual

El filtrado contextual le permite segmentar o bloquear las oportunidades publicitarias en función del contexto de la página en la que aparecería el anuncio. El Adobe proporciona un filtrado contextual a través de integraciones con proveedores líderes del sector: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], y [!DNL Peer39]. Algunos ejemplos de filtros actuales son [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics], y [!UICONTROL G-rated Sites].

Puede establecer controles de filtro contextual predeterminados para cada anunciante<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->y, a continuación, opcionalmente [personalizar la configuración para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales al utilizar esta función.

![Logotipo de Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo de DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo de Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logotipo de Peer39](/help/dsp/assets/peer39-logo.png)

### Bloqueo por fraude antes de la puja

Aproveche las integraciones de terceros con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], y [!DNL Peer39] para bloquear el tráfico no humano de sus campañas. Estas integraciones proporcionan capacidades de bloqueo de oferta previas líderes en el sector para minimizar el tráfico no válido general y sofisticado (GIVT y SIVT) en sus campañas.

Puede establecer controles predeterminados de bloqueo de fraude de ofertas previas para cada anunciante<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->y, a continuación, opcionalmente [personalizar la configuración para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales al utilizar esta función.

Para obtener más información sobre la funcionalidad, póngase en contacto directamente con el proveedor preferido o con el equipo de cuenta de Adobe.

![Logotipo de Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo de DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo de Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logotipo de Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilidad de pujas previas {#pre-bid-viewability}

Filtros de visualización de ofertas previas impulsados por nuestros socios líderes del sector [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]), y [!DNL Integral Ad Science] permita a los anunciantes asegurarse de que sus campañas cumplan los objetivos de rendimiento de visibilidad deseados en todo el vídeo y muestre el inventario.

Puede establecer filtros de visibilidad predeterminados para cada anunciante<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->y, a continuación, opcionalmente [personalizar la configuración para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales al utilizar esta función.

![Logotipo de DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo de oracle Advertising](/help/dsp/assets/oracle-advertising-logo.png) ![Logotipo de Integral Ad Science](/help/dsp/assets/ias-logo.png)

### Segmentación de temas

DSP La segmentación de temas le permite segmentar o bloquear listas de palabras clave mediante el uso de socios contextuales líderes en el sector [!DNL Comscore] y [!DNL Oracle Data Cloud] ([!DNL Grapeshot]). La segmentación de temas le ayuda a garantizar que los anuncios se publiquen siempre en un entorno que se ajuste a su marca, ya sea bloqueando contenido perjudicial o asegurando un gasto en un contexto que garantice un mayor resultado.

El direccionamiento de temas requiere que cree segmentos de temas personalizados directamente con [!DNL Comscore] o [!DNL Grapeshot] (con [!DNL Oracle Data Cloud]). Una vez creados en la plataforma de socio, puede [segmentar o excluir un ID de segmento en la [!UICONTROL Audience Targeting] para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales para esta función.

Para crear segmentos de tema personalizados:

* Para crear un [!DNL Comscore] y crear segmentos personalizados, puede solicitar que se inicie sesión en [!DNL Activation Segment Manager] en [https://agents.comscore.com](https://agents.comscore.com). Consulte la [[!DNL Comscore] centro de ayuda](https://comscoreactivation.zendesk.com/hc/) para obtener instrucciones completas para configurar segmentos personalizados. Las tarifas para los segmentos personalizados se pueden ver en [!DNL Segment Manager] a medida que los crea.

* Para empezar con [!DNL Oracle Data Cloud], contacto [!DNL Oracle Data Cloud] o su equipo de cuenta de Adobe.

![Logotipo de Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo de Grapeshot](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP se ha asociado con el [!DNL DoubleVerify] para ofrecer sus [!DNL Authentic Brand Safety] solución de segmentación, que le permite crear un conjunto centralizado de requisitos de seguridad de marca para dirigirse a todas las plataformas de compra para mantener la coherencia.

Una vez que haya creado una [!DNL DoubleVerify] DSP segmento de seguridad de marca con el direccionamiento necesario, puede utilizarlo en para replicar las reglas de bloque posteriores a la oferta con ofertas previas en entornos web.

Puede especificar un [!DNL DoubleVerify] ID de segmento para cada anunciante<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->y, a continuación, opcionalmente [habilitar o deshabilitar [!UICONTROL Authentic Brand Safety] para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). DSP factura a su cuenta por el uso del ID de segmento.

Para obtener más información sobre la funcionalidad, póngase en contacto con [!DNL DoubleVerify] directamente o póngase en contacto con el equipo de cuenta de Adobe.

![Logotipo de DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
