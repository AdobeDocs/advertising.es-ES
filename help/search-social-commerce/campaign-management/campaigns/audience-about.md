---
title: Acerca de las audiencias
description: Obtenga información acerca de las opciones para rastrear, crear y administrar [!DNL Google Ads] y [!DNL Microsoft® Advertising] audiencias.
source-git-commit: 0b77c54ee9214021c841b4c1cca0b3439ea71f6f
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# Acerca de la administración [!DNL Google Ads] y [!DNL Microsoft® Advertising] audiencias en Search, Social y Commerce

*[!DNL Google Ads]y [!DNL Microsoft® Advertising] solamente*

La Biblioteca de audiencias enumera todas las [!DNL Google Ads] audiencias basadas en datos de clientes, en el mercado y similares, y su [!DNL Microsoft® Advertising] remarketing y remarketing dinámico, personalizado, coincidencia de clientes, en el mercado y audiencias similares. Puede utilizar cualquiera de las [!DNL Google Ads] audiencias como [!DNL Google Ads] objetivos y exclusiones a nivel de campaña y de grupo de publicidad, y puede utilizar cualquiera de los [!DNL Microsoft® Advertising] audiencias como [!DNL Microsoft® Advertising] objetivos y exclusiones a nivel de campaña y de grupo de publicidad (solo para audiencias de remarketing dinámico). Puede añadir o editar un ajuste de oferta para cualquier destinatario de audiencia.

También puede crear y administrar audiencias mediante segmentos o listas de correo electrónico de sus audiencias de Adobe Experience Cloud existentes y de varios tipos de datos de clientes de su sistema de administración de la relación con los clientes (CRM):

* **Segmentos de audiencia de Adobe:** Los anunciantes con cuentas de Adobe Audience Manager o Adobe Analytics pueden crear [!DNL Google Ads] audiencias de coincidencia de clientes de su [!DNL Adobe] segmentos:

   * (Anunciantes con [!DNL Analytics] cuentas que no tengan también Audience Manager) Puede crear lo siguiente: [!DNL Google Ads] audiencias de coincidencia de clientes con ID de usuario de [!DNL Analytics] segmentos que se comparten con Adobe Experience Cloud.

   * (Anunciantes con cuentas de Audience Manager) Puede crear lo siguiente [!DNL Google Ads] audiencias de coincidencia de clientes que usan ID de usuario de segmentos de Audience Manager que tienen como destino Search, Social y Commerce. Esto puede incluir segmentos de Adobe Analytics que se publican en Adobe Experience Cloud y segmentos creados con la biblioteca de audiencias de Adobe Experience Cloud.

  Para crear audiencias coincidentes con el cliente, el del anunciante [!DNL Google Ads] la cuenta debe ser [apto para coincidencia personalizada](https://support.google.com/adspolicy/answer/6299717) y se ha suscrito para [segmentos de ID de usuario](https://support.google.com/google-ads/answer/9199250). Además, la cuenta del anunciante en Buscar, Social y Comercio debe configurarse para permitir la creación de audiencias de coincidencia de clientes.<!-- For Analytics audiences: Analytics Only Integration. For Audience Manager, Enable CM/CRM option) -->

  [!DNL Adobe] los archivos de sincronización de cookies y datos de segmentos para las audiencias basadas en datos del cliente se sincronizan con [!DNL Google Ads] diariamente.

* **Listas de correo electrónico de Adobe Campaign:** El equipo de cuenta de Adobe puede ayudarle a configurar un flujo de trabajo para crear y actualizar una cuenta de [!DNL Google Ads] audiencia de coincidencia de clientes de una lista de correo electrónico en [!DNL Campaign].

* **Listas de datos de clientes:** Anunciantes con [!DNL Google Ads] o [!DNL Microsoft® Advertising] las cuentas de elegibles para la segmentación por lista de clientes pueden crear y actualizar una audiencia basada en datos de clientes específica de la red de publicidad &lt;!>— o audiencia de remarketing dinámico — incluida en la audiencia basada en datos del cliente, al menos durante [!DNL Google Ads]?—> cargando un archivo CSV con identificadores principales.

* **Listas de remarketing dinámico:** Anunciantes con [!DNL Microsoft® Advertising] Las cuentas de pueden crear y administrar audiencias de remarketing dinámico, que pueden utilizarse para redireccionar a clientes potenciales que hayan interactuado recientemente con sus productos de una o varias formas (como visualizadores de productos o compradores anteriores). Las audiencias de remarketing dinámico requieren que utilice la etiqueta de seguimiento de conversión y audiencia de JavaScript de la red de publicidad en sus páginas web. Utilice listas de remarketing dinámico con campañas de compra en las redes de búsqueda y audiencia para redireccionar las audiencias con anuncios de productos, así como con campañas de búsqueda para redireccionar las audiencias con anuncios de texto y anuncios dinámicos de búsqueda. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Los modificadores de oferta para los destinos de audiencia de remarketing dinámico no están optimizados en los portafolios con la etiqueta &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

>[!NOTE]
>
>Search, Social y Commerce no almacenan ninguno de los datos de clientes que carga o del [!DNL Adobe] segmentos utilizados para crear o editar un [!DNL Google Ads] o [!DNL Microsoft® Advertising] audiencia.

>[!MORELIKETHIS]
>
>* [Crear [!DNL Google Ads] audiencias de coincidencia de cliente de [!DNL Adobe] audiencias](google-audience-from-adobe-audience.md)
>* [Crear un [!DNL Google Ads] audiencia de customer match de una lista de correo electrónico de Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes](audience-from-customer-data-list.md)
>* [Administración de audiencias de remarketing dinámico](audience-dynamic-remarketing-manage.md)
>* [Administrar destinatarios de audiencia para campañas y grupos de anuncios](audience-targets-manage.md)
>* [Administración de exclusiones de audiencia para campañas y grupos de anuncios](audience-exclusions-manage.md)
