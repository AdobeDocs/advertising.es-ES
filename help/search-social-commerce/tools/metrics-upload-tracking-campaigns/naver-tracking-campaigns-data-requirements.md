---
title: Requisitos de datos para métricas de conversión y tráfico para [!DNL Naver] cuentas solo de seguimiento
description: Consulte los requisitos de carga de datos para [!DNL Naver] cuentas solo de seguimiento.
exl-id: 6f79730b-f8d6-4a7f-9d31-f42fe63e6b5d
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Requisitos de datos de métricas para [!DNL Naver] cuentas solo de seguimiento

Los siguientes son los requisitos de datos para [!DNL Naver] métricas de tráfico y conversión para cuentas solo de seguimiento.

Los archivos de datos deben estar en formato TSV, CSV o TXT.

Los siguientes campos de encabezado son obligatorios y opcionales. Cada fila de datos debe incluir un valor agregado diario para al menos un campo de métrica.

| Nombre de campo/columna de encabezado | Tipo | Descripción |
| ---- | ---- | ---- |
| Periodo | DateTime | La fecha a la que se aplican los datos, con el formato `YYYY.MM.DD.` (como `2019.11.15.`, con un punto después del día). |
| Campaign | Cadena que distingue entre mayúsculas y minúsculas | Nombre de la campaña. |
| Adgroup (como una palabra) | Cadena que distingue entre mayúsculas y minúsculas | El nombre del grupo de publicidad. |
| Palabra clave | Cadena que distingue entre mayúsculas y minúsculas | (Anuncios por palabras clave) La palabra clave que generó el anuncio. |
| [Métrica] | Entero | (Opcional) El número de [cualquiera que sea la métrica que mida].</br><br>Las métricas estándar incluyen Impresiones, Coste y Clics. Puede incluir cualquier métrica adicional que desee de la red de publicidad. Incluya cada métrica en una columna independiente.<br><br><b>Notas:</b><ul><li>El encabezado de columna Costo debe ser &quot;Costo (KRW)&quot;.</li><li>Para incluir el coste (KRW) de los anuncios de marca, divida manualmente el coste mensual fijo por día en el nivel de grupo de anuncios.</li><li>Elimine todas las comas de los valores de métrica estándar. Por ejemplo, utilice 1000 en lugar de 1000.</li><li>Para valores nulos, utilice 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementación [!DNL Naver] cuentas solo de seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Apéndice: Datos de hojas de edición masiva requeridos para [!DNL Naver] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Cargar métricas de tráfico y conversión para [!DNL Naver] cuentas solo de seguimiento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
