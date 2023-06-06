---
title: Seguimiento de conversión mediante una fuente de ID de transacción
description: Obtenga información acerca del uso de una fuente de ID de transacción para los datos de seguimiento de conversión.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Seguimiento de conversión mediante una fuente de ID de transacción

Cuando un anunciante tiene transacciones en línea y sin conexión, la publicidad de Adobe puede rastrear las transacciones en línea a través del píxel de seguimiento de conversiones de la publicidad de Adobe, y el anunciante puede rastrear las transacciones sin conexión mediante un ID de transacción y enviarlas a través de una fuente:

* Para las transacciones en línea, Adobe Advertising rastrea los clics en sus anuncios y las transacciones resultantes en su sitio web.

* El anunciante debe rastrear las conversiones sin conexión y enviar archivos de fuentes de nivel de transacción a la publicidad de Adobe.

## Resumen de implementación

*Administrador de cuentas de agencia, [!DNL Adobe] administrador de cuentas y roles de usuario administrador solamente*

1. Utilice las opciones de cuenta o seguimiento de campaña &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot; para generar automáticamente una URL de destino o una URL final para cada palabra clave (para el seguimiento a nivel de palabra clave) o anuncio (para el seguimiento a nivel de anuncio) en la cuenta o campaña.

1. Configure el seguimiento de conversiones de Adobe Advertising para las conversiones en línea. Este proceso es el mismo que para los anunciantes con seguimiento de conversión basado en píxeles de la publicidad de Adobe. Es importante generar etiquetas de conversión que incluyan un parámetro para un ID de transacción único (`ev_transid=<transid>`).

1. Para la parte sin conexión de cada transacción, el anunciante genera el mismo ID de transacción que se utilizó en la parte en línea de la transacción para incluirlo en el archivo de fuente.

1. El anunciante carga un archivo con la variable [datos de conversión necesarios](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) a la ubicación designada del servidor.

1. Los servicios técnicos analizan los datos de conversión de los archivos cargados y, a continuación, cargan los datos en la publicidad de Adobe. A continuación, Adobe Advertising realiza un seguimiento de los datos utilizando palabras clave, anuncios y ubicaciones para cada uno, y crea previsiones de ingresos para cada uno de ellos.

1. Los servicios técnicos validan los datos procesados con los datos de las fuentes y comprueban la existencia de cualquier [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de archivo para archivos de fuentes de conversión](feed-file-requirements.md)
>* [Requisitos de datos para fuentes de datos que utilizan un ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

