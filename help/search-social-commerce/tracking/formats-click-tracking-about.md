---
title: Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising
description: Obtenga información acerca de los formatos de seguimiento de clics para redes de publicidad admitidas.
exl-id: 12148caf-fde6-4ac2-b8b4-222409895dd7
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Acerca de los formatos de URL de seguimiento de clics para el servicio de seguimiento de conversión de Adobe Advertising

Las plantillas de seguimiento, los sufijos de la página de aterrizaje (sufijos finales de la URL) y las direcciones URL de destino para las cuentas de publicidad y las campañas que utilizan el servicio de seguimiento de conversión de Adobe Advertising tienen el siguiente formato:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

donde:

* `http://pixel.everesttech.net` redirige al usuario a los servidores de píxeles de Adobe Advertising.

* `<advertiser_ID>` es una variable para el ID de usuario único asignado al anunciante dentro del Adobe Advertising.

* `<token passing parameter>` es una variable para una de las siguientes opciones:

   * `cq?` o `rq` indica que la transferencia de tokens está habilitada.

   * `c?` o `r` indica que la transferencia de tokens está deshabilitada.

* `<ad network ID>` es una variable para el ID numérico de la red de publicidad especificada, como *3* para [!DNL Google Ads], *10* para [!DNL Microsoft Advertising], *45* para [!DNL Meta], *86* para [!DNL Yahoo! Display Network], *87* para [!DNL Naver], *88* para [!DNL Baidu], *90* para [!DNL Yandex], *94* para [!DNL Yahoo! Japan Ads], *105* para [!DNL Yahoo Native] (obsoleto), o *106* para [!DNL Pinterest] (obsoleto).

* `<tracking ID>` es una variable para una cadena de ID de seguimiento generada por el sistema que identifica una palabra clave, un anuncio o una ubicación que son únicos en la cuenta. La cadena varía según la red publicitaria.

* `<the landing page>` es una variable que representa la dirección URL del sitio a la que se dirige a los usuarios finales. Para cuentas con direcciones URL de destino, este valor es una dirección URL. Para cuentas con plantillas de seguimiento, este valor es un parámetro (como `{lpurl}`) que representa la dirección URL final.

Consulte las páginas independientes que indican la [[!DNL Baidu] formatos](formats-click-tracking-baidu.md), [[!DNL Google Ads] formatos](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formatos](formats-click-tracking-microsoft.md), [[!DNL Naver] formatos](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] formatos](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formatos](formats-click-tracking-yahoo-japan.md), y [[!DNL Yandex] formatos](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Formatos de rastreo de clics para anuncios patrocinados en [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Formatos de rastreo de clics para [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Formatos de rastreo de clics para [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Formatos de rastreo de clics para anuncios patrocinados en [!DNL Naver]](formats-click-tracking-naver.md)
>* [Formatos de rastreo de clics para anuncios patrocinados en [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Formatos de rastreo de clics para anuncios patrocinados en [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Formatos de rastreo de clics para anuncios patrocinados en [!DNL Yandex]](formats-click-tracking-yandex.md)
