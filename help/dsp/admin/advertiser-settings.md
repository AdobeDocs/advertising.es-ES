---
title: Configuración de cuenta del anunciante
description: Consulte las descripciones de la configuración de anunciante disponible.
role: User, Admin
source-git-commit: 1f8a76e060612cdcc8ee3709bdf49654faf31b57
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Configuración de cuenta del anunciante

*No disponible para usuarios de solo lectura*

<!-- Not published -->

## Configuración de [!UICONTROL General]

**[!UICONTROL Advertiser Name]:** El nombre del anunciante.

**[!UICONTROL Category]:** Categoría en la que opera el negocio del anunciante. La categoría se comunica a los editores cuando pujas por el inventario. Asegúrese de elegir una categoría que se ajuste a sus anuncios, ya que los editores podrían rechazarlos.

>[!NOTE]
>
>Si selecciona *[!UICONTROL Other]*, el anunciante no podrá obtener acceso a DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** Página principal del anunciante o URL del sitio web principal (a partir de `http://` o `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (solo para nuevas cuentas de anunciante) Hace que todas las fuentes de intercambio privadas configuradas para la cuenta de DSP de la organización estén disponibles para el anunciante.

### [!UICONTROL Adobe IMS IDs]

Los anunciantes con productos de Adobe Experience Cloud adicionales pueden compartir datos entre algunos productos mediante el ID único de la organización para Experience Cloud. Puede configurar integraciones de producto específicas en la sección [!UICONTROL Integrations].

**[!UICONTROL Account IMS org and ID]:** (Anunciantes con productos de Experience Cloud adicionales para los que se dispone de licencia a través de una cuenta de Experience Cloud con varios anunciantes; opcional) El identificador de organización de Experience Cloud del anunciante.

**[!UICONTROL Advertiser IMS org and ID]:** (Anunciantes con licencias directas para productos adicionales de Experience Cloud; opcional) El ID de organización de Experience Cloud del anunciante.

### [!UICONTROL Integrations]

(Opcional) Productos adicionales de Experience Cloud vinculados a la cuenta de DSP. Los productos deben estar asociados con el mismo ID de organización de Experience Cloud proporcionado en la sección [!UICONTROL Adobe IMS IDs].

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Anunciantes con [!DNL Advertising Search, Social, & Commerce] o que utilizan píxeles de conversión de Adobe Advertising) Una cuenta de [!DNL Search, Social, & Commerce] con la que DSP intercambia datos de atribución.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Anunciantes con Adobe Analytics; opcional; aplicable solo a los datos recopilados mediante etiquetas de seguimiento de conversión de Adobe Advertising que incluyen [!DNL EF Redirect] y solo token) Uno o más grupos de informes [!DNL Analytics] a los que DSP envía los datos que recopila de los editores y socios de suministro. Analytics también envía los datos que recopila del sitio del cliente a DSP.

Para que los datos aparezcan en los grupos de informes, se debe habilitar la configuración apropiada de nivel de anunciante [!DNL Search, Social, & Commerce]. Además, la cuenta [!DNL Analytics] del anunciante debe estar configurada para recibir datos de Adobe Advertising.

>[!WARNING]
>
>Si elimina un grupo de informes vinculado anteriormente, DSP ya no intercambia datos con ese grupo de informes. Es de esperar que se produzcan fluctuaciones de datos.

Para obtener más información acerca de la integración con [!DNL Analytics], vea &quot;[Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)&quot;.

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Anunciantes con Adobe Audience Manager o Adobe Analytics; opcional) Una cuenta de Audience Manager o [!DNL Analytics] desde la que DSP extrae metadatos de segmentos, datos de jerarquía y datos de audiencia única para todas las audiencias de Adobe del anunciante. Esto incluye datos para:

* Segmentos de Audience Manager
* [!DNL Analytics] segmentos publicados en Adobe Experience Cloud
* Segmentos creados con Adobe Experience Cloud [!DNL Audience Library]
* Segmentos creados en Adobe Experience Platform y enviados a Adobe Advertising mediante Audience Manager

La sincronización inicial dura unas 24 horas. Después, los datos se sincronizan en tiempo real, con un retraso de uno a dos segundos.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## Configuración de [!UICONTROL Targeting]

Si lo desea, puede configurar los destinos predeterminados para las nuevas ubicaciones del anunciante. Los usuarios pueden anular los destinos predeterminados de cualquier nueva ubicación.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** País predeterminado para el targeting geográfico de cada ubicación. Los usuarios pueden cambiar el país y configurar un targeting geográfico más específico para cada ubicación.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Cualquier audiencia o segmento que se va a suprimir de forma predeterminada. Los usuarios pueden cambiar las exclusiones de cada ubicación.

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

Tipos de filtros contextuales [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] y [!DNL Peer39] que aplicar. Puede anular la configuración de nivel de anunciante en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de contexto de inventario que se bloquearán de forma predeterminada. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Opcional) Uno o más tipos de atributos de inventario a destino de forma predeterminada. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de atributos de inventario para bloquear de forma predeterminada. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Opcional) Grado de contenido para adultos para el que se bloquearán los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (el valor predeterminado), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Alcohol Content]:** (Opcional) Grado de contenido alcohólico para el que se bloquearán los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (predeterminado), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Se pueden aplicar tarifas adicionales.

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

Tipos de sitios que se bloquearán según el tráfico fraudulento y las actividades sospechosas medidas a través de [!DNL DoubleVerify], [!DNL Integral Ad Science] y [!DNL Peer39]. Puede anular la configuración de nivel de anunciante en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** De forma predeterminada, bloquea todo el tráfico 100% no válido, incluido el tráfico en dispositivos secuestrados, para las nuevas ubicaciones. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Also block sites with]:** (Opcional) Un nivel adicional de fraude y tráfico no válido que hace que DSP bloquee los anuncios de forma predeterminada: *[!UICONTROL None]* (el valor predeterminado, que no bloquea el tráfico adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* o *[!UICONTROL >25% Average Fraud/IVT levels]*. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de fraude que hacen que DSP bloquee los anuncios de forma predeterminada: *[!UICONTROL Fraud]* (que bloquea todos los sitios con fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* o *[!UICONTROL Fraud: Zero Ads]*. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Tipo de actividad sospechosa en un sitio web o aplicación que hace que DSP bloquee los anuncios de forma predeterminada: *[!UICONTROL None]* (el valor predeterminado, que no bloquea los anuncios basándose en actividades sospechosas), *[!UICONTROL Suspicious Activity - High Risk]* o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Se pueden aplicar tarifas adicionales.

#### [!UICONTROL Pre-Bid Viewability]

Filtros de visibilidad de oferta previa opcionales de [!DNL DoubleVerify] y [!DNL Integral Ad Science] para aplicarlos a las ubicaciones. Los valores predeterminados de nivel de anunciante están seleccionados para nuevas ubicaciones. Puede anular la configuración de nivel de anunciante en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Vídeo

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average video viewability rate is]**. Con esta opción, seleccione los criterios.

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. Con esta opción, seleccione los criterios.

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average player size composition is]**. Con esta opción, seleccione los criterios.

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Mostrar

**&#x200B; **&#x200B;[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. Con esta opción, seleccione los criterios.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. Con esta opción, seleccione los criterios.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

Un filtro **[!UICONTROL Video Viewability Targets]** opcional y un filtro **[!UICONTROL Display Viewability Targets]** opcional. Se pueden aplicar tarifas adicionales.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** De forma predeterminada, qué nivel de [[!DNL Ads.txt] filtrado de ofertas previas](https://iabtechlab.com/ads-txt-about/) utilizar aprovechando la lista [!DNL Authorized Digital Sellers] de cada editor:
* *[!UICONTROL Opt out of ads.txt (default)]*: para comprar inventario a todos los vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: para priorizar la compra de inventario a los vendedores directos y revendedores autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar inventario solamente de vendedores y revendedores directos autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar inventario solamente de los vendedores directos autorizados de un dominio.

Puede anular la configuración de nivel de anunciante en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** De forma predeterminada, habilita un filtro posterior a la oferta en tiempo real para garantizar que los anuncios se publiquen en los sitios a los que se dirige el anunciante. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] solo clientes; opcional) Un ID de segmento [!DNL DoubleVerify Authentic Brand Safety] asociado a la cuenta [!DNL DoubleVerify] de la organización para usar de forma predeterminada en todas las ubicaciones. Especificar un ID bloquea las impresiones después de la oferta utilizando las reglas de seguridad de marca personalizadas configuradas para el ID de segmento especificado. DSP factura a su cuenta por el uso del ID de segmento.

El ID debe comenzar por &quot;51&quot; y constar de ocho dígitos. Puede cambiar o eliminar el ID de nivel de anunciante en el nivel de ubicación.

>[!MORELIKETHIS]
>
>* [Crear una cuenta de anunciante](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
