---
title: Requisitos de datos para fuentes de datos que utilizan un ID de transacción
description: Haga referencia a los requisitos de datos para las fuentes de datos mediante un ID de transacción.
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Requisitos de datos para fuentes de datos que utilizan un ID de transacción

A continuación se muestran los campos de encabezado y los campos de datos correspondientes necesarios para cada tipo de archivo de fuente.

>[!NOTE]
>* Los encabezados pueden estar en cualquier orden siempre que los datos de las filas siguientes sigan el mismo orden. Si no incluye un encabezado, el orden de las filas de datos debe ser coherente con cada archivo de fuente.
>* Cada línea del archivo de fuente debe contener datos para una transacción y la transacción debe identificarse con un ID de transacción.

| Nombre de campo/columna de encabezado | Tipo | Descripción |
| ---- | ---- | ---- |
| ID de transacción (ev_transid) | Cadena que distingue entre mayúsculas y minúsculas | El identificador generado por el anunciante asociado con la transacción. Dado que la etiqueta de seguimiento de conversión de Adobe Advertising se utiliza para las partes en línea de la transacción, debe ser el mismo que el ID de transacción (ev_transid) que el Adobe Advertising proporcionó para la parte anterior de la transacción. Esto significa que la etiqueta de conversión de la parte en línea de la transacción debe incluir una métrica de conversión para un ID de transacción único.<br><br>**Nota:** el Adobe Advertising usa el identificador para localizar los datos de transacciones antiguos y actualizarlos según un modo de inserción acordado (por ejemplo, para reemplazar los datos existentes o aumentarlos con los nuevos datos). |
| Fecha de transacción | DateTime | La fecha de la transacción. El formato debe ser coherente para cada transacción. |
| Conversión específica del cliente | Cadena | Una conversión de la que se está realizando un seguimiento (como el tipo de transacción o el importe). Analice las conversiones que se deben incluir con el equipo de implementación de Adobe Advertising antes de iniciar la fuente. |

## Ejemplo

El siguiente archivo de ejemplo incluye datos para dos métricas de conversión (Producto e Ingresos).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Requisitos de archivo para archivos de fuentes de conversión](feed-file-requirements.md)
>* [Seguimiento de conversión mediante una fuente de ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id.md)
