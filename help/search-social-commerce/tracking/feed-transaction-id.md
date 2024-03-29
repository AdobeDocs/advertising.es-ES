---
title: Seguimiento de conversión mediante una fuente de ID de transacción
description: Obtenga información acerca del uso de una fuente de ID de transacción para los datos de seguimiento de conversión.
exl-id: 58f231a6-970b-46b4-824b-67b3d3f83051
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Seguimiento de conversión mediante una fuente de ID de transacción

Cuando un anunciante tiene transacciones en línea y sin conexión, el Adobe Advertising puede rastrear las transacciones en línea a través del píxel de seguimiento de conversión de Adobe Advertising, y el anunciante puede rastrear las transacciones sin conexión mediante un ID de transacción y enviarlas a través de una fuente:

* Para las transacciones en línea, el Adobe Advertising rastrea los clics en los anuncios y las transacciones resultantes en el sitio web.

* El anunciante debe rastrear las conversiones sin conexión y enviar los archivos de fuente de nivel de transacción al Adobe Advertising.

## Resumen de implementación

*Administrador de cuentas de agencia, [!DNL Adobe] administrador de cuentas y roles de usuario administrador solamente*

1. Utilice las opciones de cuenta o seguimiento de campaña &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot; para generar automáticamente una URL de destino o una URL final para cada palabra clave (para el seguimiento a nivel de palabra clave) o anuncio (para el seguimiento a nivel de anuncio) en la cuenta o campaña.

1. Configure el seguimiento de conversión de Adobe Advertising para las conversiones en línea. Este proceso es el mismo que para los anunciantes con seguimiento de conversión basado en píxeles de Adobe Advertising. Es importante generar etiquetas de conversión que incluyan un parámetro para un ID de transacción único (`ev_transid=<transid>`).

1. Para la parte sin conexión de cada transacción, el anunciante genera el mismo ID de transacción que se utilizó en la parte en línea de la transacción para incluirlo en el archivo de fuente.

1. El anunciante carga un archivo con la variable [datos de conversión necesarios](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) a la ubicación designada del servidor.

1. Los servicios técnicos analizan los datos de conversión de los archivos cargados y, a continuación, cargan los datos en el Adobe Advertising. A continuación, Adobe Advertising realiza un seguimiento de los datos con palabras clave, anuncios y ubicaciones individuales y crea una previsión de ingresos para cada uno.

1. Los servicios técnicos validan los datos procesados con los datos de las fuentes y comprueban la existencia de cualquier [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de archivo para archivos de fuentes de conversión](feed-file-requirements.md)
>* [Requisitos de datos para fuentes de datos que utilizan un ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
