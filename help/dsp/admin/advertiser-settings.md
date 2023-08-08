---
title: Configuración de cuenta del anunciante
description: Consulte las descripciones de la configuración de anunciante disponible.
role: User, Admin
source-git-commit: 201eb485e196dc0823dd6d592f67f62122c214b1
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Configuración de cuenta del anunciante

*No disponible para usuarios de solo lectura*

## [!UICONTROL General] Configuración

**[!UICONTROL Advertiser Name]:** El nombre del anunciante.

**[!UICONTROL Category]:** La categoría en la que opera el negocio del anunciante. La categoría se comunica a los editores cuando pujas por el inventario. Asegúrese de elegir una categoría que se ajuste a sus anuncios, ya que los editores podrían rechazarlos.

>[!NOTE]
>
>Si selecciona *[!UICONTROL Other]* DSP , el anunciante no podrá acceder a la información de la cuenta de usuario de la página de la página de [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** Página de inicio del anunciante o URL del sitio web principal (que comienza con `http://` o `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** DSP (Solo cuentas de anunciante nuevas) Hace que todas las fuentes de intercambio privadas configuradas para la cuenta de la organización estén disponibles para el anunciante.

### [!UICONTROL Adobe IMS IDs]

Los anunciantes con productos de Adobe Experience Cloud adicionales pueden compartir datos entre algunos productos mediante el ID único de la organización para Experience Cloud. Puede configurar integraciones de productos específicas en [!UICONTROL Integrations] sección.

**[!UICONTROL Account IMS org and ID]:** (Anunciantes con productos de Experience Cloud adicionales con licencia a través de una cuenta de Experience Cloud con varios anunciantes; opcional) El ID de organización de Experience Cloud del anunciante.

**[!UICONTROL Advertiser IMS org and ID]:** (Anunciantes con licencias directas para productos de Experience Cloud adicionales; opcional) El ID de organización de Experience Cloud del anunciante.

### [!UICONTROL Integrations]

(Opcional) Productos de Experience Cloud DSP adicionales vinculados a la cuenta de la. Los productos deben estar asociados con el mismo ID de organización de Experience Cloud proporcionado en la variable [!UICONTROL Adobe IMS IDs] sección.

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Anunciantes con [!DNL Advertising Search, Social, & Commerce] o que utilizan píxeles de conversión de Adobe Advertising) A [!DNL Search, Social, & Commerce] DSP cuenta con la que los intercambiarán datos de atribución.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Anunciantes con Adobe Analytics; opcional; aplicable solo a los datos recopilados mediante las etiquetas de seguimiento de conversión de Adobe Advertising que incluyen un [!DNL EF Redirect] y solo token) Uno o más [!DNL Analytics] DSP grupos de informes a los que los grupos de informes enviarán los datos que recopile de los editores y los socios de suministro. DSP Analytics también enviará los datos que recopila del sitio del cliente a la dirección de correo electrónico de la dirección de correo electrónico de la dirección de correo electrónico de la dirección de correo electrónico de la dirección de correo electrónico del cliente.

Para que los datos aparezcan en los grupos de informes, la variable [!DNL Search, Social, & Commerce] la configuración de nivel de anunciante debe estar habilitada. Además, el del anunciante [!DNL Analytics] La cuenta de debe estar configurada para recibir datos del Adobe Advertising de.

>[!WARNING]
>
>DSP Si elimina un grupo de informes enlazado anteriormente, ya no se intercambiarán datos con ese grupo de informes, ya no se podrá realizar el intercambio de datos con ese grupo de informes. Es de esperar que se produzcan fluctuaciones de datos.

Para obtener más información sobre la integración de con [!DNL Analytics], consulte &quot;[Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Anunciantes con Adobe Audience Manager o Adobe Analytics; opcional) Un Audience Manager o [!DNL Analytics] DSP cuenta desde la que los extraerán los metadatos del segmento, los datos de jerarquía y los datos de audiencia única para todas las audiencias de Adobe del anunciante. Esto incluye datos para:

* Segmentos de Audience Manager
* [!DNL Analytics] segmentos publicados en Adobe Experience Cloud
* Segmentos que se crean con Adobe Experience Cloud [!DNL Audience Library]
* Segmentos creados en Adobe Experience Platform y enviados al Adobe Advertising mediante un Audience Manager

La sincronización inicial dura unas 24 horas. Después, los datos se sincronizan en tiempo real, con un retraso de uno a dos segundos.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Configuración

Si lo desea, puede configurar los destinos predeterminados para las nuevas ubicaciones del anunciante. Los usuarios pueden anular los destinos predeterminados de cualquier nueva ubicación.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** El país predeterminado para el targeting geográfico de cada ubicación. Los usuarios pueden cambiar el país y configurar un targeting geográfico más específico para cada ubicación.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Audiencias o segmentos que se suprimirán de forma predeterminada. Los usuarios pueden cambiar las exclusiones de cada ubicación.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Tipos de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], y [!DNL Peer39] filtros contextuales para aplicar. Puede anular la configuración de nivel de anunciante en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de contexto de inventario que se bloquearán de forma predeterminada. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Opcional) Uno o más tipos de atributos de inventario que se van a asignar de forma predeterminada. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de atributos de inventario para bloquear de forma predeterminada. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Opcional) Grado de contenido para adultos para el que se bloquean los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (el valor predeterminado), *[!UICONTROL Standard]*, o *[!UICONTROL Strict]*. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Alcohol Content]:** (Opcional) Grado de contenido alcohólico para el que se bloquean los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (el valor predeterminado), *[!UICONTROL Standard]*, o *[!UICONTROL Strict]*. Se pueden aplicar tarifas adicionales.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Tipos de sitios que bloquear según el tráfico fraudulento y las actividades sospechosas medidas a través de [!DNL DoubleVerify], [!DNL Integral Ad Science], y [!DNL Peer39]. Puede anular la configuración de nivel de anunciante en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** De forma predeterminada, bloquea todo el tráfico 100 % inválido, incluido el tráfico en dispositivos secuestrados, para las nuevas ubicaciones. Se pueden aplicar tarifas adicionales.

**[!UICONTROL Also block sites with]:** DSP (Opcional) Un nivel adicional de fraude y tráfico no válido que hará que los anuncios se bloqueen de forma predeterminada por parte de los:  *[!UICONTROL None]* (el valor predeterminado, que no bloquea el tráfico adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, o *[!UICONTROL >25% Average Fraud/IVT levels]*. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** DSP (Opcional) Uno o más tipos de fraude que causarán que los anuncios se bloqueen de forma predeterminada de la manera más frecuente que se puede hacer: *[!UICONTROL Fraud]* (que bloquea todos los sitios con fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, y/o *[!UICONTROL Fraud: Zero Ads]*. Se pueden aplicar tarifas adicionales.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** DSP (Opcional) Un tipo de actividad sospechosa de un sitio web o una aplicación que hará que los usuarios bloqueen los anuncios de forma predeterminada: *[!UICONTROL None]* (el valor predeterminado, que no bloquea los anuncios en función de la actividad sospechosa), *[!UICONTROL Suspicious Activity - High Risk]*, o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Se pueden aplicar tarifas adicionales.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** De forma predeterminada, qué nivel de [[!DNL Ads.txt] filtrado previo a la oferta](https://iabtechlab.com/ads-txt-about/) para usar aprovechando el de cada editor [!DNL Authorized Digital Sellers] lista:
* *[!UICONTROL Opt out of ads.txt (default)]*: para comprar inventario a todos los vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: para priorizar la compra de inventario a los vendedores directos y revendedores autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar inventario solo de los vendedores y revendedores directos autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar inventario solo de los vendedores directos autorizados de un dominio.

Puede anular la configuración de nivel de anunciante en [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** De forma predeterminada, habilita un filtro posterior a la oferta en tiempo real para garantizar que los anuncios se publiquen en los sitios a los que se dirige el anunciante. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] solo para clientes; opcional) El ID del segmento de seguridad de marca asociado con el de la organización. [!DNL DoubleVerify] cuenta.

**[!UICONTROL Enable Authentic Brand Safety]:** (Opcional) De forma predeterminada, habilita [!DNL DoubleVerify] Seguridad de marca auténtica, que bloquea las impresiones después de la oferta utilizando las reglas de seguridad de marca personalizadas configuradas para el ID de segmento especificado. DSP factura a su cuenta por el uso del ID de segmento.

Puede anular la configuración de nivel de anunciante en el nivel de ubicación.

>[!MORELIKETHIS]
>
>* [Crear una cuenta de anunciante](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
