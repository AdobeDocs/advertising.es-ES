---
title: Seguimiento de conversión mediante una fuente de ID de transacción
description: Obtenga información acerca del uso de una fuente de ID de transacción para los datos de seguimiento de conversión.
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Seguimiento de conversión mediante una fuente de ID de transacción

Cuando un anunciante tiene transacciones en línea y sin conexión, el Adobe Advertising puede rastrear las transacciones en línea a través del píxel de seguimiento de conversión de Adobe Advertising, y el anunciante puede rastrear las transacciones sin conexión mediante un ID de transacción y enviarlas a través de una fuente:

* Para las transacciones en línea, el Adobe Advertising rastrea los clics en los anuncios y las transacciones resultantes en el sitio web.

* El anunciante debe rastrear las conversiones sin conexión y enviar los archivos de fuente de nivel de transacción al Adobe Advertising.

## Resumen de implementación

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas [!DNL Adobe] y administrador de usuarios*

1. Utilice las opciones de seguimiento de cuenta o campaña &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot; para generar automáticamente una dirección URL de destino o una dirección URL final para cada palabra clave (para el seguimiento a nivel de palabra clave) o anuncio (para el seguimiento a nivel de anuncio) en la cuenta o campaña.

1. Configure el seguimiento de conversión de Adobe Advertising para las conversiones en línea. Este proceso es el mismo que para los anunciantes con seguimiento de conversión basado en píxeles de Adobe Advertising. Es importante generar etiquetas de conversión que incluyan un parámetro para un identificador de transacción único (`ev_transid=<transid>`).

1. Para la parte sin conexión de cada transacción, el anunciante genera el mismo ID de transacción que se utilizó en la parte en línea de la transacción para incluirlo en el archivo de fuente.

1. El anunciante carga un archivo con los [datos de conversión necesarios](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) en la ubicación designada del servidor.

1. Los servicios técnicos analizan los datos de conversión de los archivos cargados y, a continuación, cargan los datos en el Adobe Advertising. A continuación, el Adobe Advertising realiza un seguimiento de los datos con palabras clave, anuncios y ubicaciones individuales y crea previsiones de ingresos para cada uno.

1. Los servicios técnicos validan los datos procesados con los datos de las fuentes y comprueban si hay [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de archivo para archivos de fuentes de conversión](feed-file-requirements.md)
>* [Requisitos de datos para fuentes de datos que usan un ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
