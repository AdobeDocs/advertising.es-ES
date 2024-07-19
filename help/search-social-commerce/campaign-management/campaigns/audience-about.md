---
title: Acerca de las audiencias
description: Obtenga información acerca de las opciones para rastrear, crear y administrar  [!DNL Google Ads] y [!DNL Microsoft Advertising] audiencias.
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Acerca de la administración de audiencias [!DNL Google Ads] y [!DNL Microsoft Advertising] en Search, Social y Commerce

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solamente*

La Biblioteca de audiencias enumera todas las audiencias basadas en datos de clientes de [!DNL Google Ads], del mercado y similares, así como las audiencias de remarketing y remarketing dinámico de [!DNL Microsoft Advertising], personalizadas, de coincidencia de clientes, del mercado y similares. Puede usar cualquiera de las audiencias de [!DNL Google Ads] como [!DNL Google Ads] destinos y exclusiones en los niveles de campaña y de grupo de anuncios, y puede usar cualquiera de las audiencias de [!DNL Microsoft Advertising] como [!DNL Microsoft Advertising] destinos en los niveles de campaña y de grupo de anuncios y exclusiones (solo para las audiencias de remarketing dinámico). Puede añadir o editar un ajuste de oferta para cualquier destinatario de audiencia.

También puede crear y administrar audiencias mediante segmentos o listas de correo electrónico de sus audiencias de Adobe Experience Cloud existentes y de varios tipos de datos de clientes de su sistema de administración de la relación con los clientes (CRM):

* **Segmentos de audiencia de Adobe:** Los anunciantes con cuentas de Adobe Audience Manager o Adobe Analytics predeterminadas pueden crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de sus [!DNL Adobe] segmentos:

   * (Anunciantes con cuentas de [!DNL Analytics] que no tengan Audience Manager) Puede crear audiencias de coincidencia de clientes de [!DNL Google Ads] con los identificadores de usuario de [!DNL Analytics] segmentos que se comparten con Adobe Experience Cloud.

   * (Anunciantes con cuentas de Audience Manager) Puede crear [!DNL Google Ads] audiencias de coincidencia de clientes usando los ID de usuario de segmentos de Audience Manager que tengan como destino Search, Social y Commerce. Esto puede incluir segmentos de Adobe Analytics que se publican en Adobe Experience Cloud y segmentos creados con la biblioteca de audiencias de Adobe Experience Cloud.

  Para crear audiencias que coincidan con el cliente, la cuenta del anunciante [!DNL Google Ads] debe ser [elegible para la coincidencia personalizada](https://support.google.com/adspolicy/answer/6299717) y optar por [segmentos de ID de usuario](https://support.google.com/google-ads/answer/9199250). Además, la cuenta del anunciante en Buscar, Social y Commerce debe configurarse para permitir la creación de audiencias de coincidencia de clientes.

  [!DNL Adobe] archivos de sincronización de cookies y datos de segmentos para audiencias basadas en datos de clientes se sincronizan diariamente con [!DNL Google Ads].

* **Listas de correo electrónico de Adobe Campaign:** El equipo de cuenta de Adobe puede ayudarle a configurar un flujo de trabajo para crear y actualizar una audiencia de coincidencia de cliente de [!DNL Google Ads] desde una lista de correo electrónico de [!DNL Campaign].

* **Listas de datos de clientes:** Los anunciantes con cuentas de [!DNL Google Ads] o [!DNL Microsoft Advertising] que cumplen los requisitos para la segmentación por lista de clientes pueden crear y actualizar una audiencia basada en datos de clientes específica de la red de anuncios &lt;!— o audiencia de remarketing dinámico — incluida en la audiencia basada en datos del cliente, al menos para [!DNL Google Ads]?—> al cargar un archivo CSV con identificadores principales.

* **Listas de remarketing dinámico:** Los anunciantes con cuentas de [!DNL Microsoft Advertising] pueden crear y administrar audiencias de remarketing dinámico, que puede usar para redirigirse a clientes potenciales que hayan interactuado recientemente con sus productos de una o varias formas (como visores de productos o compradores anteriores). Las audiencias de remarketing dinámico requieren que utilice la etiqueta de seguimiento de conversión y audiencia de JavaScript de la red de anuncios en sus páginas web. Utilice listas de remarketing dinámico con campañas de compra en las redes de búsqueda y audiencia para redireccionar las audiencias con anuncios de productos, así como con campañas de búsqueda para redireccionar las audiencias con anuncios de texto y anuncios dinámicos de búsqueda. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Los modificadores de oferta para los destinos de audiencia de remarketing dinámico no están optimizados en los portafolios con la configuración &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

>[!NOTE]
>
>Search, Social y Commerce no almacenan ninguno de los datos de clientes que subió o de los segmentos de [!DNL Adobe] utilizados para crear o editar una audiencia de [!DNL Google Ads] o [!DNL Microsoft Advertising].

>[!MORELIKETHIS]
>
>* [Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias](google-audience-from-adobe-audience.md)
>* [Crear una audiencia de  [!DNL Google Ads] customer match a partir de una lista de correo electrónico de Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes](audience-from-customer-data-list.md)
>* [Administrar audiencias de remarketing dinámico](audience-dynamic-remarketing-manage.md)
>* [Administrar destinatarios de audiencia para campañas y grupos de anuncios](audience-targets-manage.md)
>* [Administrar exclusiones de audiencia para campañas y grupos de anuncios](audience-exclusions-manage.md)
