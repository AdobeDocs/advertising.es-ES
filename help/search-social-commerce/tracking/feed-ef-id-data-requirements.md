---
title: Requisitos de datos para fuentes de datos que utilizan EF ID
description: Haga referencia a los requisitos de datos para fuentes de datos mediante EF ID.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Requisitos de datos para fuentes de datos que utilizan EF ID

A continuación se muestran los campos de encabezado y los campos de datos correspondientes necesarios para cada tipo de archivo de fuente.

>[!NOTE]
>* Los encabezados pueden estar en cualquier orden siempre que los datos de las filas siguientes sigan el mismo orden. Si no incluye un encabezado, el orden de las filas de datos debe ser coherente con cada archivo de fuente.
>* Cada línea del archivo de fuente debe contener datos para una transacción y la transacción debe identificarse con un ef_id (token) generado por la publicidad de Adobe.


| Nombre de campo/columna de encabezado | Tipo | Descripción |
| ---- | ---- | ---- |
| EF ID | Cadena que distingue entre mayúsculas y minúsculas | El ef_id (token) que capturó al hacer clic en la transacción, que consiste en el ID del internauta, la hora del clic y el tipo de red. No modifique el valor. |
| ID de transacción | Cadena que distingue entre mayúsculas y minúsculas | (Opcional, pero recomendada) El ID de transacción generado por el anunciante. Se recomienda incluir esto para cada transacción, aunque se utilice ef_id para rastrear la transacción en el momento del redireccionamiento. |
| Fecha de transacción | DateTime | La fecha de la transacción. El formato debe ser coherente para cada transacción. |
| Conversión específica del cliente | Cadena | Una conversión de la que se está realizando un seguimiento (como el tipo de transacción o el importe). Analice con el equipo de implementación de Adobe Advertising las conversiones que se deben incluir antes de iniciar la fuente. |

## Ejemplo

El siguiente archivo de ejemplo incluye datos para dos propiedades de transacción (Product e Revenue).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Requisitos de archivo para archivos de fuentes de conversión](feed-file-requirements.md)
>* [Seguimiento de conversión mediante una fuente de ID de EF](/help/search-social-commerce/tracking/feed-efid.md)

