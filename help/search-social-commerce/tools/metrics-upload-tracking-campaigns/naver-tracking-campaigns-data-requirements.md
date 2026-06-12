---
title: Requisitos de datos para las métricas de tráfico y conversión de  [!DNL Naver] cuentas de solo seguimiento
description: Consulte los requisitos de carga de datos para  [!DNL Naver] cuentas de solo seguimiento.
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
TQID: https://experienceleague.adobe.com/e4n2ab469CRIiEmqq5wd97pXSQZ9Dt-tehqJSp125GU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 0%

---

# Requisitos de datos de métrica para [!DNL Naver] cuentas de solo seguimiento

A continuación se indican los requisitos de datos para las métricas de conversión y tráfico de [!DNL Naver] para las cuentas de solo seguimiento.

Los archivos de datos deben estar en formato TSV, CSV o TXT.

Los siguientes campos de encabezado son obligatorios y opcionales. Cada fila de datos debe incluir un valor agregado diario para al menos un campo de métrica.

| Nombre de campo/columna de encabezado | Tipo | Descripción |
| ---- | ---- | ---- |
| Periodo | DateTime | La fecha para la cual se aplican los datos, en el formato `YYYY.MM.DD.` (como `2019.11.15.`, con un punto después del día). |
| Campaign | Cadena que distingue entre mayúsculas y minúsculas | Nombre de la campaña. |
| Adgroup (como una palabra) | Cadena que distingue entre mayúsculas y minúsculas | El nombre del grupo de publicidad. |
| Palabra clave | Cadena que distingue entre mayúsculas y minúsculas | (Anuncios por palabras clave) La palabra clave que generó el anuncio. |
| [Métrica] | Entero | (Opcional) El número de [cualquiera que sea la métrica que mide].</br><br>Las métricas estándar incluyen Impresiones, Coste y Clics. Puede incluir cualquier métrica adicional que desee de la red de publicidad. Incluir cada métrica en una columna independiente.<br><br><b>Notas:</b><ul><li>El encabezado de columna Costo debe ser &quot;Costo (KRW)&quot;.</li><li>Para incluir el coste (KRW) de los anuncios de marca, divida manualmente el coste mensual fijo por día en el nivel de grupo de anuncios.</li><li>Elimine todas las comas de los valores de métrica estándar. Por ejemplo, utilice 1000 en lugar de 1000.</li><li>Para valores nulos, utilice 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Apéndice: datos de hoja de edición masiva requeridos para [!DNL Naver] cuentas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Cargar tráfico y métricas de conversión para [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
