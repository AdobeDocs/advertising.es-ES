---
title: Administración de anuncios
description: Obtenga información acerca de los anuncios en Search, Social y Commerce, incluidos los tipos de anuncios disponibles.
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Acerca de los anuncios

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] y solo [!DNL Baidu] cuentas existentes*

Un anuncio se puede mostrar en un sitio web de destino (para contenido o campañas con objetivo de ubicación); cuando un usuario busca una de las palabras clave en el grupo de anuncios (para campañas de búsqueda) o contenido en el sitio web (anuncios dinámicos de búsqueda en [!DNL Google Ads] campañas de solo búsqueda); o cuando un usuario realiza una búsqueda relevante para uno de los elementos de la fuente de productos [!DNL Google Merchant Center] o [!DNL Microsoft Merchant Center] (anuncios de compra en [!DNL Google Ads] o anuncios de productos en [!DNL Microsoft Advertising] campañas).

## Tipos de publicidad disponibles

Puede crear y administrar tipos de anuncios admitidos para grupos de anuncios dentro de una cuenta sincronizada de red de anuncios:

* **Anuncios de texto o anuncios de texto expandidos** para un grupo de anuncios en una campaña dirigida a la red de búsqueda. Los anuncios de texto pueden incluir parámetros de seguimiento opcionales que anulan los parámetros de nivel de grupo de anuncios o de campaña. Según la red de anuncios, puede crear anuncios de texto expandidos/extendidos o anuncios de texto estándar.

* **anuncios de audiencia** nativos y entre dispositivos para [!DNL Microsoft Advertising] campañas en [!DNL Microsoft Audience Network]. Tiene dos opciones para los anuncios de audiencia, según la configuración de la campaña:

   * Si la campaña está vinculada a una tienda del centro de comerciantes, permita que la red de anuncios genere automáticamente anuncios basados en fuentes para la campaña, utilizando la información de producto de la tienda. No es necesario crear anuncios basados en fuentes para la campaña, pero debe crear grupos de anuncios con segmentación de usuarios.

   * Si la campaña no está vinculada a una cuenta de un centro comercial, cree anuncios de audiencia basados en imágenes utilizando el formato de anuncio interactivo, que incluye varios recursos de texto e imagen. La red de anuncios organiza los anuncios mediante las combinaciones más eficaces de elementos publicitarios y los muestra en sitios como [!DNL MSN], [!DNL Outlook.com] y [!DNL Microsoft Edge].

* **Anuncios de solo llamada** para [!DNL Google Ads] campañas en la red de búsqueda. Los anuncios de solo llamada son anuncios de texto que incluyen un número de teléfono. Opcionalmente, puede usar un número de reenvío asignado por [!DNL Google Ads] para el sistema de informes de llamadas avanzado.

* **Anuncios dinámicos de búsqueda expandidos** (ahora denominados solo &quot;anuncios dinámicos de búsqueda&quot; en las redes de anuncios) para [!DNL Google Ads] y [!DNL Microsoft Advertising] grupos de anuncios dinámicos de búsqueda en campañas de búsqueda. Los anuncios dinámicos de búsqueda utilizan contenido del sitio web, en lugar de palabras clave, para decidir cuándo mostrar los anuncios. La red de anuncios genera dinámicamente el titular, elige la dirección URL de la página de aterrizaje y la dirección URL de visualización y genera automáticamente la dirección URL final.

  Puede definir las páginas de los sitios web cuyo contenido se utiliza para segmentar los anuncios dinámicos de búsqueda configurando objetivos dinámicos de búsqueda específicos para el grupo de anuncios. Para [!DNL Google Ads], puede crear destinos de búsqueda dinámica en Buscar, Social y Commerce; para [!DNL Microsoft Advertising], debe crearlos en [!DNL Microsoft Advertising]. En [!DNL Google Ads] campañas, si lo desea, puede especificar un dominio de sitio web y un idioma en la sección &quot;[!DNL DSA Options]&quot; de la campaña en lugar de crear o además de crear destinos de búsqueda dinámica.

  Cuando el término de búsqueda de un usuario coincide exactamente con una palabra clave en una de sus campañas basadas en palabras clave, se muestra un anuncio de la campaña basada en palabras clave en lugar de un anuncio de búsqueda dinámica. La red de anuncios muestra un anuncio de búsqueda dinámica en lugar de un anuncio dirigido por palabras clave cuando el término de búsqueda del usuario coincide en gran medida con una de sus palabras clave y el anuncio de búsqueda dinámica tiene una clasificación de anuncio más alta.

  Para obtener más información sobre los anuncios dinámicos de búsqueda, consulte la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/2471185) y la [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Anuncios multimedia** para [!DNL Microsoft Advertising] campañas de búsqueda. Los anuncios multimedia son anuncios de imágenes de gran tamaño que se muestran en posiciones principales y laterales destacadas, y solo se muestra un anuncio multimedia por página. Pueden incluir varios recursos de texto e imagen, como anuncios interactivos, y la red de publicidad organiza los anuncios utilizando las combinaciones más efectivas de elementos publicitarios. Los anuncios multimedia no reemplazan las ubicaciones de anuncios de texto.

* Líneas de promoción para **[!DNL Microsoft Advertising]anuncios de productos (compras)** en la red de compras. Los anuncios de compra utilizan productos de la fuente de productos [!DNL Microsoft Merchant Center] existente, en lugar de palabras clave, para decidir cómo y dónde mostrar los anuncios. La copia de anuncio y las direcciones URL de la página de aterrizaje se generan automáticamente a partir de la información del producto en la fuente, pero también puede configurar líneas de promoción para incluirlas en el grupo de anuncios.

  Puede controlar qué productos se muestran con los anuncios de compra de [!DNL Microsoft Advertising] configurando grupos de productos independientes para el grupo de anuncios desde la vista [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

  Para obtener más información acerca del flujo de trabajo para anuncios de productos o compras, consulte &quot;[Implementar [!DNL Microsoft Advertising] campañas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot;.  Para obtener información adicional sobre anuncios de productos, consulte la [documentación de Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* Anuncios de búsqueda interactivos para [!DNL Google Ads] y [!DNL Microsoft Advertising] campañas en la red de búsqueda. La red de anuncios organiza dinámicamente anuncios de búsqueda adaptables basados en texto a partir de un conjunto de títulos y descripciones de anuncios, favoreciendo combinaciones que funcionan bien juntas. El anuncio incluye hasta tres titulares, dos descripciones y una URL personalizable desde la URL base y los campos opcionales ruta1 y ruta2. Si lo desea, puede anclar títulos de anuncios y descripciones a posiciones específicas.

>[!NOTE]
>
>[!DNL Google Ads] no proporciona datos fuera de sus editores nativos sobre las combinaciones de texto que se mostraron como anuncios. Para obtener más información sobre cómo generar informes para cada combinación de texto, consulte la [documentación de Google Ads](https://support.google.com/google-ads/answer/7684791).

## La vista [!UICONTROL Ads]

Puede crear, editar y cambiar el estado de las publicidades desde la vista [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads].

## Datos de rendimiento de nivel de anuncios

Los datos de nivel de anuncio están disponibles para la mayoría de los tipos de anuncio.

Sin embargo, no está disponible para [!DNL Google Ads] publicidad de búsqueda dinámica (DSA), rendimiento máximo, compras inteligentes y [!DNL YouTube] campañas. Se esperan discrepancias entre el total de datos de nivel de anuncio de una campaña y el total de datos de la campaña.

| Red de publicidad/Campaña/Tipo de publicidad | Disponibilidad de datos |
|---|---|
| [!DNL Google Ads] anuncio de búsqueda dinámica (DSA) | Campaña y grupo de publicidad |
| [!DNL Google Ads] rendimiento máximo | Campaign |
| [!DNL Google Ads] compras, compras inteligentes | Campaña y grupo de publicidad |
| [!DNL Google Ads] [!DNL YouTube] | Campaña y grupo de publicidad |

>[!MORELIKETHIS]
>
>* [Administrar anuncios](ad-manage.md)
